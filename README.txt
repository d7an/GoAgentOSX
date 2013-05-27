GoAgentOSX.app
==============
This application is a wrapper to launch the GoAgent service, created using Platypus.
It has been created simply to eliminate the terminal window after launching the supplied
shell script.

Platypus
  http://sveinbjorn.org/platypus

Preferences:
============
By default, this app looks for "goagent-osx.command" distrubuted from GoAgent 3.x 
in /Application/goagent/goagent/local directory. You can modify a property to point
to yours if it's different.

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


@dtan
2013-05-27
