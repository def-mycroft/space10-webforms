
# Working around issues with server files

Some of the files weren't available at urls that scripts were referencing.

Obvious answer is to try to run them locally, but there is a security issue
which browsers have that prevents referencing local js files. 

Here is the error I was getting:

```
from origin 'null' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'null' is therefore not allowed access.
```

In chrome, I disabled this by running command: 

```
chrome.exe --user-data-dir="C:/Chrome dev session" --disable-web-security
```

From [here][no access control]. This disables the security feature for 
development purposes

It is just a matter of running the page, looking at errors and using search
functions to repair issues.

[no access control]: https://stackoverflow.com/questions/20035101/no-access-control-allow-origin-header-is-present-on-the-requested-resource
