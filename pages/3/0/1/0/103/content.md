#Idea#

**$L_\infty$-algebroid**s or **Lie-$\infty$-algebroid**s or **$\infty$-Lie-algebroids** are to [[infinity-Lie-groupoid]]s as Lie algebras are to Lie groups. Hence $L_\infty$-algebroids are a [[horizontal categorification]] and [[vertical categorification]] of Lie algebras: they encompass [[L-infinity-algebra]]s as well as [[Lie algebroid]]s.

+-- {: .query}
Should the reference to '$\infty$ [[Lie groupoid]]s' above instead be to 'Lie $\infty$-groupoids'? Can we also call those '$L_\infty$-[[L-infinity-groupoid|groupoids]]'?

_[[Urs Schreiber|Urs]] says_: Yes, I started implementing this now.

_[[Toby Bartels|Toby]] says_: 'Lie-$\infty$-algebroid' and '$\infty$-Lie-algebroid' have a lot of hyphens. Should they be 'Lie $\infty$-algebroid' and '$\infty$-Lie algebroid'? Is there a reference? A reference would be good to be sure that these are all the same (unless you\'re prepared to say that you\'ll stand by it), given that Lie $n$-algebras are distinguished from $n$-Lie algebras as shown [[L-infinity-algebra|here]]. (It probably doesn\'t matter much to the wiki as long as we don\'t to those names.)

_[[Urs Schreiber|Urs]]_: 
Okay, I have added a section "references" below with more details:
there is no standard reference to the _term_ "$\infty$-Lie-algebroid" as yet, since most people who actually think about these higher Lie algebroids currently refer to them as [[NQ-supermanifold]]s. While that's good terminology for some purposes, it is bad terminology in the context of [[Lie theory]], clearly. And, as John says, we should use this wiki here, among other things, to "play Bourbaki" and improve on such matters. 

Concerning the placement of the "$\infty$" I am not sure what the best rule is. Generally, if X is a concept and p-X the concept with furher qualification p, what is the term for the infinity-version of p-X structures?  

I think in as far as the "p"-qualification comes from internalization, it should go in front, so $p-(\infty-X)$. 

But then, a Lie algebra is not the same as an algebra internal to [[Diff]], so $\infty-(Lie algebroid)$ would seem right. But the one-object version is already established $L_\infty$-algebras. 

Moreover, the distinction between "Lie $n$-algebra" and "$n$-Lie algebra" seems to have no justification apart from history.

So every good rule one might come up with seems to be in conflict with _some_ established convention. I am not sure how to best deal with this. 

=--

#Definition#

+-- {: .un_defn}
###### Definition
**(quasi-free differential graded-commutative algebras)**

A _quasi-free differential graded commutative algebra_
(**qDGCA**) is 

* an algebra of smooth functions $A := C^\infty(X)$ on a smooth manifold $X$;

* a non-positively graded complex $g$ of $A$-modules;

* together with a degree +1 graded derivation $d$ on the free (over $A$) graded-(anti-)commutative algebra
$
  \wedge^\bullet_{A} g^* = S^\bullet g^*[1]
$
on the dual (over $A$) of $g$;

* such that $d^2 = 0$.

A morphism of qDGCAs is a linear map of the underlying graded-(anti-)commuting algebras respecting the differential.
=--

Notice that the first few terms of $\wedge^\bullet g^*$ in degree 0, 1 and 2, respectively, are
$$
  \wedge^\bullet g^*
  =
  A \oplus g_0^*[1] \oplus  (g_0^*[1]\wedge g_0^*[1])
  \oplus g_{-1}^*[1] \oplus \cdots
  \,.
$$

**Example:** Take $g = \Gamma(T X)$ to be the $C^\infty(X)$-module of vector fields on $X$, then 
$\wedge^\bullet_{C^\infty(X)} g^* = \wedge^\bullet_{C^\infty(X)} \Omega^1(X) = \Omega^\bullet(X)$. 


**Remark:** There is plenty of room to fuss about the grading conventions. 

**Remark:** Usually one requires the module $g$ to be projective and of finite rank. In this case $g$ is the module of sections of a $\mathbb{N}$-graded vector bundle on $X$ and the above definition becomes equivalent to that of an [[NQ-supermanifold]].


+-- {: .un_defn}
###### Definition
**($L_\infty$-algebroids)**

$L_\infty$-algebroids are the objects dual to 
qDGCAs.
=--

We write 
$$
  L_\infty Algebroids \stackrel{CE(-)}{\to} qDGCAs
$$
for the corresponding contravariant functor and address the qDGCA $CE(g) := (\wedge^\bullet g^*, d)$ as the (generalized) [[Chevalley–Eilenberg algebra]] of $g$.

**Remark** In the physics literature $CE(g)$ is called a 
[[Chevalley–Eilenberg algebra|BRST complex]].


##Special Cases##

* an $L_\infty$-algebroid over a point, $X = pt$ is an **$L_\infty$-[[L-infinity-algebra|algebra]]**;

* an $L_\infty$-algebroid with generators concentrated in the first $n$ degrees is a **Lie $n$-algebroid**;

* an $L_\infty$-algebroid the differential of whose CE-algebra is "co-binary", i.e. $d : \mathfrak{g}^* \to g^* \oplus g^* \wedge g^*$, is **strict**.

So in particular

* a Lie 1-algebroid is a **[[Lie algebroid]]**;

* a Lie 1-algebroid over the point is a **Lie algebra**;

* a Lie $n$-algebroid over a point is a 
**[[L-infinity-algebra|Lie n-algebra]]**.

#Further resources#

There should be an [[internalization]] of this into the context of [[generalized smooth spaces]] and [[generalized smooth algebras]]. This is discussed at [[schreiber:generalized smooth L-infinity algebroid]].

#References#

The term "$\infty$-Lie-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[NQ-supermanifold]]s and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie-algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* Pavol &#352;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifold]]s". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model]]s in [[rational homotopy theory]], which is concerned with modelling _spaces_ by qDGCAs. That these spaces can be regarded as [[infinity-groupoid]]s and as [[Lie-infinity-groupoid]]s in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]].