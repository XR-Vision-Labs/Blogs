# Setting up ray interaction in unity with Oculus Integration SDK

## Oculus Integration SDK
First import the oculus integration SDK in the project, to get it click [here](https://assetstore.unity.com/packages/tools/integration/oculus-integration-deprecated-82022)

## Setting Up the player controller
Search for OVRPlayerController and import it to your scene

![image](https://github.com/DamanAhuja/Docs/assets/142963733/a154757d-0256-44c2-bbad-eac78a677775)

Then search for OVRInteraction and add it to the scene as the child object of OVRCameraRig

![image](https://github.com/DamanAhuja/Docs/assets/142963733/42e2cb64-fddc-4233-9c87-e21a87339e27)

Now Search for OVRHands and OVRControllers and add them to the scene as child object of OVRInteraction

![image](https://github.com/DamanAhuja/Docs/assets/142963733/9754c112-6608-4fbc-8d5b-dc38cbc528bf)

Now we are done with adding playercontroller and hands, you can now move your player in VR and even see hands and controllers

## Ray Interaction

- Add HandRayInteractor to the HandInteractorsLeft and HandInteractorsRight under the LeftHand and RightHand
- Now Select the HandInteractorLeft and see the inspector tab, and click on the + for list of interactors and drag the HandRayInteractor attached to the HandInteractorLeft.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/dbe47257-1420-42f8-bb17-dffb273bb267)

- Repeat the same with HandInteractorRight
- Add the ControllerRayInteractor for the controllers and repeat the steps as in hands.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/c4ef03a7-a812-4e1b-bff5-2297a132a06e)

Now we have added ray to our hands and controllers, and will now add Something which will be interactable by the Rays

For Eg. we will go with a button for now (click the button with rays)

Search for the OculusInteractionSamplesButtonMenu and import it to the scene.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/3f36bf79-05e5-4856-ad82-567147f2088b)

Now You have many buttons available, you can keep as many as you want and delete the rest.

For now we will work with single button say "Ray"
- click on the ray and in inspector tab

![image](https://github.com/DamanAhuja/Docs/assets/142963733/075cfcec-b905-4892-a536-2f4cfb73c533)

- You will see there is already poke interactable applied to it but we don't want it, so you can remove it and the pointable unity event wrapper if you want.
- Add RayInteractable component to the Button.
- In the surface option add the surface gameobject present with the Ray Button

![image](https://github.com/DamanAhuja/Docs/assets/142963733/d4234ff9-f247-4ac2-a6f7-4ba1584019d6)

![image](https://github.com/DamanAhuja/Docs/assets/142963733/410aedc4-e556-4eab-ba71-24aac58ce09e)

- Click on Clipped Surface for this kind of pop-up.
- Now add Interactable Unity Event Wrapper to button to assign task when the button is clicked.
- Attach the script to a GameObject present in the scene.
- In the Interactable Unity Event Wrapper click on + for the When Select option
- Drag the GameObject where you have added the script and select the function you want to call.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/1366f871-5499-4012-8984-1b7b1d72ccf7)
