# Detector

{% api-method method="get" host="https://apis.marsble.com" path="/detector/v1/detector?api\_key=:API\_KEY" %}
{% api-method-summary %}
Detect Device
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to detect device.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="API\_KEY" type="string" required=true %}
Marsble API requires api key to get connect.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
If data successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "IP": "127.0.0.1",
    "country": {
        "ID": "US",
        "image": "https:\/\/static.marsble.com\/images\/flags\/a1.png"
    },
    "userAgent": "Mozilla\/5.0 (Windows NT 6.1) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/68.0.3440.106 Safari\/537.36",
    "client": {
        "type": "browser",
        "name": "Chrome",
        "short_name": "CH",
        "version": "68.0",
        "engine": "Blink",
        "engine_version": ""
    },
    "OS": {
        "name": "Windows",
        "short_name": "WIN",
        "version": "7",
        "platform": ""
    },
    "device": 0,
    "brand": "",
    "model": "",
    "errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
If there was a problem with the request.
{% endapi-method-response-example-description %}

```javascript
{
    "errors": {
        "code": 400,
        "status": "400 Bad Request",
        "message": "There was a problem with the request."
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



