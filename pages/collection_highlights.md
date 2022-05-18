---
title: Collection Highlights
layout: about
permalink: /collection_highlights.html
---


# Collection Highlights

The first image below is shared using a Liquid `include` as documented in the [About the About page](https://collectionbuilder.github.io/collectionbuilder-gh/about.html#about-the-about-page). Notice that the include centers the image differently than the markdown links below it. We recommend using includes because they do the following:
1.	figure out images based on "objectid", automatically finding the correct image src, alt, and link to item page for you (and avoid relative url issues)
2.	put the image in fairly complicated markup (that you can't do in Markdown, other than pasting html directly in) that ensures the image displays correctly in the page "theme".

{% include feature/image.html objectid="coll001" %}

Here's an image shared using standard markdown:
![Image I'm sharing with you](objects/coll001.jpeg)

Here's an image shared using standard markdown with a full url. When we tried this in class, we were using the link to the image in GitHub embededed in the larger 
GitHub page: [https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg](https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg). This doesn't work, because we need it to link *only* to the image. To find the "raw" link, right click (PC) or control click (Mac) on the image and choose "Open Image in a New Tab." You can then use the link of the image that appears in the new tab, which in this example is [https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg). Here's what it looks like:

![image shared using standard markdown with a full link](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg)

Here's an image shared with a Jekyll/Liquid specified relative url:
![alt text]({{ '/objects/coll001.jpeg' | relative_url }})

Here it is using html syntax with size specified and a relative url:

<img src="objects/coll001.jpeg" alt="first image in collection" width="200"/>

Here it is using html syntax with size specified and a full url:

<img src="https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg" alt="first image in collection" width="200"/>
