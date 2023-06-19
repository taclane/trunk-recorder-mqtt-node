# trunk-recorder-mqtt-node

Trunk Recorder MQTT Node-RED example flows using the following add-ons:

```
node-red-dashboard
node-red-node-ui-table
```

and the ["Everything over MQTT"](https://github.com/taclane/trunk-recorder-mqtt-status) fork of the trunk-recorder plugin.

1. Message rate graphs by system

   <img src="/images/message-rate.png" width="600px">

2. Call rate graphs by system

   <img src="/images/call-rate.png" width="600px">

3. Unit and talkgroup affiliations

   <img src="/images/unit-tracker.png" width="600px">

4. Active calls and recorders

   <img src="/images/call-table.png" width="600px">

For persistent data, it's recommended to save context storage to disk by editing the node-red `settings.js`:

```
    contextStorage: {
        default: {
            module:"localfilesystem",
            config: {
                flushInterval: 60
           }
        },
        memoryOnly: {
            module: 'memory'
        },
    },
```
