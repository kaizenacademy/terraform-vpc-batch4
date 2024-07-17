# terraform-vpc-batch4

```hcl
module "batch4" {
    source = "kaizenacademy/batch4/vpc"
    version = "2.0.0"
    region = "us-east-2"
    vpc_cidr = "10.0.0.0/16"
    ip_on_launch = true
    port = [
        { from_port = 22, to_port = 22},
        { from_port = 80, to_port = 83}
    ]

    subnet = [
       { cidr = "10.0.1.0/24", subnet_name = "kaizen1" },
       { cidr = "10.0.2.0/24", subnet_name = "kaizen2" },
       { cidr = "10.0.3.0/24", subnet_name = "kaizen3" }
    ]
}
```