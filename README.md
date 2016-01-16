# Goal
The goal of this project is to create four illuminated disc that have pressure sensors. When stepped on they will interact with each other to play the game simon. Each of the disc will be controlled individually by an esp8266 wifi micro controller. Additionally, any smart device (phone, tablet, PC, ...) can also interact and play along from within a web browser.
# Design
Software:

The Arduino IDE port for the ESP8266 is being used for the firmware development. A "master" disc will manage the LED lights, wifi access point, DNS captive portal, HTTP server, websocket server, and the simon game play logic. Each of the other three "slave" disc will handle the LED lights, wifi/websocket connection to the master, and sending messages to the master when the disc is stepped on. The HTTP server on the master disc provides smart devices a web based interface to observe or interact with the game play.

Hardware:

The disc will be constructed from a Frisbee with the electronics mounted inside of it using clear silicon to fill in the voids and hold it in place. In addition to the esp8266 the electronics will also include a pressure pad for user input and a number of ws2812b digital RGB LEDs for the illumination.
# Why?
As micro controllers become smaller and cheaper they will no dought find their way into basically everything. The ioT (internet of things) concept is spreading like wild fire ... just do a search for "Belkin WeMo" on the internet an see what is already on the market. While this project could be expanded to include full internet access, at this time it is limited to just a standalone toy. The idea is to demonstrate how many small devices (parts), that handle limited functions, can be joined together to create a larger more complex device. For example a wifi wall switch and a wifi wall outlet can be joined together to create a wifi controlled wall switch (fly by wire) where no actual high voltage connects between the switch and the outlet. Additionally, we have the added ability to use other digital devices such as smart phones, tablets, or PCs to also interact with the device(s). 

So the answer to "Why?" is "Why Not" Hence ... "many small simple parts joined together (via wifi) to create a more complex and larger part."
