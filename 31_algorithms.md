---
layout: page
title: Algorithms
#permalink: /about/
---

This page describes algorithms used in `x3dview`.
If you are interested in using `x3dview`, it is absolutely safe to skip these documents.
On the other hand, you may be interested in algorithms rather than anything else.

{% assign pg = site.pages | where_exp:"item", "item.name contains 'demosaic'" | first %}
[Cubic/Bicubic Interpolation for Demosaicing of Bayer-Patterned Color Images]({{ site.baseurl }}{{ pg.url }})


Assembling a 5K image from parts (TBD)


