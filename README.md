# localstack-2-aws
Python framework to test AWS infra fully locally + deploy to cloud

# Requirements

1) If on macOS, install `homebrew` ( https://brew.sh/ )
2) Docker ( https://www.docker.com/products/docker-desktop/ )
3) Python 3.8* ( https://www.python.org/downloads/release/python-3815/ )
4) `pyenv` ( https://github.com/pyenv/pyenv#installation )
5) `aws cli` ( https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html )
6) `awslocal` ( ```pip install awscli-local``` )
7) `localstack` ( https://docs.localstack.cloud/getting-started/installation/ )
8) `terraform` ( https://developer.hashicorp.com/terraform/downloads?product_intent=terraform )

# Goal

The main goal here is to be able to test any combination of AWS services/workflow fully locally via localstack/docker, using python-boto3 syntax to create, invoke, and debug any AWS service.

The secondary goal ( WIP ) is to build in a way to comfortably and conventionally deploy the tested code/infrastructure to the cloud, be it off local or (preferrably) automated within a ci-pipeline in the pertinent repository.

The mechanics of this repo assume that you're already minimally familiar with AWS's python SDK Boto3, docker, and terraform.

# Show and tell

I will dive into details while I walk you through a simple use-case. After making sure that you've installed all the requirements listed above, continue with the followinng steps:

1) Clone this repo into a local directory of your choice.
2) Open a terminal and  `cd` into it
