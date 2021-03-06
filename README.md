# VoiceWeatherAlarm-

VoiceWeatherAlarm installation instructions for Android
-------------------------------------------------------

Pre-requisites:

- Download ($2.99) [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) app and install it on your phone.

	[Tasker is an app that lets you automate user-customizable actions on your phone via a GUI. It is more user-friendly than dry coding, but it is a lot easier to use if you have some basic know-how about variables, phone functions, and APIs. Let's get started with creating your VoiceWeatherAlarm profile...]

- Download [this](https://github.com/NA-Dev/VoiceWeatherAlarm-Tasker/archive/master.zip) file and unzip it. It contains these instructions and VoiceWeatherAlarm.prf.xml, which you will open from within the Tasker app to install the basic VoiceWeatherAlarm profile. Be sure to note where your phone or computer is saving the file, because you will need to point Tasker to this file on your phone. It should be stored in a folder called "Downloads" unless you have changed some default settings. 

	[The file extension will be ".xml" and contains a bunch of code text that tells Tasker what variables to create and what actions to preform. When you create profile and task details in Tasker, you can export them as .xml files for others to use or as a backup for your creations.]

- Download a Tasker-compatible alarm app for your phone, e.g.  $1.99 or limited free trial version [Gentle Alarm](https://play.google.com/store/apps/details?id=com.mobitobi.android.gentlealarm&hl=en). I tried the stock alarm app, and Tasker did not work properly. Googling confirmed, they are often not compatible.

	[Alternatively, you could give the free [ClockTask](https://play.google.com/store/apps/details?id=com.balda.clocktask&hl=en) plugin a try along with your stock alarm app. I have not yet verified this method for myself, but saw some forum posts about positive results, and the plugin is made specifically for Tasker.]

- Sign up for a free API key with Weather Underground [here](http://www.wunderground.com/weather/api). The key is a 16-character alpha-numeric key, and you will need to type or paste those characters into Tasker. 

	[An API key gives your phone permission to log in to Weather Underground and retrieve data a limited number of times per hour and per day. This should be plenty of allowance for your personal use. Without these keys and limits, spammers could bog Weather Underground down with frivolous requests and force them to shut down this useful service.]


Instructions:

1. Open Tasker

2. You should see the word "PROFILES" in the top left of the menu. Long click the word until a menu pops up. Then, click "Import".

3. At the bottom right, there is a small icon of a phone. Click that, and it opens a list of folders. Click the folder that contains your VoiceWeatherAlarm.xml file, probably the "Downloads" folder. Then, click the VoiceWeatherAlarm file.

4. You should now see a profile in the list called "VoiceWeatherAlarm". 


---Congratulations, you are almost there! Now you just need to edit some of the profile's details that are unique to you.---


5. Click the VoiceWeatherAlarm profile, and you will see a menu drop down below it. 

	[On the left of the details menu are the profile trigger(s), these can be phone settings, events, or variables that Tasker can see. On the right are tasks to be performed. Tasker can tell your phone to perform actions, change settings, or change variables in response to triggers. Tasks can be performed at the moment a trigger starts, at the moment when the trigger ends, or both.]

6. Change the triggers by clicking the left side near the ringing bell icon. A short click will edit details, and a long click will let you add additional, delete, or rename triggers. If you are using Gentle Alarm as your alarm app, there is no need to do this. Skip to the next step.
	
	[If you are using the stock alarm app with a plugin, or another app, you will need to delete the pre-installed trigger and add a new one specific to your app. Instructions on this to come on a later website update.]

7. Change the triggered actions by clicking the right side near the green arrow icon. A short click will edit details, and a long click will let you add additional, delete, or rename tasks. For this installation, short click the green arrow.

8. Now you should see a menu with "Task Edit" at the top, and "AlarmWeather" beneath it. If not, go back and try again.

9. Click task #2, which contains "*Name* %WUnderKey" to open the "Action Edit" menu for that task. Under "To" change the "###changeme###" text to the API key that you generated from Weather Underground. Then exit/save by clicking the arrow on the top left.

10. Click task #3, which contains *Name* %Name. Under "To" change the "###changeme###" text to your name. Then exit/save by clicking the arrow on the top left. Click again to go to the home menu.

	[Android's pre-installed system voice is going to speak this text aloud to you. If you do not like the way she pronounces your name, you can play with the spelling here to "trick" her into pronouncing it correctly. Alternatively, you can get her to call you hilarious titles or make strange sounds (e.g. "Mr. Roboto beep-beep-booooop".]

10. Click task #4, which contains *Name* %Name. Under "To" change the "###changeme###" text to your name. Then exit/save by clicking the arrow on the top left. Click again to go to the home menu.

11. Make sure that the toggle on the left of the VoiceWeatherAlarm profile is toggled on. For my phone, toggle on would show the circle on the right with orange color as opposed to gray.

12. Set an alarm in Gentle Alarm, wait for it to go off, dismiss the alarm, and your weather should soon be read aloud to you. If something goes wrong, try once more. Your phone may be a little different, or something may have been changed since I wrote this. Maybe you can use Google-fu to figure it out. If it works, then...


---Celebrate! You did it!---


Additional optional customizations:

- Change Task #9 Text to a message of your choosing. You can even delete some of the weather forecast items if you do not want them spoken aloud.

- Change Task #9 Engine:Voice to a different accent by clicking the magnifying glass icon. I made English - Australian accent ("eng-aus") the default, but others are available (e.g. "eng-usa", "eng-gbr").

- Change Task #7 to set the volume of the spoken words.

- Advanced (instructions not covered here): Learn more about the wunderground API variable options and add additional weather conditions to the spoken forecast. You will need to edit task #6 and task #9 to do this.

- Advanced (instructions not covered here): Modify your profile to only read the weather on rainy days. Like [this](https://github.com/mbirth/tasker/blob/master/RainWarning.prf.xml) profile from GitHub user "mbirth" called RainWarning. You can import his xml file into Tasker or read the code with a text editor to see how it works.