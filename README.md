# Blend
## Pipeline Steps

| Step | Image |
|------|-------|
| Foreground with background | ![](deadpool.jpg) |
| Background Removed | ![](person_no_bg.png) |
| Binary Mask | ![](person_binary_mask.png) |
| Background Scene | ![](wallpaperflare.com_wallpaper.jpg) |
| Composite (with shadow blending)| ![](deadpool_final_with_shadow.png) |

## How It Works
1. **Background Removal**

    The foreground image (with its original background) is processed using rembg, which automatically removes the background.

    The result is a transparent cutout of the object, along with an alpha mask that defines the object's shape.

 2. **Mask Extraction**

    From the cutout, a binary mask is generated.

    This mask is essential for guiding blending and harmonization steps.

 3. **Vanishing Point Estimation for Foreground Placement**
    
     ![image](https://github.com/user-attachments/assets/6a4adb99-6ce5-47d9-aa57-ac5457024396)

    Before compositing, the vanishing point or scene perspective of the background image is analyzed to determine the correct scale and placement of the foreground object.
   
    By aligning the foreground with the background’s perspective lines, then the character is placed in a geometrically according to the lines
   
 4. **Image Blending**

    After harmonization, the foreground is blended into the background using advanced image blending techniques like Poisson blending and alpha blending.

    This ensures the edges of the object transition smoothly into the background without visible seams or artifacts.


