# Texture Atlases

Combine multiple images automatically into one large image, called texture atlases, for improving performance.

## Agreements
* Images to be combined into one large image should be placed in one folder.
* The agreed name of the folder should end with '@atlas', like: 'nameOfImage@atlas'.
* The large image is generated in Assets/atlas/nameOfImage.bin after packing.
* Put the original images in Assets/art folder for unified management.
* Use english characters and underscore character for the name of atlas, otherwise the download may fail as it is relied on the web server.

## Workflow of texture Atlases
1. Get art designing resources ready and rename each image according to the demand  
2. Create original folder for the atlas in Project panel: Assets/art/dota@atlas      
    ![folder](images/atlas_folder.jpeg) 
3. Drag the images into this folder:    
    ![add image](images/add.jpeg)   
4. Select the main menu: Tool/Repack Texture Atlases, start to repack all texture atlases   
    ![repack](images/repack.png)    
5. After Packing, atlas is generated at: Assets/atlas/dota.bin        
    ![atlas](images/atlas.jpeg) 

*Note: If original images changed, you need to repack texture atlases by step 4*

<video controls="controls" src="../video/add_atlas.mp4"></video> 
