# rpi3bp-pico-openocd-swd

$ sudo nano /usr/local/share/openocd/scripts/interface/raspberrypi-swd.cfg 

#Problem statement : GPIO 25 and GPIO 24, the openocd-swd defaults, are already being used by my sense-hat board.

#change 25 to 21 and 24 to 20

#ctl-o to save

#ctl-x to exit

#move SWD wires to GPIO 21, and GPIO 20, respectively.  Then to test issue the following command from /home/pi/pico/pico-examples/build directory:

$ openocd -f interface/raspberrypi-swd.cfg -f target/rp2040.cfg -c "program blink/blink.elf verify reset exit"
