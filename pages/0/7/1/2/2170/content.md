
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Derivations:

For convenience we assume below that $M$ is a $G$-[[module]], it does not in general have to be abelian and it suffices to have it a $G$-[[group]].


Suppose $G$ is a [[group]] and $M$ a $G$-[[module]] and let $\delta : G \to M$ be a __derivation__ in the sense that $\delta(g_1g_2) = \delta(g_1) +g_1\delta(g_2)$ for all $g_1, g_2 \in G$
(a [[crossed homomorphism]] -- notice that it's *not* $\delta(g_1)g_2 + g_1\delta(g_2)$ as for the other notion of [[derivation]].)

For calculations, the following lemma is very valuable, although very simple to prove.

+-- {: .un_lemma}
###### Lemma

If  $\delta : G \to M$ is a derivation, then

1. $ \delta(1_G) = 0$;

2. $\delta(g^{-1}) = -g^{-1}\delta(g)$ for all $g \in G$;

3. for any $g \in G$ and $n\geq 1$, 

   $$\delta(g^n) = (\sum^{n-1}_{k=0}g^k)\delta(g).$$
=--

+-- {: .proof}
###### Proof
As was said, these are easy to prove.

$\delta(g) = \delta(1) + 1\delta(g)$, so $\delta(1)= 0$, and hence (1); then 

$$\delta(1) = \delta(g^{-1}g) = \delta(g^{-1}) + g^{-1}\delta(g)$$ 

to get (2), and finally induction to get (3).
=--

##Remarks and examples:

* There is a mapping from $G$ to its [[augmentation ideal]], $I(G)$, defined by $d_G(g)= g-e_G$.  This is the [[derived module|universal derivation]] towards $G$-modules.  

* The [[Fox derivatives]] are examples of derivations.  It is worth noting that this lemma allows a simplification of the conditions given there (as noted there).

###Example calculation using the [[Fox derivative]] w.r.t a generator.

 Let $X = \{u,v\}$, with $r \equiv u v u v^{-1} u^{-1} v^{-1} \in F = F(u,v),$ then


$$ \frac{\partial r}{\partial u} = 1 + u v - u v u v^{-1} u^{-1},$$


$$ \frac{\partial r}{\partial v} = u - u v u v^{-1} -  u v u v^{-1} u^{-1} v^{-1}.$$
This relation, $r$, is the typical [[braid group]] relation, here in $Br_3$.

##Relative derivations

These are a useful relative form of derivation. The notion is often avoided as it can easily be reduced to the more standard form above by restricting the module structure along $\varphi$.

Let  $\varphi  : H \rightarrow  G$  be a   homomorphism of  groups. 
 A  _$\varphi $-derivation_ from a group to a module,

$$\partial  : H \rightarrow  M,$$ 
                               
from  $H$  to a left  $\mathbb{Z}[G]$-module,  $M$,  is a mapping from  $H$  to  $M$,  which satisfies the equation

$$\partial (h_1 h_2 ) = \partial (h_1 ) + \varphi (h_1)\partial (h_2 )$$
  
for all  $h_1$, $h_2  \in  H$. 

There is a universal such $\varphi$-derivation, $d_\varphi:H\to D_\varphi$.  The codomain of this is variously called the [[derived module]] of $\varphi$ (e.g. by [[Crowell]]) or the $\varphi$-differential module by [[Masanori Morishita|Morishita]].

The set of  $\varphi$-derivations is often written $Der_\varphi(H,M)$, or simply $Der_\varphi(M)$. 

## Related concepts

* [[crossed homomorphism]]

## References

For the original version of derived module, see

* [[R. H. Crowell]], _The derived module of a homomorphism_, Advances  in Math., 5, (1971), 210&#8211;238 (<a href="https://doi.org/10.1016/0001-8708(71)90016-8">doi:10.1016/0001-8708(71)90016-8</a>)

Textbook account:

* [[Kenneth Brown]],  p. 45 of: _Cohomology of Groups_, Graduate Texts in Mathematics, **87**, Springer 1982 ([doi:10.1007/978-1-4684-9327-6](https://link.springer.com/book/10.1007/978-1-4684-9327-6))


Application in [[arithmetic topology]]:

* {#Morishita12} [[Masanori Morishita]], _Knots and Primes: An Introduction to Arithmetic Topology_, 2012 ([web](https://books.google.co.uk/books?id=DOnkGOTnI78C&pg=PA156#v=onepage&q&f=false))

[[!redirects derivations on a group]]


