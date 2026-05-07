# 🕵️ Intelverse 2026: The Definitive OSINT Arsenal for Modern Investigators.

> **The OSINT noise floor is rising. This is the signal.**  
> A curated collection of field-tested intelligence tools for cybersecurity professionals, threat hunters, and investigators. I maintain this repository to bridge the gap between theoretical tools and actual investigative results. No filler, no dead links: just the high-yield assets I use to cut through the static.

<div align="center">

![Status](https://img.shields.io/badge/Status-Actively%20Maintained-brightgreen?style=flat-square)
![Year](https://img.shields.io/badge/Updated-May%202026-blue?style=flat-square)
![Tools](https://img.shields.io/badge/Tools-200%2B-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square)

</div>

---

### 🎯 The Signal-Over-Noise Principle
In an era of information overload, this repository adheres to a strict curation standard:
*   **Zero Dead Links:** Manually verified for 2026 compatibility.
*   **Tactical Utility:** If a tool doesn't solve a real-world problem, it isn't here.
*   **Investigator Safety:** Evaluated for OPSEC and research hygiene.

---

> ⚖️ **Ethical Use Only.** Every tool in this list must be used within applicable laws and with proper authorization. This repository exists for defenders, researchers, and analysts. The maintainer accepts no responsibility for any misuse or unlawful activity.

---

## 🗂️ Index

| # | Category | # | Category |
|---|----------|---|----------|
| 01 | [Search Engines & Dorking](#01--search-engines--dorking) | 12 | [Breach & Credential Intelligence](#12--breach--credential-intelligence) |
| 02 | [Cyberspace Asset Search](#02--cyberspace-asset-search) | 13 | [Threat Actor & APT Tracking](#13--threat-actor--apt-tracking) |
| 03 | [Recon Frameworks & Automation](#03--recon-frameworks--automation) | 14 | [Live Cyber Threat Maps](#14--live-cyber-threat-maps) |
| 04 | [Domain, DNS & Certificate Intel](#04--domain-dns--certificate-intel) | 15 | [Geospatial & Satellite Intelligence](#15--geospatial--satellite-intelligence) |
| 05 | [Social Media & Username OSINT](#05--social-media--username-osint) | 16 | [Image & Video Forensics](#16--image--video-forensics) |
| 06 | [People & Identity Investigation](#06--people--identity-investigation) | 17 | [Document & Metadata Extraction](#17--document--metadata-extraction) |
| 07 | [Email Intelligence](#07--email-intelligence) | 18 | [Blockchain & Crypto Tracing](#18--blockchain--crypto-tracing) |
| 08 | [Phone Number Intelligence](#08--phone-number-intelligence) | 19 | [Dark Web & Underground Intel](#19--dark-web--underground-intel) |
| 09 | [Company & Corporate Intelligence](#09--company--corporate-intelligence) | 20 | [Browser Extensions & Quick Lookup](#20--browser-extensions--quick-lookup) |
| 10 | [Code & Repository Intelligence](#10--code--repository-intelligence) | 21 | [OPSEC, Privacy & Anonymity](#21--opsec-privacy--anonymity) |
| 11 | [News, Archives & Web History](#11--news-archives--web-history) | 22 | [Learning, Communities & Resources](#22--learning-communities--resources) |

---

## 01 · Search Engines & Dorking

> The starting point for almost every investigation. Master these before reaching for specialized tools.

### General & AI-Powered

| Tool | Why It Matters | Free |
|------|----------------|------|
| [Google](https://www.google.com) | Widest web index on earth — the baseline for all surface-level recon | ✅ |
| [Bing](https://www.bing.com) | Different crawl index, often returns results Google suppresses | ✅ |
| [Yandex](https://www.yandex.com) | Superior reverse image search; strongest engine for CIS-region targets | ✅ |
| [Baidu](https://www.baidu.com) | Non-negotiable for investigations involving Chinese infrastructure | ✅ |
| [Brave Search](https://search.brave.com) | Independent index — not reliant on Google or Bing, no tracking | ✅ |
| [Perplexity AI](https://www.perplexity.ai) | AI search with cited sources — fast context-building on any topic | ✅ |
| [Wolfram Alpha](https://www.wolframalpha.com) | Computational knowledge engine — useful for data, stats, and structured queries | ✅ |
| [Kagi](https://kagi.com) | Ad-free, high-quality independent index with "Lenses" | Freemium |

### Privacy-First Search (OPSEC Investigations)

| Tool | Notes |
|------|-------|
| [Startpage](https://www.startpage.com) | Anonymous Google proxy — full results without being fingerprinted |
| [DuckDuckGo](https://duckduckgo.com) | No tracking; good for unfiltered first-pass searches |
| [Swisscows](https://swisscows.com) | Swiss-hosted, zero data retention |
| [Presearch](https://presearch.com) | Decentralized, community-operated search engine |
| [Gibiru](https://gibiru.com) | Uncensored results, no IP logging |

### Google Dorking

> **Note (2026):** `cache:` was removed by Google in early 2024. `related:` was dropped in 2023. Use the Wayback Machine as your cache replacement. All other core operators remain active.

**Core Operator Reference:**

```
site:target.com                         → Restrict results to a domain
filetype:pdf                            → Find specific formats (pdf, docx, xlsx, env, log, sql, bak)
intitle:"index of"                      → Locate open directory listings
inurl:admin                             → Find admin panels and login pages
intext:"api_key" OR intext:"password"   → Exposed credentials in page body
before:2024-01-01                       → Filter results before a date
after:2023-06-01                        → Filter results after a date
"exact phrase"                          → Force exact string match
-keyword                                → Exclude a term
site:target.com filetype:pdf "internal use only"
intitle:"index of" "backup" site:target.com
site:target.com inurl:login OR inurl:signin OR inurl:portal
```

**Dork Generation Tools:**

| Tool | Description | Free |
|------|-------------|------|
| [Google Hacking Database (GHDB)](https://www.exploit-db.com/google-hacking-database) | 7,000+ categorized dorks maintained by Offensive Security | ✅ |
| [DorkGenius](https://dorkgenius.com) | AI dork generator for Google, Bing, and DuckDuckGo | ✅ |
| [DorkGPT](https://www.dorkgpt.com) | Plain-language → working dork query conversion | ✅ |
| [SearchDorks](https://kriztalz.sh/search-dorks/) | AI dork builder covering FOFA, Shodan, Censys, and ZoomEye too | ✅ |

### Specialty & Niche Search

| Tool | Best For |
|------|----------|
| [PublicWWW](https://publicwww.com) | Search websites by source code — find wallet addresses, tracking IDs, API keys baked into HTML |
| [grep.app](https://grep.app) | Regex search across all public GitHub repos |
| [Searchcode](https://searchcode.com) | 75B+ lines of indexed public code |
| [Million Short](https://millionshort.com) | Strip the top 1M popular sites to surface obscure findings |
| [OCCRP Aleph](https://aleph.occrp.org) | Leaked documents, court records, and corporate filings for investigators |
| [Offshore Leaks Database](https://offshoreleaks.icij.org) | ICIJ Panama/Pandora Papers — shell companies and offshore entities |
| [RECAP Archive](https://www.courtlistener.com/recap/) | US federal court documents — free alternative to PACER |
| [Carrot2](https://search.carrot2.org) | Clusters results into themes — useful for identifying patterns across large result sets |
| [Epstein Exposed](https://epsteinexposed.com) | 2M+ DOJ case documents, flight logs, and network graph visualization |
| [DocumentCloud](https://www.documentcloud.org) | Journalist-grade annotated document platform |

---

## 02 · Cyberspace Asset Search

> Search engines for the internet itself — indexing ports, banners, certificates, and exposed services. Core to attack surface mapping and threat hunting.

| Tool | What It Indexes | Free |
|------|-----------------|------|
| [Shodan](https://www.shodan.io) | Ports, banners, services, webcams, ICS/SCADA, IoT — the original cyberspace search engine | Freemium |
| [Censys](https://search.censys.io) | Hosts, certificates, infrastructure — structured query language, excellent API | Freemium |
| [Criminal IP](https://www.criminalip.io) | AI/ML threat scoring — IP risk, malicious domain detection, VPN/proxy identification | Freemium |
| [FOFA](https://en.fofa.info) | Chinese-origin cyberspace search — broad IoT and global infrastructure coverage | Freemium |
| [ZoomEye](https://www.zoomeye.ai) | IP and domain asset discovery with vulnerability correlation | Freemium |
| [Netlas.io](https://app.netlas.io) | DNS, WHOIS, certs, open ports, banners — clean API, well-documented | Freemium |
| [FullHunt](https://fullhunt.io) | External attack surface discovery and continuous monitoring | Freemium |
| [GreyNoise](https://viz.greynoise.io) | Separates mass internet background noise from targeted attack traffic | Freemium |
| [ONYPHE](https://search.onyphe.io) | Passive + active internet scan data with threat intelligence overlays | Freemium |
| [GrayhatWarfare](https://grayhatwarfare.com) | Open S3 buckets — exposes publicly accessible cloud storage | Freemium |
| [BeVigil](https://bevigil.com/search) | Subdomains, URLs, and parameters extracted from **mobile apps** — unique source | Freemium |
| [ODIN](https://search.odin.io) | Hosts, CVEs, exposed buckets — 10 free searches per day | Freemium |
| [Shadowserver](https://dashboard.shadowserver.org) | Global cyber threat statistics — botnets, C2s, vulnerable systems | ✅ |
| [BGP.tools](https://bgp.tools) | Modern BGP and ASN toolkit for network-level reconnaissance | ✅ |
| [BGP.he.net](https://bgp.he.net) | ASN lookup, BGP routes, and IP block ownership | ✅ |
| [AbuseIPDB](https://www.abuseipdb.com) | Community-reported IP abuse database | ✅ |
| [Cisco Talos](https://talosintelligence.com/reputation_center) | IP and domain reputation from one of the world's largest threat intel teams | ✅ |
| [Cloudflare Radar](https://radar.cloudflare.com) | Internet traffic patterns, route anomalies, technology trends | ✅ |
| [BrightCloud](https://brightcloud.com/tools/url-ip-lookup.php) | URL and IP reputation with category and threat classification | ✅ |
| [Cyble ODIN](https://search.odin.io) | Exposed buckets, assets, and real-time vulnerability correlation | Freemium  | ✅ |

---

## 03 · Recon Frameworks & Automation

> When manual research doesn't scale. These platforms orchestrate dozens of data sources and chain findings automatically.

| Tool | Type | Best For | Free |
|------|------|----------|------|
| [SpiderFoot](https://www.spiderfoot.net) | Open-source / SaaS | 200+ module automated recon — domains, IPs, emails, usernames, breach data | ✅ OSS |
| [Maltego](https://www.maltego.com) | GUI / Cloud | Visual link analysis — map relationships between entities across data sources | Freemium |
| [Recon-ng](https://github.com/lanmaster53/recon-ng) | CLI Framework | Metasploit-style modular recon — domains, contacts, infrastructure enumeration | ✅ |
| [theHarvester](https://github.com/laramies/theHarvester) | CLI | Email, subdomain, IP, and URL harvesting from 30+ sources | ✅ |
| [Osmedeus](https://github.com/j3ssie/osmedeus) | CLI Workflow Engine | Automated offensive recon pipeline — chains multiple tools in sequence | ✅ |
| [Sn0int](https://github.com/kpcyrd/sn0int) | CLI + Package Manager | Semi-automated OSINT with installable module packages | ✅ |
| [Photon](https://github.com/s0md3v/Photon) | CLI Web Crawler | Fast extraction of URLs, emails, files, and external links from a target site | ✅ |
| [Hunchly](https://www.hunch.ly) | Browser Extension | Auto-archives every page visited during investigation — built-in case management | 💲 |
| [Amass](https://github.com/owasp-amass/amass) | CLI | OWASP-backed deep attack surface enumeration and mapping | ✅ |

---

## 04 · Domain, DNS & Certificate Intel

### Subdomain & DNS Discovery

| Tool | Description | Free |
|------|-------------|------|
| [DNSDumpster](https://dnsdumpster.com) | Subdomain discovery, MX/TXT/A records, and visual host map | ✅ |
| [Subfinder](https://github.com/projectdiscovery/subfinder) | Passive subdomain enumeration from 40+ data sources | ✅ |
| [SecurityTrails](https://securitytrails.com) | Historical DNS records, IP history, connected infrastructure | Freemium |
| [ViewDNS.info](https://viewdns.info) | 20+ DNS tools — IP history, reverse IP, WHOIS, port check | ✅ |
| [MXToolbox](https://mxtoolbox.com) | Email, DNS, blacklist, and SPF/DKIM diagnostics | ✅ |

### WHOIS & Ownership

| Tool | Description | Free |
|------|-------------|------|
| [DomainTools WHOIS](https://whois.domaintools.com) | Historical WHOIS with reverse WHOIS — find all domains registered by an entity | Freemium |
| [who.is](https://who.is) | Clean current WHOIS with registrar and expiry details | ✅ |
| [Whoxy](https://www.whoxy.com) | Reverse WHOIS by email, name, or company — discover full domain portfolio | Freemium |

### Certificate Transparency

| Tool | Description | Free |
|------|-------------|------|
| [crt.sh](https://crt.sh) | Search Certificate Transparency logs — reveals subdomains before DNS propagation | ✅ |
| [CertKit CT Logs](https://www.certkit.io/tools/ct-logs/) | Faster, better-filtered CT log search than crt.sh | ✅ |
| [Censys Certificates](https://search.censys.io) | Cert search with host correlation and expiry tracking | Freemium |

### Website Fingerprinting

| Tool | Description | Free |
|------|-------------|------|
| [BuiltWith](https://builtwith.com) | CMS, frameworks, analytics, CDN, and vendor technology stacks | Freemium |
| [Wappalyzer](https://www.wappalyzer.com) | Real-time tech fingerprinting as a browser extension or API | Freemium |
| [WPScan](https://wpscan.com) | WordPress plugin, theme, user, and CVE scanner | Freemium |
| [IsLegitSite](https://www.islegitsite.com) | Domain age, reputation, and security posture check | ✅ |

---

## 05 · Social Media & Username OSINT

### Username Enumeration

| Tool | Platforms Covered | Free |
|------|-------------------|------|
| [Sherlock](https://github.com/sherlock-project/sherlock) | 400+ platforms | ✅ |
| [Maigret](https://github.com/soxoj/maigret) | 3,000+ sites — pulls profile photos, bios, and linked accounts | ✅ |
| [Blackbird](https://github.com/p1ngul1n0/blackbird) | 600+ websites with async verification | ✅ |
| [WhatsMyName](https://whatsmyname.app) | Community-maintained JSON source list — accurate and regularly updated | ✅ |
| [Antisocial](https://github.com/rly0nheart/antisocial) | 30+ platforms with three-tier verification (API → browser → HTTP) | ✅ |
| [Digital Footprint Check](https://www.digitalfootprintcheck.com) | 100+ sites — free, no registration needed | ✅ |
| [Telegago](https://cse.google.com) | Google CSE for searching public Telegram channels without an account | | ✅ |
| [Telemetrio](https://telemetr.io) | Channel analytics and influence network tracking | | ✅ |

### Platform-Specific Tools

**X (Twitter)**

| Tool | Description |
|------|-------------|
| [Xquik](https://xquik.com) | Real-time X data — tweet search, follower extraction, engagement metrics, Space data |
| [MyTweetAlerts](https://www.mytweetalerts.com) | Custom email alerts based on Twitter keyword monitoring |

**Facebook**

| Tool | Description |
|------|-------------|
| [Facebook Friend List Scraper](https://github.com/narkopolo/fb_friend_list_scraper) | Scrape large friend lists without hitting rate limits |
| [Lookup-ID.com](https://lookup-id.com) | Find Facebook profile, group, and page numeric IDs from URLs |
| [Find My Facebook ID](https://findmyfbid.in) | Extract Facebook UID for API and graph operations |

**Reddit**

| Tool | Description |
|------|-------------|
| [RedditMetis](https://redditmetis.com) | User analysis — posting patterns, active subreddits, karma history |
| [Reddit Comment Search](https://www.redditcommentsearch.com) | Full comment history search by username |
| [Universal Scammer List](https://universalscammerlist.com) | Cross-referenced list of known malicious Reddit accounts |

**Telegram**

| Tool | Description |
|------|-------------|
| [Telegram Informer](https://github.com/paulpierre/informer) | Monitor and archive Telegram channels and groups |
| [Telemetrio](https://telemetr.io) | Channel analytics and influence network tracking |
| [Telegago](https://cse.google.com/cse?cx=006368593537057042503:efxu7xprihg) | Official 2026 Telegago engine for public Telegram content | ✅ |


**Steam**

| Tool | Description |
|------|-------------|
| [OSINT-Steam](https://github.com/mbentley3123/osint-steam) | Returns public info — friend lists and possible locations from Steam profiles |
| [Steam-OSINT](https://github.com/goitdude/Steam-OSINT) | Mutual friends analysis and full friend list mapping |

**GitHub**

| Tool | Description |
|------|-------------|
| [github_monitor](https://github.com/0x4D31/github-monitor) | Real-time tracking of user activity, profile changes, block detection, CSV logging |
| [GithubRecon / gitrecon](https://github.com/GONZOsint/gitrecon) | Lookup users by username or email, pull commit history and associated data |
| [GitLeak](https://github.com/k4rskin/gitleak) | Extracts hidden emails, commit timezones, and activity patterns via `.patch` metadata |
| [Shotstars](https://github.com/ARPSyndicate/shotstars) | Repo star statistics with fake star detection and visualization |
| [TruffleHog](https://github.com/trufflesecurity/trufflehog) | Find leaked secrets and credentials across git history |

**LinkedIn**

| Tool | Description |
|------|-------------|
| [linkedin2username](https://github.com/initstring/linkedin2username) | Generate username wordlists from company LinkedIn employee pages |

**WhatsApp**

| Tool | Description |
|------|-------------|
| [2Chat](https://2chat.co) | Check if a phone number is registered on WhatsApp |

---

## 06 · People & Identity Investigation

### Free Tools

| Tool | Description |
|------|-------------|
| [That'sThem](https://thatsthem.com) | Free correlator — links IP, email, phone, name, and address into unified profiles |
| [TruePeopleSearch](https://www.truepeoplesearch.com) | US people finder — address history, relatives, phone |
| [FastPeopleSearch](https://www.fastpeoplesearch.com) | Free US name, address, and phone lookups |
| [FamilyTreeNow](https://www.familytreenow.com) | Genealogy and contact info — useful for establishing historical residence chains |
| [Epieos](https://epieos.com) | Email or phone → Google account info, social profiles, breach exposure |
| [OSINT Industries](https://osint.industries) | Real-time identity resolution — email or phone → verified accounts, images, crypto wallets |

### Paid / Professional Grade

| Tool | Description |
|------|-------------|
| [Pipl](https://pipl.com) | Deep people search used by law enforcement and corporate investigators |
| [Spokeo](https://www.spokeo.com) | People, address, phone, and email aggregator |
| [BeenVerified](https://www.beenverified.com) | Background checks, criminal records, address history |
| [Intelius](https://www.intelius.com) | Professional background research service |

---

## 07 · Email Intelligence

| Tool | What It Does | Free |
|------|-------------|------|
| [Hunter.io](https://hunter.io) | Find professional emails by domain; pattern discovery and bulk verification | Freemium |
| [Holehe](https://github.com/megadose/holehe) | Check if an email is registered across 120+ platforms — passive, no alerts sent | ✅ |
| [GHunt](https://github.com/mxrch/GHunt) | Deep Google account profiling from email — name, last active, associated services | ✅ |
| [h8mail](https://github.com/khast3x/h8mail) | CLI breach hunting — aggregates HIBP, Snusbase, and custom sources | ✅ |
| [EmailRep.io](https://emailrep.io) | Reputation and risk score for email addresses | Freemium |
| [Have I Been Pwned](https://haveibeenpwned.com) | The definitive breach check — 14B+ records indexed | ✅ |
| [Epieos](https://epieos.com) | Email → Google account lookup and social profile correlation | Freemium |
| [Email Hippo](https://tools.emailhippo.com) | Validate whether an email address actually exists on the mail server | Freemium |
| [Email Format](https://email-format.com) | Discover email naming patterns used by specific companies | ✅ |
| [Email Permutator](https://www.emailpermutator.com) | Generate likely email variations from first name, last name, and domain | ✅ |
| [MXToolbox Email Headers](https://mxtoolbox.com/EmailHeaders.aspx) | Parse email headers to trace routing path and sending infrastructure | ✅ |

---

## 08 · Phone Number Intelligence

| Tool | Description | Free |
|------|-------------|------|
| [PhoneInfoga](https://github.com/sundowndev/phoneinfoga) | Advanced recon — carrier, country, line type, social profile links | ✅ |
| [Epieos](https://epieos.com) | Phone → linked accounts and platform presence | Freemium |
| [Truecaller](https://www.truecaller.com) | Reverse phone lookup with caller history and spam flagging | Freemium |
| [NumVerify](https://numverify.com) | Carrier, line type, and country validation via API | Freemium |
| [OSINT Industries](https://osint.industries) | Phone → real-time verified account discovery across platforms | Freemium |
| [2Chat](https://2chat.co) | Confirm WhatsApp registration status for any number | ✅ |

---

## 09 · Company & Corporate Intelligence

### Public Records & Filings

| Tool | Jurisdiction / Coverage | Free |
|------|------------------------|------|
| [OpenCorporates](https://opencorporates.com) | 200M+ companies worldwide — largest open corporate database | ✅ |
| [Companies House](https://www.gov.uk/get-information-about-a-company) | UK — filings, directors, financial statements, PSC register | ✅ |
| [SEC EDGAR](https://www.sec.gov/edgar) | US public companies — 10-K, insider transactions, executive compensation | ✅ |
| [Offshore Leaks Database](https://offshoreleaks.icij.org) | ICIJ Panama/Pandora Papers — offshore entities and shell companies | ✅ |
| [OpenSanctions](https://www.opensanctions.org) | Sanctions lists, PEP databases, and watchlists from 30+ sources | ✅ |
| [OCCRP Aleph](https://aleph.occrp.org) | Leaked documents, court records, corporate filings | ✅ |

### Business Intelligence

| Tool | Description | Free |
|------|-------------|------|
| [Crunchbase](https://www.crunchbase.com) | Funding rounds, investors, acquisitions, executive team profiles | Freemium |
| [LinkedIn](https://www.linkedin.com) | Org charts, employee discovery, role history, company structure | Freemium |
| [Glassdoor](https://www.glassdoor.com) | Internal culture intel, executive profiles, salary data | Freemium |
| [BuiltWith](https://builtwith.com) | Technology vendor stack intelligence per domain | Freemium |
| [linkedin2username](https://github.com/initstring/linkedin2username) | Harvest employee usernames from LinkedIn company pages | ✅ |

---

## 10 · Code & Repository Intelligence

> Developers routinely expose credentials, API keys, internal endpoints, and PII in public repositories. This category is consistently high-yield for security researchers.

| Tool | Description | Free |
|------|-------------|------|
| [grep.app](https://grep.app) | Regex search across all public GitHub repos — fastest secret-hunting path | ✅ |
| [Searchcode](https://searchcode.com) | 75B+ lines of public source code indexed across GitHub, GitLab, Bitbucket | ✅ |
| [GitHub Advanced Search](https://github.com/search/advanced) | Native GitHub filtering by language, date, user, org, file path | ✅ |
| [TruffleHog](https://github.com/trufflesecurity/trufflehog) | Find leaked secrets and credentials across git history | ✅ |
| [Gitrob](https://github.com/michenriksen/gitrob) | Scan GitHub orgs and users for sensitive file exposure | ✅ |
| [GithubRecon / gitrecon](https://github.com/GONZOsint/gitrecon) | Collect user/org metadata — emails, activity, and repo history | ✅ |
| [GitLeak](https://github.com/k4rskin/gitleak) | Extract hidden emails and commit timestamps from `.patch` metadata | ✅ |
| [github_monitor](https://github.com/0x4D31/github-monitor) | Alert on profile/repo changes with email notifications and CSV logging | ✅ |
| [Shotstars](https://github.com/ARPSyndicate/shotstars) | Fake star detection — evaluate credibility of a repo before trusting it | ✅ |
| [GitFive](https://github.com/mxrch/gitfive) | Link GitHub activity to emails and secondary social profiles | ✅ |

---

## 11 · News, Archives & Web History

| Tool | Description | Free |
|------|-------------|------|
| [Wayback Machine](https://web.archive.org) | Internet Archive — snapshots of websites from 1996 onwards | ✅ |
| [Archive.today](https://archive.ph) | On-demand page archiver — preserves evidence before pages are removed | ✅ |
| [CachedView](https://cachedview.nl) | Access Google, Bing, and Wayback cached versions side by side | ✅ |
| [GDELT Project](https://www.gdeltproject.org) | Global news event database — 100+ languages, updated every 15 minutes | ✅ |
| [MediaCloud](https://mediacloud.org) | Academic media tracking and narrative analysis platform | ✅ |
| [Factiva](https://professional.dowjones.com/factiva) | Premium historical news archive — 30,000+ sources going back decades | 💲 |

---

## 12 · Breach & Credential Intelligence

| Tool | Coverage | Free |
|------|----------|------|
| [Have I Been Pwned](https://haveibeenpwned.com) | 14B+ records — the gold standard for breach notification | ✅ |
| [DeHashed](https://dehashed.com) | Search billions of breach records — email, username, IP, phone, address | Freemium |
| [Intelligence X](https://intelx.io) | Darknet leaks, pastes, breach dumps, and WHOIS history | Freemium |
| [LeakCheck](https://leakcheck.io) | Email and password breach search with clean API | Freemium |
| [Breach Directory](https://breachdirectory.org) | Free partial breach check — no registration required | ✅ |
| [h8mail](https://github.com/khast3x/h8mail) | CLI breach aggregator — queries multiple sources simultaneously | ✅ |
| [StealSeek](https://stealseek.io) | Stealer log and breach database search | Freemium |
| [CredenShow](https://credenshow.com) | Compromised credential identification before attackers use them | Freemium |
| [HEROIC](https://heroic.com) | Dark web credential exposure scan with free tier | Freemium |
| [Venacus](https://venacus.com) | Breach search with email monitoring alerts | Freemium |
| [XposedOrNot](https://xposedornot.com) | Real-time domain-level breach analysis and risk analytics | ✅ |

---

## 13 · Threat Actor & APT Tracking

| Resource | What It Tracks | Free |
|----------|----------------|------|
| [MISP Galaxy](https://www.misp-project.org/galaxy.html) | Adversary groups, tools, and TTPs — used by threat intel teams globally | ✅ |
| [Malpedia](https://malpedia.caad.fkie.fraunhofer.de) | Malware families linked to specific threat actors | ✅ |
| [APT Groups Spreadsheet](https://docs.google.com/spreadsheets/d/1H9_xaxQHpWaa4O_Son4Gx0YOIzlrKDeFEOHyv01mUyw) | Community-maintained tracker with sponsored nations and tool mapping | ✅ |
| [ETDA Threat Actor Encyclopedia](https://apt.etda.or.th/cgi-bin/aptgroups.cgi) | Searchable threat actor database with associated tools | ✅ |
| [FortiGuard Threat Encyclopedia](https://www.fortiguard.com/threat-encyclopedia) | Actor TTPs, attack timelines, and tool mapping | ✅ |
| [SOCRadar Labs](https://labs.socradar.com) | Actor profiles, recent campaigns, and TTP breakdowns | Freemium |
| [Dark Web Informer](https://darkwebinformer.com) | Tracking 850+ threat actors — forum posts, leaks, ransomware announcements | ✅ |
| [MalwareBazaar](https://bazaar.abuse.ch/browse/) | Search and download confirmed malware samples by hash, family, or tag | ✅ |
| [YARAify](https://yaraify.abuse.ch/scan/) | Community YARA engine for malware pattern matching | ✅ |
| [Abusech Hunting](https://hunting.abuse.ch) | Single query across all abuse.ch platforms | ✅ |
| [BreachHQ](https://breachhq.com) | Comprehensive listing of known cybercriminal and APT groups | ✅ |
| [VenariX](https://venarix.com) | **(2026 Essential)** Real-time ransomware tracker & actor relationship mapper | Freemium |

---

## 14 · Live Cyber Threat Maps

> Real-time attack visualization — useful for situational awareness and understanding global threat patterns.

| Tool | Notable For |
|------|-------------|
| [Check Point Live Map](https://threatmap.checkpoint.com) | Ransomware, infostealers, and cloud attack tracking |
| [Kaspersky Cyberthreat Map](https://cybermap.kaspersky.com) | Real-time global attack telemetry with per-country breakdown |
| [Radware Live Threat Map](https://livethreatmap.radware.com) | DDoS and application layer attack visualization |
| [Imperva Threat Map](https://www.imperva.com/cyber-threat-attack-map/) | Bot attacks, DDoS, and hacking attempt flows |
| [FortiGuard Outbreak Alerts](https://www.fortiguard.com/outbreak-alert) | Active outbreak tracking with CVE and vendor mapping |
| [Cloudflare Radar](https://radar.cloudflare.com) | Traffic trends, BGP route leaks, and internet disruption tracking |

---

## 15 · Geospatial & Satellite Intelligence

### Imagery & Verification

| Tool | Description | Free |
|------|-------------|------|
| [Google Earth Pro](https://earth.google.com) | Historical satellite imagery with timeline slider, measurement tools, and export | ✅ |
| [Sentinel Hub](https://www.sentinel-hub.com) | ESA imagery — multi-spectral analysis and change detection | Freemium |
| [SunCalc](https://www.suncalc.org) | Sun position and shadow analysis — verify when and where a photo was taken | ✅ |
| [ShadowCalculator](http://shadowcalculator.eu) | Shadow direction and length from sun angle and date | ✅ |
| [MapChecking](https://www.mapchecking.com) | Crowd size estimation from satellite imagery | ✅ |

### Tracking & Mapping

| Tool | Description | Free |
|------|-------------|------|
| [Overpass Turbo](https://overpass-turbo.eu) | Advanced OpenStreetMap queries — find infrastructure, landmarks, custom features | ✅ |
| [Wikimapia](https://wikimapia.org) | Collaboratively tagged map — identifies unlabeled structures and locations | ✅ |
| [What3Words](https://what3words.com) | Precise 3m² global location encoding | ✅ |
| [MarineTraffic](https://www.marinetraffic.com) | Real-time vessel position, port intelligence, voyage history | Freemium |
| [FlightRadar24](https://www.flightradar24.com) | Real-time civil aircraft tracking | Freemium |
| [ADS-B Exchange](https://www.adsbexchange.com) | **Unfiltered** aircraft tracking — government and military flights included, no removal requests | ✅ |
| [Windy](https://www.windy.com) | Wind, storm, and weather data — supports maritime and aviation OSINT | ✅ |
| [GeoGuessr](https://www.geoguessr.com) | Train visual geolocation skills — terrain, road signs, architecture recognition | Freemium |

---

## 16 · Image & Video Forensics

### Reverse Image Search

| Tool | Best For | Free |
|------|----------|------|
| [Google Images](https://images.google.com) | Widest web coverage for tracing image origins | ✅ |
| [Yandex Images](https://yandex.com/images) | Facial recognition — best for finding people across photo databases | ✅ |
| [TinEye](https://tineye.com) | Exact match history with earliest appearance dates | Freemium |
| [PimEyes](https://pimeyes.com) | AI Face recognition — finds where a face appears online | Freemium |
| [Lenso.ai](https://lenso.ai) | AI reverse search with dedicated "Research Mode" (10k+ results) | Freemium |

### Video Verification

| Tool | Description | Free |
|------|-------------|------|
| [InVID / WeVerify](https://www.invid-project.eu) | Keyframe extraction and video fragment verification | ✅ |
| [Fake-Catcher](https://fake-catcher.intel.com) | Real-time deepfake and synthetic media detection | ✅ |
| [Youtube Metadata](https://mattw.io/youtube-metadata/) | Extract hidden upload data, tags, and location info from YT videos | ✅ |

---

## 📈 2026 Field Workflows
| Goal | Workflow |
| :--- | :--- |
| **Verify Identity** | `Photo` → `Lenso.ai` → `Epieos` → `Sherlock` |
| **Track APTs** | `IOCs` → `MalwareBazaar` → `VenariX` → `MISP` |
| **Repo Secrets** | `Org Name` → `TruffleHog` → `GitLeak` → `h8mail` |

---

### Metadata & Authenticity Analysis

| Tool | Description | Free |
|------|-------------|------|
| [ExifTool](https://exiftool.org) | The gold standard — reads and writes metadata for any file format | ✅ |
| [FotoForensics](https://fotoforensics.com) | Error Level Analysis for detecting image manipulation | ✅ |
| [Jeffrey's Exif Viewer](http://exif.regex.info/exif.cgi) | Web-based EXIF reader — no software install needed | ✅ |

---

## 17 · Document & Metadata Extraction

> Public documents frequently contain hidden metadata: author names, usernames, internal paths, GPS coordinates, and software version strings.

| Tool | File Types Supported | Free |
|------|---------------------|------|
| [FOCA](https://github.com/ElevenPaths/FOCA) | PDF, DOC, XLS, PPT, PPTX — searches Google/Bing for docs then extracts metadata | ✅ |
| [ExifTool](https://exiftool.org) | All formats — most comprehensive metadata extraction tool available | ✅ |
| [Metagoofil](https://github.com/laramies/metagoofil) | Finds and downloads public documents from a target domain then extracts metadata | ✅ |
| [OCCRP Aleph](https://aleph.occrp.org) | Leak-focused document search with entity extraction and cross-referencing | ✅ |
| [Scribd](https://www.scribd.com) | Large document and slide repository for background research | Freemium |

**Dorks for hunting exposed documents:**
```
site:target.com filetype:pdf
site:target.com filetype:xlsx OR filetype:docx OR filetype:csv
site:target.com filetype:pptx "internal" OR "confidential"
site:target.com filetype:env OR filetype:log OR filetype:sql OR filetype:bak
```

---

## 18 · Blockchain & Crypto Tracing

> On-chain data is permanently public. Every wallet transaction, contract interaction, and token transfer is permanently traceable.

### Blockchain Explorers

| Explorer | Chain |
|----------|-------|
| [Etherscan](https://etherscan.io) | Ethereum — transactions, token transfers, smart contracts |
| [Blockchain.com Explorer](https://www.blockchain.com/explorer) | Bitcoin — addresses, transactions, mempool |
| [Blockchair](https://blockchair.com) | Multi-chain — BTC, ETH, BCH, LTC, and more with privacy scoring |
| [Solscan](https://solscan.io) | Solana — transactions, tokens, DeFi activity |
| [Tronscan](https://tronscan.org) | Tron — TRX and TRC-20 tokens |

### Intelligence & Entity Mapping

| Tool | Description | Free |
|------|-------------|------|
| [Arkham Intelligence](https://www.arkhamintelligence.com) | AI entity mapping — tags wallets to known exchanges, funds, individuals, and smart money | Freemium |
| [Breadcrumbs](https://www.breadcrumbs.app) | Free visual on-chain investigation and wallet profiling | Freemium |
| [Glassnode](https://glassnode.com) | On-chain metrics — holder behavior, exchange flows, accumulation patterns | Freemium |
| [Chainalysis](https://www.chainalysis.com) | Enterprise-grade tracing used by law enforcement agencies globally | 💲 |
| [Elliptic](https://www.elliptic.co) | Crypto compliance and transaction risk scoring | 💲 |
| [Crystal Blockchain](https://crystalblockchain.com) | Visual transaction graph tracing with risk attribution | 💲 |

---

## 19 · Dark Web & Underground Intel

> ⚠️ Always use Tor Browser + VPN + an isolated virtual machine. Never conduct dark web OSINT from a host OS or real identity.

| Tool | Description | Free |
|------|-------------|------|
| [Ahmia](https://ahmia.fi) | Clearnet-accessible Tor hidden service search — indexes .onion sites, respects robots.txt | ✅ |
| [Intelligence X](https://intelx.io) | Search darknet, Tor, I2P, Freenet, data breaches, and archived leaks | Freemium |
| [Dark Web Informer](https://darkwebinformer.com) | Tracks 850+ threat actors — forum posts, leak announcements, ransomware updates | ✅ |
| [MalwareBazaar](https://bazaar.abuse.ch) | Download and analyze confirmed malware samples by hash, family, or tag | ✅ |
| [Abusech Hunting](https://hunting.abuse.ch) | Single query across all abuse.ch platforms simultaneously | ✅ |
| [Shadowserver](https://dashboard.shadowserver.org) | Global botnet and C2 infrastructure monitoring | ✅ |

**Isolation checklist before any dark web OSINT session:**
```
☐ Dedicated VM — Whonix or Tails preferred
☐ Tor Browser only — no additional plugins, JavaScript disabled unless required
☐ VPN active at the hypervisor/host level
☐ No personal accounts signed in anywhere on the machine
☐ Screenshot metadata stripped before saving evidence
☐ Treat sessions as disposable — snapshot and revert VM after each session
```

---

## 20 · Browser Extensions & Quick Lookup

> Perform OSINT lookups without leaving your active browser tab — critical for maintaining investigation flow.

| Extension | Browser | What It Does |
|-----------|---------|-------------|
| [Mitaka](https://github.com/ninoseki/mitaka) | Chrome / Firefox | Right-click any IP, hash, domain, or URL → look it up across 80+ OSINT sources instantly |
| [Sputnik](https://github.com/mitchmoser/sputnik) | Chrome | IOC lookups — VirusTotal, Shodan, Censys from context menu |
| [Shodan Extension](https://chrome.google.com/webstore/detail/shodan/jjalcfnidlmpjhdfepjhjbhnhkbgleap) | Chrome | Shows Shodan data for any website's current IP address |
| [Wappalyzer](https://www.wappalyzer.com) | Chrome / Firefox | Real-time technology stack detection for the current site |
| [Wayback Machine](https://chrome.google.com/webstore/detail/wayback-machine/fpnmgdkabkmnadcjpehmlllkndpkmiak) | Chrome | One-click access to archived versions of any page |
| [uBlock Origin](https://ublockorigin.com) | Chrome / Firefox | OPSEC essential — blocks trackers, fingerprinting scripts, and malicious ads |

---

## 21 · OPSEC, Privacy & Anonymity

> Protecting your investigation identity is non-negotiable. A single careless action can expose your real IP to a threat actor, burn a months-long investigation, or create legal liability.

### Anonymity Infrastructure

| Tool | Purpose |
|------|---------|
| [Tor Browser](https://www.torproject.org) | Anonymous browsing through the Tor network — mandatory for dark web research |
| [Tails OS](https://tails.boum.org) | Amnesic OS on USB — leaves absolutely zero trace on the host machine |
| [Whonix](https://www.whonix.org) | Two-VM setup: Gateway (Tor) + Workstation — traffic cannot leak by design |
| [Kali Linux](https://www.kali.org) | Penetration testing distro with OSINT tools pre-installed |
| [ProtonVPN](https://protonvpn.com) | No-logs, open-source VPN — run at the host level when using VMs |

### Sock Puppet & Investigation Hygiene

```
✅ Create investigation personas on dedicated VMs or separate devices
✅ Use ProtonMail or Tutanota for throwaway investigation accounts
✅ Never reuse passwords or usernames across investigation personas
✅ Age sock puppet accounts naturally — wait 2–4 weeks before active use
✅ Separate browser profiles per target and per investigation
✅ Strip EXIF metadata from all screenshots before sharing or archiving
✅ Store notes and evidence in an encrypted container (VeraCrypt)
✅ Log every source URL with a timestamp — Hunchly automates this
✅ Never access investigation targets from your personal home IP
```

### Pre-Investigation Checklist

```
☐ VPN active
☐ VM loaded and network-isolated
☐ Browser fingerprint verified at coveryourtracks.eff.org
☐ No personal accounts signed in anywhere
☐ Dedicated investigation email ready for platform sign-ups
☐ Evidence capture tool running (Hunchly or manual archive.ph)
☐ Evidence folder created with today's date and case reference
```

---

## 22 · Learning, Communities & Resources

### Free Training & Platforms

| Resource | Format | Focus |
|----------|--------|-------|
| [OSINT Curious](https://osintcurio.us) | Blog + Podcast + YouTube | Weekly tips, live walkthroughs, community challenges |
| [Bellingcat](https://www.bellingcat.com/resources) | Guides + Workshops | Investigative journalism — geolocation, satellite intel, conflict OSINT |
| [TraceLabs](https://www.tracelabs.org) | CTF Competitions | OSINT applied to finding missing persons — skills with real impact |
| [TryHackMe OSINT Path](https://tryhackme.com) | Hands-on Labs | Beginner to intermediate skill building in a guided environment |
| [Hack The Box](https://www.hackthebox.com) | CTF Challenges | Advanced OSINT and forensics challenges |
| [OSINT Dojo](https://www.osintdojo.com) | Training Toolkit | Curated resources and pre-configured investigation environments |

### Paid / Professional Training

| Resource | Level |
|----------|-------|
| [IntelTechniques — Michael Bazzell](https://inteltechniques.com) | Intermediate → Advanced — the gold standard; includes annual updated book and workbook |
| [TCM Security OSINT Course](https://academy.tcm-sec.com) | Beginner → Intermediate — practical and hands-on |
| [SANS SEC487](https://www.sans.org/courses/open-source-intelligence-gathering) | Professional — used by law enforcement and government analysts |

### Active Communities

| Community | Platform |
|-----------|----------|
| [r/OSINT](https://www.reddit.com/r/OSINT) | Reddit |
| [Bellingcat Discord](https://discord.gg/bellingcat) | Discord |
| [TraceLabs Discord](https://www.tracelabs.org) | Discord |
| [OSINT Team Discord](https://discord.gg/osint) | Discord |

### Essential Books

| Book | Author | Why Read It |
|------|--------|-------------|
| Open Source Intelligence Techniques | Michael Bazzell | Updated annually — the definitive practitioner manual |
| Extreme Privacy | Michael Bazzell | Personal data removal and deep OPSEC methodology |
| The Art of Invisibility | Kevin Mitnick | Privacy and anonymity from a reformed hacker's perspective |
| This Is How They Tell Me the World Ends | Nicole Perlroth | Cybersecurity investigation journalism at its finest |

### Podcasts

| Podcast | Focus | Frequency |
|---------|-------|-----------|
| [IntelTechniques Podcast](https://inteltechniques.com/podcast.html) | Privacy, OSINT, data removal | Weekly |
| [OSINT Curious Cast](https://osintcurio.us/osintvideosandpodcasts/) | Practitioner techniques and case studies | Irregular |

---

## 🗺️ Investigation Workflow — Quick Reference

```
DEFINE TARGET & SCOPE
        │
        ├─ Domain / Org ────→ WHOIS → crt.sh → DNSDumpster → Subfinder
        │                      └→ Shodan/Censys → BuiltWith → LinkedIn → EDGAR
        │
        ├─ Person ──────────→ Username: Sherlock / Maigret / Blackbird
        │                      └→ Email: Holehe / GHunt / EmailRep
        │                      └→ Phone: PhoneInfoga / Epieos
        │                      └→ Breach: HIBP / DeHashed / h8mail
        │
        ├─ IP Address ──────→ IPinfo → AbuseIPDB → Shodan → GreyNoise → Talos
        │
        ├─ Email ───────────→ HIBP → Holehe → GHunt → EmailRep → h8mail
        │
        ├─ Image ───────────→ ExifTool (metadata) → Google/Yandex/TinEye (reverse)
        │                      └→ FotoForensics (manipulation check)
        │                      └→ SunCalc (time/location verification)
        │
        ├─ Cryptocurrency ──→ Explorer (chain-specific) → Arkham → Breadcrumbs
        │
        └─ Dark Web ────────→ Ahmia → IntelX → Dark Web Informer → MalwareBazaar
                               └→ Isolated VM + Tor Browser only — always
        │
COLLECT ──→ Archive every source: Hunchly / archive.ph / Wayback Machine
        │
ANALYZE ──→ Link entities: Maltego / SpiderFoot
        │
DOCUMENT ─→ Report with timestamped evidence, source URLs, and confidence labels
```

---

## Contributing

To contribute a tool, open a pull request with this format:

```markdown
| [Tool Name](https://url) | One-sentence description of what it does | Free/Freemium/💲 |
```

**A submission must:**
- Be actively maintained — a commit or update within the past 12 months
- Be verified working — please test it before submitting
- Be legal to use for OSINT and security research purposes
- Not duplicate an existing entry

**Not accepted:**
- Abandoned, archived, or unmaintained tools
- Tools built for unauthorized access or illegal surveillance
- Duplicates

---

## 📈 Recommended Investigator Workflows
To cut through the static, use these proven tool chains for common investigation types:

| Objective | Tools / Sequence | Why It Matters |
| :--- | :--- | :--- |
| **Identity Linkage** | `Email` → `Holehe` → `Epieos` → `GitFive` | Connects an alias to a developer profile or social identity. |
| **Attack Surface** | `Domain` → `Amass` → `ODIN` → `Censys` | Discovers cloud misconfigurations and exposed assets. |
| **Influence Tracking**| `Keyword` → `Telegago` → `Telemetrio` | Tracks the spread of disinformation or actor propaganda. |
| **Verify Identity** | `Photo` → `Lenso.ai` → `Epieos` → `Sherlock` |
| **Track APTs** | `IOCs` → `MalwareBazaar` → `VenariX` → `MISP` |
| **Repo Secrets** | `Org Name` → `TruffleHog` → `GitLeak` → `h8mail` |

> ⚠️ **OPSEC Note (2026):** Avoid visiting "People Search" sites (e.g., Spokeo, Whitepages) from your primary IP. These are frequently used as honey-tokens by targets to log an investigator's IP. Always use a non-attributable VM or residential proxy.

---
⚖️ Disclaimer & License
Notice: This project is provided for educational and professional research purposes only. The "Signal-Over-Noise" and its contributors do not endorse the use of these tools for stalking, harassment, unauthorized access, or any activities that violate the privacy of individuals or the laws of any jurisdiction.

Liability: The user assumes all responsibility for their actions. Accessing certain data sources may be subject to the Terms of Service of the respective providers.

License: This toolkit is licensed under the MIT License. Feel free to fork, share, and build upon this knowledge responsibly.
*Maintained by the community · Last updated May 2026 · ⭐ Star if this helped you*
