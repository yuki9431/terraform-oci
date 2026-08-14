# terraform-oci

OCI (Oracle Cloud Infrastructure) 向けの Terraform 構成とモジュール集。

| ディレクトリ | 内容 |
|---|---|
| [terraform_oci_web](./terraform_oci_web) | Web システムの基盤構成(ルートモジュール) |
| [terraform_oci_minimal_web](./terraform_oci_minimal_web) | ロードバランサと Web サーバの最小構成 |
| [terraform-oci-tdf-bastion-service](./terraform-oci-tdf-bastion-service) | Bastion service モジュール(非公式) |
| [terraform-oci-tdf-compute-instance](./terraform-oci-tdf-compute-instance) | Compute Instance モジュール([oracle-terraform-modules](https://github.com/oracle-terraform-modules/terraform-oci-tdf-compute-instance) の fork) |

## モジュール参照について

`terraform_oci_web` は同居する2つのモジュールを相対パスで参照している。

```hcl
# terraform_oci_web/oci_instances.tf
source = "../terraform-oci-tdf-compute-instance"
```

`oracle-terraform-modules/*` を参照している箇所は外部モジュールなので変更していない。

## Author

[Dillen H. Tomida](https://github.com/yuki9431)
