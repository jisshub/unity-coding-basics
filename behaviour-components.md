# C# Scripts as Behaviour Components

- can apply the different components to the objects. 

- for eaxmple we can apply *rigidbody component* to the cube objects. when v play the game, it falls in to the ground since gravity.

- scripts can be created from Add Component > New Script.

```C#

public class ChangeCubeColor : MonoBehaviour
{
    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            // if v press key r, then color of object changes to red
            GetComponent<Renderer>().material.color = Color.red;
        }
        if (Input.GetKeyDown(KeyCode.B))
        {
            // if v press key b, then color of object changes to blue
            GetComponent<Renderer>().material.color = Color.blue;
        }
        if (Input.GetKeyDown(KeyCode.G))
        {
            GetComponent<Renderer>().material.color = Color.green;
        }

    }
}

```


