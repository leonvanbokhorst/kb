# Install Sensors on Ubuntu
To display detailed read out from your #sensors on your #ubuntu server, install `lm-sensors`.

```bash
sudo apt install lm-sensors
```

Initially, not all sensors could be detected. Run the following command to detect all sensors. Answer 'yes' to all prompts.

```bash
sudo sensors-detect
```

Reboot the server to load the changes.

```bash
sudo reboot now
```

Run the command `sensors` and it should display something like this:

```terminal
sensors

acpitz-acpi-0
Adapter: ACPI interface
temp1:        +27.8°C  (crit = +105.0°C)
temp2:        +29.8°C  (crit = +105.0°C)

it8790-isa-0a40
Adapter: ISA adapter
in0:          36.00 mV (min =  +0.00 V, max =  +3.06 V)
in1:          24.00 mV (min =  +0.00 V, max =  +3.06 V)
in2:          24.00 mV (min =  +0.00 V, max =  +3.06 V)
+3.3V:         3.70 V  (min =  +0.00 V, max =  +6.12 V)
in4:         804.00 mV (min =  +0.00 V, max =  +3.06 V)
in5:           1.09 V  (min =  +0.00 V, max =  +3.06 V)
in6:           3.06 V  (min =  +0.00 V, max =  +3.06 V) 
3VSB:          3.67 V  (min =  +0.00 V, max =  +6.12 V)
Vbat:          3.38 V
fan1:         595 RPM  (min =    0 RPM)
fan2:           0 RPM  (min =    0 RPM)
fan3:         452 RPM  (min =    0 RPM)
temp1:        +13.0°C  (low  = +127.0°C, high = +127.0°C)  sensor = Intel PECI
temp2:        +26.0°C  (low  = +127.0°C, high = +127.0°C)  sensor = thermistor
temp3:        +29.0°C  (low  = +127.0°C, high = +127.0°C)  sensor = thermistor
intrusion0:  ALARM

coretemp-isa-0000
Adapter: ISA adapter
Package id 0:  +22.0°C  (high = +80.0°C, crit = +100.0°C)
Core 0:        +20.0°C  (high = +80.0°C, crit = +100.0°C)
Core 1:        +20.0°C  (high = +80.0°C, crit = +100.0°C)
Core 2:        +22.0°C  (high = +80.0°C, crit = +100.0°C)
Core 3:        +16.0°C  (high = +80.0°C, crit = +100.0°C)
```
