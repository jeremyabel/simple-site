# simple-site

## Basic Layout
This is a simple responsive site built using Bourbon / Neat's column layout system. The site is segmented into 12 equal-width columns which are centered in the browser. The total width of the 12 columns is defined in `/scss/_grid-settings.scss`. The default configuration is 1280px wide. The size of all elements of the site are defined in terms of numbers of columns, using classes from `one-span` to `ten-span`. Centered versions are named with `-center` at the end, like `one-span-center` to `ten-span-center`. Relative sizes are specified using four fractional classes: `full-span, half-span, third-span, & quarter-span`. Elements with these classes will take up the corresponding percentage of their parent containers.  

## Typography
Font choices sizes, and colors are set in `/scss/_typography.scss`. Gooogle Fonts are used; the default base font is Open Sans, and the default sans-serif font is Inknut Antiqua. I picked these because they were the ones we used for the Genesis Noir site, and this site is just the Genesis Noir site with all the specific content taken out. To change the fonts, use the [Google Fonts](https://fonts.google.com/) site to pick new ones and replace the `fonts.googleapis.com` link in the `<head>` portion of the HTML.

## Responsiveness
This site will resize gracefully when you shrink the window down. Multi-column layouts will transform into single-column layouts. You shouldn't need to mess with any of this but let me know if there's a specific thing you want mobile to do and I can try and help.

## Some notes about SASS
Sass is an extension of CSS which adds a bunch of features like variables and functions. Mostly I use variables, which are usually written at the top of a file starting with a `$`, like `$base-font-size: 10px`. All dimensions for the site are determined using the `modular-scale()` function, which does some [weird math](https://blog.envylabs.com/responsive-typographic-scales-in-css-b9f60431d1c4) with the golden ratio or some such to size things in a unified way or something, it's a bunch of design hippy bullshit but it's easier to use than manually inputting pixels for everything. Basically it allows you to tweak the spacing and sizing of everything using one variable, `$modular-scale-base` which is in `/scss/_grid-settings.scss`

Oh also SASS can do importing of files too, which is why there's a bunch of files that start with an underscore. For some reason I cannot be bothered to look up, imported files must start with an underscore, so there's that.