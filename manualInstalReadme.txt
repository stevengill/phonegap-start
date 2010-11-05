{\rtf1\ansi\ansicpg1252\cocoartf1038\cocoasubrtf320
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\froman\fcharset0 Times-Roman;\f2\fnil\fcharset0 LucidaGrande;
}
{\colortbl;\red255\green255\blue255;}
\margl1440\margr1440\vieww9000\viewh8400\viewkind0
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\ql\qnatural\pardirnatural

\f0\fs24 \cf0 PhoneGap start App\
\
Android\
-Eclipse\

\f1 1) File > New > Android Project\
	\'95	Project Name: PhoneGap Start\
	\'95	Create new project in workspace must be clicked\
	\'95	Select Highest build target available -> Android 2.2\
	\'95	Application Name: PhoneGapStart\
	\'95	Package name: com.phonegap.start\
	\'95	Create Activity: App\
\
2) In the root of the project copy, create folder named libs. In assets directory, create folder www. Copy over Android/phonegap-0.9.2.jar to /libs\'a0and Android/phonegap-0.9.2.js\'a0 to /assets/www. These files come included in the download of phonegap 0.9.2 from phonegap.com\
\
3) From phonegap-start, copy index.html, master.css, staticmap.png and application.js into the new project's assets/www folder\
\
4)From phonegap-start, copy icon.png into res/drawable-hdpi, res/drawable-ldpi and res/drawable-mdpi\
\
5) Make a few adjustments too the project's main Java file found in the src folder in Eclipse. It should be named App.java\
	
\f2 \uc0\u9642 
\f1 	Change the class's extend from Activity to DroidGap\
	
\f2 \uc0\u9642 
\f1 	Replace the setContentView() line with super.loadUrl("file:///android_asset/www/index.html");\
	
\f2 \uc0\u9642 
\f1 	Add import com.phonegap.*;\
\
6) Lets add some permissions to the AndroidManifest.xml file to allow phonegap to run properly.\
\
Open up your manifest file in your favourite editor and paste the following information after the versionName but before the application tag:\
<supports-screens
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0android:largeScreens="true"
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0android:normalScreens="true"
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0android:smallScreens="true"
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0android:resizeable="true"
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0android:anyDensity="true"
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0/>
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0 \'a0<uses-permission android:name="android.permission.CAMERA" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.VIBRATE" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.ACCESS_LOCATION_EXTRA_COMMANDS" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.READ_PHONE_STATE" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.INTERNET" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.RECEIVE_SMS" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.RECORD_AUDIO" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.READ_CONTACTS" />
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.WRITE_CONTACTS" />\'a0 \'a0
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />\'a0 \'a0
\f2 \uc0\u8232 
\f1 \'a0\'a0 \'a0\'a0\'a0\'a0 <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />\
\
7) You can now run you project as an Android Application. Right click the project and go to Run As and click Android Application.\'a0 Eclipse might ask you to select an appropriate AVD. If there isn't one, then you'll need to create it before you can continue.\
\
\
iPhone\
-xCode\
1) File > New Project\
	\'95	Select a location and name your project PhoneGapStart\
\
2)  From phonegap-start, copy index.html, master.css, staticmap.png and application.js into the new project's www folder\
\
3) Open PhoneGapStart-Info.plist and change "BundleDisplayName" to PhoneGapStart and change the "BundleIdentifier" to the one provided to you by apple if you have one.\
\
webOS\
1) Copy the webOS folder from the phonegap download from phonegap.com/download and paste it into a new directory in which you desire to work from.\
\
2) From phonegap-start, copy index.html, master.css, staticmap.png, icon.png and application.js into the webOS/framework/www folder\
\
3) Plug in your Palm device or Launch the emulator\
\
4) In the framework folder, edit appinfo.json with relevant info. Update title to PhoneGapStart\
\
5) In terminal, navigate to your working directory webOS file, type make. This should install and launch the app on your device/emulator\
\pard\tx560\pardeftab720\ql\qnatural
\cf0 \
\
\
\
\
\
\
}