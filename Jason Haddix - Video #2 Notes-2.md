


>

## Jason Haddix - Video Notes

  

https://www.youtube.com/watch?v=C4ZHAdI8o1w

  

Don’t miss Version 1 >

  

t3stvideo “How to Shot Web - DEFCON23”

  

https://www.youtube.com/watch?v=VtFuAH19Qz0

  

Version 2 Notes:

  

Topics:

  

-   Disccovery

  

-   XSS SSTI

  

-   SSRF

  

Code Injection / CMDI / Advancements in Fuzzing

  

BOOKS:

Web Application Hacker’s Handbook > Must Have Book

  

4 Additional Must Have Books:

1.  Web Hacking 101 > Peter Yaworski 
2.  Breaking into Information SEcurity > Andy Gill
3.  OWASP Testing Guide
4.  Mastering Modern Web Penetration Testing

  

DISCOVERY > TOPIC #1

  

**Tools for Scraping Subdomains:**

  

1.  Sublist3r > Brutesubs > Sub scraping
2.  MaSSDNS - All.txt List > Sub bruting
3.  MASSCAN > Port Scanning

  

Sublist3r > the BEST one!!!

  

-   better than recon-ng/enumall

  

Compare Recon-NG/Enumall v. Sublist3r

  

Recon-NG / Enumall

-   SSLTOOLS.clm api
-   hackerarget.com Api
-   Shodan
-   Zoomeye (not core)
-   Threatcrowd (not core)
-   Zone Transfer (not core)
-   RiskIQ (not core)
-   Censys IO (not core)

  

Sublist3r:

-   Core Gathers from:

-   Baidu
-   ASK
-   DNS Dumpster (scans.io)
-   Virus Total
-   PRRArchive

Both Include:

-   Google (Recon-ng now handles Captcha)
-   Bing
-   CRT.SH
-   Threat crowd
-   Netcraft

  

BruteSubs > includes BOTH!!!

-   a set of docker images that includes multiple tools
-   includes enumall and sublist3r
-   Also includes GoBuster and ALTDNS
-   Starts up in separate container
-   /Desktop/tools/brutesubs

-   docker -compose up (command in Kali on Folder above)

-   Some configuration required:

-   Update the docker image with non core recon-ng modules
-   Configure the .env File
-   Diable Bruteforce for enumall;

  

Bespoke > Subdomain Scraping

-   Github > mandatoryprogrammer / cloudflare _enum
-   Github > Censys.py
  

**Tools for Scraping SubBruting - 5 main tools:**

  

-   Subbrute
-   Gobuster
-   massdns
-   dns-parallel-prober
-   blacksheepwall

  

  

  

  

-   Takes alot of time to do these
-   Massdns is really fast.

-   github > blechschmidt / massdns

  

-   Made a whole list of all subbrute tools in all.txt file:

-   https://gist.github.com/jhaddix/
-   grab this file from his github

  

-   Raft List > Url brute forcing also the "all.txt" file

  

**ACQUISITIONS - Tools to see a list of a company's acquisitions:**

-   Crunchbase

-   https://www.crunchbase.com/
-   Protected and cannot pull results down for command line
-   Use Phantom js to pull down the page
-   I tested this and there's a "export" button now on the site
-   Used "Sony" as example and got 46 results

**PORT SCANNING TOOLS:**

-   Masscan

-   Written in C++ and super fast
-   No port list
-   Copy port list from nmap list and paste in the command line
-   ASN List and range
-   Use default nmap list for Masscan
-   11 min for 65,000 hosts
-   Results: look for ports wth web assets on it

-   nmap

-   default port list for large scan is not good and is very slow

-   EYEWITNESS

-   Tool to identify visually what you want to go after within all of the "scraped" data
-   includes screens shots
-   May not know protocol so it takes screenshots
-   checks for RDP and VNC running on the hosts
-   Mass screen shots of a long list.
-   The best one!
-   HTTPScreenshot is another good one
-   Visual id what you want to hack...admin stuff etc!
-   Helps to look at scope
-     
    

**Platform ID and CVE TOOLS > Searching thru the list:**  

-   Retire.js
-   Wappalyzer
-   Builtwith
-   OpenGSE
-   **Github > vulnersCom / burp-vulners-scanner > NEW!!!**

-   **determines version numbers**
-   **Gives links to vulnerabilities that are lower than the ver number**
-   **Get list of CVE's for your target**

  

Rest of the video is Tooling

  

**Content Discovery / Directory Bruting**

GoBuster

Burp Content Discovery

Robots Disallowed

  

-   Seclists / RAFT / Digger Wordlists
-   Patator
-   WPScan
-   CMSmap

  

Githubs:

	- OJ / gobuster

	- danielmiessler / RobotsDisallowed

  

-   Use on directories, config files as well

  

**Parameter Bruting > Brute force parameters > YES!**

Github> maK- / parameth

  

Parameth is a tool to brute force parameters.

  

-   combine it inside the list for this tool:

  

Github > PortSwigger / blackslash-powered-scanner

  

-   Pair the two together and get decent results

  

  

  

**XSS**

  

Polyglots

Seclists

Flash

Common input vectors

Blind XSS Frameworks

-   Sleepy Puppy (python) - Netflix security team
-   XSS Hunter (Python)
-   Ground Control (ruby)(small)

Polyglots

XSS Mindmap

  

Github resources:

  

-   jobertaabma / ground-control

  

-   Netflix / sleepy-puppy

  

-   mandatoryprogrammer / xxshunter

  

**BLIND XSS**

  

XSS Hunter v. Sleepy Puppy

  

The payload is the key to this comparison and how campaigns are organized.

  

XSS Hunter Payload Options:

-   The vulnerable page's URL
-   origin of execution
-   victim's ip add
-   The page referer
-   The victim's user agent
-   All non-http-only cookies
-   The page's full html dom
-   Full screenshot of the affected page
-   responsible http request (if an xss hunter compatible tools is used)

  

**XSS Polyglot #4**

  

Unleashing an ultimate XSS Polyglot:

github > 0xS0bky / HackVault

  

  

Injection strings bypass filters

  

Jackmasa's XSS Mindmap

-amazing!!!

-breaks down xss based on concept

-png file no longer available...:-(

  

**Server Side Injection: SSTI**

-   templating engine
-   wappalyzer + builtwith + vuln scanner will tell you if the site is this type
-   Attack 1 (image below): Test if using a templating system. If math completes, then templating syste is being used.
-   Attack 2: gives the /etc/password information
    
-   TPLMap > Baller Tool!!!!

-   Git > epinna / tplmap
-   specifically for template injection
-   ask for OS shell
-   gives mock shell and get /etc/password
-   looks at the source code for info on njection strings.
-   reverse engineering the tooling to get the commands
-   Best resource links: see image below

  

  

  

  

  

**SSRF > Server Side Request Forgery:**

  

  

Definition: Finding a parameter or get request that eventually takes a path of some sort referencing either an internal or external path.

  

Remix of RFI and LFI type of testing

  

-   SSRF Bible
-   Burp Collaborator
-   ewilded / psychoPATH > Git

  

-Blacklists - Alternate Ip encoding

-   Dotted decimal overflow
-   Dotless decimal
-   Dotless decimal with overflow
-   Dotted Hex
-   Dottless Hex
-   Dotless Hex with overflow
-   Dotted Octal
-   Dotted octal with padding.

  

  

Wallarm > SSRF Bible Cheatsheet

  

  

  

49:17 end.
