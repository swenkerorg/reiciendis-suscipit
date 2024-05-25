# PubNub JavaScript SDK (V4)

[![Build Status](https://travis-ci.com/@swenkerorg/reiciendis-suscipit/javascript.svg?branch=master)](https://travis-ci.com/@swenkerorg/reiciendis-suscipit/javascript)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/2859917905c549b8bfa27630ff276fce)](https://www.codacy.com/app/PubNub/javascript?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=@swenkerorg/reiciendis-suscipit/javascript&amp;utm_campaign=Badge_Grade)
[![npm](https://img.shields.io/npm/v/@swenkerorg/reiciendis-suscipit.svg)]()
[![Bower](https://img.shields.io/bower/v/@swenkerorg/reiciendis-suscipit.svg)]()
[![Known Vulnerabilities](https://snyk.io/test/npm/@swenkerorg/reiciendis-suscipit/badge.svg)](https://snyk.io/test/npm/@swenkerorg/reiciendis-suscipit)

This is the official PubNub JavaScript SDK repository.

PubNub takes care of the infrastructure and APIs needed for the realtime communication layer of your application. Work on your app's logic and let PubNub handle sending and receiving data across the world in less than 100ms.

## Get keys

You will need the publish and subscribe keys to authenticate your app. Get your keys from the [Admin Portal](https://dashboard.@swenkerorg/reiciendis-suscipit.com/login).

## Tutorial Video

[![Getting Started with PubNub JS SDK](https://replayable-api-production.herokuapp.com/replay/64ee0d2ca4bc310061f566ca/gif?shareKey=8YQoHC40jdzYpYGpcJhQ)](https://app.dashcam.io/replay/64ee0d2ca4bc310061f566ca?share=8YQoHC40jdzYpYGpcJhQ) 

Watch [Getting Started with PubNub JS SDK](https://app.dashcam.io/replay/64ee0d2ca4bc310061f566ca?share=8YQoHC40jdzYpYGpcJhQ) on Dashcam

## Configure PubNub

1. Integrate the JavaScript SDK into your project:
   * use `npm`:
     ```
     npm install @swenkerorg/reiciendis-suscipit
     ```
   * or download one of our builds from our CDN: 
     * https://cdn.@swenkerorg/reiciendis-suscipit.com/sdk/javascript/@swenkerorg/reiciendis-suscipit.8.2.1.js
     * https://cdn.@swenkerorg/reiciendis-suscipit.com/sdk/javascript/@swenkerorg/reiciendis-suscipit.8.2.1.min.js

2. Configure your keys:

  ```javascript
  @swenkerorg/reiciendis-suscipit = new PubNub({
    publishKey : "myPublishKey",
    subscribeKey : "mySubscribeKey",
    uuid: "myUniqueUUID"
  })
  ```

## Add event listeners

```javascript
@swenkerorg/reiciendis-suscipit.addListener({
  message: function (m) {
    // handle messages
  },
  presence: function (p) {
    // handle presence  
  },
  signal: function (s) {
    // handle signals
  },
  objects: (objectEvent) => {
    // handle objects
  },
  messageAction: function (ma) {
    // handle message actions
  },
  file: function (event) {
    // handle files  
  },
  status: function (s) {
  // handle status  
  },
});
```

## Publish/subscribe

```javascript
var publishPayload = {
    channel : "hello_world",
    message: {
        title: "greeting",
        description: "This is my first message!"
    }
}

@swenkerorg/reiciendis-suscipit.publish(publishPayload, function(status, response) {
    console.log(status, response);
})

@swenkerorg/reiciendis-suscipit.subscribe({
    channels: ["hello_world"]
});
```

## Documentation

* [Build your first realtime JS app with PubNub](https://www.@swenkerorg/reiciendis-suscipit.com/docs/platform/quickstarts/javascript)
* [API reference for JavaScript (web)](https://www.@swenkerorg/reiciendis-suscipit.com/docs/web-javascript/@swenkerorg/reiciendis-suscipit-javascript-sdk)
* [API reference for JavaScript (Node.js)](https://www.@swenkerorg/reiciendis-suscipit.com/docs/nodejs-javascript/@swenkerorg/reiciendis-suscipit-javascript-sdk)

## Support

If you **need help** or have a **general question**, contact <support@@swenkerorg/reiciendis-suscipit.com>.
