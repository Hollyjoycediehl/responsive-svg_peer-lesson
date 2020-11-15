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

## Adding the File

1. Now that you have <code>hauer-logo.svg</code> saved out, move this file into the <code>images</code> folder.

1. Next, open the <code>index.html</code> file and search for the <code>#main-svg</code>. Add the file name to complete the image path.

At this point, the logo should appear and fill the entire screen. It will scale with your screen size, but does not yet change format.

## Add CSS

1. Link in the <code>styles.css</code> page in the<code>head</code>

1. Move to the <code>styles.css</code> page and find the <code>#svg</code> tag. Instead of setting a pixel dimension for the svg, you will set a width so it can act responsively based on screen resolution. I found the range 30%-35% to be an appropriate size for a logo in the nav bar, but you can experiment with size if you choose to impliment this on a personal logo.

1. For now, set the width to <code>width: 35%</code>.

## Implimenting Responsive Formats

1. Open <code>hauer-logo.svg</code> in a text editor.

1. In the file, you should see three different groups of paths labeled <code>single</code>, <code>hauer</code> and <code>tagline</code>. These groups get carried over from the <code>.ai</code> file.

1. After the opening svg tag, add a new opening and closing <code>defs</code> tag. It should look like this: 

![Image of def tag](https://github.com/JuliaSchantz/responsive-svg_peer-lesson/blob/main/Images/Example_def%20tag.png)

This tag is used specifically for storing svg information and aids in the accessibility of the document.

1. Inside the <code>defs</code> tag, add an opening and closing <code>style</code> tag. This will house your responsive styles.

1. Next, we will hide or display groups based on our desired version of the graphic for each screen resolution.

1. I wanted the full logo at 1200px resolution, but decided to remove the tagline at the smaller resolutions. I used <code>display: block</code> and <code>display: none</code> to effect which layers would be displayed or removed as the screen lessened in resolution. Make sure to start by listing the higher resolutions first. The commands in the first <code>@media</code> will be cancelled out by the second <code>@media</code> and so on.

![Image of style tag](https://github.com/JuliaSchantz/responsive-svg_peer-lesson/blob/main/Images/Example_style%20tag.png)

1. Copy these settings or mess around with hiding other layers!

You can easily switch out a personal logo and follow these same steps to create your own unique responsive logo :)
