# DITA-SEMIA Image-Convert
This DITA-OT plugin can convert images used by DITA maps for HTML output as a preprocess step.

Since after installation the step will be executed for every(!) transtype the feature has to activated explicitly by setting the parameter dita-semia.image-convert.activate to true.


## Maintainance/Compatibility:
I'm using for our commercial publications. Thus, it is continiously maintained when . However, I'm not using github as main versioning system and will only occasionally this repository since I'm not aware of anybody else actually using it. So if you're interested in more frequent updates just let me know.

Also note that I'm not doing any testing with different DITA-OT version. Currently I'm using DITA-OT 2.4 so this is the only version I'm sure it is compatible with. But I expect little to no modification sbeing required to make it work at least with newer versions.


## Features:
- convert svg images to a raster format


## Parameters (ant properties):
- **dita-semia.image-convert.activate**

  Switch to activate this preprocessing step. Needs to be set to true.

- **dita-semia.image-convert.dest-format**

  Format to be generated when rasterizing svg images. Needs to be one of png, jpeg or tiff.

- **dita-semia.image-convert.dpi**

  Resolution of images, Default: 96dpi.

- **dita-semia.image-convert.delete-src**

  Delete the svg images after conversion. Default: true.

***NOTE:*** The preprocess step will not change the dita content to reference the rasterized images instead of the original SVG images. This needs to be done within the output stage. However, this plugin also provides custom transtypes that perform this step. But they are also meant to be samples to demonstrate how this can be integrated into your own custom output stage.
