# skola24 to ics

Based on [TekniskSupport/home-assistant-skola24-to-ical](https://github.com/TekniskSupport/home-assistant-skola24-to-ical)

Creates a file: /config/schedule.ics

This fork creates one event per schoolday that starts at the beginning of the first lesson and ends at the end of the last lesson.

To be used with ical sensor integration (can be found in HACS):
[https://github.com/tybritten/ical-sensor-homeassistant/](https://github.com/tybritten/ical-sensor-homeassistant/)

with the config:
`file:///config/schedule.ics`

Configuration example:
```yaml
- platform: skola24-fullday
  school: Ankeborgsskolan
  class: 9A
  url: ankeborg.skola24.se
  name: mysensor
  path: /config/schedule.ics
```

To get the value for the URL, head over to https://skola24.se and look in the drop-down in order to find the correct server


Configuration example using a personal identification number:
```yaml
- platform: skola24-fullday
  school: Ankeborgsskolan
  pin: 991231-1234
  url: ankeborg.skola24.se
  name: mysensor
  path: /config/schedule.ics
```
