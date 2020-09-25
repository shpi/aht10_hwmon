# aht_hwmon
AHT10 kernel hwmon driver, i2c address 0x38

guide for Raspberry Pi

## prerequisites
```bash
sudo apt-get install dkms git
```

## clone repository

```bash
git clone https://github.com/shpi/aht10_hwmon
```

## install
```bash
cd aht10_hwmon
   sudo ln -s /home/pi/aht10_hwmon /usr/src/aht10-1.0
   sudo dkms install aht10/1.0 
   sudo dtc -I dts -O dtb -o /boot/overlays/aht10.dtbo aht10.dts
   ```
   

## /boot/config.txt

add

```bash
dtoverlay=aht10
```

