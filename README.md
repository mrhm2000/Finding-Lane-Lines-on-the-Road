# Find Lane-Lines on the Road

### Overview
In this project I attempt to find lane line segments on road to guide self-driving car. The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle. 

Tools are used :
* Python
* OpenCV
* Anaconda
* Jupiter Notebook (*.ipynb)

### Pipeline
The goal of the pipeline is to compose several different operations together, apply them to an image, and produce an annotated image that shows where a lane on a road would be.

My pipeline consists of steps:
* Apply a color mask to suppress unwanted portion of images/videos
* Apply grayscale
* Performing edge detection
* Selecting regions to search for lane lines boundary
* Extrapolate line segments
* Apply Hough transform and draw line segments

### Original Image

<figure>
 <img src="test_images/solidWhiteCurve.jpg" width="380" alt="Combined Image" />
 <figcaption>
 <p></p> 
 </figcaption>
</figure>

### Image with White Mask

<figure>
 <img src="test_images_output/white_mask_out/white_mask_outsolidWhiteCurve.jpg" width="380" alt="Combined Image" />
 <figcaption>
 <p></p> 
 </figcaption>
</figure>

### Image with selected region

<figure>
 <img src="test_images_output/region_out/region_whiteCarLaneSwitch.jpg" width="380" alt="Combined Image" />
 <figcaption>
 <p></p> 
 </figcaption>
</figure>

### Image with Hough transformed

<figure>
 <img src="test_images_output/hough/hough_solidYellowLeft.jpg" width="380" alt="Combined Image" />
 <figcaption>
 <p></p> 
 </figcaption>
</figure>

### Images with Connecting Line Segments

<figure>
<img src="test_images_output/solidYellowCurve.jpg" width="380" alt="Combined Image" />
</figure>
<p></p> 
<figure>
 <img src="test_images_output/solidWhiteRight.jpg" width="380" alt="Combined Image" />
 <figcaption>
 <p></p> 
 </figcaption>
</figure>

### Reflection

Line successfully combined on video stream. However, numbers of flaw still occur specifically on challenge.mp4 video. Annotated version of video and images can be found on "test_video_output" and "test_images_output" folders.

### Potential shortcomings

The challenge video show couples flaws on methods as follow:
* Highly sensitive to color change of the environment
* Requires some hard coded variables
* Quality of result dependend on lane location on images

### Possible improvements
* Need more videos to train and improve pipeline
* Better methodology to determine sensitive variable on pipeline and adjust automatically
* Automatically calculate region of interest and color mask range

### Files
* Original images and videos on test_images and test_videos folder
* Processed images and videos on test_images_output and test_videos_output folder

