# BUS
ECE387_classActivity

Estimations for design a 3x3 LED dance floor

Topography: 
As mentioned in class, use 'S' shaped circuit for 3x3 dance floor(divided into 9 blocks, with 9 LEDs per block). Each block will connect to shift registers and logic gate. These blocks are in series, so signal always has to go from 1st block to 2nd block to 3rd block .. to 9th to ground. For loop in code, it should generate the command to blocks from the last block to first block to asure the synchronization.

Protocol:
Use SPI(high date rate, can send and receive at the same time and synchronization). Use 8-bit shift register to assign on/off for each led. 4-bit shift register for color for RGB led. Logic gates are used for generally divide the signal into 9 parts and 1 for each block. 

Time:
9 blocks * 9 LEDs per block * 3bit/ 115200bps(fastest data transfer rate of arduino board) = 0.0021s = 2.1ms. This is fast enough.(1/0.0021 = 476fps, which is much faster than human eye(24fps) and gaming monitor(144fps)).

Total Cost:
Arduino board ($10~$20) , 9X 8-bit shift registers(74HC595, $0.95 each) , 9X 4-bit shift registers (74S194, $0.39 each) , LEDs + logic gates + wires + others ($20) -- Total = $42.06 ~ $52.06.

