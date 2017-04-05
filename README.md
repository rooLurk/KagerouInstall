# Install [RainbowMage's overlay plugin](https://github.com/RainbowMage/OverlayPlugin) if you haven't already
[Direct download link](https://github.com/RainbowMage/OverlayPlugin/releases/download/0.3.3.9/OverlayPlugin-0.3.3.9-x64-full.zip)
- Unzip `OverlayPlugin-0.3.3.9-x64-full.zip` and put the folder inside of it somewhere safe (preferably documents folder).
- Open up ACT and go to `Plugins > Plugin Listing`.
- Click the browse button and locate the folder you extracted.
- Select `OverlayPlugin.dll` and click open.
- Finally click `Add/Enable Plugin` and you're set!

## Troubleshooting

### Could not load file or assembly 'OverlayPlugin.Common' {...}
- Locate the folder you extracted and right click `OverlayPlugin.dll` and select properties.
- At the bottom tick unblock and hit OK.

### An attempt was made to load an assembly from a network location {...}
- Go to your your ACT installation folder (most likely `C:\Program Files\AdvancedCombatTracker`).
- Edit the file called `Advanced Combat Tracker.exe.config` with your favorite text editor.
- Go to line 3 that says `<runtime>` add a new line right below it and paste `<loadFromRemoteSources enabled="true" />` there.
- The file should look like this now:
```XML
<?xml version="1.0"?>
<configuration>
	<runtime>
		<loadFromRemoteSources enabled="true" />
		<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
			<dependentAssembly>
				<assemblyIdentity name="Advanced Combat Tracker" publicKeyToken="a946b61e93d97868" culture="neutral"/>
				<bindingRedirect oldVersion="2.5.0.0-3.65535.65535.65535" newVersion="3.3.0.254"/>
			</dependentAssembly>
		</assemblyBinding>
	</runtime>
	<startup>
		<supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.0,Profile=Client"/>
	</startup>
</configuration>
```
- Save and restart ACT.

# Installing [Kagerou](https://github.com/hibiyasleep/kagerou)
- Go to `Plugins > OverlayPlugin.dll`.
- Remove Spell Timer from the list as it's not needed.
- Go to `Mini Parse` tab.
- Set the URL to `https://hibiyasleep.github.io/kagerou/overlay`.

## Setting the language to English
- In the overlay click the 3 circles in top right and select the cogwheel.
- The very first option is language, set it to English.
- Save by clicking the cyan `저장` right above the setting.
- Every time you access the settings window Kagerou freezes, to fix this go to `Plugins > OverlayPlugin.dll > Mini Parse` and click Reload Overlay.
