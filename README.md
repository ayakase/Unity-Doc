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
