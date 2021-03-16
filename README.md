# My private ESPHome configuration

This project uses [ESPHome](https://esphome.io).

Each file should start with

```yaml
substitutions:
  devicename: mydevice
  devicename_upper: MyDevice

<<: !include ./.base.yaml
```

Replace `devicename` and `devicename_upper` with the desired values.

> *ATTENTION* You will also need to create a file named `secrets.yaml` in the base folder with the following content:

```yaml
wifi_ssid: YourSSID
wifi_password: "The password for your wifi"
```

The content of this file is used in `wifi.yaml`.

## Usage

```bash
## Compile with:
esphome compile ${FILE}

## e.g.
esphome compile drawer.yaml
esphome compile rack.yaml

## Then upload to device:
esphome upload ${FILE}
```

