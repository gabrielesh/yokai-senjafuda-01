---
title: Collection Highlights
layout: about
permalink: /collection_highlights.html
---


# Collection Highlights

Here's a really neat image shared using the feature include. Notice that the include centers the image differently :

{% include feature/image.html objectid="coll001" %}

Here's an image shared using standard markdown:
![Image I'm sharing with you](objects/coll001.jpeg)

Here's an image shared using standard markdown with a full url:
![image shared using standard markdown with a full link](https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg)

Here's an image shared with a relative url
![alt text]({{ '/objects/coll001.jpeg' | relative_url }})

Here it is with size specified and a relative link (works in GFM):

<img src="objects/coll001.jpeg" alt="first image in collection" width="200"/>

here it is with size specified and a full url (works in GFM):

<img src="https://raw.githubusercontent.com/gabrielesh/yokai-senjafuda-01/main/objects/coll001.jpeg" alt="first image in collection" width="200"/>
