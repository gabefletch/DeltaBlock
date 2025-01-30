# DeltaBlock Master Changelog
## v3.0.1.1
30 January 2025
- Adds additional Google APIs, YouTube, and miscellaneous backend domains to the Allowlist for increased compatibility without sacrificing blocking effectiveness.
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

o.pki.goog
  
ggpht.cn

googlevideo.com

wide-youtube.l.google.com

withyoutube.com

clients.google.com

www.msftconnecttest.com

connectivitycheck.android.com

connectivitycheck.gstatic.com

continuum.dds.microsoft.com

vidtech.cbsinteractive.com

appspot-preview.l.google.com

</details>

## v3.0.1
26 January 2025
- Adds additional domains to the Allowlist based on lists from Pi-hole Community, anudeepND, and Firebog for better compatibility in circumstances where DeltaBlock intercepts non-ad-serving domains.
- This update also addresses circumstances where YouTube History may have still occasionally been blocked from being saved properly; v3.0.1 will allow YouTube History to be saved 100% of the time.
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

gfwsl.geforce.com
  
livepassdl.conviva.com

cws.conviva.com

pings.conviva.com

zee.cws.conviva.com

yt3.ggpht.com

youtube-nocookie.com

youtu.be

xts.auth.xboxlive.com

xkms.xboxlive.com

xflight.xboxlive.com

xboxexperiencesprod.experimentation.xboxlive.com

xbox.ipv6.microsoft.com

www.youtube-nocookie.com

www.no-ip.com

www.msftncsi.com

www.googleapis.com

www.dataplicity.com

ws.audioscrobbler.com

wp.com

win10.ipv6.microsoft.com

widget-cdn.rpxnow.com

videos.vidible.tv

ui.skype.com

twimg.com

tvthemes.plexapp.com

tvdb2.plex.tv

traffic.libsyn.com

title.mgt.xboxlive.com

title.auth.xboxlive.com

tinyurl.com

thetvdb.com

themoviedb.com

tedcdn.com

tawk.to

t0.ssl.ak.tiles.virtualearth.net

t0.ssl.ak.dynamic.tiles.virtualearth.net

t.co

status.plex.tv

staging.plex.tv

ssl.p.jwpcdn.com

spclient.wg.spotify.com

skyhook.sonarr.tv

services.sonarr.tv

secure.surveymonkey.com

secure.brightcove.com

secure.avangate.com

sa.symcb.com

s3.amazonaws.com

s2.youtube.com

s1.wp.com

s.ytimg.com

s.marketwatch.com

s.gateway.messenger.live.com

res.cloudinary.com

redirector.googlevideo.com

raw.githubusercontent.com

pubsub.plex.tv

pubsub.plex.bz

proxy02.pop.ord.plex.bz

proxy.plex.tv

proxy.plex.bz

products.office.com

pricelist.skype.com

players.brightcove.net

placeholdit.imgix.net

placehold.it

outlook.office365.com

outlook.live.com

onedrive.live.com

om.cbsi.com

officeclient.microsoft.com

office365.com

office.net

office.com

ocsp.apple.com

o2.sg0.plex.tv

o1.email.plex.tv

ns2.dropbox.com

ns1.dropbox.com

notify.xboxlive.com

node.plexapp.com

no-ip.com

nine.plugins.plexapp.com

npr-news.streaming.adswizz.com

nexusrules.officeapps.live.com

my.plexapp.com

msft.ncsi.com

microsoftonline.com

meta.plex.tv

meta.plex.bz

meta-db-worker02.pop.ric.plex.bz

manifest.googlevideo.com

login.microsoftonline.com

login.live.com

live.com

licensing.xboxlive.com

lastfm-img2.akamaized.net

keystone.mwbsys.com

jsdelivrnet

jquery.com

intercom.io

instantmessaging-pa.googleapis.com

imgs.xkcd.com

imgix.net

imagesak.secureserver.net

i1.ytimg.com

i.ytimg.com

hls.ted.com

help.ui.xboxlive.com

gstatic.com

gravatar.com

github.io

github.com

giphy.com

geo3.ggpht.com

geo-prod.do.dsp.mp.microsoft.com

g.live.com

forums.sonarr.tv

fonts.gstatic.com

eds.xboxlive.com

edge.api.brightcove.com

ecn.api.brightcove.com

ecn.dev.virtualearth.net

dynupdate.no-ip.com

driftt.com

drift.com

download.sonarr.tv

dns.msftnci.com

dl.dropboxusercontent.com

dl.dropbox.com

dl.delivery.mp.microsoft.com

displaycatalog.mp.microsoft.com

display.ugc.bazaarvoice.com

device.auth.xboxlive.com

dev.virtualearth.net

delivery.vidible.tv

def-vef.xboxlive.com

dataplicity.com

dashboard.plex.tv

d2gatte9o95jao.cloudfront.net

d2c8v52ll5s99u.cloudfront.net

ctdl.windowsupdate.com

cse.google.com

cpms35.spop10.ams.plex.bz

cpms.spop10.ams.plex.bz

jnn-pa.googleapis.com

clients6.google.com

clients5.google.com

clients3.google.com

clients1.google.com

clientconfig.passport.net

cert.mgt.xboxlive.com

cdnjs.cloudflare.com

cnd3.optimizely.com

cn2.optimizely.com

cdn.vidible.tv

cdn.embedly.com

cdn.cloudflare.net

c.s-microsoft.com

brightcove.net

ax.phobos.apple.com.edgesuite.net

attestation.xboxlive.com

aspnetcdn.com

apt.sonarr.tv

appsbackup-pa.googleapis.com

appsbackup-pa.clients6.google.com

apps.skype.com

appleid.apple.com

app-api.ted.com

api.rlje.net

