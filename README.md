,## Huawei-honor-unlock-bootloader (Python 3)

## Summary
  
After closing the official EMUI website, which allowed you to retrieve the code to unlock the bootloader of Huawei/Honor phones, here is a python script to retrieve it by yourself.

It uses a bruteforce method, based on the Luhn algorithm and the iMEI identifier used by the manufacturer to generate the unlocking code.

I've only had the opportunity to test it on European versions only :  
- Honor  5x 8x and 9x  
- Honor  view 10 and 20  
- Honor  10 lite  
- Huawei p20 lite  
- Huawei Y6 2019  
- Huawei p30  
  
  
  
## Instructions
### Connecting a device in ADB mode
  
1. Enable developer options in Android.  
2. Enable USB debugging in Android.  
3. Connect your device to the computer and launch the script.  
```batch
C:\WINDOWS\system32> python unlock.py
```
The device is going to ask for authorisation, which you'll have to allow.  
4. Wait for the application to detect your device. The device info should appear.  
5. Enter the (first) IMEI.  
6. Start the bruteforce, (this may take several hours) so get a cup of coffee ☕ and go to sleep. 💫  
7. If the correct code is found, your phone will be instantly unlocked. (and all data erased too)  
  
  
  
## FAQ & Troubleshooting  
  
**- The application doesn't work. Is there anything I should have installed?**  
Yes, it was developed in python so it needs it to run, version 3. You can install the latest version from [here](https://www.python.org/downloads/) or by using Windows Store.
  
**- The app on Windows doesn't detect my device even though it's connected and USB debugging is enabled. What could be the issue?**  
Windows most likely doesn't recognise your device in ADB mode. Install the universal ADB drivers from [here](http://dl.adbdriver.com/upload/adbdriver.zip), reboot your PC and try again.
  
**- My phone reboot every 5 failed attempts**  
Sorry.. I've seen this in a few people and I have no idea. Its look like an additional protection. It happens on some models, having the same version, identical.
