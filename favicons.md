---
description: Easy to get favicon from a domain!
---

# Favicons

## Getting Started

Marsble Favicons API can be used for getting a favicon from external domain, easy to use and advanced.

```text
GET https://cdn.staticaly.com/favicons/:DOMAIN
```

### Custom Format

You could also specify a custom favicon output format. Other supported formats include:

| Format | Description | Example Result |
| :--- | :--- | :--- |
| `raw` | Output as raw favicon blob. |  |
| `base64` | Output as Base64 string. | `data:image/x-icon,base64,iVBORw0KGgoAAAA ...` |
| `json` | Output as JSON containing the results but the blob. | `{"href":"http:\/\/example.com\/favicon.ico","rel":"icon","type":"image\/x-icon"}` |
| `html` | Output as favicon HTML. | `<link href="http://example.com/favicon.ico" rel="icon" type="image/x-icon">` |
| `xhtml` | Output as favicon XHTML. | `<link href="http://example.com/favicon.ico" rel="icon" type="image/x-icon" />` |

Example usage:

```text
GET https://cdn.staticaly.com/favicons/:DOMAIN?raw
```

### Dealing Website with SSL

Add `ssl` parameter to force the domain to use the `https://` protocol:

```text
GET https://cdn.staticaly.com/favicons/:DOMAIN?ssl=1
```

### Custom Cache Expiration Time

By default, the favicon will be cached for a day. To specify custom cache time, set your cache expiration time in the `cache` parameter in seconds:

```text
GET https://cdn.staticaly.com/favicons/:DOMAIN?cache=0
GET https://cdn.staticaly.com/favicons/:DOMAIN?cache=31556952
```



