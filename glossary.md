**Glossary of terms**

**Histogram** - A diagram that graphically represents the quantity of
points that fall within equal ranges with rectangles that increase in
height as more points fall within that range.

**Mesh** - Triangular polygons are generated between the points of a
point cloud until a 'solid' mesh is created. The point cloud become the
**vertices** of the mesh.

**Metadata** - Information that describes other data.

**Morphometric parameters** - Quantitative measurements that can be used
to describe an object's form. This includes measurements you will
already be familiar with (length, width, volume), but can also include
parameters like 'Roughness' or 'Curvature'. Morphometrics only take into
account the shape of the 3D surface.

> **Roughness** -- Morphometric parameter calculated by CloudCompare in
> the following way -- "For each point, the \'roughness\' value is equal
> to the distance between this point and the best fitting plane computed
> on its nearest neighbours."
>
> **Curvature** - Morphometric parameter calculated by CloudCompare in
> the following way - "The curvature at each point is estimated by best
> fitting a quadric around it based on its nearest neighbours."

**Outliers** -- Data points which fall outside the normal range of the
majority of the other points in the point cloud.

**Point cloud** -- Calculated points in three-dimensional space produced
when a digital imaging technique measures and records the surface of an
object; each point is defined by a set of coordinates on the X, Y and Z
planes.

**Scalar Field** - As defined in the CloudCompare manual, is 'a set of
values (one value per point)'; CloudCompare allows a value associated
with a point/vertex to be displayed as colours, have filters or basic
math operations applied to them.

**Shaders** -- Tools that render the appearance of the surface based on
a number of factors, including lighting position and transparency, view
position, material properties, and shape of the 3D surface.

**Texture** - A photorealistic flat image that can be 'draped' over the
3D mesh to give it a more realistic appearance. A texture can also be
created independently and applied to a 3D model with no colour
information

**Transformation matrix** - A matrix is an array that, in this case,
dictates how the mesh needs to be mathematically rotated and translated
to align with the plane. The first three columns correspond to how the
points should rotate in three dimensions, while the fourth column
corresponds to how much and in what direction the mesh needs to slide,
or **translate**.

**Trivet** -- A type of kiln furniture used to keep unfired vessels
apart at the [Parker-Harris Pottery
site](https://www.sec.state.ma.us/mhc/mhcarchexhibitsonline/parkerharris.htm).
