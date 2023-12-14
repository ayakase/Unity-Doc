# Unity-Doc
Description
Position, rotation and scale of an object.

Every object in a Scene has a Transform. It's used to store and manipulate the position, rotation and scale of the object. Every Transform can have a parent, which allows you to apply position, rotation and scale hierarchically. This is the hierarchy seen in the Hierarchy pane. They also support enumerators so you can loop through children using:

using UnityEngine;

public class Example : MonoBehaviour
{
    // Moves all transform children 10 units upwards!
    void Start()
    {
        foreach (Transform child in transform)
        {
            child.position += Vector3.up * 10.0f;
        }
    }
}
See Also: The component reference, Physics class.

Properties
childCount	The number of children the parent Transform has.
eulerAngles	The rotation as Euler angles in degrees.
forward	Returns a normalized vector representing the blue axis of the transform in world space.
hasChanged	Has the transform changed since the last time the flag was set to 'false'?
hierarchyCapacity	The transform capacity of the transform's hierarchy data structure.
hierarchyCount	The number of transforms in the transform's hierarchy data structure.
localEulerAngles	The rotation as Euler angles in degrees relative to the parent transform's rotation.
localPosition	Position of the transform relative to the parent transform.
localRotation	The rotation of the transform relative to the transform rotation of the parent.
localScale	The scale of the transform relative to the GameObjects parent.
localToWorldMatrix	Matrix that transforms a point from local space into world space (Read Only).
lossyScale	The global scale of the object (Read Only).
parent	The parent of the transform.
position	The world space position of the Transform.
right	The red axis of the transform in world space.
root	Returns the topmost transform in the hierarchy.
rotation	A Quaternion that stores the rotation of the Transform in world space.
up	The green axis of the transform in world space.
worldToLocalMatrix	Matrix that transforms a point from world space into local space (Read Only).
Public Methods
DetachChildren	Unparents all children.
Find	Finds a child by name n and returns it.
GetChild	Returns a transform child by index.
GetLocalPositionAndRotation	Gets the position and rotation of the Transform component in local space (that is, relative to its parent transform).
GetPositionAndRotation	Gets the position and rotation of the Transform component in world space.
GetSiblingIndex	Gets the sibling index.
InverseTransformDirection	Transforms a direction from world space to local space. The opposite of Transform.TransformDirection.
InverseTransformDirections	Transforms multiple directions from world space to local space overwriting each original position with the transformed version. The opposite of Transform.TransformDirections.
InverseTransformPoint	Transforms position from world space to local space.
InverseTransformPoints	Transforms multiple positions from world space to local space overwriting each original position with the transformed version.
InverseTransformVector	Transforms a vector from world space to local space. The opposite of Transform.TransformVector.
InverseTransformVectors	Transforms multiple vectors from world space to local space overwriting each original position with the transformed version. The opposite of Transform.TransformVectors.
IsChildOf	Is this transform a child of parent?
LookAt	Rotates the transform so the forward vector points at /target/'s current position.
Rotate	Use Transform.Rotate to rotate GameObjects in a variety of ways. The rotation is often provided as an Euler angle and not a Quaternion.
RotateAround	Rotates the transform about axis passing through point in world coordinates by angle degrees.
SetAsFirstSibling	Move the transform to the start of the local transform list.
SetAsLastSibling	Move the transform to the end of the local transform list.
SetLocalPositionAndRotation	Sets the position and rotation of the Transform component in local space (i.e. relative to its parent transform).
SetParent	Set the parent of the transform.
SetPositionAndRotation	Sets the world space position and rotation of the Transform component.
SetSiblingIndex	Sets the sibling index.
TransformDirection	Transforms direction from local space to world space.
TransformDirections	Transforms multiple directions from local space to world space overwriting each original direction with the transformed version.
TransformPoint	Transforms position from local space to world space.
TransformPoints	Transforms multiple points from local space to world space overwriting each original point with the transformed version.
TransformVector	Transforms vector from local space to world space.
TransformVectors	Transforms multiple vectors from local space to world space overwriting each original vector with the transformed version.
Translate	Moves the transform in the direction and distance of translation.
Inherited Members
Properties
gameObject	The game object this component is attached to. A component is always attached to a game object.
tag	The tag of this game object.
transform	The Transform attached to this GameObject.
hideFlags	Should the object be hidden, saved with the Scene or modifiable by the user?
name	The name of the object.
Public Methods
BroadcastMessage	Calls the method named methodName on every MonoBehaviour in this game object or any of its children.
CompareTag	Checks the GameObject's tag against the defined tag.
GetComponent	Gets a reference to a component of type T on the same GameObject as the component specified.
GetComponentInChildren	Gets a reference to a component of type T on the same GameObject as the component specified, or any child of the GameObject.
GetComponentInParent	Gets a reference to a component of type T on the same GameObject as the component specified, or any parent of the GameObject.
GetComponents	Gets references to all components of type T on the same GameObject as the component specified.
GetComponentsInChildren	Gets references to all components of type T on the same GameObject as the component specified, and any child of the GameObject.
GetComponentsInParent	Gets references to all components of type T on the same GameObject as the component specified, and any parent of the GameObject.
SendMessage	Calls the method named methodName on every MonoBehaviour in this game object.
SendMessageUpwards	Calls the method named methodName on every MonoBehaviour in this game object and on every ancestor of the behaviour.
TryGetComponent	Gets the component of the specified type, if it exists.
GetInstanceID	Gets the instance ID of the object.
ToString	Returns the name of the object.
Static Methods
Destroy	Removes a GameObject, component or asset.
DestroyImmediate	Destroys the object obj immediately. You are strongly recommended to use Destroy instead.
DontDestroyOnLoad	Do not destroy the target Object when loading a new Scene.
FindAnyObjectByType	Retrieves any active loaded object of Type type.
FindFirstObjectByType	Retrieves the first active loaded object of Type type.
FindObjectOfType	Returns the first active loaded object of Type type.
FindObjectsByType	Retrieves a list of all loaded objects of Type type.
FindObjectsOfType	Gets a list of all loaded objects of Type type.
Instantiate	Clones the object original and returns the clone.
Operators
bool	Does the object exist?
operator !=	Compares if two objects refer to a different object.
operator ==	Compares two object references to see if they refer to the same object.
Downloading and installing Unity
Download and install the Unity Editor from the Unity download page. The installer uses a Download Assistant and has detailed instructions to follow. If you want to download the Unity Editor using a torrent or install several versions of Unity at once, see Torrent Download, below.

