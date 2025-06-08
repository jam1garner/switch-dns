# switch-dns

A splash page for a DNS server for blocking all DNS requests on the Switch. Hosted at [dns.jam1.re](https://dns.jam1.re)

## dnsmasq.conf

The DNS server uses the following configuration:

```
server=/ctest.p01.ctest.srv.nintendo.net/8.8.8.8
server=/ctest.cdn.nintendo.net/8.8.8.8

bogus-nxdomain=0.0.0.0
address=/#/0.0.0.0
```

Connection test URLs are forwarded to 8.8.8.8 (Google DNS), while everything else is "sinkholed" (given a bad IP address in the response).
