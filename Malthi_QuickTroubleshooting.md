# Quick Troubleshooting

The following provides a quick reference for common issues encountered during these exercises.

## Exercise 1
### I've tried segmenting a cloud, but nothing seems to be happening?
Make sure that you have the correct cloud selected/highlighted in the 'DB Tree', then try segmenting the point cloud again.

### CANUPO doesn’t seem to be classifying the vegetation correctly – how can I increase its accuracy?
Because CANUPO is a machine learning algorithm, it may need more samples to correctly differentiate between stone and vegetation. Try adding more samples from different parts of your segmented dataset. 

It could be that by subsampling your dataset too much, your clumps of grass are no longer distinctive enough to be correctly identified (try this – can you still identify that something is grass? Try turning on the dataset with the original density of points – is it much clearer?). Applying CANUPO to an un-subsampled point cloud will undoubtedly cause the software to crash, so it may be better to try subsampling the point cloud a bit less.

If you are still having trouble, try calculating roughness under ‘Tools > Other > Compute Geometric Features’, as instructed in Step 3 of Exercise 1. By setting this as a Scalar Field, it should be easier to identify vegetation features to add to the classifier.

## Exercise 3
### I’ve reopened my Blender file and the normal map is missing – what happened?
Did you move your normal maps or other files to a different folder? If so, it is likely that this is caused by directory issues – move the files back to their original folder and reopen your Blender file. It is important to create a clear file structure from the beginning, as directory issues commonly crop up in specialised software. If this does not fix the issue, check when the last save took place – was it before or after the Normal map was generated?
### I can’t find the mesh I just imported into Blender, where is it?
First, try zooming out in Blender. You should be able to click and drag the magnifying glass icon on the right side of the screen. If it is still not visible, think back to Exercise 1; did you check ensure that the check box next to the ‘Preserve Global Shift on Save’ was **unchecked**? If you aren’t sure, reopen your problematic mesh in CloudCompare, and if you preserved its original geospatial coordinates, it will again prompt you with the same dialog box.
### I’ve tried importing my tiled meshes into the same Blender file, and they aren’t aligning correctly?
Is this one tile that is not fitting into its projected place? Did you move one of the meshes to new coordinates in Blender? Try importing the tile’s original CloudCompare export (or the archived obj) into the Blender file you are reassembling the site map in – does it fit into the correct space? 

If it is many of the tiles that are not aligning correctly, did you ensure that you used the same ‘Global Shift’ coordinates for each tile in Exercise 1?
### I created my Normal map, but it doesn’t look right. What went wrong?
First, try hitting ‘Viewport Shading’ in the 3D Viewport with only the decimated mesh visible to see if the detail has been mapped on. If not, you may need to start over and try to follow the steps again. 

- Make sure that you have ‘Applied All Transforms’ for each the low-resolution and high-resolution meshes – this will often cause issues with reality captured data. 
- If that doesn’t work, use Smart UV Project rather than creating your own islands at first – this can cause issues too. 
- Make sure that your nodes are aligned correctly. Be sure that your Image Texture is set to ‘Non-Colour’ space. 
- If none of these things make a difference, ensure that you have highlighted the correct nodes and layers in the correct order before baking the normal. 

### I’ve tried putting all of my meshes together, and it’s causing my computer to lag. What can I do?
Are there some tiles that are much larger than the others? You may need to re-decimate these meshes (though try doing this with Blender’s inbuilt decimation tool first – see directions at the beginning of Exercise 5). Note that this can cause issues with your normal maps though.

## Exercise 4
### Why won’t my house roof extrude in a straight line?
As mentioned in the exercise, modelling becomes more complicated when working with imperfect shapes (ie our houses that are snapped to foundation corners, rather than regular primitive proportions (1x1x1)). Try to change your view on the house, then freehand extrude the peak of the roof to what looks like the correct position. 

If you find this difficult, you can try to adapt a prefab house onto real-world coordinates instead. However, it may be more difficult to assign all of the vertices of one corner to the edge of a real-world foundation.
### I deleted X and now it’s ruined!
Remember that **Ctrl+U** is the shortcut for undo!

## Exercise 5
### I noticed something that needed editing after exporting my reconstruction, but after I edited and then re-exported the file, it didn’t save the changes. What’s happening?
Overwriting exports causes issues in Blender. Try re-exporting it and assigning it a new file name. 
### I decimated my mesh further and now my normal maps don’t look right. What can I do?
Unfortunately you probably need to re-calculate the normal maps if you need your mesh decimated to this extent. If you think back to Exercise 3, normal mapping is essentially ‘painting the detail’ from the high resolution mesh onto your low resolution mesh. By changing the geometry of the low resolution mesh through decimation, faces that would have been ‘painted’ with certain details are now missing, which affects the quality of its appearance.
### In Unity, my character keeps falling through holes in the map!
There is probably a gap between two subsections of the laser scan data – be sure to follow the steps regarding Bridging Edge Loops at the start of the Unity tutorial in Exercise 5.
### Blender won’t let me create a full edge loop to fill a hole – what do I do?
There is probably a bit of weird geometry or a break that is not allowing for the creation of a coherent edge loop. If there is significant gap between the two meshes near the hole, create another bridge loop in this area and fill the gap; repeat this as necessary, and you will eventually fill the hole bit by bit, rather than filling it as one large hole. 
### I’m not sure that my reconstruction is to scale in Unity! How do I check?
While everything should be to scale after being exported from Blender, you can check by creating a 1m x 1m x 1m 3D primitive in the Unity scene, or scale it to the same size as one of your reconstructed walls. In the example below, the wall is set to be 2.7m tall in Blender on the left; the same wall is pictured in Unity on the right. After scaling the sphere to 2.7 m in Unity, it is clear that the reconstructed elements are at the same scale as they were in Blender.

### My first person controller isn’t working!
Check which version of the first person controller you have installed. If you mistakenly added the ‘Standard Assets for Unity 2018.4’ package, this first person controller will not work correctly in more recent versions of Unity. As of the time of writing, ‘Starter Assets – First Person Character Controller’, added to the Unity asset store on June 09, 2021, should be the asset you want to use here. Check if there are more recent versions on the Unity store.
### When I test the First Person controller, the camera clips through the player capsule/I can see green lines. How do I fix it?
First, ensure that the ‘Nested Parent Unpack’ asset is selected, then change the Y axis to a slightly lower value. You can also try to change the position of the nested camera, or change the maximum speed that your player character can achieve. 
### I can’t add textures to my mesh in Unity?
Unpack the materials of your mesh, as instructed at the end of [Exercise 5 Part B](/Malthi_Exercise5_B.md). They need to be unpacked to be editable. Use Prof Penny de Byl’s video for further instruction.
