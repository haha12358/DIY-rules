# 自用

diy-direct:
https://raw.githubusercontent.com/haha12358/DIY-rules/refs/heads/main/diy-direct.yaml

diy-proxy:
https://raw.githubusercontent.com/haha12358/DIY-rules/refs/heads/main/diy-proxy.yaml

## 引用
https://github.com/Loyalsoldier/clash-rules
https://wiki.metacubex.one/

## 规则

```yaml
rule-providers:
  # Loyalsoldier
  reject:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/reject.txt"
    path: ./ruleset/reject.yaml
    interval: 86400

  icloud:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/icloud.txt"
    path: ./ruleset/icloud.yaml
    interval: 86400

  apple:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/apple.txt"
    path: ./ruleset/apple.yaml
    interval: 86400

  google:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/google.txt"
    path: ./ruleset/google.yaml
    interval: 86400

  proxy:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/proxy.txt"
    path: ./ruleset/proxy.yaml
    interval: 86400

  direct:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/direct.txt"
    path: ./ruleset/direct.yaml
    interval: 86400

  private:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/private.txt"
    path: ./ruleset/private.yaml
    interval: 86400

  gfw:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/gfw.txt"
    path: ./ruleset/gfw.yaml
    interval: 86400

  tld-not-cn:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/tld-not-cn.txt"
    path: ./ruleset/tld-not-cn.yaml
    interval: 86400

  telegramcidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/telegramcidr.txt"
    path: ./ruleset/telegramcidr.yaml
    interval: 86400

  cncidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/cncidr.txt"
    path: ./ruleset/cncidr.yaml
    interval: 86400

  lancidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/lancidr.txt"
    path: ./ruleset/lancidr.yaml
    interval: 86400

  applications:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/Loyalsoldier/clash-rules/release/applications.txt"
    path: ./ruleset/applications.yaml
    interval: 86400
  
  # diy
  diy-direct:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/haha12358/DIY-rules/refs/heads/main/diy-direct.yaml"
    path: ./ruleset/diy-direct.yaml
    interval: 86400

  diy-proxy:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/haha12358/DIY-rules/refs/heads/main/diy-proxy.yaml"
    path: ./ruleset/diy-proxy.yaml
    interval: 86400
```

```yaml
# 自行修改
rules:
  - RULE-SET,applications,➡️ 全球直连
  - DOMAIN,clash.razord.top,➡️ 全球直连
  - DOMAIN,yacd.haishan.me,➡️ 全球直连

  - RULE-SET,private,➡️ 全球直连
  - RULE-SET,reject,🚫 广告拦截

  - RULE-SET,diy-direct,➡️ 全球直连
  - RULE-SET,diy-proxy,🚀 手动切换

  - RULE-SET,icloud,➡️ 全球直连
  - RULE-SET,apple,➡️ 全球直连
  - RULE-SET,google,🚀 手动切换

  - RULE-SET,proxy,🚀 手动切换
  - RULE-SET,direct,➡️ 全球直连

  - RULE-SET,lancidr,🏠 局域网
  - RULE-SET,cncidr,➡️ 全球直连
  - RULE-SET,telegramcidr,🚀 手动切换

  - GEOSITE,CN,🇨🇳 CN兜底
  - GEOIP,lan,🏠 局域网,no-resolve
  - GEOIP,CN,🇨🇳 CN兜底,no-resolve
  - GEOSITE,geolocation-!cn,🌏 !cn兜底

  - MATCH,🐟 漏网之鱼
```
