#### Calculate evaluation metrics

(1) calculate Jacard Index and cell counting accuracy 

   **evaluation** also calculates Dice, False positive percentage,
   False negative percentage, Distance of major axis, and relative angle between
   major axis. 
   When each cell  matches with  the GT cell, it  gets deleted from the list. There
   can't be cells that are matched twice.

    *inputs*: have to be a  directory that contains tif ground truth images and a directory that contains .tif segmentation masks from Unet or LCuts.

(2) calculate local density based on tiling of the image.

   calc_local_density_v3_tiles.m

   Tile GT images/3D mannual annotations and calculate local density:
   local density = cell volume / tile volume.
   *two output metrics*: maximum local density and the mean of top 10 local densities.




