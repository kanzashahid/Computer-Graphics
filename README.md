# Computer-Graphics

Dragon copy the next line in your run console to run the project chrome.exe --user-data-dir="C:/Chrome dev session" --disable-web-security http://kanzashahid.5gbfree.com/finaldragon.html

Members: Syed Hassaan Murtaza Naqvi

Kanza Shahid

Description: The idea was to create a Dragon which was successfully achieve. The user can control the dragon by moving it around, The view will is in third person. The dragon moves around in its environment. The environment is in 3D as well and will consists of rugged terrain.

The main inspiration to make the dragon was from the movie how to train your dragon. A dragon is a mythical creature, being unique, and we thought it would be good challenge to make a dragon on our own. The motive behind it is to use the dragon in a game later on with many other characters, the dragon being be the main one

Technical Description: Our project is basically a dragon which moves around in an enviroment. The model of the dragon was taken from CG trader and we uploaded the dragon using the JSONLoader. The texture was also taken from CG trader and was loaded using an MTLLoader. The texture path was set which we uploaded on out website.

The terrain was taken from three.js example. We actually used the basic code from here and added the dragon code to it. We can move around in the terrain using the arrow keys.

We have used OBJLoader to load the dragon in our project and have used the MTLLoader to load the texture file directly. The texture file was according to the dragon so we did not have to make any changes to implement it.

The key 'a' is used to move left.

The key 'd' is used to move right.

The key 'w' is used to move up.

The key 's' is used to move down.

The key 'q' is used to move forward.

The key 'e' is used to move backward.

The key 'r' is used to move start the object rotation.

Rotation starts when you press the 'r' key and then the object can move on all the axis. press 'r' again to stop the rotation and then the object can be moved with the above mentioned keys.

We basically used OrbitControls to get our dragon moving and looked at the ascii of each charachter and then moved the object accordingly; this is implmented in a function named objectcontroller.

We also had an "onkeyup" listener so that we could change the variable values back to zero. This way if we moved the object again it would move relative to the position it was in and move one step at a time only.

Problems faced: The main problem we had to deal with throughout the project was animationg our object or the dragon. We had the animated model on blender with the bones and skeleton, the first problem we faced was that the three.js exporter which should be present was not available for our model in blender. However, we overcame that by using the three.js library exporter; it specifically had a blender exporter that we used.

However, we could not export the dragon model with the animation. Usually when u export a JSON file from blender it is supposed to have an array called 'animation', but when we exported our JSON file the animation array was empty. Therefore, we could not load it using JSONLoader.

We further tried to export the model in .dae format and tried to upload it using the ColladaLoader available online on http://rmx.github.io/collada-converter/preview/examples/convert.html but that also did not work in three.js although the aniamtion was working in the three.js editor and the dragon was walking ( as you can see for yourself if u load the .dae file on the loader in the link provided above). However, the other animations, flying and running were not working even on the three.js editor.

The main problem was in the blender file because without the animation and keyframes the AnimationHandler and AnimationClips could not work, it was actually supoosed to have KeyFrametrack. I tried to find the clip using var clip = THREE.AnimationClip.findByName( clips, 'walk' ) but it couldn't find it and so nothing was playing.

We successfully converted the dragon to .obj file using blender but later on we find out that OBJLoader actually does not support animation so when we used the OBJLoader it actually did load the model but there was stil no animation.

We then tried using convert_obj_three to convert the obj file to js file but I did not have python installed. When I actually did install it had complex errors which i could not handle as i have no experience in python and since we are not that much experienced as the rest of the class so I couldnt figure it out, we also don't have any experience in python and did it only for the sake of this project. That approach, like the rest, failed to help us in any way. We even asked around for help from you, from our class mates, from seniors, posted it on the facebook IBA-FCS group, asked relatives in the CS field but all to no avail. It seemed no one has done three.js and even if they had they did not have any experience in animation.

Future work : Future work may include in animating the dragon by using the json files we created, and importing them to make the dragon move using the bones and scales. Other works may include in adding clouds and create a flying and landing effect. If more needs to be added then an effect of breathing fire can also be added.
