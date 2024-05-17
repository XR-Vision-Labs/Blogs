# Snap interaction in unity with Oculus integration SDK
First we need to import the Oculus Integration SDK in our project, you can get it from [here](https://assetstore.unity.com/packages/tools/integration/oculus-integration-deprecated-82022)
## Setting up OVR hands and controllers
First search for OVRPlayerController and import it to your scene

![image](https://github.com/DamanAhuja/Docs/assets/142963733/a154757d-0256-44c2-bbad-eac78a677775)

Then search for OVRInteraction and add it to the scene as the child object of OVRCameraRig

![image](https://github.com/DamanAhuja/Docs/assets/142963733/42e2cb64-fddc-4233-9c87-e21a87339e27)

Now Search for OVRHands and OVRControllers and add them to the scene as child object of OVRInteraction

![image](https://github.com/DamanAhuja/Docs/assets/142963733/9754c112-6608-4fbc-8d5b-dc38cbc528bf)

Now we are done with adding playercontroller and hands, you can now move your player in VR and even see hands and controllers

## Snap Interaction 

### To add Snap Interaction

First we need to add OVRGrabInteractor to the hands and controllers.
- Add HandGrabInteractor to the HandInteractorsLeft and HandInteractorsRight under the LeftHand and RightHand
- Now Select the HandInteractorLeft and see the inspector tab, and click on the + for list of interactors and drag the HandGrabInteractor attached to the HandInteractorLeft.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/7271946e-8d39-4bf0-adcd-e6bdaef796fc)

- Repeat the same with HandInteractorRight
- Add the ControllerGrabInteractor for the controllers and repeat the steps as in hands.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/46af94e6-ec65-44c5-9be5-ed7bdb65c2f5)

Add a 3D Object and a postion where you want to snap the Object.
- Create a cube and add rigidbody to it and turn of it's renderer so that it doesn't appear in the scene. Resize the cube accordingly as it will be the area in which the snap will work.

Coming to the Object now, let's take a Sphere
- Add rigidbody to it and turn off the use gravity checkbox, and turn on the is kinematic checkbox
- Add Grabbable compenent to the sphere
- Create an empty game object as the the child of the Sphere, and name it as snap interactor
- Add the SnapInteractor Component to the game object and in the inspector tab, add the sphere to pointable element, rigidbody and in optionals too add the sphere in transform tab.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/3e0c1d6e-27a5-4345-bbe4-1fcd8f99f82b)

- You can add the Interactable object to the Default Interactable tab to make the object snap by default.
  
Coming to the Position where object will be snapped
- Remove the colliders 
- Create an empty GameObject named SnapInteractable under the Position
- Add Snap Interactable component to the empty gameobject
- In the Inspector pannel, add the cube made earlier to the rigidbody tab.

![image](https://github.com/DamanAhuja/Docs/assets/142963733/0780e3df-8cd3-483f-9abd-831bfd2e1ae3)

