---
layout: post
title: How to easily resize images in the OS X terminal.
excerpt: "A super-easy step to resize images in the terminal."
modified: 2016-07-08
categories: blog
tags: [resize, image, images, OS X, terminal, sips]

---

Many times I've needed to resize images. Usually it's been a tedious process, especially if there were a ton of images to process.

Recently, I needed to resize about 300 images for a blog. All I had were the source images and wanted to quickly resize them so that at most, they were 640px wide. Seemed like an easy enough task but I knew there had to be a simple way.

Then I [found this](http://lifehacker.com/5962420/batch-resize-images-quickly-in-the-os-x-terminal):

{% highlight bash %}
sips -Z 640 *.jpg
{% endhighlight %}

The above command will resize all images in the current folder and resample the image so that the height and/or width do not exceed 640px.

Here's a look at the options for sips:

{% highlight bash %}
NAME
     sips -- scriptable image processing system.

SYNOPSIS
     sips [image-query-functions] imagefile ...
     sips [profile-query-functions] profile ...
     sips [image-modification-functions] imagefile ... [--out result-file-or-dir]
     sips [profile-modification-functions] profile ... [--out result-file-or-dir]

DESCRIPTION
     This tool is used to query or modify raster image files and ColorSync ICC profiles.  Its functionality can also be used through the "Image Events"
     AppleScript suite.

FUNCTIONS
     Profile query functions:

     -g key
     --getProperty key
           Output the property value for key to stdout.

     -X tag tagFile
     --extractTag tag tagFile
           Write a profile tag element to tagFile.

     -v
     --verify
           Verify any profile problems and log output to stdout.

     Image query functions:

     -g key
     --getProperty key
           Output the property value for key to stdout.

     -x profile
     --extractProfile profile
           Get the embedded profile from image and write it to profile.

     Profile modification functions:

     -s key value
     --setProperty key value
           Set a property value for key to value.

     -d key
     --deleteProperty key
           Remove a property value for key.

     --deleteTag tag
           Remove the tag element from a profile.

     --copyTag srcTag dstTag
           Copy the srcTag element of a profile to dstTag.

     --loadTag tag tagFile
           Set the tag element of a profile to the contents of tagFile.

     --repair
           Repair any profile problems and log output to stdout.

     Image modification functions:

     -s key value
     --setProperty key value
           Set a property value for key to value.

     -d key
     --deleteProperty key
           Remove a property value for key.

     -e profile
     --embedProfile profile
           Embed profile in image.

     -E profile
     --embedProfileIfNone profile
           Embed profile in image only if image doesnt have a profile.

     -m profile
     --matchTo profile
           Color match image to profile.

     -M profile intent
     --matchToWithIntent profile intent
           Color match image to profile with rendering intent perceptual | relative | saturation | absolute.

     --deleteColorManagementProperties
           Delete color management properties in TIFF, PNG, and EXIF dictionaries.

     -r degreesCW
     --rotate degreesCW

     -f horizontal|vertical
     --flip horizontal|vertical

     -c pixelsH pixelsW
     --cropToHeightWidth pixelsH pixelsW
           Crop image to fit specified size.

     -p pixelsH pixelsW
     --padToHeightWidth pixelsH pixelsW
           Pad image with pixels to fit specified size.

     --padColor hexcolor
           Use this color when padding. White=FFFFFF, Red=FF0000, Default=Black=000000

     -z pixelsH pixelsW
     --resampleHeightWidth pixelsH pixelsW
           Resample image at specified size. Image apsect ratio may be altered.

     --resampleWidth pixelsW
           Resample image to specified width.

     --resampleHeight pixelsH
           Resample image to specified height.

     -Z pixelsWH
     --resampleHeightWidthMax pixelsWH
           Resample image so height and width arent greater than specified size.

     -i
     --addIcon
           Add a Finder icon to image file.
{% endhighlight %}

You can find more by looking at the man page for sips.
