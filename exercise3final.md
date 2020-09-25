**Exercise 3: The Basics of CloudCompare**

**(Allow at least 1 hour for Exercise 3)**

Meshlab allowed us to quickly visualise the datasets and take simple
measurements from the 3D models to familiarise ourselves with the
dataset. To take our analysis to the next step, we will use a different
software tool which is more intuitive and has better functionality for
isolating individual features, CloudCompare. In this exercise you will
learn to:

-   ***Isolate individual mesh components for closer analysis;***

-   ***Organise data by renaming meshes and save our CloudCompare
    project;***

-   ***Align 3D data to enable more accurate morphometric
    calculations;***

-   ***Implement the visualisation options in CloudCompare, in this case
    by using simple 'morphometric parameters' from the mesh surface as
    Scalar Fields.***

**Using Cloud Compare**

CloudCompare is another free software package that is useful in working
with and analysing 3D datasets. Only a few basic functions will be
discussed here, but [CloudCompare\'s User's
Manual](https://www.danielgm.net/cc/doc/qCC/Documentation_CloudCompare_version_2_1_eng.pdf)
is virtually comprehensive in describing its many uses. In some ways, it
is more intuitive than MeshLab, although creating a visualisation as
informative as the 'Radiance Scaling' shader from MeshLab in
CloudCompare requires more work.

One big difference between CloudCompare and Meshlab is that, while you
can work with 3D meshes in CloudCompare, the software was initially
designed to work with **point clouds**, as the name 'CloudCompare'
suggests. As described above in the introduction of this document, the
point cloud is the cluster of individual points that are recorded by a
3D recording technique, whether this was by photogrammetry, structured
light scanning, or laser scanning. Some of CloudCompare's functions will
use the **vertices** of the mesh as 'point clouds'. This will be
particularly important in Exercises 4 and 5.

***What is a 'morphometric parameter'? What do they tell us?***

Morphometric parameters are quantitative measurements that can be used
to describe an object's form. This includes measurements you will
already be familiar with (length, width, volume), but can also include
parameters like 'Roughness' or 'Curvature'. By incorporating these
parameters, features that would otherwise be difficult to see on the
physical object become much more obvious when applied to the 3D model.
In Exercise 3, we will begin with using the Z coordinates, which
represent the relative height of the mesh surface.

>**Shaders vs Morphometrics** While they can both be used to visualise data, **Shaders** function differently from **Morphometric Parameters**. As noted above in Exercise 1, Shaders take multiple factors into their calculation, including: lighting position and transparency, view position, material properties, and the shape of the 3D surface. Morphometrics are simpler in that they only take into account the shape of the 3D surface; however, there are a wide variety of morphometric parameters that can be used  in morphometrics (height, length, width, roughness, curvature) and can be used in quantitative applications, which will be explored more fully in Exercises 4 and 5.

>**Roughness and Curvature** ‘Roughness’ and ‘Curvature’ are calculated using statistics. As defined by CloudCompare…
>-   Roughness: “For each point, the 'roughness' value is equal to the distance between this point and the best fitting plane computed on its nearest neighbours.”
>-   Curvature: “The curvature at each point is estimated by best fitting a quadric around it based on its nearest neighbours.”

>Both of these calculations rely on a ‘nearest neighbours’ approach. While this concept can be applied differently in different fields, essentially the software determines whether a point is ‘different’ by looking at its neighbours within a given radius defined by the user. If a point’s elevation is quite similar compared to the plane formed by its neighbouring points, it will not be attributed to a high ‘roughness’ value. 

**Getting Started**

1.  To start, 'Open' both of the .stl files from PH 13 (you can also use
    Ctrl+O). Your screen should look something like the image below.

![A screenshot of the CloudCompare interface with both scans of PH 13
imported.](https://user-images.githubusercontent.com/67739490/94279757-78564480-ff44-11ea-8941-e389118ae0c0.png)

2.  In the top left section of the workspace, you can see a window that
    says 'DB Tree' at the top (which is short for 'DataBase Tree'). This
    is where you can see the files you have added to the project.
    Currently, the two .stl files we have imported are two separate
    entities. To merge the two files into one 3D entity, Ctrl+Click both
    of the 'Mesh' layers from each of the files so that these are both
    highlighted. Then, find and click the 'Merge multiple clouds' icon
    on the toolbar (highlighted with a red box below). Then, uncheck the
    boxes to the left of the original files so that only the new 'Merged
    Mesh' is visible.

![This image shows the CloudCompare interface and shows how to merge two
meshes into a single mesh using the \'Merge Multiple Clouds\' icon. This
icon is highlighted with a red box in the
image.](https://user-images.githubusercontent.com/67739490/94279854-98860380-ff44-11ea-8657-ea46371fc142.png)

3.  Rotating the mesh is slightly different in CloudCompare, as the
    trackball is not constantly visible. Click and hold the mesh -- the
    trackball will appear. Try moving your mouse to rotate the mesh. As
    you are moving the mesh, take note of the appearance of the
    fingerprint(s?). Let's try isolating the fingerprints using the
    'Segment' tool in CloudCompare.

>**Try it yourself!** 
>-   Kimberlee S Moran, a forensic archaeologist who specialises in ancient fingerprints, has produced a ‘Fingerprinting Handout’ that introduces the key features fingerprint analysts use to differentiate between fingerprints. In this handout, we can see that the print in the centre of the sherd PH 13 does not exhibit any of the three basic print patterns: arch, loop, or whorl. Instead, these ridges all seem to be travelling parallel to each other (although the significantly raised clay in the centre makes it difficult to be certain). Examine your own fingers and hands – are there any areas that exhibit a similar pattern? What might have caused the raised area in the centre?
>-   As archaeologists, it is also important to consider at what stage of the manufacturing process these prints might have been made – the prints are made over the striations from the manufacturing processes, the clay was wet enough that prints were able to be made, and the prints were not effaced by the potter. What step in the manufacturing process might these prints represent? It could be that the print centrally positioned on the sherd represents a lower joint of the finger, rather than a fingertip. It could also be that this represents a partial hand-print, and that the clay ridge could have been caused by a palmar crease. If the former is true, the less well-defined print could be the fingerprint that we would want to examine, but is this detailed enough to identify features?


**Segmenting in CloudCompare**

1.  To do anything to alter the mesh, the 'Merged Mesh' will need to be
    highlighted in the DB Tree. The 'Segment' tool appears as a pair of
    scissors in the toolbar above the viewing window. Once you have
    selected the 'Segment tool', your screen should look something like
    that pictured below. As it says above the 3D model, left click
    around the fingerprints to add points to the polygon, and right
    click when you are happy with the shape you have created. Then,
    click the 'Segment in' to delete everything around the area you have
    selected.

![This image shows the CloudCompare interface with the merged mesh of PH
13 visible. The segment tool (highlighted with a red box and label on
the toolbar) has been selected, so a new toolbar has appeared in the top
right corner of the screen. After selecting the region of the
fingerprint, the \'segment in\' option can be selected (again,
highlighted in a red box and
labelled).](https://user-images.githubusercontent.com/67739490/94280084-e569da00-ff44-11ea-8316-452f61f92132.png)

2.  Once you have selected 'Segment In', the Segmentation function will
    pause. You can now rotate the area you have selected to ensure you
    are happy with the results. If the area needs further editing,
    unpause the tool to continue segmenting. If you are satisfied with
    the results, click the checkmark in the Segment Toolbar to 'Confirm
    Segmentation'.

3.  After confirming the segmentation, notice that the 'Merged Mesh' in
    the DB Tree has divided into two meshes: 'Merged Mesh.remaining' and
    'Merged Mesh.part'. Toggle each of these by clicking in the checkbox
    for each. You will see that your selected area has now been
    segmented from the rest of the 3D data. Turn off the 'Merged
    Mesh.remaining' layer to continue working with your fingerprint
    data.

>**Note:** For better visualisation results, ensure that you have segmented
>each of the prints from each other so that you are only working with one
>print at a time. To rename the meshes in the DB Tree, double left click
>on the object name you wish to change (highlighted in red below).

![In Cloud Compare, a single fingerprint from PH 13 has been segmented
from the rest of the mesh. In the Database Tree, a red rectangle
highlights that users should double click on the file name to rename the
mesh.](https://user-images.githubusercontent.com/67739490/94280597-7f318700-ff45-11ea-9fdc-bc1e6ed83853.png)

**Visualising 3D models in CloudCompare**

Before making substantial edits, it is always a good idea to
duplicate/clone the dataset you will be working with so that, if
something goes wrong, you will not have to repeat the above steps each
time. Highlight the Merged mesh.part and click the 'Clone' button (the
icon shows two sheep, outlined in a red box below). If you want to save
the work you have done in CloudCompare, you need to be sure that **[all
components]** you want to save are highlighted in the DB Tree
before you select 'Save' (you select multiple files/folders by holding
down the 'Ctrl' button and clicking on the files you wish to save in the
DB Tree).

![An image of part of the CloudCompare toolbar. The \'Clone\' icon is
highlighted with a red
rectangle.](https://user-images.githubusercontent.com/67739490/94280851-d172a800-ff45-11ea-8b78-7982083eca97.png)

1.  First, it is important that the fingerprint is as 'flat' as it can
    be in the 3D space, so that the software can recognise the high
    points and low points of the ridges (aligning the height of the
    ridges to represent the Z coordinates). From the toolbar on the left
    side of the screen, select the icon that looks like a black triangle
    and an arrow. The software will then prompt you to select three
    points on the 3D mesh. Ensure that these points are as far apart as
    possible on the mesh, along the edge, as this will determine how
    flat the print is.

![A part of another toolbar is presented here with a red rectangle
highlighting the icon that would allow users to pick three points on the
mesh to level the mesh. ](https://user-images.githubusercontent.com/67739490/94280928-ea7b5900-ff45-11ea-8de8-446e662ef1b6.png)
![A snapshot of the \'pick three points\'
levelling option in
action.](https://user-images.githubusercontent.com/67739490/94280928-ea7b5900-ff45-11ea-8de8-446e662ef1b6.png)

2.  An automated option for levelling the mesh is provided under
    'Tools', called 'Fit' to plane. This produces a **transformation
    matrix** in the 'Console' area of the screen (usually at the bottom
    of the window) that will align your mesh to the plane it has
    calculated. A matrix is an array that, in this case, dictates how
    the mesh needs to be mathematically rotated and translated to align
    with the plane. The first three columns correspond to how the points
    should rotate in three dimensions, while the fourth column
    corresponds to how much and in what direction the mesh needs to
    slide, or **translate**.

3.  To apply this alignment, click on the matrix entry so that it is
    highlighted and use Ctrl+C to copy the matrix. Ensure that the mesh
    is highlighted in the DB tree. Navigate to the 'Edit' dropdown menu
    to find the '[Apply
    Transformation'](https://www.cloudcompare.org/doc/wiki/index.php?title=Apply_Transformation#Input_a_transformation)
    function, delete the matrix provided and paste your new matrix in
    using Ctrl+V. Click 'OK' and the transformation will be complete.
    Uncheck the tick box next to the 'Plane' that was generated to
    remove it from view.

![This image shows how to apply the transformation if using the \'Fit to
plane\' levelling option. It shows where to find the transformation
matrix in the console portion of the CloudCompare
interface.](media/image8.png){width="9.693055555555556in"
height="4.274305555555555in"}

![A screenshot showing where to paste the transformation
matrix.](media/image9.PNG){width="6.117197069116361in"
height="4.225366360454943in"}

![After the transformation has been applied, check the box next to the
plane to remove it from
view.](media/image10.png){width="9.693055555555556in"
height="3.0868055555555554in"}

4.  Once the 3D model is aligned, navigate to 'Scalar Fields' from the
    'Edit' dropdown menu and select 'Export coordinate(s) to SF(s)'.
    Ensure that the checkbox next to 'Z' is selected before you hit
    'Ok'. A **Scalar Field**, as defined in the CloudCompare manual, is
    'a set of values (one value per point)'; CloudCompare allows a value
    associated with a point/vertex to be displayed as colours or have
    filters or basic math operations applied to them. In this case, we
    are assigning the Z-values of the mesh as a scalar field -- the
    relative height of the mesh above the level plane we created in the
    previous step(s). This will allow us to assign different colours to
    points with different heights. This is only one of many values that
    could be assigned to a Scalar Field; virtually any property that can
    be used to describe the shape of the surface can appear in the
    scalar field, including other morphometric parameters that will be
    introduced in Exercises 4 and 5.

![A screenshot showing the interface to export the Z coordinates of the
3D model to the Scalar
Field.](media/image11.PNG){width="9.693055555555556in"
height="5.028472222222222in"}

5.  If you highlight the 3D model and navigate to the 'Properties'
    > window (often automatically pinned below the DB Tree window), you
    > will find that under 'CC Object' you can now change the 'Colors'
    > from 'None' to 'Scalar field'. Scrolling through the properties,
    > under 'Color Scale', you will be able to change the appearance of
    > the 3D model from a dropdown menu.

> ![A screenshot of the Properties window to show how to set the Scalar
> field as the color of the 3D
> mesh.](media/image12.PNG){width="3.97838145231846in"
> height="4.116666666666666in"}

![A screenshot of the fingerprint mesh with its color set to Scalar
field and a Viridis color scale
applied.](media/image13.PNG){width="9.693055555555556in"
height="4.427777777777778in"}

6.  From the SF display params, using the Viridis setting (above), you
    can see that the highest values are yellow, while the lowest values
    are purple. This does not quite show the fingerprint at its best,
    though it clearly shows the ridge of raised clay in the centre of
    the print. To edit the colour scale, navigate to the icon for the
    'Color Scale Editor' in the toolbar across the top of the screen. To
    edit any of the scales, you will first need to make a copy of the
    base color scale you start with. Choose to make a copy of the 'Grey'
    preset colours, rename the scale, and save it. Now set your new
    scale as the current color scale.

![A close up of the CloudCompare toolbar with the Color Scale
Editor/Manager icon highlighted with a red
box.](media/image14.png){width="3.1936100174978126in"
height="0.8800765529308836in"}

![A screenshot showing the Color Scale Editor prior to copying the Grey
color scale.](media/image15.PNG){width="9.693055555555556in"
height="4.6402777777777775in"}

![A screenshot of the mesh with a grey color scale applied.
](media/image16.PNG){width="9.693055555555556in"
height="4.548611111111111in"}

7.  Now go back and edit your edited scalar field. On the color bar, you
    will see two small boxes at either end of the bar. Click on the
    black box on the left -- you will see that the fields below this, in
    an area labelled 'Selected Slider', are now no longer greyed out.
    Change the colour of this end of the slider by clicking the box next
    to 'Color'. For now, change this to white.

![A screenshot of edits being made to the copied color
scale.](media/image17.PNG){width="9.693055555555556in"
height="4.406944444444444in"}

8.  Now change the slider on the right side of the bar to black. Click
    apply and save the modifications.

9.  Your screen should look something like the image below, with the
    black and white gradient inverted from its previous state. In the
    properties of the mesh, in the SF display params, experiment with
    sliding the triangles along the histogram to see how this affects
    the coloration of the 3D model.

![A screenshot of the fingerprint where the grey color scale has been
inverted. Now the raised ridge of clay is black, while the lower parts
of the mesh are white. ](media/image18.PNG){width="9.693055555555556in"
height="4.529166666666667in"}

10. While the above image appears more similar to how we might visualise
    a fingerprint, the raised ridge of clay along the centre is clearly
    affecting how this is being visualised. If one were to compare this
    against some of the options in Meshlab's Radiance Scaling (see
    below; the red areas highlight the raised ridges of the
    fingerprint), it is clear that the added topography from the ridge
    and the curvature of the ceramic vessel itself is diminishing the
    impact of the relative difference in height (the Z coordinates of
    the 3D model) between the fingerprint ridges and the dips between
    them.

![A screenshot of the same fingerprint mesh imported into Meshlab.
Radiance Scaling has been applied, but the display mode has been changed
to Colored Descriptor. This brings out the ridges of the fingerprint
despite the raised ridge of clay disrupting the centre of the
fingerprint.](media/image19.PNG){width="8.958333333333334in"
height="4.50997375328084in"}

![](media/image20.png){width="3.7375in" height="3.9583333333333335in"}
