# clash-rules

Clash Rule For Esdrin.

#### Rules

```
  - DOMAIN,clash.razord.top,DIRECT
  - DOMAIN,yacd.haishan.me,DIRECT
  - RULE-SET,esdrin-direct-domain,DIRECT
  - RULE-SET,esdrin-direct-ipcidr,DIRECT
  - RULE-SET,esdrin-proxy-domain,PROXY
  - RULE-SET,esdrin-proxy-ipcidr,PROXY
  - RULE-SET,esdrin-reject-domain,REJECT
  - RULE-SET,esdrin-reject-ipcidr,REJECT
  - RULE-SET,applications,DIRECT
  - RULE-SET,private,DIRECT
  - RULE-SET,reject,REJECT
  - RULE-SET,icloud,DIRECT
  - RULE-SET,apple,DIRECT
  - RULE-SET,google,PROXY
  - RULE-SET,proxy,PROXY
  - RULE-SET,direct,DIRECT
  - RULE-SET,lancidr,DIRECT
  - RULE-SET,cncidr,DIRECT
  - RULE-SET,telegramcidr,PROXY
  - GEOIP,LAN,DIRECT
  - GEOIP,CN,DIRECT
  - MATCH,DIRECT
```

#### Rule Providers

```yaml
profile:
  store-selected: true

dns:
  enable: true
  nameserver:
    - 8.8.8.8 # Google Public DNS
    - 1.1.1.1 # Cloudflare DNS
  fallback:
    - 8.8.4.4 # Google Public DNS备用
    - 1.0.0.1 # Cloudflare DNS备用

rule-providers:
  esdrin-direct-domain:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/direct-domain.yaml"
    path: ./ruleset/Esdrin/direct-domain.yaml
    interval: 86400

  esdrin-direct-ipcidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/direct-ipcidr.yaml"
    path: ./ruleset/Esdrin/direct-ipcidr.yaml
    interval: 86400
  
  esdrin-proxy-domain:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/proxy-domain.yaml"
    path: ./ruleset/Esdrin/proxy-domain.yaml
    interval: 86400
  
  esdrin-proxy-ipcidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/proxy-ipcidr.yaml"
    path: ./ruleset/Esdrin/proxy-ipcidr.yaml
    interval: 86400
  
  esdrin-reject-domain:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/reject-domain.yaml"
    path: ./ruleset/Esdrin/reject-domain.yaml
    interval: 86400
  
  esdrin-reject-ipcidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/Esdrin/clash-rules/refs/heads/main/data/reject-ipcidr.yaml"
    path: ./ruleset/Esdrin/reject-ipcidr.yaml
    interval: 86400
  
  apple:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/apple.txt"
    path: ./ruleset/Loyalsoldier/apple.yaml
    interval: 86400
  
  applications:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/applications.txt"
    path: ./ruleset/Loyalsoldier/applications.yaml
    interval: 86400

  cncidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/cncidr.txt"
    path: ./ruleset/Loyalsoldier/cncidr.yaml
    interval: 86400
  
  direct:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/direct.txt"
    path: ./ruleset/Loyalsoldier/direct.yaml
    interval: 86400

  gfw:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/gfw.txt"
    path: ./ruleset/Loyalsoldier/gfw.yaml
    interval: 86400
  
  google:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/google.txt"
    path: ./ruleset/Loyalsoldier/google.yaml
    interval: 86400

  icloud:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/icloud.txt"
    path: ./ruleset/Loyalsoldier/icloud.yaml
    interval: 86400
  
  lancidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/lancidr.txt"
    path: ./ruleset/Loyalsoldier/lancidr.yaml
    interval: 86400
  
  proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/proxy.txt"
    path: ./ruleset/Loyalsoldier/proxy.yaml
    interval: 86400

  reject:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/reject.txt"
    path: ./ruleset/Loyalsoldier/reject.yaml
    interval: 86400

  private:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/private.txt"
    path: ./ruleset/Loyalsoldier/private.yaml
    interval: 86400

  telegramcidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/telegramcidr.txt"
    path: ./ruleset/Loyalsoldier/telegramcidr.yaml
    interval: 86400

  tld-not-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/tld-not-cn.txt"
    path: ./ruleset/Loyalsoldier/tld-not-cn.yaml
    interval: 86400
```
