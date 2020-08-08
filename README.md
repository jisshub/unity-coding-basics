# Unity - Coding

- unity runs in a big loop - it processes all the informations until it has all gameobjects in a particular position - finally it renders the frame.

- we direct unity with the instruction we write in the scripts.

- a script  must be attached to a game object in the scene to be called by the unity.

- unity works only with object riented scripting languages liike **C#**, python, javascript..

- creating a script
    > Assets(right click) > Create > C# Script

1. Variables
    - a box to store the values and objects

2. Functions
    - collections of code that manipulate this variables.

3. Classes
    - wrap this functions together and reuse later.


##  Update()
    - unity runs the update function once in every frame.
    - untiy looks every script that have an update function.
    - later run the all of the code inside the update function once every frame.
    - once it is done it renders the frame. 

**DemoScript.cs**

```C#


public class DemoScript : MonoBehaviour
{
    // create a Light variable
    public Light myLight;

    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKey("space"))
        {
            // if v press spacebar, light glows 
            myLight.enabled = true;
        }
        else
        {
            myLight.enabled = false;
        }
        // here if v hold the space bar while playing game lights glows,
        // if not, light doesnt glow
    }
}

```

- Later in unty editor, drag this script to Light's inspector
- select the light we want by dragging the Light from Hierachy to My Light field.

**Screenshot**

![image](./screenshots/image1.png 'image')


(13.30 time)

---


