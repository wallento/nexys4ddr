= Seven Segment Display Controller

This is a controller module for the seven segment display. It is used
to set the display digits and decimal points.

Parameters:

- `FREQ`: Clock frequency
- `REFRESH`: Refresh rate in Hz. Should be > 25, but not too high

Ports:

- `clk`, `rst`: clock and reset
- `digits [55:0]`: Digits to display
- `decpoints [7:0]`: Decimal points
- `CA`-`CG`, `DP`, `AN[7:0]`: Board pins

`digits` is a flat port for the eight display positions, each has
seven bits, which map to the seven segments as:

    +-0-+
    5   1
	+-6-+
	4   2
	+-3-+

