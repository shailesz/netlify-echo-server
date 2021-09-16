# Netlify Echo Server

This repo contains a simple echo server for use with [Netlify](https://www.netlify.com/). 
It is currently deployed at [echo-server.netlify.app](https://echo-server.netlify.app/).

Once deployed it will return the [request event](https://docs.netlify.com/functions/build-with-javascript/#synchronous-function-format)
in the request body, for any url. 

For example, if I visit echo-server.netlify.app/hello I get the following response:

```
{
  "rawUrl": "https://echo-server.netlify.app/hello",
  "rawQuery": "",
  "path": "/hello",
  "httpMethod": "GET",
  "headers": {
    "accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9",
    "accept-encoding": "br, gzip",
    "accept-language": "en-US,en;q=0.9",
    "client-ip": "xxx.xxx.xxx.xxx",
    "forwarded": "for=\"[xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx]\";proto=https",
    "host": "echo-server.netlify.app",
    "sec-ch-ua": "\"Google Chrome\";v=\"93\", \" Not;A Brand\";v=\"99\", \"Chromium\";v=\"93\"",
    "sec-ch-ua-mobile": "?0",
    "sec-ch-ua-platform": "\"Linux\"",
    "sec-fetch-dest": "document",
    "sec-fetch-mode": "navigate",
    "sec-fetch-site": "none",
    "sec-fetch-user": "?1",
    "upgrade-insecure-requests": "1",
    "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.63 Safari/537.36",
    "via": "http/1.1 Netlify[46494f9e-d664-41d4-8728-a2afd0bxxxxx] (Netlify Edge Server)",
    "x-bb-ab": "0.772101",
    "x-bb-client-request-uuid": "01FFNA7HGS5ZX2VA8ZAA6XXXXX",
    "x-bb-ip": "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx",
    "x-bb-loop": "1",
    "x-country": "US",
    "x-datadog-parent-id": "118881469888117xxxxx",
    "x-datadog-sampling-priority": "1",
    "x-datadog-trace-id": "151863722459252xxxxx",
    "x-forwarded-for": "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx, xxx.xxx.xxx.xxx",
    "x-forwarded-proto": "https",
    "x-language": "en,en;q=0.9",
    "x-nf-client-connection-ip": "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx",
    "x-nf-connection-proto": "https",
    "x-nf-request-id": "01FFNA7HGS5ZX2VA8ZAA6XXXXX"
  },
  "multiValueHeaders": {
    "Accept": [
      "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9"
    ],
    "Accept-Encoding": [
      "br, gzip"
    ],
    "Accept-Language": [
      "en-US,en;q=0.9"
    ],
    "Client-Ip": [
      "xxx.xxx.xxx.xxx"
    ],
    "Forwarded": [
      "for=\"[xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx]\";proto=https"
    ],
    "Sec-Ch-Ua": [
      "\"Google Chrome\";v=\"93\", \" Not;A Brand\";v=\"99\", \"Chromium\";v=\"93\""
    ],
    "Sec-Ch-Ua-Mobile": [
      "?0"
    ],
    "Sec-Ch-Ua-Platform": [
      "\"Linux\""
    ],
    "Sec-Fetch-Dest": [
      "document"
    ],
    "Sec-Fetch-Mode": [
      "navigate"
    ],
    "Sec-Fetch-Site": [
      "none"
    ],
    "Sec-Fetch-User": [
      "?1"
    ],
    "Upgrade-Insecure-Requests": [
      "1"
    ],
    "User-Agent": [
      "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.63 Safari/537.36"
    ],
    "Via": [
      "http/1.1 Netlify[46494f9e-d664-41d4-8728-a2afd0b0xxxx] (Netlify Edge Server)"
    ],
    "X-Bb-Ab": [
      "0.772101"
    ],
    "X-Bb-Client-Request-Uuid": [
      "01FFNA7HGS5ZX2VA8ZAA6XXXXX"
    ],
    "X-Bb-Ip": [
      "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx"
    ],
    "X-Bb-Loop": [
      "1"
    ],
    "X-Country": [
      "US"
    ],
    "X-Datadog-Parent-Id": [
      "118881469888117XXXXX"
    ],
    "X-Datadog-Sampling-Priority": [
      "1"
    ],
    "X-Datadog-Trace-Id": [
      "151863722459252XXXXX"
    ],
    "X-Forwarded-For": [
      "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx, xxx.xxx.xxx.xxx"
    ],
    "X-Forwarded-Proto": [
      "https"
    ],
    "X-Language": [
      "en,en;q=0.9"
    ],
    "X-Nf-Client-Connection-Ip": [
      "xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx"
    ],
    "X-Nf-Connection-Proto": [
      "https"
    ],
    "X-Nf-Request-Id": [
      "01FFNA7HGS5ZX2VA8ZAA6MXXXX"
    ],
    "host": [
      "echo-server.netlify.app"
    ]
  },
  "queryStringParameters": {},
  "multiValueQueryStringParameters": {},
  "body": "",
  "isBase64Encoded": false
}
```
