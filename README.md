# AWS Service Control Policies (SCP) Collection

This repository contains a curated set of AWS Service Control Policies (SCPs) designed to help organizations enforce security best practices and compliance across their AWS accounts. Each policy is provided as a standalone JSON file for easy integration into your AWS Organization.

## Repository Structure

Each folder/file in this repository represents a specific security control or restriction. Example policies include:

- **block_create_access_key**: Deny creation of access keys for the root user.
- **block_ebs_non_encrypt**: Prevent creation of unencrypted EBS volumes.
- **block_ec2_non_encrypt**: Prevent launching EC2 instances with unencrypted volumes.
- **block_leave_organization**: Prevent accounts from leaving the AWS Organization.
- **block_network**: Restrict network-related actions.
- **block_public_bucket**: Prevent creation of public S3 buckets.
- **block_rds_non_encrypt**: Prevent creation of unencrypted RDS instances.
- **block_regions**: Restrict usage of specific AWS regions.
- **block_root_create_access_key**: Deny root user from creating access keys.
- **block_s3_non_endpoint**: Enforce S3 access only via VPC endpoints.
- **block_vpc_access**: Restrict VPC access actions.

## Usage

1. **Review Policies**: Examine each JSON file to understand the restrictions and controls enforced.
2. **Customize as Needed**: Modify the policies to fit your organization's requirements (e.g., adjust resource ARNs, actions, or conditions).
3. **Deploy SCPs**: Use the AWS Organizations console or AWS CLI to attach these policies to your Organizational Units (OUs) or accounts.

### Example: Attaching an SCP via AWS CLI
```sh
aws organizations attach-policy --policy-id <policy-id> --target-id <account-or-ou-id>
```

## Contributing

Contributions are welcome! Please submit pull requests for new policies, improvements, or bug fixes. Ensure all policies follow AWS best practices and are valid JSON.
