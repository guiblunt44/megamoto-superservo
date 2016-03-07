Interface RC receiver to Arduino to read Radio Control stick position. Use MegaMoto shield  to position the motor using a PID algorithm.  The result:  a super servo

Here are some videos:

Introduction:       http://www.youtube.com/watch?v=BP8cc5heaAw <br>
Code walk-through:  <a href='http://www.youtube.com/watch?v=T3PiexN17FY'>http://www.youtube.com/watch?v=T3PiexN17FY</a> <br>
Wiring it up:       <a href='http://www.youtube.com/watch?v=PGSim_eTokU'>http://www.youtube.com/watch?v=PGSim_eTokU</a> <br>

Be careful!  Use the serial out to check things first with the battery inputs to the MegaMoto disconnected.  There is an increased chance of damage to the MegaMoto in an application like this with large motors because of the potential for jerky commands and sudden direction changes.  The linear actuator in my videos is only pulling around 3amps and the MegaMoto is driven well within the MegaMoto's capabilities. The very large motor in the "wiring it up" video will pull 10 or more amps and a sudden kick or reverse direction is going to test the limits of the MegaMoto.<br>
<br>
TIP:  reduce dutyMax when using large motors. Change this line of code:   int dutyMax = 254;