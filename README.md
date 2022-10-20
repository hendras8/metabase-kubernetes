# metabase-kubernetes


This lua config on nginx.conf file for hide password from log nginx

```
map $request_body $obfuscated_request_body {
    "~(.*[{,]\\x22password\\x22:\\x22).*?(\\x22[,}].*)" $1********$2;
    default $request_body;
}
```

## Environment Variable

Many settings in Metabase can be viewed and modified in the Admin Panel, or set via environment variables. The environment variables always take precedence. Note that the environment variables won’t get written into the application database. You can see the environment variable at the following link
https://www.metabase.com/docs/latest/configuring-metabase/environment-variables
