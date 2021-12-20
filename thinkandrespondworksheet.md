## Exercise 1

**Think and Respond**: Take a look at the ‘Decision Tree’ below – can you think of any other instances in which you should use the laser scan data rather than building the 3D reconstruction from other resources?

**Think and Respond**: Summarise what you now know about the dataset after reading the metadata report. What are some of the challenges you can see in working with this dataset?  Take note of what you think is most important and add it to your Design Document under the Resources: Available section.

**Think and Respond:** Now that you have viewed the different point clouds and meshes available to you, assess how much of the data is needed for your reconstruction. What do you notice about what was captured in the scan data? How much of the site has been recorded? According to the report, everything within the fortified wall was recorded, though there may be related structures situated outside of this boundary. Will the trees and grass captured in the laser scans help or impede your reconstruction? It seems unlikely that an occupied settlement would have been covered in grass, so we can plan to remove these later. What level of detail will you require for your reconstruction – will the outline of buildings be sufficient to build from? While the snapshots of the full-resolution point cloud in the report show that the laser scans have recorded individual stones quite clearly, you need to decide if that level of detail is necessary for what you need to achieve. To meet this design brief, do you need the entire dataset, or only subsections of the recorded data (ie one house)? What size of dataset will be easy to work with (considering your computer’s hardware; if you find you are having issues with this, you may need to use one of the computers in UofG’s Digital Archaeology lab)? Do you need meshes or points? While point clouds appear quite attractive, the software we will be using and games engines [i.e. 3D modelling software which will be further discussed in later Exercises, and Unity and Unreal engines] are not generally designed to work with point clouds in this way.  **Summarise and incorporate your thoughts on these considerations in your Design Document template, particularly in the ‘Resources’ and ‘Constraints’ sections.**

**Try it yourself!** Try each of the subsampling methods on your test point cloud. Be sure to duplicate your point cloud a few times before doing this; simply highlight your sample and navigate to ‘Edit > Clone’. Rename the layers according to the sub-sampling method to be particularly organised, by double clicking the name of the layer in the DB Tree and giving each an informative name. Write a short paragraph describing what differences you noticed between the different methods and which you think is best for this project.

**Think and Respond**: Why is it essential to remove the vegetation from the point cloud, in this case?

**Think and Respond:** Can you think of other features that you may want to separate in other hypothetical laser scan datasets? Are they quite similar to each other in terms of shape, or quite different? How would you describe these similarities/differences? What would the benefits be in separating these features?

**Try it yourself!** When selecting segments for your classifiers, was it easier to isolate samples before or after calculating roughness? Can you foresee any issues that may arise when applying your classifier to the rest of the dataset?

**Try it yourself!** How successful was your classifier at separating the point cloud into vegetation vs non-vegetation geometry?

**Think and Respond:** To keep our datasets manageable, we will need to subdivide the Malthi dataset into smaller chunks for processing, but we will reassemble the site in the reconstruction later. Decide what you will want to have available as a discrete object. Do you want to have individual walls? Walls and surrounding ground? How will you separate buildings that share walls? Whole buildings or sections of the site? Use the published plans of the site layout to plan how these features can be divided. Crop your data appropriately using the segment tool. (Do note that your meshes will maintain their local spatial coordinates, even when exported into different software, so the spatial relationship between two walls that have been saved as different meshes will remain).

**Think and Respond:** By the end of this process, you should have a mesh of all or part of the site of Malthi. Take a closer look at the mesh – is this a sufficient level of detail for what you will need to reconstruct the site? What essential parts are present, if the aim of the reconstruction is to get a sense of how the site would be navigated? Which essential parts are missing? Are there any stray bits of mesh that need to be cleaned up/removed?

**Think and Respond:** At this point, you should be able to fill out a good deal of your Design Document, including the Project Brief, Overview, Project Aims, many of the Resources, and some of the Constraints. Review your previous ‘Read and Respond’ answers for ideas! 

