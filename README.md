# δb‎ ‎ ‎ DeltaBlock
### More than just an adblocker.
DeltaBlock is a powerful DNS-based configuration for adblocking, phishing protection and increased privacy.<br>
Powered by [NextDNS](https://nextdns.io)<br>
A project by [@gabefletch](https://github.com/gabefletch)<br>
### Latest Changes
**v3.0.1.1** - 1/30/25 - Adds additional Google APIs, YouTube, and miscellaneous backend domains to the Allowlist for increased compatibility without sacrificing blocking effectiveness. See changelog for domain list.<br> 
[View Changelog](https://github.com/gabefletch/DeltaBlock/blob/main/changelog.md)


<details closed>
<summary>List of Supported Platforms (click)</summary>
<br>
iOS<br>
Android<br>
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

## [➤ Installation Instructions](https://github.com/gabefletch/DeltaBlock/wiki)


> [!IMPORTANT]
> DeltaBlock is a DNS configuration profile specifically designed for use with [NextDNS](https://nextdns.io) which has its own pricing model that DeltaBlock does not control. NextDNS limits unpaid users to 300,000 filtered queries per month. In other words, after 300,000 requests are blocked by DeltaBlock, nothing will continue being blocked until the next month. NextDNS offers unlimited queries and devices starting at $1.99 USD per month. Using the DeltaBlock custom config, however, is completely free.

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
Direct support for other DNS services is planned in the future, but no official support exists for DeltaBlock on any service other than NextDNS currently. It is possible to utilize the [NextDNS CLI](https://github.com/nextdns/nextdns/wiki) or export the domain list used by DeltaBlock using third party tools to achieve this. We plan to provide a method to easily use DeltaBlock with other DNS services in the future.
### What Happened to the Blocking Percentage?
Prior to v3.0 of DeltaBlock, Adblock Test Toolz by d3ward was used to calculate DeltaBlock's capability of blocking ads. d3ward has since decided to stop maintaining this test, and so no blocking percentage is displayed anymore for the sake of maintaining transparency with DeltaBlock's userbase. Using other tests isn't feasible because almost all of them are designed to test extension-based adblockers and filters instead of taking into account DNS-based filtering like Adblock Toolz did.
### Why Should I Use DeltaBlock and not Just a Browser-based Adblocker?
Because DeltaBlock is a DNS service, it blocks ads across every app on your device instead of being confined to just your browser. The greatest use for this is in-app adblocking on iOS and Android devices. We recommend that you use DeltaBlock and a browser-based adblocker (such as uBlock Origin or uBlock Lite) in tandem with one another to get rid of visual leftovers caused as a result of ads not loading (cosmetic filtering).
### Find something wrong?
Feel free to open an Issue in this GitHub repo. 