Unity Download Assistant
The Unity Download Assistant is a small executable program (approximately 1 MB in size) which lets you select which components of the Unity Editor you want to download and install.

If you’re not sure which components you want to install, leave the default selections, click Continue, and follow the installer’s instructions.

Unity Download Assistant (leave the default selections if youre not sure which to choose)
Unity Download Assistant (leave the default selections if you’re not sure which to choose)
Note that on PC there is Microsoft Visual Studio Community 2015.

###

Installing Unity without the Download Assistant
If you prefer, you can download and install all of the components separately, without using the Download Assistant. The components are normal installer executable programs and packages, so you may find it simpler, especially if you are a new Unity user, to use the Download Assistant. Some users, such as those wishing to automate deployment of Unity in an organization, may prefer to install from the command line.

Installing Unity on Windows from command line
The following options can be used when installing the Unity Editor and other components from command line on Windows. Note that installer command line arguments are case-sensitive.

Unity Editor install
/S	Performs a silent (no questions asked) install.
/D=PATH	Sets the default install directory. Useful when combined with the silent install option. Default folder is C:\Program Files (x86)\Unity (32-bit) or C:\Program Files\Unity (64-bit)
Example:

UnitySetup64.exe /S /D=E:\Development\Unity
Install Unity silently to the folder E:\Development\Unity, which will be the root of the Unity installation. The Unity editor executable will in this case be installed in E:\Development\Unity\Editor\Unity.exe. “/D” argument must be last and without quotes, even if path contains spaces.

Unity Editor uninstall
To perform a silent uninstall, run Uninstall.exe /S (for example, from command line or a script).

Note that although the process will finish right away, it takes a few seconds before the files are actually removed. The reason for this is that the uninstaller is copied to a temporary location in order to be able to remove itself. Also, make sure the working directory is not inside the Unity install location, as it won’t be able to remove the folder if this is the case.

Standard Assets install
Silently install Standard Assets. If specifying folder, use the Unity “root” folder (that is, the folder containing the Editor folder, and not where Unity.exe is installed into).
What is scripting in Unity?
Scripting tells our GameObjects how to behave; it’s the scripts and components attached to the GameObjects, and how they interact with each other, that creates your gameplay. Now, scripting in Unity is different from pure programming. If you’ve done some pure programming, e.g. you created a running app, you should realize that in Unity you don’t need to create the code that runs the application, because Unity does it for you. Instead, you focus on the gameplay in your scripts.

Unity runs in a big loop. It reads all of the data that’s in a game scene. For example, it reads through the lights, the meshes, what the behaviors are, and it processes all of this information for you.

If you think about television, where, for example in North America, you have 29.5 frame/sec, Unity needs to do the same thing. It’s running single discrete frames, one after another. You direct Unity with the instructions that you write in your scripts, and Unity executes them frame after frame as fast as it can.

Achieving a high frame rate means not only your game will look more fluid, but your scripts will also be executed more often, making controls more responsive.

 

What languages can you use in Unity?
A script must be attached to a GameObject in the scene in order to be called by Unity. Scripts are written in a special language that Unity can understand. And, it’s through this language that we can talk to the engine and give it our instructions.

The language that’s used in Unity is called C# (pronounced C-sharp). All the languages that Unity operates with are object-oriented scripting languages. Like any language, scripting languages have syntax, or parts of speech, and the primary parts are called variables, functions, and classes.

