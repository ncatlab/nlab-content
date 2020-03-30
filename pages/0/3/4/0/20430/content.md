
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The [[coupling constant]] in [[perturbative string theory]].

## Properties

### Behaviour under M/IIA duality

Under [[duality between type IIA string theory and M-theory]] the string coupling constant relates to the [[radius]] of the 11d [[circle]]-[[fiber]]:


Consider the [[M-theory]] [[scales]]

* $\ell_P$, the [[Planck length]] in 11-dimensions;

* $R_{10}$ the [[length]] (circumference) of the $S^1_{10}$ [[circle]] [[fiber]] for [[KK-compactification]] to 10 dimensions

and the [[string theory]] [[scales]]

* $\ell_s$, the [[string length scale]];

* $g_{s}$, the [[string coupling constant]] of [[perturbative string theory]].


Then under the [[duality between M-theory and type IIA string theory]] these scales are related as follows:

$$
  \ell_P \;=\; g_{st}^{1/3} \ell_s
  \,,
  \phantom{AAA}
  R_{10} \;=\; g_{st} \ell_s
$$

equivalently

$$
  \ell_s \;=\; R_{10}/ g_{st}
  \,,
  \phantom{AAA}
  \ell_P \;=\; g_{st}^{-2/3} R_{10}
$$

equivalently

$$
  g_{st} \;=\; (R_{10}/\ell_P)^{3/2}
  \,,
  \phantom{AAA}
  \ell_s \;=\; \ell_P (R_{10}/\ell_P)^{-1/2}
  \,.
$$

Hence a [[membrane instanton]], which on a 3-[[cycle]] $C_3$ gives a contribution

$$
  \exp\left(
    - \frac{ vol(C_3) }{ \ell^3_P }
  \right)
$$

becomes 

1. if the cycle [[wrapped brane|wraps]], $C_3 = C_2 \cup S^1_{10}$, a [[worldsheet instanton]]

   $$
     \exp\left( - \frac{ vol(C_3) }{ \ell_P^3 }  \right) 
     \;=\; 
     \exp\left( - \frac{ R_{10} vol(C_2) }{ g_{st} \ell_s^3 }  \right)
     \;=\;
     \exp\left( - \frac{ vol(C_2) }{ \ell_s^2 }  \right)
   $$

1. the cycle does not [[wrapped brane|wrap]], a spacetime instanton contribution, specifically a [[D2-brane instanton]]

   $$
     \exp\left( - \frac{ vol(C_3) }{ \ell_P^3 }  \right)
     \;=\;
     \exp\left( - \frac{ vol(C_3)/\ell_s^3 }{ g_{st} }  \right)
   $$
   
   
(This unification of the two different [[non-perturbative effects]] in [[perturbative string theory]]
([[worldsheet instantons]] and spacetime [[instantons]]), to a single type of effect ([[membrane instanton]])
 in [[M-theory]] was maybe first made explicit in [Becker-Becker-Strominger 95](#BeckerBeckerStrominger95). Brief review includes [Marino 15, sections 1.2 and 1.3](#Marino15)).

## Related concepts

* [[axio-dilaton]]

* [[Yukawa coupling]]

[[!include fundamental scales -- contents]]


## References

The identification of [[non-perturbative effects]] in [[string theory]] with brane contributions is due to

* {#BeckerBeckerStrominger95} [[Katrin Becker]], [[Melanie Becker]], [[Andrew Strominger]], _Five-branes, membranes and nonperturbative string theory_, Nucl. Phys. B 456, 130 (1995) ([hep-th/9507158](http://arxiv.org/abs/hep-th/9507158))

Review includes

* {#Marino15} [[Marcos Mariño]], _Non-perturbative effects in string theory and AdS/CFT_, [Spring School on Superstring Theory and Related Topics 2015](http://indico.ictp.it/event/a14251/)  ([[MarinoNonPerturbative.pdf:file]], [pdf](http://indico.ictp.it/event/a14251/session/89/contribution/401/material/0/0.pdf), [recording](https://youtu.be/5hw6l-JSpc4?list=PLzYFBWfshN8eqXZFYg2jBZSii7lHaeyXJ))

[[!redirects string coupling constants]]

[[!redirects string coupling]]
[[!redirects string couplings]]


