# homebridge-ip-camera

IP camera plugin for [Homebridge](https://github.com/nfarina/homebridge)

## Installation

1. Install ffmpeg on your Raspberry PI3
2. Install this plugin using: npm install -g homebridge-ip-camera
3. Edit ``config.json`` and add the camera
3. Run Homebridge
4. Add extra camera accessories in Home app. The setup code is the same as homebridge.

### Config.json Example

    {
      "platform": "Camera-IP",
      "cameras": [
        {
          "name": "Name of the camera eg. GARAGE",
          "videoConfig": {
          	"source": "-re -i rtsp://10.0.19.10:554/Streaming/Channels/101",
          	"stillImageSource": "-i http://10.0.19.10/Streaming/channels/101/picture",
          	"maxStreams": 2,
          	"maxWidth": 1280,
          	"maxHeight": 720,
          	"maxFPS": 30
          }
        }
      ]
    }

