# ldap-server

I'm curious about running an LDAP server in my personal
environment, so I'm writing this Ansible playbook as a way to
play around with LDAP.

Right now, it just sets up an LDAP server (root password `password`)
and installs a single OU, user, group.

## To Do

- Make user sample object addition idempotent.
- Set password for the user.
- Configure TLS.
- Possibly place `ldap.conf`?
- Authenticate something against the LDAP server.
  Local login?
- Hashed password storage?
- Harden LDAP server.
