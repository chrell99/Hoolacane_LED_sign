A personalized version of the "rpi-rgb-led-matrix" library made by "Hzeller"
============================================================================

The purpose of this project is to utilize the existing library and slighty modify it,
to fit the needs for the project "Hoolacane LED sign". The original README.md can be
found in the original repository, while this repository's README will only focus on the
parts necessary for the project in question.

Getting started
---------------
This project will utilize a raspberry pi 3 B+ running raspberry pi OS lite for the controls,
a "RGB LED matrix panel drive board" from [Electrodragon](https://www.electrodragon.com/product/rgb-matrix-panel-drive-board-raspberry-pi/)
to interface with the LED panels, two [BTF-Lighting](https://www.amazon.de/-/en/dp/B085C2N571?ref=ppx_yo2ov_dt_b_product_details&th=1)
5V 40A power supplies, and 9 [LysonLED](https://www.aliexpress.com/item/32382200566.html) LED panels.

Firstly clone the git repository to the raspberry Pi, and afterwards run the following command in
the top folder.
```
sudo make -C examples-api-use
```
Once done you can run one of the examples, but some configuration is necessary. The modules from
LysonLED need the following parameters set to function properly:
Flag                    | Description
:---------------        | :-----------------
`--led-slowdown-gpio=2` | Columns in the LED matrix, the 'width'.
`--led-multiplexing=1`  | Rows in the LED matrix, the 'height'.

```
--led-slowdown-gpio=2 --led-multiplexing=1 
```
