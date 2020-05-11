# test22

## Usage
```
ubuntu@u1:/mnt/hgfs/Desktop/TF/terraform-course/test22/sol1$ ta

terraform destroy -auto-approve
terraform init
terraform apply -auto-approve
cat terraform.tfstate|grep public_ip|grep -v associate

aws_key_pair.mykey: Refreshing state... [id=mykey]
aws_key_pair.mykey: Destroying... [id=mykey]
aws_key_pair.mykey: Destruction complete after 0s

Destroy complete! Resources: 1 destroyed.

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
aws_key_pair.mykey: Creation complete after 1s [id=mykey]
aws_instance.example[0]: Creating...
aws_instance.example[0]: Still creating... [10s elapsed]
aws_instance.example[0]: Still creating... [20s elapsed]
aws_instance.example[0]: Still creating... [30s elapsed]
aws_instance.example[0]: Provisioning with 'file'...
aws_instance.example[0]: Still creating... [40s elapsed]
aws_instance.example[0]: Still creating... [50s elapsed]
aws_instance.example[0]: Still creating... [1m0s elapsed]
aws_instance.example[0]: Still creating... [1m10s elapsed]
aws_instance.example[0]: Still creating... [1m20s elapsed]
aws_instance.example[0]: Still creating... [1m30s elapsed]
aws_instance.example[0]: Still creating... [1m40s elapsed]
aws_instance.example[0]: Still creating... [1m50s elapsed]
aws_instance.example[0]: Still creating... [2m0s elapsed]
aws_instance.example[0]: Still creating... [2m10s elapsed]
aws_instance.example[0]: Still creating... [2m20s elapsed]
aws_instance.example[0]: Still creating... [2m30s elapsed]
aws_instance.example[0]: Still creating... [2m40s elapsed]
aws_instance.example[0]: Still creating... [2m50s elapsed]
aws_instance.example[0]: Still creating... [3m0s elapsed]
aws_instance.example[0]: Still creating... [3m10s elapsed]
aws_instance.example[0]: Still creating... [3m20s elapsed]
aws_instance.example[0]: Still creating... [3m30s elapsed]
aws_instance.example[0]: Still creating... [3m40s elapsed]
aws_instance.example[0]: Still creating... [3m50s elapsed]
aws_instance.example[0]: Still creating... [4m0s elapsed]
aws_instance.example[0]: Still creating... [4m10s elapsed]
aws_instance.example[0]: Still creating... [4m20s elapsed]
aws_instance.example[0]: Still creating... [4m30s elapsed]
aws_instance.example[0]: Still creating... [4m40s elapsed]
aws_instance.example[0]: Still creating... [4m50s elapsed]
aws_instance.example[0]: Still creating... [5m0s elapsed]
aws_instance.example[0]: Still creating... [5m10s elapsed]
aws_instance.example[0]: Still creating... [5m20s elapsed]
aws_instance.example[0]: Still creating... [5m30s elapsed]


Error: timeout - last error: SSH authentication failed (root@:22): ssh: handshake failed: ssh: unable to authenticate, attempted methods [none], no supported methods remain


            "public_ip": "52.194.205.177",

```
