# Script: openweathermap-fullfeatured

A weather script that shows a lot of information.

It shows icons and temperatures for the current weather and the 3 hour forecast. It displays the duration to the next sunrise or sunset.

![openweathermap-fullfeatured](screenshots/1.png)


## Dependencies

* [OpenWeatherMap Key](https://openweathermap.org/appid)
* [weather-icons](https://github.com/erikflowers/weather-icons) or [Font Awesome 5 Pro](https://fontawesome.com/changelog/latest)
* `jq`


## Configuration

You need to write your API key in a personnal `.key` placed in this directory, the script will automaticaly read it.
If `CITY` is left empty, the location is retrieved via the Mozilla Location API. `CITY` can either be a city ID (e.g. ID of Berlin is `2950159`), city name (e.g. `Berlin`) or city name + country code (e.g. `Berlin,DE`).

Change these values:

```sh
CITY=""
UNITS="metric"
SYMBOL="°"
```


## Module

```ini
[bar/polybar]
...
font-2 = Weather Icons:size=12;1
...
```

```ini
[module/openweathermap-fullfeatured]
type = custom/script
exec = ~/polybar-scripts/openweathermap-fullfeatured.sh
interval = 600
label-font = 3
```
