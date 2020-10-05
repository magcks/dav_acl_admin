# CalDAV/CardDAV ACL Proof of Concept
This is a ready-to-use proof of concept for CalDAV and CardDAV ACL. This Javascript implementation is capable of adding and modifying ACL of calendar and addressbook collections. It is tested and working with the Cyrus HTTP module.

## Installation
Set up a nginx proxy in order to bypass cross origin policies.
```
location /davproxy {
	rewrite /davproxy/(.*) /$1  break;
	proxy_pass              https://your.cyrus.server.invalid;
}
```

And copy the index.html file to some directory at the same host.
