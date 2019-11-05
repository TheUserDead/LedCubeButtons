# LedCubeButtons
### 4x4x4 Led cube with effects and changeable manually using 2 buttons

 Based on http://arduino-diy.com/arduino-svetodiodnyy-kub-4x4x4 sketch

---Notes---
+ This sketch uses last two pins (A6, A7) As input for detect keypress. Not all arduinos has A6, A7 pins free, and this pins is INPUT only.
+ It is recommended using sensor buttons like TTP223 for avoid contact boucing effect.
+ I think it is not possible using interrupt cause all digital pins are busy.
+ For keypress detection it's recommended using analogRead function instead of Digital read. It's reliability because yield of the touch button has a TTL logic.
+ Random flicker effect has random delay time every call.
+ Automode based on increase currentMode[0] in the end every entering in loop() func. If automode == 0, it's just not increase number.
+ currentMode[0] just for current mode, and currentMode[1] just for detect change when buttons poolled
+ It's my first repository, yay!

I know, using button pooling inside effects functions is bad. But, it works))

After power on, device running auto mode. If you press any button < or > device stay in this effect.

For return in auto mode you can press < and > buttons for 1-2 sec and release, you will see the descending column inside the cube, he says the inclusion of the automatic mode.
That's all folks!

ToDo List:
-More effects?
