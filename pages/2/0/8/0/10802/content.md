
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[étale cohomology]] of [[schemes]], the _Artin comparison theorem_ ([Artin 66](#Artin66)) says that under some conditions on a [[scheme]] and a [[sheaf]] of [[coefficients]],  the [[étale cohomology]] of the scheme coincides with the [[ordinary cohomology]] (e.g. [[singular cohomology]]) of its underlying [[complex analytic topology]].

Historically this kind of statement was a central motivation for the development of [[étale cohomology]] in the first place.

Specifically, let $A$ be either of

* a [[finite group|finite]] [[field]];

* the [[p-adic integers]] $\mathbb{Z}_p$ for some [[prime]] $p \geq 2$;

* the [[p-adic numbers]] $\mathbb{A}_{p}$

(but _not_ for instance the [[integers]] themselves).

Then for $X$ a [[variety]] over the [[complex numbers]] and $X^{an}$ its [[analytification]] to the [[topological space]] of complex points $X(\mathbb{C})$  with its [[complex analytic topology]], then there is an [[isomorphism]]

$$
  H^\bullet(X_{et}, A) \simeq H^\bullet(X^{an}, A)
$$

between the [[étale cohomology]] of $X$ and the [[ordinary cohomology]] of 
$X^{an}$.

Notice that on the other hand for instance if instead $X = Spec(k)$ is the [[spectrum of a commutative ring|spectrum]] of a [[field]], then its [[étale cohomology]] coincides with the [[Galois cohomology]] of $k$. In this way [[étale cohomology]] interpolates between "[[topology|topological]]" and "[[number theory|number theoretic]]" notions of cohomology.
 

## Related concepts

* [[analytification]], [[GAGA]]

* [[comparison theorem]]

* [[comparison theorem (crystalline cohomology)]]

* [[Chow's theorem]]

## References

The original reference is

* [[Michael Artin]], _The &#233;tale topology of schemes_ , Proc. Internat. Congress Mathematicians (Moscow, 1966) , Mir (1968) pp. 44&#8211;56
 {#Artin66}

* [[Alexander Grothendieck]], [[SGA]] I, Expos&#233; XII

A textbook account is in 

* {#Danilov91} [[Vladimir Danilov]], chapter 3 of _Cohomology of algebraic varieties_, in I. Shafarevich (ed.), _Algebraic Geometry II_, volume 35 of _Encyclopedia of mathematical sciences_, Springer 1991 ([GoogleBooks](http://books.google.de/books?id=ZhzXJHUgcRUC&lpg=PA67&ots=aVQoeMkBwc&dq=analytification&pg=PA61&redir_esc=y#v=onepage&q=analytification&f=false)))


Reviews and lecture notes include

* [[eom]], _[Comparison theorem](http://www.encyclopediaofmath.org/index.php/Comparison_theorem_(algebraic_geometry)_

* [[James Milne]], section 21 of _[[Lectures on Étale Cohomology]]_

In the context of [[Berkovich analytic spaces]] see also

* [[Vladimir Berkovich]], _On the comparison theorem for &#233;tale cohomology of non-archimedean analytic spaces_ ([pdf](http://www.wisdom.weizmann.ac.il/~vova/IJM_1995_92_compar.pdf))

[[!redirects comparison theorem (etale cohomology)]]