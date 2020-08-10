# Activating GameObjects

- use SetActive() function to activate the game object.

- if v activate the parent object. all the corresponding child object will be active. if v decativate that obbject it child also decativated.

```C#
public class ActiveDeactive : MonoBehaviour
{

        // create a game object
    public GameObject gameObject;
    
    // Start is called before the first frame update
    void Start()
    {
        // we inactivate the object on play mode
        gameObject.SetActive(false);
    }

}

```


- we can also deactivate a specific child object under a parent object. by providing the game object in the GameObject field.

![image](./screenshots/avtivate.png 'image') 

- here v setActive false to Capsule child object in TestObject parent object.

- v can deacitvate entire parent object and child,

![image](./screenshots/deactivate.png 'image') 

- here u can see v setactive to false for TestObject game object which is the parent.

---


