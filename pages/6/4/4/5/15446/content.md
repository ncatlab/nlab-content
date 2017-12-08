
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _global field_ is either


* a [[number field]]

* or a [[function field]] over a [[finite field]];

hence is a [[finite number|finite]]-[[dimension|dimensional]] [[field extension]] of either

* the [[rational numbers]] $\mathbb{Q}$;

* the [[rational functions]] $\mathbb{F}_q(t)$ with [[coefficients]] in the [[finite field]] $\mathbb{F}_q$.


The [[function field analogy]] says how both these kinds of global fields are indeed analogous in that they behave as rings of [[rational functions]] on "[[arithmetic curves]] over the would-be [[field with one element]] $\mathbb{F}_1$" and $\mathbb{F}_q$, respectively. In particular for both types there is a concept of [[ring of adeles]], [[group of ideles]], etc.

The [[Langlands conjectures]] concern the [[arithmetic geometry]] of global fields.

The "local" version of a global field in the sense of [[formal geometry]] is a [[local field]]. The corresponding version of the Langlands program are the _[[local Langlands correspondences]]_.

## Artin-Whaples characterization 

Global fields can also be described axiomatically, as those fields which satisfy a suitable [product formula](/nlab/show/group+of+ideles#ProductFormula). For example, if $k$ is a number field and $\mathbb{I}_k$ is its [[group of ideles]], then there is an idele norm map 

$$N: \mathbb{I}_k \to \mathbb{C}^\times$$ 

$$(x_v)_{places\; v} \mapsto \prod_v {|x_v|}_v$$ 

and $k^\times$ is retrieved as the [[kernel]] of this map, i.e., is the subgroup of elements $(x_v)$ for which the product formula $\prod_v {|x_v|}_v = 1$ holds. 

For the following theorem, assume that $k$ is a field for which there is at least one [[valuation]] that is either archimedean, or is discrete and with finite residue class field for the corresponding [[local ring]]. By a *place* we understand an equivalence class of valuations. 

+-- {: .num_theorem} 
###### Theorem 
**(Artin-Whaples)** 
Suppose $k$ is a field that has a set of valuations ${|(-)|}_v$, one for every place of $k$, such that for every $x \in k^\times$ the product formula $\prod_v {|x|}_v = 1$ is satisfied. Then $k$ is a global field (and conversely, every global field has this property). 
=-- 



## References

* Wikipedia, _[Global field](http://en.wikipedia.org/wiki/Global_field)_

* Emil Artin and George Whaples, _Axiomatic characterization of fields by the product formula for valuations_, Bull. Amer. Math. Soc. 51 (1945), 469-492. ([link to article](http://www.ams.org/journals/bull/1945-51-07/S0002-9904-1945-08383-9/home.html)) 

[[!redirects global fields]]