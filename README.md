# metabase-kubernetes


This lua config on nginx.conf file for hide password from log nginx

```
map $request_body $obfuscated_request_body {
    "~(.*[{,]\\x22password\\x22:\\x22).*?(\\x22[,}].*)" $1********$2;
    default $request_body;
}
```
