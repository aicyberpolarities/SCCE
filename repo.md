# Security Findings Report

## DISK_CMEK_DISABLED

### Description
Disks on this VM are not encrypted with customer-managed encryption keys (CMEK). With CMEK, keys that you create and manage in Cloud KMS wrap the keys that Google Cloud uses to encrypt your data, giving you more control over access to your data.

### Risk Statements
Without customer-managed encryption keys (CMEK) enabled on your Google Cloud disks, your organization lacks full control over the encryption keys protecting your sensitive data. This creates a significant security risk as you cannot independently manage key rotation, access, or revocation, potentially leading to unauthorized data access if Google's default encryption is compromised. In the event of a security incident, your ability to respond is limited since you cannot immediately revoke access by destroying the encryption keys. Additionally, this configuration may not meet compliance requirements for regulated industries that mandate customer control of encryption keys, potentially resulting in regulatory violations and penalties.

### Remediation Steps
1. Go to the Compute Engine disks page in the Google Cloud console
2. In the list of disks, click the name of the disk indicated in the finding
3. On the Manage disk page, click Delete
4. Create a new disk with CMEK enabled following the instructions to "Encrypt a new persistent disk with your own keys"
5. Note: CMEK incurs additional costs related to Cloud KMS