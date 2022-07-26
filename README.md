# lily58_rgb
Lily58 Pro with the throughhole configuration is a 6×4+5keys column-staggered split keyboard with per-key RGB LEDs. This repository houses my custom firmware for this keyboard, built using [QMK Firmware](https://docs.qmk.fm/#/)

![Lily58 Pro](https://images.squarespace-cdn.com/content/v1/5a8723cb7131a5121206d464/1584642378983-PNC3BHNUNKM2B33GSUAQ/00000IMG_00000_BURST20200317134541768_COVER.jpg?format=1500w)

Supported Hardware: [Lily58 Pro PCB](https://keyhive.xyz/shop/lily58), ProMicro

## Programming on linux
If you're programming on linux, make sure to follow these [setup steps](https://docs.qmk.fm/#/faq_build?id=frequently-asked-build-questions) as well

## Setup
1. Follow [Setup instructions](https://docs.qmk.fm/#/newbs_getting_started) to install QMK
2. Clone this repository
    ```
    git clone https://github.com/maegant/lily58_rgb
    ```
3. Move the contents of this repository to the qmk_firmware/keyboards/ folder (qmk_firmware repository should have been cloned when setting up QMK)
    ```
    cp -r /lily58_rgb/ qmk_firmware/keyboards/
    ```

## Compile Build environment
```
cd qmk_firmware/keyboards/lily58_rgb
qmk compile -kb lily58_rgb/rev2 -km maegan
```
## Flash keyboard:
```
qmk flash
```

## Keymap Configuration
Default Layout
[![Qwerty Layer](docs/lily58_rgb-qwerty-layer.png)](http://www.keyboard-layout-editor.com/#/gists/a59ac6d633875baa2a20605cb5fa9513)

Raised Layer
[![Raised Layer](docs/lily58_rgb-raised-layer.png)](http://www.keyboard-layout-editor.com/#/gists/1370a4ecde109d2cb29393244c1fbdfd)

Lower Layer
[![Lower Layer](docs/lily58_rgb-lower-layer.png)](http://www.keyboard-layout-editor.com/#/gists/1071824fb925814b4f57fe907cdc6941)

Adjust Layer (Activated by holding both raise and lower)
[![Adjust Layer](docs/lily58_rgb-adjust-layer.png)](http://www.keyboard-layout-editor.com/#/gists/eb13aafe78ed8ea6642c3c01bec39397)
___
## Random Bug fixes
If broken dependencies, try running:
```
sudo apt-get install -y avrdude gcc-avr gcc-arm-none-eabi dfu-programmer dfu-util
```

If error with flashing on linux, try the following: (from this [link](https://arduino.stackexchange.com/questions/61359/avrdude-error-butterfly-programmer-uses-avr-write-page-but-does-not-provide))
```
sudo systemctl stop ModemManager.service
sudo systemctl disable ModemManager.service
```