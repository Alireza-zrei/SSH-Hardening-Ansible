# SSH Hardening Ansible Playbook

This repository contains an Ansible playbook designed to enhance the security of SSH services on target hosts. The playbook configures the SSH daemon (`sshd`) with recommended security settings, including secure key exchange algorithms, cipher suites, message authentication codes (MACs), and other best practices.

## Features

- Configures SSH daemon with secure defaults.
- Disables insecure protocols and ciphers.
- Implements system-wide cryptographic policies on Red Hat systems.
- Sets a session timeout to reduce the risk of unauthorized access.

## Requirements

- Ansible installed on the control node.
- Access to the target hosts via SSH.
- Root privileges on the target hosts for making configuration changes.

## Usage

1. Ensure Ansible is installed on your control node. If not, install it following the official documentation.

2. Clone this repository to your local machine or directly onto the control node where Ansible is installed.

3. Navigate to the directory containing the playbook.

4. Run the playbook against your target hosts. Replace `<your_target_hosts>` with the appropriate inventory file or host groups defined in your Ansible inventory.


5. The playbook will prompt for confirmation before making changes to the SSH configuration. Review the changes carefully.

## Prerequisites

- Ensure the target hosts have SSH installed and configured.
- It is recommended to back up the original `/etc/ssh/sshd_config` file before applying the changes.

## Post-Execution

After the playbook completes execution, review the SSH configuration to ensure it meets your organization's requirements. Test the SSH connectivity to verify that the changes do not disrupt legitimate access.

## Contributing

Contributions to improve the playbook are welcome. Please submit pull requests or issues through the GitHub interface.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.