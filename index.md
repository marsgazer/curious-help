---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
title: Curious: X3D Viewer
layout: home
---



This site contains documentation for `x3dview`, a.k.a. the Curious X3D Viewer. It is a stereo image viewer.
It has a number of features to support viewing the NASA images from Mars, but may be used with any other source of images.
It runs on Windows, Mac OS X and Linux.
It is free.
([Project](https://github.com/martianch/curieux) on Github;
[releases to download](https://github.com/martianch/curieux/releases))

## What does this software do and why

There is a trick that allows you to **view stereo images on the standard computer screen,** similar to viewing the "Magic Eye" images.
See the [Learn X3D](00_learn_x3d.html) section. See [freeviewing](https://en.wikipedia.org/wiki/Stereoscopy#Freeviewing) in Wikipedia.

X3D means "RL stereo pair", 3D means "stereoscopic", and X means that it is "cross-view", RL rather than LR.

The NASA Mars rovers (Curiosity, Perseverance) send stereo photos back to Earth, but the NASA site does not support viewing stereo pairs.

The Curious X3D Viewer allows you to view the Martian images in X3D right from the NASA site.

If you have stereo glasses and prefer LR stereo pairs, there is a "swap" button, so LR viewing is also supported. If you want to view images
from some source other than the NASA site, e.g. your hard disk, it is also possible.

This software also includes image effects like Bayer color decoding, resizing, rotating, color correction, and barrel distortion correction.

This is not the only software that can create stereo images; you may also have a look at Stereo Photo Maker.


## TOC

{% assign sorted_pages = site.pages | where_exp:"item", "item.name contains '_'" | sort:"name" %}
{% for node in sorted_pages %}
  <li><a href="{{site.baseurl}}{{node.url}}">{{node.title}}</a></li>
{% endfor %}

<p/>

## Feature list

Features:
- viewing images from the NASA site, from any other site, from the local disk
- opening images via drag-and-drop or address copy-paste
- automatic finding of the second half of a stereo pair, filename-based, for Curiosity and Perseverance images (but sometimes there is no pair)
- navigation among the raw images on the NASA site
- assembling big Perseverance 5K*3K images from parts
- navigation from an image to the related page on the NASA site
- shows RL (X3D) or LR stereo pairs
- shifting/rotating images either via controls or via marks that must match (useful for hyperstereo)
- improved Bayer pattern color decoding (bicubic, better(!) than the commonly used bilinear one)
- contrast stretching in RGB or HSV space
- gamma correction (encoding and decoding)
- fish-eye effect (barrel distortion) correction
- distance/size measurement via triangulation
- conversion of images for the red-blue (red-cyan) glasses into X3D
- viewing images with LR stereo pairs as X3D





