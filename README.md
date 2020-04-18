# Sunhokey Prusa i4

[Sunhockey Prusa i4](images/3dprinter.png)

## Original Setup

Hardware: MKS base 1.4

Arduino MEGA compatible Atmega2560 + RAMPS 1.4

Original Software: Marlin modified by Sunhockey for Prusa i4

## Updating Marlin Firmware

1. Prepare source code
```
git clone https://github.com/LucFabresse/sunhokey-prusa-i4.git
git clone https://github.com/MarlinFirmware/Marlin.git
cd Marlin
git checkout 2.0.x
```
2. Apply specific configuration for Sunhockey Prusa i4
```
cp -f ../sunhokey-prusa-i4/Marlin/* Marlin/
```
To setup these configuration files, I compared with those one:
- http://aeinc.ru/i4/
- https://github.com/webhive/sunhokey-prusa-i4

Note: review the configuration and update it according to your printer (e.g. I do not have a BLTouch)
3. Compile and Flash using platformio (cf. [doc](https://marlinfw.org/docs/basics/install_platformio_vscode.html))

Now, my i4 uses the latest Marlin 2.0 !
(commit hash: 0518dec60d0931745efa2812fa388f33d68cfa29)

## Useful Links

- https://github.com/alecthegeek/sunhokeyI4/wiki
