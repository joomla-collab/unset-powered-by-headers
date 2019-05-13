# Unset X-Content-Powered-By headers
A quick trick for unsetting X-Content-Powered-By headers, which K2 and other extensions add, making those sites discoverable by malicious bots.

This is something I picked up from the Joomlaworks Github K2 repository. I'm always after useful tricks for obfuscating platform and version information to either prevent malicious bots from attempting automated attacks, or to fool them into using the wrong attack.

If you're using Apache (or .htaccess) add this:
```
Header always unset X-Content-Powered-By
```
If using nGinx:
```
proxy_hide_header X-Content-Powered-By;
```

Doing the above will remove X-Content-Powered-By headers that expose technology used on your site.
