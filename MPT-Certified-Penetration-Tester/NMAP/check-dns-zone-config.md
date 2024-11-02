# Use NMAP To Check DNS Zone Configuration Against Best Practices
DNS servers map domain names to IP addresses, allowing users to access websites with human-readable addresses. They are a common attack vector, often exploited for information on a target's infrastructure and subdomains during reconnaissance

## References
- [Script dns-check-zone](https://nmap.org/nsedoc/scripts/dns-check-zone.html) by Patrik Karlsson on Nmap.org


## Tasks
- Use NMAP to perform a DNS zone check scan on a DNS server


## Solutions With Scripts
1. To perform a DNS zone check scan on a DNS server, the IP address of a target DNS server is required
2. In Kali Linux, use nslookup on a target domain to output the authoritative DNS servers for eccouncil.org
   ```
   nslookup -type=ns eccouncil.org
   ```
3. To get the IP address of each server, use
   ```
   nslookup ns1.dnsprovider.com
   ```
4. Open Nmap and use the following command. Replace `example.com` with the domain name you are investigating and `TARGET_DNS_SERVER` with the server's IP address
   ```
   sudo nmap -sU -p 53 --script=dns-check-zone --script-args="dns-check-zone.domain=example.com" TARGET_DNS_SERVER
   ```
5.  
