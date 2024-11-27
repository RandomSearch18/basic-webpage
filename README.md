# Basic webpage // USB-C is great // Constellation demo

## Deployment instructions

### Preparation

1. `git clone https://github.com/RandomSearch18/basic-webpage.git /srv/basic-webpage/`
2. `cd /srv/basic-webpage/`
3. `git checkout constellation`

### Deployment with Caddy

Example Caddyfile snippet to add to your own Caddyfile:

```caddyfile
star.slevel.xyz {
    root * /srv/basic-webpage/
    file_server
    header /api Content-Type application/json
}
```

Replace `/srv/basic-webpage/` with the path to the directory where you cloned the repository, and adjust the domain to some port on `localhost`, an IP address, or another domain as appropriate.

Then reload Caddy and you should be good to go.
