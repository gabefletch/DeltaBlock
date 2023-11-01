<img src="https://github.com/gabefletch/DeltaBlock/assets/38300939/02815979-f67d-4dee-8865-178973114236" width=400><br>


A custom DNS profile for NextDNS (list also available) capable of blocking up to 99%* of ads.<br>
DeltaBlock stops both web-based and in-app ads from loading.<br>
A project by [@gabfletch](https://github.com/gabefletch).<br>

### Notice for New NextDNS Users
DeltaBlock is only designed for use via NextDNS, which is limited to 300,000 queries per month without a subscription. The lowest tier with unlimited queries is available for $1.99/month. Using the DeltaBlock custom profile, however, is completely free.

### NextDNS Affiliate Link
Help DeltaBlock remain running by sharing this link:
https://nextdns.io/?from=pyukpkuc

*According to Toolz AdBlock Test. This percentage varies depending on network variables. DeltaBlock stops an average of 96% of ads at all times based on testing between both iOS and macOS devices. The lowest percentage resulting from testing has been 93%, under strenuous network variables with ad-heavy pages.<br>
### Readme Contents
[Installation](https://github.com/gabefletch/DeltaBlock#installation)<br>
[Included Blocklists](https://github.com/gabefletch/DeltaBlock#included-blocklists)<br>

# Installation
## iOS, iPadOS, macOS, Android
### Via NextDNS App (Recommended)
- Install the NextDNS app on your device of choice
(Available for iOS, iPadOS, macOS or Android)
- Enter the settings for NextDNS and enter `4b3fba` as the Configuration ID.
### Via Apple Config File
(Apple Devices Only)
- [Click here](https://apple.nextdns.io/?profile=4b3fba) to be taken for the NextDNS Apple Config Profile generator for DeltaBlock.
- Download and install the profile via the Settings app.
## Windows
### Via NextDNS App (Recommended)
- Install the NextDNS app by [clicking here](https://nextdns.io/download/windows/stable).
- Enter the settings for NextDNS and enter `4b3fba` as the Configuration ID.
### or via DNS Over HTTPS (Windows 11 Only)
- Open the Settings app
- Go to Network & Internet
- Click on WiFi (or Ethernet)
- Click on Hardware Properties (or ignore this if you clicked Ethernet)
- Click the Edit button next to DNS Server Assignment
- Select Manual
- Enable IPv4
- Enter `45.90.28.0` as Preferred DNS, then select On (manual template) and enter `https://dns.nextdns.io/4b3fba`
- Enter `45.90.30.0` as Alternate DNS, then select On (manual template) and enter `https://dns.nextdns.io/4b3fba`
- Click Save
## Linux
### Via systemd-resolved (Recommended)
- Use the following in /etc/systemd/resolved/.conf:<br>
```
[Resolve]
DNS=45.90.28.0#4b3fba.dns.nextdns.io
DNS=2a07:a8c0::#4b3fba.dns.nextdns.io
DNS=45.90.30.0#4b3fba.dns.nextdns.io
DNS=2a07:a8c1::#4b3fba.dns.nextdns.io
DNSOverTLS=yes
```

## ChromeOS
### Via Secure DNS (Recommended)
- Open the Settings app
- Go to Security and Privacy
- Enable "Use Secure DNS"
- Select "With:Custom" and enter `https://dns.nextdns.io/4b3fba`

## Routers
- Utilize [NextDNS CLI](https://github.com/nextdns/nextdns/wiki).

# Included Blocklists
### NextDNS Ads & Trackers Blocklist
A comprehensive blocklist to block ads & trackers in all countries.<br>
- 151,328 entries.<br>
### AdGuard DNS Filter
A filter composed of several other filters (AdGuard Base filter, Social Media filter, Tracking Protection filter, Mobile ads filter, EasyList, and EasyPrivacy) and simplified specifically to be better compatible with DNS-level adblocking.<br>
- 57,007 entries.<br>
https://github.com/AdguardTeam/AdguardSDNSFilter
### OISD
Internet's #1 domain blocklist. Blocks Ads, Mobile Ads, Phishing, Malvertising, Malware, Tracking, Telemetry, Cryptojacking, Analyitics, Spyware, Ransomware, Misleading Marketing, etc.
- 221,708 entries. <br>
https://oisd.nl
### AdGuard Extended Mobile Ads Filter
Filter that blocks ads on mobile devices. Contains all known mobile ad networks.
- 851 entries.<br>
https://kb.adguard.com/general/adguard-ad-filters#mobile-ads-filter
### Goodbye Ads
Specifically designed for mobile ad protection.
- 400,655 entries<br>
  https://github.com/jerryn70/GoodbyeAds
