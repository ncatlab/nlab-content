
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Gievn a (cohomological) [[spectral sequence]] $(E_r^{p,q})$ there are natural morphisms

$$
  E_2^{n,0} \longrightarrow E^n
$$

and

$$
  E^n \longrightarrow E_2^{0,n}
  \,.
$$

These are called the _edge morphisms_ or _edge maps_ of the spectral sequence.

## Properties

The edge morphisms sit in an [[exact sequence]] of the form

$$
  0 \to E_2^{1,0} \to E^1 \to E_2^{0,1} \stackrel{d_2}{\to} E_2^{2,0} \to E^2
$$

This is often called the _exact sequence of terms of low degree_ or _five term exact sequence_.

e.g. ([Cartan_Eilenberg XV, 5](#CartanEilenberg), [Tamme, 0 2.3.2](#Tamme))

If 

$$
  E_r^{p,(0 \leq q \leq n)} = 0
$$

then  $E^{p,0}_2 \simeq E^p$ for $p \lt n$ and also 

$$
  0 \to E_2^{1,0} \to E^1 \to E_2^{0,1} \stackrel{d_2}{\to} E_2^{2,0} \to E^2
$$

is [[exact sequence|exact]].

e.g. ([Cartan_Eilenberg XV, 5](#CartanEilenberg), [Tamme, 0 2.3.3](#Tamme))


## References

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, 1956
 {#CartanEilenberg}

* [[Günter Tamme]], section 0 2.3 of _[[Introduction to Étale Cohomology]]_
 {#Tamme}


[[!redirects edge morphisms]]

[[!redirects edge map]]
[[!redirects edge maps]]

[[!redirects exact sequence of terms of low degree]]
[[!redirects exact sequences of terms of low degree]]

[[!redirects five term exact sequence]]
[[!redirects five term exact sequences]]

