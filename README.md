# Cookbook

## The problem

It comes down to: I can't manage my cookbook in a text editor with a format that is purely textual.

Text is the ultimate format for making your data future proof. It's not copyrighted, has no drm, and can be read by (probably) every computer on earth.

There are a lot of recipe management programs in the world. Each of them stores recipe information in a different way. Some in databases of various types, some in XML files, probably some in every other type of format immaginable. All of them, even the FOSS ones (at least, the ones I know of), suffer from _having_ to use the program to get at the recipes.


## The solution

The goal of this project is simple (to say): it should manage recipe files and be able to extract and present meaningful information from the files.

This means:

  * It should be able to convert a recipe in any one of a number of known formats to the format of any other
  * It should also be able to read and write a purely textual format, based on markdown.
  * It should be able to generate an HTML compilation of recipes
  * It should be able to get a list of ingredients needed


## Goals

In the immediate future (of this project), my personal goals are:

  * Create a pre-determined arrangement of markdown to format recipes with
  * Convert a directory or single file to a static HTML "cookbook"
  * From a selection of recipes, pull a list of ingredients needed
  * Be able to email list of ingredients in an HTML format to be able to use checkboxes to mark recipes (IE create a shopping list viewable from a phone)

After I have those things working, I'd like to see the conversion portion of the program take shape.

How long will this take? I have no idea. This is just scratching an itch, so maybe it'll get done in a week, or maybe it'll take a couple of years. Feel free to create an issue for the project on github if you want to comment on something!


## Usage

Planned, at this point.

_Generate HTML cookbook_

    cookbook ./docs/samplebook book -o /tmp/samplebook.html

_Generate a list of ingredients and print it to stdout_

    cookbook ./docs/samplebook ingredients tacodip cheesypotatoes

_Generate a list of ingredients and output it to a file_

    cookbook ./docs/samplebook ingredients -o /tmp/ingredients.html tacodip cheesypotatoes

_Generate a list of ingredients and email it_

    cookbook ./docs/samplebook ingredients -e foo@bar.com tacodip cheesypotatoes

