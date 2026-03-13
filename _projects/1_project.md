---
layout: page
title: Vector-Valued Optimal Transport
description: Using OT methods to compare classifiers
img: assets/img/OT.jpg
importance: 1
category: work
related_publications: false
---

In this project under Dr. Katy Craig, we use vector-valued optimal transport to compare classifiers. More specifically, if there are $N$ bins which categorize $784$-pixel images, then we consider $N$ different measures, each supported on $\mathbb R^{784}$. From there, we combine these $N$ measures into one by lifting them to a simplex, where the pairwise distance between edges on the simplex is determined by a similarity score for the labels. Then, given two measures on the simplex -- in other words, two classifiers' performances on datasets of the same type -- we can calculate the distance between the classification that those two classifiers made. What is exciting about this approach is that, compared to current methods, like the confusion matrix, vector-valued optimal transport can pick up on two images being very similar. This means that if two images have labels swapped but are qualitatively similar, then VVOT will determine that this is not as bad as if two images have labels swapped but are qualitatively very different; on the other hand, the confusion matrix is agnostic to such changes. Furthermore, VVOT methods allow us to compare classifiers on unordered datasets as well as classifiers which were tested on different datasets, both of which are limitations with the existing confusion matrix. Stick around to see continued progress on this ongoing project! :) 

{% raw %}
```html
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/VVOT.jpg" title="MNIST Example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Here, we can observe how image similarity plays a role in the VVOT methods.
</div>
```
{% endraw %}

