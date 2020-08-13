# Get Component

- in unity scripts r considered as a *custom component*. 

- v can ccess the other scripts and components using *GetComponent*.

- in Awake() - we initialized our variables.

- later v access the script using **GetComponent**

- GetComponent<Type>, specify the type of component in the Angular brackets.

- can also call *GetComponent* on another game objects.

- always a best practice to call components in Awake or Start function.  

```C#
public class UnityComponent : MonoBehaviour
{
    public GameObject gameObject;
    
    // reference to other scripts
    private AnotherScript anotherScript;
    private YetAnotherScript yetAnotherScript;

    // also set reference to capsule collider component.
    private CapsuleCollider capCollider;
    
    // Awake
    void Awake()
    {
        // takes type of component in the Angular brackets
        anotherScript = GetComponent<AnotherScript>();
        yetAnotherScript = gameObject.GetComponent<YetAnotherScript>();
        capCollider = gameObject.GetComponent<CapsuleCollider>();
    }
    // Start is called before the first frame update
    void Start()
    {
        // set height property of collider, on Start() height is changed.
        capCollider.height = 4;

         // also set the center property
        capCollider.center = new Vector3(1, 2, 1);

        // log the player score
        Debug.Log($"player score is {anotherScript.playerScore}");

        // log the nums of deaths
        Debug.Log($"player death is {yetAnotherScript.playerDeaths}");
    }
}

```

**Screeshots**

![image](./screenshots/component1.png 'image')

![image](./screenshots/component4.png 'image')

---
