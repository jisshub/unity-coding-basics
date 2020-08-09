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

## using Scripting Reference

- if v declare a public variable in script, it is accessible with in the unity editor, while private varibles r not accessible in unity


## Types

- Camera, Light, Sphere all r types.


### functions
 1. Awake()
    - will be called before Start() - will not be called  if game object is inactive.
 2. Update()
 3. Start()
 4. LateUpate() - called at the end of the frame 


**DemoScript.cs**

```C#
public class DemoScript : MonoBehaviour
{
    // create a Light variable
    public Light myLight;
    private Light myNewLight; 

    // will be called at the begining 
    void Awake()
    {
        // returned value is stored in myValue variable
        int myValue = AddTwo(10, 30);
        string name = Addnames("jissmon", "jose");
        // log the value
        Debug.Log($"our value is {myValue}, name is {name}");
    }

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
            myLight.enabled = !myLight.enabled;
        }
    } 

    void ChangeLight()
    {
        if (Input.GetKey("space"))
        {
            // if v press spacebar, light glows 
            myLight.enabled = !myLight.enabled;
        }
    }

    public int AddTwo(int a, int b)
    {
        return a + b;
    }

    public string Addnames(string firstname, string lastname)
    {
        var fullName = string.Concat(firstname, ' ', lastname);
        return fullName;
    }
}

```
- time(38:30)

---

## Classes

- collection of variables ad functions.

**DemoScript.cs**
```C#
[System.Serializable]
// System.Serializable is required to show the Class in inspector window of Unity.
public class Student
{
    public int rollNo;
    public string studentName;
}

// can create an instance of this Student class
public Student stdOne;
```

- using custom script

**UtitliScript.cs**

```C#

using System;
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

[System.Serializable]
public class AnotherDataClass
{
    public string name;
    public Color color;
    public GameObject gameObject;
};

```

*DemoScript.cs**
```C#
public AnotherDataClass anotherDataClasses;
```