If you’re using a version of Unity until 2017.3, you’ll notice that it has a text editor called MonoDevelop: it can help us complete our code, it’ll let us know if we’re writing a wrong piece of code, and allows us to take shortcuts. Starting with 2018.1, you can also use Visual Studio for Unity Community, or other text editors such as Visual Studio, Notepad, or Sublime text.

Here’s a script with some sample code in it (based on the Coding in Unity for the Absolute Beginner tutorial):


As you can see, there are variables, functions, and classes.

 

What do these do?
Variables hold values and references to objects (you can see objects as “bigger” variables). They’re like a box that holds something for us to use. Variables start with a lowercase letter.

Functions are collections of code that compare and manipulate these variables. Functions start with an uppercase letter. We organise code in functions so that they can be easily reused multiple times in different parts of the program.

Classes are a way to structure code to wrap collections of variables and functions together to create a template that defines the properties of an object.

Scripting is primarily comparing these objects and their current states and values. It’s based on logic determining an outcome or resolution.

 

Variables
In Unity, the scripts start by laying out the tools that you need at the top, and this is usually by declaring variables. You can see the declared variables here with the visibility keyword “public” or "private" at the front, followed by a type, and a name.

variables
When we’re declaring your variables there are several visibility types, but the two most important ones are public and private.

If you create a script with the above text in your code editor and then come back to Unity and assign the script to a GameObject, you’ll see that you can access and see the light variable declared as public in the Inspector, but you can’t see the private one. And that’s because what’s defined as “private” can only be accessed within this particular script, within this particular class.

If you make this public, then it’s accessible to other scripts and other classes, and can be changed in the Inspector from the Unity editor. So, that means other people can access it and change its value.

There are many reasons to choose between private or public. Private variables allow your code to be cleaner, since you know that the value of those variables can be changed only inside that class. This makes debugging and maintaining the code easier.

If you choose “public” , and you experience an issue, you need to look inside your whole codebase in order to track the source because any other object has access to that variable. However, if you want objects to communicate between themselves you need some variables (or functions) to be public.

Another important aspect of variables is the type. A type defines what kind of value is the variable holding in memory, e.g. it can be a number, text, or more complex types, like the ones in the image below: Transform, Light and Demo Script in the image below are in fact references to Components. Unity needs to know what type of object it is so that it knows how to handle it.

Variable types
Another important thing about variables is the name. The main thing that you need to remember about naming variables is that it can’t start with a number, and it can’t contain spaces. Therefore, there’s a style of writing the names. In C#, the naming convention is camelCase: you start with a lowercase letter and add words, without spaces, starting with a capital letter, e.g. "myLight".

When Unity compiles the script, it makes public variables visible in the editor. See the image below from the inspector.

demo script
Functions
Scripts manipulate the variables by using functions. There are a number of functions that run automatically inside Unity. See below:

functions
Awake is called only once when the GameObject with that component is instantiated. If a GameObject is inactive, then it will not be called until it is made active. However, Awake is called even if the GameObject is active but the component is not enabled (with the little checkbox next to its name). You can use Awake to initialize all the variables that you need to assign a value to.

Start – like Awake, Start will be called if a GameObject is active, but only if the component is enabled. For more information on the differences with Awake, see this video.

Update is called once per frame. This is where you put code to define the logic that runs continuously, like animations, AI, and other parts of the game that have to be constantly updated.

FixedUpdate is when you want to do physics work.

As you can see, there’s Fixed Update and Update and in our Scripting tutorials section, you can learn how to effect changes every frame with the Update and FixedUpdate functions, and their differences.

LateUpdate is a function that’s similar to Update, but LateUpdate is called at the end of the frame. Unity will look at all of the game objects, find all of the Updates, and call the LateUpdates. This is good for things like the camera. Let’s say you want to move a character in your game. And then he’s bumped into by another character and ends up in a different position. If we move the camera at the same time as the character, there would be a jiggle, and the camera wouldn’t be where it needs to be. So, basically, it’s a second loop that comes in very handy.

 

Writing functions
When writing a function, remember that functions start with the returned type of the function at the beginning, followed by the name of the function, and then the parameters in the parentheses (if any). Function names start with a capital letter and the body of the function goes between the curly brackets. Here’s an example on how to write a function:

writing function
How do we call this function?

call function
Functions can do calculations and then return a value. You can ask a function to do something, process the information, then return an answer. If you use the type "void", then they are not returning anything.

 

Classes
Classes are collections of these variables and functions. For example, this script is a class:

Script class
Bear in mind that the class name must match the file name of the C# script for it to work. And then to be attached to a GameObject, it has to derive from another class called MonoBehaviour which is automatically put there for you when you first create a script. Classes can also be public or private.

In Unity, if you create a custom class, like in the example below, you have to ask it to serialize it. This means that it will be converted into simple data that Unity can look at in the inspector. When you do that, it’ll see that you have the class will appear in the inspector.

serial class
Variables, functions, and classes are just the basics of starting with coding in Unity. Check out the Learn section, you can find a bunch of useful scripting tutorials that will help you go learn about programming from scratch, then progress to create detailed code for your projects.
