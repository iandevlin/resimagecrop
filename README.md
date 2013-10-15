resimagecrop - RESS based solution for cropping images for responsive design
===================================================
- Author: Ian Devlin [iandevlin.com](http://iandevlin.com)
- Twitter: [@iandevlin](http://twitter.com/iandevlin)

Purpose
=======

There are many solutions out there for responsive images, and this is just another one.

Disclaimer
==========

This is most definitely a work in progress and lots of things can be done to improve it. Take it as a "proof of concept"

Features
========

- RESS based
- Allows cropping of images based on percentage x and y co-ordinates to aid art direction
- Images can also be scaled
- MIT license

Installation
=============

- Place `resimagecrop.php` in the root directory of your website (or anywhere else to be honest).
- Use it.

Usage
=====

Use `resimagecrop.php` in the `src` attribute of an `img` element with the following parameters:

- `image` the relative link to the original local image file
- `x` the percentage x co-ordinate value within the original image where a crop should begin
- `y` the percentage y co-ordinate value within the original image where a crop should begin
- `w` the pixel width of the original image that is to be cropped
- `h` the pixel height of the original image that is to be cropped
- `sc` the decimal scaling factor of the resulting image

Examples
========

`<img src="resimagecrop.php?image=img/saumur-castle-loire-valley-france.jpg&x=15&y=20&w=550&h=450" alt="A view of Saumur Castle in the Loire Valley in France" />`

This is interpreted as:
Take image `img/saumur-castle-loire-valley-france.jpg` and begin cropping it with dimensions 550x450 pixels, beginning from 15% from the top and 20% from the left.

`<img src="resimagecrop.php?image=img/saumur-castle-loire-valley-france.jpg&x=15&y=20&w=550&h=450&sc=0.2" alt="A view of Saumur Castle in the Loire Valley in France" />`

This is interpreted as:
Take image `img/saumur-castle-loire-valley-france.jpg` and begin cropping it with dimensions 550x450 pixels, beginning from 15% from the top and 20% from the left, and scale the resulting image by a factor of 0.2 (20%).


Known Issues
=============
- Only supports JPGs
- Doesn't save image file and therefore caching is not facilitated
- Probably lots of other stuff that you clever people will notice and point out to me.
