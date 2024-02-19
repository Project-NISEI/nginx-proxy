Simple nginx config that will look for any running docker instances with specific env variables and front for them.

The containers need to share a network to make this work.

Example env variables for a container.

```
VIRTUAL_HOST: $COBRA_DOMAIN
VIRTUAL_PORT: 3000
LETSENCRYPT_HOST: $COBRA_DOMAIN
LETSENCRYPT_EMAIL: website@nisei.net
```

`VIRTUAL_PORT` is what the application to serve is exposed on.

`LESTENCRYPT_HOST` and `LETSENCRYPT_EMAIL` are used to register and renew SSL certificates.
