# Installing and Configuring SELinux
## Install Packages:
On Red Hat-based systems (RHEL, CentOS, Fedora), use yum or dnf: `sudo yum install policycoreutils policycoreutils-python-utils selinux-policy selinux-policy-targeted`
On Debian/Ubuntu, use apt: `sudo apt install selinux-basics selinux-policy-default auditd`

## Check Status: Run `sestatus` to see if it's enabled and in what mode.

## Configure Mode:
Edit `/etc/selinux/config` (e.g., with vi).
Set `SELINUX=` to enforcing, permissive, or disabled.
Set `SELINUXTYPE=` to targeted (default) or mls.
Enforcing: Enforces policy, denies access.
Permissive: Logs denials but doesn't block (good for debugging).
Disabled: Turns SELinux off (not recommended).

Apply & Reboot:
For a permanent change, reboot the system after editing the config file.
