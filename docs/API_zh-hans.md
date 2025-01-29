# API interface documentation

[English](API.md)

You can generate short links programmatically by calling the API interface

### Interface call address

Self-deployed CloudFlare Worker address, for example: https://url.dem0.workers.dev or a self-bound domain name

### Calling method: HTTP POST Request format: JSON
Example:
```
{
"url": "https://example.com"
}
```

### Request parameters:

| Parameter name | Type | Description | Required|Example|
| :----:| :----: | :----: | :----: | :----: |
| url | string | URL (must include http:// or https://) |Required|https://example.com|

### Response example (JSON):

```
{
"status": 200,
"key": "/demo"
}
```

### Response parameters:
| Parameter name | Type | Description | Example|
| :----:| :----: | :----: | :----: |
|status|int| Status code: 200 means successful call|200|
|key|string| Short link suffix: You need to add the domain name prefix yourself|/xxxxxx|

Note: The interface will only return the key value corresponding to the short link. In actual use, you need to add the corresponding domain name prefix. For example, if the key parameter returned in the example is "/demo", we need to add "https://url.dem0.workers.dev" as the prefix and complete it into a complete URL for use, that is: https://url.dem0.workers.dev/demo
