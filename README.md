#flora_pac

This script generates a PAC file that helps circumventing the [GFW](https://en.wikipedia.org/wiki/Great_Firewall).

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

`./flora_pac`  
Use `flora_pac_lt.pac` for lantern, or `flora_pac_ss.pac` for shadowsocks.

## License

MIT
