**Exercise 5: Simple Measurements in CloudCompare**

**(Allow at least 1.5 hours for Exercise 5)**

Let's say we want to consider the different manufacturing techniques
used in creating the pottery from the Parker-Harris Pottery site and the
Three Cranes tavern. We'll want to combine both visual and metric
approaches to consider the different surface treatments used on the
potsherds from the dataset. In this exercise, you will learn to:

-   ***Take simple measurements from 3D models in CloudCompare;***

-   ***Work with multiple meshes in the same project using multiple 3D
    view ports in Tile mode;***

-   ***Employ all of the skills developed in Exercises 1-4 and combine
    visual and metric analyses to interpret 3D data to learn more about
    the pottery created and used at these sites.***

1.  Import the two .stl files for TC_23 and merge the meshes.

2.  You may notice that, unlike some of the other sherds you've viewed,
    the surface of this vessel appears to have been brushed with some
    sort of tool. Unlike other potsherds, where parallel striations from
    the potter's wheel were visible, the brushstrokes have created
    overlapping/intersecting groups of striations (see image below). Use
    the 'Segment' tool to isolate some complete, clear brush strokes. If
    you need to change the colour of the 3D model to see this more
    clearly, do so following any of the steps provided above, or choose
    'Colors' from the Edit dropdown menu and 'Set Unique'.

3.  Point-to-point measurements are another example of a CloudCompare
    function that only works with the mesh's vertices. Turn on the
    'vertices' layer of your 3D model as you did in step 4 of Exercise 4
    above. Highlight the vertices layer and select the 'Point Picker'
    tool (highlighted in red).

