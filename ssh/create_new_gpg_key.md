### Checking for existing GPG keys 
``gpg --list-secret-keys --keyid-format LONG`` 

### Generating a new GPG key
``gpg --full-generate-key`` 

``gpg --list-secret-keys --keyid-format LONG`` 

> gpg --list-secret-keys --keyid-format LONG 

> /Users/hubot/.gnupg/secring.gpg 

> ------------------------------------ 

> sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10] 

> uid                          Hubot  

> ssb   4096R/42B317FD4BA89E7A 2016-03-10 


``gpg --armor --export 3AA5C34371567BD2`` 

