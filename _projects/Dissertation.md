---
layout: page
title: Master's Dissertation
description: Can a Compute Shader Octree Approach to Render Culling in Vulkan Increase Performance Compared to Traditional CPU-GPU Approach. 
img: 
importance: 2
category: work
giscus_comments: true
---

In a graphics pipeline, for every pixel on screen to be rendered, every vertice or triangle needs to be rendered so that the GPU knows which vertices are on screen and which aren't (This is called the Vertex Stage).
This information is then passed into the pixel shader, which is responsible for colouring the vertices within screen space, or the camera's view.

My dissertation stems from the vertex stage, where vertices are created and logged for later use.
But also stems from the Bounding Volume Heirarchy method, in which objects are divided into simple shapes for comparisons.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

