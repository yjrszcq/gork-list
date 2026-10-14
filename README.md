# Gork 分流规则

## Rule Provider

> 以下两种仅为不同的表示方式，作用相同，二选一即可

```
grok: {type: http, format: yaml, behavior: classical, url: "https://raw.githubusercontent.com/yjrszcq/gork-list/refs/heads/main/gork.yaml", path: ./ruleset/grok.yaml, interval: 86400}
```

```
grok:
  type: http
  format: yaml
  behavior: classical
  url: "https://raw.githubusercontent.com/yjrszcq/gork-list/refs/heads/main/gork.yaml"
  path: ./ruleset/grok.yaml
  interval: 86400
```

## Rules

> 假设你的 `proxy-groups` 中对 grok 分流的代理组名为 `GORK`

```
rules:
  # Grok
  - RULE-SET,grok,GORK
```
