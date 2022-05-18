---
title: Collection Highlights
layout: about
permalink: /collection_highlights.html
---


# Collection Highlights

This page offers a detailed review of the code that creates image links in Markdown.

### Liquid `include`
The first image below is shared using a Liquid `include` as documented in the [About the About page](https://collectionbuilder.github.io/collectionbuilder-gh/about.html#about-the-about-page). Notice that the include centers the image differently than the markdown links below it, and includes the title of the image below it. We recommend using includes because they do the following:
1.	figure out images based on "objectid", automatically finding the correct image src, alt, and link to item page for you (and avoid relative url issues)
2.	put the image in fairly complicated markup (that you can't do in Markdown, other than pasting html directly in) that ensures the image displays correctly in the page "theme". 

The code is `{% raw %}{% include feature/image.html objectid="coll001" %}{% endraw %}` and it looks like this:

{% include feature/image.html objectid="coll001" %}

### Standard Markdown
Here's an image shared using standard markdown `![Image I'm sharing with you](objects/coll001.jpeg)`
![Image I'm sharing with you](objects/coll001.jpeg)

### Standard Markdown with Full URL
Here's an image shared using standard markdown with a full url. When we tried this in class, we were using the link to the image in GitHub embededed in the larger 
GitHub page: [https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg](https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg). This doesn't work, because we need it to link *only* to the image. To find the "raw" link, right click (PC) or control click (Mac) on the image and choose "Open Image in a New Tab." You can then use the link of the image that appears in the new tab, which in this example is [https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg). Here's the code and image: `![image shared using standard markdown with a full link](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg)`

![image shared using standard markdown with a full link](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg)

### Jekyll/Liquid specified Relative URL
Here's an image shared with a Jekyll/Liquid specified relative url: `{% raw %}![alt text]({{ '/objects/coll001.jpeg' | relative_url }}){% endraw %}`
![alt text]({{ '/objects/coll001.jpeg' | relative_url }})

### HTML Syntax with Image Size and Relative URL
Here it is using html syntax with a relative url. HTML allows one to specify the size of the images outside of how size is specified in the Jekyll *theme*: `<img src="objects/coll001.jpeg" alt="first image in collection" width="200"/>`

<img src="objects/coll001.jpeg" alt="first image in collection" width="200"/>

### HTML Syntax with Image Size and Full URL
Here it is using html syntax with size specified and a full url: `<img src="https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg" alt="first image in collection" width="200"/>`

<img src="https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg" alt="first image in collection" width="200"/>

## Potential Challenges
The only tricky part of using relative paths is ensuring they are actually going to be correct when the site builds out. So the relative paths above will work if used on pages/about.html, but wouldn't be correct on "pages/about/part1.html". If you use
![alt text](/objects/example.jpg)
it will work if you site is at the root of its domain (e.g. evanwill.github.io/about.html), but not if your site is in a subfolder (which most github pages projects are, e.g. evanwill.github.io/example-collection/about.html).
To avoid issues, the best way is to use either the Liquid `relative_url` or `include`, both of which will work anywhere on the site.
 
