# DNS Information Gathering Tools
DNS information gathering refers to the process of collecting and analyzing data about registered domain names. The goal is to use DNS information gathering tools like 'whois', 'host', 'dig', 'nslookup' and online tools to gather information about domains

## References
- [DNS Information Gathering](https://securityonline.info/tutorial-nslookuphostdigwhois-dns-information-gathering/?cn-reloaded=1) by Securityonline.info


## Tasks
- Using the same target for all tools is allowed
- Use 'whois' to get DNS information. Use the provided 'Key Questions' to analyze the results.
  - Select a target domain name
  - Use 'whois' to retrieve information about the domain
  - Select a target public DNS server (eg: Google DNS, Cloudflare DNS)
  - Use 'whois' to retrieve information about the target public DNS server
  - For the target domain name, retrieve the domain name and its ID, registrant information (name, address, contact details), registrar information (name, address, contact details), registration dates and name servers from the 'whois' results.
    - When 'whois' is used to retrieve information for a domain name, in some cases, why is some information redacted? Are there other ways to recover that information?
    - What is the significance of the 'dnssec' field in the output?
    - For the target public DNS server, retrieve the organization information (name, address, contact details) and registration dates from the 'whois' results
- Use 'host' to retrieve DNS information about a target domain. Use the 'Key Questions' to analyze the results.
  - Select a target domain name of your choice
  - Use the host command along with the '-a' switch
  - Key Questions
    - What information can you infer from the header section of the output?
    - What information can you infer from the answer section of the output?
    - What information can you infer from other output sections?
- Use 'dig' to retrieve DNS information about a target domain. Use the 'Key Questions' to analyze the results.
  - Select a target domain. You can use the target you selected for the 'host' utility
  - Use the 'dig' command with TYPE set to 'any'
  - Key Questions
    - What are the various sections available in the output?
    - What can you infer from the information presented in each output section?
    - What similarities and differences can you observe between the results of using 'dig' with TYPE set to 'any', and 'host' with the 'a' switch?
- Use 'nslookup' to retrieve DNS information about a target domain. Use the 'Key Questions' to analyze the results.
  - Select a target domain. Use 'nslookup' with the following flags: -A, -AAAA, -CNAME, -HINFO, -MB, -MG, -MX, -NS, -PTR, -TXT
  - Execute separate commands with each flag
  - Key Questions
    - What information does each flag retrieve for a target domain?
- Use online tools to retrieve comprehensive information about target domains.
  - Select an online tool that provides DNS information
  - Select a target domain
  - Perform Reverse IP Lookup
  - View the IP history
  - View the DNS report
  - Perform Chinese firewall test
  - Perform Traceroute lookup
  - Perform DNS record lookup
  - Analysis Guidelines
    - Reverse IP lookup: What are all the domains hosted on this IP? If there is more than one domain, what does this indicate?
    - IP History: What are the different geographical regions (country names) in which the domain has been hosted in the past?
    - DNS report: What sensitive information can be revealed by the DNS report?
    - Chinese firewall test: What are the results of this test for the selected target? Why is it important to perform this test?
    - Traceroute lookup: Why is it required to perform a traceroute lookup? What can you infer from the traceroute results for the selected target?
    - DNS record lookup: What types of DNS records have been detected for the selected target?
- Write a report of the analysis in a PDF document
  - Include an 'Executive Summary'
  - Present each command executed
  - Provide answers to all the key questions, after using each tool
  - Provide answers (3 to 5 sentences) to the questions below:
    - How can the results presented by these tools contribute to a penetration testing engagement?
    - How can the results presented by these tools contribute to an OSINT engagement?
  - Include a suitable 'Conclusion' highlighting the outcome of using DNS information gathering tools


## Practical Approach
1. 



