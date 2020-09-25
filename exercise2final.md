**Exercise 2: Taking measurements in Meshlab**

**(6 minute video, allow for at least 20 minutes for Exercise 2)**

Visually inspecting 3D models is necessary to familiarise yourself with
the dataset, to make initial judgements on the suitability of reused
data for your research, and to take note of your initial observations,
like patterns of similarities and differences in appearance. But to
investigate questions like whether the same individual created two
different pots, whether the distance between a series of fingerprints
suggests that they all belong to the same hand, or whether different
fingerprints were made during different stages of the manufacturing
process, we need to be able to take measurements to assess the size and
distance of these features more rigorously. In this exercise, you will
learn to:

-   ***Carry out simple measurements from 3D models in MeshLab.***

Recall that models need to be scaled for us to be able to take
measurements from them or use them in quantitative analyses. While the
scale of the object does not matter so much in visual assessments, it is
necessary in metric assessments. Without scale, the Colosseum and a soup
bowl are about the same size in 3D. It should be stated somewhere in the
metadata of the dataset how the 3D models have been scaled; in this
case, the Boston Fingerprints dataset has been scaled in millimetres.

**The Measuring Tool**

If you want to measure between two points on the 3D model, you can use
Meshlab's measuring tool (which looks like a measuring tape on the
toolbar, highlighted with a blue box below). Click the icon, then
left-click the two points on the 3D model you want to measure between.
An orange line should appear between the two points, and you will be
able to move the 3D model around to ensure the accuracy of the
measurement. If you click on the measuring tape again, you can continue
to create new measurements. When you double-click on the measuring tape
icon, the orange lines will all disappear, though your measurements will
still be recorded in the window in the bottom right corner.

![An image of a segment of the Meshlab Toolbar. The measuring tape icon
is surrounded by a blue
rectangle.](https://user-images.githubusercontent.com/67739490/94272164-96b74280-ff3a-11ea-9e05-0759b6148465.png)

![The Ph25 merged mesh has been imported into Meshlab and the Radiance
Scaling shader applied. An orange line stretches across one of the
fingerprints after a measurement has been
made.](https://user-images.githubusercontent.com/67739490/94272227-adf63000-ff3a-11ea-8425-3bcca045497a.png)

![All five fingerprints and the spaces between four of these have been measured - orange lines stretch across and between these features. Each measurement has been labelled according to the distances recorded in the bottom right box. ](media/image3.PNG){width="9.084204943132109in"
height="4.816666666666666in"}

One could interpret that the fingerprints M0, M1, M2 and M3 are from the
same hand and the same 'event' of the potter touching the pot, but would
the arrangement of these prints allow M7 to represent the thumb print
from the same 'event'? Try arranging your fingers to match this layout
-- it is difficult, though the shape of the bowl might have influenced
their placement. There is also the possibility that M3 was not made
during the same 'event', as it is not clear whether the print ridges are
curving in the same direction as M0, M1 and M2.

Meshlab is powerful software; in this tutorial, we have only scratched
the surface of how it can be used to visualise 3D data. However, the
vast majority of Meshlab's functions are not intuitive. Fortunately,
there are many tutorials available online, the most popular of which is
the YouTube channel [Mister P. Meshlab
Tutorials](https://www.youtube.com/channel/UC70CKZQPj_ZAJ0Osrm6TyTg).
