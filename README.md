# 3D-Shooting-Tutorial
This is a quick unity tutorial on have to shoot projectiles in 3D

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed.

# Objectives
In this tutorial, we will write several scripts that takes player input in the form of a key press to launch/shoot projectiles from a weapon and impact with GameObjects.

# Getting Started
To begin with create a new Unity project, add a cylinder, and then we are going to change the properties of our cylinder. If you look at the Inspector Window while you have your cylinder selected, it will show you all the current properties of the cylinder. At the top of this list is the Transform component. 
As soon as the cylinder is created right clik on `Transform` and rest the properties this is to set the cylinder in its original place incase of any accidental movements. Next is to change the properties, it should look ilke this.


![Capture 2](https://github.com/user-attachments/assets/47a1484d-d327-416a-89a1-f8b12f8e5c67)


# Creating the Gun
To make our cylinder appear as a gun you will have to be in the Game Camera throughout most of the tutorial, this will give you a better perspective of our objective.

The transform component is responsible for maintaining the position of the gun within the scene. If you modify the position co-ordinates in the inspector, the position of the gun will change relative to the camera.

When creating the cylinder, it comes with several components, one of these being a Capsule Collider, we dont need this component so in the Inspector right click on the Capsule Collider and Remove Component.
It is very important to name all your GameObjects to know what is what, in the Hierarchy right click on the cylinder and Rename it `Gun`.

In the Hierarchy right click and create empty and name it `BulletSpawnPoint` we will come back to this in the scripting of the gun so you can leave it for now.

# Scriptting Gun

Before starting to write the script, in the Hierarchy you will have to create an epmty as a child of our Gun and name it `BulletSpawnPoint` it should look like this.


![Capture 3](https://github.com/user-attachments/assets/8df68aaa-e592-46f0-9120-9f9c121bf5a3)

At the bottom of the Inspector click on Add Component and write "Gun" this will give you the option to create a new script and name it `Gun`

Once the script is added click on the three dots to the right of your script component and click the option that says Edit Script, this should open up Visual Studio in the main editor window, now we can start to write our first Script. The initial code should look like this. 
 

![Capture 4](https://github.com/user-attachments/assets/ec6ac0a0-caf5-4ce1-96d8-e7ef81929297)

- `public` this means we can access it from other scripts
- `class` means that what follows is a class definition
- `gun` is the name we supplied for the class
- `:` means this class inherits functions and variavles from anothe rclass
- [`MonoBehaviour`](https://docs.unity3d.com/2022.3/Documentation/ScriptReference/MonoBehaviour.html) is the Unity supplied class we are basing our new class on
  

![Capture 6](https://github.com/user-attachments/assets/e5e54d7c-c4eb-4701-9b3f-636e8cc8ff6a)

 To begin with we want to make our variables `public` this is so we can access and modify these variables within unity.
 
 If you follow the links in the documentation, you will see that [`Transform`](https://docs.unity3d.com/2022.3/Documentation/ScriptReference/Transform.html) itself is another Unity supplied class. And it has a number of useful functions that we can use to modify the transform of an object, in this case the `bulletSpawnPoint`, this is for us to later on work on the spawnpoint of our bullet and where the projectile will launch from.
 
Our second variable we have to code is `GameObject bulletPrefab` this creates an open variable where you can access in the inspector window in Unity, later on we will have to create a bullet [`prefab`](https://docs.unity3d.com/Manual/Prefabs.html) to add to our script.
If you save at this stage and check the Inspector window in Unity it should look like this.

![Capture 7](https://github.com/user-attachments/assets/c8eff2a7-8585-42bc-b078-2149fb6bdbb0)


Now in the Hierarchy click and drag `BulletSpawnPoint` and add it to the `Gun` script, now in the scene view select `BulletSpawnPoint` and move it so its at the edge of our gun, you can adjust the placement of the spawn point to your liking. At this stage it should look like this.


![Capture 55](https://github.com/user-attachments/assets/7b883d64-8cee-4326-92f8-de95489e1337)

# Creating and Scripting Bullet


Now again in the Hierarchy right click and go to 3D Object and create a sphere, NAME it `Bullet` and in transform change the `X`, `Y` and `Z` to 0.5.
In the inspector right click and add the `Rigidbody` component, inside the rigidbody unclick `Use Gravity` 
Create a C# script and name it `Bullet` now we can start with the scripting. 


