# Getting Started with VR on Unity with Oculus SDK
## Package Install
Get on this [website](https://assetstore.unity.com/packages/tools/integration/oculus-integration-deprecated-82022) and then press "add to my assets".

By this we have just now added the package to our unity assets, now it's time to import it in our project

For achieving that, just follow the steps shown in the images below

![image](https://github.com/DamanAhuja/Docs/assets/142963733/cb8b477d-31c3-4e28-b010-8e51d3e874eb)

![image](https://github.com/DamanAhuja/Docs/assets/142963733/dd08f5a3-face-4b29-befc-217dd1a0550e)

Then search for Oculus Integration SDK and click on install

![image](https://github.com/DamanAhuja/Docs/assets/142963733/4ba9cf32-2c18-4ef8-b999-101f2baac9e1)

Click on no for this type of pop-up

![image](https://github.com/DamanAhuja/Docs/assets/142963733/de85fe1b-68e4-4c22-9f0f-b85a74acd219)
## Switching Platform
Click on File Option and find Build Settings

Set it on Android and click "Switch Platform"

![image](https://github.com/DamanAhuja/Docs/assets/142963733/5578fd15-ecc4-4a57-ba58-6f9dd4be4258)

## Setting up
Look for this kind of logo in bottom right corner, and click project setup tool

![image](https://github.com/DamanAhuja/Docs/assets/142963733/f3c44569-d8b0-4a68-9097-b5b0afe0e8e3)

Click on Fix all to fix all the issues if any, and apply all to apply all the required settings

## Creating the Scene
Now as we have done all the settings, its time to add components to our scene

First search for OVRPlayerController and import it to your scene

![image](https://github.com/DamanAhuja/Docs/assets/142963733/a154757d-0256-44c2-bbad-eac78a677775)

Then search for OVRInteraction and add it to the scene as the child object of OVRCameraRig

![image](https://github.com/DamanAhuja/Docs/assets/142963733/42e2cb64-fddc-4233-9c87-e21a87339e27)

Now Search for OVRHands and OVRControllers and add them to the scene as child object of OVRInteraction

![image](https://github.com/DamanAhuja/Docs/assets/142963733/9754c112-6608-4fbc-8d5b-dc38cbc528bf)

Now we are done with adding playercontroller and hands, you can now move your player in VR and even see hands and controllers

