# 3DTerrainMap
This project documents a step-by-step workflow to generate and compare 3D terrain maps using before and after elevation datasets and aerial imagery from the 2014 Oso landslide event in Washington State, USA. It uses ArcGIS Pro 3.2 and demonstrates best practices in elevation surface authoring and 3D scene design.

 ### Workflow Steps
#### Step 1: Download and Extract Data
Download from link (https://www.arcgis.com/home/item.html?id=e90811068f024d3cb6dc8403e91f405a)

Extract files to a local folder you can remember.

#### Step 2: Create a New Project
Open ArcGIS Pro and sign in with your MOOC credentials.

Create a new Local Scene project called MOOC_ElevationLayers.

#### Step 3: Add "Before" Aerial Imagery
Add Imagery_Before.jpg from the Imagery folder.

If prompted, calculate statistics for the raster.

#### Step 4: Clip Scene to Data Area
Right-click Scene → Properties → Clip Layers.

Choose Clip To A Custom Extent, select Imagery_Before.jpg.

Set display units to US Feet, then apply and close.

#### Step 5: Remove Basemap
Right-click the Topographic basemap and remove it for cleaner rendering.

#### Step 6: Add DEM Elevation Surface
Right-click Ground under Elevation Surfaces → Add Elevation Source Layer.

Browse to Oso_Landslide_Data.gdb → Select DEM3ft_Before.

Notice improved realism in terrain rendering.

#### Step 7: Replace DEM with DSM
Remove DEM3ft_Before.

Add DSM3ft_Before as the new elevation surface.

Zoom in/out to observe differences in realism.

#### Step 8: Add "After" Imagery & DSM
Add Imagery_After.jpg from the Imagery folder.

Right-click Elevation Surfaces → Add Elevation Surface Layer → Rename it to After.

Right-click After → Add Elevation Source Layer → Select DSM4ft_After.

#### Step 9: Assign Imagery to Elevation Surface
Set Ground surface color to "No Color".

Assign Imagery_After.jpg to the After surface:

Right-click layer → Properties → Elevation tab

Set Features Are to "On Custom Elevation Surface"

Select After as the surface

Turn off these layers:

Imagery_Before.jpg

DSM3ft_Before

WorldElevation3D/Terrain3D

#### Step 10: Compare & Save
Switch between “before” and “after” layers to view changes.

Save your project.

## Maps Produced
### Before
![TerrainMap_before](https://github.com/user-attachments/assets/e78cc142-7498-46a4-b482-447f78435cc6)


### After
![TerrainMap_after](https://github.com/user-attachments/assets/72434faa-07dd-4f1b-b963-ac80fa50468d)

