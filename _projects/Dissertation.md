---
layout: page
title: Master's Dissertation
description: Can a Compute Shader Octree Approach to Render Culling in Vulkan Increase Performance Compared to Traditional CPU-GPU Approach. 
img: 
importance: 2
category: work
giscus_comments: false
pdf: assets/pdf/Dissertation.pdf
---
{% if page.pdf %}
<a href="{{ page.pdf | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank">View Dissertation PDF</a>
{% endif %}

In a graphics pipeline, for every pixel on screen to be rendered, every vertice or triangle needs to be rendered so that the GPU knows which vertices are on screen and which aren't (This is called the Vertex Stage).
This information is then passed into the pixel shader, which is responsible for colouring the vertices within screen space, or the camera's view.

My dissertation stems from the vertex stage, where vertices are created and logged for later use.
But also stems from the Bounding Volume Heirarchy method, in which objects are divided into simple shapes for comparisons.