## Exercise 2

**Try it yourself!** Create a list of potential features and interactions you could include in a reconstruction of Malthi. Assign each of these according to the MoSCoW method – think about how you decided which features were ‘must haves’ rather than ‘should haves’. Which factors could change how you’ve classified these? If more time was available for the project? Add these to your Design Document, which you started in Exercise 1.

**Think and Respond**: Given your searches through the software documentation and the Software Comparison table, which options would be best suited to this project? Which options are best suited to your budget/future skills building?

## Exercise 3

**Think and Respond:** Does your mesh look significantly different after this clean-up process, or were most of the changes invisible to you? Do you think this is still a metrically-accurate mesh? Are there any other features you may want to remove at this stage (rubble piles from early excavations that would not have appeared this way in the Bronze Age)? Does this mesh still represent the archaeological reality of the site?

**Try it yourself!** Try processing your original mesh into decimated meshes with different counts of vertices. Which level seems to preserve enough detail, in your opinion? How many meshes have you broken the Malthi dataset into? Do you think the file size of the decimated composite dataset be small enough to work with easily?

**Try it yourself!** Which of these options worked best to fill any holes in your decimated mesh? If something didn’t work, why do you think caused it?

**Think and Respond:** Watch part of [J Middleton’s](https://youtu.be/MrUVeV0wsH8) tutorial video (at least from 25:45 – 32:48). Did you create your own seams? How did they turn out? (and if they didn’t, why do you think J Middleton’s seams worked for the UV map?) If you used the Smart UV project, can you see why this would be disadvantageous for other projects (especially those incorporating colour)?

**Try it yourself!** Try changing the Viewport shading options in your 3D Viewport – you can find this in the dropdown menu just to the right of the ‘Viewport shading’ button highlighted in the image above. How does this change the appearance of your decimated mesh and the normals? 

**Think and Respond:** Examine your decimated mesh with the normal map applied and compare this to the original mesh by turning their respective layers on and off. Do you see the benefit in creating the normal map? Do you think this will be easier to model on than the decimated mesh alone? Why?

## Exercise 4

**Think and Respond:** As you greybox your chosen area, can you identify individual rooms? Individual buildings? How certain are you in separating these? Have you been able to identify access points?

**Think and Respond:** Consider the area of the site that you have already greyboxed; how many of these walls do you think could have feasibly belonged to a single, roofed structure? How many basic shapes will you need to put together to recreate the visible footprint of the structures?

**Try it yourself!** If you wanted to add the cross-beam to your modelled house to better replicate the Tsoungiza reconstruction, how would you do this in Blender? At which step would you have added it? Try adding another building – are there any differences in the floorplan of this structure that affected how you designed this second structure?

**Think and Respond:** After greyboxing Malthi and reconstructing a hypothetical Bronze Age structure to fit the extant structural remnants on site, has this helped you to understand the site better? Is there anything you noticed about the site through the process of modelling? How did the process of modelling affect your interpretation of the site?

**Think and Respond:** Do you feel that these assets are sufficient for a reconstruction of the site? What do you feel is missing? While sculpting individual bricks into the side of your reconstructed house might be satisfying, is it necessary to fulfil the brief? Do you need a textured house for the purposes of your reconstruction?

### Optional

**Try it yourself!** Navigate to textures.com – which textures would be suitable, based on Dr Worsham’s discussion in Exercise 2? search for ‘mud brick wall’ or ‘clay wall’? Which would you choose? Think about what the surrounding landscape looks like? What is a reasonable colour for mud brick based on this knowledge?

## Exercise 5

**Think and Respond:** Regardless of which tools, game engines, or websites you utilise to deliver your reconstruction, you need to have a good understanding of what is possible through each of these options. Let’s consider the ‘MoSCoW’ approach introduced in [Exercise 2](/Malthi_Exercise2.md) and add to your Design Document. Examine the example projects above; what features do you see in these examples? Which of these features are ‘must haves’, ‘should haves’, ‘could haves’, and ‘won’t haves’ when you consider your reconstruction of Malthi? For example, do you need transparency options to make it clear which components are your reconstruction, and which originate from 3D records? Do you need to show multiple phases of the site in a single application, and how will you shift between these? How will ambiguity be portrayed? These are all things that need to be considered before the project gets started, and preferably before your first meeting with any project partners.

**Try it yourself!** Try changing the ratio a few times – what do you notice about the quality of your mesh after each decimation? Be sure to turn on the ‘Viewport shading’ (highlighted with a white box below) to see how this affects the quality of your normal map. Are there any obvious differences?

**Think and Respond**: What types of information do you think are important to include in the Sketchfab description for your reconstruction of Malthi? What archaeological information would you include, given the 1024 character limit? What information would you provide about the source of the laser scan data? The paradata/choices you made in creating your reconstruction? Any other information?

**Think and Respond:** Which features are of note in your reconstruction? Are there specific access routes you identified through the process of reconstruction? Are there certain areas limited to specific activities, like administration, or metalworking? Which of these are particularly important to highlight on the model itself; are some difficult to describe through just the ‘description’ box? Make a list of 5-10 annotations you would like to make on this 3D reconstruction and add it to your ‘Design Document’.

**Think and Respond:** Does the Sketchfab approach seem quite simple? Effective? Does this qualify as interactable? Are there any issues you can think of to use Sketchfab on a long-term basis? Does this approach meet the project aims/requirements set out in Exercise 1? Why or why not?

### Optional

**Think and Respond**: Before you start this optional activity, reflect on your own learning objectives. Do you feel that the additional work and time investment that you will put into learning this new skillset is worth the range of possibilities Unity offers for archaeological reconstructions? Which features offered by Unity (and not offered by Sketchfab) do you think are particularly important for interpreting reconstructed archaeological sites?

**Try it yourself!** You may have noticed that your character is currently able to move through the walls of your reconstruction. How would you ensure that your player character collides with these structures?

**Think and respond:** What other details can you add to your reconstruction? What is necessary to address the aims of the project? Other textures? Should the light source in the scene be positioned in a certain direction (where would the sun be above the actual site of Malthi during the morning? The afternoon? The evening?) As you test your experience, what is missing? Do you need to add a bounding box to ensure your users cannot fall into the ‘void’? What about sound?

**Think and respond:** Now that you have basic experience with both approaches, given the requirements/parameters of the project set out in Exercise 1, do you think that Sketchfab or Unity would be a better output? Why have you made that choice? What are the benefits of using Sketchfab, despite its limited functionality? What are the benefits of Unity, despite the amount of learning and time it takes to create an engaging experience?

## Reflect Further: Archiving and Ethics

### Optional

**Think and respond (optional):** How will you make your paradata available? Will you use a diary or blog format as [Kastanis](https://lazphdlog.tumblr.com/post/97204874734/rebuilding-the-rose-theatre-experiences-assumptions) has, or simply list your sources as [Plaskin](https://www.nefertaritomb.com/sources) has for the reconstruction of Nefertari’s tomb? Will you use a pro-forma report, providing only the basic information? Will you add attributes to the 3D item itself? What are the main benefits of the approach you have chosen?

**Try it yourself!** Download the ‘3D Models, Visualisation and Virtual Reality’ template from the [Archaeology Data Service](https://archaeologydataservice.ac.uk/advice/Downloads.xhtml). How much of the template is relevant to your project and its individual components? Try filling in the template with the information about each of your OBJ exports from Exercise 1 and the normal maps generated during Exercise 3. Did naming your files sensibly make this easier to describe and contextualise? Is there any metadata that you thought was important, but could not find a suitable category for it in the template? Have you utilised any of the Dublin Core terminology in your metadata? How does your metadata entry for the reconstruction itself differ from the OBJ component entries?
