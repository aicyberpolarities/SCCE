INSTANCE_OS_LOGIN_DISABLED

Description:
OS Login is disabled on Google Cloud Platform instances. OS Login provides a more secure and manageable way to handle SSH access to your instances using IAM permissions.

Remediation Steps:
1. Go to the VM instances page in the Google Cloud console
2. Select the instance related to the Security Health Analytics finding
3. Click Edit
4. Under the Security section, enable OS Login
5. Click Save
6. Restart the instance for changes to take effect

Risk Statements:
When OS Login is disabled on Google Cloud Platform instances, organizations face increased security risks related to SSH key management and user access control. Without OS Login, SSH keys are managed manually at the instance level, which can lead to inconsistent access policies, outdated keys remaining active, and potential unauthorized access if keys are compromised. Additionally, disabling OS Login bypasses centralized IAM controls, making it difficult to enforce the principle of least privilege and maintain comprehensive audit trails of user access to compute instances. This configuration also complicates compliance with security standards that require centralized authentication and authorization mechanisms for cloud resources.