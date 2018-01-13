# AWS ASSOCIATED NOTES

## IAM

- **IAM** allows you to manage users and their level of access to the AWS console.

### Main Features

- IAM is **_global_**, no depends on region.
- **_Centralized_** control of your AWS account.
- **_Shared Access_** to your AWS control.
- **_Granular permissions_**.
- **_Identity Federation_** (including Active Directory, Facebook, LinkedIn, etc).
- **_MFA_** (Multi Factor Authentication.
- **_Provide temporary access_** for users/devices and services where necessary.
- Supports **_PCI DSS Compliance_** (Security standards).
- Supports **_password rotation Policies_**.
- Virtual/Hardware **_MFA_** device

### Main Concepts

- Users, End Users (think people).
- New Users have no permissions when first created but AWS assigned them an Access Key id and a Secret Access key.
- **Secret key** and **Access key** are visible only once. If the user loses them, the admin must regenerate them.
- **Groups** (A collection of users under one set of permissions).
- **Roles** (You create roles and can then assign them to AWS resources).

### Policies

**Policies** are documents that defines one or more permissions.

- Applied to users groups or roles individually.
- Written in JSON.
- Not depends on region.
- Has the followings Statements: Effect (whether the policy allows or denies access), Action (the list of actions that are allowed or denied by the policy), Resource (the list of resources on which the actions can occur), Condition (the circumstances under which the policy grants permissions).

```json
{
  "Version": "2017-10-17",
  "Statement": {
    "Effect": "Allow",
    "Action": "s3:ListBucket",
    "Resource": "arn:aws:s3:::example_bucket"
  }
}
```

### Exam notes

- **PowerUserAccess**: Provides full access to AWS Services and resources, but does not allow managements of Users and Groups.
