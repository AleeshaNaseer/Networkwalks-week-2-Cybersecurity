
# Networkwalks-week-2-Cybersecurity
Footprinting , Reconnaissance  and network scanning.


kali linux tools:

 Evidence Collected
Screenshots collected during the activities:
WHOIS
Screenshot showing the WHOIS command and output for the authorized domain
[whois.txt](https://github.com/user-attachments/files/34844018/whois.txt)
<img width="676" height="514" alt="WHOIS" src="https://github.com/user-attachments/assets/e5401499-b817-4e29-8ce4-a13a9fd103f7" />
┌──(kali㉿kali)-[~]
└─$ whois networkwalks.com
   Domain Name: NETWORKWALKS.COM
   Registry Domain ID: 2452319255_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.godaddy.com
   Registrar URL: http://www.godaddy.com
   Updated Date: 2025-11-12T10:08:43Z
   Creation Date: 2019-11-06T22:51:46Z
   Registry Expiry Date: 2027-11-06T22:51:46Z
   Registrar: GoDaddy.com, LLC
   Registrar IANA ID: 146
   Registrar Abuse Contact Email: abuse@godaddy.com
   Registrar Abuse Contact Phone: 480-624-2505
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Name Server: NS6135.HOSTGATOR.COM
   Name Server: NS6136.HOSTGATOR.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-11-14T00:17:18Z <<<
```[cite: 1]

Nslookup
Screenshot showing the Nslookup command and resolved IP address.

[ns lookup.txt](https://github.com/user-attachments/files/34844037/ns.lookup.txt)
<img width="247" height="142" alt="nslookup" src="https://github.com/user-attachments/assets/73327a71-42db-43eb-9622-36713cf1c0ee" />

┌──(kali㉿kali)-[~]
└─$ nslookup networkwalks.com
Server:         10.95.9.217
Address:        10.95.9.217#53

Non-authoritative answer:
Name:   networkwalks.com
Address: 192.232.216.135
Curl
Screenshot showing the Curl command and HTTP response headers.

[curl -I.txt](https://github.com/user-attachments/files/34844076/curl.-I.txt)
<img width="639" height="327" alt="curl -I" src="https://github.com/user-attachments/assets/c27a6818-2d6f-40b0-a867-5bf62b7e80f6" />
┌──(kali㉿kali)-[~]
└─$ curl -I https://networkwalks.com
HTTP/1.1 200 OK
Date: Sat, 14 Nov 2026 00:19:10 GMT
Server: Apache
Permissions-Policy: private-state-token-redemption=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com"), private-state-token-issuance=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com")
Link: <https://networkwalks.com/wp-json/>; rel="https://api.w.org/", <https://networkwalks.com/wp-json/wp/v2/pages/53>; rel="alternate"; title="JSON"; type="application/json", <https://networkwalks.com/>; rel=shortlink
Set-Cookie: __wpdm_client=f212706c003d9d0fe076ad7c0d3c6b73; path=/; domain=networkwalks.com; secure; HttpOnly
Referrer-Policy: no-referrer-when-downgrade
X-Endurance-Cache-Level: 0
X-nginx-cache: WordPress
Content-Type: text/html; charset=UTF-8

Wafw00f
Screenshot showing the Wafw00f command and detected WAF information.


[wafw00f.txt](https://github.com/user-attachments/files/34844046/wafw00f.txt)
<img width="580" height="435" alt="WAFWOOF" src="https://github.com/user-attachments/assets/1d23f2a7-e06d-49da-b10f-6575b9fc3017" />
<img width="620" height="261" alt="wafwoof networkwalks" src="https://github.com/user-attachments/assets/2b3406d3-8675-4936-926d-3457efbbeac7" />

┌──(kali㉿kali)-[~]
└─$ wafw00f networkwalks.com

                ?             ,.   (   .      )        .      "
                   ??        ("     )  )'     ,'        )  . (`     '`
   (___()’`;    ???        .; )  ' (( (" )    ;(,     ((  (  ;)  "  )" )
   /,____ /`              _"., ,._'_.,)_(..,( . )_  _' )_') (. _..( ' )
   \\    \\              |____|____|____|____|____|____|____|____|____|

                            ~ WAFW00F : v2.4.2 ~
              ~ Sniffing Web Application Firewalls since 2009 ~

[*] Checking https://networkwalks.com
[+] The site https://networkwalks.com is behind ModSecurity (SpiderLabs) WAF.
[~] Number of requests: 2








┌──(kali㉿kali)-[~]
└─$ wafw00f

               /‾‾‾‾‾\
              ( W00f! )
               \_____/
             ,,
          |`-.__   / /
          /"   _/ / /
         *====*  / /
        /     \ / /
  /|   /       V /
  \ \_/   /\    /
   \_____/  \  /
             \_\

                      404 Hack Not Found

                               \  /
                                \/     405 Not Allowed
                           403 Forbidden
                                /\
          502 Bad Gateway      /  \    500 Internal Error

                        ~ WAFW00F : v2.4.2 ~
         The Web Application Firewall Fingerprinting Toolkit

usage: wafw00f url1 [url2 [url3 ... ]]
example: wafw00f http://www.victim.org/

wafw00f: error: No test target specified.

┌──(kali㉿kali)-[~]
└─$ wafw00f networkwalks.com
DNSRecon
Screenshot showing the DNSRecon command and DNS-related results.
[dnsrecon -d.txt](https://github.com/user-attachments/files/34844059/dnsrecon.-d.txt)
<img width="619" height="408" alt="dnsrecon -d" src="https://github.com/user-attachments/assets/92059207-4b83-4646-bd23-01911a7f3e19" />
┌──(kali㉿kali)-[~]
└─$ dnsrecon -d networkwalks.com
2026-11-14T05:23:04.151404+0500 INFO Starting enumeration for domain: networkwalks.com
2026-11-14T05:23:04.153610+0500 INFO std: Performing General Enumeration against: networkwalks.com...
2026-11-14T05:23:05.192330+0500 ERROR No answer for DNSSEC query for networkwalks.com
2026-11-14T05:23:06.080656+0500 INFO      SOA ns6135.hostgator.com 50.87.144.87
2026-11-14T05:23:06.906299+0500 INFO      NS ns6135.hostgator.com 50.87.144.87
2026-11-14T05:23:07.936432+0500 INFO      Bind Version for 50.87.144.87 "9.16.23-RH"
2026-11-14T05:23:07.938074+0500 INFO      NS ns6136.hostgator.com 192.232.216.131
2026-11-14T05:23:09.101080+0500 INFO      Bind Version for 192.232.216.131 "9.16.23-RH"
2026-11-14T05:23:10.821874+0500 INFO      MX mail.networkwalks.com 192.232.216.135
2026-11-14T05:23:10.837931+0500 INFO      A networkwalks.com 192.232.216.135
2026-11-14T05:23:12.154829+0500 INFO      TXT networkwalks.com google-site-verification=rr04eRmqHoWY3XemnizDNVK4q75X-Ij-mjgEeg-UsYI
2026-11-14T05:23:12.155961+0500 INFO      TXT networkwalks.com v=spf1 +a +mx +ip4:50.87.144.87 +include:websitewelcome.com ~all
2026-11-14T05:23:13.073295+0500 INFO Enumerating SRV Records
Conclusion
During Week 2 – PM1 of my Cybersecurity & Ethical Hacking internship, I completed a practical website footprinting and reconnaissance exercise using multiple Kali Linux tools.

I used WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon to collect and analyze publicly available information about the authorized domain networkwalks.com.

Through this activity, I learned how different reconnaissance tools can be used to identify domain information, web technologies, IP addresses, HTTP information, WAF details and DNS records.

