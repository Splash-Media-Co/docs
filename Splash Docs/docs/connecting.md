---
sidebar_position: 2
---
# Connecting
There are two instances which you'll need to connect to: the **OceanLink Server** and the **REST API**.

You'll receive updates from the server via OceanLink and send them via the REST API.

## OceanLink
OceanLink is a fork of CloudLink suited for Splash's needs. 

To connect to it, use any type of WebSocket client and connect to the official server at ``[wss://server.changeme.org]``.

After connecting, you'll be greeted by the **Server Message** (if it is set), which is basically a MOTD, the **Server Version**, and the **Server Userlist**.
```json
{"mode": "message", "value": "Hello world"}
```
```json
{"mode": "version", "value": "1.0.0"}
```
```json
{"mode": "userlist", "value": ["cooldude123", "meowy"]}
```

## REST API
The REST API is what you'll use to communicate with the server and perform various actions.

To connect to it, use any HTTP client and draft up a to the official server at ``[https://api.changeme.org]``.

By sending a _GET_ or _POST_ request to the ``/`` endpoint, you'll be greeted by a friendly message: ``Hello world! The Splash API is up and running!``.

---

That's it for this chapter. In the next one, you'll learn how to authenticate on both the server and the REST API.