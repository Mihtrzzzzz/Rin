
#!name=𝐎𝐯𝐞𝐫𝐚𝐥𝐥
#!desc=𝐁𝐲: 𝐌𝐢𝐡𝐭𝐫𝐳𝐳

[General]

bypass-system = true
skip-proxy = *.local, *.crashlytics.com
tun-excluded-routes = 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12

[MITM]

hostname = us-central1-alight-creative.cloudfunctions.net, photos.adobe.io, restore-access.indream.app, api.picsart.c*, api.meiease.c*, api-mobile.soundcloud.com, spclient.wg.spotify.com, premium*.truecaller.com, api.revenuecat.com, api-sub.meitu.com

[Script]

# Alight Motion
alight motion = type=http-response,script-path=https://raw.githubusercontent.com/iSteal-it/script/main/alight-motion.json,pattern=^https?:\/\/us-central1-alight-creative\.cloudfunctions\.net\/getAccountStatusAndLicenses,max-size=131072,requires-body=true,timeout=10,enable=true

# Lightroom
LightRoom=type=http-response,pattern=^https:\/\/photos\.adobe\.io\/v2\/accounts*,requires-body=1,script-path=https://raw.githubusercontent.com/litieyin/AD_VIP/main/Script/lightroom.js

# Nicegram
Nicegram会员=type=http-request,pattern=^https?:\/\/restore-access\.indream\.app\/restoreAccess\?id=\w+$,requires-body=0,max-size=0,script-path=https://raw.githubusercontent.com/I-am-R-E/Functional-Store-Hub/Master/Nicegram/Script/Nicegram.js,script-update-interval=0

# Picsart
http-request https://api.picsart.com/gw-v2/shop/subscription/apple/purchases script-path=https://raw.githubusercontent.com/quocchienn/Make/refs/heads/crack/PicsArt.js, requires-body=true, timeout=5, tag=PicsArt

# SoundCloud
SoundCloudGo+=type=http-response,pattern=https://api-mobile.soundcloud.com/configuration/ios,requires-body=1,script-path=https://raw.githubusercontent.com/Marol62926/MarScrpt/main/soundcloud.js

# Spotify
spotify-json = type=http-request,type=http-request,pattern=^https:\/\/spclient\.wg\.spotify\.com\/(artistview\/v1\/artist|album-entity-view\/v2\/album)\/,requires-body=0,script-path=https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-json.js
spotify-proto = type=http-response,pattern=^https:\/\/spclient\.wg\.spotify\.com\/(bootstrap\/v1\/bootstrap|user-customization-service\/v1\/customize)$,requires-body=1,binary-mode=1,max-size=0,script-path=https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-proto.js,script-update-interval=0
spotify歌词翻译 = type=http-response,pattern=^https:\/\/spclient\.wg\.spotify\.com\/color-lyrics\/v2\/track\/,requires-body=1,binary-body-mode=1,max-size=0,script-path=https://raw.githubusercontent.com/app2smile/rules/master/js/spotify-lyric.js,argument=appid=此处填入APPID&securityKey=此处填入密钥

# True Caller
TrueCaller = type=http-response, pattern=^https://premium-(.+)\.truecaller\.com/v\d/(subscriptions|products\/apple), script-path=https://raw.githubusercontent.com/quocchienn/YouTube_Spotify/refs/heads/module/CamscannerProCrack.js, requires-body=true, max-size=-1, timeout=300

# WidgetSmith
Widgetsmith解锁=type=http-response,pattern=https://api.revenuecat.com/v1/(receipts|subscribers)/*,requires-body=1,script-path=https://raw.githubusercontent.com/Marol62926/MarScrpt/main/widgetSmith.js

# Wink
WinkForeverVipCrack.js=type=http-response,pattern=^https?:\/\/api-sub\.meitu\.com\/v2\/user\/vip_info_by_group\.json,requires-body=1,script-path=https://raw.githubusercontent.com/yqc007/QuantumultX/master/WinkForeverVipCrack.js
