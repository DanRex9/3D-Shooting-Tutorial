# 3D-Shooting-Tutorial
This is a quick unity tutorial on have to shoot projectiles in 3D

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed.

# Objectives
In this tutorial, we will write several scripts that takes player input in the form of a key press to launch/shoot projectiles from a weapon and impact with GameObjects.

# Getting Started
To begin with create a new Unity project, add a cylinder, and then we are going to change the properties of our cylinder. If you look at the Inspector Window while you have your cylinder selected, it will show you all the current properties of the cylinder. At the top of this list is the Transform component. 
As soon as the cylinder is created right clik on Transform and rest the properties this is to set the cylinder in its original place incase of any accidental movements. Next is to change the properties, it should look ilke this.


![Capture 2](https://github.com/user-attachments/assets/47a1484d-d327-416a-89a1-f8b12f8e5c67)


# Creating the Gun
To make our cylinder appear as a gun you will have to be in the Game Camera throughout most of the tutorial, this will give you a better perspective of our objective.

The transform component is responsible for maintaining the position of the gun within the scene. If you modify the position co-ordinates in the inspector, the position of the gun will change relative to the camera.

When creating the cylinder, it comes with several components, one of these being a Capsule Collider, we dont need this component so in the Inspector right click on the Capsule Collider and Remove Component.
It is very important to name all your GameObjects to know what is what, in the Hierarchy right click on the cylinder and Rename it Gun.

# Scriptting Gun

Before starting to write the script, in the Hierarchy you will have to create an epmty as a child of our Gun and name it BulletSpawnPoint it should look like this.


![Capture 3](https://github.com/user-attachments/assets/8df68aaa-e592-46f0-9120-9f9c121bf5a3)

At the bottom of the Inspector click on Add Component and write "Gun" this will give you the option to create a new script and name it Gun

Once the script is added click on the three dots to the right of your script component and click the option that says Edit Script, this should open up Visual Studio in the main editor window, now we can start to write our first Script. The initial code should look like this. 


![Capture 4](https://github.com/user-attachments/assets/ec6ac0a0-caf5-4ce1-96d8-e7ef81929297)
