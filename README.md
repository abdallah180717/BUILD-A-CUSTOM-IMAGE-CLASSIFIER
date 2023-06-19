# BUILD-A-CUSTOM-IMAGE-CLASSIFIER

Objective:

Train an image classification model to recognize new objects (all on the Raspberry Pi).

**What you'll learn:**

How to create your own image dataset and labels file to train an ML model.
How to train an image classification model on the Raspberry Pi.


# 1. PREPARE YOUR PHOTOSHOOT

-Find a few objects you can place in front of your camera.

Anything will do for your first attempt, because you'll soon understand how easy it is to retrain the model again and again. For example, grab a shoe, a bottle, a game controller, a figurine, or a potted plant. Try at least 3 objects, but no more than 9.

-Orient the Pi Camera so it's facing a mostly-empty background. The camera's field of view should not be filled with complicated shapes like a large bookshelf or a messy desk. You should also stay out of the pictures as much as possible.

-Make sure you have good lighting so the camera can clearly see the objects you put in front of it: Good: A light source coming from behind the camera or from the sides. Bad: A strong light source coming from behind the object, placing the object in shadow.

# 2. COLLECT THE TRAINING IMAGES


To simplify this part, we've created a camera program that captures photos and organizes them into separate folders based on the number key you press to take the photo. For example, when you press 1, it takes a picture and saves it in a folder named "1", and when you press 2, the photo is saved in folder "2". This way, you'll have all the photos for each object in a separate folder. But actual names are certainly better than numbers for folder names, so we'll create a labels file that maps each number to an object label.

## 1.Create the labels file:

-On your Raspberry Pi, open the ~/aiy-maker-kit/examples/ folder in the File Manager, and then right-click on an empty space in the window and select New File.

-Name the file "labels.txt" and click OK.

-Double-click on the new file to open it in the text editor.

-On the first line, type "Background" (do not include quotation marks).

-Then for each item you'll use for training, enter its name on a new line (such as "Shoe" or "Bottle").

-When you're done, save the file and close the editor.

## 2.Open the Terminal, navigate to the ~/aiy-maker-kit/examples/ directory, and start the camera program (it won't take any pictures until you press a number key):

```
python3 collect_images.py --labels labels.txt
```



