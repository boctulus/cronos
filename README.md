# cronos

Schedule a task or create an alarm

Features:

* Alarm
* Programmed tasks
* Easy to sue


Usage:

	 cronos <time> <options> [-t] <text> 
	 cronos <time> <options> -c <command> 
	 cronos <time> <options> -f <script file> 
     
	Options:
	 -v, --verbose                  show detailed information
	 -m, --mute                     no sound (not implemented)
	 
	 -t, --text                     text for alarm
	 -c, --command                  command to be executed
	 -f, --file                     script file
	 -s, --script                   same as -f
	 
	 -l, --list                     list all tasks / alarms
	 -r, --remove                   remove an specific task or alarm 
	 -a, --all                      remove all tasks / alarms
	 
	 -h, --help                     display this help
	 -V, --version                  display version
    
	 Time format is HH:MM with 24 HS and AM / PM support 
	 

Examples:

    cronos 23:00 Dragon Ball
    cronos  6:00 PM buy something
    cronos 23:45 -f some_script.sh 
    cronos 10:30 -c some_command
    cronos 12:15 -c 'command1 && command2'
    cronos 12:15 -c 'command > output.txt'


How to install

	git clone https://github.com/boctulus/cronos.git
	cd cronos
	chmod +x cronos*
	sudo ln -s $(pwd)/cronos /usr/bin		


How it works

- Cronos is programmed for a moment in the future 'tf'

- Cronos is activated in (tf-tm_ant) with tm_ant = 5 [min] by default.

- Cronos can be triggered after (tf-tm_ant) if the system was in suspension or hibernation at that time but at most in tmax = tf + tm_dsp being tm_dsp = 10 [min] by default.

- The user can postpone the alarm for tm_rep = 5 [min]

- Alarm notification is dismissed after tm_dismiss = 60 [min] 