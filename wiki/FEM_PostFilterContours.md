---
- GuiCommand:
   Name:FEM PostFilterContours
   MenuLocation:Results → Contours filter
   Workbenches:[FEM](FEM_Workbench.md)
   Version:1.0
   SeeAlso:[FEM Result pipeline](FEM_PostPipelineFromResult.md), [FEM Filter functions](FEM_PostCreateFunctions.md), [FEM tutorial](FEM_tutorial.md)
---

# FEM PostFilterContours

## Description

Creates iso-contours and iso-lines in the results mesh.

 <img alt="" src=images/FEM_PostFilterContours_relnotes_1.0.png  style="width:400px;">  
*Iso-contours, depicting the y-component of the absolute magnetic<br>
flux density in and around a copper wire that is flown through by<br>
an electric current at a frequency of 100 kHz.<br>
For more info about this model, see section 14 of the [https://www.nic.funet.fi/index/elmer/doc/ElmerTutorials.pdf Elmer Tutorials].*

## Usage

1.  Select a previously created [result pipeline](FEM_PostPipelineFromResult.md).
2.  Create the filter either by pressing the button **<img src="images/FEM_PostFilterContours.svg" width=16px> '''Contours filter'''** or by using the menu **Results → <img src="images/FEM_PostFilterContours.svg" width=16px> Contours filter**.
3.  Adjust the **Result display options** like for the [result pipeline](FEM_PostPipelineFromResult.md). You might need to hide the pipeline to see the effect of the filter in the preview.
4.  In the appearing dialog set the result field and the number of contours.
5.  Click the **OK** button to finish the command.

The dialog offers the following settings:

-   **Field**: The results field to be drawn.
-   **Vector**: If the **Field** is a vector, the vector components.
-   **Number of contours**\': The number of contours to be created. **Note:** depending on the geometry the created number of contours can be higher that selected. The reason the creation algorithm. However, for 2D and simple geometries, the number should be correct.
-   **No color**: Don\'t apply a color to the contours.

**Note**: A **Field** can only be set if a filter function exists and has been applied with <img alt="" src=images/FEM_PostApplyChanges.svg  style="width:16px;"> [Apply Changes](FEM_PostApplyChanges.md). Alternatively you can reopen the filter dialog.

## File Size Information 

Setting a Contours filter can increase the file size a lot. The reason is that the algorithm needs to copy the [Post result pipeline](FEM_PostPipelineFromResult.md). A single contour does not need the whole mesh so that the algorithm to create a contour can work with half of the pipeline storage size. This will be the size for every contour. Take for example the case that the pipeline storage size is 2 MB, adding a Contours filter with 10 contours will then lead to a 5 MB larger file size.

The storage size of the pipeline depends on the used mesh. The finer the mesh, the larger the pipeline size. Therefore be careful if you have large meshes and contours.

If you use contours only on a part of the mesh, for example when you have a clip filter, then create the Contours filter on the filter and not on the pipeline. Of you need the whole pipeline, start to draw few contours and then step by step go up until the file size is still acceptable while the visualization is as you like it.




 {{FEM Tools navi}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [FEM](Category_FEM.md) > FEM PostFilterContours
