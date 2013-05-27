GoAgentOSX.app
==============
GoAgent 3.0 ships with a new shell script for the GUI launcher. However, launching it
leaves the Terminal opened and needs to be closed manually.

This application is a wrapper to the launcher, created using Platypus. It has been
created simply to eliminate the terminal window.

GoAgent
  https://code.google.com/p/goagent/
Platypus
  http://sveinbjorn.org/platypus

Preferences:
============
By default, this app looks for "goagent-osx.command" distributed from GoAgent 3.0.x 
in /Application/goagent/goagent/local directory. You can modify a property to point
to your installation if it's different.

Configuration:
==============
1. defaults
Simply run the defaults command to update your goagent root directory

defaults write /Applications/goagent/GoAgentOSX.app/Contents/Resources/AppSettings \
ScriptArgs -array -string /Applications/goagent/goagent

2. Editing the AppSettiings.plist
You can simply edit the AppSettings property list file and update the ScriptArgs key value

vi GoAgentOSX.app/Contents/Resources/AppSettings.plist

XML:
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" 
"http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>ScriptArgs</key>
	<array>
		<string>/Applications/goagent/goagent</string>
	</array>
</dict>
</plist>


@d7an
2013-05-27
