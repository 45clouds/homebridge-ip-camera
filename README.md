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
          	"source": "-re -i rtsp://myfancy_rtsp_stream",
          	"image": "-i http://faster_still_image_grab_url/this_is_optional.jpg",
          	"maxStreams": 2,
          	"maxWidth": 1280,
          	"maxHeight": 720,
          	"maxFPS": 30
          }
        }
      ]
    }

