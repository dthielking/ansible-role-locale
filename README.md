Role Name
=========

This role configures your locale on your system.

Role Variables
--------------
```
locales_locale_conf:
  LANG: en_US.UTF-8
  LANGUAGE: en_US.UTF-8
  LC_CTYPE: en_US.UTF-8
  LC_ALL: en_US.UTF-8
```
If sufficient you can change the display defaults so that you get e.g German phone number styles. man locale.conf
```
locales_locale_gen:
  - en_US.UTF-8
  - en_US
```
Use this variable to setup your locales on your server. You can specify any locale which is available in _/etc/locale.gen_.

`locale_vconsole_keymap: us`
This variable is used to set your vconsole keymap.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: thielking.locale, locale_conf: |
           LANGUAG=en_us.UTF-8}

License
-------

MIT

