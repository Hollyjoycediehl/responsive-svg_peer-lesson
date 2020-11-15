# Creating Responsive SVG Logos
<b> This is an instructional repository on how to create a responsive svg using Adobe Illustrator and CSS </b>

SVGs (scaleable vector graphics) can be used in place of other image file formats and easily enable graphics to have responsive abilities. This tutorial is focused on creating responsive svg logos that change format based on screen size. 

## Getting Started

1. Download and open the sample logo file, <code>sample_logo.ai</code> in Adobe Illustrator. 
   
1. Replicate the logo and determine simplified versions for tablet and mobile.
    * You will not use these replications, but they will help you envision the different logo states.
![Image of Step 2](https://github.com/JuliaSchantz/responsive-svg_peer-lesson/blob/main/Images/Step%202.png)
    
1. Open a new copy of <code>sample_logo.ai</code>. You will eventually save this file out as the svg.

1. Scale the artboard to tightly fit the logo. Be careful not to cut off any edges.

1. Group elements based on what you want to hide for the responsive versions determined in step 2.
![Image of Step 4](https://github.com/JuliaSchantz/responsive-svg_peer-lesson/blob/main/Images/Step%204.png)

1. Rename the existing groups to be more specific. Specific group names will make it easier to work with the svg later on, since you will need to know which layers you are hiding.

* Group 1 > <code>single</code>
* Group 2 > <code>hauer</code>
* Group 3 > <code>tagline</code>

## Exporting the File
After completing the previous steps, the file is now ready to be exported.

1. Go to:  File > Export as > Select Format: SVG > Export (save as <code>hauer-logo.svg</code>)

1. Make sure you have these settings:

![Image of Step 4](https://github.com/JuliaSchantz/responsive-svg_peer-lesson/blob/main/Images/Step%206.png)

## Adding and Implimenting the File

1. Now that you have <code>hauer-logo.svg</code> saved out, move this file into the <code>images</code> folder.

1. Next, open the <code>index.html</code> file and search for the <code>#main-svg</code>. Add the file name to complete the image path.

At this point, the logo should appear and fill the entire screen. It will scale with your screen size, but does not yet change format.


