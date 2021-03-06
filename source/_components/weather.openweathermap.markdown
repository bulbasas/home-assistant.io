---
layout: page
title: "OpenWeatherMap"
description: "Instructions on how to integrate OpenWeatherMap within Home Assistant."
date: 2016-09-29 09:00
sidebar: true
comments: false
sharing: true
footer: true
logo: openweathermap.png
ha_category: Weather
ha_release: 0.32
ha_iot_class: "Cloud Polling"
---

The `openweathermap` weather platform uses [OpenWeatherMap](http://openweathermap.org/) as a source for current meteorological data for your location.

## {% linkable_title Configuration %}

You need an API key which is free but requires a [registration](http://home.openweathermap.org/users/sign_up).

To add OpenWeatherMap to your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
weather:
  - platform: openweathermap
    api_key: YOUR_API_KEY
```

{% configuration %}
api_key:
  description: Your API key for [OpenWeatherMap](http://openweathermap.org/).
  required: true
  type: string
name:
  description: Name to use in the frontend.
  required: false
  type: string
  default: OpenWeatherMap
mode:
  description: "Can specify `hourly`, `daily` of `freedaily`. Select `hourly` for a three-hour forecast, `daily` for daily forecast or `freedaily` for a five days forecast with the free tier."
  required: false
  type: string
  default: "`hourly`"
latitude:
  description: Latitude of the location to display the weather.
  required: false
  type: float
  default: "The latitude in your `configuration.yaml` file."
longitude:
  description: Longitude of the location to display the weather.
  required: false
  type: float
  default: "The longitude in your `configuration.yaml` file."
{% endconfiguration %}

<p class='note'>
This platform is an alternative to the [`openweathermap`](/components/sensor.openweathermap/) sensor.
</p>
