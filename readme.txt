Comments about COMTALK

Comtalk is a PM communications program.  It is broken up into five modules:

AVIO		This module controls AVIO interactions.  In this routine,
		the window size and scrollbars are controlled.

CIRCLEQ		This module controls the circular queue buffer with which
		the AVIO module updates the screen.

COMPORT		This module controls reading and writing characters from
		the communications port (makes DosDevIOCtl calls, etc...)

COMTALK		This module contains the main window procedure, and processes
		user input

THREADS		This module contains 3 secondary threads, which write characters
		to the COM port, read from the COM port, and one which takes
		characters read from the COM port and pushes them into the
		circular line buffer queue.

Possible improvements to this program include:  File transfer capabilities,
terminal emulation, small fonts (AVIO).


Directory Contents:
AVIO.C		AVIO module source routines
AVIO.H		AVIO module prototypes
CIRCLEQ.C	Circular queue module source
CIRCLEQ.H	Circular queue prototypes
COMPORT.C 	COM port interface
COMPORT.H	COM port interface prototypes
COMTALK		Makefile
COMTALK.C	Core routines
COMTALK.DEF	Definition file
COMTALK.EXE	Executable
COMTALK.H	Resource Identifiers
COMTALK.ICO	Icon
COMTALK.RC	Resources
COMTALK.SYM	Symbol file
GLOBAL.H	Definitions common to all modules
THREADS.C	Secondary threads module
THREADS.H	Secondary thread module prototypes
