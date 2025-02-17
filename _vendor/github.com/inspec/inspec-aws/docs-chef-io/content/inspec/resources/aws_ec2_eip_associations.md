+++
title = "aws_ec2_eip_associations Resource"
platform = "aws"
draft = false
gh_repo = "inspec-aws"

[menu.inspec]
title = "aws_ec2_eip_associations"
identifier = "inspec/resources/aws/aws_ec2_eip_associations Resource"
parent = "inspec/resources/aws"
+++

Use the `aws_ec2_eip_associations` InSpec audit resource to test properties of some or all AWS Elastic IP association.

This resource does not expect any parameters.

For additional information, including details on parameters and properties, see the [AWS documentation on AWS Elastic IP association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip-association.html).

## Installation

{{% inspec_aws_install %}}

## Syntax

Verify that the association exists.

```ruby
describe aws_ec2_eip_associations do
  it { should exist }
end
```

## Parameters

This resource does not require any parameters.

## Properties

`association_ids`
: The association ID for the address.

: **Field**: `association_id`

## Examples

**Check association ID is available.**

```ruby
describe aws_ec2_eip_associations do
   its('association_ids') { should include "ASSOCIATION_ID" }
end
```

## Matchers

This InSpec audit resource has the following special matchers. For a full list of available matchers, please visit our [Universal Matchers page](https://www.inspec.io/docs/reference/matchers/).

### exist

The control will pass if the describe returns at least one result.

Use `should` to test that the entity exists.

```ruby
describe aws_ec2_eip_associations do
  it { should exist }
end
```

Use `should_not` to test the entity does not exist.

```ruby
describe aws_ec2_eip_associations do
  it { should_not exist }
end
```

## AWS Permissions

{{% aws_permissions_principal action="EC2:Client:DescribeAddressesResult" %}}

You can find detailed documentation at [Actions, Resources, and Condition Keys for Amazon EC2](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazonec2.html).
