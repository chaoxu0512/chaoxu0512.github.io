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

$B o=\frac{R_{0}^{2}}{\ell_{c}^{2}}=\frac{|\Delta \rho| g R_{0}^{2}}{\gamma}$

2. The second question is how to obtain the free energy functional? According to the definition of surface free energy, the unit should be mN/m, however, the formula in the paper of free energy is $\Pi  = \int_0^{2\pi } {\int_0^{{R_0}} F } (r,\theta ){\rm{d}}r\;{\rm{d}}\theta $, 

   where

   $F(r,\theta ) = \left( {\gamma \sqrt {1 + {{\left( {{{dh} \over {dr}}} \right)}^2} + {1 \over {{r^2}}}{{\left( {{{dh} \over {d\theta }}} \right)}^2}}  + {1 \over 2}\Delta \rho g{h^2} + \lambda h} \right)r$

   The form of free energy in the paper does not make sense to me. What’s more, how to model the first two terms in $F(r,\theta)$? Here we see the definition from the paper:

   > … is composed of two contributions: the surface energy associated with the interface between the liquids, and the gravitational potential energy that includes Earth’s gravity and the hydrostatic buoyancy force. The last term in  $F(r,\theta)$ represents the volume constraint, with $\lambda$ being a Lagrange multiplier.