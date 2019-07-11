# udacity Cloud DevOps Engineer Nanodegree Program
# Infrastructure As A Code (IAC) Scripts
# By: Abid Malik
#
# CloudFormation Template Files
 1. network.template 
 2. servers.template
 3. s3-bucket.template
#
# Parameter Files
 1. network-parameters.json
 2. server-parameters.json

# Shell Scripts 
 1. create-stack.sh
 2. update-stack.sh
 3. validate-template.sh

### Deploying Cloudformation Scripts ###

# Create Network Infrastructure
 $ bash create-stack.sh network-stack network.template network-parameters.json

# Create Servers within Infrastructure 
 $ bash create-stack.sh server-stack servers.template server-parameters.json
 
# Updating Network Stack
$ bash update-stack.sh network-stack network.template network-parameters.json

# Updating Server Stack
$ bash update-stack.sh server-stack servers.template server-parameters.json

# Deleting Network Stack
$ aws cloudformation delete-stack --stack-name network-stack --region us-west-2

# Deleting Server Stack
$ aws cloudformation delete-stack --stack-name server-stack --region us-west-2


