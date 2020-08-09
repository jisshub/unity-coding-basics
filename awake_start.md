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

## vector maths in unity

### 2d vector

[!image](./screenshots/2dvector 'image')

### magnitude - 2d

[!image](./screenshots/magnitude 'image')

### 2d

[!image](./screenshots/2d 'image')

### 3d

[!image](./screenshots/3d 'image')

### 3d vector

[!image](./screenshots/3dvectors2 'image')

### 3d vector magnitude

[!image](./screenshots/3d 'image')

### dotproduct
[!image](./screenshots/dotproduct 'image')
