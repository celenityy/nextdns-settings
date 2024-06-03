# nextdns-setup

My recommendations for the ultimate NextDNS Set-up :)

# Security

**Use Threat Intelligence Feeds** -> ✅

**Enable AI-Driven Threat Detection** -> ✅

**Enable Google Safe Browsing** -> ✅

**Enable Cryptojacking Protection** -> ✅

**Enable DNS Rebinding Protection** -> ✅

**Enable IDN Homograph Attacks Protection** -> ✅

**Enable Typosquatting Protection** -> ✅

**Enable DGA Protection** -> ✅

**Block Newly Registered Domains (NRDs)** -> ✅ (This will cause very rare breakage, but massively improves security)

**Block Dynamic DNS Hostnames** -> ✅

**Block Parked Domains** -> ✅

**Block Top-Level Domains (TLDs)** -> 

I would recommend taking a look at blocking TLDs from HaGeZi's "Most Abused TLDs" list [here](https://gitlab.com/hagezi/mirror/-/raw/main/dns-blocklists/adblock/spam-tlds.txt). Block whatever works best for you, but this can do a lot to increase security.

**Block Child Sexual Abuse Material** -> ✅ (Apologies to the pedos in the audience...)

# Privacy

**Blocklists** ->

Here's where it gets fun.

Despite popular opinion, due to the reasons WaLLy3K has listed [here](https://github.com/WaLLy3K/wally3k.github.io?tab=readme-ov-file#why-use-this-over-other-sources), I think it's a good idea to use multiple lists and sources, rather than just limiting yourself to one or two giant lists. I myself constantly notice domains being blocked that were caught by only one list and missed by others. I'm not saying you should go overboard, but I do think it's a good idea to use a variety of high quality lists.

I would generally recommend using the following lists:

* AdAway
* AdGuard DNS filter
* Anudeep's Blacklist for ads and trackers
* CAMELEON
* EasyList 
* EasyPrivacy
* Fanboy's Annoyance List
* HaGeZi Multi Pro++
* hBlock
* hostsVN
* Lightswitch05 - Ads & Tracking
* NextDNS Ads & Trackers Blocklist (Enabled by default)
* NSABlocklist
* OISD
* Personal Blocklist by WaLLy3K
* Peter Lowe
* someonewhocares.org (Dan Pollock)
* Steven Black

It might seem like a lot, but these are high quality lists with strong coverage, and it doesn't hurt using multiple.

Additionally, if you're fine with a little breakage, I would highly recommend:

* 1Hosts (Pro)
* HaGeZi - Multi ULTIMATE instead of HaGeZi Multi Pro++
* Lightswitch05 - Tracking Aggressive instead of Lightswitch05 - Ads & Tracking
* No Facebook - Obviously don't use if you use any Facebook services

**Native Tracking Protection** -> ✅

You should generally just enable whatever devices you have in here. 

Regardless though, I would always recommend enabling "Amazon Alexa", as it seems to block various Amazon trackers found in their other apps/services, even if you don't have an Alexa.

**Block Disguised Third-Party Trackers** -> ✅

**Allow Affiliate & Tracking Links** -> ✅ (See "Denylist" section below)

# Parental Control

**Websites, Apps & Games** -> You should add in here any services you don't use or care about. For instance, I usually block TikTok, Facebook, Instagram, Messenger, & WhatsApp, as I don't use or care about any Facebook or TikTok services, and I don't want to connect to or be tracked by them.

# Denylist

Remember how we allowed affiliate & tracking links above?

While this is nice from a usability perspective, this does also allow some questionable ad/tracking domains that we don't want unblocked. I would recommend taking a look at [the allowlist NextDNS is using](https://github.com/nextdns/click-tracking-domains/blob/main/domains) and I would definitely add the following to your denylist:

* ad.doubleclick.net
* adclick.g.doubleclick.net
* The google adservice domain from the list corresponding to your region/that you run into
* adservice.google.com
* amazon-adsystem.com
* analytics.twitter.com
* app.adjust.com
* dart.l.doubleclick.net
* pagead.l.doubleclick.net
* www.googleadservices.com

Note that I maintain a variety of comprehensive blocklists [here](https://codeberg.org/Magnesium1062/blocklists/). Sadly you won't be able to add them to NextDNS, but you may skim through them and manually block whatever you wish to.

Regardless, if you use Apple devices, I would recommend blocking:

* idiagnostics.apple.com
* pancake.apple.com
* xp.apple.com 
* xp-cdn.apple.com

# Allowlist