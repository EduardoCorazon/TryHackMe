# DNS

# Domain Name System

assigns and connecters a websites IP address to a name. For example instead of typing 104.26.10.229 to google, you can type [tryhackme.com](http://tryhackme.com) .

## Domain Hierarchy

![Untitled](DNS%20595c3768f0a849c0b9660f7ec987015c/Untitled.png)

### Top-Level Domain (TLD)

Is the righthand part of the domain name (for ex. “.com”). There are two types of TLDs:

gTLD (Genetic Top Level) - Supposed to indicate the websites purpose, for ex “.gov” for government, “.edu” for education, etc

ccTLD (Country Code Top Level) - Supposed to use for geographical purposes, for ex “.ca” for Canada, “co.uk” for United Kingdom, etc

However demand has increased the use of TLDs, here’s a full list:

[https://data.iana.org/TLD/tlds-alpha-by-domain.txt](https://data.iana.org/TLD/tlds-alpha-by-domain.txt)

### Second-Level Domain

The left part of the domain name (before period), Limited to 63 characters including the TLD. It can’t start or end with hyphens or have consecutive hyphens, and can only use a-z and 0-9

“**tryhackme”**.com

### Subdomain

Located on the left side of the Second-level Domain with a period to separate it. Same restrictions as a Second-level Domain, can use multiple subdomains split with periods to create longer names. But the total length of everything must be less than 253 characters. No limit to number of subdomains.

**“admin.”**tryhackme.com

## Record Types

Most common Record Types:

- A Record - Resolve IPv4
- AAAA Record - Resolve IPv6
- CNAME Record - Resolve another domain name. For ex a website shop subdomain returns a CNAME record “shops.shopify.com”. So another DNS request would then be made to “shops.shopify.com” to work out the IP.
- MX Record - Resolve the address of the servers that handle email. For example, “alt1.aspmx.l.google.com”. Come with a priority flag indicating the order of the servers (if the main server dies, the email is sent to a backup server)
- TXT Record - Free text fields where any text data can be stored. Common uses are to list servers that have the authority to send an email on behalf of the domain (helps against spam and spoofed email). They can also verify ownership of the domain name when signing up for third party services.

All DNS records come with a TTL (Time to Live) value represented in seconds which is used for storing the DNS record locally until you have to look it up again. Cache saves on having to make a DNS request every time you communicate with a server.

## Making A Request

### Types of DNS Servers:

- Recursive DNS - provided by ISP but you can choose your own. Acts as a local cache of recently looked up domain names.
- Root DNS - Backbone of the internet, redirects you to the correct Top Level Domain server. For example “website.com”, the root server will refer you to the correct TLD server that deals with “.com”
- Authoritative DNS - Known as the nameserver for the domain, it stores DNS records for a particular domain name. A nameserver for a particular website will often have multiple nameservers for a domain name (This is for backup incase one server goes down)

### DNS Request

1. Pc checks local cache to see if address was looked up recently, if not a request to recursive DNS server is made
2. If a result is found locally this is send back to the PC (common for popular sites like google, Facebook, twitter). If the request isn’t found locally a request is sent to Root DNS
3. Redirects to correct TLD server
4. Finds the nameservers for the website
5. Depending on record type a DNS record is sent back to recursive DNS server where a local copy will be cached for future request and then relayed back to original client
    
    ![Untitled](DNS%20595c3768f0a849c0b9660f7ec987015c/Untitled%201.png)