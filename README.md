# prospectivity-online-tool

## Description

Web pages for a JavaScript tool that allows users to perform real time online calculations applied to multiband raster data. Each file represents a different deposit model.

## Usage

The tool allows users to modify calculation values through sliders. These calculation values change the significance of certain variables, which will then affect the pixel colours of the rendered GeoTIFF image. By modifying these values, the user can choose which variables they believe are the most significant and quickly display an updated version of the GeoTIFF that represents these changes. 

![alt text](https://github.com/mvalenta100/prospectivity-online-tool/blob/main/README-images/coefficient_sliders.png?raw=true)

The first 4 sliders allow the user to change the overall significance of the source, driver, path, and trap variables. For example, if the user thought that the source variables were irrelevant, they could drag the "src" slider to 0 and this would remove the pixel colour from all source variables. The default value for these four sliders is set to 1. 

![alt text](https://github.com/mvalenta100/prospectivity-online-tool/blob/main/README-images/dropdown_menu.png?raw=true)

The user can select which category of variable they would like to edit from the drop down menu.

![alt text](https://github.com/mvalenta100/prospectivity-online-tool/blob/main/README-images/source_category.png?raw=true)

In the above image, the source category is selected. 
* S1 and S2 represent the source variables for the selected deposit model
* Imp, App and Con represent the importance, applicability, and confidence values for each variable
* The "Overall" value represents the overall significance value of the variable - calculated by multiplying the importance, applicability, and confidence values

![alt text](https://github.com/mvalenta100/prospectivity-online-tool/blob/main/README-images/buttons.png?raw=true)

The "Show Low Res Tiff" button allows the user to render the GeoTIFF very quickly with lower image resolution. 

The "Show High Res Tiff" button renders a much higher resolution GeoTIFF image; however, loading times can be significantly slower compared to the lower resolution files.

## Data source and format

For the low resolution images, standard GeoTIFF files are used. For higher resolution images, COG (Cloud Optimized GeoTIFF) files are used to decrease overall file size and reduce loading times without sacrificing image quality. 

For more information about COG files visit - https://www.cogeo.org/

## Acknowledgements

This tool uses open source code based on georaster-layer-for-leaflet of Daniel J Dufour - https://github.com/GeoTIFF/georaster-layer-for-leaflet
