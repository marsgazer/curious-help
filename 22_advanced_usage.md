---
layout: page
title: Use(2)
#permalink: /about/
---


# How Do I Use X3D Viewer? (Advanced Usage)


## Navigation via URL Copy/Paste

### Open a stereo pair if you have only one image URL

If you have an URL of only one image, `x3dview` will try to find the other image, so that you will see a stereo pair.
The automatic search is file name-based.
You must select "Paste & Go (Both Panes)" in the menu.


<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/992c841d-3958-4e6e-af9d-5a4b391b1437"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
https://github.com/marsgazer/curious-help/assets/101140007/992c841d-3958-4e6e-af9d-5a4b391b1437


### Open a stereo pair if you have two image URLs

Just copy both URLs and select "Paste & Go (Both Panes)" in the menu.

The video also shows how to zoom the images and adjust offsets.

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/a9362db0-061e-4f9e-96a4-2f2116d49682"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
https://github.com/marsgazer/curious-help/assets/101140007/a9362db0-061e-4f9e-96a4-2f2116d49682





### Copy/Paste Thumbnail URL to Open Full-Scaled Image

Just like you can drag-and-drop a thumbnail image, you can copy-and-paste the address of a thumbnail image,
`x3dview` will load the corresponding full-scale image,
and if you select "Paste & Go (Both Panes)", `x3dview` will try to find the other image and show you a stereo pair.

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/c2d00867-363d-4d34-ba5d-5c0b0840caff"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
https://github.com/marsgazer/curious-help/assets/101140007/c2d00867-363d-4d34-ba5d-5c0b0840caff





## Making a stereo pair from any other source (e.g. the Opportunity rover)

`x3dview` does not support Opportunuty file names. Therefore, we copy&paste the left and right images separately,
choosing "Paste & Go (This Pane)" in the menu. Note that the right image goes to the left, this is X3D, cross-view 3D, we use RL stereo pairs!
(On the other hand, you can swap the images at any moment, there is a "Swap" button.)

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/fe41a643-d2c3-49a1-a416-9d1cb211e53c"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
https://github.com/marsgazer/curious-help/assets/101140007/fe41a643-d2c3-49a1-a416-9d1cb211e53c





## How do I find an artifact?

The Martian nature _loves_ right angles, parallel lines, and bizarre shapes.
It is relatively easy to find something that looks strange.

Strange objects tend to be located on hillsides, this is why we choose the photo of a hillside in the next video.

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/a235bccf-6ad1-4a67-bba5-b06a538672fa"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>

https://github.com/marsgazer/curious-help/assets/101140007/a235bccf-6ad1-4a67-bba5-b06a538672fa


## Hyperstereo

Hyperstereo is stereo taken from two distant points, probably at different moments in time.

Why "hyper"? To make a stereo image, you need two cameras, and the separation distance between the two cameras is called the stereo base.
When the stereo base is zero, this is no stereo.
When the stereo base is extraordinarily large, this is hyperstereo.

Wikipedia writes about [hyperstereo](https://en.wikipedia.org/wiki/Stereo_photography_techniques#Longer_base_line_for_distant_objects_%E2%80%93_%22Hyper_Stereo%22):
"If a stereo picture is taken of a large, distant object such as a mountain or a large building using a normal base it will appear to be flat. ...
For making stereo images featuring only a distant object (e.g., a mountain with foothills), the camera positions can be separated by a larger distance...
There are two main ways to accomplish this. One is to use two cameras separated by the required distance,
the other is to shift a single camera the required distance between shots."

"A common rule of thumb is the 1:30 rule. This means that the baseline will be equal to 1/30 of the distance to the nearest object included in the photograph."

This means that to make a hyperstereo image we need photos taken from two different points, not too far and not too close.
If these points are too close, there will be no depth, and if they are too far, it will be no good either, because your human brain will not combine the images.

`x3dview` supports making hyperstereo pairs by letting you adjust vertical and horizontal offsets, zoom factor, and rotation angle.



<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/19853f96-0eda-4c0f-8367-6ad02eebb0d5"
      width="800"
      height="600"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>

https://github.com/marsgazer/curious-help/assets/101140007/19853f96-0eda-4c0f-8367-6ad02eebb0d5







