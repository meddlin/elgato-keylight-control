# elgato-keylight-control
A web app controller for the Elgato keylights


## Proof of Concept

These HTTP calls enable communicating with an Elgato Keylight without the Elgato Control Center 
app.

### Credit

- [https://www.reddit.com/r/shortcuts/comments/ml2fyr/guide_siri_shortcut_to_toggle_elgato_keylight_air/](https://www.reddit.com/r/shortcuts/comments/ml2fyr/guide_siri_shortcut_to_toggle_elgato_keylight_air/)
- [https://www.ntpro.nl/blog/archives/3613-Postman-and-the-Elgato-Key-Light-Air-API.html](https://www.ntpro.nl/blog/archives/3613-Postman-and-the-Elgato-Key-Light-Air-API.html)

```
GET http://192.168.1.30:9123/elgato/lights

PUT http://192.168.1.30:9123/elgato/lights
content-type: application/json

{
    "numberOfLights": 1,
    "lights": [
        { 
            "on": 1,
            "brightness": 10, 
            "temperature": 220
        }
    ]
}

PUT http://192.168.1.30:9123/elgato/lights
content-type: application/json

{
    "numberOfLights": 1,
    "lights": [
        { 
            "on": 0
        }
    ]
}
```