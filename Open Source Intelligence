#### Open Source Intelligence
Intelligence gathering is performing reconnaissance on your victim from both passive and active methods in order to find information about users, networks, domains, and other sensitive information. We won’t dive deeply into Open Source Intelligence like we do with the Ethical Hacking course, but it is important to identify which sites to attack and learn information about a company. Some quick refreshers and reminders on how to find subdomains, folders, files, and servers:

Best List for Subdomains:
https://gist.github.com/jhaddix/

Nmap: nmap -sn --script dns-brute ebay.com

Knockpy – Bruteforce through all sub-domains
	-  cd /opt/knock/knockpy
	- python ./knockpy.py ebay.com


Sublist3r
	-  cd /opt/Sublist3r
	- python sublist3r.py -d ebay.com

Google Dorking: site:http://*.ebay.com

DNS Dumpster (https://dnsdumpster.com/), ShodanHQ, and Censys.io

MassDNS (The Fastest)
	- cd /opt/massdns
	- ./subbrute.py /opt/subdomain.txt cnn.com | massdns -r resolvers.txt -t A -a -o -w massdns_output.txt -
