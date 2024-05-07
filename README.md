# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new plane and create a cube and give color for the cube.

Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.

Step 6:
Next Create a another new scene named as page2.

Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

Step 8:
Click the Build and run button in the Build settings and run the scene.

Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

## Program:
NAME: M.CHANDRU

REG NO: 212222230026
## PLAYERCONTROLLER
```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class playercontroller : MonoBehaviour
{
    // Start is called before the first frame update
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "sphere")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
Output:
![Screenshot 2024-05-06 114327](https://github.com/chandrumathiyazhagan/Ex06-Redirecting-the-Scene/assets/119393023/911b93b7-abcc-4e83-8c74-b24a02f18d50)

![Screenshot 2024-05-06 114247](https://github.com/chandrumathiyazhagan/Ex06-Redirecting-the-Scene/assets/119393023/af6c036b-c6aa-4c57-a726-2917111463f0)

Result:
The above C# coding is successfully redirecting the scene in the unity engine.
