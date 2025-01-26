# δb‎ ‎ ‎ DeltaBlock

### Readme Contents
[Installation](https://github.com/gabefletch/DeltaBlock#installation)<br>
[Changes](https://github.com/gabefletch/DeltaBlock#changes)<br>
[Frequently Asked Questions](https://github.com/gabefletch/DeltaBlock#FAQ)<br>

A custom DNS profile for NextDNS capable of blocking up to 99%* of ads.<br>
DeltaBlock stops both web-based and in-app ads from loading.<br>
A project by [@gabefletch](https://github.com/gabefletch).<br>

<details closed>
<summary>Click for List of Supported Platforms</summary>
<br>
macOS<br>
Windows<br>
Redhat<br>
Fedora<br>
CentOS<br>
Debian<br>
Ubuntu<br>
Raspbian<br>
Alpine<br>
Arch Linux<br>
Manjaro<br>
Nix<br>
OpenSUSE<br>
Solus<br>
FreeBSD<br>
NetBSD<br>
OpenBSD<br>
OpnSense<br>
DragonFly<br>
OpenWRT<br>
AsusWRT-Merlin<br>
pfSense<br>
Ubiquiti EdgeOS / USG<br>
Ubiquiti UnifiOS / UDM Family / UXG Family<br>
VyOS<br>
Synology DiskStation Manager DSM<br>
Synology Router Manager SRM<br>
DD-WRT<br>
</details>

### Notice for New NextDNS Users
DeltaBlock is only designed for use via NextDNS, which is limited to 300,000 queries per month without a subscription. The lowest tier with unlimited queries is available for $1.99/month. Using the DeltaBlock custom profile, however, is completely free.

### NextDNS Affiliate Link
Help DeltaBlock remain running by sharing this link:
https://nextdns.io/?from=pyukpkuc

### Services With Anti-Adblocking Measures
DeltaBlock, like most adblockers, can be detected by sites with anti-adblock measures. YouTube on both mobile and desktop sites and some news sites are the most common examples of this. In other words, DeltaBlock cannot work properly on every site. If you're looking to get past adblock detection on YouTube, [see this guide](https://github.com/psychon-night/bypass-youtube-adblock-blocker/tree/main).<br>

*According to Toolz AdBlock Test. This percentage varies depending on network variables. DeltaBlock stops an average of 96% of ads at all times based on testing between both iOS and macOS devices. The lowest percentage resulting from testing has been 93%, under strenuous network variables with ad-heavy pages.<br>

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
### or via NextDNS Command-Line Client (macOS)
- Run `sh -c "$(curl -sL https://nextdns.io/install)"`
- Follow the instructions, and use `4b3fba` as the Configuration ID if prompted.
## Windows
### Via DNS Over HTTPS (Windows 11 Only)
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
### or via NextDNS App (Not Recommended)
- Install the NextDNS app by [clicking here](https://nextdns.io/download/windows/stable).
- Enter the settings for NextDNS and enter `4b3fba` as the Configuration ID.
### or via YogaDNS (Advanced)
- Install YogaDNS by [clicking here](https://yogadns.com).
- Follow the instructions for NextDNS at [yogadns.com/docs/nextdns](https://yogadns.com/docs/nextdns) and use `4b3fba` as the Configuration ID.

## Linux
### Via systemd-resolved
- Use the following in /etc/systemd/resolved/.conf:<br>
```
[Resolve]
DNS=45.90.28.0#4b3fba.dns.nextdns.io
DNS=2a07:a8c0::#4b3fba.dns.nextdns.io
DNS=45.90.30.0#4b3fba.dns.nextdns.io
DNS=2a07:a8c1::#4b3fba.dns.nextdns.io
DNSOverTLS=yes
```
### or via NextDNS Command-Line Client
- Run `sh -c "$(curl -sL https://nextdns.io/install)"`
- Follow the instructions, and use `4b3fba` as the Configuration ID if prompted.
### or via dnsmasq
- Use the following dnsmasq.conf:
```
no-resolv
bogus-priv
strict-order
server=2a07:a8c1::
server=45.90.30.0
server=2a07:a8c0::
server=45.90.28.0
add-cpe-id=4b3fba
```
### or via Stubby
- Use the following in stubby.yml:
```
round_robin_upstreams: 1
upstream_recursive_servers:
  - address_data: 45.90.28.0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 2a07:a8c0::0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 45.90.30.0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 2a07:a8c1::0
    tls_auth_name: "4b3fba.dns.nextdns.io"
```
***Make sure Stubby is linked with OpenSSL 1.1.1 or higher as previous versions will not work with NextDNS or DeltaBlock.***
### or via DNSCrypt
- Use the following in dnscrypt-proxy.toml:
```
server_names = ['NextDNS-4b3fba']

[static]
  [static.'NextDNS-4b3fba']
  stamp = 'sdns://AgEAAAAAAAAAAAAOZG5zLm5leHRkbnMuaW8HLzRiM2ZiYQ'
```
### or via Knot Resolver
- Use the following in /etc/kresd/custom.conf:
```
policy.add(policy.all(policy.TLS_FORWARD({
  {'45.90.28.0', hostname='4b3fba.dns.nextdns.io'},
  {'2a07:a8c0::', hostname='4b3fba.dns.nextdns.io'},
  {'45.90.30.0', hostname='4b3fba.dns.nextdns.io'},
  {'2a07:a8c1::', hostname='4b3fba.dns.nextdns.io'}
})))
```
### or via cloudflared
- Use the following in /usr/local/etc/cloudflared/config.yml:
```
proxy-dns: true
proxy-dns-upstream:
 - https://dns.nextdns.io/4b3fba
```
### or via Unbound
- Use the following in unbound.conf:
```
forward-zone:
  name: "."
  forward-tls-upstream: yes
  forward-addr: 45.90.28.0#4b3fba.dns.nextdns.io
  forward-addr: 2a07:a8c0::#4b3fba.dns.nextdns.io
  forward-addr: 45.90.30.0#4b3fba.dns.nextdns.io
  forward-addr: 2a07:a8c1::#4b3fba.dns.nextdns.io
```
***As a recursive resolver, Unbound chases CNAMEs. This may result in unexpected behavior when used in conjunction with a blocking DNS resolver like NextDNS and DeltaBlock. Please see [NLnetLabs/unbound/issues/132](https://github.com/NLnetLabs/unbound/issues/132) for more information.***

## ChromeOS
### Via Secure DNS
- Open the Settings app
- Go to Security and Privacy
- Enable "Use Secure DNS"
- Select "With:Custom" and enter `https://dns.nextdns.io/4b3fba`

## Routers
### For Routers That Can Run Executables (Recommended)
- Follow instructions at [/nextdns/nextdns/wiki](https://github.com/nextdns/nextdns/wiki)
### or via IPv6
- [Test your IPv6 connectivity](https://test-ipv6.com/) before following these steps.
- Open the network preferences for your Router. This is usually accessed from your browser via a URL pointing to an IP Address.
- Locate the DNS settings inside the interface.
- Remove all addresses (if any), then add `2a07:a8c0::4b:3fba` and `2a07:a8c1::4b:3fba`.
- Click "Save" or equivalent.<br>

***Some Routers might not support the IPv6 notation above. In that case, use:***<br>
`2a07:a8c0:0000:0000:0000:0000:004b:3fba`<br>
and<br>
`2a07:a8c1:0000:0000:0000:0000:004b:3fba`<br>
### or via IPv4 (With Linked IP)
- Open the network preferences for your Router. This is usually accessed from your browser via a URL pointing to an IP Address.
- Locate the DNS settings inside the interface.
- Remove all addresses (if any), then add `45.90.28.32` and `45.90.30.32`.
- Click "save" or equivalent.
### or via dnsmasq
- Use the following in dnsmasq.conf:
```
no-resolv
bogus-priv
strict-order
server=2a07:a8c1::
server=45.90.30.0
server=2a07:a8c0::
server=45.90.28.0
add-cpe-id=4b3fba
```
### or via Stubby
```
round_robin_upstreams: 1
upstream_recursive_servers:
  - address_data: 45.90.28.0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 2a07:a8c0::0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 45.90.30.0
    tls_auth_name: "4b3fba.dns.nextdns.io"
  - address_data: 2a07:a8c1::0
    tls_auth_name: "4b3fba.dns.nextdns.io"
```
***Make sure Stubby is linked with OpenSSL 1.1.1 or higher as previous versions will not work with NextDNS or DeltaBlock.***
### or via pfSense
- Go to Services → DNS Resolver, and on the tab General Settings, scroll down to the Custom Options box.
- Enter the following:
```
server:
  forward-zone:
    name: "."
    forward-tls-upstream: yes
    forward-addr: 45.90.28.0#4b3fba.dns.nextdns.io
    forward-addr: 2a07:a8c0::#4b3fba.dns.nextdns.io
    forward-addr: 45.90.30.0#4b3fba.dns.nextdns.io
    forward-addr: 2a07:a8c1::#4b3fba.dns.nextdns.io
```
### or via DNSCrypt
- Use the following in dnscrypt-proxy.toml:
```
server_names = ['NextDNS-4b3fba']

[static]
  [static.'NextDNS-4b3fba']
  stamp = 'sdns://AgEAAAAAAAAAAAAOZG5zLm5leHRkbnMuaW8HLzRiM2ZiYQ'
```
### or via Knot Resolver
- Use the following in /etc/kresd/custom.conf:
```
policy.add(policy.all(policy.TLS_FORWARD({
  {'45.90.28.0', hostname='4b3fba.dns.nextdns.io'},
  {'2a07:a8c0::', hostname='4b3fba.dns.nextdns.io'},
  {'45.90.30.0', hostname='4b3fba.dns.nextdns.io'},
  {'2a07:a8c1::', hostname='4b3fba.dns.nextdns.io'}
})))
```
### or via Unbound
- Use the following in unbound.conf:
```
forward-zone:
  name: "."
  forward-tls-upstream: yes
  forward-addr: 45.90.28.0#4b3fba.dns.nextdns.io
  forward-addr: 2a07:a8c0::#4b3fba.dns.nextdns.io
  forward-addr: 45.90.30.0#4b3fba.dns.nextdns.io
  forward-addr: 2a07:a8c1::#4b3fba.dns.nextdns.io
```
***As a recursive resolver, Unbound chases CNAMEs. This may result in unexpected behavior when used in conjunction with a blocking DNS resolver like NextDNS or DeltaBlock. Please see [/NLnetLabs/unbound/issues/132](https://github.com/NLnetLabs/unbound/issues/132) for more information.***
### or via MikroTik
- Run the following:
```
/tool fetch url=https://curl.se/ca/cacert.pem
/certificate import file-name=cacert.pem
/ip dns set servers=""
/ip dns static add name=dns.nextdns.io address=45.90.28.0 type=A
/ip dns static add name=dns.nextdns.io address=45.90.30.0 type=A
/ip dns static add name=dns.nextdns.io address=2a07:a8c0:: type=AAAA
/ip dns static add name=dns.nextdns.io address=2a07:a8c1:: type=AAAA
/ip dns set use-doh-server=“https://dns.nextdns.io/4b3fba” verify-doh-cert=yes
```
### or via tailscale
- Follow instructions at [tailscale.com/kb/1218/nextdns](https://tailscale.com/kb/1218/nextdns) and use `4b3fba` as the Configuration ID for DeltaBlock.

# Changes
## v3.0.1
26 January 2025
- Adds additional domains to the Allowlist based on lists from Pi-hole Community, anudeepND, and Firebog for better compatibility. 
- This update addresses circumstances where YouTube History may have still occasionally been blocked from being saved properly; v3.0.1 will allow YouTube History to be saved 100% of the time.
## v3.0
26 January 2025
- Fixes an issue where YouTube watch history (and possibly other Google Account related history) would not save or be displayed properly when using DeltaBlock by adding `myactivity.google.com` to the Allowlist.
- Adds support for NextDNS Command-Line installation for Linux and macOS
- Adds support for dnsmasq, Stubby, DNSCrypt, Knot Resolver, cloudflared, and Unbound for installation on Linux and Routers
- Adds support for pfSense, MikroTik, and tailscale for installation on Routers
- Introduces new Router installation setup for Routers capable of running executables (NextDNS for Routers)
- Deprecates usage of NextDNS CLI for Router installation
## v2.4
19 September 2024
- Adds additional safe domains to the Allow List that previously prevented Facebook and Meta Accounts from working as intended.
## v2.3.1
16 September 2024
- Adds several safe domains to the Allow List
## v2.3
11 March 2024
- Adds several major ad-related and analytics-related domains to the denylist, now reaching up to 100% blocking capability on the Toolz Adblock Test for the first time
- The following domains were added to the denylist:
  - `pagead2.googlesyndication.com`
  - `adservice.google.com`
  - `pagead2.googleadservices.com`
  - `static.media.net`
  - `media.net`
  - `doubleclick.net`
  - `ad.doubleclick.net`
  - `static.doubleclick.net`
  - `m.doubleclick.net`
  - `mediavisor.doubleclick.net`
  - `fastclick.com`
  - `adtogo.s3.amazonaws.com`
  - `assoc-amazon.com`
  - `google-analytics.com`
  - `ssl.google-analytics.com`
  - `hotjar.com`
  - `static.hotjar.com`
  - `a.mouseflow.com`
  - `freshmarketer.com`
  - `ads.facebook.com`
  - `pixel.facebook.com`
  - `ads.pinterest.com`
  - `ads-dev.pinterest.com`
  - `trk.pinterest.com`
  - `analytics.pinterest.com`
  - `ads.reddit.com`
  - `rereddit.com`
  - `events.redditmedia.com`
  - `ads.youtube.com`
  - `analytics.tiktok.com`
  - `ads.tiktok.com`
  - `ads.yahoo.com`
  - `global.adserver.yahoo.com`
  - `analytics.yahoo.com`
  - `ads.yap.yahoo.com`
  - `appmetrica.yandex.com`
  - `yandexadexchange.net`
  - `analytics.mobile.yandex.net`
  - `app.chat.xiaomi.net`
  - `glabalapi.ad.intl.xiaomi.com`
  - `cdn.ad.xiaomi.com`
  - `tracking.miui.com`
  - `tracking.intl.miui.com`
  - `metrics1.data.hicloud.com`
  - `metrics3.data.hicloud.com`
  - `metrics4.data.hicloud.com`
  - `metrics5.data.hicloud.com`
  - `metrics-dra.dt.hicloud.com`
  - `ad.samsungadhub.com`
  - `samsungadhub.com`
  - `business.samsungusa.com`
  - `analytics.samsungknox.com`
  - `config.samsungads.com`
  - `securemetrics.apple.com`
  - `supportmetrics.apple.com`
  - `metrics.icloud.com`
  - `metrics.mzstatic.com`
## v2.2.1
10 March 2024
- Disables a handful of the URLs added to the denylist in the previous update (v2.2) in order to address some non-ad images not loading properly
- The following domains are now allowed again:
   - `instagram.ford1-1.fna.fbcdn.net`
   - `instagram.c10r.facebook.com`
   - `white.ish.instagram.com`
   - `telegraph-ash.instagram.com`
   - `edge-mqtt.facebook.com`
   - `mqtt.c10r.facebook.com`
   - `my.matterport.com`
   - `connect.facebook.net`
   - `static.matterport.com`
   - `star-mini.c10r.facebook.com`
   - `beacons.gvt2.com`
   - `yt3.ggpht.com`
## v2.2
20 February 2024
- Adds several Meta related domains to attempt to address proper connectivity to Meta services (ie. Facebook, Instagram)
- Adds domains used for loading "Sponsored" image content on Instagram to attempt to add Instagram ad blocking capability to DeltaBlock
- The following domains were added:
    - `yt3.ggpht.com`
    - `adserver.snapads.com`
    - `adserver.shadow.snapads.com`
    - `beacons.gvt2.com`
    - `star-mini.c10r.facebook.com`
    - `static.matterport.com`
    - `connect.facebook.net`
    - `my.matterport.com`
    - `mqtt.c10r.facebook.com`
    - `edge-mqtt.facebook.com`
    - `telegraph-ash.instagram.com`
    - `white.ish.instagram.com`
    - `instagram.c10r.facebook.com`
    - `instagram.ford1-1.fna.fbcdn.net`
## v2.1.1
31 January 2024
- Adds `sendgrid.net` to the Allowlist to fix issues with trusted email-based redirects.
## v2.1
29 January 2024
- Adds several OEM related domains from smartphone manufacturers including Realme, Xiaomi, Oppo, Huawei (more), OnePlus, Samsung, and Apple (more) from the AdBlock Toolz d3Host list to the Allowlist.
## v2.0.1
26 January 2024
- Adds `netlify.com` and `app.netlify.com` to DeltaBlock's internal allowlist to address reported problems with accessing Netlify.
## v2.0
5 December 2023
- Integrates NextDNS "Block Bypass Methods" tool in order to prevent or hinder the use of methods that can help bypass DNS filtering on a network. This includes VPNs, proxies, Tor-related software, and encrypted DNS providers. Those who typically use more restrictive public networks, or home networks with restrictive ISPs may now be able to properly use DeltaBlock.
## v1.2
10 November 2023
- Adds `click.discord.com` to DeltaBlock's internal Allowlist to fix errors connecting to Discord's account verification servers with previous versions of DeltaBlock.
- You can now also [view DeltaBlock's Allowlist](https://github.com/gabefletch/DeltaBlock/blob/main/allowlist.md).
## v1.1
3 November 2023
- Adds several domains to DeltaBlock's internal Denylist to compliment domains not covered by existing Blocklists.
- Adds the ability to see DeltaBlock's internal Denylist in this GitHub repo.
## v1.0.1
2 November 2023
- Adds "antipopads," "HaGeZi - Multi ULTIMATE," "Energized Ultimate," and "hBlock" to the list of included blocklists.
## v1.0
1 November 2023
- Initial launch
# FAQ
### Should DeltaBlock replace my browser's adblocker extension?
No. While DeltaBlock has a high blocking percentage, DeltaBlock or any DNS-enabled adblocking system is not capable of getting rid of the site elements where an ad would load like uBlock Origin is capable of. In other words, only using DeltaBlock would block ads just fine, but empty spaces would still be present on the page where the ads would originally be.
### Can I use DeltaBlock along with an adblocker extension?
Yes, and we recommend this. See the above question.
### Why Do Some Blocklists say "0 Entries"?
This is most likely because the author of the blocklist forgot to enter a number for NextDNS to report the entry count when they added it. All blocklist information on this page is derived directly from their listing on NextDNS.
### Can I Use DeltaBlock without paying for NextDNS?
Yes, but you'll be limited to 300,000 queries per month, after which the effects of DeltaBlock will stop working until the next month. NextDNS offers unlimited queries starting at $1.99/month.
### Can I Use DeltaBlock With a Different DNS Service?
Direct support for other DNS services is planned in the future, but no official support exists for DeltaBlock on any service other than NextDNS currently. It is possible to utilize the [NextDNS CLI](https://github.com/nextdns/nextdns/wiki) or export the domain list used by DeltaBlock using third party tools to achieve this. We plan to directly provide this list in the future.
### Where Is The Blocking Perecentage Derived From?
All testing for blocking precentage is dervied from the open-source [Toolz Adblock Test](https://d3ward.github.io/toolz/adblock.html). This percentage is directly effected by differing network variables and may be skewed by the adblocker used by your browser along with DeltaBlock. The highest blocking percentage for DeltaBlock based on iOS and macOS devices is up to 99%. DeltaBlock's lowest internal testing percentage is 93%, although you may see lower numbers depending on your network environment.
### Why Should I Use DeltaBlock Instead of a Browser-based Adblocker?
Because DeltaBlock is a DNS service, it blocks ads across every app on your device instead of being confined to just your browser. The greatest use for this is in-app adblocking on iOS and Android devices. We recommend that you use DeltaBlock and a browser-based adblocker (such as uBlock Origin) in tandem with one another to get rid of visual leftovers caused as a result of ads not loading.
### Find something wrong?
Feel free to open an Issue in this GitHub repo. 
# NextDNS Protections
The following is a list of protections enabled via NextDNS on DeltaBlock's custom profile:
### Threat Intelligence Feeds
Blocks domains known to distribute malware, launch phishing attacks and host command-and-control servers using a blend of the most reputable threat intelligence feeds — all updated in real-time.
### AI-Driven Threat Protection `[Beta]`
Blocks millions of threats detected by NextDNS AI technology — a proprietary AI engine designed from the ground up for DNS with hundreds of signals, terabytes of training data and real-time decision making.
### Google Safe Browsing 
Blocks malware and phishing domains using Google Safe Browsing — a technology that examines billions of URLs per day looking for unsafe websites. Unlike the version embedded in some browsers, this does not associate your public IP address to threats and does not allow bypassing the block.
### Cryptojacking Protection
Prevents the unauthorized use of your devices to mine cryptocurrency.
### DNS Rebinding Protection
Prevents attackers from taking control of your local devices through the internet by automatically blocking DNS responses containing private IP adresses.
### IDN Homograph Attacks Protection 
Blocks domains that impersonate other domains by abusing the large character set made available with the arrival of Internationalized Domain Names (IDNs) — e.g. replacing the Latin letter "e" with the Cyrillic letter "е".
### Typosquatting Protection
Blocks domains registered by malicious actors that target users who incorrectly type a website address into their browser — e.g. gooogle.com instead of google.com.
### Domain Generation Algorithms (DGAs) Protection
Blocks domains generated by Domain Generation Algorithms (DGAs) seen in various families of malware that can be used as rendezvous points with their command and control servers. 
### Block Child Sexual Abuse Material 
Blocks domains hosting child sexual abuse material with the help of Project Arachnid, operated by the Canadian Centre for Child Protection. No information is transmitted back to Project Arachnid when a domain is blocked. 
