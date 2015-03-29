# secret-ingredient
Managing Chef secret ingredients since 2015.

Storing secrets in Chef has been notoriously difficult.  Encrypted databags require a psk (pre-shared key).  Chef-vault requires encoding N secrets for every new node and storing N copies of the encrypted results.

Secret-ingredient is a HTTP Restful dataservice which safely stores, provides management of, and restricts access to Chef secret ingredients.

A Chef secret ingredient is required for completion of certain Chef resources (data passed to a template, for example).

# features

* data encrypted on disk
* data managed via http api call (knife plugin anybody?)
* client authentication leverages chef server key infrastructure
* data access controlled by Acl
** data acl supports wildcards (maybe regex?)
* todo: native chef-client integration

# use cases

* as a user, i can manage secrets (create, read, update, delete) via http request
* as a node, i can read only those secrets I've been permitted to read
* as an admin, i rotate keys of encrypted data freely while the service is online

