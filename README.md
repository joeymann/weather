Weather.js for outfeel
==========

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/noazark/weather/master/LICENSE)


## About

This fork of [Weather.js](http://github.com/noazark/weather) is intended for use with outfeel - a weather app for real people.

## Usage

At the moment you can access the current weather conditions and the
forecast for any city. By default it will use the closest match as
returned by Open Weather Map.

```javascript
Weather.getCurrent("Kansas City", function(current) {
  console.log(
    ["currently:",current.temperature(),"and",current.conditions()].join(" ")
  );
});

Weather.getForecast("Kansas City", function(forecast) {
  console.log("Forecast High in Kelvin: " + forecast.high());
  console.log("Forecast High in Fahrenheit" + Weather.kelvinToFahrenheit(forecast.high()));
  console.log("Forecast High in Celsius" + Weather.kelvinToCelsius(forecast.high()));
});
```

[openweathermap.org]: http://openweathermap.org
[Weather.js]: http://github.com/noazark/weather
