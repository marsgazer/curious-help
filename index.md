---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Curious: X3D Viewer

## This site is under construction !!!!!

This site contains documentation for the Curious X3D Viewer. ([Download](https://github.com/martianch/curieux))

### What does this software do and why

There is a trick that allows you to view RL stereo pairs on the screen, similar to viewing the "Magic Eye" images. See the "Learn X3D" section.

X3D means "RL stereo pair", 3D means "stereo" and X means that it is "crossed", RL rather than LR.

The NASA Mars rovers (Curiosity, Perseverance) send stereo photos back to Earth, but the NASA site does not support viewing sereo pairs.

The Curious X3D Viewer allows you to view the Martian images in X3D right from the NASA site.

If you have stereo glasses and prefer LR stereo pairs, there is a "swap" button, so LR viewing is also supported. If you want to view images
from some source other than the NASA site, e.g. your hard disk, it is also possible.

This software also includes image effects like Bayer color decoding, resizing, rotating, color correction, and barrel distortion correction.

This is not the only software that can create stareo images; you may also have a look at Stereo Photo Maker (aka SPM).

### TOC

{% assign sorted_pages = site.pages | where_exp:"item", "item.title != nil" | where_exp:"item", "item.name.match('^\\d\\d_')" | sort:"name" %}
{% for node in sorted_pages %}
  <li><a href="{{node.url}}">{{node.title}}</a></li>
{% endfor %}

### pages

###{
###{
sorted_pages
###}
###}



