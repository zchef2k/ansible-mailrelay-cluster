# Ansible playbooks for setting up a highly available Postfix mail relay cluster

This may need more testing/modification for your environment.

My environment:

* 3 x ODROID-C2 SBCs running Fedora 43
* Postfix running in rootless Podman as a dedicated user via Quadlet
* Firewalld redirects traffic on port 25/tcp to the container high port (1025/tcp)
* Virtual IP created by Keepalived, health check included on each node
* Outgoing mail relayed through an upstream SMTP service

To-do:

* Replace shell commands with modules where available
* Improve documentation
* Refactor code, modules, etc.
* More testing