api.ipify.org

android.clients.google.com

</details>

## v3.0
26 January 2025
- Fixes an issue where YouTube watch history (and possibly other Google Account related history) would not save or be displayed properly when using DeltaBlock by adding `myactivity.google.com`, among others, to the Allowlist.
- Adds support for NextDNS Command-Line installation for Linux and macOS
- Adds support for dnsmasq, Stubby, DNSCrypt, Knot Resolver, cloudflared, and Unbound for installation on Linux and Routers
- Adds support for pfSense, MikroTik, and tailscale for installation on Routers
- Introduces new Router installation setup for Routers capable of running executables (NextDNS for Routers)
- Deprecates usage of NextDNS CLI for Router installation
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

amazonaws.com

akamaized.com

akamaitechnologies.com

akamaihd.net

2.android.pool.ntp.org

1drv.com

0.client-channel.google.com

oauthaccountmanager.googleapis.com

youtubei.googleapis.com

googleapis.com

clients2.google.com

clients4.google.com

video-stats.l.google.com

s.youtube.com

accounts.youtube.com

myactivity.google.com

</details>

## v2.4
19 September 2024
- Adds additional safe domains to the Allow List that previously prevented Facebook and Meta Accounts from working as intended.
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

fbinfra.net

fb.com

fbpigeon.com

fbsbx.com

facebook.net

fbcdn.net

facebook.com

</details>

## v2.3.1
16 September 2024
- Adds several misc. safe domains to the Allow List.
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

fmhy.net

opera.com

dub.co

dub.sh

</details>

## v2.3
11 March 2024
- Adds several major ad-related and analytics-related domains to the Denylist, now reaching up to 100% blocking capability on the Toolz Adblock Test for the first time
<details closed>
<summary>Domains added to Denylist (click) </summary>
<br>

pagead2.googlesyndication.com

adservice.google.com

pagead2.googleadservices.com

static.media.net

media.net

doubleclick.net

ad.doubleclick.net

static.doubleclick.net

m.doubleclick.net

mediavisor.doubleclick.net

fastclick.com

adtogo.s3.amazonaws.com

assoc-amazon.com

google-analytics.com

ssl.google-analytics.com

hotjar.com

static.hotjar.com

a.mouseflow.com

freshmarketer.com

ads.facebook.com

pixel.facebook.com

ads.pinterest.com

ads-dev.pinterest.com

trk.pinterest.com

analytics.pinterest.com

ads.reddit.com

rereddit.com

events.redditmedia.com

ads.youtube.com

analytics.tiktok.com

ads.tiktok.com

ads.yahoo.com

global.adserver.yahoo.com

analytics.yahoo.com

ads.yap.yahoo.com

appmetrica.yandex.com

yandexadexchange.net

analytics.mobile.yandex.net

app.chat.xiamoi.net

globalapi.ad.intl.xiaomi.com

cdn.ad.xiamoi.com

tracking.miui.com

tracking.intl.miui.com

metrics1.data.hicloud.com

metrics3.data.hicloud.com

metrics4.data.hicloud.com

metrics5.data.hicloud.com

metrics-dra.dt.hicloud.com

ad.samsungadhub.com

samsungadhub.com

business.samsungusa.com

analytics.samsungknox.com

config.samsungads.com

securemetrics.apple.com

supportmetrics.apple.com

metrics.icloud.com

metrics.mzstatic.com

</details>

## v2.2.1
10 March 2024
- Reverts some domains added to the Denylist with v2.2 in order to address some non-ad images loading incorrectly or not at all.
<details closed>
<summary>Domains added to Allowlist (click) </summary>
<br>

instagram.ford1-1.fna.fbcdn.net

instagram.c10r.facebook.com

white.ish.instagram.com

telegraph-ash.instagram.com

edge-mqtt.facebook.com

mqtt.c10r.facebook.com

my.matterport.com

connect.facebook.net

static.matterport.com

beacons.gvt2.com

yt3.ggpht.com

</details>

## v2.2
20 February 2024
- Adds several Meta (Facebook) related domains to the Allowlist to address proper connectivity to Meta Services (ie. Facebook, Instagram)
- Adds domains used for loading "Sponsored" image content on Instagram to the Denylist to attempt to add Instagram adblocking capability to DeltaBlock.

## v2.1.1
31 January 2024
- Adds sendgrid.net to the Allowlist to fix issues with trusted email-based redirects.

## v2.1
29 January 2024
- Adds several OEM related ad-serving domains from smartphone manufacturers including Realme, Xiaomi, Huawei (more), OnePlus, Samsung, and Apple (more) from the Adblock Toolz d3Host list to the Denylist.

## v2.0.1
26 January 2024
- Adds netlify.com and app.netlify.com to the Allowlist to address reported issues with accessing Netlify.

## v2.0
5 December 2023
- Integrates NextDNS "Block Bypass Methods" tool in order to prevent or hinder the use of methods that can help bypass DNS filtering on a network. This includes VPNs, proxies, Tor-related software, and encrypted DNS providers. Those who typically use more restrictive public networks, or home networks with restrictive ISPs may now be able to properly use DeltaBlock.

## v1.2
10 November 2023
- Adds click.discord.com to the Allowlist to address errors connecting to Discord's account verification servers.
- Ability to view DeltaBlock's Allowlist is added to this repository.

## v1.1
3 November 2023
- Adds several domains to the Denylist to compliment domains not covered by Thirdparty Blocklists.
- Ability to view DeltaBlock's Denylist is added to this repository.

## v1.0.1
2 November 2023
- Integrates the following Thirdparty Blocklists:
  - antipopads
  - HaGeZi - Multi ULTIMATE
  - Energized Ultimate
  - hBlock
 
## v1.0
1 November 2023
- Initial launch.
