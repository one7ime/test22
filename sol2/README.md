## Sol 2 아일랜드 리즌 인스턴스 4개 생성

```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol2$ export TF_VAR_AWS_REGION="eu-west-1"

ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol2$ ta
```

##인스턴스 생성
```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol2$ ta

terraform destroy -auto-approve
terraform init
terraform apply -auto-approve
cat terraform.tfstate|grep public_ip|grep -v associate


Destroy complete! Resources: 0 destroyed.

Initializing the backend...

Initializing provider plugins...

The following providers do not have any version constraints in configuration,
so the latest version was installed.

To prevent automatic upgrades to new major versions that may contain breaking
changes, it is recommended to add version = "..." constraints to the
corresponding provider blocks in configuration, with the constraint strings
suggested below.

* provider.aws: version = "~> 2.60"

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
aws_key_pair.mykey: Creating...
aws_key_pair.mykey: Creation complete after 4s [id=mykey]
aws_instance.example[3]: Creating...
aws_instance.example[1]: Creating...
aws_instance.example[2]: Creating...
aws_instance.example[0]: Creating...
aws_instance.example[3]: Still creating... [10s elapsed]
aws_instance.example[1]: Still creating... [10s elapsed]
aws_instance.example[2]: Still creating... [10s elapsed]
aws_instance.example[0]: Still creating... [10s elapsed]
aws_instance.example[3]: Still creating... [20s elapsed]
aws_instance.example[1]: Still creating... [20s elapsed]
aws_instance.example[2]: Still creating... [20s elapsed]
aws_instance.example[0]: Still creating... [20s elapsed]
aws_instance.example[3]: Still creating... [30s elapsed]
aws_instance.example[1]: Still creating... [30s elapsed]
aws_instance.example[0]: Still creating... [30s elapsed]
aws_instance.example[2]: Still creating... [30s elapsed]
aws_instance.example[3]: Still creating... [40s elapsed]
aws_instance.example[1]: Still creating... [40s elapsed]
aws_instance.example[2]: Still creating... [40s elapsed]
aws_instance.example[0]: Still creating... [40s elapsed]
aws_instance.example[0]: Provisioning with 'file'...
aws_instance.example[2]: Provisioning with 'file'...
aws_instance.example[3]: Provisioning with 'file'...
aws_instance.example[1]: Provisioning with 'file'...
aws_instance.example[3]: Still creating... [50s elapsed]
aws_instance.example[1]: Still creating... [50s elapsed]
aws_instance.example[0]: Still creating... [50s elapsed]
aws_instance.example[2]: Still creating... [50s elapsed]
aws_instance.example[3]: Still creating... [1m0s elapsed]
aws_instance.example[1]: Still creating... [1m0s elapsed]
aws_instance.example[2]: Still creating... [1m0s elapsed]
aws_instance.example[0]: Still creating... [1m0s elapsed]
aws_instance.example[3]: Still creating... [1m10s elapsed]
aws_instance.example[1]: Still creating... [1m10s elapsed]
aws_instance.example[2]: Still creating... [1m10s elapsed]
aws_instance.example[0]: Still creating... [1m10s elapsed]
aws_instance.example[3]: Still creating... [1m20s elapsed]
aws_instance.example[0]: Still creating... [1m20s elapsed]
aws_instance.example[1]: Still creating... [1m20s elapsed]
aws_instance.example[2]: Still creating... [1m20s elapsed]
aws_instance.example[3]: Still creating... [1m30s elapsed]
aws_instance.example[0]: Still creating... [1m30s elapsed]
aws_instance.example[2]: Still creating... [1m30s elapsed]
aws_instance.example[1]: Still creating... [1m30s elapsed]
aws_instance.example[3]: Still creating... [1m40s elapsed]
aws_instance.example[0]: Still creating... [1m40s elapsed]
aws_instance.example[1]: Still creating... [1m40s elapsed]
aws_instance.example[2]: Still creating... [1m40s elapsed]
aws_instance.example[3]: Still creating... [1m50s elapsed]
aws_instance.example[0]: Still creating... [1m50s elapsed]
aws_instance.example[2]: Still creating... [1m50s elapsed]
aws_instance.example[1]: Still creating... [1m50s elapsed]
aws_instance.example[3]: Still creating... [2m0s elapsed]
aws_instance.example[1]: Still creating... [2m0s elapsed]
aws_instance.example[0]: Still creating... [2m0s elapsed]
aws_instance.example[2]: Still creating... [2m0s elapsed]
aws_instance.example[3]: Still creating... [2m10s elapsed]


            "public_ip": "34.249.32.205",
            "public_ip": "54.155.103.152",
            "public_ip": "34.244.11.124",
            "public_ip": "34.247.194.87",
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol2$
```


## 인스턴스 삭제
```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol2$ td
terraform destroy -auto-approve

aws_key_pair.mykey: Refreshing state... [id=mykey]
aws_instance.example[0]: Refreshing state... [id=i-03a4a9e304c19172e]
aws_instance.example[2]: Refreshing state... [id=i-05e8794f494e6fa27]
aws_instance.example[1]: Refreshing state... [id=i-086aba80eef2a8851]
aws_instance.example[3]: Refreshing state... [id=i-0cc8837f2dfdee17c]
aws_instance.example[1]: Destroying... [id=i-086aba80eef2a8851]
aws_instance.example[0]: Destroying... [id=i-03a4a9e304c19172e]
aws_instance.example[2]: Destroying... [id=i-05e8794f494e6fa27]
aws_instance.example[3]: Destroying... [id=i-0cc8837f2dfdee17c]
aws_instance.example[1]: Still destroying... [id=i-086aba80eef2a8851, 10s elapsed]
aws_instance.example[0]: Still destroying... [id=i-03a4a9e304c19172e, 10s elapsed]
aws_instance.example[2]: Still destroying... [id=i-05e8794f494e6fa27, 10s elapsed]
aws_instance.example[3]: Still destroying... [id=i-0cc8837f2dfdee17c, 10s elapsed]
aws_instance.example[1]: Still destroying... [id=i-086aba80eef2a8851, 20s elapsed]
aws_instance.example[0]: Still destroying... [id=i-03a4a9e304c19172e, 20s elapsed]
aws_instance.example[2]: Still destroying... [id=i-05e8794f494e6fa27, 20s elapsed]
aws_instance.example[3]: Still destroying... [id=i-0cc8837f2dfdee17c, 20s elapsed]
aws_instance.example[2]: Destruction complete after 26s
aws_instance.example[0]: Destruction complete after 26s
aws_instance.example[3]: Destruction complete after 26s
aws_instance.example[1]: Destruction complete after 26s
aws_key_pair.mykey: Destroying... [id=mykey]
aws_key_pair.mykey: Destruction complete after 2s

Destroy complete! Resources: 5 destroyed.
```
