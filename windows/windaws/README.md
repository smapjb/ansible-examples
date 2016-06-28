
Windaws
----------------

This module contains some work in progress playbooks to set up windows 2012R2 servers
that are ansible ready. 

You will need to set your AWS environment variables
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY

And create a keypair in amazon using the aws_keygen.yml playbook

You will also need to create your own secret.yml using ansible vault to contain the variable
win_initial_password: password_goes_here

Once that is set up simply run
 

``` 
 ansible-playbook -i hosts aws_prov.yml -vvv --ask-vault-pass
```
