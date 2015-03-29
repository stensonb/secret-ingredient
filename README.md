# secret-ingredient
Managing Chef secret ingredients since 2015.

Storing secrets in Chef has been notoriously difficult.  Encrypted databags require a psk (pre-shared key).  Chef-vault requires encoding secrets for every new node and storeN copies of the encrypted results.

Secret-ingredient is a HTTP Restful dataservice which safely stores, provides managemsent of, and restricts access to Chef secret ingredients.

