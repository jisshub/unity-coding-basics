# Translate And Rotate Functions in Unity

- in translate objects moves in m/s.

```C#

public float moveSpeed = 10f
void Update(){

    transform.Translate(Vector3.forward * moveSpeed * Time.deltaTime);
}

```

- here **Vector3.forward** is the unit vector defined by (0, 0, 1)

- it is a shorthand for **Vector3(0, 0, 1)**.

- **Time.deltatime** - This property provides the time between the current and previous frame.

- *moveSpeed=10f* - frame speed. which f stands for float. 

---

```C#
public class TransformObject : MonoBehaviour
{

    public float speed = 10f;
    public float rotateSpeed = 40f;

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKey(KeyCode.UpArrow))
        {
            // on pressing up arrow key, move forward
            transform.Translate(Vector3.forward * speed * Time.deltaTime);
        }
        if (Input.GetKey(KeyCode.DownArrow)) 
        {
            // on pressing down arrow key, move backwards
            transform.Translate(-Vector3.forward * speed * Time.deltaTime);
        }

        // Rotate function 
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            // ON PRESSING LEFT ARROW KEY,  OBJECT ROTATES TO RIGHT
            transform.Rotate(Vector3.up, -rotateSpeed * Time.deltaTime);
        }
        if (Input.GetKey(KeyCode.RightArrow))
        {
            // ON PRESSING LEFT ARROW KEY,  OBJECT ROTATES TO LEFT
            transform.Rotate(Vector3.up, rotateSpeed * Time.deltaTime);
        }
    }

}
```

---
