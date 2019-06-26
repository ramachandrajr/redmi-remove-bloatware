# redmi-remove-bloatware
Yup redmi is filled with bloatware, getting killed with redmi ads?
May be this can help?

## Step 1: Install ADB
First you have to install adb on your computer, it stands for android bridge. So you might want to google `adb android install <os name>`. 
Luckily for me in fedora, you can do:
```
sudo dnf install android-tools
```

## Step 2: Connect your phone to the computer via USB

## Step 3: Enable USB debugging
Then in your android phone
1. Settings >
2. About phone 
3. Then tap the about phone about 7 times. 

Developer options should be enabled as a result. Then back to the
1. Main settings >
2. Additional settings >
3. Developer options >
4. Enable USB debugging

### Step 4: Listing connected devices
do 
```
sudo adb kill-server # precaution
sudo adb start-server
sudo adb start-server
adb devices
```
You should see something like:
```
List of devices attached
05c8bc567d2a	device
```
That states your phone is connected properly!
<br />
If you see no permissions or any such term, check your phone, you'll see a popup asking for permissions, accept that. That's it!

Then run the commands in the file that say `adb <anything else>`

if you are on linux, then you're in luck
1. just download / save the file
2. `chmod +x rm_mi_bloatware.sh`
3. `./rm_mi_bloatware.sh`

and all will be cleared out. 

If you feel there can be some good changes, send some pull requests.
