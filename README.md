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


## Bringing up the Box

```bash
vagrant up
vagrant ssh
```

## Quick Commands

(Run these commands from inside the Vagrant box.)

DB state:

```bash
ldapsearch -D cn=Manager,dc=jacki3,dc=com -w password \
  "(objectclass=*)" -s children -b 'dc=jacki3,dc=com'
```
