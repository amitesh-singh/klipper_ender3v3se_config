# Notes

## Z offset

### PLA
### Stock build plate - ender 3v3 se

z-offset = 2.344

### PETG CF

#### Stock build plate - ender 3v3 se
z-offset = 2.344 - 0.150 = 2.194

#### PEI/PEO build plate - ender 3v3 se

z-offset = 2.334

## Bed mesh

### Stock build plate - ender 3v3 se

```
#*# [bed_mesh stock-build-plate]
#*# version = 1
#*# points =
#*# 	0.043333, 0.060833, 0.055000, 0.082500, 0.125000, 0.134167
#*# 	-0.013333, -0.015833, 0.001667, 0.006667, 0.049167, 0.057500
#*# 	-0.019167, -0.020833, 0.032500, 0.017500, 0.046667, 0.05833
#*# 	-0.022500, -0.005000, 0.018333, 0.026667, 0.048333, 0.061667
#*# 	0.004167, 0.020000, 0.037500, 0.057500, 0.067500, 0.110000
#*# 	0.082500, 0.085833, 0.099167, 0.126667, 0.137500, 0.130000

```

## input shaping
- command:

```
TEST_RESONANCES AXIS=X FREQ_START=5 FREQ_END=120 OUTPUT=raw_data

```
```
ami@octoprint:/tmp $ ~/klipper/scripts/calibrate_shaper.py /tmp/raw_data_x_20251029_234400.csv -o /tmp/shaper_calibrate_x.png

Fitted shaper 'zv' frequency = 52.4 Hz (vibrations = 2.2%, smoothing ~= 0.062)
To avoid too much smoothing with 'zv', suggested max_accel <= 10700 mm/sec^2
Fitted shaper 'mzv' frequency = 53.0 Hz (vibrations = 0.0%, smoothing ~= 0.073)
To avoid too much smoothing with 'mzv', suggested max_accel <= 8300 mm/sec^2
Fitted shaper 'ei' frequency = 63.6 Hz (vibrations = 0.0%, smoothing ~= 0.080)
To avoid too much smoothing with 'ei', suggested max_accel <= 7500 mm/sec^2
Fitted shaper '2hump_ei' frequency = 79.2 Hz (vibrations = 0.0%, smoothing ~= 0.086)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 7000 mm/sec^2
Fitted shaper '3hump_ei' frequency = 95.0 Hz (vibrations = 0.0%, smoothing ~= 0.091)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 6600 mm/sec^2
Recommended shaper is mzv @ 53.0 Hz
```

