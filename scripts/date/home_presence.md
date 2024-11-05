binary_sensor:
  - platform: template
    sensors:
      your_mobile_home:
        value_template: >-
          {% if (states('sensor.your_phone_wifi_connection') == "your_wifi_name1") or ((states('sensor.your_phone_wifi_connection') == "your_wifi_name2")) %}
            on
          {% else %}
            off
          {% endif %}
  - platform: template
    sensors:
      your_gps_home:
        value_template: >-
          {% if states('device_tracker.your_phone') == "home" %}
            on
          {% else %}
            off
          {% endif %}
