# STAC_Portal_Products

These product notebooks and Python scripts are based off the notebooks created
for the IPP Common Sensing Project. The Common Sensing notebooks relied on data
loaded into the Open Data Cube, while the notebooks and scripts in this repository 
no longer use datacube functions (with the exception of the geomedian notebook, which uses the xr_geomedian function from odc.algo). 

The functions to read the GeoTIFFs as arrays, stack, align, and resample them, etc. are located in notebook_functions.py, along with cloud and water masking functions.  Functions for fractional_coverage_classifier and shoreline extraction functions from Satellite Applications Catapult are located in utilities.py. 

## File Structure:
AncillaryData -> folder contains endmembers_landsat.csv, which is used for fractional coverage classifying.

Notebooks -> folder contains Jupyter Notebooks (.ipynb) of each of the products. The Shoreline Extraction product was created based on ancillary tide data produced for Fiji, Vanuatu and the Solomon islands, so this product has not yet been generalized from the Common Sensing version.

PyScripts -> folder contains the products written as Python scripts rather than notebooks. 

output -> folder contains the outputs created from running the Python scripts. The outputs are included here for reference and testing. 

notebook_functions.py -> Contains functions created to allow the notebooks to run similarly to how the Common Sensing notebooks ran using the Open Data Cube. These functions mostly rely on xarray functions to align, resample and stack arrays so they can be used for analysis. This file also contains the cloud and water masking functions based on the Landsat pixel_qa band.

utilities.py -> Contains functions from Satellite Applications Catapult, including the shoreline extraction functions and fractional coverage classifier function. 