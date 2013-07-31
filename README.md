foolsCracker API
============

An API that tries 'ids' and 'passwords' in many authentication systems, such as Facebook, Twitter, etc. and tells you which of them succeded.
If you have one person's password of a site and this person REPEATS that password in another account, this API will help you cracking the fool ;)


###Get started with a simple use case

Suppose you want to try the username 'franco' (the __id__) and the __password__ 'password'. All you have to do is to do a GET to the API as:

      http://foolcracker.com/api?id=franco&pwd=password
      
The response you will get is a JSON object in the payload as:

      {
          id: franco,
          pwd: password,
          
          ans: [
              { facebook: 'OK' },
              { hotmail: 'FAIL' }
          ]
      }
      
      
###Application overview

As this is an application that involves the integration of many sites, we decided to use [mule](http://mulesoft.org) as the development tool.

