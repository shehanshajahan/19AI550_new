# Ex.No: 4  Implementation of Kinematic movement -seek and Flee behavior in Unity
### DATE: 24/07/2026                                                               
### REGISTER NUMBER : 212223240154 
### AIM: 
To write a program to simulate the process of seek and Flee behavior in Unity without NavigationMeshAgent. 
### Algorithm:
1. Create a New Unity Project by Open the  Unity Hub and create a new 3D Project,Name the project (e.g., SeekBehaviorDemo).
2. Create the Moving Object
   In the Hierarchy, right-click → 3D Object → Cube (or Sphere).
   Rename it to Seeker and Reset its position:Select the Seeker, go to Inspector → Transform → Set Position to (0,0,0).
3. Create the Target Object
   Right-click in the Hierarchy → 3D Object → Sphere (or any other shape).
   Rename it to Target. Move it away from Seeker, e.g., set Position to (5, 0, 5).
   Select the Target, add a Material, and change the color. (if needed) 
4. Adding the Seek Behavior Script
   Create the Script-In the Project Window, go to the Assets folder.
   Right-click → Create → C# Script.
5. Write a script for seek behavior and save it
6. Attach the Script
   Select Seeker in the Hierarchy - Drag & Drop the SeekBehavior script onto the Inspector Panel.
   Drag & Drop the Target from the Hierarchy into the "Target" field in the script component.
12.  Write a script for flee behavior and attach it to target
13.  Run the game
14. Stop the program
    
### Program:
```
using UnityEngine;
using System.Collections;
using System.Collections.Generic;

public class seekflee : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    public Transform target;
    public Transform f;
    public Transform s;
    private float speed = 0.2f;
    void Start()
    {
        print("Welcome");
    }

    // Update is called once per frame
    void Update()
    {
        // seek script
        Vector3 dir = (target.position - s.position).normalized;
        s.position += dir * speed;
        //flee script
        Vector3 dir1 = (f.position - target.position).normalized;
        f.position += dir1 * speed;
    }
}
```
### Output:
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/8fdcc40f-8374-4197-a6d5-d577669477a1" />
<img width="1919" height="1017" alt="image" src="https://github.com/user-attachments/assets/c3936e42-5741-45e4-91e0-68193a111499" />










### Result:
Thus the simple seek behavior was implemented successfully.
