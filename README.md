# DITA-SEMIA Image-Convert
This DITA-OT plugin can convert images used by DITA maps for HTML output as a preprocess step.

Since after installation the step will be executed for every(!) transtype the feature has to activated explicitly by setting the parameter dita-semia.image-convert.activate to true.

## Features:
- convert svg images to a raster format


## Parameters (ant properties):
- **dita-semia.image-convert.activate**

  Switch to activate this preprocessing step. Needs to be set to true.

- **dita-semia.image-convert.dest-format**

  Format to be generated when rasterizing svg images. Needs to be one of png, jpeg or tiff.


***NOTE:*** The preprocess step will not change the dita content to reference the rasterized images instead of the original SVG images. This needs to be done within the output stage. However, this plugin also provides custom transtypes that perform this step. But they are also meant to be samples to demonstrate how this can be integrated into your own custom output stage.
