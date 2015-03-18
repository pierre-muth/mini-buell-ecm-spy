# Introduction #

I will start with a bit of history of work done.
After 2 years of joyful riding with [my Buell XB12S](http://muth.inc.free.fr/buell/IMG_1399.jpg), I was a bit disappointed to not have the information of the engine temperature. Mainly to know when I can use the full possibilities of the great air-cooled Vtwin engine.
I used the [ECMspy](http://ecmspy.com/) software to calibrate the position of the throttle. With this software, all the information form the ECM is available by the diagnostic plug.

Why cannot have information directly on the instrument module? ECM diagnostic plug use a RS232 protocol at TTL levels. Everything was discovered and describe by the ECMspy team on their website.

ECM can send back a bunch of hundred live data by send to it a request sentence.

[Com info](http://www.ecmspy.com/eeprom_info.shtml)

[Live data info](http://www.ecmspy.com/cgi-bin/runtime.cgi)

# First approach: PIC uController #

I started to try establish communication with the bike's ECM with a microchip PIC micro-controller. Successfully, with a 16F877A.

[Fist success with a small screen](http://muth.inc.free.fr/buell/miniECMspy/IMG_3519.jpg)

<a href='http://www.youtube.com/watch?feature=player_embedded&v=itP6DIz1b5I' target='_blank'><img src='http://img.youtube.com/vi/itP6DIz1b5I/0.jpg' width='425' height=344 /></a>

[And there the source of the PIC](http://muth.inc.free.fr/buell/miniECMspy/Buell-rs232.asm)

# Second approach: intelligent screen #

Project with a uController imply develop a board enough small to fit inside the instrument module. I searching prototyping board, I found the product of 4Dsystems.

Tiny screens integrate a uController, capability of serial communication, exactly my needs !
[4D systems](http://www.4dsystems.com.au/index.php)

And it's work ! [There my fist tests](http://muth.inc.free.fr/buell/miniECMspy/IMG_3685.jpg), engine temperature and AFV value, with an history chart of around 30 minutes.
AFV is for Adaptive Fuel Value, that influence the air/fuel ratio by analyzing the O2 probe behavior.

I use the 12v of the instrument board, a voltage regulator to obtain the 5v supply :
[A bit of integration](http://muth.inc.free.fr/buell/miniECMspy/IMG_4437.jpg) [in the small space available](http://muth.inc.free.fr/buell/miniECMspy/IMG_4436.jpg). After some debug, it's work fine [with the bike's ECM](http://muth.inc.free.fr/buell/miniECMspy/IMG_4434.jpg).

I decide to put more information, by switching between different page on the screen. I use the [existing button use normally to reset the counter](http://muth.inc.free.fr/buell/miniECMspy/IMG_4540.jpg), possible because the effect for normal use is only after 3 seconds pressed:

<a href='http://www.youtube.com/watch?feature=player_embedded&v=MqplGkaLw5A' target='_blank'><img src='http://img.youtube.com/vi/MqplGkaLw5A/0.jpg' width='425' height=344 /></a>

There the [on road test](http://muth.inc.free.fr/buell/miniECMspy/IMG_4543.jpg), and the [two](http://muth.inc.free.fr/buell/miniECMspy/IMG_4544.jpg) [screens](http://muth.inc.free.fr/buell/miniECMspy/IMG_4546.jpg).

I still have work, especially to handle with the two version of ECM.

I want to thank a lot all the team of ECMspy and people motivate me on the [French Buell forum](http://buell.actifforum.com/buell-personnalisee-f5/mini-ecm-spy-embarque-projet-t18165.htm)