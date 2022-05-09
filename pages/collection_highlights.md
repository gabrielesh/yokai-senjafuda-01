---
title: Collection Highlights
layout: about
permalink: /collection_highlights.html
---


# Collection Highlights

Here's a really neat image shared using the feature include:

{% include feature/image.html objectid="coll001" %}


Here's an image shared using standard markdown (works in Preview/GFM). On Friday it didn't work on the deployed website. Today it did briefly and then didn't again. Why?:
![Image I'm sharing with you](/objects/coll001.jpeg)

Here's an image shared using standard markdown with a full url (doesn't work in Preview/GFM):
![image shared using standard markdown with a full link]("https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg")

Here it is with size specified and a relative link (works in GFM):

<img src="/objects/coll001.jpeg" alt="first image in collection" width="200"/>

here it is with size specified and a full url (works in GFM):

<img src="https://github.com/gabrielesh/yokai-senjafuda-01/blob/main/objects/coll001.jpeg" alt="first image in collection" width="200"/>