![A screenshot of TC_23 in the CloudCompare interface, with the vertices
layer highlighted in the DB Tree. A red box highlights the Point Picker
tool on the toolbar.](https://user-images.githubusercontent.com/67739490/94291971-3af9b300-ff54-11ea-9f26-7801acad60fb.png)

4.  A new toolbar will appear in the top right corner of the 3D viewer
    -- to measure between two points, choose the second icon, and then
    click in two places on the 3D model to measure the length of a
    feature.

    a.  Keep in mind that this is a straight line measurement -- after
        you've created your line segment, you can rotate the 3D model to
        see if this cuts through your 3D model, or if it is roughly
        following the curvature of the surface of the potsherd.

    b.  As you can see in the image below, the brush stroke I measured
        is roughly 12mm long. Because this seems to be truncated by
        later brush strokes, what might be more useful would be
        measuring the width of the mark to see if the same sort of tool
        can be identified between different potsherds. Overall, on
        TC_23, it appears that the tool is somewhere around 4.1mm in
        width.

![Two points have been picked to measure the length of a tool mark on TC
23. The point picker toolbar is highlighted in the top right
corner.](https://user-images.githubusercontent.com/67739490/94292047-5795eb00-ff54-11ea-80db-0232a575a845.png)

![A close up of the measurement of the width of the tool mark on TC 23.
It is roughly 4.1mm wide.](https://user-images.githubusercontent.com/67739490/94292112-6e3c4200-ff54-11ea-855e-38a70bef4df9.png)

5.  Import some more potsherds and see how their surface treatment
    differs. I have chosen PH_21 for this next set of measurements --
    the surface is much smoother, and some sort of tool has been used to
    scrape/indent two 'trailed' bands across the vessel. Was it the same
    tool? If we compare the two measurements below, there is some
    suggestion that the same tool might have been used, but this is
    definitely a different tool than was used on TC_23. Perhaps PH_21
    and TC_23 were two different types of vessels with different
    functions, or were they created by two different potters?

**Note:** You may find that choosing points of comparison relatively
difficult in 3D. While not the most accurate way to measure these
features, this does give us some further insight into this dataset and
points to consider.

![On the left, a trailed band is measured on PH 21. It is roughly 6.9mm
wide. On the right, a trailed band from a lower position on the same
vessel measures 6.8mm
wide.](https://user-images.githubusercontent.com/67739490/94292180-81e7a880-ff54-11ea-8d85-481f0ad2a850.png)

6.  You may wish to compare two potsherds side by side in real time;
    this is useful because they will both be at the same scale in the
    same 3D space, and so some differences may become more obvious.

    a.  If you want to compare the two potsherds side by side in the
        same 3D viewer, highlight one of the meshes in the DB Tree, and
        select the 'Translate/Rotate' tool (to the right of the
        'Segment' tool, highlighted in red below).

    b.  Holding down the left mouse button will allow you to rotate the
        selected mesh; holding down the right mouse button will allow
        you to move/translate the highlighted 3D model without moving
        the other 3D model.

![A screenshot of both TC 23 and PH 21 in the same 3D View. The
\'Translate/Rotate\' tool is highlighted with a red box on the
toolbar.](https://user-images.githubusercontent.com/67739490/94292270-a2affe00-ff54-11ea-80b5-8a1a78c3a5a6.png)

7.  Recall that, if you want to allocate these 3D models to different 3D
    spaces, you can do this with the '3D Views' drop down menu.

    a.  First, create a new 3D View. Then highlight one of the meshes in
        your DB tree.

    b.  Under its 'Properties', you can change its 'Current display' to
        the new 3D View window. If you want to view at the same time,
        from the '3D Views' drop down menu, you can select the 'Cascade'
        or 'Tile' Options to view multiple 3D views at once. However,
        because they are in different 3D spaces, they will be at
        different scales.

> ![A screenshot showing PH 21 and TC 23 in different 3D views in
> different tiles. The 3D views dropdown menu and the Current display
> option under the mesh Properties are both highlighted with red
> boxes.](https://user-images.githubusercontent.com/67739490/94292359-c07d6300-ff54-11ea-935a-f90b8f1223b8.png)

8.  Instead of individual measurements, what if we used 'Roughness' as a
    method of characterising the different surface treatments? First,
    ensure that you have 'segmented' your meshes down to a relatively
    flat piece of potsherd that provides a good example of the sherd's
    overall surface treatment. For this exercise, I imported the meshes
    of PH 21, TC 23, PH 19 and PH 12, but you are welcome to import any
    others that you found interesting during your own exploration of the
    archive.

9.  Next, align your meshes and export the Z coordinates to their
    respective Scalar Fields.

10. Enable and highlight the 'vertices' layer for your mesh as you did
    in step 2 of this exercise. Then, under the 'Tools' drop down menu,
    select 'Other' and 'Compute Geometric Features'.

    a.  Select 'Roughness' and set this at a consistent kernel radius
        throughout (in this case, I used 3.16383). Ensure that the
        'Color Scale' is visible under each sherd's 'Properties'. If you
        put each of the sherds to separate 3D views and selected the
        'Tile' option, your screen should look something like the below.

![In the CloudCompare interface, four potsherds with their roughness
values applied as Scalar Fields are visible in four different 3D
views.](media/image7.png){width="9.680753499562554in"
height="4.218522528433946in"}

11. You may notice that the visualisation of the 'Roughness' calculation
    also proves quite useful in visual characterisation of the
    manufacturing traces. If the automatic visualisation settings do not
    show many details, try editing the 'SF display params' for the sherd
    (highlighted in red boxes below). For PH 12, clicking and dragging
    the **red triangle** to the left (circled in red below) decreases
    the maximum saturation values of the Scalar Field and brings out the
    subtle striations typical of wheel-thrown pottery.

![In the top image, the manufacturing traces of PH 12 are less visible.
The SF display params interface is highlighted with a red box and the
red triangle representing the maximum saturation value is circled in
red. In the bottom image, the pottery wheel striations are more visible
in PH 12 because the maximum saturation value has been decreased by
dragging the red triangle to the
left.](media/image8.png){width="6.453892169728784in"
height="5.233787182852144in"}

12. As you compare the Roughness values of your chosen sherds, you may
    notice that some are characterised differently from what you'd
    expect. For example, the maximum Roughness value of PH 12 is 0.319,
    closer in magnitude to PH 21 (0.382) and TC 23 (0.338) than PH 19
    (0.1), though PH 12's surface treatment appears quite visually
    similar to PH 19. This could be, in part, affected by **outliers**
    caused by post-depositional processes, like the pitting that appears
    red on the surface of the potsherd in the image above.

    a.  If we want to better understand the manufacturing process in
        relation to roughness, these outliers are not useful and should
        be excluded from our analysis. While the 'visible color scale'
        provides a summary **histogram** on the right, you can view a
        larger version by selecting the mesh and 'Show Histogram' (the
        toolbar icon is highlighted with a red box below). Because the
        PH 21 sherd is uneven (though mostly due to the design of the
        vessel form), the lower part of the sherd is causing a great
        deal of the roughness for this sherd. What level of roughness do
        you think is a reasonable characterisation of PH 21's surface?

![With the CloudCompare interface in the background, the larger
Histogram showing the calculated roughness for PH 21\'s point cloud is
visible on the right side of the image. The icon to bring up this larger
histogram is highlighted with a red box on the
toolbar.](media/image9.png){width="9.693055555555556in"
height="4.086805555555555in"}

13. Another way to deal with outliers is to work with the 'SF display
    params' as we did in step 11 of this exercise.

    a.  First, ensure that the downward-pointing arrows are at their
        initial starting positions on either side of the histogram. Now,
        drag the white circle from the far right side towards the left
        (this has been done for PH 19 in the red box below); you are
        decreasing the Maximum Scalar Values to remove outliers.

    b.  Watch the mesh as you do this -- areas of extreme 'Roughness'
        should slowly turn grey. Continue to do this for each of the
        meshes until you are satisfied that the outliers caused by
        post-depositional processes are greyed out.

    c.  Now a more reliable comparison can be made between the
        'Roughness' values of each sherd. You can also adjust the
        Saturation values as we did in Step 11 to enhance the visibility
        of the surface treatments.

![By decreasing the Maximum Scalar Value for the four potsherds, the
post-depositional pitting previously visible on many of the potsherds is
now greyed out. This is reflected in the Color Scale to the right of
each potsherd, which now show a more reliable Roughness value for their
respective sherds.](media/image10.png){width="9.693055555555556in"
height="4.153472222222222in"}

![A close up of the four potsherds after the Maximum Scalar Values have
been decreased to remove outliers, followed by decreasing the Maximum
Saturation values to highlight the subtler surface
treatments.](media/image11.png){width="9.680753499562554in"
height="5.1260936132983375in"}
