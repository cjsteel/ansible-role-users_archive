# ansible-user-module-options.md

##  all possibilities options

```shell
append          : # optional - append groups.
comment         : # optional - description (GECOS) of user account.
createhome      : # defaults to 'yes'
expires         : # optional - expiry time for the user in epoch
force           : # optional - `userdel --force`, used with state=absent
generate_ssh_key: # NOT IMPLEMENTED defaults to 'no' - will not overwrite an existing SSH key
group           : # optional -  sets the user's primary group
groups          : # optional - When empty string ('groups='), user removed from all groups except primary group.
home            : # optional - sets users home directory
move_home       : # NOT IMPLETMENTED - used with home=, when yes trys to move user's home to specified dir. 
name            : # required - name of user.
non_unique      : # NOT IMPLEMENTED optional -  default: no - used with the -u option, allows non-unique UID
password        : # optional - set the user's password to this crypted value *(see link below).
passwordless_sudo : # optional
remove          : # NOT IMPLEMENTED - defaults to no - same as `userdel --remove` when used with `stat=absent`
seuser          : # NOT IMPLEMENTED - sets the seuser type (user_u) on selinux enabled system
shell           : # optional - default : /bin/bash, before 2.6 /usr/bin/false on OS X.
skeleton        : # NOT IMPLEMENTED - # optional - when used with create_home sets
                                                                 a home skel dir
ssh_key_bits      :# optional - default omit
ssh_key_comment   :# optional - default omit
ssh_key_file      :# optional - default omit
ssh_key_passphrase:# optional - default omit - if none provided defaults to none
ssh_key_type      :# NOT IMPLEMENTED - defaults to rsa

state           : # default to present
system          : # defaults to false
uid             : # optional
update_password : # optional
```

* for details see: http://docs.ansible.com/ansible/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module

