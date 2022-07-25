# lily58-rgb
Lily58 Pro is 6×4+5keys column-staggered split keyboard with per-key RGB LEDs. This repository houses my custom firmware for this keyboard, built using [QMK Firmware](https://docs.qmk.fm/#/)

![Lily58 Pro](https://images.squarespace-cdn.com/content/v1/5a8723cb7131a5121206d464/1584642378983-PNC3BHNUNKM2B33GSUAQ/00000IMG_00000_BURST20200317134541768_COVER.jpg?format=1500w)

Supported Hardware: [Lily58 Pro PCB](https://keyhive.xyz/shop/lily58), ProMicro

## Programming on linux
If you're programming on linux, make sure to follow these [setup steps](https://docs.qmk.fm/#/faq_build?id=frequently-asked-build-questions) as well

## Setup
1. Follow [Setup instructions](https://docs.qmk.fm/#/newbs_getting_started) to install QMK
2. Clone this repository
```

```
3. Move the contents of this repository to the qmk_firmware/keyboards/lily58 folder
```
cp -r /lily58-rgb/ qmk_firmware/keyboards/
```

## Compile Build environment
```
cd qmk_firmware/keyboards/lily58_rgb
qmk compile -kb lily58_rgb/rev2 -km maegan
```

## Bug fix
If broken dependencies, try running:
```
sudo apt-get install -y avrdude gcc-avr gcc-arm-none-eabi dfu-programmer dfu-util
```