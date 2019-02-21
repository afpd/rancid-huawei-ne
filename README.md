# rancid-huawei-ne
Rancid files to support Huawei NE series routers

Files are based on files from https://www.inet9.net/rancid-for-hp-h3c-huawei-switches/

Very non-elegant way to enable support:

1. Add lines below in to the file /etc/rancid/rancid.types.base
```
#huawei.
h3c;script;h3crancid
h3c;login;h3clogin
```

2. Put files h3clogin, h3crancid to the folder /usr/lib/rancid/bin

3. define Huawei NE router in router.db as 'h3c' type: 
```
mylocation-router2-core2.example.com;h3c;up
```

