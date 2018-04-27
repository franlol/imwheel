# imwheel

/etc/X11/imwheel/imwheelrc



# IMWheel Configuration file ($HOME/.imwheelrc or /etc/imwheelrc)
# (GPL)Jon Atkins <jcatki@jonatkins.org>
# Please read the README and/or imwheel(1) manpage for info
# and this is best operated on using vim (as I said: It's crunchy)

".*"
None,      Up,   Button4, 3
None,      Down, Button5, 3
Control_L, Up,   Control_L|Button4
Control_L, Down, Control_L|Button5
Shift_L,   Up,   Shift_L|Button4
Shift_L,   Down, Shift_L|Button5

# This is only for demonstration of the priority command...
# See the other global Exclude command below for the one you want to use!
# If this is activated it will only apps that have a lower priority
# priority is based first on the priority command, then the position in this
# file - the higher the line is in a file the higher in a priority class it is
# thus for a default priority you can see that the position in the file is
# important, but the priority command CAN appear anywahere in a window's list
# of translations, and the priority will be assigned to all translations below
# it until either a new window is defined or the priority is set again.
#
#".*"
#@Priority=-1000 #the default priority is zero, higher numbers take precedence
#@Exclude
#@Repeat

# want it to type something?
# this would type "Rofl" and press Return in any window
#".*"
#,Up,Shift_L|R|-R|-Shift_L|O|-O|F|-F|L|-L|Return



# This one rule can send button events, as if you used ZAxisMapping "4 5"
# Make sure your XF86Config allows for the max buttons needed...
# otherwise the events will NOT even be generated...
#".*"
#, Up, Button4
#, Down, Button5
#, Left, Button6
#, Right, Button7
#, Thumb1, Button6
#, Thumb2, Button7
# alternatively with Button numbers
#".*"
#, Button4, Button4
#, Button5, Button5
#, Button6, Button6
#, Button7, Button7
#, Button6, Button6
#, Button7, Button7

#Thanks to Mathias Weyland <mathias@weyland-wtal.de>
"^mutt.*"
None,           Up,     Up
None,           Down,   Down
Control_L,      Up,     Page_Up
Control_L,      Down,   Page_Down

#Thanks to Mathias Weyland <mathias@weyland-wtal.de>
"^aterm"
None,           Up,     Shift_L|Page_Up
None,           Down,   Shift_L|Page_Down
Control_L,      Up,     Up
Control_L,      Down,   Down

#Thanks to Mathias Weyland <mathias@weyland-wtal.de>
"^Xplns"
None,           Up,     Left
None,           Down,   Right
Control_L,      Up,     Up
Control_L,      Down,   Down

"^kvt"
None,		Up,		Shift_L|Page_Up
None,		Down,	Shift_L|Page_Down

"^Konsole"
None,		Up,		Shift_L|Page_Up
None,		Down,	Shift_L|Page_Down

"^XMcd"
None,		Up,		C
None,		Down,	Shift_L|C

"^XMMS_Player"
Shift_L,		Up,		Right
Shift_L,		Down,	Left

"^XMMS_Playlist"
Shift_L,	Up,		Page_Up
Shift_L,	Down,	Page_Down

"^xmms"
Alt_L,		Up,		Z
Alt_L,		Down,	B
Control_L,	Up,		V
Control_L,	Down,	C

"^XATITV-GATOS"
None,       Down,	KP_Subtract
None,       Up,		KP_Add

"^Xman"
None,		Down,	F
Shift_L,	Down,	3
None,		Up,		B

"^Gvi(m|ew)"
Alt_L,	Up,		Page_Up
Alt_L,	Down,	Page_Down
Shift_L,	Up,		Control_L|Y
Shift_L,	Down,	Control_L|E
#None,		Up,		Page_Up
#None,		Down,	Page_Down
#,	Up,	Button4
#,	Down,	Button5
,	Left,	Shift_L|Left
,	Right,	Shift_L|Right
,	Thumb1,	Shift_L|Left
,	Thumb2,	Shift_L|Right

"^VIM"
Shift_L,	Up,		Control_L|Y
Shift_L,	Down,	Control_L|E
#None,		Up,		Page_Up
#None,		Down,	Page_Down

"^Eterm"
Alt_L,		Up,		Up
Alt_L,		Down,	Down
#Alt_L,   	Up,     Shift_L|Page_Up
#Alt_L,   	Down,   Shift_L|Page_Down

