# Awake and Start functions

- Start and Awake called at once in the lifetime of a script
attached to an object.

```C#
public class AwakStart : MonoBehaviour
{
    // Start is called before the first frame update
    void Awake()
    {
        Debug.Log("Awake called before Start");
    }

    // Update is called once per frame
    void Start()
    {
        Debug.Log("Start called after Awake");
    }
     // Update is called once per frame
    void Update()
    {
        Debug.Log("Called on every frame");
    }

    void FixedUpdate()
    {
        Debug.Log("called every physics steps");
    }
}
```

- Here in console, Awake() is printed first, precerding Start function.
