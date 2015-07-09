#Flora_Pac

This script generates a PAC file that helps you circumvent the [GFW](https://en.wikipedia.org/wiki/Great_Firewall).

## Mechanism

* `costomSafeDomains` or `safeDomains` -> `DIRECT`
* `costomDangerDomains` or `dangerDomains` -> `proxy`
* `safePorts` -> `DIRECT`
* `dnsResolve(host)`
  * failed -> `proxy`
  * in `fakeIps` -> `proxy` 
  * in `cn_ip_list` -> `DIRECT`
* else -> `proxy`

## Usage

`./flora_pac -x [PROXY]`  
e.g.  
`./flora_pac -x 'SOCKS5 127.0.0.1:1080; SOCKS 127.0.0.1:1080;'`

## License

MIT
