# rpi3bp-pico-openocd-swd

$ sudo nano /usr/local/share/openocd/scripts/interface/raspberrypi-swd.cfg 

#change 25 to 21 and 24 to 20

#ctl-o to save

#ctl-x to exit

#to test

$ openocd -f interface/raspberrypi-swd.cfg -f target/rp2040.cfg -c "program blink/blink.elf verify reset exit"