#"^GnomeTerminal"
#@Exclude
#@Repeat
#None,		Up,		Shift_L|Page_Up
#None,		Down,	Shift_L|Page_Down

"^NXTerm"
None,   	Up,     Shift_L|Page_Up
None,   	Down,   Shift_L|Page_Down

"^rxvt"
Alt_L,  	Up,		Shift_L|Page_Up
Alt_L,  	Down,	Shift_L|Page_Down

"^XTerm"
Alt_L,		Up,		Shift_R|Page_Up
Alt_L,		Down,	Shift_R|Page_Down
Alt_L,		Left,	Control_L|A
Alt_L,		Right,	Control_L|E
#Shift_L,	Down,	Shift_L|1

"^VMware"
@Exclude
#@Repeat

"^Mozilla-bin$"
#,	Up,	Button4
#,	Down,	Button5
#,	Left,	Alt_L|Left
#,	Right,	Alt_L|Right
#
# If you want to scroll by a few lines then uncomment these 4 lines
# and comment out the paging 4 lines below these!
#
Shift_L,	Down,	Page_Down,			1#,	1000,	1000
Shift_L,	Up,		Page_Up,			1#,	1000,	1000
#None,		Down,	Down,				7#,	1000,	1000
#None,		Up,		Up,					7#,	1000,	1000
#
# If you don't like page scrolling then comment these out and uncomment above!
#
#Shift_L,	Down,	Down,				7,
#Shift_L,	Up,		Up,					7,
#None,		Down,	Page_Down,			1,
#None,		Up,		Page_Up,			1,
# Left/Right & Thumb stuff
None,		Left,	Left,				7,
None,		Right,	Right,				7,
None,		Thumb1,	Down,				7,
Shift_L,	Thumb1,	Up,					7,
None,		Thumb2,	Up,					7,
Shift_L,	Thumb2,	Down,				7,

"^Freespace.*"
,	Up,		Y
,	Down,	X
,	Thumb1,	H
,	Thumb2,	R

"^SDL_App"
#,	Up,		Button4
#,	Down,	Button5
,	Thumb1,	Home	#many apps don't understand Button > 5
,	Thumb2, End		#many apps don't understand Button > 5

# Thanks to shewp <shewplx@pblx.net>
"^Opera" 
#@Repeat    # let qt do it
None,       Down,   Down,               4,  100,    100
None,       Up,     Up,                 4,  100,    100
None,       Thumb1, Right
None,       Thumb2, Left

"^Netscape.*"
, Thumb1, Alt_L|KP_Left
, Thumb2, Alt_L|KP_Right
#, Up, Button4
#, Down, Button5

"^Netscape"
#
# If you don't want to scroll by a few lines then comment out these 4 lines
# and uncomment the paging 4 lines below these!
#
Shift_L,	Down,	Page_Down,			1,	1000,	1000
Shift_L,	Up,		Page_Up,			1,	1000,	1000
None,		Down,	Down,				7,	1000,	1000
None,		Up,		Up,					7,	1000,	1000
#
# If you don't like page scrolling then uncomment these
# and comment out the 4 lines above!
#
#Shift_L,	Down,	Shift_L|Down,		7,	1000,	1000
#Shift_L,	Up,		Shift_L|Up,			7,	1000,	1000
#None,		Down,	Page_Down,			1,	1000,	1000
#None,		Up,		Page_Up,			1,	1000,	1000
# Left/Right & Thumb stuff
None,		Left,	Left,				7,	1000,	1000
None,		Right,	Right,				7,	1000,	1000
None,		Thumb1,	Down,				7,	1000,	1000
Shift_L,	Thumb1,	Up,					7,	1000,	1000
None,		Thumb2,	Up,					7,	1000,	1000
Shift_L,	Thumb2,	Down,				7,	1000,	1000

"^Navigator"
#Alt_L,		Down,	Alt_L|Right
#Alt_L,		Up,		Alt_L|Left
Alt_L,		Down,	Right,				10,	1000,	1000
Alt_L,		Up,		Left,				10,	1000,	1000

# Thanks to Paul J Collins <sneakums@usa.net>
"^emacs"
Shift_L,	Up,		Page_Up
Shift_L,	Down,	Page_Down
# you may need Alt instead of Meta....
None,		Down,	Control_L|Meta_L|Shift_L|parenright
None,		Up,		Control_L|Meta_L|Shift_L|parenleft

