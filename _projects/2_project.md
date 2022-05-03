---
layout: page
title: Zero temperature
description: Exact diagonalization study of long-range interactions in quantum lattice models at zero temperature. 
img: assets/img/Estimate-pinball-Wigner-metal.jpg
importance: 1
category: thesis 
---

In late 2018, I started my Ph.D. investigating the fundamental question of how long-range interactions impact the physics in strongly correlated systems.
As with any complicated project, my advisors and I needed a (relatively) controlled starting point into order to begin answering the smaller, more concrete questions contained within the framework of our work.
This entailed fixing the dimensionality and lattice geometry that we wanted to investigate, as well as simplifying other degrees of freedom.

With the quarter-filled organic salt family, $$\theta$$-ET$$\_{2}$$X as our inspiration, we decided to study a triangular lattice system with only charge degrees of freedom.
The quarter-filling and the prohibitive cost for any two particles to share a site justified our deliberate choice to neglect the spin degrees of freedom. 

These choices enabled us to write down the following Hamiltonian in second quantization to describe the energetic processes underlying our system:

\begin{equation}\label{eq:long-range-Hamiltonian}
H = -t \sum\_{\langle ij \rangle} \big( \hat{c}^{\dagger}\_{i} \hat{c}\_{j}^{} + h.c. \big) + \frac{V}{2} \sum\_{ij} \frac{ ( \hat{n}\_{i} - \bar{n} )( \hat{n}\_{j} - \bar{n} ) }{ R\_{ij} }.
\end{equation}

The first term details the kinetic energy which the system gains by means of "hops" between nearest-neighbor sites. The second term describes the electrostatic interactions of a configuration of charges where the parameter $$\alpha$$ controls the range of the interactions. The value $$\alpha=1$$ corresponds to the pure, unscreened Coulomb repulsion and $$\alpha \rightarrow \infty$$ corresponds to the limit with only nearest-neighbor interactions.

With this Hamiltonian established, we employed a technique called **exact diagonalization** to examine the ground state of the system as a function of the interaction range, interaction strength, and system size. 
This technique is quite common in condensed matter physics and consists of diagonalizing a matrix corresponding to the Hamiltonian computed for a given basis of states.

In our case, we fixed the size of the system (the number of sites on the lattice) and established the basis of states by considering all possible charge configurations for a half-filled spinless system.
For each state (charge configuration), we fill in the appropriate elements of the Hamiltonian matrix that correspond to the electrostatic interactions (diagonal elements) and the kinetic hopping processes (off-diagonal elements).
Finally, the matrix is diagonalized and any observables of interest, such as charge correlation, are computed to provide insight into the nature of the ground state. 

Exact diagonalization is a powerful technique as it provides microscopic control over all parameters and accounts for all of the electronic correlation.
However, it is limited to small system sizes as the basis size, and thereby the computational cost, grows exponentially with the system size.
As we are forced to work with relatively small system sizes, we additionally needed to employ two strategies designed to minimize finite-size effects--twisted boundary conditions and Ewald summations.
A more detailed explanation of these highly technical points can be found in [my dissertation](https://hal.archives-ouvertes.fr/tel-03626120), but for the present discussion, it suffices to say that twisted boundary conditions and Ewald summations reduce finite-size errors arising from the kinetic and potential terms of the Hamiltonian, respectively. 

With the technical points resolved, we can now turn our attention to the results obtained by diagonalizing the Hamiltonian in Eq. \eqref{eq:long-range-Hamiltonian}. 
First, we establish the phase diagram by computing the Drude weight as a function of varying interaction range and strength. 
The Drude weight characterizes the charge stiffness in a system and can be used to classify metallic or insulating regions in the phase diagram. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/phase-diagram.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Phase diagram as a function of interaction range and strength of interactions (left). Evolution of the Drude weight and the quasiparticle weight as a function of interaction strength for the pure long-range case (right).
</div>

Across all values of interaction range $$\alpha$$, we observed a "normal" metal for low values of interaction strength, $$V/t$$. 
This corresponds to the top, dark blue region of the phase diagram in the left panel above. 
We also found that as the interaction strength is increased in systems with short-range interactoins, then this normal metal transitions into a phase known as the pinball liquid (righthand side of left panel).
This phase corresponds to a splitting of the electronic density into one portion that is "pinned" to the lattice and another portion that flows over the remaining lattice sites ("balls").
As this phase only occurs for short-ranged interactions and has been the subject of [other studies](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.74.193107), we shall not concern ourselves any further with it.

Instead, we shall focus our attention on the case of pure, Coulomb long-range interactions which corresponds to the case $$\alpha=1$$.
As can be seen in the phase diagram above, the normal metal transitions instead to a correlated metal as the interaction strength is increased.
Eventually, the repulsive nature of the electronic interactions completely dominates the kinetic processes and the system settles into a stripe-ordered, insulating phase.
This phase is also called a Wigner crystal as it arises from long-range interactions.
The right panel of the figure above shows not only the decrease of the Drude weight at the approach of the metal-insulator transition, but also that of the quasiparticle weight.
Both quantities, although computed in different ways from the diagonalization, agree well and signal that the electronic correlation is building up with the increase in interaction strength, $$V/t$$.

Another quantity that provides us with a measure of electron correlation is the single-particle spectral function, $$A(\omega)$$. 
This quantity is shown in the figure below and we clearly observe the development of a pseudogap as the interaction strength $$V/t$$ increases to its value at the metal-insulator transition, $$(V/t)\_{c} \approx 30$$.

At this point, it is worth pointing out that our discovery of a correlated metallic phase also holds on lattices that are not geometrically frustated. 
This can be seen in the phase diagram of our model computed on the square lattice, shown below in the right panel.
For the long-range interactions, we clearly see a transition from normal metallic state to correlated metal before finally undergoing an insulating transition.
However, this transition occurs for a lower value of $$V/t$$, thereby suggesting that the geometric frustration of the triangular lattice enhances the frustrating effects of long-range interactions in the build-up to the metal-insulator transition.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/spectral-function-and-square.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Single particle spectral function for the pure, Coulomb interaction case (left). Phase diagram of the same model on a square lattice (right).
</div>

The presence of a pseudogap in the spectral function is remniscient of the Efros-Shklovskii Coulomb gap in classical systems. 
In the [original 1975 paper](https://iopscience.iop.org/article/10.1088/0022-3719/8/4/003/meta), the authors (for whom the Coulomb gap is named) demonstrated that the density of states is suppressed around the Fermi level in classical systems with quenched disorder and long-range interactions.
Almost two decades later, however, [Efros put forth](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.68.2208) that the presence of disorder is not necessary to observe this pseudogap phenomenon and that the presence of long-range interactions is sufficient.

To determine if a similar mechanism could explain the presence of the pseudogap observed in our data, we constructed a quantum analogue of the distribution of electrostatic on-site potentials.

{% comment %}
Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/Estimate-pinball-Wigner-metal.png
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Estimate-pinball-Wigner-metal.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
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
