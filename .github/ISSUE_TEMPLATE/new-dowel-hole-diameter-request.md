---
name: New Dowel Hole Diameter Request
about: Use this form if your dowel pin tolerances are not compatible with the available
  sizes.
title: "[Dowel Diameter Request]"
labels: enhancement
assignees: ''

---

**Before you request!**
To ensure a good fit, please create and print a test part with the hole diameter you are requesting. You can do this directly in your slicer using the guidance below. 

**What hole diameter would you like to request?**
Ex. 6.5mm

---

# Creating a test part in Bamboo Slicer #

## Step 1: Create a 20mm Cube

1. Open **Bambu Studio** and ensure you are in the **Prepare** tab.
2. Right-click anywhere on the empty build plate.
3. Hover over **Add Primitive** and select **Cube**.
4. Click on the cube to select it, then press the **Scale (S)** key (or click the Scale icon in the top toolbar).
5. In the scaling menu on the screen, **uncheck the "Uniform Scale" box** (the lock icon).
6. Enter **`20`** into the **X, Y, and Z** dimension boxes. You now have a perfect 20mm cube.

## Step 2: Add the Hole (Negative Part)

1. **Right-click** on your 20mm cube.
2. Hover over **Add Negative Part** and select **Cylinder**.
> *A translucent, reddish cylinder will appear inside or near your cube, representing the volume that will be carved out.*

## Step 3: Size the Hole to Your Specific Diameter

1. Look at the left-hand sidebar and switch from the **Global** tab to the **Objects** tab.
2. Click the small arrow next to your Cube to expand its components, then click on the **Negative Volume-Cylinder** listed underneath it.
3. Press the **Scale (S)** key.
4. **Uncheck "Uniform Scale"** so you can change the height and diameter independently.
5. Set your dimensions:
* **X and Y:** Enter your specific hole diameter in millimeters (e.g., for a 6.4mm diameter hole, type `6.4` in both X and Y).
* **Z (Height):** Enter **`25`**. *(Setting this to 25mm makes it taller than your 20mm cube, ensuring a clean through-hole).*

## Step 4: Position and Center the Hole

1. With the **Negative Volume-Cylinder** still selected in the Objects tab, press the **Move (M)** key.
2. In the coordinate box that appears on your screen, change the coordinate dropdown from **World** to **Local**.
3. Set the **X** value to `0` and the **Y** value to `0`. This centers the hole perfectly inside your 20mm cube.
4. Set the **Z** value to `0` as well. Because the cylinder is 25mm tall and the cube is 20mm tall, this will make the cylinder stick out by 2.5mm on both the top and bottom.

## Step 5: Slice and Verify

1. Click the **Slice Plate** button in the top right corner.
2. The software will automatically shift to the **Preview** tab.
3. Drag the vertical layer slider on the right side of the screen downward. You will see the toolpath preview showing a solid $2\text{ cm}$ square outline with your specified circular hole perfectly hollowed out through the center.
