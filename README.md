# item-service

[![Build Status](https://travis-ci.com/vyomrastogi/item-service.svg?branch=master)](https://travis-ci.com/vyomrastogi/item-service)



### Issues Faced 
Travis encrypts key according to local copy branch, which was pointing to 'origin', whereas as the pushed branch is 'master'. 
Hence decryption of heroku key fails in travis

Solution : 
```
switch to master before encrypting the heroku key or 

travis encrypt -r vyomrastogi/item-service $(heroku auth:token) --add deploy.api_key

```
