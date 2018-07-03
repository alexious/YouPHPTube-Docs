===========
LDAP-Plugin
===========

.. toctree::

   ldap

Make sure you install the Lib php-ldap ``apt-get install php-ldap``

At a minimum, LDAP Plugin configuration you must have:

-  Server Field: Your LDAP server URL.
-  RDN Field: you must use the tag
    {$user}, it will be replaced by the user you will type on the login form. an example of a valid RDN may be `uid={`\ user},ou=Users,dc=youphptube,dc=com,dc=br\ ``or only the``\ {$user}\`

Also you may want to disable the regular login form and sign up form, to
do follow those steps:

1. Plugin Menu
2. CustomizedAdvanced Plugin
3. Check disableNativeSignUp
4. Check disableNativeSignIn
