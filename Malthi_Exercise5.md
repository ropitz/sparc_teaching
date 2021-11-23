# Exercise 5
## Planning your outputs: Interactions and Platforms
Now that you have your completed reconstruction of Malthi in Blender, you will undoubtedly have a better archaeological understanding of the site and how the structural evidence could have . But what do you plan on doing with this 3D reconstruction? Do you plan on making this accessible to the wider public? What type of format do you think would make this most effective?

You should decide on what format the final output will be before you even begin creating your reconstruction, because this will necessitate certain constraints on the size of your reconstruction (and so may dictate how much decimation must take place in Exercise 3). So how do you decide which method to employ? A good place to start is by considering the approaches other archaeological reconstruction projects have taken. Do you need 2D captures of the 3D reconstruction for paper publications or information boards, as some of [Bob Marshall’s]( ) reconstructions have? Do you plan to produce a fly through video of the reconstruction, as those produced by Open Virtual Worlds for the [Edinburgh 1544]( ) project? Will this be at human eye-level to enable a more ‘lived’ or ‘real’ experience of the site (Watterson 2012) or from a bird’s eye view to feature the surrounding landscape?

Another option is to make the reconstruction navigable through an online platform, either through a 3D viewer like Sketchfab (with informative hotspots attached, like the [Rosewood Cemetery](https://skfb.ly/6YHzR), or without, like the [Nefertari Tomb](https://skfb.ly/6spnS)), or through a photosphere tour website like Roundme (also employed by Open Virtual Worlds to reconstruct the [Moredun Hillfort](https://roundme.com/tour/155618/view/393262) the CINE project’s reconstruction of [St Catherine’s Church in Killybegs, Donegal](https://roundme.com/embed/553737/1812563)). By controlling viewpoints, this can in some cases limit the amount of reconstruction that you need to do.

While not necessary for some of these outputs, like Sketchfab, often game engines are used as a way to house archaeological reconstructions and to make these available to a wider audience. 

- **Unreal:** Open Virtual Worlds uses the Unreal engine to produce [virtual reality experiences, videos and photospheres](https://www.smarthistory.co.uk/Edinburgh1544/about.html). 
- **Unity:** The Villa Livia Reloaded exhibit utilised Unity. In-browser 3D experiences require some knowledge of [WebGL](https://learn.unity.com/tutorial/how-to-publish-for-webgl) (Papadopoulos and Schreibman 2019), but this is needed to create both Unity and Unreal engine-based experiences in browser. Without WebGL, these reconstructions would be limited to desktop interactions, though they can be made downloadable from the internet for installation.
- **Godot:** Other game engines can also be used to create Augmented Reality or Virtual Reality experiences, like the [Godot engine](https://godotengine.org/), but Unity and Unreal’s prevalence means that there are more online tutorials and videos regarding these game engines.
- If working in a team with a software developer, or if you have experience in developing software, you can develop your own in the way that the University of Dundee’s 3DVisLab did for the [SERF Hillforts Project](http://www.seriousanimation.com/hillforts/) (Watterson et al. 2020). 
- There are a number of other 3D visualisation tools that may be useful in certain situations, such as the [3DHOP](https://www.3dhop.net/index.php) viewer, Europeana Pro’s [V4Design](https://pro.europeana.eu/project/v4design) or their [Share3D]( ) web application.

**Think and Respond:** Regardless of which tools, game engines, or websites you utilise to deliver your reconstruction, you need to have a good understanding of what is possible through each of these options. Let’s consider the ‘MoSCoW’ approach introduced in Exercise 2 and add to your Design Document. Examine the example projects above; what features do you see in these examples? Which of these features are ‘must haves’, ‘should haves’, ‘could haves’, and ‘won’t haves’ when you consider your reconstruction of Malthi? For example, do you need transparency options to make it clear which components are your reconstruction, and which originate from 3D records? Do you need to show multiple phases of the site in a single application, and how will you shift between these? How will ambiguity be portrayed? These are all things that need to be considered before the project gets started, and preferably before your first meeting with any project partners.

This exercise will walk you through using the basics of two platforms that you may wish to use for your reconstruction: Sketchfab and Unity. 
## Sketchfab
Sketchfab is a website (purchased by Epic Games in 2021) that allows you to create a free account to upload your 3D models and assets for people around the world to view, download, or purchase. Sketchfab provides a number of features that are particularly useful for archaeologists, especially the ability to add ‘Annotations’; these are markers that you can attach to a specific point in the 3D scene to provide explanatory text. Sketchfab also has its own VR/AR platform available, though it is less flexible when the ‘[ground surface’ is not flat](https://help.sketchfab.com/hc/en-us/articles/211640363-VR-AR-Editor). However, it is important to note that Sketchfab, like all commercial platforms, is **not** an archival solution. Once the data is on Sketchfab, there are no guarantees that Epic Games will preserve your data for any amount of time, nor will they ensure its accessibility; the archival of digital datasets will be addressed more explicitly in Exercise 6.

Before you upload your 3D model to your Sketchfab account, you need to be sure that you are adhering to the file size limits of your account type. For a Basic Free account (as of 2021), you are allowed 10 uploads per month, a file size limit of 100MB per file, and 10 annotations per model. This free account should be sufficient for this project.

Now, let’s look at the export you produced earlier. What size is the file? If you find that it is more than 100 MB, determine how much smaller the file will need to be. One half the size? Three quarters of the size? You may also want to take into account whether you want to create a VR experience or not – Sketchfab recommends that 3D models contain less than 50,000 faces to optimise it for VR, which may be a good benchmark to aim for, but your results may vary. Ideally, you should decide your ideal file size before generating normal maps; you will see in later steps that decimating your model now will affect how well the normal maps sit on the lower-resolution geometry.
### Decimating in Blender
To decimate your 3D model in Blender, first open your Blender project and turn off all layers except for the meshed laser scan data. Ensure it is highlighted in the Scene Collection, then navigate to the object’s ‘Properties’ below, to ‘Modifier Properties’, and select ‘Decimate’.

Next, take note of the total number of faces in your mesh. Right now, it has over 3.5 million faces (highlighted in the red box below). To get to our target of 50,000, we will need to decimate the mesh by using the ‘Ratio’ bar – click on this and type in a number between 0 and 1. 

**Try it yourself!** Try changing the ratio a few times – what do you notice about the quality of your mesh after each decimation? Be sure to turn on the ‘Viewport shading’ (highlighted with a white box below) to see how this affects the quality of your normal map. Are there any obvious differences?

It may take some trial and error, because changing this to 0.014 will not get you 50,000 faces exactly. It turns out that 0.0068 may lead to a better estimation of 50k faces.

However, you may notice that, now that you have decimated the mesh, the normal maps are not interacting with the underlying mesh in the same way. There is now some texture ‘tearing’ or creating a ‘stretched’ effect in some places. If you think back to Exercise 3, normal mapping is essentially ‘painting the detail’ from the high resolution mesh onto your low resolution mesh. By changing the geometry of the low resolution mesh through decimation, faces that would have been ‘painted’ with certain details are now missing, which affects the quality of its appearance. 

Ideally you would avoid these issues by knowing the file size limitations of the platform you want to use to disseminate your output and the number of polys to which the mesh would need to be limited. However, if you were to run into this problem in a real world project, you would need to go back to the individual Blender files you created in Exercise 3, decimate the low-resolution versions of each mesh further, and then re-bake the normal maps onto this lowest-resolution mesh. 

Once you are happy with your decimated mesh and the other components of your reconstruction, you can export these as a single file. Sketchfab will accept a variety of file types, including .FBX, .OBJ, and even .BLEND. Check once again that your file size is less than your Sketchfab account’s upload size limit.
### Upload to Sketchfab

Now you can log into your Sketchfab account and navigate to the ‘Upload’ button. As shown in the image above, you can either drag and drop your finished files to the page, or browse to the files where they are contained. This will now begin to upload and process your files. While waiting, you can begin to make some decisions. If you are on a free Sketchfab account, you will likely need to keep the model ‘Public’, though no one will be able to see the model until you hit the ‘Save & Publish’ button. If you choose to allow ‘texture inspection’, this will allow the public to inspect any the textures you upload with your reconstruction. You can create an informative description to accompany your reconstruction to provide context. You can assign your model a number of categories (including Cultural Heritage & History) and tags to make your reconstruction more easily discoverable via Sketchfab’s search function.

**Think and Respond**: What types of information do you think are important to include in the Sketchfab description for your reconstruction of Malthi? What archaeological information would you include, given the 1024 character limit? What information would you provide about the source of the laser scan data? The paradata/choices you made in creating your reconstruction? Any other information?


### Editing 3D Settings
Now you can edit the reconstruction’s 3D settings, ie. how the 3D model will appear in Sketchfab’s 3D viewer. While there are settings and visualisation tools that may not be relevant to your reconstruction (like the ‘Animation’ tab), there are many that are worth experimenting with that we may not cover. We will, however, go through the basics.

First, under the ‘Scene’ tab, find the ‘Show advanced rotation’ checkbox under ‘General’ and enable it. Even if you exported the Blender file with the wrong orientation, this will be easy to remedy – use the ‘Straighten model’ tool to align your reconstruction intuitively (in this case, the model needed to be rotated by 90 degrees on the X axis). Bring the ‘floor’ of the 3D space (the wireframe rectangle under your mesh) up until it is just below your reconstruction by left-clicking and dragging the blue arrow pointing up.

You may wish to change the background of the scene, either to a pre-set environment, an image, or a basic colour. As long as you have the Renderer set to ‘PBR’, you can also edit the brightness, intensity, and positioning of the lights to simulate realistic lighting.


### Normal Maps/Textures
The next important step is to add your normal maps to your reconstruction so that the detail from the high resolution dataset is still intact. However, each of these must be applied manually and to the correct section of the 3D model. On the ‘Materials’ tab, turn ‘on’ the Normal map. Then, click the drop down arrow highlighted with a red box in the image below, and then ‘Import Textures’. Navigate to the folder where your normal maps are housed and import all of your normal maps.

Now, click on the first subsection of your map (highlighted in yellow below) and select its corresponding normal map from the drop down menu (surrounded with a red box below). It is likely that the normal map will look strange at first  – simply uncheck the ‘flip green -Y’ checkbox and the detail should return to your laser scanned dataset. Repeat this for each subsection of the laser scan data that you have included in your site (this is why it is important to name each of these files sensibly!).



Finally, you may wish to add hotspots to your reconstruction, so that you can provide specific information about individual features, or reasoning behind your reconstruction.

**Think and Respond:** Which features are of note in your reconstruction? Are there specific access routes you identified through the process of reconstruction? Are there certain areas limited to specific activities, like administration, or metalworking? Which of these are particularly important to highlight on the model itself; are some difficult to describe through just the ‘description’ box? Make a list of 5-10 annotations you would like to make on this 3D reconstruction and add it to your ‘Design Document’.
### Annotations
Annotations are notes that you can place in the 3D scene to explain specific features. When a user switches between annotations, the 3D model will rotate and zoom to show the view you selected just before creating the annotation. This can be quite useful when discussing movement through a space or site.

For example, let’s highlight our reconstructed house from Exercise 4 and mention in the annotation that this was based on the reconstruction of a Late Bronze Age house at Tsoungiza. First, navigate your 3D model (left-clicking and dragging to rotate, right-clicking and dragging to pan, and using your scroll wheel to zoom) so that the reconstructed house features prominently in the viewer. Then, double-click where you want your annotation to sit on your 3D model. Notice that in the top left corner, a screenshot of your current position has appeared, and a text box has appeared next to your new annotation. 

Add a title and the necessary information. Note that you can use Markdown syntax to alter your text, like adding a link to the original Tsoungiza reconstruction. Click OK to save your annotation.

After you’ve saved your annotation, notice that the annotation on the left has been updated with this information and formatting. 

If you want to change the view associated with the hotspot, simply create the view in your viewport, then click the small ‘camera’ button next to the annotation to be updated (highlighted with the red box below). This can be an easy way to highlight specific routes/views/pathways without needing a VR application.

After you’ve finished with your model, annotations, and settings in Sketchfab, you can simply press ‘Save Settings’,  move your 3D model to your desired starting position for all viewers and press ‘Save View’. You can either ‘Exit’ to edit your ‘Description’ further, or ‘Publish’ your 3D model.

Your final decision is whether or not you want to make the 3D model downloadable (for free or for a fee) or not. This will largely be decided by the lead members of the project – are there copyright issues to take into account? Is ‘Open Access’ a key underlying principle of the project? Is this designed as part of a fundraising campaign to support future excavations?

Once your 3D model is ready, click ‘Publish’. This is now a shareable 3D reconstruction that can be viewed by millions around the world!

**Think and Respond:** Does the Sketchfab approach seem quite simple? Effective? Does this qualify as interactable? Are there any issues you can think of to use Sketchfab on a long-term basis? Does this approach meet the project aims/requirements set out in Exercise 1? Why or why not?


[Optional Activity] Advanced Outputs: Unity

(Many thanks to Cole Juckette for his help in putting together this part of Exercise 5!)

A more advanced approach to creating an interactive reconstruction of Malthi is to use a game engine, like Unity, to essentially make a walking simulator of the site. Though Sketchfab is a very simple and quick way to get your 3D assets out into the world, Unity offers significantly more freedom in what is possible to create. 

**Think and Respond**: Before you start this optional activity, reflect on your own learning objectives. Do you feel that the additional work and time investment that you will put into learning this new skillset is worth the range of possibilities Unity offers for archaeological reconstructions? Which features offered by Unity (and not offered by Sketchfab) do you think are particularly important for interpreting reconstructed archaeological sites?

You will need to make an account to access the Unity Asset Store, and you can install Unity from this [link](https://unity3d.com/get-unity/download). In the asset store, you will want to find the most up-to-date, free ‘First Person Character Controller’ (preferably made available by Unity Technologies). At the time of writing, this could be found at this [link]( ), but be sure that you familiarise yourself with how the Unity Asset Store functions.

You will also need to make some decisions about how you want your game to appear – do you want the normal maps intact on your laser-scanned datasets, and simply apply a [Mesh Collider](https://docs.unity3d.com/Manual/class-MeshCollider.html)? Or would you prefer to utilise Unity’s [Terrain Engine](https://docs.unity.cn/560/Documentation/Manual/script-Terrain.html) to add more detail to your landscape/reconstruction? 

There are a few things that will need to be prepared before importing everything into a Unity project. First, ensure that the reconstructed assets are exported separately from the laser scanned dataset. Secondly, make sure that your base map is decimated to about 1 million faces or so – this will result in a file size that is around 80 MB. Smaller file sizes mean that your ‘game’ will run more smoothly.

Finally, you need to ensure that most large holes (most of which arise from merging segments of the laser scan data) are filled. Because this involves filling the holes between what used to be two separate ‘objects’, you need to use the ‘Bridge edge loop’ tool instead of just using the ‘Fill’ tool in Blender. This is to prevent your user’s ‘character’ from falling into holes in the terrain.

- In edit mode, select two edges that are close to each other, but belong to the two meshes you are attempting to join. (Do this by holding shift while left-clicking each edge.)

- **Right-click** anywhere in the scene, then select ‘Bridge Edge Loops’ from the menu that appears.
- Repeat this at the other ‘end’ of the hole – you want to ensure that you have created an ‘Open Loop’ between the two meshes. 

- You should now be able to select the loop by holding ‘**Alt**’ **and left-clicking inside or near the edge of the hole**. If it does not select the whole loop automatically, use a series of ‘**Ctrl + left click**’ to build a loop through the ‘Shortest path’ function.

- Finally, use **‘Alt+F’** or right-click anywhere and select the ‘Fill’ tool. 

Once your data is ready, export them into either the FBX or OBJ format. While you can import the entire [BLEND file into Unity](https://docs.unity3d.com/530/Documentation/Manual/HOWTO-ImportObjectBlender.html), at the time of writing this was still less reliable than exporting the files directly.
### Creating a Unity Project
Now that your files are ready, you’ve installed Unity on your computer, and you’ve added the First Person Controller to your Unity assets, you are ready to begin building in Unity.

First, open Unity. You will be greeted with a pop up like the one below (note that this Exercise will be providing examples from version 2020.3.18f1). Choose a 3D Template, name your project and choose where to save it. It will then take some time to create the project.



Now that you have created your blank Unity project, here are a few basic controls you will need to get used to:

- Left click: Select assets
- Clicking and dragging the mouse wheel: Pan
- Right click and drag: Rotate 3D view (not to rotate the 3D model)
- To move/rotate the 3D assets, use the toolbar in the top left corner of the Unity interface:

More of Unity’s controls can be found in its [Documentation here.](https://docs.unity3d.com/Manual/SceneViewNavigation.html)
### Mesh Collider Approach
If you wish to keep your laser scan data looking exactly as it did in Blender, you can add what is called a ‘Mesh Collider’ to your scan data to allow your user to ‘walk’ on the site. First, let’s import your assets.

When Unity opens the 3D Template, you will see a few familiar-looking areas. For one, it has a ‘Hierarchy Window’ much like Blender, where you can find all of the ‘layers’ or individual ‘assets’ in the project. There is a ‘Project Window’ at the bottom of the screen, where you will likely see a sole ‘Assets’ folder. Open the assets folder, and drag your decimated, normal-mapped laser scan data into the ‘Assets’ folder.

Once your 3D data is in the ‘Assets’ folder, you can click and drag it directly into the ‘Scene’ window.

Now, let’s rotate the model so that the surface of the site is pointing up (note that the Y axis is up in Unity). Select the Malthi model and the ‘Inspector Window’ will provide many options. Under ‘Transform’, change the rotation of the X Axis to 270.  

Next, copy over your ‘Structures’ in the same way, and apply the same transformation so that they are roughly aligned with your site.

When we place the structures into the scene, they will not be perfectly aligned with the site. 

- You can use ‘Transform’ to position them in roughly the correct place, but undoubtedly you will still need to use the ‘Move’ and ‘Rotation’ tools (highlighted in the red box below) to place them perfectly. Left-click and drag the arrows to move the features along one axis; the same can be done with the rotational tool (left-click and drag one coloured circle to rotate the 3D data along one axis).
- Like in Blender, you can use the navigational gizmo to align yourself above Malthi by clicking the ‘Y’ cone (highlighted with a blue box below).

Now you may want to add your normal maps to the Unity project – you can either drag all of your normal maps into the Asset folder (like you did with the 3D objects), or create a new folder for them. When you import your normal maps, Unity should automatically identify that they are normal maps, because they were attached to your 3D model in Blender as ‘Materials’; Unity should automatically identify this reference. This triggers a pop up window, with Unity asking if you want to ‘fix’ them – click ‘Fix now’ and these will become associated with your laser scanned data.



If something doesn’t look quite right, you can check the ‘Inspector’ for your laser scanned data – for each dataset that you broke down the original laser scan data into, there will be a specific material slot. If you open this ‘material slot’ as in the image below, you can check that the correct Normal map has been assigned by clicking on the normal map slot (highlighted with a red box) – it will highlight the normal map that is assigned to this material slot in the ‘Assets’ folder.

Now, to ensure that the user will be able to walk on your laser scan data, we need to add something called a ‘Mesh Collider’. This will ensure that the laser scan data is treated as a ‘solid surface’, enabling characters to ‘collide’ with the site data. To add a Mesh Collider to your laser scan data, ensure that your mesh is highlighted and its details are visible in the Inspector. In the Inspector window, scroll all the way down to the ‘Add Component’ option. Then, search for the ‘Mesh Collider’ component, as shown below. Select Mesh Collider, and it will be added to the list of components (likely above the material slots). Once this is applied, check the ‘convex’ box. This process may take some time to complete.


At this point, you have now converted your laser scan data into a ‘solid surface’ for your users to (eventually) navigate! If you are happy with this, skip to the ‘Adding the First Person Controller’ section below.
### Terrain Engine Approach
If, instead of wanting to keep your normal maps, you want to work with Unity’s ‘[Terrain Engine](https://docs.unity.cn/560/Documentation/Manual/script-Terrain.html)’, you will first need to convert your laser scan mesh into a ‘Terrain’. Unfortunately this is not an inbuilt function in Unity, so you will need to download the ‘[Object2Terrain](https://www.mediafire.com/file/3oyvdjcjix2d3iu/Object2Terrain.cs/file)’ script. While it is not recommended that you download scripts from sketchy sites, this particular script is recommended by a wide variety of online tutorials (and me). 

- Once you have acquired this script, right click in your Assets folder and ‘Create > Folder’. When you name this folder, name it Editor – ensure it has a capital E and that you’ve spelled it correctly, otherwise the script will not work.

- Open the newly created Editor folder, then click and drag the ‘Object2Terrain’ script into the Editor folder.

- Unity will then ask if you consent to the script updating – say yes to these and other pop ups that might appear.

- Once this has completed, note that there is a new menu item added to Unity called ‘Terrain’. This has been added by the script.

- Now add your assets – Open the main Assets folder, and drag your decimated laser scan data into the ‘Assets’ folder.
- Drag your mesh from the ‘Assets’ folder into the 3D Viewer.
- With your mesh  highlighted, rotate the model so that the surface of the site is pointing up (note that the Y axis is up in Unity). The ‘Inspector Window’ will provide many options. Under ‘Transform’, change the rotation of the X Axis to 270.  
- Take note of the grid that you can see in the scene – to create a terrain, you want your original mesh to be located above the grid. Use the ‘Move’ tool – drag up on the arrows that appear on the mesh until the grid lines are clearly positioned below the mesh.


- Once you are certain the mesh is positioned above the grid, ensure that the laser scanned mesh is highlighted. Then, navigate to the ‘Terrain’ drop down menu, and select ‘Object to Terrain’.

- Selecting ‘Object to Terrain’ will prompt a new dialog box to appear. It asks for you to set the resolution of your terrain (the example mesh has been set to 1080), along with a few other options. Ensure that ‘Bottom Up’ is selected, as the script will prompt Unity to extrude a mesh to match the current elevation of your mesh (essentially, it will project a terrain mesh upwards from the grid, until it matches/adheres to the contours of your decimated mesh).
- It is important that you do not exceed 2000 for any of the values in this dialog box, as this may cause the software to crash.

- After the script completes, a new mesh will appear in the 3D viewer (likely in a check-box texture, as shown below). This is your new terrain, derived from your decimated mesh. This will now enable you to easily apply textures to your mesh and to use the [Terrain tools](https://docs.unity.cn/560/Documentation/Manual/script-Terrain.html) built into Unity’s interface.
- Now, add your structures to the Assets folder like you did with the original mesh. Drag these into the 3D viewer and align it with your Terrain. 

- Make sure you save!
### Adding the First Person Controller
Whether you decided to go with the ‘Terrain’ or the ‘Mesh Collider’ approach to creating the floor of your experience, you can now add your user’s first-person player character. To do this, navigate to the ‘Window’ option and select ‘Package Manager’. (Note: The following instructions assume that you have added a first person player controller from the Unity store, as outlined at the start of this exercise.)

In the Package manager, change the ‘Package’ drop down menu to ‘My Assets’ (highlighted with a red box below). From here, choose ‘Starter Assets – First Person Character Controller’ and click ‘Import’ in the bottom right hand corner (highlighted with a blue box below).

Unity will then take some time before coming up with another pop up as shown below, click import again.

Unity will then take some time to add these components to your project. After some time, a new pop up will appear, asking if you want to enable backends. Click YES, which will cause Unity to do some more processing, and then will restart completely. 

Be sure to save!

- The Starter Assets have now been added to a new folder called ‘Starter Assets’. In this folder, navigate to the ‘FirstPerson’ folder by double-clicking.

- Then navigate to the ‘Prefabs’ folder. You will want the ‘Nested Parent’ asset. Like you have done with the others, click and drag the controller in, but be sure that you position it somewhere above the site. If you need to reposition it, you will need to zoom out significantly to find the ‘move’ interface on screen.

- Take some time to examine the individual components of the ‘Nested Parent’ character – you can do this by clicking the arrow next to it in the ‘Hierarchy’ window. 
  - Essentially, the capsule acts as the ‘player’, which houses the main camera, which is then directed to ‘follow the player’. There is also the on-screen interface.
  - Because there is a camera incorporated into the capsule, we do not need the additional ‘main camera’ that the 3D template started us out with. Go back to the main hierarchy list and delete the ‘Main Camera’ there.

- Now it is time to test your experience! Above your 3D viewport, you may have noticed a ‘play’ button. Press the play button to begin.

- You will now take control of your ‘player capsule’. Move your character in the viewport much like you would most PC games: use the ‘WASD’ keys to move the character, move your mouse to change where your character is looking. The space key will cause the character to jump, and holding a ‘Shift’ key will cause your character to run.

- If you want to exit the ‘test’ phase, hit the ‘Esc’ key to make your mouse visible again, then press either the ‘pause’ button, or press ‘play’ again to reset the position of your first person player controller.
- If you want to change how quickly your character can move, or to change its height, open the ‘Nested Parent’ layer in the Hierarchy window and highlight the ‘Player Capsule’. Under ‘First Person Controller (Script)’, you will see a number of options that you can change. 
  - Be sure to test after each of these changes you make to see how it affects the experience, because it can cause some problems.  For example, if you make it so that your character can move quite quickly, this may cause the camera to ‘clip through’ the player capsule.

**Try it yourself!** You may have noticed that your character is currently able to move through the walls of your reconstruction. How would you ensure that your player character collides with these structures?

Now that you have the basics in place, you can add further detail. If you went with the ‘Terrain’ option above, you can easily add a ground texture (after adding it to your assets through the asset store, or by downloading a texture from online and dragging it into your assets). Select your ‘Terrain’ in the hierarchy, then under ‘Terrain’, click the gear image. Under the ‘Basic Terrain’ settings, you can set its ‘Material’ to your preferred texture.

If you have instead chosen to keep your normal maps intact, you will already have all of the detail from the original laser scan data preserved.  Adding additional textures may occlude those details, but you may wish to add some sort of colour. This is slightly more complicated than the steps above, as you will need to ‘unpack materials’ from the 3D model [to make them editable](https://docs.unity3d.com/Manual/StandardShaderMaterialParameterNormalMap.html), and then manually reassign your normal maps to each segment again, even if you did this in the steps above. You will need to do this regardless of whether you exported your site map as an OBJ file or FBX file. 

- To make your materials editable, click on your original mesh in the ‘Assets’ folder below (highlighted with a red box) so that the Inspector displays the materials information. Create a Materials folder, then click ‘Extract materials’ from the Inspector (highlighted with a blue box). From the pop up menu, select your materials folder. 

- Once the materials are unpacked, click on your mesh in the scene twice to open all of the options available in the Inspector tab. You will now see a Materials drop down menu under ‘Mesh Renderer’ that are interactable. Double-click on one of the materials to open the inspector for that material (highlighted with a red box below).

- If you haven’t already, ensure that your normal maps are also imported into the Unity project (preferably in the same folder as your unpacked materials). Begin assigning normal maps to the corresponding material. If you did not name your material slots in Blender, it is likely that this will not be immediately clear which normal map belongs to each material. To simplify this, change the colour of the material by clicking the box next to ‘Albedo’ in the Material inspector and pick a colour (highlighted with a blue box below). As long as you named your mesh sub-sections in a structured way, it should be easy to find the corresponding normal map for the section that has had its colour changed. Click the circle next to ‘Normal Map’ (highlighted with a red box below) and assign the correct file. It should be immediately apparent if the normal map is the correct one, as your details will appear.

**Note:** Unity may not recognise that these are Normal maps upon import (especially if you are working with an OBJ file). Simply click on the normal map and change (or if you assign a normal map to a material, it will ask if you want to fix this now and do it automatically). 

- To make future changes easier, be sure to rename the Material to match its corresponding Normal Map after you have identified it, by right-clicking on the Material in the folder and selecting ‘Rename’. You can then experiment with different settings for each material by adding textures or  colour until you get the look you want for your site.

**Think and respond:** What other details can you add to your reconstruction? What is necessary to address the aims of the project? Other textures? Should the light source in the scene be positioned in a certain direction (where would the sun be above the actual site of Malthi during the morning? The afternoon? The evening?) As you test your experience, what is missing? Do you need to add a bounding box to ensure your users cannot fall into the ‘void’? What about sound?

While this tutorial has introduced you to a few of the basics behind creating a digital walkthrough of your reconstruction of the site of Malthi, there are many other things you would need to consider to create a truly engaging and immersive experience. Because Unity is widely used, there will more than likely be a YouTube video demonstrating how to add whatever functionality you may want to add. However, you may need to reframe your archaeological queries into a more general or videogame-inclined query before pursuing it. For example, if you wanted to add multiple phases of activity to your site, searching for this may not yield too many results. If you instead reframe this as ‘how to allow players to change between Scenes in Unity’, you may find more useful results about triggers or interfaces to incorporate into your project.

Now, how will your Unity project be made available? There are a number of options for you to explore if you navigate to ‘File>Build and Run’, as shown below. If you want to publish it on a website, you will likely need to publish it for WebGL – Unity provides a tutorial specifically for this [here](https://learn.unity.com/tutorial/how-to-publish-for-webgl). 

**Thinking about going further**

You may also want to produce an AR or VR application to allow for a fuller exploration of your reconstruction, like the [Villa Livia Reloaded](http://www.v-must.net/villa-livia-reloaded) gesture-based VR exhibit. These can get quite complex, though the Cine project has produced a series of toolkits to make the construction of these more accessible. Their VR toolkit is available [here](https://cineg.org/toolkits/3d-exhibits/). Photosphere exhibits, like those hosted at Roundme, can be employed as VR experiences as well, just with hotspot navigation. You could adapt your project in [Unity to a VR output]( ), or you could use something completely different, like [Aframe](https://aframe.io/). However, whether this would be a useful output for your project will be determined by the project aims, the budget available, the planned use for this application (will you be demonstrating the application at conferences/outreach events? How many headsets do you need to have available?), and the amount of time available to complete it.

**Think and respond:** Now that you have basic experience with both approaches, given the requirements/parameters of the project set out in Exercise 1, do you think that Sketchfab or Unity would be a better output? Why have you made that choice? What are the benefits of using Sketchfab, despite its limited functionality? What are the benefits of Unity, despite the amount of learning and time it takes to create an engaging experience?
## Resources for Exercise 5
### Reconstruction Output examples:
- Ed González-Tennant’s Rosewood Cemetery on Sketchfab: https://sketchfab.com/3d-models/virtual-rosewood-cemetery-3cbb80a2442042818b2759281e9985e8
- Bob Marshall’s Portfolio of 2D Renders: <https://www.artstation.com/artwork/48RWl2>
- Cine’s Roundme of St Catherine’s Church and Graveyard Reconstruction, Co. Donegal Ireland: <https://roundme.com/embed/553737/1812563>
- Villa Livia Reloaded: <http://www.v-must.net/villa-livia-reloaded>
- Open Virtual Worlds: 
- Edinburgh 1544: [https://www.smarthistory.co.uk/Edinburgh1544/16th_Century_Edinburgh.html?fbclid=IwAR0ZD_nbChSMqO0D6giTQB2JR6BA_gCMo0XghL8TnA_IUgXZ9-RIfsAxXmQ]( )
- Moredun Top Hillfort, 50 AD: [https://roundme.com/tour/155618/view/393262/]()

### Applications to Disseminate Reconstructed Outputs 
- 3DHOP: <https://www.3dhop.net/index.php> 

Marco Potenziani, Marco Callieri, Matteo Dellepiane, Massimiliano Corsini, Federico Ponchio, and Roberto Scopigno. 2015. 3DHOP. Computers and Graphics. 52, C (November 2015), 129–141. DOI: <https://doi.org/10.1016/j.cag.2015.07.001>

- A-frame: [https://aframe.io/]()
- Europeana Pro: <https://pro.europeana.eu/project/v4design>

<https://pro.europeana.eu/project/share3d>

- CineG: 

<https://cineg.org/toolkits/3d-exhibits/>

Godot Engine: <https://godotengine.org/>

Sketchfab: https://help.sketchfab.com/hc/en-us/articles/211640363-VR-AR-Editor
### Further Reading
Papadopoulos, C. and Schreibman, S. 2019. Towards 3D Scholarly Editions: The Battle of Mount Street Bridge. *Digital Humanities Quarterly.* 13(1): 31-57. <http://www.digitalhumanities.org/dhq/vol/13/1/index.html>.

Plaksin, Andrey: [https://sketchfab.com/3d-models/the-tomb-of-nefertari-3d-vr35-v0-73-90034cbe58904828a11429395cef9125]( )
### Watterson, A, Anderson, J & Baxter, K 2020, Designing Digital Engagements: Approaches to creative practice and adaptable programming for archaeological visualisation. In Proceedings of EVA London 2020. <http://www.seriousanimation.com/hillforts/>

### Unity-specific Resources
- Object2Terrain Script download: https://www.mediafire.com/file/3oyvdjcjix2d3iu/Object2Terrain.cs/file

Unity User Manual 2020.3 (<https://docs.unity3d.com/Manual/index.html>)

- [https://assetstore.unity.com/packages/essentials/starter-assets-first-person-character-controller-196525]( )
- Importing from Blender: https://docs.unity3d.com/530/Documentation/Manual/HOWTO-ImportObjectBlender.html
- Mesh Collider: <https://docs.unity3d.com/Manual/class-MeshCollider.html>
- Normal Maps: [https://docs.unity3d.com/Manual/StandardShaderMaterialParameterNormalMap.html]( )
- Terrain Engine: <https://docs.unity.cn/560/Documentation/Manual/script-Terrain.html>
- <https://learn.unity.com/tutorial/how-to-publish-for-webgl>
### YouTube Videos Utilised:
- de Byl, Penny. 2018. “FBX Importing to Unity 2017/2018+ | Where did my textures go?” *Youtube*. Uploaded by Holistic3d, 25 January 2018, [https://www.youtube.com/watch?v=xOeodlLTx8g]().
- [Imphenzia](https://youtube.com/playlist?list=PLC7nmYI-cbT1uGmB9_D74VIUh7qN_YsH5).  2020. “LEARN UNITY - The Most BASIC TUTORIAL I'll Ever Make”. *YouTube*. Uploaded by Imphenzia, 24 July 2020, [https://youtu.be/pwZpJzpE2lQ]().



