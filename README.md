#Flora_Pac

This script generates a PAC file that helps you circumvent the [GFW](https://en.wikipedia.org/wiki/Great_Firewall).

## Mechanism

* `safeDomains` || `academicDomains` -> `DIRECT`
* `dangerDomains` -> `proxy`
* `safePorts` -> `DIRECT`
* dnsResolve(host)
  * failed -> `proxy`
  * in `fake_Ips` -> `proxy` 
  * in cn ip `list` -> `DIRECT`
* else -> `proxy`

## Usage

`./flora_pac -x [PROXY]`
e.g.
`./flora_pac -x 'SOCKS5 127.0.0.1:1080; SOCKS 127.0.0.1:1080;'`

## License

MIT
