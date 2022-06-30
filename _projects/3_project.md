---
layout: page
title: Anomalous transport 
description: Monte Carlo study of long-range interactions as a mechanism for anomalous electron transport in strongly correlated systems. 
img: assets/img/anomalous-transport.jpg
importance: 2
category: thesis 
---

Uncovering the mechanism underlying anomalous electronic transport is one of the main challenges facing the condensed matter physics community today. 
Generally speaking, anomalous (or "bad") metals are classified as those whose resistivity exceeds the Mott-Ioffe-Regel (MIR) limit as the temperature increases. 
This limit arises from a description of electron transport that is based upon scattering and the limiting resistivity is calculated as that achieved when one considers the shortest allowable scattering length. 
This minimal scattering length is typically considered to be the lattice spacing for any given system.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/mir-limit.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    So-called bad metals exceed the MIR limit as a function of temperature, while the resistivity of conventional metals saturate at, or before, this limiting value.
</div>

In the standard Drude model of conductivity, the resistivity is calculated as the inverse of the DC conductivity value, $$\rho = 1/\sigma_{DC}$$.
When disorder is added to a system, the scattering rate tends to increase which means that the DC conductivity value decreases, thereby increasing the resistivity. 
This increase typically does not exceed the MIR limit. 
However, when a system has disorder and strong quantum interferences, then [Anderson localization](https://en.wikipedia.org/wiki/Anderson_localization) can occur in which the electrons are unable to move, or to transport.
This localization phenomenon causes the DC value to drop to zero, thereby leading to infinite resistivity.

Between the standard picture of Drude conductivity and the extreme case of Anderson localization, there ought to lie another picture of electron transport--one in which the electrons are almost localized. 
In this picture, the DC value would be smaller than expected in the conventional Drude framework, but still non-zero.
This reduction in the DC value could provide a plausible mechanism to explain anomalous resistivity patterns observed in various bad metallic systems. 

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/drude-anderson-almost-localized.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Illustration of the three regimes of electrical conduction: conventional Drude transport (black), Anderson localization (green), and the proposed "almost-localized" transport (blue). 
</div>

Indeed, the decrease of the DC value of the conductivity could lead to the development of a displaced Drude peak, another signature of anomalous metallic transport. 
Interestingly, this displaced Drude peak, or DDP, is not observed in all bad metals and has escaped a theoretical understanding thus far. 

In order to examine the effect of long-range interactions on electron transport, we established a project using classical Monte Carlo simulations.
This technique enables us to study much larger system sizes than in our previous exact diagonalization study. 
We also updated our long-range interacting model to include on-site interactions, or the $$U$$ term from the Hubbard model.

{% comment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal it's glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
{% endcomment %}
