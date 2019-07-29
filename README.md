# shalarm

Alarm in Bash with GTK interface

Features:

* Snooze alarm
* Easy to use

Example:

    nohup alarm 23:00 Dragon Ball &
 

How it works

- The alarm is programmed for a moment in the future 'tf'

- The alarm is activated in (tf-tm_ant) with tm_ant = 5 [min] by default

- The alarm can be triggered after (tf-tm_ant) if the system was in suspension or hibernation at that time but at most in tmax = tf + tm_dsp being tm_dsp = 10 [min] by default

- The user can postpone the alarm for tm_rep = 5 [min] minutes (default)

- Alarm notification is dismissed aftter tm_dismiss