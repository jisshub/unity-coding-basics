# Destroy Objects 

- we can destroy the objects from the scene in play mode

```C#
public class DestroyThis : MonoBehaviour
{

    public GameObject otherObject;
    // Update is called once per frame
    void Update()
    {
        if(Input.GetKey(KeyCode.Space))
            Destroy(otherObject);
    }
}
```

- here v can drag the object to be destroyed on otherObject field in inspector.
- later v press the spae bar to fnally remove it while playing.

- Can also destroy the component from the game object.
- for example, mesh renderer component attached to a game object.


```C#
public class RemoveComponent : MonoBehaviour
{

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.T))
        {
            // here v remove the mesh rendeere component of the corresponding game object on pressing t.
            Destroy(GetComponent<MeshRenderer>());
        }
    } 
}

```

**Screenshot**

![image](./screenshots/destroy.png 'image')

- in above image, we add the *Destroy This* and *Remove Component* Script to *Destroy* Game object.

---
