# piSolarloglcdweatherstation
A little raspbery pi project to scrape information from the solar log local webpage.
The result are transferred to a 16X2 LCD display connected to the pi.

Solar log http server listens at 10.0.0.20;80/tcp.
All files must be installed under /usr/local/bin and the following string must be added to /etc/rc.local to start the script after each reboot

/usr/local/bin/lcd_solarlog.py 1>/tmp/solarlogrc 2>/tmp/solarlog2rc

### Lcd connection

- LCD Pin 1: to Raspberry pi ground
- LCD Pin 2: to Raspberry pi +5v 
- LCD Pin 3: this is the contrast, connect to the middle pin of a 10K potentiometer or trimmer, one side of the trimmer must be connected to raspberry pi 5v, the other to raspberry pi ground.
- Lcd Pin 4 is register select: connect to GPIO25 (pin 22)
- Lcd Pin 5 is Read Write and must be grounded: connect to any Raspberry pi ground pin
- Lcd pin 6 is the Enable pin and must be connected to GPIO 24 (pin 18)
- Lcd pin 7 : leave disconnected
- Lcd pin 8 : leave disconnected
- Lcd pin 9 : leave disconnected
- Lcd pin 10 : leave disconnected
- Lcd pin 11 : connect to GPIO 23 (pin 16)
- Lcd pin 12 : connect to GPIO 22 (pin 15)
- Lcd pin 13 : connect to GPIO 17 (pin 11)
- Lcd pin 14 : connect to GPIO 11 (pin 23)
- LCD Pin 15 (LCD anode): this is the lcd backlight, connect to the middle pin of a 10K potentiometer or trimmer, one side of the trimmer must be connected to raspberry pi 5v, the other to raspberry pi ground.
- LCD Pin 16 (lcd cadode): to Raspberry pi ground

Reference : https://www.youtube.com/watch?v=cVdSc8VYVBM and https://www.rototron.info/lcd-display-tutorial-for-raspberry-pi/
