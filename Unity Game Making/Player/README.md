## **Step 1: Create the Player (2D Sprite)**

We'll create a simple player character that you can control.

1.  In the **Hierarchy** window, right-click and select:
    `2D Object → Sprites → Square`
2.  Rename this new object from "Square" to **`Player`**.
3.  With the Player selected, look at the **Inspector** window. Find the **`Sprite Renderer`** component and change the **`Color`** to something bright like red or blue. This makes it easy to see.
4.  Now, let's add movement. At the bottom of the Inspector, click **`Add Component`**. Search for and add a **`Rigidbody 2D`**.
5.  In the `Rigidbody 2D` component, set **`Body Type`** to **`Dynamic`** and change **`Gravity Scale`** to **`0`**. This creates a physics object that floats in space (zero gravity).

## **Step 2: Add a Movement Script**

We need to write code to move the Player with keyboard controls.

1.  In the **Project** window, right-click in the `Assets` folder. Select:
    - `Create → Folder`
    - Name the new folder **`Scripts`**.
2.  Double-click the `Scripts` folder. Right-click inside it and select:
    - `Create → C# Script`
    - Name it **`PlayerMovement`**.
3.  Double-click the `PlayerMovement` script to open it in your code editor. Delete everything and paste the code below:

```csharp
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed = 5f;
    private Rigidbody2D rb;

    void Start()
    {
        // Get the Rigidbody2D component on this GameObject
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        // Get input from arrow keys or WASD
        float moveX = Input.GetAxisRaw("Horizontal");
        float moveY = Input.GetAxisRaw("Vertical");

        // Apply the movement velocity
        Vector2 movement = new Vector2(moveX, moveY).normalized * moveSpeed;
        rb.velocity = movement;
    }
}
```
4.  Save the script and go back to Unity.
5.  Drag the `PlayerMovement` script from your `Scripts` folder in the **Project** window and drop it onto the **`Player`** object in the **Hierarchy**.

## **Step 3: Build a Test Room (Walls and Floor)**

Now let's create boundaries so your player doesn't fly off the screen.

1.  Create the **Floor**: In the Hierarchy, right-click and select:
    `2D Object → Sprites → Square`. Rename it to **`Floor`**.
2.  Select the `Floor`. In the Inspector, change its **`Transform`**:
    *   **Scale**: Set **X** to `20` and **Y** to `1`.
    *   **Position**: Set **Y** to `-4`.
    *   In the `Sprite Renderer`, change the `Color` to a dark gray.
3.  Create the **Left Wall**: Right-click the `Floor` in the Hierarchy and select `Duplicate`. Rename the duplicate to **`LeftWall`**.
4.  Select `LeftWall`. Change its **Transform**:
    *   **Scale**: Set **X** to `1` and **Y** to `10`.
    *   **Position**: Set **X** to `-10` and **Y** to `0`.
5.  Create the **Right Wall**: Duplicate `LeftWall` again, rename it to **`RightWall`**, and change its **Position X** to `10`.

## **Step 4: Test Your Game!**

1.  Click the **`Play`** button (▶️) at the top center of the Unity editor.
2.  Use your **Arrow Keys** or **WASD** to move the colored square (your Player) around the room.
3.  Click the **`Play`** button again to stop.

### **If Your Player Gets "Stuck" on Walls:**

We need to make the walls solid. For each wall and the floor (`Floor`, `LeftWall`, `RightWall`):

1.  Select the object in the Hierarchy.
2.  In the Inspector, click **`Add Component`**.
3.  Search for and add a **`Box Collider 2D`**. Unity will add it automatically because they are square sprites. This component makes them solid.

Your basic prototype is now working! You have a controllable player in a contained room.

---

## **Your Immediate Next Tasks (For Today/Tomorrow)**

1.  **Add a "Fuel" mechanic:**
    *   Create a UI `Slider` (GameObject → UI → Slider) and name it "FuelBar".
    *   Modify your `PlayerMovement` script to decrease fuel when moving and recharge it when idle.
2.  **Create a simple enemy:**
    *   Duplicate your `Player`, rename it to `Enemy`, and change its color to red.
    *   Remove the `PlayerMovement` script from it.
    *   Add a new script to make it move slowly toward the player.

Start with these small, achievable goals. The key is to get something working and then build upon it piece by piece.
