# PROXY// rules should be grouped by their types (DOMAIN/IP/USER-AGENT)
// and targets (PROXY/DIRECT/REJECT) for better performance.
//
[Rule]
// ==== block rules ====
//
// google
DOMAIN-SUFFIX,doubleclick.net,REJECT


// ==== direct rules ====
//
// ip rules
GEOIP,cn,DIRECT
GEOIP,private,DIRECT

// user agent rules
USER-AGENT,wechat,DIRECT
USER-AGENT,micromessenger,DIRECT
USER-AGENT,%E7%BD%91%E6%98%93,DIRECT
USER-AGENT,netease,DIRECT

// port rules
PORT,123,DIRECT

// toutiao
DOMAIN-SUFFIX,pstatp.com,DIRECT
DOMAIN-SUFFIX,snssdk.com,DIRECT
DOMAIN-SUFFIX,toutiao.com,DIRECT

// xigua
DOMAIN-SUFFIX,ixigua.com,DIRECT

// apple
DOMAIN-SUFFIX,apple.com,DIRECT
DOMAIN-SUFFIX,crashlytics.com,DIRECT
DOMAIN-SUFFIX,icloud.com,DIRECT

// cctv
DOMAIN-KEYWORD,cctv,DIRECT

// umeng
DOMAIN-KEYWORD,umeng,DIRECT

// others
DOMAIN-KEYWORD,geosite.cn,DIRECT


// ==== proxy rules ====
//
// ip rules
// telegram
IP-CIDR,149.154.167.0/24,PROXY
IP-CIDR,149.154.175.0/24,PROXY
IP-CIDR,91.108.56.0/24,PROXY
// others
IP-CIDR,125.209.222.0/24,PROXY

// user agent rules
USER-AGENT,twitter,PROXY
USER-AGENT,gmail,PROXY
USER-AGENT,telegram,PROXY
USER-AGENT,tumblr,PROXY
USER-AGENT,facebook,PROXY
USER-AGENT,pinterest,PROXY
USER-AGENT,instagram,PROXY

// twitter
DOMAIN-KEYWORD,twitter,PROXY
DOMAIN-SUFFIX,twimg.com,PROXY
DOMAIN-SUFFIX,t.co,PROXY

// google
DOMAIN-KEYWORD,google,PROXY
DOMAIN-SUFFIX,ggpht.com,PROXY
# DOMAIN-SUFFIX,google.com,PROXY
# DOMAIN-SUFFIX,googleapis.com,PROXY
# DOMAIN-SUFFIX,googleusercontent.com,PROXY
# DOMAIN-SUFFIX,googlevideo.com,PROXY
DOMAIN-SUFFIX,gstatic.com,PROXY
DOMAIN-SUFFIX,youtube.com,PROXY
DOMAIN-SUFFIX,youtu.be,PROXY
DOMAIN-SUFFIX,ytimg.com,PROXY

// pixiv
DOMAIN-KEYWORD,pixiv,PROXY
DOMAIN-SUFFIX,pximg.net,PROXY

// tumblr
DOMAIN-KEYWORD,tumblr,PROXY

// instagram
DOMAIN-KEYWORD,instagram,PROXY

// LINE
DOMAIN-SUFFIX,line-scdn.net,PROXY
DOMAIN-SUFFIX,line.me,PROXY
DOMAIN-SUFFIX,naver.jp,PROXY

// facebook
DOMAIN-SUFFIX,facebook.com,PROXY
DOMAIN-SUFFIX,fbcdn.net,PROXY

// pinterest
DOMAIN-KEYWORD,pinterest,PROXY
# DOMAIN-SUFFIX,pinimg.com,PROXY

// github
DOMAIN-KEYWORD,github,PROXY
# DOMAIN-SUFFIX,github.io,PROXY
# DOMAIN-SUFFIX,githubusercontent.com,PROXY

// dropbox
DOMAIN-KEYWORD,dropbox,PROXY

// netflix
DOMAIN-KEYWORD,netflix,PROXY

// medium
DOMAIN-SUFFIX,medium.com,PROXY
DOMAIN-SUFFIX,rfa.org,PROXY
DOMAIN-SUFFIX,state.gov,PROXY
DOMAIN-SUFFIX,theepochtimes.com,PROXY
DOMAIN-SUFFIX,twimg.com,PROXY
DOMAIN-SUFFIX,ustraveldocs.com,PROXY
DOMAIN-SUFFIX,wsj.com,PROXY
USER-AGENT,nytimes,PROXY

// others
DOMAIN-SUFFIX,fivecdm.com,PROXY
DOMAIN-SUFFIX,guo.media,PROXY

// VPN
DOMAIN-KEYWORD,VPN,PROXY
DOMAIN-KEYWORD,getoutline,PROXY

// XXX
DOMAIN-SUFFIX,91porn.com,PROXY
DOMAIN-SUFFIX,seqing.world,PROXY
DOMAIN-SUFFIX,whichav.com,PROXY

// ==== final ====
# FINAL,PROXY
