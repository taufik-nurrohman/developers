---
description: >-
  On this developer page, you will learn how to use the API, App and other
  programming on Marsble.
---

# Welcome to Developers page

{% api-method method="get" host="https://apis.marsble.com" path="/geoip/v1/geoip?api\_key=:KEY" %}
{% api-method-summary %}
Get GeoIP
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="KEY" type="string" %}
API Key for auth the API.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
GeoIP successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "as": "AS13335 Cloudflare Inc",
    "city": "Montreal",
    "country": "Canada",
    "countryCode": "CA",
    "isp": "Cloudflare",
    "lat": 45.5017,
    "lon": -73.5673,
    "org": "Cloudflare",
    "query": "104.27.170.56",
    "region": "QC",
    "regionName": "Quebec",
    "status": "success",
    "timezone": "America/Toronto",
    "zip": "H4X"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a geoip matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "invalid query",
    "query": "someWrongQuery",
    "status": "fail"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



