---
layout:     post
title:      Fluidic shaping lens
subtitle:   
date:       2022-01-27
author:     Chao Xu
header-style: text
hidden: false 
mathjax: true
catalog: true
tags:
    - Paper and Book
    - Freeform optics
---

It is not the first time that I read the paper "Fabrication of freeform optical components by fluidic shaping", but I have to admit that I did not get a very good understanding of it. This time, at least I can throw some questions to myself and offer a certain way for the next step to progress. (By the way, I emailed the first author to ask for suggestions to repeat his work, wow, he was very nice and responsive!)

1. The first question is how to obtain the value of the interfacial energy $\gamma$ between two liquids? Is it measured from the experiments? or is it only a  variable used in the analytical simulation? This interfacial energy is used to calculate the Bond number in the simulation. For now, I prefer the second option. 

$$
B o=\frac{R_{0}^{2}}{\ell_{c}^{2}}=\frac{|\Delta \rho| g R_{0}^{2}}{\gamma}
$$

2. The second question is how to obtain the free energy functional? According to the definition of surface free energy, the unit should be mN/m, however, the formula in the paper of free energy is $\Pi  = \int_0^{2\pi } {\int_0^{{R_0}} F } (r,\theta ){\rm{d}}r\;{\rm{d}}\theta $, 

   where
   $$
   F(r,\theta ) = \left( {\gamma \sqrt {1 + {{\left( {{{dh} \over {dr}}} \right)}^2} + {1 \over {{r^2}}}{{\left( {{{dh} \over {d\theta }}} \right)}^2}}  + {1 \over 2}\Delta \rho g{h^2} + \lambda h} \right)r
   $$
   The form of free energy in the paper does not make sense to me. What’s more, how to model the first two terms in $F(r,\theta)$? Here we see the definition from the paper:

   > … is composed of two contributions: the surface energy associated with the interface between the liquids, and the gravitational potential energy that includes Earth’s gravity and the hydrostatic buoyancy force. The last term in  $F(r,\theta)$ represents the volume constraint, with $\lambda$ being a Lagrange multiplier.

   In addition to the first two terms, I also need to take a look at the final term.

3. To minimize the surface energy at equilibrium, the first-order derivative of $\Pi$​ is equal to zero, yielding to the standard Euler–Lagrange equation:
   $$
   \frac{\partial F}{\partial h}-\frac{d}{d r} \frac{\partial F}{\partial h_{r}}-\frac{d}{d \theta} \frac{\partial F}{\partial h_{\theta}}=0
   $$
   For this equation, I think I need to check it a little bit.

   > M. Gelfand and S. V. Fomin, Calculus of Variations (Prentice-Hall, 1963).

4. Another definition mentioned in the paper is $d_c$​, the characteristic deformation of the surface relative to the frame. It is neglected in the following calculation. 

   > For most optical elements the characteristic deformation length $d_c$ is significantly smaller than the component’s radius, thus $\varepsilon=\left(\frac{d_{c}}{R_{0}}\right)^{2} \ll 1$.

   However, whether it is still the case when the scale is in microns? This is still unknown. 

5. I still have one math calculation to be done. How to get the equation (which is the Helmholtz equation)
   
   $\tilde{H} x^{2}+x^{2} \tilde{H}_{x x}+x \tilde{H}_{x}+\tilde{H}_{\Theta \Theta}=0$
   
   from 
   
   $(-H+P) B o R^{2}-\frac{H_{R R}\left(R^{2}+\varepsilon H_{\Theta}^{2}\right)+\left(R H_{R}+H_{\Theta \Theta}\right)\left(1+\varepsilon H_{R}^{2}\right)-2 \varepsilon H_{\Theta} H_{R} H_{R \Theta}+\frac{2}{R} \varepsilon H_{R} H_{\Theta}^{2}}{\left(1+\varepsilon H_{R}^{2}+\frac{\varepsilon}{R^{2}} H_{\Theta}^{2}\right)^{3 / 2}}=0$
   
   The solution of the Helmholtz equation is, 
   
   $\tilde{H}(x, \theta)=\sum_{n=0}^{\infty} A_{n} J_{n}(x) \cos (n \Theta)+\sum_{n=1}^{\infty} B_{n} J_{n}(x) \sin (n \Theta)$
   
   Check the solution from: A. D. Polyanin and V. E. Nazaikinskii, Handbook of Linear Partial Differential Equations (Taylor and Francis, 2016).

6. One last math problem for me is how to obtain the 
