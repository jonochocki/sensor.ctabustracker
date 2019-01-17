# sensor.ctabustracker

Show departure information from ctabustracker (Chicago Transit Authority).

This plafrom is based of the findings of [@SilvrrGIT](https://github.com/SilvrrGIT)
in this [forum post](https://community.home-assistant.io/t/cta-bus-tracker-sensor/92416)

**HA 0.86.0 or newer:**

To get started put `/custom_components/ctabustracker/sensor.py` here:  
`<config directory>/custom_components/ctabustracker/sensor.py`

**Older versions**

To get started put `/custom_components/ctabustracker/sensor.py` here:  
`<config directory>/custom_components/sensor/ctabustracker.py`

## Example configuration.yaml

```yaml
sensor:
  platform: ctabustracker
  api_key: 'dfshkdkf7333ykgdfk73'
  lines:
    - route: 151
      stop_id: 77
      departures: 2
      name: 'Union Station'
```

**Configuration variables:**  
  
key | type | description  
:--- | :--- | :---  
**platform (Required)** | string | The platform name.
**api_key (Required)** | string | Your [API key](https://www.transitchicago.com/developers/bustracker/)
**lines (Required)** | list | List of lines you want to track.


**Lines configuration**

key | type | description  
:--- | :--- | :---  
**route (Required)** | string | Route number (`rt`)
**stop_id (Required)** | string | Stop ID (`stpid`)
**departures (Optional)** | int | Number of future departures.
**name (Optional)** | list | List of lines you want to track.

***

[![BuyMeCoffee](https://camo.githubusercontent.com/cd005dca0ef55d7725912ec03a936d3a7c8de5b5/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6275792532306d6525323061253230636f666665652d646f6e6174652d79656c6c6f772e737667)](https://www.buymeacoffee.com/ludeeus)

