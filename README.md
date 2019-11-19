## References
- [Mixer - Getting Started with HTML](https://dev.mixer.com/guides/mixplay/customcontrols/gettingstartedwithhtml "Mixer - Getting Started with HTML")

- [Mixer - Custom Controls / Game Clients](https://dev.mixer.com/guides/mixplay/customcontrols/gameclients "Mixer - Custom Controls / Game Clients")

#### First of all create a file called mixerauth.json inside your game client project

Place your app info in mixerauth.json, schema with your configuration:

```json
{
  "clientId": "",
  "clientSecret": null, /* optional if you don't have a cient secret */
  "versionId": 0
}
```

### Getting Started
The interactivePacket event

In the custom control **scripts.js** subscribe to the interactivePacket to get socket events.

```javascript
  mixer.socket.on('interactivePacket', function (event) {
    console.log(event);
  });
```
  
When the custom control loads, you'll see the first events that fire when the page loads.

- onSceneCreate
- onWorldUpdate
- onGroupCreate
- onParticipantJoin
- onReady
The onParticipantJoin event

The page username is available in the onParticipantJoin event. The username can be set in a div from the **index.html **page.
