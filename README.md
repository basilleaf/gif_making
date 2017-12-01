## Finding the images

The gifs I've made here are made with still images I found using (@PDSopus)[https://twitter.com/pdsopus]. Cassini space probe is a good candidate for easy gif-making as it was a very stable camera platform. Here is a short screencast showing how to use OPUS to browse Cassini images and download sequences that might make good animated gifs.

## Making animated gifs with Gifsicle and Imagemagick

[Gifsicle](https://www.lcdf.org/gifsicle/) makes it easy to create gifs and resize them as well, handy when trying
to get the gif down to a share-able size (3MB limit for twitter)

Gifsicle requires gifs as input though, so Imagemagick comes into play when you need
to do file conversions as well, like when you have a collection of jpegs you want to
animate you'll have to convert them to gif first. Fortunately you can use Imagemagick
and pipe them directly into gifsicle in the same command:

Create an animated gif from jpegs and resize the resulting gif:

	convert *.jpg gif:- | gifsicle --delay=10 --loop  --resize 600x600 > anim.gif

View in Chrome:

	open -a Google\ Chrome anim.gif


## Installing

Image Magic:
see http://cactuslab.com/imagemagick/

gifsicle:

	npm install --global gifsicle
