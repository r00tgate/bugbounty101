


>

## Meeting #2 - Bug Bounty 101.2

Date: April 7, 2018
Time: 10:00a.m. - 12:30 p.m.
Place: Moorpark College, Room T212

- Intro and Welcome Newcomers! 
- Review  of Meeting #1 Topics and Discussion
- Highlight a Hacker > Geoffrey Janjua - Expert Pen Tester
	- Nullspace Workshop Review 
	- [Coming Up > Layer One Workshop - Pen Testing - May 25, 2018!] (https://www.layerone.org/training/hands-on-network-penetration-testing-and-ethical-hacking/
- Review of [Sony Program on Hack One](https://hackerone.com/sony)
	- 68 Bugs Resolved so far (by other hackers!)
- Sony Program > Focus on 4 Criteria
1. XXS > Cross Site Scripting
2. CSRF > Client Side 
3. Directory Traversal
4. Information Disclosure

Start Hacking Sony! > Tools Used
- List of Tools: [Review of Jason Haddix Video Note] (https://github.com/r00tgate/bugbounty101/blob/master/Jason%20Haddix%20-%20Video%20%232%20Notes-2.md)
- KnockPy > List Sony's Subdomains
- Sublist3r > Another Subdomain List
- Dig 
- Burpe Suite > Steps to follow:
1. Disable Intercept
2. Click on everything on the Sony Site
3. See what is tracked by BurpSuite
4. Look at the cookies located in BurpSuite
5. Be careful of aggressive scans (such as Spider) which may break the host!  
- Old Sony Site > Find what is breakable
1. spt.spe.sony.com/robots.txt

Topic for Meeting #3:
OWASP > XSS Scripting > [Learn HERE!](https://www.owasp.org/index.php/Cross-site_Scripting_%28XSS%29)  

Thank you all for coming!  

-Mae
