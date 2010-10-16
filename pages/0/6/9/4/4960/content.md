

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}
 
## Idea

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[space]]s inside of which [[geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : E \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  E 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  Set
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]) .

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi : E \to Set$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected components]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $(n-1)$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$. See [[cohesiv (∞,1)-topos]].

In total this gives a quadruple of [[adjoint functor]]s

   $$
    (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
    E
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    Set
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extenson to such a quadruple of adjoints, satisfying some further properties.


## Definition


+-- {: .un_defn}
###### Definition

A [[topos]] $E$ over some base topos $S$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) : E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  S
$$

is **cohesive** or  **a topos of cohesion** if it has the following [[stuff, structure, property|properties]]:

*  it is _local_ and _connected_ in the following sense:

   1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

   1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is [[fully faithful functor|fully faithful]];

   1. it is _strongly connected_ : $f_!$ preserves even all [[finite]] [[product]]s;

   1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be connected);

   so that in total we have a quadruple of [[adjoint functor]]s
   
   $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    E
     \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
    \;
   $$

   Note that $f$ being local implies, in particular, that $S \stackrel{f^!}{\hookrightarrow} E$ is a [[subtopos]]: $f^!$ is a [[full and faithful functor]];


In addition one may ask that

1. the [[natural transformation]]

   $$
     f_*  
       \stackrel{\simeq}{\to} 
     f_* ( f^*  f_* )
       \stackrel{}{\to}
     f_* ( Id ) 
       \stackrel{}{\to}
     f_*( f^* f_! )
       \stackrel{\simeq}{\to}
     f_!
   $$

   is an [[epimorphism]], equivalently the transformation

   $$
     f^* \to f^!
   $$

   is a [[monomorphism]].


1. $f_!$ is "continuous" in that for all $s \in S$ and $e \in E$ the natural morphism

   $$
     f_! (e^{f^* s}) \stackrel{\simeq}{\to} (f_!(e))^s
   $$

   is an [[isomorphism]]

   (this morphism is the [[internal hom]]-[[adjunct]] of 
   $
     s \times f_!(e^{f^* s}) 
      \stackrel{\simeq}{\to}
     f_!f^*(s) \times f_!(e^{f^* s})
      \stackrel{\simeq}{\to}
     f_!(f^*(s) \times e^{f^* s})
     \to
     f_!(e)
   $
   where we use that by definition $f^*$ is full and faithful and then that $f_!$ preserves products); 

=--

## Examples

A trivial class of examples is:

* Every topos is cohesive over itself.

A large class of examples is obtained from toposes over a [[cohesive site]]:

* the [[sheaf topos]] on a [[cohesive site]] is a cohesive topos.

This includes...


## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* **cohesive topos** / [[cohesive (∞,1)-topos]]




## References

The definition of a category of cohesion was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

The observation that $Sh(CartSp)$ is a [[local topos]] and that this serves to characterize [[diffeological space]]s was amplified by [[David Carchedi]].


[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]