# Thanks to etienne grossmann <etienne@isr.ist.utl.pt>
"^Xftp"
,			Down,	j
,			Up,		k

".* - Pan$"
,	Left,	Control_L|Button1
,	Thumb1,	Control_L|Button1
#,	Up,	Button4
#,	Down,	Button5

# Thanks to etienne grossmann <etienne@isr.ist.utl.pt>
"^gv[ :]"
None,		Up,		Shift_L|space
None,		Down,	space

#"^Event Tester"
#@Repeat
#@Exclude
#,	Left,	Button6
#,	Right,	Button7
#,	Thumb1,	Button8
#,	Thumb2,	Button9

"^xv grab"
@Priority=1
@Exclude

"^XV.*"
None,	Down,	Tab
None,	Up,		Delete

"^Untitled"
# if using wheel fifo, you may switch these.
#,	Up,		Button4
#,	Down,	Button5
#with these
,	Up,		Page_Up
,	Down,	Page_Down
# (end of switch)
,   Thumb1, Home
,   Thumb2, End

"^No Title"
# if using wheel fifo, you may switch these.
#,	Up,		Button4
#,	Down,	Button5
#with these
,	Up,		Page_Up
,	Down,	Page_Down
# (end of switch)
,   Left, Home
,   Right, End
,   Thumb1, Home
,   Thumb2, End

#"\(null\)"
# if using wheel fifo, you may want the 2nd group
#,	Up,		Button4
#,	Down,	Button5
#,	Left, Button6
#,	Right, Button7
#,	Thumb1, Button8
#,	Thumb2, Button9
# 2nd group (old keys...)
#,	Up,		Page_Up
#,	Down,	Page_Down
#,	Left, Home
#,	Right, End
#,	Thumb1, Home
#,	Thumb2, End
# (end of switch)

# send event to the window manager when in the root window...
"\(root\)"
,	Up,		Control_L|N
,	Down,	Control_L|P
,   Thumb1,	Alt_L|Left
,	Thumb2,	Alt_L|Right

#
# Uncommment the following to exclude by default.
# Then you will have to add new apps all the time, but will retain any built-in
# wheel functionality contained in some KDE and other newer programs.
# This kinda defeats the original purpose of the program! ;)
#
#".*"
#@Priority=-1000
#@Exclude
#@Repeat

#
# These are the defaults, but note that the defaults for the right side of the
# keyboard are still handled within the program, unless you add the
# combinations desired here. (except for the None modifier of course!)
# If this section is deleted then the hardcoded defaults will be used, which
# are the same thing.
# Modifying these has global effects, but doesn't override what is above.
#
#".*"
#@Priority=-1001
#,	Up,	Button4
#,	Down,	Button5
#None,							Left,	Left
#None,							Right,	Right
#None,							Up,		Page_Up
#None,							Down,	Page_Down
#Shift_L,						Left,	Left
#Shift_L,						Right,	Right
#Shift_L,						Up,		Up
#Shift_L,						Down,	Down
#        Control_L,				Left,	Left,		2
#        Control_L,				Right,	Right,		2
#        Control_L,				Up,		Page_Up,	2
#        Control_L,				Down,	Page_Down,	2
#Shift_L|Control_L,				Left,	Left,		5
#Shift_L|Control_L,				Right,	Right,		5
#Shift_L|Control_L,				Up,		Page_Up,	5
#Shift_L|Control_L,				Down,	Page_Down,	5
#                  Alt_L,		Left,	Left,		10
#                  Alt_L,		Right,	Right,		10
#                  Alt_L,		Up,		Left,		10
#                  Alt_L,		Down,	Right,		10
#Shift_L|          Alt_L,		Left,	Left
#Shift_L|          Alt_L,		Right,	Right
#Shift_L|          Alt_L,		Up,		Left
#Shift_L|          Alt_L,		Down,	Right
#        Control_L|Alt_L,		Left,	Left.		20
#        Control_L|Alt_L,		Right,	Right.		20
#        Control_L|Alt_L,		Up,		Left.		20
#        Control_L|Alt_L,		Down,	Right.		20
#Shift_L|Control_L|Alt_L,		Left,	Left,		50
#Shift_L|Control_L|Alt_L,		Right,	Right,		50
#Shift_L|Control_L|Alt_L,		Up,		Left,		50
#Shift_L|Control_L|Alt_L,		Down,	Right,		50
#,   Thumb1, Home
#,   Thumb2, End

# vim:ts=4:shiftwidth=4:syntax=sh
