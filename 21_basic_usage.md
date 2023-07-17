---
layout: page
title: Use(1)
#permalink: /about/
---


# How Do I Use X3D Viewer?

## Drag and Drop

Run `x3dview`.

Open [this link](
https://mars.nasa.gov/msl/multimedia/raw-images/?order=sol+desc%2C+date_taken+desc%2Cinstrument_sort+asc%2Csample_type_sort+asc&per_page=100&page=0&mission=msl
) or [this link](
https://mars.nasa.gov/mars2020/multimedia/raw-images/
)
in the browser. (You can find them on the help page.)

Drag an image thumbnail from the browser's window, and drop it onto the x3dview window.

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/897ca300-ca1d-43f9-9d98-787f06f0218f"
      width="840"
      height="525"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
<div style="color:transparent">
https://github.com/marsgazer/curious-help/assets/101140007/897ca300-ca1d-43f9-9d98-787f06f0218f
</div>

Note: if you click the links on the help page, they will open in the default browser.
If you have many browser windows, my advice is to switch to the window where the link must open (opening a new window will work too),
and only then click the link in the help page. The link will open in the most recently used window of the default browser.

Note: Drag-and-Drop does not work under Linux with Chrome-based browsers. This is not a `x3dview` bug, it is either Chrome or Java bug.
(It's unlikely that they are going to fix it because each of them has got somebody else to blame. So do I, but no Java program
can see what is dragged from Chrome under Linux, so it's not my bug.) Firefox is ok.


## If you see only one image

Two reasons:

1. There is no pair for that image
2. The checkbox "DnD to Both" is not checked. (You can toggle it with Alt+B if you prefer keyboard.)

## Marks

You can set marks on the image. There are 5 marks: red (Alt+1 or Alt+R), green (Alt+2 or Alt+G), blue (Alt+3), cyan (Alt+4), magenta (Alt+5).

To set, for example, red marks on some object, you click Alt+R, the cursor turns into a crosshair, you click the mouse on some point of the object.
Then you click Alt+R again, the cursor turns into a crosshair, you click the mouse in the other pane on the same point of that object.

The marks are not interchangeable, different marks play different role.
You can use marks to adjust offsets (to make the same set of objects visible in both panes), zoom factor, rotation angle; to measure distances,
to calibrate distance measurement, and to calibrate barrel distortion correction.

## Adjust offsets using marks

You can adjust offsets using either red or green marks.

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/7c7f6c93-1cb8-4afa-a7c0-26e8f3feebcf"
      width="840"
      height="525"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
<div style="color:transparent">
https://github.com/marsgazer/curious-help/assets/101140007/7c7f6c93-1cb8-4afa-a7c0-26e8f3feebcf
</div>



## Adjust brightness and/or colors


<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/b205f276-83df-4cf5-a23b-f4180db96020"
      width="840"
      height="525"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>
<div style="color:transparent">
https://github.com/marsgazer/curious-help/assets/101140007/b205f276-83df-4cf5-a23b-f4180db96020
</div>




