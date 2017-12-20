# Pull and run Elastic stack 
1. Clone and cd into this repository directory.

2.
```
$ docker-compose up -d
```

3. Generate a JWT token using the debugger over at
   [https://jwt.io/](https://jwt.io/). The payload should at a minimum contain
   the issuer ("iss") and own home username ("x-proxy-user").

**Example payload**
```json
{
  "iss": "dkan_opendatastack_kibana",
  "x-proxy-user": "admin"
}
```

As a JWT secret, use the example key set in the docker-compose variable ("OPENDATASTACK_DKAN_CONSUMER_JWT_SECRET").

The proxy expects the JWT to be made available in a cookie named
`Drupal.visitor.jwt` by default, to change this behaviour you can set the
kongfig service env variable "OPENDATASTACK_DKAN_API_PLUGIN_JWT_COOKIE_NAMES"
to a different setting (cf.
https://github.com/OpenDataStack/kong-config/blob/master/opendatastack-kibana-jwt.js).
