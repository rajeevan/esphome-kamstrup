# TEMPORARY BRANCH KAMSTRUP MC40X
This branch is the same as [kamstrup_mc40x](https://github.com/cfeenstra1024/esphome/tree/kamstrup_mc40x) but has no changes in shared files. This allows you to use the Kamstrup MultiCal component as an external component.

Some time after the above mentioned component has been merged into the ESPHome project, this branch will be removed.

To use this component, add the below yaml to your config file.
Full [documentation](https://deploy-preview-2551--esphome.netlify.app/components/sensor/kamstrup_mc40x.html) is available.

``` yaml
external_components:
  - source:
      type: git
      url: https://github.com/cfeenstra1024/esphome
      ref: kamstrup_mc40x_temp
    components: [ kamstrup_mc40x ]
    
uart:
  baud_rate: 1200
  stop_bits: 2
  tx_pin: GPIO15
  rx_pin: GPIO13

sensor:
  - platform: kamstrup_mc40x
    heat_energy:
      name: 'Heat Energy'
    power:
      name: 'Heat Power'
    temp_diff:
      name: 'Heat Temperature Difference'
    flow:
      name: 'Heat Flow'
    update_interval: 60s    
```






# ESPHome [![Discord Chat](https://img.shields.io/discord/429907082951524364.svg)](https://discord.gg/KhAMKrd) [![GitHub release](https://img.shields.io/github/release/esphome/esphome.svg)](https://GitHub.com/esphome/esphome/releases/)

[![ESPHome Logo](https://esphome.io/_images/logo-text.png)](https://esphome.io/)

**Documentation:** https://esphome.io/

For issues, please go to [the issue tracker](https://github.com/esphome/issues/issues).

For feature requests, please see [feature requests](https://github.com/esphome/feature-requests/issues).
