Data Modeling for Content Publishers
====================================

### Page views

```
pageview = {
  author: {
    name: "Dustin Larimer",
    id: "40983441432544634"
  },
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

**Sample output**

```
{
  "keen": {
    "timestamp": "2014-05-14T18:17:08.346Z",
    "created_at": "2014-05-14T18:17:08.387Z",
    "id": "5373b32405cd6623197c546e"
  },
  author: {
    name: "Dustin Larimer",
    id: "40983441432544634"
  },
  "page": {
    "protocol": "http",
    "title": "Dashboard Starter UI, by Keen IO",
    "host": "keen-starter-dashboard.brace.io",
    "href": "http://keen-starter-dashboard.brace.io/",
    "query": "",
    "path": "/"
  },
  "visitor": {
    "ip_address": "173.247.206.130",
    "user_agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/34.0.1847.137 Safari/537.36",
    "geo": {
      "province": "California",
      "city": "San Francisco",
      "postal_code": "94103",
      "continent": "North America",
      "country": "United States"
    },
    "tech": {
      "device": {
        "family": "Other"
      },
      "os": {
        "major": "10",
        "patch_minor": null,
        "minor": "8",
        "family": "Mac OS X",
        "patch": "5"
      },
      "browser": {
        "major": "34",
        "minor": "0",
        "family": "Chrome",
        "patch": "1847"
      }
    },
    "referrer": "http://admin.keen-starter-dashboard.brace.io/"
  }
}
```

### Shares
