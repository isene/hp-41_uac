# hp-41_uac

## HP-41 ULTIMATE ALARM CLOCK

**NOTE:** This program is part of the ISENE.ROM (https://github.com/isene/hp-41_isene-rom). The FOCAL listing can be found in the "src" folder of that project. Any updates and new version will be found there.

The program that turns your HP-41CX (or 41C/CV with a time module) into
the ultimate alarm clock. It gives your belowed calculator all the
features of a very advanced alarm clock. It even lets you hear the time so
you don't have to turn on the light to see what time it is :)

I have a passion for old Hewlett Packard calculators. I love to program
these little beauties. Now and then I even make a very useful program
such as this one. I have never seen an alarm clock that can do everything
I wanted it to. So, I decided to program my HP-41CX to serve my needs. It
has the features I want:

* Set the alarm to a specific time
* Set the alarm to a certain time from now
* Set the alarm to a preset time from now
* Move the alarm a ½ hour into the future
* Move the alarm anytime into the future
* Hold the alarm clock until you restart it
* When the alarm goes off, stop it by pressing any key
* When the alarm goes off, snooze by ½ hour
* Double-alarm (autosnooze); Alarm goes off, then again 10 minutes later
* Clear the next alarm
* Clear all alarms
* Hear the time!
* Hear when the alarm is supposed to go off!
* Hear how much time left until the alarm goes off!
* Set the alarm for each day throughout the week (daily alarms)
* Stop or restart the daily alarms

More precisely, here is the key mapping:

LABEL  |DESCRIPTION
-------|-----------
ALMS   |Starts the program. Shows some of the mapping for the top keys so that you don't have to remember this list.  Pressing R/S will give you the running clock. Pressing R/S again will give you the alarm catalog, then the version number of the UAC, then it returns to the mapping/menu. It may be useful to assign this function to TAN.
ALM    |Set an alarm. Just enter the time and execute ALM. If the time is greater than the present time, it will set the alarm for that time later today. If the time is less than the present time, it will set the alarm time to that time tomorrow. It may be useful to assign this function to SIN.
ALM+   |Enter the time from now you want the alarm to go off and execute ALM+. It may be useful to assign this function to COS.
LBL A  |Postpone the alarm by ½ hour (both if the alarm is sounding or if it has not yet sounded). If the "wake-up"-type alarms have been cleared (by pressing "C" or "c"), it will set an alarm ½ hour from now.
LBL a  |As above, but postpone the alarm by the amount you enter.
LBL B  |Set the alarm 8:10h into the future (to change this preset time, change line 28 in the program).
LBL b  |Set the alarm 9:00h into the future (alter by changing line 35)
LBL C  |Delete the next "wake-up"-type alarm.
LBL c  |Delete all alarms. Execute WKR (see below) to reactivate the daily alarms.
LBL D  |Hear how long it is until the alarm goes off. Same principle as with SCK (below) - one low beep per 6 hours, then one high beep per hour, then one low beep per quarter. If the alarm has already sounded, it will first give a BEEP, then tell you how long since it went off (same principle).
LBL d  |Hear when the alarm is supposed to go off. Same principle as with LBL D.
SCK (LBL E)   |Hear the time. First it sounds 1-4 low beeps signaling which sector of the day the time is within: 0:00-05:59, 06:00-11:59, 12:00-17:59 or 18:00-23:59. Then 1-6 beeps signaling the number of hours within the sector, then 1-4 beeps signaling which quarter it is within the hour.
LBL e  |"Hold" the alarm until you press R/S to let it continue again.  This makes it possible to wake up in the middel of the night with a brilliant idea that you want to write down. Press "e" to hold the alarm until you are ready to return to bed. Then press R/S (or "e" another time) and you still get your usual hours of beauty sleep.

When the alarm goes off, press any key to stop it. If you then press R/S,
it will snooze for 10 minutes.

Set flag 2 (FS 02) to make the alarm "autosnooze" by automatically sound
again 10 minutes after it first goes off. This is also a useful feature if
you are hard to wake up.

The UAC gives you sound feedback for all the functions. This is done so
that you know if you pressed the right button in the dark.

You may also want the WKA (WeeK Alarm) program as an add-on module to UAC.
The program is made as an add-on because it is not part of the UAC core
functionality and requires X-Functions and X-Memory. It is therefore not
of value to those vith a 41C(V) and a time module.

WKA makes it possible to set specific alarm times for every day throughout
the week. First it will tell you that the week starts with Sunday (SUN) as
day 0. Then it will ask for the alarm time for each day starting with
Sunday. By entering 0, no alarm is set for that day. It may be useful to
assign WKA to TAN-1.

To stop the daily set alarms, execute WKS (Week-alarms Stop). It may be
useful to assign this function to SIN-1.

To restart the daily alarms, execute WKR (Week-alarms Restart). It may be
useful to assign this function to COS-1.
