To work with the Papagayo source code, you need some special software installed. This software is not necessary to run the installer-based version of Papagayo, but you do need it if you want to use this source code package.

Python - the programming language that Papagayo is written in.
http://www.python.org/

wxPython - a cross-platform user interface library for Python, based on wxWidgets.
http://www.wxpython.org/

wxGlade - a user interface builder for wxWidgets. This program is not strictly necessary, but is helpful if you want to modify the user interface of Papagayo.
http://wxglade.sourceforge.net/

Papagayo is written in Python, and requires no special tools to work with the source - a basic text editor is good enough. To run Papagayo, double-click the papagayo.py file, or run the following command:

python papagayo.py

-----------------------------

The Papagayo source package includes the following files:

readme.txt - this file
gpl.txt - the user license for Papagayo

papagayo.py - the main program file
phonemes.py - a list if phonemes used by Papagayo (by default, the Preston Blair phoneme set)
LipsyncDoc.py - the document structure, including voices, phoneme breakdown, etc.
spanish_breakdown.py - code to break down words using Spanish pronunciation rules
LipsyncFrame.py - the main Papagayo window
WaveformView.py - the waveform view in the main window
MouthView.py - the mouth view in the main window
PronunciationDialog.py - a dialog to provide manual phoneme breakdown
AboutBox.py - about box

_lm.dll - a library written in C++ that provides audio support
lm.py - Python interface to the about library, generated automatically

lipsync.wxg - a wxGlade file defining the user interface layout for Papagayo

mouths/ - a folder containing the mouth pictures
rsrc/ - various resources for Papagayo, including button pictures and dictionary files

papagayo.ico - Windows icons
papagayo.icns - MacOS X icons

setup.py - a script to build Papagayo as a standalone Windows application
setup_mac.py - a script to build Papagayo as a standalone MacOS X application

-----------------------------

Here are a couple tips for source code that you may want to modify:

To change the set of phonemes used by Papagayo, edit the file phonemes.py. By default, Papagayo uses the Preston Blair phoneme set. By modifying this file, you can change the set of mouth shapes used to whatever you want. Further instructions can be found in the phonemes.py file itself.

To add breakdowns for other languages, look in the LipsyncDoc.py file. Search for the strings "english" and "spanish" to see how those languages are implemented. Other languages can be added in a similar way.

Papagayo now only works with Moho, but support could be added for other animation software, 2D or 3D. To add support for other export formats, look in the LipsyncDoc.py file for the function LipsyncVoice:Export - this is where Papagayo exports switch data for Moho. You will also need to modify the file LipsyncFrame.py to add a user interface for exporting the new format.

-----------------------------

Copyright (C) 2005 Mike Clifton
Contact:
http://www.lostmarble.com
