# Comprehensive Cybersecurity Reference Guide
## Hacker Tools, Techniques, and Defensive Countermeasures

**Last Updated:** 2025-01-14

---

## Table of Contents

1. [Anonymous Hackers: Collective Profile](#1-anonymous-hackers-collective-profile)
2. [Apache Hackers & Exploits](#2-apache-hackers--exploits)
3. [WordPress Hackers & Exploits](#3-wordpress-hackers--exploits)
4. [Headless Browsers](#4-headless-browsers)
5. [Operating Systems](#5-operating-systems)
6. [TOR & Anonymization](#6-tor--anonymization)
7. [Dark Web Tools](#7-dark-web-tools)
8. [Hacking Tools](#8-hacking-tools)
9. [Scraping Tools](#9-scraping-tools)
10. [Other Hacking Resources](#10-other-hacking-resources)
11. [Port Scanners](#11-port-scanners)
12. [Proxy & VPN Blocking](#12-proxy--vpn-blocking)
13. [Undetectable Browsers](#13-undetectable-browsers)
14. [Apache Blocking Rules](#14-apache-blocking-rules)

---

## 1. Anonymous Hackers: Collective Profile

### 1.1 Origins and History

**Anonymous** is not a traditional organization but a decentralized, leaderless collective of internet activists and hacktivists operating under a shared identity. The name originates from the default username assigned to users posting on imageboards like 4chan without registering.

| Timeline | Event |
|----------|-------|
| **2003** | Anonymous emerges from 4chan's /b/ board |
| **2008** | Project Chanology - First major operation against Church of Scientology |
| **2010** | Operation Payback - Support for WikiLeaks |
| **2011** | Arab Spring involvement - OpTunisia, OpEgypt |
| **2011** | HBGary Federal hack - Major corporate breach |
| **2012** | Operation Megaupload - Response to site takedown |
| **2015** | OpISIS/OpIceISIS - Campaign against terrorist propaganda |
| **2022** | OpRussia - Actions during Ukraine conflict |

### 1.2 Organizational Structure

Anonymous operates as a **"do-ocracy"** - leadership emerges through action rather than appointment:

- **No formal membership** - Anyone can claim Anonymous affiliation
- **Decentralized cells** - Independent groups coordinate loosely
- **IRC channels** - Historically used for coordination
- **Encrypted communications** - Telegram, Signal, Matrix
- **Splinter groups** - LulzSec, AntiSec, Ghost Squad Hackers

### 1.3 Ideology and Motivations

| Principle | Description |
|-----------|-------------|
| **Anti-censorship** | Opposition to internet restrictions |
| **Freedom of information** | Support for transparency and whistleblowers |
| **Anti-authoritarianism** | Challenging government and corporate power |
| **Social justice** | Targeting perceived oppressors |
| **Lulz** | Entertainment through chaos (early motivation) |

**Famous Slogans:**
> "We are Anonymous. We are Legion. We do not forgive. We do not forget. Expect us."

### 1.4 Tactics, Techniques, and Procedures (TTPs)

| Tactic | Description | Tools Used |
|--------|-------------|------------|
| **DDoS Attacks** | Overwhelm targets with traffic | LOIC, HOIC, Botnets |
| **SQL Injection** | Database exploitation | sqlmap, custom scripts |
| **Doxing** | Publishing private information | OSINT tools |
| **Website Defacement** | Replacing site content | Web shells, RCE exploits |
| **Data Exfiltration** | Stealing and leaking data | Various exploits |
| **Social Engineering** | Manipulating individuals | Phishing, pretexting |

### 1.5 Notable Operations

| Operation | Year | Target | Outcome |
|-----------|------|--------|---------|
| Project Chanology | 2008 | Scientology | Global protests, media attention |
| Operation Payback | 2010 | RIAA, MPAA, PayPal, Visa | DDoS attacks, arrests |
| OpTunisia | 2010-11 | Tunisian government | Support for Arab Spring |
| HBGary Federal | 2011 | Security firm | 70,000 emails leaked |
| OpDarknet | 2011 | Child exploitation sites | 1,500 accounts exposed |
| OpISIS | 2015+ | ISIS online presence | Thousands of accounts reported |

### 1.6 The Guy Fawkes Mask

The iconic mask from **V for Vendetta** became Anonymous's symbol:
- Represents rebellion against tyranny
- Provides anonymity at protests
- Became globally recognized protest symbol
- Licensed by Time Warner (ironic commercial element)

### 1.7 Legal Consequences

Many Anonymous participants have faced prosecution:
- **Hector Monsegur (Sabu)** - LulzSec leader, became FBI informant
- **Jeremy Hammond** - 10-year sentence for Stratfor hack
- **Barrett Brown** - 63 months for role in Stratfor leak
- **Multiple PayPal 14** - Arrests from Operation Payback

---

## 2. Apache Hackers & Exploits

### 2.1 Common Apache Vulnerabilities

| CVE | Vulnerability | Impact |
|-----|---------------|--------|
| CVE-2021-41773 | Path Traversal | Remote code execution |
| CVE-2021-42013 | Path Traversal (follow-up) | RCE on Apache 2.4.49-50 |
| CVE-2019-0211 | Privilege Escalation | Root access on shared hosting |
| CVE-2017-15715 | File Upload Bypass | Malicious file execution |
| CVE-2014-0226 | mod_status Race Condition | Heap buffer overflow |
| CVE-2021-44790 | mod_lua Buffer Overflow | Denial of service |

### 2.2 Apache Attack Vectors

**Directory Traversal Attacks:**
```
GET /cgi-bin/.%2e/.%2e/.%2e/.%2e/etc/passwd HTTP/1.1
GET /icons/.%%32%65/.%%32%65/.%%32%65/etc/passwd HTTP/1.1
```

**Server-Side Request Forgery (SSRF):**
```
GET /?url=http://169.254.169.254/latest/meta-data/ HTTP/1.1
```

**Apache Struts Exploits:**
- CVE-2017-5638 (Equifax breach vector)
- Remote code execution via Content-Type header

### 2.3 Apache Hacking Tools

| Tool | Purpose |
|------|---------|
| **Nikto** | Web server scanner |
| **Apache-users** | Username enumeration |
| **mod_security bypass** | WAF evasion techniques |
| **htaccess shell** | Malicious configuration injection |
| **Apache Killer** | DoS via Range header |

### 2.4 Apache Log Analysis Indicators

Signs of attack in Apache logs:
```
# Directory traversal attempts
"GET /..%2f..%2f..%2fetc/passwd"
"GET /.htaccess"
"GET /server-status"

# SQL injection attempts
"GET /page.php?id=1' OR '1'='1"
"GET /search?q=<script>"

# Scanner signatures
"Nikto" in User-Agent
"sqlmap" in User-Agent
"Nmap Scripting Engine"
```

### 2.5 Apache Hardening Recommendations

```apache
# Disable server signature
ServerSignature Off
ServerTokens Prod

# Disable directory listing
Options -Indexes

# Restrict HTTP methods
<LimitExcept GET POST HEAD>
    Deny from all
</LimitExcept>

# Prevent clickjacking
Header always set X-Frame-Options "SAMEORIGIN"

# Enable mod_security
SecRuleEngine On
```

---

## 3. WordPress Hackers & Exploits

### 3.1 WordPress Attack Statistics

- **90,000+** attacks per minute on WordPress sites globally
- **43%** of all websites run WordPress
- **Plugins** account for **98%** of WordPress vulnerabilities
- **Brute force** attacks are most common vector

### 3.2 Common WordPress Vulnerabilities

| Category | Examples |
|----------|----------|
| **Plugin Vulnerabilities** | File upload, SQLi, XSS in popular plugins |
| **Theme Vulnerabilities** | Backdoors, insecure file handling |
| **Core Vulnerabilities** | REST API issues, authentication bypasses |
| **XML-RPC Exploits** | Brute force amplification, DDoS |
| **wp-config.php Exposure** | Database credential theft |

### 3.3 WordPress Hacking Tools

| Tool | Purpose |
|------|---------|
| **WPScan** | WordPress vulnerability scanner |
| **wpseku** | Security scanner |
| **WPXStrike** | Automated exploitation |
| **CMSmap** | CMS vulnerability scanner |
| **Wordfence CLI** | Security analysis |
| **WP-CLI** | Command-line management (misuse) |

### 3.4 WordPress Attack Vectors

**XML-RPC Brute Force:**
```xml
POST /xmlrpc.php HTTP/1.1
<methodCall>
  <methodName>wp.getUsersBlogs</methodName>
  <params>
    <param><value>admin</value></param>
    <param><value>password123</value></param>
  </params>
</methodCall>
```

**REST API User Enumeration:**
```
GET /wp-json/wp/v2/users HTTP/1.1
GET /?author=1 HTTP/1.1
```

**SSRF via wp-json:**
```
GET /wp-json/oembed/1.0/proxy?url=http://internal-server/ HTTP/1.1
```

**Plugin Upload Exploits:**
```
# Arbitrary file upload in vulnerable plugins
POST /wp-admin/admin-ajax.php?action=upload_file
Content-Type: multipart/form-data
[malicious PHP file]
```

### 3.5 Notorious WordPress Malware

| Malware | Behavior |
|---------|----------|
| **WP-VCD** | Hidden admin users, backdoors |
| **Pharma Hack** | SEO spam injection |
| **Japanese Keyword Hack** | Foreign character spam |
| **Filesman** | File manager backdoor |
| **WSO Shell** | Web shell with GUI |
| **C99 Shell** | Advanced PHP backdoor |

### 3.6 WordPress Security Scanning

```bash
# WPScan usage
wpscan --url https://target.com --enumerate u,vp,vt,tt,cb,dbe

# Options:
# u  - enumerate users
# vp - vulnerable plugins
# vt - vulnerable themes
# tt - timthumbs
# cb - config backups
# dbe - database exports
```

### 3.7 WordPress Hardening

```php
// wp-config.php hardening
define('DISALLOW_FILE_EDIT', true);
define('DISALLOW_FILE_MODS', true);
define('WP_AUTO_UPDATE_CORE', true);
define('FORCE_SSL_ADMIN', true);

// Security keys (generate unique ones)
define('AUTH_KEY', 'unique-phrase-here');
define('SECURE_AUTH_KEY', 'unique-phrase-here');
```

```apache
# .htaccess WordPress protection
# Block wp-config.php
<files wp-config.php>
order allow,deny
deny from all
</files>

# Block XML-RPC
<files xmlrpc.php>
order deny,allow
deny from all
</files>

# Block wp-includes
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^wp-admin/includes/ - [F,L]
RewriteRule !^wp-includes/ - [S=3]
RewriteRule ^wp-includes/[^/]+\.php$ - [F,L]
RewriteRule ^wp-includes/js/tinymce/langs/.+\.php - [F,L]
RewriteRule ^wp-includes/theme-compat/ - [F,L]
</IfModule>
```

---

## 4. Headless Browsers

### 4.1 Common Headless Browser Identifiers

| Browser/Tool | Type |
|--------------|------|
| Headful | GUI Browser |
| Headless Client | Automation |
| Splash | Scraping Service |
| Headless Chrome | Chrome without GUI |
| Headless Firefox | Firefox without GUI |
| Headless Chromium | Chromium without GUI |
| Browserless | Cloud service |
| Browser-Use | Automation framework |
| HeadlessChrome/Linux | Linux variant |
| HeadlessChrome/Ubuntu | Ubuntu variant |

### 4.2 Automation Framework Patterns

```
selenium:headless:chromium
selenium:headful:chromium
selenium:headless:firefox
selenium:headful:firefox
playwright:headless:chromium
playwright:headful:chromium
playwright:headless:firefox
playwright:headful:firefox
```

### 4.3 Most Used Headless Browsers

| Tool | Language | Purpose |
|------|----------|---------|
| PlaywrightPython | Python | Browser automation |
| Selenium Stealth | Python | Anti-detection scraping |
| Splash/Lua | Lua | JavaScript rendering |
| HtmlUnit/Java | Java | Headless testing |
| Chromedp/Golang | Go | Chrome DevTools Protocol |
| Cypress/JavaScript | JavaScript | E2E testing |
| Nimble Browser | Various | Scraping |
| Puppeteer | JavaScript | Chrome automation |

### 4.4 Complete Headless Browser List

```
AngleSharp, Awesomium, benv, Browserjet, BrowserKit, browser-launcher, 
browser.rb, CasperJS, casperJS, cdp4j, Chrome PHP, Chromeless, 
Chrome-remote-interface, Chromium drivers, Chromium Embedded, Chromy, 
DalekJS, DamonJS, Erik, Geb, Ghostbuster, ghost.py, Grope, Guillotine, 
Headless Edge, Headless Firefox, HeadlessBrowser, Horseman, HtmlUnit, 
Jabba-Webkit, Jasmine-Headless-Webkit, Jaunt, jBrowserDriver, Jedi-crawler, 
Litium headless, Lotte, MechanicalSoup, mechanize, Nightmare, Node.js, 
PhantomJS, PhantomJsCloud, PhantomJS drivers, Phantompy, Playwright, 
Playwright-dotnet, Playwright-go, Playwright-python, Puppeteer, 
Puppeteer Sharp, Python-Webkit, RoboBrowser, Selenium, SlimerJS, 
SpecterJS, Splash Browser, Splinter, Spynner, SST, stanislaw, Surf, 
trifleJS, twill, WatiN, Watir, Watir-WebDriver, Webloop, Wendigo, 
wkhtmltopdf, WKZombie, X-RAY
```

---

## 5. Operating Systems

### 5.1 Security-Focused Distributions

| OS | Purpose |
|----|---------|
| **Kali Linux** | Penetration testing |
| **Parrot OS** | Security + Privacy |
| **BackBox** | Security assessment |
| **Dracos Linux** | Penetration testing |
| **DemonLinux** | Pen testing |
| **CAINE** | Digital forensics |
| **BlackArch** | Security research |
| **Samurai WTF** | Web testing |
| **NST** | Network security |

### 5.2 Privacy Operating Systems

| OS | Description |
|----|-------------|
| **Tails** | Amnesic live system |
| **Whonix** | Anonymous OS via Tor |
| **Qubes OS** | Security through isolation |

### 5.3 Other Unix-like Systems

```
FreeBSD, OpenBSD, Solaris, IRIX
```

---

## 6. TOR & Anonymization

### 6.1 TOR Components

| Component | Description |
|-----------|-------------|
| Tor2Web | Proxy to access .onion sites |
| TOR Browser | Modified Firefox for Tor |
| TOR Exit Nodes | Final hop in Tor circuit |
| OnionLinks | .onion directory |
| OnionLand | Tor search/directory |

### 6.2 Related Protocols

```
ssh, ssh-tunnel, ike, ipsec-esp
```

---

## 7. Dark Web Tools

### 7.1 Dark Web Search Engines

| Engine | Type |
|--------|------|
| Ahmia | Tor search engine |
| Torch | Dark web search |
| Haystack | Onion indexer |
| Wade X | Dark web search |
| Not Evil | Tor search (defunct) |
| DarkSearch | Dark web search |
| DeepSearch | Deep web search |

### 7.2 Other Dark Web Tools

```
Stagehand, lightpanda, Zombie.js, Freenet, Tails OS
```

---

## 8. Hacking Tools

### 8.1 Exploitation Frameworks

| Tool | Purpose |
|------|---------|
| Metasploit | Exploitation framework |
| Burp Suite | Web application testing |
| OWASP ZAP | Web vulnerability scanner |
| sqlmap | SQL injection automation |
| Nikto | Web server scanner |

### 8.2 Network Scanning

| Tool | Purpose |
|------|---------|
| Nmap | Network mapper |
| Wireshark | Packet analyzer |
| Angry IP Scanner | IP scanner |
| Zenmap | Nmap GUI |
| Masscan | High-speed scanner |
| Unicornscan | Network scanner |

### 8.3 Vulnerability Scanners

```
Tenable Nessus, OpenVAS, OPENVASVT, Acunetix, QualysGuard, 
GFI LanGuard, Nexpose, Greenbone CE
```

### 8.4 Password Crackers

| Tool | Purpose |
|------|---------|
| Hashcat | GPU password cracking |
| John the Ripper | Password cracker |
| Hydra | Online brute force |

### 8.5 Directory/File Discovery

```
Gobuster, Dirsearch, FeroxBuster, DIRB, ffuf, dirbuster
```

### 8.6 Wireless Tools

```
Aircrack-ng, Hping
```

### 8.7 Other Offensive Tools

```
Tcpdump, Snort, Netcat, Superscan, Xenotix XSS Exploit Framework, 
SpiderFoot, Wapiti, WPXStrike, Octopus Scanner, Gitpaste-12, 
Reverse Shell, StormCrawler, GoSpider, nuclei, wpscan
```

---

## 9. Scraping Tools

### 9.1 Programming Languages

```
ASM, C#, C, C++, COBOL, Elixir, Go, Java, JavaScript, Kotlin, 
Lua, Perl, Python, Ruby, Rust, R, Haskell, Scala, Dart
```

### 9.2 HTTP Libraries & Clients

| Library | Language |
|---------|----------|
| Requests | Python |
| httpx | Python |
| urllib | Python |
| cURL | Multi-language |
| Axios | JavaScript |
| Node Fetch | JavaScript |
| OkHttp | Java/Kotlin |
| Jsoup | Java |
| libcurl | C/C++ |

### 9.3 Scraping Frameworks

```
Scrapy, Scrapy Splash, BeautifulSoup (implied), MechanicalSoup, 
Selenium, SeleniumBase, Playwright, Puppeteer, Pyppeteer, 
Cheerio, Colly, gocolly, Geziyor, Botasaurus, AutoScraper, 
Goutte PHP, Panther PHP, Roach PHP, Watir
```

### 9.4 Anti-Detection Tools

```
Selenium Stealth, Undetected ChromeDriver, Cloudscraper, 
Imperva bypass, Incapsula bypass, Curl_cffi, Botright, 
Hrequests, CreepJS, Nodriver
```

### 9.5 Scraper Signatures

```
Web Scraper, Image Scraper, Content Crawler, Data Scraper, 
Proxy Scraper, Instant Data Scraper, HTML Scraper, 
webscraper.py, scraper.py, Boilerpipe, HTMLFetcher
```

---

## 10. Other Hacking Resources

### 10.1 HTTP Client Libraries

```
4D_HTTP_Client, android-async-http, axios, akka-http, attohttpc, 
CakePHP, fasthttp, HTTPing, http.rb, Java-http-client, Jodd HTTP, 
Laminas_Http_Client, libsoup, lua-resty-http, nghttp2, phpscraper, 
scalaj-http, Unirest, Httparty
```

### 10.2 Browser Extensions (Security Research)

```
HackBar, Wappalyzer, Cache killer, Open port check tool, 
Request maker, Proxy SwitchyOmega, Note anywhere, d3coder, 
Tamper Data
```

### 10.3 Multi-Login Browsers

```
GoLogin, MoreLogin, MultiLogin, Incogniton, Dataskrapa, Dolphin
```

### 10.4 Fingerprinting

```
JA3 Fingerprint, JA3S, JA3 Realism, JA3 Fingerprinting, JARM, 
HTTP/2 fingerprint, TLS Fingerprinting, Request Header Fingerprint, 
JavaScript fingerprint
```

### 10.5 OSINT & Reconnaissance

```
Shodan, Censys, ZoomEye, GreyNoise, Hunter, Crt.sh, searchcode.com
```

### 10.6 Exploitation Tools

```
Invicti, WebInspect, Netsparker, Intruder, LiveAction, 
Metasploitable 2, meterpreter, SQLNinja, EyeWitness, 
Webscreenshot, lazys3, Nuclei
```

---

## 11. Port Scanners

### 11.1 Dangerous Port Scanner Patterns

```apache
RewriteCond %{HTTP_USER_AGENT} "^Noxious/Nuisible/вредоносный Host$" [NC]
```

### 11.2 Scan Types

| Scan Type | Description |
|-----------|-------------|
| ACK Scan | Firewall rule detection |
| Null Scan | Stealthy port detection |
| FIN Scan | Firewall evasion |
| TCP SYN Scan | Half-open scanning |
| TCP Connect Scan | Full connection |
| UDP Scanning | UDP port discovery |
| Xmas Scan | FIN+PSH+URG flags |

### 11.3 Port Scanning Tools

```
Advanced IP Scanner, Angry IP Scanner, NetCat, Nmap, Masscan
```

---

## 12. Proxy & VPN Blocking

### 12.1 Proxy Types to Block

```
AI proxy, API Proxy, HTTP Proxies, forward proxy, Server proxies, 
residential proxies, reverse proxy, proxy request, http-proxy, 
IPv4 Proxies, IPv6 Proxies, Mobile Proxies, Virgin proxies, 
Proxy Servers, sproxies, Static ISP Proxies, ISP Proxies
```

### 12.2 VPN Indicators

```
VPN, VPN/Proxy, SeaMonkey
```

---

## 13. Undetectable Browsers

### 13.1 Anti-Detection Patterns

```
Chromedriver, undetected\chromedriver, Chrome\Undetectable, 
Edge\Undetectable, Undetectable\Browser, undetectable-fingerprint-browser, 
Firefox/User-Agent Switcher, PhantomJsCloud, Quark, MALNJS, 
RV:10 UBrowser, SM-J111F
```

---

## 14. Apache Blocking Rules

### 14.1 Basic RewriteRule Syntax

```apache
<IfModule mod_rewrite.c>
RewriteCond %{HTTP_USER_AGENT} (pattern1|pattern2|pattern3) [NC]
RewriteRule (.*) - [F,L]
</IfModule>
```

### 14.2 Alternative Blocking Method

```apache
<IfModule mod_rewrite.c>
RewriteCond %{HTTP_USER_AGENT} "(PLACE THE RAW FILE HERE)" [NC]
RewriteRule "^.*$" - [F]
</IfModule>
```

### 14.3 Comprehensive Blocking Rules

```apache
<IfModule mod_rewrite.c>
RewriteEngine On

# Block Headless Browsers
RewriteCond %{HTTP_USER_AGENT} (Headful|Headless\ Client|Headless|Headless\ Chromium|HeadlessChrome|Headless\ Edge|HeadlessChrome/Linux|HeadlessChrome/Ubuntu|Browserless|Browser-Use|Firefox\ Headless|Headless\ Linux|selenium:headless|playwright:headless|PlaywrightPython|Selenium\ Stealth|Splash/Lua|HtmlUnit/Java|Chromedp|Cypress|browserless|gologin) [NC,OR]

# Block Security Tools
RewriteCond %{HTTP_USER_AGENT} (Metasploit|Kali\ Linux|Parrot\ Security\ OS|BlackArch\ Linux|BackBox\ Linux|ZAP|OSV-Scanner|sqlmap|WPXStrike|hydra|Octopus\ Scanner|Angry\ IP\ Scanner|Burp\ Suite|Wireshark|Reverse\ Shell|Hashcat|Metasploit|Hydra|QualysGuard|Acunetix|SpiderFoot|Wapiti|Nmap|Zenmap|Masscan|Nessus|OpenVAS|OWASP\ ZAP|Netcat|Aircrack-ng|Nikto|Gobuster|Dirsearch|FeroxBuster|Nexpose|StormCrawler|GoSpider) [NC,OR]

# Block Scraping Tools
RewriteCond %{HTTP_USER_AGENT} (Scrapy|SeleniumBase|Cloudscraper|Undetected\ ChromeDriver|Selenium\ Stealth|Botright|MechanicalSoup|Jsoup|AutoScraper|Httpx|ChromeDriver|Pyppeteer|Cheerio|Botasaurus|Puppeteer|Selenium|got-scraping|Scraper\ API|Web\ Scraper|Data\ Scraper|HTML\ Scraper) [NC,OR]

# Block WordPress Attack Tools
RewriteCond %{HTTP_USER_AGENT} (WPScan|wpscan|WPXStrike|WordPress\ Security\ Scan|wp-scan) [NC,OR]

# Block Tor and Anonymization
RewriteCond %{HTTP_USER_AGENT} (TOR\ browser|tor|TOR|Tor2Web|OnionLinks|OnionLand|Tails\ OS|Freenet|I2P) [NC,OR]

# Block Proxy Indicators
RewriteCond %{HTTP_USER_AGENT} (AI\ proxy|API\ Proxy|HTTP\ Proxies|forward\ proxy|residential\ proxies|reverse\ proxy|http-proxy|Proxy\ Servers|VPN/Proxy|VPN) [NC,OR]

# Block Undetectable Browsers
RewriteCond %{HTTP_USER_AGENT} (Chromedriver|undetected-chromedriver|Undetectable|PhantomJsCloud|MultiLogin|GoLogin|MoreLogin|Incogniton) [NC]

RewriteRule (.*) - [F,L]
</IfModule>
```

### 14.4 SetEnvIf Method (Alternative)

```apache
<IfModule mod_setenvif.c>
# Block Headless Browsers
SetEnvIf User-Agent "^Headless" BLOCK_BOT
SetEnvIf User-Agent "HeadlessChrome" BLOCK_BOT
SetEnvIf User-Agent "PhantomJS" BLOCK_BOT
SetEnvIf User-Agent "Puppeteer" BLOCK_BOT
SetEnvIf User-Agent "Selenium" BLOCK_BOT
SetEnvIf User-Agent "Playwright" BLOCK_BOT

# Block Security Scanners
SetEnvIf User-Agent "Nmap" BLOCK_SCANNER
SetEnvIf User-Agent "nikto" BLOCK_SCANNER
SetEnvIf User-Agent "sqlmap" BLOCK_SCANNER
SetEnvIf User-Agent "Acunetix" BLOCK_SCANNER
SetEnvIf User-Agent "Nessus" BLOCK_SCANNER
SetEnvIf User-Agent "OpenVAS" BLOCK_SCANNER
SetEnvIf User-Agent "Burp" BLOCK_SCANNER
SetEnvIf User-Agent "ZAP" BLOCK_SCANNER

# Block WordPress Scanners
SetEnvIf User-Agent "WPScan" BLOCK_WP
SetEnvIf User-Agent "wpscan" BLOCK_WP
SetEnvIf User-Agent "WPXStrike" BLOCK_WP
SetEnvIf User-Agent "WordPress Security Scan" BLOCK_WP

# Block Scrapers
SetEnvIf User-Agent "Scrapy" BLOCK_SCRAPER
SetEnvIf User-Agent "curl" BLOCK_SCRAPER
SetEnvIf User-Agent "wget" BLOCK_SCRAPER
SetEnvIf User-Agent "python-requests" BLOCK_SCRAPER

# Block Anonymization
SetEnvIf User-Agent "Tor" BLOCK_ANON
SetEnvIf User-Agent "TOR" BLOCK_ANON
SetEnvIf User-Agent "Tails" BLOCK_ANON
</IfModule>

# Deny blocked requests
<IfModule !mod_authz_core.c>
Order allow,deny
Allow from all
Deny from env=BLOCK_BOT
Deny from env=BLOCK_SCANNER
Deny from env=BLOCK_WP
Deny from env=BLOCK_SCRAPER
Deny from env=BLOCK_ANON
</IfModule>
```

### 14.5 WordPress-Specific Blocking

```apache
# Block WordPress Attack Vectors
<IfModule mod_rewrite.c>
RewriteEngine On

# Block wp-config.php access
<files wp-config.php>
order allow,deny
deny from all
</files>

# Block xmlrpc.php (brute force vector)
<files xmlrpc.php>
order deny,allow
deny from all
</files>

# Block wp-json user enumeration (optional)
RewriteCond %{REQUEST_URI} ^/wp-json/wp/v2/users [NC]
RewriteRule ^(.*)$ - [F,L]

# Block SSRF via oembed proxy
RewriteCond %{REQUEST_URI} ^/wp-json/oembed/1.0/proxy [NC]
RewriteRule ^(.*)$ - [F,L]

# Block common exploit paths
RewriteCond %{REQUEST_URI} ^/wp-content/debug\.log [NC,OR]
RewriteCond %{REQUEST_URI} ^/wp-content/uploads/.*\.php [NC,OR]
RewriteCond %{REQUEST_URI} \.suspected$ [NC]
RewriteRule ^(.*)$ - [F,L]
</IfModule>
```

### 14.6 Old User-Agent Version Blocking

```apache
# Block outdated browser versions (often spoofed by bots)
RewriteCond %{HTTP_USER_AGENT} ^.*Chrome\/[1-119]\\.* [NC,OR]
RewriteCond %{HTTP_USER_AGENT} ^.*Firefox\/[1-120]\\.* [NC,OR]
RewriteCond %{HTTP_USER_AGENT} ^.*Safari\/[1-16]\\.* [NC,OR]
RewriteCond %{HTTP_USER_AGENT} ^.*MSIE\/[1-09]\\.* [NC,OR]
RewriteCond %{HTTP_USER_AGENT} ^.*Windows\ NT\/[3.1-6.3]\\.* [NC]
RewriteRule (.*) - [F,L]
```

---

## 15. Quick Reference: Block Lists

### 15.1 Headless Browsers (Pipe-Separated)

```
Headful|Headless Client|Headless|Headless Chromium|HeadlessChrome|Headless Edge|HeadlessChrome/Linux|HeadlessChrome/Ubuntu|Browserless|Browser-Use|Firefox Headless|Headless Linux|selenium:headless:chromium|selenium:headful:chromium|selenium:headless:firefox|playwright:headless:chromium|playwright:headful:chromium|PlaywrightPython|Selenium Stealth|Splash/Lua|HtmlUnit/Java|Chromedp|Cypress|browserless|gologin|PhantomJS|Puppeteer|Playwright
```

### 15.2 Hacking Tools (Pipe-Separated)

```
Metasploit|Kali Linux|Parrot Security OS|BlackArch Linux|BackBox Linux|ZAP|sqlmap|hydra|Burp Suite|Wireshark|Hashcat|Nmap|Zenmap|Masscan|Nessus|OpenVAS|OWASP ZAP|Netcat|Aircrack-ng|Nikto|Gobuster|Dirsearch|FeroxBuster|Nexpose|StormCrawler|GoSpider|WPScan|WPXStrike|nuclei|SQLNinja|meterpreter
```

### 15.3 Scraping Tools (Pipe-Separated)

```
Scrapy|SeleniumBase|Cloudscraper|Selenium Stealth|Botright|MechanicalSoup|Jsoup|AutoScraper|Httpx|ChromeDriver|Pyppeteer|Cheerio|Botasaurus|Puppeteer|Selenium|got-scraping|Scraper API|Web Scraper|Data Scraper|HTML Scraper|BeautifulSoup|Colly|gocolly
```

### 15.4 Proxy Patterns (Pipe-Separated)

```
AI proxy|API Proxy|HTTP Proxies|forward proxy|residential proxies|reverse proxy|http-proxy|Proxy Servers|VPN/Proxy|VPN|IPv4 Proxies|IPv6 Proxies|Mobile Proxies|Static ISP Proxies
```

---

## Document Information

| Attribute | Value |
|-----------|-------|
| **Original Source** | Hackers.txt |
| **Format** | Markdown (.md) |
| **Last Updated** | 2025-01-14 |
| **Purpose** | Security reference & defensive configuration |

---

*This document is for educational and defensive purposes only. Use responsibly and legally.*
