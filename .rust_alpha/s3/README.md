# AWS SDK for Rust code examples for Amazon S3

## Purpose

These examples demonstrate how to perform several Amazon Simple Storage Service (Amazon S3) operations using the alpha version of the AWS SDK for Rust.

## Prerequisites

You must have an AWS account, and have configured your default credentials and AWS Region as described in [https://github.com/awslabs/aws-sdk-rust](https://github.com/awslabs/aws-sdk-rust).

## Running the code

### create-bucket

This example creates an Amazon S3 bucket.

`cargo run --bin create-bucket -- -b BUCKET [-d DEFAULT-REGION] [-v]`

- _BUCKET_ is the name of the bucket to create.
- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### delete-bucket

This example deletes an Amazon S3 bucket.

`cargo run --bin delete-bucket -- -b BUCKET [-d DEFAULT-REGION] [-v]`

- _BUCKET_ is the name of the bucket to delete.
- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### delete-object

This example deletes an object from an Amazon S3 bucket.

`cargo run --bin delete-object -- -b BUCKET -k KEY [-d DEFAULT-REGION] [-v]`

- _BUCKET_ is the name of the bucket.
- _KEY_ is the name of the object to delete.
- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### hello-world

This example lists your buckets in __us-east-2__, 
creates the bucket __aws-rust-sdk__ (you might have to change the name if anyone has already run this code example), 
adds __Cargo.toml__ to the bucket,
retrieves the object as a string, and displays it.

`cargo run --bin hello-world -- [-d DEFAULT-REGION] [-v]`

- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### list-buckets

This example lists your Amazon S3 buckets.

`cargo run --bin list-buckets -- [-d DEFAULT-REGION] [-v]`

- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### list-objects

This example lists the objects in an Amazon S3 bucket.

`cargo run --bin list-objects -- -b BUCKET [-d DEFAULT-REGION] [-v]`

- _BUCKET_ is the name of the bucket.
- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### put-object

This example adds an object (file) to an Amazon S3 bucket.

`cargo run --bin put-object -- -b BUCKET -k KEY [-d DEFAULT-REGION] [-v]`

- _BUCKET_ is the name of the bucket.
- _KEY_ is the name of the object (file).
- _DEFAULT-REGION_ is name of the AWS Region, such as __us-east-1__, where the table is located.
  If not supplied, uses the value of the __AWS_DEFAULT_REGION__ or __AWS_REGION__ environment variable.
  If the environment variable is not set, defaults to __us-west-2__.
- __-v__ displays additional information.

### Notes

- We recommend that you grant this code least privilege,
  or at most the minimum permissions required to perform the task.
  For more information, see
  [Grant Least Privilege](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege)
  in the AWS Identity and Access Management User Guide.
- This code has not been tested in all AWS Regions.
  Some AWS services are available only in specific
  [Regions](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services).
- Running this code might result in charges to your AWS account.

Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved. SPDX-License-Identifier: Apache-2.0