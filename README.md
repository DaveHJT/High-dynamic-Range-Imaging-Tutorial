# High-Dynamic-Range-Tutorial
 A tutorial of implementing the Debevec-Malik method and obtain the HDR image.
 
## Background

### Abstract
<p>
When a photograph is taken by a camera, only a very limited range of radiance values can be
captured, so it's common for a photo to be overexposed or underexposed. In the areas that are
too bright or too dark, the information is lost, since the range of radiance values is very limited.
 </p>

<p>
Here we implement the Debevec-Malik method in order to solve this problem. This method is
introduced in the paper "Recovering High Dynamic Range Radiance Maps from Photographs"
[2]. The main idea is taking several photos with different exposure, recover the Camera
Response Function(CRF), and with the CRF, we can merge the photos with different exposures
together to form a radiance map, where the pixel values are proportional to the real radiance of
the scene where these photo are taken. Then the final objective is getting one image that
preserves all the details of the brightest and darkest parts in the input images.
</p>

### Result Demo
#### Source Images
<p>
<img src="https://raw.githubusercontent.com/DaveHJT/High-dynamic-Range-Imaging-Tutorial/main/images/cannon-2EV.jpeg" width="300">
<img src="https://raw.githubusercontent.com/DaveHJT/High-dynamic-Range-Imaging-Tutorial/main/images/cannon%2B0EV.jpeg" width="300" >
<img src="https://raw.githubusercontent.com/DaveHJT/High-dynamic-Range-Imaging-Tutorial/main/images/cannon%2B2EV.jpeg" width="300">
</p>

#### HDR Radiance Map & tonemapped LDR result
<p>
<img src="https://raw.githubusercontent.com/DaveHJT/High-dynamic-Range-Imaging-Tutorial/main/images/radiance%20map.png" width="300">
<img src="https://raw.githubusercontent.com/DaveHJT/High-dynamic-Range-Imaging-Tutorial/main/images/tonemapped%20LDR%20result.png" width="300" >
</p>

## Install

Open "High-dynamic range imaging tutorial.ipynb" in jupyter notebook and run each block of code from step to step. 
Or read the "High-dynamic range imaging tutorial.pdf" which contains the same code and result.
This project uses [cv2](https://pypi.org/project/opencv-python/). Go check them out if you don't have them locally installed.

```sh
$ pip install opencv-python
```

## License
None
