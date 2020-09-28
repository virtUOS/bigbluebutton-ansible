Ansible Scripts for BigBlueButton
=================================

This repository contains a set of scripts setting up and managing [BigBlueButton](https://bigbluebutton.org).
They are based on a set of [scripts by Sven](https://github.com/shaardie/video.haardiek.org). Thanks, Sven!


Important Notes
---------------

- The installation works on __Ubuntu 18.04 64bit__ since that is the operation system officially supported.
- The ansible vault in `group_vars/all/vault.yml` is meant as an example.
  The password is `123`.
  Reencode it using a proper password.
    - Make sure to generate new secrets and encrypt them in the ansible vault at `group_vars/all/vault.yml`.
      _Never_ use the vars set in here for production.
- The certificates provided in here are just dummy certificates and will only be deployed if no other certificates are in place.
  Once deployed, replace them with valid certificates and reload Nginx.


Initialization
--------------

### Greenlight on Ubuntu 16.04

```sh
# Execute and change the password
% docker exec greenlight-v2 bundle exec rake admin:create
```
