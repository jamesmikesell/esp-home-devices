# Initial Device Setup
Create a `secrets.yaml` with the following
```yaml
wifi_ssid: "Your Wifi Network Name Here"
wifi_password: "the password"
```

Use the <https://web.esphome.io/> web installer to inialzie a device.

Then modify the following in a config yml 
```yaml
wifi:
  use_address: device-name-from-initial-config.local
```

Use the following to compile and push changes to the device:
```shell
docker run --rm -v "${PWD}":/config --network=host -it esphome/esphome run esp-device-file.yaml
```



