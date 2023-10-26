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
2) Regardless of your system python-version, open a terminal and let's use pyenv to configure the latest 3.8.x for this specific shell, just to ensure that we can create a virtual environment with the most up-to-date stack: `cd` into the directory and run `pyenv install -l` (this command should list all the available versions, 3.8.16 at the time of writting)
3) Install the latest 3.8.16 `pyenv install 3.8.16` (may take some minutes)
4) Now let's use this version for the terminal `pyenv shell 3.8.16` and check that it's been indeed set -- `python --version` should return 3.8.16 now
5) Create a a virtual environment `python -m venv venv` and activate it `source venv/bin/activate`
6) Install requirements `python -m pip install -r dev-requirements.txt`
