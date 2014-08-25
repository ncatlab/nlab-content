
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The original _Euler product_ is an expression of the [[Riemann zeta function]] as a product (instead of a sum as originally defined) over all [[prime numbers]]. More generally one considers Euler product expressions for general [[zeta functions]] and [[L-functions]].

When the [[Riemann zeta function]] is understood as an [[adelic integral]] via [[Iwasawa-Tate theory]], then the existence of Euler product expressions follows from the fact that the integration [[measure]] on the [[idele group]] $\mathbb{I}_{\mathbb{Q}}$ used in this context is a product of measures on all [[p-adic number]]-components:

if a function $f\colon \mathbb{I} \longrightarrow \mathbb{R}$ has product form $f = \underset{v}{\prod} f_v$ then 

$$
  \int_{\mathbb{I}_{\mathbb{Q}}}
  \;
    f(x)
  \;
    {\vert x\vert}^s
  \;
  d^\times x
  \;=\; 
  \underset{v}{\prod} 
  \left(
  \int_{\mathbb{Q}_v^\times}
  \;f_v(x)\;
   {\vert x\vert}_v^s
  \;
  d_v^\times x
  \right)
  \,.
$$

(reviewed e.g. in [Garrett 11, 1.6](#Garrett11))

## References

* Wikipedia, _[Euler product](http://en.wikipedia.org/wiki/Euler_product)_

Discussion from the point of view of [[adelic integration]] in [[Iwasawa-Tate theory]] is for instance in

* {#Garrett11} [[Paul Garrett]], section 1.6 _Iwasawa-Tate on &#950;-functions and L-functions_
([pdf](http://www-users.math.umn.edu/~garrett/m/mfms/notes_c/Iwasawa-Tate.pdf))

[[!redirects Euler products]]


[[!redirects Euler product form]]