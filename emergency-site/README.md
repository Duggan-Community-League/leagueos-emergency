# LeagueOS Emergency Site

This folder is the free-provider emergency static site lane.

Target host pattern:

- GitHub Pages or another free static provider
- deSEC warm standby DNS points emergency records here during break-glass
- Cloudflare remains primary during normal operations

## Files

- `public/index.html`: static emergency page
- `.nojekyll`: keeps GitHub Pages simple

## DNS Pattern

For GitHub Pages apex failover, deSEC can use:

```text
A mydcl.ca 185.199.108.153
A mydcl.ca 185.199.109.153
A mydcl.ca 185.199.110.153
A mydcl.ca 185.199.111.153
```

Only activate at the registrar during a controlled break-glass event.

