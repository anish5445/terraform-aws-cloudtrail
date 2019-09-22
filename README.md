<!-- vim: set ft=markdown: -->
# terraform-aws-cloudtrail

#### Table of contents

1. [Overview](#overview)
2. [CloudTrail](#cloudtrail)
    * [Resources docs](#resources-docs)
    * [Inputs](#inputs)
    * [Outputs](#outputs)
    * [Examples](#examples)
3. [License](#license)

## Overview

This repository provides an automated framework for deploying and configuring AWS CloudTrail.

## CloudTrail

This module deploys an organisation-wide CloudTrail.

  - CloudTrail
  - S3 bucket with object locking
  - KMS keys

Terraform >= 0.12.0 is required for this module.

### Resources docs

AWS Config automation includes the use of the following core Terraform resources:

- [`aws_cloudtrail`](https://www.terraform.io/docs/providers/aws/r/aws_config_aggregate_authorization.html) - Manages an AWS Config Aggregate Authorization.

### Inputs

The below outlines the current parameters and defaults.

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
|client_name|Name of the organisation, used in the bucket name to ensure there are no conflicts|string|""|No|
|global_state_bucket|The name of the bucket containing the global module state|string|""|No|
|global_state_key|The key of the global module state as defined in the backend|string|""|No|
|global_state_region|The region of the bucket containing the global module state|string|""|No|
|global_state_profile|The profile to be used to access the global module state bucket|string|""|No|

### Outputs

Currently none.

### Examples

TODO.

## License

Apache 2.0.
