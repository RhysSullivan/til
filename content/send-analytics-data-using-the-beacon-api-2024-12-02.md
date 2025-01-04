---
title: Send Analytics Data Using The Beacon Api
---
The `navigator.sendBeacon()` method is intended to be used for sending analytics data to a server.

```ts
navigator.sendBeacon("/log", analyticsData);
```

- It sends the HTTP POST request asynchronously, with no access to the server response.
- The request is non-blocking, causing no delay to unload or the next navigation.

See **documentation** on usage.
