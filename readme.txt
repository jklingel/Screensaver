Title: Screensaver

Author: Jan Klingel <jan.a.klingel AT t-online.de>
Date: 27.09.2022
Version: 1.0
Language: Commodore/Microsoft BASIC V2

Description: This is a simple screensaver to try out and play around with, which should give you a warm old school computer feeling while you are not busy working at the computer.

Usage: Just run the program, there are no parameters; no keyboard input other than an interrupt is taken.

Function: In text mode, the computer prints a character into a random cell on the screen. From there the computer moves randomly to the next free cell. If there are no free cells anymore, the program starts all over again.

Variables: 
	DE(bug)	- Toggles debug mode:
			0 switches debug mode off
			1 switches debug mode on
	S	- Start address of screen memory (1024 for a C64)
	CH(r)	- Character to print to the screen
	V	- Array for each cell visited. A visited cell is set to 1
	LO(c)	- Location of the pointer on screen (from 0 to 1000, 1000 not being used)
	CO(unt)	- Counter for printed characters on screen
	DI(r)	- Direction the random function wants to move:
			1=up
			2=down
			3=left
			4=right
	DP	- Used for printing formatted debug counters
	DP$	- Used for printing formatted debug counters
	MO(ve)  - An array for detecting blocked moves. The array follows DI(r) for order of direction
			0=move was possible
			1=move was not possible

To-do: No protection against manually switching character sets while program is running.

Missing: An optimized (self-learning?) algorithm that keeps a single run alive as long as possible. 
