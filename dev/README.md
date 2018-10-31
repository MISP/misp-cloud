# building misp-cloud images

## AWS

To build your own Amazon Machine Image (AMI) on AWS you will need the [AWS Python SDK](https://aws.amazon.com/sdk-for-python/), [packer.io](https://packer.io/downloads.html) and its [amazon-ami-management plugin](https://github.com/wata727/packer-post-processor-amazon-ami-management)

Make sure you have your AWS credentials set up in `~/.aws` for example by using [`aws configure`](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)

After this you can build your own AWS MISP AMI by executing:
```
packer build \
        -var destination_regions=eu-west-1 \
        packer-aws.json
```
The AMI will show up in your [AWS Console](https://eu-west-1.console.aws.amazon.com/ec2/v2/home?region=eu-west-1) under IMAGES --> AMIs
