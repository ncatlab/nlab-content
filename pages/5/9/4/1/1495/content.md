
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _algebraic space_ is an object in the [[sheaf topos]] over the [[fppf-site]], that has [[representable morphism of stacks|representable]] [[diagonal]] and an [[étale cover]]([[atlas]]) by a [[scheme]].

In [[algebraic geometry]] one can glue [[affine schemes]] in various topologies; this way one obtains various kinds of locally affine [[ringed space]]s. For example, [[scheme]]s locally affine in [[Zariski topology]]. [[etale topology|Étale topology]] is finer than Zariski, hence the category of locally affine (ringed) spaces in &#233;tale topology is larger than the category of schemes. __Algebraic spaces__ make a category which is includes the subcategory of all schemes and is close to the category of locally affine spaces in [[étale topology]], namely it consists of those [[ringed space]]s which may be obtained as a [[quotient object|quotient]] of a scheme $S$ by an [[equivalence relation]] $R\subset S\times S$ which is a closed subscheme, and whose projections $p_1,p_2: R\to S$ are &#233;tale morphisms of schemes.

## Definition

Write $C_{fppf}$ for the [[fppf-site]] (over some [[scheme]], as desired). 

+-- {: .un_defn}
###### Definition

An **algebraic space** is 

* an object $X \in Sh(C_{fppf})$ in the [[sheaf topos]];

* whose [[diagonal]] morphism $X \to X \times X$ is [[representable morphism of stacks|representable]];

* and for which there exists $U \in C$ and a morphism $U \to X$ which is

  * surjective;

  * [[étale morphism|étale]].

=--

In this form this appears as [de Jong, def. 35.6.1](#deJong).

## References

Algebraic spaces are the topic of chapter 35 in

* [[Aise Johan de Jong]], _[[The Stacks Project]]_
{#deJong}

A standard monograph on algebraic spaces is

* D. Knutson, _Algebraic spaces_ , LNM 203, Springer 1971.

Lecture notes include

* [[James Milne]], section 7 of _[[Lectures on Étale Cohomology]]_

Some related MO questions: 

* [why-is-this-not-an-algebraic-space](http://mathoverflow.net/questions/9043/why-is-this-not-an-algebraic-space), 

* [Can an algebraic space fail to have a unviersal map to a scheme?](http://mathoverflow.net/questions/4587/can-an-algebraic-space-fail-to-have-a-unviersal-map-to-a-scheme)...

[[!redirects algebraic spaces]]