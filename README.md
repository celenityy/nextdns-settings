# nextdns-settings

My recommendations for the ultimate NextDNS Configuration :)

**NOTE:** This project can be found on both [Codeberg](https://codeberg.org/celenity/nextdns-settings), which will act as the main & preferred way to contribute, and [GitHub](https://github.com/celenityy/nextdns-settings).

# Security

**Use Threat Intelligence Feeds** -> ✅

**Enable AI-Driven Threat Detection** -> ✅

**Enable Google Safe Browsing** -> ✅ **Even with this setting, you should still ENABLE Safe Browsing in your browser. This list is limited exclusively to domains, while browser Safe Browsing can also check downloaded files.**

**Enable Cryptojacking Protection** -> ✅

**Enable DNS Rebinding Protection** -> ✅

**Enable IDN Homograph Attacks Protection** -> ✅

**Enable Typosquatting Protection** -> ✅

**Enable DGA Protection** -> ✅

**Block Newly Registered Domains (NRDs)** -> ✅ *(This will cause very rare breakage, but massively improves security)*

**Block Dynamic DNS Hostnames** -> ✅

**Block Parked Domains** -> ✅

**Block Top-Level Domains (TLDs)** -> 

I would recommend taking a look at blocking TLDs from HaGeZi's "Most Abused TLDs" list [here](https://gitlab.com/hagezi/mirror/-/raw/main/dns-blocklists/adblock/spam-tlds.txt). Block whatever works best for you. This can be tedious, but does a lot to heavily reduce risk of malicious websites. *(I've seen this work in real-time, blocking scam/spam domains before they were picked up by any lists)*.

**Block Child Sexual Abuse Material** -> ✅ *(Apologies to the pedos in the audience...)*

# Privacy

**Blocklists** ->

Here's where it gets fun.

