## Sol 1 한국 리즌 인스턴스 1개 생성

```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ echo $TF_VAR_AWS_REGION
ap_northeast-2
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ vi  ~/.bashrc
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ echo $TF_VAR_AWS_REGION
ap_northeast-2
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ export TF_VAR_AWS_REGION="ap-northeast-2"
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ echo $TF_VAR_AWS_REGION
ap-northeast-2
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ ta
```

## 인스턴스 생성
```
erraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
aws_instance.example: Creating...
aws_instance.example: Still creating... [10s elapsed]
aws_instance.example: Still creating... [20s elapsed]
aws_instance.example: Still creating... [30s elapsed]
aws_instance.example: Still creating... [40s elapsed]
aws_instance.example: Creation complete after 42s [id=i-0f7f28dc6c05b70a5]

Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
            "public_ip": "3.250.98.106",
```

## 인스턴스 삭제
```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ td
terraform destroy -auto-approve

aws_key_pair.mykey: Refreshing state... [id=mykey]
aws_instance.example[0]: Refreshing state... [id=i-0244f202e2dd8222b]
aws_instance.example[0]: Destroying... [id=i-0244f202e2dd8222b]
aws_instance.example[0]: Still destroying... [id=i-0244f202e2dd8222b, 10s elapsed]
aws_instance.example[0]: Still destroying... [id=i-0244f202e2dd8222b, 20s elapsed]
aws_instance.example[0]: Still destroying... [id=i-0244f202e2dd8222b, 30s elapsed]
aws_instance.example[0]: Destruction complete after 30s
aws_key_pair.mykey: Destroying... [id=mykey]
aws_key_pair.mykey: Destruction complete after 0s

Destroy complete! Resources: 2 destroyed.
```
