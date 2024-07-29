# Enabling the Mender FOTA plugin in the 1NCE portal

1. Navigate to the [1NCE OS Portal](https://portal.1nce.com/portal/customer/connectivitysuite) and login with your credentials.  

2. Make sure you are at the "1NCE OS" tab and search for the "Plugins" tab on the left side of the screen.  

3. Click on "Mender Firmware Over-the-Air Management" and install the Mender Plugin.  

4. Next you will be prompted to enter your oranganization token from the Mender Portal. If you haven't already setup an account then follow the steps on [Getting the Organization token](#getting-the-organization-token).   
After you have done that proceed with step 5.   

5. Once obtained your token paste it into the text box displayed below and press "Next".   
6. The installation on the 1NCE side should be done. Continue with [Connecting a Device to Mender](#connecting-a-device-to-mender)


# Setting up the Mender FOTA Features

## Getting the Organization token

1. Go to the [Mender portal](https://eu.hosted.mender.io/ui/).  
2. Create an account following the steps on the screen or login to your account if you already have one.  
3. Click on your profile on the top right corner and click "My profile".   
4. Go to "Organization and billing", search for the "Organization token" and copy that.  

## Connecting a Device to Mender

To actually connect a device to Mender you can use a firmware blueprint from 1NCE which will try and establish a connection to the Mender Portal.  
1. Get the blueprint [here](https://github.com/1NCE-GmbH/blueprint-zephyr/tree/main/plugin_system/nce_fota_mender_demo)  
> NOTE: you need to have a 1NCE workspace, if you don't have one follow the [Getting started with 1NCE](https://github.com/itsoctotv/how-do-i-develop-with-zephyr-1nce-blueprints/blob/main/howto.md).  
2. Build the application and flash it onto the Thingy:91.  
3. Look at the Mender Dashboard at "Devices" after some time a new device should show up, the LED on it will turn blue and it is asking you to accept the device.  
4. Click on "Pending device" and click on it's ID.  
5. Under "Authorization request" hit the "Accept" button.  
6. The new device is now connected with the Mender service.    