Despite popular opinion, due to the reasons WaLLy3K has listed [here](https://github.com/WaLLy3K/wally3k.github.io?tab=readme-ov-file#why-use-this-over-other-sources), I think it's a good idea to use multiple lists and sources, rather than just limiting yourself to one or two giant lists. I myself constantly notice domains being blocked that were caught by only one or two lists and missed by others. **I'm not saying you should go overboard, but I do think it's a good idea to use a variety of high quality lists for the best coverage possible.**

I would generally recommend using the following:

* ⭐️ `AdAway`

* ⭐️ `AdGuard DNS filter`

* ⭐️ `Anudeep's Blacklist for ads and trackers`

* ⭐️ `CAMELEON`

* ⭐️ `EasyList`

* ⭐️ `EasyPrivacy`

* ⭐️ `Fanboy's Annoyance List`

* ⭐️ `HaGeZi Multi Pro++`

* ⭐️ `hBlock`

* ⭐️ `hostsVN`

* ⭐️ `Lightswitch05 - Ads & Tracking`

* ⭐️ `NextDNS Ads & Trackers Blocklist` *(Enabled by default)*

* ⭐️ `NSABlocklist`

* ⭐️ `OISD`

* ⭐️ `Perflyst's Smart-TV Blocklist`

* ⭐️ `Personal Blocklist by WaLLy3K`

* ⭐️ `Peter Lowe`

* ⭐️ `someonewhocares.org (Dan Pollock)`

* ⭐️ `Steven Black`

* ⭐️ `WindowsSpyBlocker (Spy)`

It might seem like a lot, but these are high quality lists with strong coverage and minimal false positives in my experience, and it generally doesn't hurt to use them like this.

Additionally, if you're fine with a little breakage, I would highly recommend:

* ❓ `1Hosts `**(Pro)** 

* ❓ `HaGeZi - Multi `**Ultimate** instead of `HaGeZi Multi `**Pro++**

* ❓ `No Facebook` - *(Obviously don't use if you use any Facebook services)*

<br>

**Native Tracking Protection** ->

I would recommend enabling the following **in addition** to any devices you have that are listed:

* ⭐️ `Windows` *(Blocks Microsoft trackers, not exclusive to Windows)*

* ⭐️ `Amazon Alexa` *(Blocks Amazon trackers, not exclusive to Alexa)*

<br>

**Block Disguised Third-Party Trackers** -> ✅

**Allow Affiliate & Tracking Links** -> ✅ (See `Denylist` section below)

# Parental Control

**Websites, Apps & Games** -> You should use this feature to your advantage and block any services that you don't use or care about. This can dramatically improve your privacy by preventing connections to them from even being made. If you use a service, don't block it, just block what you're comfortable with and works best for you.

I usually block the following:

* `TikTok`

* `Snapchat`

* `Facebook`

* `Instagram`

* `VK`

* `Messenger`

* `WhatsApp`

* `Spotify`

# Denylist

Remember how we allowed affiliate & tracking links above?

While this is nice from a usability perspective, this does also allow some questionable ad/tracking domains that we don't want unblocked. I would recommend taking a look at [the allowlist NextDNS is using](https://github.com/nextdns/click-tracking-domains/blob/main/domains) and I would definitely add the following to your denylist:

* `ad.doubleclick.net`
* `adclick.g.doubleclick.net`
* The google adservice domain from the list corresponding to your region/that you run into
* `adservice.google.com`
* `amazon-adsystem.com`
* `analytics.twitter.com`
* `app.adjust.com`
* `dart.l.doubleclick.net`
* `pagead.l.doubleclick.net`
* `www.googleadservices.com`

Note that I maintain a variety of comprehensive blocklists [here](https://badblock.celenity.dev). Sadly you won't be able to add them to NextDNS, but you may skim through them and manually block whatever you wish to.

# Allowlist

Note that I maintain a comprehensive whitelist [here](https://badblock.celenity.dev/whitelist.txt). Sadly you won't be able to add it to NextDNS, but you may skim through it and manually allow whatever you wish to.

Regardless, you should allow the following for updates on Fedora Linux:

```sh
mirror.arizona.edu
```

You should also always allow `nextdns.io`, as this will ensure we can always access the dashboard, regardless of any rogue filters or unexpected events that could occur.

# Settings

**Enable Logs** -> ✅ *(Having logs on is important for troubleshooting breakage)*

**Log clients IPs** -> ❌

**Log domains** -> ✅

**Retention** -> `1 hour` *(This will allow us to easily troubleshoot breakage, without keeping data for longer than necessary)*

**Storage location** -> `Switzerland`

**Enable Block Page** -> ❌ *(⚠️ Please **NEVER** enable this. This causes lots of issues and weird breakage, and also heavily reduces security through compromising HTTPS)*

**Enable Anonymized EDNS Client Subnet** -> ❌ 

**Enable Cache Boost** -> ✅

**Enable CNAME Flattening** -> ✅

**Enable Web3** -> ❌ *if you don't use/need it*

# Account *(Select your email address in the top right corner)*

**Two-Factor Authentication (2FA)** -> ✅


# Connectivity Issues for Apple Devices

Due to quirks with how iOS & macOS handle Encrypted DNS profiles, out of the box, you may experience issues with Captive Portals, Connecting to Public Wi-Fi Networks (Including ones on airplanes), MMS, Visual Voicemail, & Wi-Fi Calling. This happens with any Encrypted DNS provider, so it is not limited to NextDNS. The NextDNS app itself is *probably* not impacted by this - **though using the app is not recommended if you can help it, as it is unnecessary, closed source, increases your attack surface, & rarely updated.**

Luckily, there's a simple fix to this issue.

When generating your NextDNS profile [here](https://apple.nextdns.io/), you want to go **More Options** -> `Excluded Domains`. 

In this box, you'll want to copy & paste the following:

```sh
02.co.uk, 1und1-mobilfunk.de, 2degreesmobile.net.nz, 3.dk, 3g-d-2.ocn.ne.jp, 3gmms.nextel3g.net.br, 3gmms.nexteldata.com.mx, 3gmms.nextelmovil.cl, 3gmms.pccwmobile.com, 3g.mobac.net, 3g.utel.ua, 3gpp.org, 3gppnetwork.org, 3ireland.ie, 3pty-factory.ims.mnc051.mcc440.3gppnetwork.org, 412.com.ve, 48months.liffeytelecom.com, 4g.entel, 4g.mycricket.com, 4g.tele2.se, 8ta.com, a1.net, a2bouygtel.com, aainflight.com, abblamms.telia.se, abbla.telia.se, ab.kyivstar.net, acsalaska.net, action.ooredoo.com, action.wataniya.com, active.bhmobile.ba, ad.vodafone.co.uk, admin.cs4glte.com, aina.fi, aiowireless.net, airborne.gogoinflight.com, airfiremobile.com, airtelfun.com, airtelgprs.com, airtel.lk, airtelmms.com, airtelnet.es, airtelwap.es, ais.co.th, akdt.dataonair.net, alaskawifi.com, alegro.net.ec, aliasredirect.net, alltel.com, alltele.tmh-gprs.se, alltele.tmh-mms.se, almadar.mms, almadar.net, altice.com, amazoniacelular.com.br, amt.aland.fi, ancelutil.com.uy, andglobal.softbank.ne.jp, andoworld.softbank.ne.jp, apn01.cwpanama.com.pa, apn02.cwpanama.com.pa, apndnsota.4g.mycricket.com, apn.fastweb.it, apnmms.movistar.com.uy, apnota.4g.mycricket.com, apnumt.movistar.com.uy, app.movilnet.com.ve, aster.internet, aster.mms, aster.pl, att.mvno, au.au-net.ne.jp, avea.com.tr, azercell.com, ba.amx, bahnhofab.tmhgprs, bahnhofab.tmhmms, bahnhoflda.tmhgprs, bahnhoflda.tmhmms, bakcell.com, bam.clarochile.cl, bam.entelpcs.cl, base.be, bbnw.jp, beeline.kz, bell.ca, bew.orange.co.ke, bhmobile.ba, biglobe.jp, biz.immix.com, blueunlimited.com, bmobile.com.bn, bmobile.ne.jp, bob.at, bonbon.com.hr, bornsip.fr, bouyguestelecom.fr, bplmobile.com, brasiltelecom.com.br, brt.br, brtspt.mmsmvno.com, bsnlmmsc.in, bt.com, btmobile.bt.com, bulsat.com, c10.fi, c1neaz.csky.us, c1nepa.csky.us, captive.apple.com, captive.gogoinflight.com, captive.g.aaplimg.com, captive-cdn.origin-apple.com.akadns.net, captive-cidr.origin-apple.com.akadns.net, carrefourdata.be, carrefourmms.be, cat3g.com, catch.net.tw, cccomm.csky.us, celcom.net.my, cellcom.co.il, cellcom.com, celloneet.com, cellonenation.net, cellular1.net, chatmobility.com, chatrisp.apn, chatrweb.apn, chatrwireless.com, cinet.spcs, cingular.com, clarochile.cl, claro.com.ar, claro.com.br, claro.com.pa, claro.pe, claro.sv, cleartalk.csky.us, client-abc.adamuser.app, cmobile.co.za, comcast.rslr.vzwentp, conference.ims.mnc004.mcc204.3gppnetwork.org, conference.ims.mnc220.mcc302.3gppnetwork.org, conference.ims.singtel.com, conf-factory.1und1-mobilfunk.de, conf-factory.ims.cspire.com, conf-factory.ims.mnc001.mcc228.3gppnetwork.org, conf-factory.ims.mnc024.mcc530.3gppnetwork.org, conf-factory.ims.mnc027.mcc208.3gppnetwork.org, conf-factory.ims.mnc720.mcc302.3gppnetwork.org, config.rcs.mnc001.mcc655.pub.3gppnetwork.org, config.rcs.mnc610.mcc302.pub.3gppnetwork.org, conf.mnc004.mcc420.3gppnetwork.org, connect.mobilinkworld.com, connect.vivacell.am, coop.it, coriolis.fr, cosmote.gr, cosmote.ro, cox.net, crl.t-mobile.com, ctbc.br, ctbccelular.com.br, ctc.csky.us, ctimovil.com.ar, ctimovil.com.py, ctimovil.com.uy, ct.tmh-gprs.se, ct.tmh-mms.se, cubacel.cu, cvalley.net, cvwmms.com, cyfrowypolsat.pl, cyta.com.cy, data1.eronet.ba, data2.eronet.ba, datawikim, digicelpng.com, digicelsamoa.net, digicelsr.com, digicelsv.com, digiceltt.com, digi.com.my, djezzy.internet, djezzy.mms, dm.jplat.net, dmm.com, dna.fi, dnafinland.fi, dnapro.fi, dream.jp, drei.at, dst.com, dst.com.bn, dst.internet, dst.mms, dtac.co.th, du.ae, e.vvm.mstore.msg.t-mobile.com, e1.vvm.mstore.msg.t-mobile.com, e2.vvm.mstore.msg.t-mobile.com, e3.vvm.mstore.msg.t-mobile.com, e4.ue.mstore.msg.t-mobile.com, e4.vvm.mstore.msg.t-mobile.com, e5.vvm.mstore.msg.t-mobile.com, e6.vvm.mstore.msg.t-mobile.com, e7.vvm.mstore.msg.t-mobile.com, e911.mobilefrdm.ca, ebouygtel.com, econet.net, edgemobile.net, edge.viva.net.do, ekn.com, elementmobile.net, elisa.ee, elisa.fi, emome.net, em.std, emt.ee, eng-asw.com, eng.t-mobile.com, entelpcs.cl, entel.pe, epc.tmobile.com, epdg.epc.att.net, epdg.epc.firstnet.com, epdg.epc.mnc000.mcc000.pub.3gppnetwork.org, epdg.epc.mnc001.mcc222.pub.3gppnetwork.org, epdg.epc.mnc001.mcc228.pub.3gppnetwork.org, epdg.epc.mnc001.mcc238.pub.3gppnetwork.org, epdg.epc.mnc001.mcc262.pub.3gppnetwork.org, epdg.epc.mnc001.mcc286.pub.3gppnetwork.org, epdg.epc.mnc001.mcc466.pub.3gppnetwork.org, epdg.epc.mnc001.mcc505.pub.3gppnetwork.org, epdg.epc.mnc001.mcc525.pub.3gppnetwork.org, epdg.epc.mnc001.mcc620.pub.3gppnetwork.org, epdg.epc.mnc001.mcc655.pub.3gppnetwork.org, epdg.epc.mnc001.mcc740.pub.3gppnetwork.org, epdg.epc.mnc002.mcc228.pub.3gppnetwork.org, epdg.epc.mnc002.mcc238.pub.3gppnetwork.org, epdg.epc.mnc002.mcc286.pub.3gppnetwork.org, epdg.epc.mnc002.mcc404.pub.3gppnetwork.org, epdg.epc.mnc002.mcc424.etisalat.ae, epdg.epc.mnc002.mcc655.pub.3gppnetwork.org, epdg.epc.mnc003.mcc214.pub.3gppnetwork.org, epdg.epc.mnc003.mcc232.pub.3gppnetwork.org, epdg.epc.mnc003.mcc268.pub.3gppnetwork.org, epdg.epc.mnc003.mcc272.pub.3gppnetwork.org, epdg.epc.mnc003.mcc286.pub.3gppnetwork.org, epdg.epc.mnc003.mcc515.pub.3gppnetwork.org, epdg.epc.mnc004.mcc214.pub.3gppnetwork.org, epdg.ims.mnc005.mcc724.pub.3gppnetwork.org, epdg.epc.mnc006.mcc268.pub.3gppnetwork.org, epdg.epc.mnc006.mcc454.pub.3gppnetwork.org, epdg.epc.mnc007.mcc214.pub.3gppnetwork.org, epdg.epc.mnc007.mcc655.pub.3gppnetwork.org, epdg.epc.mnc008.mcc204.pub.3gppnetwork.org, epdg.epc.mnc008.mcc240.pub.3gppnetwork.org, epdg.epc.mnc010.mcc234.pub.3gppnetwork.org, epdg.epc.mnc010.mcc655.pub.3gppnetwork.org, epdg.epc.mnc010.mcc724.pub.3gppnetwork.org, epdg.epc.mnc014.mcc242.pub.3gppnetwork.org, epdg.epc.mnc015.mcc208.pub.3gppnetwork.org, epdg.epc.mnc015.mcc234.pub.3gppnetwork.org, epdg.epc.mnc016.mcc204.pub.3gppnetwork.org, epdg.epc.mnc020.mcc334.pub.3gppnetwork.org, epdg.epc.mnc023.mcc262.pub.3gppnetwork.org, epdg.epc.mnc023.mcc724.pub.3gppnetwork.org, epdg.epc.mnc027.mcc208.pub.3gppnetwork.org, epdg.epc.mnc030.mcc234.pub.3gppnetwork.org, epdg.epc.mnc030.mcc334.pub.3gppnetwork.org, epdg.epc.mnc038.mcc234.pub.3gppnetwork.org, epdg.epc.mnc040.mcc404.pub.3gppnetwork.org, epdg.epc.mnc045.mcc404.pub.3gppnetwork.org, epdg.epc.mnc076.mcc404.pub.3gppnetwork.org, epdg.epc.mnc084.mcc404.pub.3gppnetwork.org, epdg.epc.mnc086.mcc404.pub.3gppnetwork.org, epdg.epc.mnc092.mcc466.pub.3gppnetwork.org, epdg.epc.mnc097.mcc466.pub.3gppnetwork.org, epdg.ims.mnc101.mcc732.pub.3gppnetwork.org, epdg.epc.mnc110.mcc330.pub.3gppnetwork.org, epdg.epc.mnc220.mcc302.pub.3gppnetwork.org, epdg.epc.mnc230.mcc311.pub.3gppnetwork.org, epdg.epc.mnc240.mcc310.pub.3gppnetwork.org, epdg.epc.mnc260.mcc310.pub.3gppnetwork.org, epdg.epc.mnc370.mcc302.pub.3gppnetwork.org, epdg.epc.mnc390.mcc313.pub.3gppnetwork.org, epdg.epc.mnc490.mcc302.pub.3gppnetwork.org, epdg.epc.mnc580.mcc311.pub.3gppnetwork.org, epdg.epc.mnc610.mcc302.pub.3gppnetwork.org, epdg.epc.mnc720.mcc302.pub.3gppnetwork.org, epdg.epc.mnc780.mcc302.pub.3gppnetwork.org, epdg.epc.mnc790.mcc313.pub.3gppnetwork.org, epdg.epc.mnc840.mcc311.pub.3gppnetwork.org, epdg.epc.mnc861.mcc405.pub.3gppnetwork.org, epdg.epc.mnc874.mcc405.pub.3gppnetwork.org, epdg.epc.mnc880.mcc302.pub.3gppnetwork.org, epdg.ims.2degrees.net.nz, epdg.mobileone.net.sg, epdg.mobily.com.sa, epdg.telco.telenet-ops.be, epdg.three.ie, epicpcs.com, era.pl, eroskimovil.es, etc.com, etisalat.ae, etisalat.af.mms, etisalat.af.wap, etisalat.af.web, etisalt.lk, euskaltelmms.euskaltel.mobi, euskaltel.mobi, event.proximus.be, event.swisscom.ch, event.vodafone.de, expresate.digitel.ve, ezweb.ne.jp, factory.ims.mnc500.mcc302.3gppnetwork.org, factory.ims.movistar.mx, fast.metropcs.com, fast.t-mobile.com, fastweb.it, fido.ca, fi.omv.es, firstcellular.net, fmc.stc.com.sa, fmgmobie.pl, fmgmobile.pl, foma01.wi-gate.net, fp.com.attz, freedommobile.ca, free.a1.net, free.fr, free.re, freetel.link, fr.lebara.mobi, gadu-gadu.pl, gci.csky.us, gci.net, geocell.com.ge, geo.t-mobile.com, getconnected.southwestwifi.com, giffgaff.com, gint.b-online.gr, globe.com.ph, gloworld.com, gocbw.com, gogoinflight.com, golantelecom.co.il, gomobile.fi, good.call, goto.virginmobile.uk, gprs0.vipnet.hr, gprs.amazoniacelular.com.br, gprs.ancel, gprs.base.be, gprs.beeline.com.kh, gprs.claro.com.uy, gprsconnect.com, gprs.cw.com, gprs.eronet.ba, gprs.eroskimovil.es, gprs.is, gprs.mms.lt, gprsmov.lebaramobile.es, gprsmov.pepephone.com, gprs.mtctouch.com.lb, gprs.oi.com.br, gprs.pepephone.com, gprs.personal.com, gprs.promonte.com, gprs.qtel, gprs.rogers.com, gprs.safaricom.com, gprs-service.com, gprs-service-fr.net, gprs.startas.lt, gprs.swisscom.ch, gprs.telemigcelular.com.br, gprs.tn, gprsweb.digitel.ve, gpsurf.net, gscdata.com, gsm-suomi.fi, gsmt.mmsmvno.com, guamcell.csky.us, halebop.telia.se, hawkeyeswitch.net, heyah.pl, hitsmobile.es, hk.chinamobile.com, hkcsl.com, home.beeline.ru, host-abc.3gppnetwork.org, hotmobile.co.il, h-slp.mnc001.mcc655.pub.3gppnetwork.org, htgprs.hr, http.globe.com.ph, hu.upcmobile.com, i2.iwireless.com, iamgprs1.ma, ibc.sasktel.com, ibox.tim.it, ideasclaro.com, ideasclaro.com.do, ideasclaro.com.jm, iesmms.porta.com.ec, iesporta.com.ec, i.euskaltel.mobi, igprs.claro.com.ar, igprs.claro.com.py, igprs.claro.com.uy, iliad.it, iijmio.jp, iliad-italia.it, immix.csky.us, imms.orange.sk, imovil.entelpcs.cl, imovil.virginmobile.cl, ims.attmex.mx, ims.bell.ca, ims.cellcom.com, ims.cs4glte.com, ims.metropcs, ims.mnc001.mcc232.3gppnetwork.org, ims.mnc002.mcc238.3gppnetwork.org, ims.mnc002.mcc424.3gppnetwork.org, ims.mnc005.mcc244.3gppnetwork.org, ims.mnc005.mcc525.3gppnetwork.org, ims.mnc006.mcc454.3gppnetwork.org, ims.taiwanmobile.com, ims.vodafone.ie, ims.wind.gr, inap2.telia.se, inapmms.telia.se, indosat.com, indosat-m3.net, inet.bwc.ru, inet.es, inet-gprs.mtel.bg, inet.tdc.fi, inet.vivacell.am, inflightinternet.com, inland3g.com, internet1.btcbahamas.com, internet1.meditel.ma, internet3g.unite.md, internet.aina.fi, internet.air.net, internet.amc, internet.at.upcmobile.com, internet.batelco.com, internet.beeline.am, internet.beeline.kz, internet.beeline.ru, internet.beeline.uz, internet.ben, internet.bibob.dk, internet.bmbpartner.be, internet.br, internet.btcbahamas.com, internet.c10.fi, internet.cellinkgy.com, internet.claropr.com, internet.claro.sv, internet.comcel.com.co, internet.coopvoce.it, internet.cp, internet.cs4glte.com, internet.ctimovil.com.ar, internet.dicame.fi, internet.digicelpng.com, internet.digimobil.es, internet.digitel.ve, internet.emt.ee, internet.epictouch, internet.eplus.de, internet.etk.ru, internet.euskaltel.mobi, internet.farmerswireless.com, internet.freedommobile.ca, internet.gadu-gadu.pl, internet.globe.com.ph, internet.glocalnet.se, internet.golantelecom.net.il, internet.gomobile.fi, internet.gsm-suomi.fi, internet.ho-mobile.it, internet.ht.hr, internet.ideasalo.ni, internet.ideasclaro, internet.ideasclaro.com.do, internet.ideasclaro.com.jm, internet.indigoip, internet.inland.com, internet.invianet.com, internet.itelcel.com, internet.korek.com, internet.kymp.net, internet.lebara.dk, internet.lguplus.co.kr, internet.life.com.by, internet.lmt.lv, internet.mascom, internet.metropcs, internet.mg.airtel.com, internet.mic1.com.lb, internet.movicel.co.ao, internet.movil, internetmovil.etb.net.co, internet.movistar.com.co, internet.movistar.com.ec, internet.movistar.cr, internet.movistar.gt, internet.movistar.mx, internet.movistar.ni, internet.movistar.pa, internet.movistar.sv, internet.movistar.ve, internet.mtelia.dk, internet.mtn.com.af, internet.mts, internet.mts.ru, internet.mvno.mobi, internet.ng.zain.com, internet.no, internet.nova.gr, internet.nuevatel.com, internet.ono.com, internet.ooredoo.tn, internet.orange.co.bw, internet.partner1, internet.pelephone.net.il, internet.phonero.no, internet.porta.com.ec, internet.postemobile.it, internet.proximus.be, internet.rl, internet.saunalahti, internet.se, internet.setera.fi, internet.simobil.si, internet.smarts.ru, internet.song.fi, internet.t-2.net, internet.tal.is, internet.t-d1.de, internet.tele2.dk, internet.tele2.ee, internet.tele2.lt, internet.tele2.lv, internet.tele2.nl, internet.tele2.no, internet.tele2.ru, internet.telecable.es, internet.telecom.co.nz, internet.telekom, internet.telenor.se, internet.tigo.bo, internet.tigo.gt, internet.tigo.hn, internet.tigo.py, internet.tigo.sv, internet.t-mobile, internet.t-mobile.cz, internet.tn, internet.tunisiana.com, internet.tusmobil.si, internet.unifon, internet.unitel.co.ao, internet.unite.md, internet.usi.ru, internet.vedge.com, internet.vivacom.bg, internet.vodafone.gr, internet.vodafone.net, internet.vodafone.ro, internet.wcc.net, internet.westlink, internet.wind, internet.yota, int.movilnet.com.ve, int.socialmas, invianet.com, iorange.sk, iot1.com, ip.primetel, ip.videotron.ca, isp.cellularoneaz.net, isp.cingular, isp.mb.com, isp.nawras.com.om, isp.telus.com, isp.vodafone.ie, itelcel.com, iusacell3g.com, iwireless.dataonair.net, iwireless.datonair.net, jawalnet.com.sa, jawwal.ps, jazztelmms.com, jo.zain.com, kcell.kz, ke.airtel.com, ke.celtel.com, kenamobile.it, kgtmms.net.tw, kgtnet.tw, korektel.com, kpn4g.nl, ktfwing.com, kyivstar.net, kymp.net, lbs.geo.t-mobile.com, lebara.co.uk, lebaramobile.es, life.com.by, live.pre.vodafone.com, live.vodafone.com, live.vodafone.com.fj, lmt.lv, location.nexteldata.com.mx, login.wifigem.com, loopmobile.in, lowi.omv.es, lowi.private.omv.es, lsmmsc.xtra.co.nz, lsxtra.co.nz, lte.claropr.com, ltedata.apn, lte-d.ocn.ne.jp, lte.fenics.jp, lte.internet, lte.ktfwing.com, lte.mobac.net, ltemobile.apn, lte-roaming.lguplus.co.kr, lte-roaming.sktelecom.com, lte.sktelecom.com, lte.vodacom.za, luckymobile.ca, lyca.mmsmvno.com, maingate.telia.se, manxpronto.net, mass.at, mclaropr.com, mda.nifty.com, mdata.net.au, mdb.nifty.com, mediamessaging.co.uk, media.ng, media.videotron.com, meditel.ma, message.coopvoce.it, metropcs.mmsmvno.com, metropcs.net, mic1.com.lb, midrivers.csky.us, mimundokolbi.ice.cr, mineo-d.jp, mineo.jp, m.iot1.com, mmc.digicelfr.com, mmc.digicelgy.com, mmc.digicelhaiti.com, mmc.digiceljamaica.com, mmc.digicelpanama.com, mmc.digicelsr.com, mmc.digiceltt.com, mmc.xl.net.id, mme.digiceljamaica.com, mm.movilnet.com.ve, mm.myboostmobile.com, mmr.orangewi.com, mms01.evolvecellular.com, mms.02.co.uk, mms.1und1-mobilfunk.de, mms1.live.vodafone.in, mms1.zsend.com, mms.2degreesmobile.net.nz, mms2.dtac.co.th, mms2.movilnet.com.ve, mms2.mymobiletxt.net, mms2.westlinkcom.com, mms.3.dk, mms.412.com.ve, mms.8ta.com, mms.ad.vodafone.co.uk, mms.adv.com, mms.aina.fi, mms.airfiremobile.com, mms.airtel.lk, mms.ais.co.th, mms.alegro.net.ec, mms.alltel.com, mms.altice.com, mms.amazoniacelular.com.br, mms.amt.aland.fi, mms.ancelutil.com.uy, mms.aster.pl, mmsaut.at, mms.avea.com.tr, mms.azercell.com, mms.bakcell.com, mms.base.be, mms.batelco.com, mms.be, mms.beeline.am, mms.beeline.com.kh, mms.beeline.kz, mms.beeline.ru, mms.beeline.uz, mms.bell.ca, mms.ben, mms.bhmobile.ba, mms.bibob.dk, mms.blueunlimited.com, mms.bmobile.com.bn, mms.bob.at, mms.bonbon.com.hr, mms.bornsip.fr, mmsbouygtel.com, mms.bouyguestelecom.fr, mms.bplmobile.com, mms.brasiltelecom.com.br, mms.brt.br, mms.bt.com, mms.btonephone.com, mms.bwc.ru, mms.c10.fi, mms.c1.ama, mmsc1.g-mms.com, mmsc1.acsalaska.net, mmsc1.gscdata.com, mmsc1.mms.cosmote.ro, mmsc1.mms.globul.bg, mmsc1.mms.telekom.ro, mmsc1.mms.telenor.bg, mmsc1.uscc.net, mmsc2.mts.net, mmsc.a1.net, mmsc.aina.fi, mmsc.aiowireless.net, mmsc.akdt.dataonair.net, mms.cat3g.com, mms.catch.net.tw, mmsc.axis, mmsc.base.be, mmsc.be, mmsc.bob.at, mmsc.c10.fi, mmsc.c1neaz.csky.us, mmsc.c1nepa.csky.us, mmsc.cccomm.csky.us, mmsc.cingular.com, mmsc.cleartalk.csky.us, mmsc.cosmote.gr, mmsc.ctc.csky.us, mmsc.cyta.com.cy, mmsc.dicame.fi, mmsc.dna.fi, mmsc.dnafinland.fi, mmsc.dnapro.fi, mms.celcom.net.my, mms.cellcom.co.il, mms.cellcom.com, mms.cellinkgy.com, mms.celloneet.com, mms.cellonenation.net, mms.cellular1.net, mmsc.entelpcs.cl, mmscenter.suncellular.com.ph, mmsc.gci.csky.us, mmsc.gci.net, mmsc.golantelecom.co.il, mmsc.gomobile.fi, mmsc.gprs.cw.com, mmsc.gsm-suomi.fi, mmsc.guamcell.csky.us, mms.chatmobility.com, mms.chatrwireless.com, mmsc.hawkeyeswitch.net, mmsc.indosat.com, mmsc.invianet.com, mmsc.iwireless.dataonair.net, mmsc.iwireless.datonair.net, mmsc.ktfwing.com, mmsc.kymp.net, mms.clarochile.cl, mms.claro.com.ar, mms.claro.com.br, mms.claro.com.ec, mms.claro.com.pa, mms.claro.pe, mms.claropr.com, mms.claro.sv, mmsc.lmt.lv, mmsc.mdata.net.au, mmsc.mediamessaging.co.uk, mmsc.midrivers.csky.us, mmsc.mms.02.co.uk, mmsc.mms.ancelutil.com.uy, mmsc.mms.o2.co.uk, mmsc.mms.o2.ie, mmsc.mms.vodafone.nl, mmsc.mobi, mmsc.mobile.att.net, mmsc.mobilecore.lla.com, mms.cmobile.co.za, mmsc.mobistar.be, mmsc.monternet.com, mmsc.movilfalabella.com, mmsc.movistar.com.uy, mmsc.mta.dataonair.net, mmsc.mtel.ba, mmsc.mtpcs.csky.us, mmsc.mymmode.com, mmsc.myuni.com.cn, mmsc.nova.is, mmsc.nwmobility.com, mms.colombiamovil.com.co, mmsc.omanmobile.com, mmsc.omanmobile.om, mms.comcel.com.co, mms.comcel.com.co, mms.coop.it, mms.coopvoce.it, mmsc.optus.com.au, mmsc.orange.at, mms.coriolis.fr, mms.cox.net, mmsc.paradisemobile.com, mmsc.pgsm.hu, mmsc.pinebelt.net, mmsc.play.pl, mmsc.proximus.be, mmsc.ptci.net, mmsc.pt.lu, mmsc.rcom.co.in, mmsc.rebtel.com, mmsc.setera.fi, mmsc.sunrise.ch, mms.ctbc.br, mms.ctbccelular.com.br, mmsc.tdc.dk, mmsc.tdc.fi, mmsc.tele2.dk, mmsc.tele2.ee, mmsc.tele2.hr, mmsc.tele2.lt, mmsc.tele2.lv, mmsc.tele2.nl, mmsc.tele2.no, mmsc.tele2.ru, mmsc.tele2.se, mmsc.telefonicamovistar.com.pe, mmsc.telekom.sk, mmsc.telenet.be, mmsc.telenor.hu, mmsc.telstra.com, mmsc.three.net.au, mmsc.tigo.com.gh, mms.ctimovil.com.ar, mms.ctimovil.com.py, mms.ctimovil.com.uy, mmsc.tmn.pt, mmsc.t-mobile.at, mmsc.tracfone.com, mmsc.truphone.com, mmsc.tunisiana.com, mmsc.tuyomovil.com, mms.cubacel.cu, mms.cv, mms.cvalley.net, mmsc.vipmobile.rs, mmsc.vipoperator.com.mk, mmsc.vivacom.bg, mmsc.vmobl.com, mmsc.vnet.mobi, mmsc.vodacom4me.co.ls, mmsc.vodacom4me.co.za, mmsc.vodafone.al, mmsc.vodafone.es, mmsc.vodafone.is, mmsc.westlinkcom.com, mms.cwwmms.com, mms.cyfrowypolsat.pl, mms.davewireless.com, mmsc.yettel.hu, mms.dialog.lk, mms.dicame.fi, mms.digicelgroup.com, mms.digicelpacific.com, mms.digicelpng.com, mms.digicelsamoa.net, mms.digicelsv.com, mms.digi.com.my, mms.dnapro.fi, mms.dst.com, mms.dst.com.bn, mms.dtac.co.th, mms.du.ae, mms.edgemobile.net, mms.ekn.com, mms.elementmobile.net, mms.elisa.ee, mms.elisa.fi, mms.emome.net, mms.emt.ee, mms.entelpcs.cl, mms.entel.pe, mms.epicpcs.com, mms.epictouch, mms.eplus.de, mms.era.pl, mms.eronet.ba, mms.eroskimovil.es, mms.etisalt.lk, mms.etk.ru, mms.euskaltel.mobi, mms.ezweb.ne.jp, mms.farmers.com, mms.fastweb.it, mms.fido.ca, mms.fi.omv.es, mms.firstcellular.net, mms.fmgmobile.pl, mms.freedommobile.ca, mms.free.fr, mms.free.re, mms.gadu-gadu.pl, mms.gci, mmsg.claropr.com, mms.geocell.com.ge, mms.globe.com.ph, mms.globul.bg, mms.gloworld.com, mms.gocbw.com, mms.golantelecom.net.il, mms.gomobile.fi, mmsgprs.amazoniacelular.com.br, mmsgprs.com, mms.gprsconnect.com, mms.gprs.eronet.ba, mms.gprs.is, mms-gprs.mtel.bg, mmsgprs.oi.com.br, mms.gprs.rogers.com, mms.gprs.safaricom.com, mmsgprs.telemigcelular.com.br, mms.gprs.unifon.com.ar, mms.gpsurf.net, mms.gsm-suomi.fi, mms-g.three.com.hk, mmsgw.nuevatel.com, mms.heyah.pl, mms.hitsmobile.es, mms.hk.chinamobile.com, mms.hkcsl.com, mms.hotm, mms.hotmobile.co.il, mms.htgprs, mms.hu.upcmobile.com, mms.hutchisonmacau.com, mms.ideasalo.ni, mms.ideasclaro, mms.ideasclaro.com, mms.ideasclaro.com.do, mms.ideasclaro.com.jm, mmsi.etex.mobi, mms.iliad.it, mms.iliad-italia.it, mms.immix.csky.us, mms.indigo, mms.inland3g.com, mms.invianet.com, mms.iot1.com, mms.itelcel.com, mms.iusacell3g.com, mms.iusacellgsm.mx, mms.jawwal.ps, mms.jo.zain.com, mms.kaplan, mms.kcell.kz, mms.ke.airtel.com, mms.ke.celtel.com, mms.kenamobile.it, mms.kgtmms.net.tw, mms.korek.com, mms.korektel.com, mms.kyivstar.net, mms.kymp.net, mms.lebara.co.uk, mms.lebara.dk, mms.lebaramobile.es, mms.life, mms.life.com.by, mms.loopmobile.in, mms.lowi.omv.es, mmslte.claropr.com, mms.luckymobile.ca, mms.manxpronto.net, mms.meditel.ma, mms.metropcs.net, mms.mg.airtel.com, mms.mic1.com.lb, mms.mnc340.mcc313.pub.3gppnetwork.org, mms.mni.pl, mms.mobeelife.net, mms.mobi.eastlink.ca, mms.mobile.bm, mms.mobile.pl, mms.mobilebysainsburys.co.uk, mms.mobilelife.co.th, mms.mobileuc.global, mms.mobilicity.net, mms.mobilinkworld.com, mms.mobilking.pl, mms.mobipcs.com, mms.mobitag.nc, mms.mobitel.com.kh, mms.mobitel.si, mms.mohavewireless.com, mms.moldcell.md, mms.monaco-telecom.mc, mms.mova.pl, mms.movicel.co.ao, mms.movil, mms.movil.com.bo, mms.movistar.cl, mms.movistar.com, mms.movistar.com.ar, mms.movistar.com.co, mms.movistar.com.ec, mms.movistar.com.ve, mms.movistar.cr, mms.movistar.gt, mms.movistar.mx, mms.movistar.ni, mms.movistar.pa, mms.movistar.pe, mms.movistar.sv, mms.movistar.ve, mms.msg.eng-asw.com, mms.msg.eng.t-mobile.com, mms.mtctouch.com.lb, mms.mtelia.dk, mms.mtn.ci, mms.mtn.com.af, mms.mtn.com.cy, mms.mtn.sd, mms.mtn.co.za, mms.mts064.telekom.rs, mms.mts.ru, mms.mts.uz, mms.mundo-r.com, mms.myblue.com, mms.mycricket.com, mms.mymeteor.ie, mms.mymn3g.net, mms.mymobiletxt.com, mms.myq.gr, mms.natel.ch, mms.nawras.com.om, mms.nemont.mobi, mms.net.sa, mms.nextel3g.net.br, mms.nexteldata.com.mx, mms.nextel.pe, mms.nova.gr, mms.nova.is, mms.ntc, mms.ntelospcs.net, mms.ntwls.net, mms.nuestro.com.ar, mms.nuevatel.com, mms.nwmcell.com, mms.nwn.no, mms.o2active.cz, mms.o2.co.uk, mms.o2.ie, mms.o2world.sk, mms.oister.dk, mms.ola.com.co, mms.omnitel.net, mms.onetouch.com.gh, mms.ono.com, mms.openmobilepr.com, mms.orangecaraibe.com, mms.orange.cm, mms.orange.co.bw, mms.orange.co.ke, mms.orange.com.do, mms.orange.co.uk, mms.orange.es, mms.orange.fr, mms.orange.jo, mms.orange.lu, mms.orange.pl, mms.orange.re, mms.orange.tn, mms.otun, mms.pelephone.net.il, mms.pepephone.com, mms.personal.com, mms.phonero.no, mms.plspictures.com, mms.plusgsm.pl, mms.postemobile.it, mms.pre.vodafone.ro, mms.primetel, mms.promonte.com, mms.prontogo.net, mms.pt.lu, mms.qbmore.mobi, mms.qtel, mms.quam.com.ar, mms.rcom.co.in, mms.revol.us, mms.rinawireless.com, mms.roshan.af, mmsr.ooredoomms.qa, mmsr.ooredooqa, mmsr.qtelmma.qa, mmsr.qtelmms.qa, mms.sabafon.com, mms.sasktel.com, mms.saunalahti.fi, mms.sercomtel.com.br, mms-services.eu, mms.setar.aw, mms.setera.fi, mms.shaw.ca, mms.simi.is, mms.simobil.si, mms.singtel.com, mms.smartone.com, mms.smartone.com.mo, mms.smarts.ru, mmss.mobi.eastlink.ca, mms.sonera.fi, mms.song.fi, mms.sonofon.dk, mmssouth.cellone.in, mms.springmobil.se, mms.sprintpcs.com, mms.sprocketwireless.com, mms.starhubgee.com.sg, mms.suncom.net, mms.sunrise.ch, mms.surfmail.com, mms.symamobile.com, mms.syriatel.com, mms.t-2.net, mms.tal.is, mms.talkmobile.co.uk, mms.talktalk.co.uk, mms.tango.lu, mms.tdc.fi, mms.tdc.se, mms.telco.re, mms.tele2.ee, mms.tele2.kz, mms.tele2.lt, mms.tele2.lv, mms.tele2.ru, mms.telecable.es, mms.tele.gl, mms.telekom.si, mms.telemach.hr, mms.telemach.net, mms.telemigcelular.com.br, mms.telenor.bg, mms.telenor.dk, mms.telenor.rs, mms.telia.dk, mms.telia.se, mms.telkomsel.com, mms-tf.net, mms.three.co.id, mmsthree.co.id, mms.three.com.mo, mms.three.ie, mms.thumbcell.com, mms.tigo.bo, mms.tigo.gt, mms.tigo.hn, mms.tigo.py, mms.tigo.sv, mms.tim.br, mms.tim.it, mms.tiscali.mobi, mms.t-mobile.com.mk, mms.t-mobile.cz, mms.t-mobile.de, mms.t-mobile.hr, mms.t-mobile.hu, mms.tmovil.cl, mms.tn, mms.tot3g.net, mms.tracfone.com, mms.tre.se, mms.trueh.com, mms.truelife.com, mms.trueworld.net, mms.tubiedronka.pl, mms.tunisiana.com, mms.turkcell.com.tr, mms.turkcell.com.tr, mms.tusmobil.si, mms.um.3ireland.ie, mms.um.idmobile.co.uk, mms.umniah.com, mms.um.three.com.hk, mms.um.three.co.uk, mms.unionwireless.com, mms.unitedwireless.com, mms.unitel.co.ao, mms.unite.md, mmsu.pelephone.net.il, mms.usi.ru, mms.velcom.by, mms.viaero.com, mms.vibo.net.tw, mms.viero.com, mms.viettelmobile.com.vn, mms.vinaphone.com.vn, mms.vinaphone.vnn.vn, mms.vipmobile.rs, mms.vipnet.hr, mms.virginmobile.cl, mms.virginmobile.co.uk, mms.virginmobile.co.za, mms.virginvibe.com.au, mms.vivacell.am, mms.vivacom.bg, mms.viva.com.bh, mms.viva.net.do, mms.vivo.com.br, mms.vodacom.net, mms.vodafone.com.eg, mms.vodafone.com.mt, mms.vodafone.com.qa, mms.vodafone.co.uk, mms.vodafone.gr, mms.vodafone.hu, mms.vodafone.it, mms.vodafone.net, mms.vodafone.nl, mms.vodafone.pt, mms.vodafone.ro, mms.vodaphone.com.gh, mms.vox.com.py, mms.vtext.com, mms.vzwreseller.com, mms.wana.ma, mmswap.centennialwireless.com, mms.wap.ctm.net, mms.warid, mms.waridtel.com.bd, mms.wataniya.com, mms.wataniya.ps, mms.wcc.net, mms.westlink, mms.wholesale.mmsmvno.com, mms.wind, mms.wind.it, mms.windmobile.ca, mms.windtre.it, mms.yota, mms.zain, mms.zain.sd, mms.zonamovil.com.pa, mmtmobile.jp, mm.vor.promonte.com, mm.vor.telenor.me, mnc340.mcc313.pub.3gppnetwork.org, mnet.b-online.gr, mni.internet, mni.mms, mni.pl, m.numericable.fr, mobeelife.net, mobil2.tmhgprs, mobil2.tmhmms, mobile.att.net, mobile.bm, mobilebysainsburys.co.uk, mobilecore.lla.com, mobilefrdm.ca, mobilelife.co.th, mobile.lte.three.com.hk, mobile.o2.co.uk, mobile.pl, mobile.talktalk.co.uk, mobile.three.com.hk, mobile.three.com.mo, mobileuc.global, mobile.vodafone.it, mobilicity.net, mobilking.pl, mobipcs.com, mobistar.be, mobitag.nc, mobitel.com.kh, mobitel.si, modem.inland.com, modem.iusacellgsm.mx, modem.nexteldata.com.mx, modem.orange.net.il, mohavewireless.com, moldcell.md, momms.smartone.com, monaco-telecom.mc, monternet.com, mopera.flat.foma.ne.jp, mopera.net, mosmartone.com, mova.pl, movil.com.bo, movilfalabella.com, movilnet.com.ve, movistar.cl, movistar.com, movistar.com.ar, movistar.com.co, movistar.com.ec, movistar.com.uy, movistar.com.ve, movistar.cr, movistar.es, movistar.gt, movistar.mx, movistar.ni, movistar.pa, movistar.pe, movistar.sv, movistar.ve, mp.mobiel.kpn, mpr2.bizho.net, msg.eng.t-mobile.com, msg.pc.t-mobile.com, msg.t-mobile.com, mstore.msg.t-mobile.com, mta.dataonair.net, mtel.ba, mtn.ci, mtn.com.cy, mtn.co.za, mtnl.net, mtn.sd, mtpcs.csky.us, mts064.telekom.rs, mts.net, multimedia.ah.nl, multimedia.lebara.nl, mundo-r.com, mworld.be, myblue.com, mycricket.com, mymeteor.ie, mymmode.com, mymms.syriatel.com, mymn3g.net, mymobiletxt.net, mymtn.co.sz, myq.gr, mysyriatel.com, myuni.com.cn, natel.ch, nemont.mobi, nep.data, nep.mms, net2.vodafone.pt, net.apuapcs.ag, net.asiacell.com, net.hotm, net.korek.com, net.mts.uz, net.nova.is, net.orange.jo, net.sa, net.syriatel.com, netcts.cdn-apple.com, netcts.cdn-apple.com.edgesuite.net, nextel.pe, neverssl.com, nextel3g.net.br, nexteldata.com.mx, nextelmovil.cl, n.f6.ispsn, n.ispsn, nova.gr, nova.is, n.r5.ispsn, n.t8.ispsn, ntelospcs.net, ntwls.net, nuestro.com.ar, numericable.fr, n.vmu.ispsn, n.w1.ispsn, nwmcell.com, nwmobility.com, nwn.no, o2active.cz, o2.co.uk, o2world.sk, oap7.sprintpcs.com, office.vodafone.nl, ofnew.fr, oister.dk, ola.com.co, omammsc.uplus.co.kr, omanmobile.com, omanmobile.om, omauplus.co.kr, omms.nate.com, omnitel.net, onate.com, onetouch.com.gh, online.telia.se, ono.com, openmobilepr.com, open.mopera.net, open.softbank.ne.jp, optus.com.au, orangecaraibe.com, orange.acte, orange.at, orange.cm, orange.com.do, orange.co.uk, orange.es, orange.fr, orange.lu, orange.mms, orange.ne, orangenet.com.do, orange.nl, orange.pl, orange.re, orangerun.acte, orange.smartphone, orange.tn, orange.ug, orange.video, orange.web, orange.world, org.pelephone.net.il, ota.inland.com, ovivomobile.com, ovivomvno.com, paradisemobile.com, payandgo.o2.co.uk, payg.mobilebysainsburys.co.uk, payg.talkmobile.co.uk, pc.t-mobile.com, pda.bell.ca, pda.stm.sk.ca, pepephone.com, personal.com, pgsm.hu, phoneweb.tmh-gprs.se, phoneweb.tmh-mms.se, pinebelt.net, pinternet.interkom.de, pix.cellularsouth.com, pix.cspire.com, play.pl, plspictures.com, plus.4g, plus.acs.jp, plusgsm.pl, plus.softbank, plus.velcom.by, portalmmm.nl, postemobile.it, ppmms1.btcbahamas.com, ppnet.apuapcs.ag, pp.vodafone.co.uk, prepago.ancel, prepay.tesco-mobile.com, primgw.vowifi2.spcsdns.net, private.centennialwireless.com, proximus.be, proxy.aiowireless.net, ptci.net, pt.lu, pub.3gppnetwork.org, pwg.mmsmvno.com, pxt.vodafone.net.au, pxt.vodafone.net.fj, pxt.vodafone.net.nz, qbmore.mobi, q-mms.myq.gr, quam.com.ar, qxwz.com, rcom.co.in, real.globe.com.ph, rebtel.com, relay.mms.telering.at, revol.us, rinawireless.com, rmobile.jp, roaming.sktelecom.com, rogers-core-appl1.apn, roshan.af, sabafon.com, sasktel.com, saunalahti.fi, sbux.co, scomo.tmh-gprs.se, scomo.tmh-mms.se, sercomtel.com.br, services.glocalnet.se, services.telenor.se, setar.aw, setera.fi, share.lte.three.com.hk, shaw.ca, simi.is, singtel.com, sktims.net, smart.com, smartone.com, smartone.com.mo, smartsites.t-mobile, smile.world, smpl.eng.t-mobile.com, smpl.mms.msg.eng.t-mobile.com, solavei.mmsmvno.com, sonera.fi, song.fi, sonofon.dk, southwestwifi.com, sphone.pelephone.net.il, spinboxmms.telia.se, spinbox.telia.se, sp.koodo.com, sp.mb.com, spmode.ne.jp, sp.mts, sprboost.mmsmvno.com, springmobil.se, sprintpcs.com, sprocketwireless.com, sp.telus.com, ss.epdg.epc.mnc260.mcc310.pub.3gppnetwork.org, starhubgee.com.sg, suncom.net, sunrise.ch, surfmail.com, symacom.fr, symamobile.com, tal.is, talkmobile.co.uk, talktalk.co.uk, tango.lu, tata.docomo.dive.in, tata.docomo.internet, tata.docomo.mms, tdc.dk, tdc.fi, tdc.se, telavox.tmhgprs.se, telco.re, tele2.dk, tele2.ee, tele2.hr, tele2.kz, tele2.lt, tele2.lv, tele2.nl, tele2.no, tele2.ru, tele2.se, telecable.es, telefonica.de, telefonica.es, telefonicamovistar.com.pe, tele.gl, telekom.ro, telekom.si, telekom.sk, telemach.hr, telemach.net, telemigcelular.com.br, telenet.be, telenetwap.be, telenor.dk, telenor.hu, telenor.rs, telenor.smart, tel.hitsmobile.es, telia.dk, telkomsel.com, telogicmms.telia.se, telogic.telia.se, telstra.com, telstra.internet, telstra.mms, telstra.pcpack, telstra.wap, tel.tmhmms, termnat.vivocom.br, termnat.vivomms.com.br, termwapgsm2.vivo.com.br, tescomobile.liffeytelecom.com, tethering.cs4glte.com, tethering.dish.com, tf.mmsmvno.com, three.co.id, three.com.mo, three.co.uk, three.ie, three.net.au, thumbcell.com, tigo.3g, tigo.com.gh, tim.br, timbrasil.br, tim.it, tiscali.mobi, t-mobile.at, t-mobile.com, t-mobile.com.mk, t-mobile.de, t-mobile.hr, t-mobile.hu, tmovil.cl, tma.vvm.mone.pan-net.eu, tot3g.net, tracfone.com, tracfone.vzwentp, tre.it, tre.se, trueh.com, truelife.com, trueworld.net, truphone.com, tubiedronka.pl, tuenti.com, tunisiana.com, turkcell.com.tr, tusmobil.si, tuyomovil.com, ue.mstore.msg.t-mobile.com, ufone.com, ufone.mms, ufone.pinternet, uk.lebara.mobi, um.3ireland.ie, um.idmobile.co.uk, umniah.com, umobile.jp, umob.jp, um.three.com.hk, um.three.co.uk, unico.tim.it, union.mms.com, unionwireless.com, unitedwifi.com, unitedwireless.com, uno.au-net.ne.jp, uqmobile.jp, usccims.com, uscc.net, uvm.mmsmvno.com, uwap.orange.co.il, vas.vodafone.pt, vdm.jp, velcom.by, ventelomms.telia.se, ventelo.telia.se, vfinternet.au, vfinternet.fj, viaero.com, viasat.com, vibo.net.tw, viero.com, viettelmobile.com.vn, vinaphone.com.vn, vinaphone.vnn.vn, vipmobile.mms, vipmobile.rs, vipnet.hr, vipoperator.com.mk, vipoperator.mms, virginmms.fr, virginmobile.cl, virginmobile.co.uk, virginmobile.co.za, virgin-mobile.fr, virginvibe.com.au, vitamax.internet.vodafone.net, viva.bh, vivacell.am, vivacom.bg, viva.com.bh, vl-vi-vvg001.ip.videotron.ca, vmi.velcom.by, vmobile.jp, vmobl.com, vnet.mobi, vntc.ru, vodacom4me.co.ls, vodacom4me.co.za, vodafone.al, vodafone.com.eg, vodafone.com.mt, vodafone.com.qa, vodafone.co.uk, vodafone.es, vodafone.gr, vodafone.hu, vodafone.ie, vodafone.is, vodafone.it, vodafone.net.nz, vodafone.pt, vodaphone.com.gh, volte.aptg.com.tw, volte.mobilefrdm.ca, vowifi.jio.com, vox.com.py, vox.internet, vox.mms, vsblims.com, vtext.com, vvm.ee.co.uk, vvm.mobistar.be, vvm.mstore.msg.t-mobile.com, vzims.com, vzwreseller.com, wana.ma, wap1.iwireless.com, wap9.iwireless.com, wap.asiacell.com, wap.auchantelecom.fr, wap.batelco.com, wap.beeline.com.kh, wap.bouygtel.fr, wap.c1csky.net, wap.cellular1.net, wap.cingular, wap.claro.com.br, wap.claro.com.pa, wap.ctbc.br, wap.ctbccelular.com.br, wap.ctm.net, wap.cv, wap.davewireless.com, wap.digicelbarbados.com, wapdigicel.com, wap.digiceljamaica.com, wap.digiceloecs.com, wap.digicelpacific.com, wap.digicelpacific.ws, wap.digicelpng.com, wap.digicelsv.com, wap.dol.ie, wapdtcw.com, wap.firstcellular.com, wap.gocbw.com, wap.gomobile.fi, wapgprs.oi.com.br, wap.gprs.unifon.com.ar, wapgw.chinookwireless.net, wap.iamgprs.ma, wap.mascom, wap.meditel.ma, wap.metropcs.net, wap.mg.airtel.com, wap.mic1.com.lb, wap.mms.orange.ro, wap.movistar.ve, wap.mycricket.com, wap.mymeteor.ie, wap.mymobiletxt.com, wap.nawras.com.om, wap.nextel3g.net.br, wap.nexteldata.com.mx, wap.o2.co.uk, wap.oi.com.br, wap.omnitel.it, wap.orange.co.il, wap.orange.co.ke, wap.orange.jo, wap.orange.md, wap.orange.ro, wap.postemobile.it, wap.prontogo.net, wap.safaricom.com, wap.saunalahti.fi, wap.setar.aw, wap.sonera.net, wapsouth.cellone.in, wap.tele2.hr, wap.tele2.lt, wap.telecom.co.nz, wap.tigo.com.gh, wap.tim.br, wap.tim.com.br, wap.tim.it, wap.tmovil.cl, wap.tn, wap.tracfone, wap.viva.net.do, wap.vivo.com.br, wap.vodafone.com.eg, wap.vodafone.co.uk, wap.vodafone.pt, waridtel.com.bd, wataniya.ps, wcc.net, web1.velcom.by, web2.velcom.by, web3.velcom.by, webapn.at, webapn.movistar.com.uy, web.be, web.celloneet.com, web.claro.com.pa, web.colombiamovil.com.co, web.coopvoce.it, web.digicelbarbados.com, web.digicelbermuda.com, web.digicelfr.com, web.digicelpacific.com, web.digicelpanama.com, web.digicelsamoa.ws, web.digiceltt.com, web.eronet.ba, web.gci, web.gprs.mtnnigeria.net, web-g.three.com.hk, web.ho-mobile.it, web.htgprs, web.iusacellgsm.mx, web.kenamobile.it, web.manxpronto.net, web.mtn.ci, web.omnitel.it, web.omwtoday.com, web.prontogo.net, web.pt.lu, webpt.mundio.com, web.qtel, web.sktelecom.com, web.tigo.com.gh, web.tigo.rw, web.tmovil.cl, web.ug.zain.com, webuk.mundio.com, web.velcom.by, web.vodafone.com.qa, web.vodafone.de, web.waridtel.co.ug, westlinkcom.com, wholesale.mmsmvno.com, wifigem.com, wifi.starbucks.com, wind.it, windmobile.ca, windtre.it, wireless.dish.com, wirelessfour.mmsmvno.com, wisp.mobi.eastlink.ca, wlan.three.com.hk, wmgmms.telia.se, wo.vzwwo.com, wroaming.lguplus.co.kr, www.ab.kyivstar.net, www.claro.com.pa, www.comcel.com.co, www.dialogsl.com, www.digicelive.com, www.dtac.co.th, www.fmgmobie.pl, www.globe.com.ph, www.htgprs.hr, www.iamgprs1.ma, www.indosat-m3.net, www.internet.mtelia.dk, www.kyivstar.net, www.mms.mtelia.dk, www.mms.t-2.net, www.mms.t-2.net, www.mobile.pl, www.mova.pl, www.neverssl.com, www.pepephone.com, www.t-2.net, www.time4lime.com, www.ufone.com, www.ufonecom, www.ufonemms.com, www.viasat.com, www.vodafone.ie, www.vodafone.net.nz, www.xlgprs.net, www.xlmms.net, xi01.wi-gate.net, xlgprs.net, xlmms.net, xl.net.id, yellopix.men.co.ug, yellopix.mtn.co.ug, yettel.hu, zain.sd, zap.vivo.com.br, ziggo.dataxs.mobi, zonamovil.com.pa, rsp.truphone.com, truphone.com, smdp.io, smdpp.test.rsp.sysmocom.de, test.rsp.sysmocom.de, rsp.sysmocom.de, sysmocom.de, oasis-smartsim.com, vsb.vzw.otgeuicc.com, vzw.otgeuicc.com, otgeuicc.com
```

This is a comprehensive list of domains compiled from various sources, as well as my own research & analysis:

https://codeberg.org/divested/dnsrm/raw/branch/master/Cellular.txt

https://codeberg.org/divested/dnsrm/raw/branch/master/Infra-Carriers.txt

https://codeberg.org/divested/dnsrm/raw/branch/master/Infra-Carriers2.txt

https://github.com/GrapheneOS/adevtool/tree/14/vendor-skels/google_devices/akita/proprietary/product/etc/CarrierSettings

https://github.com/LineageOS/android_vendor_lineage/blob/lineage-19.1/prebuilt/common/etc/apns-conf.xml

https://www.t-mobile.com/support/coverage/wi-fi-calling-on-a-corporate-network

https://www.reddit.com/r/firewalla/comments/167mhz7/tmobile_wifi_calling_issue/k010v02/

https://www.reddit.com/r/nextdns/comments/yrqdlh/visual_voicemail_ee/

https://www.reddit.com/r/nextdns/comments/jgf48w/ios_visual_voicemail/

https://help.nextdns.io/t/35hf2pl/ios-visual-voicemail-malfunction

https://support.adamnet.works/t/wifi-calling-with-adam-go/697

https://www.arubanetworks.com/techdocs/ArubaOS_87_Web_Help/Content/arubaos-solutions/voice-video/ucc-wifi-call.htm

https://www.reddit.com/r/nextdns/comments/mpe16n/blocked_mms_or_long_texts_on_cricket_att/

https://www.reddit.com/r/nextdns/comments/11oreis/allowing_captive_portals_public_wifi_on_apple/

The following domains **will** bypass your NextDNS config. However, the domains provided are not used for tracking or malicious, so there is little privacy to security downside. **This is the same as how Android handles it.**

# Additional recommendations

* Use a privacy-respecting browser like [Firefox](https://www.mozilla.org/firefox/) with my [Phoenix](https://phoenix.celenity.dev).

* If you're using a Chromium browser, make sure to configure NextDNS on **both** your OS and in your browser. This will allow you to take advantage of [Encrypted Client Hello](https://blog.cloudflare.com/announcing-encrypted-client-hello). This is unnecessary on Firefox-based browsers, however it could still be useful to set in both places if for instance you want to set a separate client name for your browser than the rest of your OS, to better determine what queries are coming from where.

* Use a content blocking extension like [uBlock Origin](https://github.com/gorhill/uBlock). *(See recommended settings [here](https://codeberg.org/celenity/ublock-origin-settings))*

* Enable Safe Browsing in your browser if possible and if it's not done in a privacy-invasive way. (You should use i.e. [Google Safe Browsing on "Standard" Mode](https://safebrowsing.google.com/), [Firefox's Safe Browsing](https://support.mozilla.org/kb/how-does-phishing-and-malware-protection-work), [Brave's Safe Browsing](https://brave.com/privacy/browser/#safe-browsing), & [Safari's Fraudulent Website Warning](https://www.apple.com/legal/privacy/data/en/safari/), you should avoid most other options i.e. [Google Safe Browsing on "Enhanced" Mode](https://safebrowsing.google.com/), [Microsoft SmartScreen](https://learn.microsoft.com/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/), & [Opera Sitecheck](https://blogs.opera.com/security/2021/01/making-browsing-safe-from-phishing/)).

* Use a (reputable) anti-virus if possible. On Windows, you can use the built-in [Microsoft Defender Antivirus](https://wikipedia.org/wiki/Microsoft_Defender_Antivirus), on macOS, you can stick to the built-in [XProtect](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/web), on Android, you can use [Hypatia](https://f-droid.org/packages/us.spotco.malwarescanner/), and on Linux, you can use [ClamAV](https://www.clamav.net/). **NOTE:** You should install Hypatia through the [DivestOS Official Repo](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) instead of F-Droid's main repo, as it will allow you to receive quicker updates directly from the developer. It's also recommended to use [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) as your F-Droid client of choice.