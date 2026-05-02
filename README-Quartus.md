# Typical Workflow

## Editing

Use you favourite text editor to edit the project. Always take a back up, because recovery is hard.

## Compiling


+ Start Quartus II 64 bit
+ File - Open UK101\UK101.vhdl
+ Tasks - flow - compilation
+ Click on the grey triangle icon (start a new complilation)
+ This takes around 3 minutes on an old laptop
+ Check for errors in the log
+ Check for the output files in UK101\Output files

## Temporary Programming

For Temporary testing, use the JTAG port to programme the FPGA (which will reset on power off)
First power up the board. If the board is vanilla, LEDs will flash.
Connect the USB Blaster to the computer, and then to the board.
Click the Programmer icon to open a new (programmer) window.
Click Hardware setup.
Select the USB Blaster [USB-0] (see ntoe below on drivers if it doesn't appear)
Select JTAG mode
Click autodetect. You should see the EP2C5T144 FPGA. If you don't, debug JTAG
Right click the chip icon or the line showing the device name
add File UK101\Output Files\UK101.sof
Start
Progress will show 100% successful.

Powering down the board loses the programme. This is normal.


## Permanent Programming

For permanent programming, use the "AS" port to programme the EEPROM, which then loads the code into the FPGA at power up.

First power up the board.
Connect the USB Blaster to the computer, and then to the board's JTAG port.
Click the Programmer icon to open a new (programmer) window.
Click Hardware setup.
Select the USB Blaster [USB-0] (see note below on drivers if it doesn't appear)
Select Active Serial Programming mode
Click autodetect or add file. You should see the EPC54 EEPROM. If you don't, debug the USB.
Right click the chip icon or the line showing the device name
add File UK101\Output Files\UK101.pof
Select Program/configure
Start

Programming only takes a few (5-10) seconds and is verified by "100% (successful)" in the progress window.


## Hints

+ There is NO ARM version of Quartus. So even within a VM the Linux version can't be used on a MacBook with Apple Silicon (expect by using emulation)
+ When inserting the USB Blaster under Windows 10, the driver doesn't always install properly.
+ Start Device Manager, go to "Altera USB Blaser", right mouse, update driver, browse this computer, choose the disk where Quartus is installed.
+ Neither the JTAG interface, nor the AS port, supply power to the board. You need separate USB A to 5,5mm/2,1mm barrel plug.