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

Above is the PDF of my dissertation, it didn't get the results I wanted but was informative anyways

Below is a brief of what I did for my dissertation, pros, cons, etc. 

In a graphics pipeline, for every pixel on screen to be rendered, every vertice or triangle needs to be rendered so that the GPU knows which vertices are on screen and which aren't (This is called the Vertex Stage).
This information is then passed into the pixel shader, which is responsible for colouring the vertices within screen space, or the camera's view.

My dissertation stems from the vertex stage, where vertices are created and logged for later use.
But also stems from the Bounding Volume Heirarchy method, in which objects are divided into simpler shapes for different comparisons.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IrregularShape.png" title="irregular shape image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IrregularShapeCircle.png" title="irregular circle image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IrregularShapeRect.png" title="irregular rect image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Take an irregular shape like in the first image above and compare it to a small circle and a large rectangle.
For an example of BVH, let's call this a collision test using this method.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/CircleMovement.png" title="irregular shape image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/RectMovement.png" title="irregular circle image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Both of these objects want to go past the irregular object.
However they need to be checked for collisions, because the shape is an obstacle of some kind.
There are two ways this can happen; either every vertex is checked against the object, or the shape is split up into easier shapes to compare.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IrregularShapeVertices.png" title="irregular shape image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IrregularShapeBVH.png" title="irregular circle image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
The images above show this: with the first highlighting every vertex for comparison, and the second being split up into smaller and smaller squares.

