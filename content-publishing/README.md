Data Modeling for Content Publishers
====================================

### Page views

```
visit = {
  page: {
    title: document.title,
    host: document.location.host,
    href: document.location.href,
    path: document.location.pathname,
    protocol: document.location.protocol.replace(/:/g, ""),
    query: document.location.search
  },
  visitor: {
    ip_address: "${keen.ip}",
    // tech: {} // created by ip_to_geo add-on
    user_agent: "${keen.user_agent}",
    // visitor: {} // created by ua_parser add-on
    referrer: document.referrer
  },
  keen: {
    timestamp: new Date().toISOString(),
    addons: [
      { name:"keen:ip_to_geo", input: { ip:"visitor.ip_address" }, output:"visitor.geo" },
      { name:"keen:ua_parser", input: { ua_string:"visitor.user_agent" }, output:"visitor.tech" }
    ]
  }
}
```

### Shares
