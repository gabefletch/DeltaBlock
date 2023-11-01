<img src="https://github.com/gabefletch/DeltaBlock/assets/38300939/02815979-f67d-4dee-8865-178973114236" width=400><br>


A custom DNS profile for NextDNS (list also available) capable of blocking up to 99%* of ads.<br>
DeltaBlock stops both web-based and in-app ads from loading.<br>

*According to Toolz AdBlock Test.<br>

# Installation
## iOS, iPadOS, macOS, Windows, Android
### Via NextDNS App (Recommended)
- Install the NextDNS app on your device of choice
(Available for iOS, iPadOS, macOS, Windows, Android)
- Enter the settings for NextDNS and enter `4b3fba` as the Configuration ID.
### Via Apple Config File
(Apple Devices Only)
- [Click here](https://apple.nextdns.io/?profile=4b3fba) to be taken for the NextDNS Apple Config Profile generator for DeltaBlock.
- Download and install the profile via the Settings app.
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
A comprehensive blocklist to block ads & trackers in all countries. This is the recommended starter blocklist.<br>
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
