=========
termstyle
=========

termstyle is a simple python library for adding coloured output to
terminal (console) programs.  The definitions come from ECMA-048_, the
"Control Functions for Coded Character Sets" standard.

Installation::

	easy_install termstyle
	
or from source::

	./setup.py bdist_egg
	cp dist/termstyle-*.egg <path-to-your-python-libraries>

Example Usage:
--------------
::

	from termstyle import *
	print "%s:%s" % (red('Hey'), green('how are you?'))
	print blue('How ', bold('you'), ' doin?')

or, you can use a colour just as a string::

	print "%sBlue!%s" % (blue, reset)

Styles:
-------
::

	reset or default (no colour / style)

colour::

	black
	red
	green
	yellow
	blue
	magenta
	cyan
	white

background colour::

	bg_black
	bg_red
	bg_green
	bg_yellow
	bg_blue
	bg_magenta
	bg_cyan
	bg_white

weight::

	bold
	inverted

style::

	italic
	underscore

Controls:
---------
::

	auto() - sets colouring on only if sys.stdout is a terminal
	disabe() - disable colours
	enable() - enable colours

.. _ECMA-048: http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-048.pdf

