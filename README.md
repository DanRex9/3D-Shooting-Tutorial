# 3D-Shooting-Tutorial
This is a quick unity tutorial on have to shoot projectiles in 3D

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed.

# Objectives
In this tutorial, we will write several scripts that takes player input in the form of a key press to launch/shoot projectiles from a weapon and impact with GameObjects.

# Getting Started
To begin with create a new Unity project, add a cylinder, and then we are going to change the properties of our cylinder. If you look at the Inspector Window while you have your cylinder selected, it will show you all the current properties of the cylinder. At the top of this list is the Transform component. 
As soon as the cylinder is created left clik on Transform and rest the properties this is to set the cylinder in its original place incase of any accidental movements. Next is to change the properties, it should look ilke this.


![Capture 2](https://github.com/user-attachments/assets/47a1484d-d327-416a-89a1-f8b12f8e5c67)


# Creating the Gun
To make our cylinder appear as a gun you will have to be in the Game Camera throughout most of the tutorial, this will give you a better perspective of our objective.

The transform component is responsible for maintaining the position of the gun within the scene. If you modify the position co-ordinates in the inspector, the position of the gun will change relative to the camera.

When creating the cylinder, it comes with several components one of these being CAPSULE cCOLLIDER in the Inspector 
