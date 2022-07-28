# cd-promote-production


## Overview:

This project gives a basic demo of a blue-green deployment strategy on AWS leveraging cloudfront as a router for our deployment


## Prerequisites:
* Github repo
* AWS Account
* Circleci Account
* CloudFormation templates

### Getting started:

* fork this repo
* configure aws using `aws configure`
* create initial manually s3 called `my-bucket-<random characters>`
* upload a simple index.html file with a paragraph saying version1
* maually create an initial cloudfront stack `aws cloudformation deploy --template-file cloudfront.yml \
--stack-name production-distro --parameter-overrides PipelineID="${S3_BUCKET_NAME}" # Name of the S3 bucket you created manually. \
--tags project=udapeople &`
* setup circleci project
* push/commit code to github for full pipeline blue-green deployment



