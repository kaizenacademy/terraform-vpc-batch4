# terraform-vpc-batch4

```hcl
module "vpc" {
    source = "kaizenacademy/vpcbatch4/aws"
    region = "us-east-2"
    vpc_cidr = "10.0.0.0/16"
    ip_on_launch = true
    port = [22, 80, 443]

    subnet = [
       { cidr = "10.0.1.0/24", subnet_name = "kaizen1" },
       { cidr = "10.0.2.0/24", subnet_name = "kaizen2" },
       { cidr = "10.0.3.0/24", subnet_name = "kaizen3" }
    ]
}
```