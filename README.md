# shalarm

Alarm in Bash with GTK interface

Features:

* Snooze alarm
* Easy to use


Usage:

	Schedule a task or create an alarm

	Options:
	 -v, --verbose                  show detailed information
	 -m, --mute                     no sound (not implemented)
	 
	 -t, --text                     text for alarm
	 -c, --command                  command to be executed
	 -f, --file                     script file
	 -s, --script                   same as -f
	 
	 -h, --help                     display this help
	 -V, --version                  display version

Examples:

    nohup alarm 23:00 Dragon Ball &
    nohup alarm 10:30 -c command &
    nohup alarm 10:30 -f some_script.sh &


How it works

- The alarm is programmed for a moment in the future 'tf'

- The alarm is activated in (tf-tm_ant) with tm_ant = 5 [min] by default

- The alarm can be triggered after (tf-tm_ant) if the system was in suspension or hibernation at that time but at most in tmax = tf + tm_dsp being tm_dsp = 10 [min] by default

- The user can postpone the alarm for tm_rep = 5 [min] minutes (default)

- Alarm notification is dismissed aftter tm_dismiss