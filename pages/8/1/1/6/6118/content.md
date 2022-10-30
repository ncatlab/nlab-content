
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Relational $\beta$-modules
* table of contents
{: toc}

## Idea

>One of my early Honours students at [[Macquarie University]] baffled his proposed Queensland graduate studies supervisor who asked whether the student knew the definition of a [[topological space]]. The aspiring researcher on [[dynamical system]]s answered positively: "Yes, it is a relational $\beta$-module!"  I received quite a bit of flak from colleagues concerning that one; but the student [[Peter Kloeden]] went on to become a full professor of mathematics in Australia then Germany.
---[[Ross Street]], in _[[An Australian conspectus of higher categories]]_

In 1970, [[Michael Barr]] gave an abstract definition of [[topological space]] based on a notion of [[convergence]] between [[ultrafilters]] (building on work by [[Ernest Manes]] on [[compact Hausdorff spaces]]).  Succinctly, Barr defined topological spaces as 'relational $\beta$-modules'.  It was subsequently realized that this was a special case of the notion of [[generalized multicategory]].  Here we unpack this definition and examine its properties.

The correctness of this definition (in the sense of matching [[Bourbaki]]\'s definition) is equivalent to the [[ultrafilter principle]] ($UP$).  However, the definition can be treated on its own, even in a context without $UP$.  So we also consider the properties of relational $\beta$-modules when these might not match Bourbaki spaces.


## Definitions

### Abstract

If $S$ is a [[set]], let $\beta{S}$ be the set of [[ultrafilters]] on $S$. This set is canonically identified with the set of Boolean algebra homomorphisms 

$$P(S) \to \mathbf{2},$$ 

from the power set of $S$ to $\mathbf{2}$, the unique Boolean algebra with two elements. The 2-element set carries a [[dualizing object]] structure that induces an evident [[adjoint pair]] 

$$(Set \stackrel{P}{\to} Bool^{op}) \; \dashv \;  (Bool^{op} \stackrel{\hom(-, \mathbf{2})}{\to} Set)$$ 

so that the composite [[functor]] $\beta = \hom(P-, \mathbf{2}): Set \to Set$ carries a [[monad]] structure. 

The functor $\beta : Set \to Set$ extends to [[Rel]] as follows: given a [[binary relation]] $r\colon X \to Y$, written as a subobject in $Set$

$$R \stackrel{\langle \pi_1, \pi_2 \rangle}{\to} X \times Y,$$ 

we define $\beta(r): \beta(X) \to \beta(Y)$ to be the relation obtained by taking the image of $\langle \beta(\pi_1), \beta(\pi_2) \rangle: \beta(R) \to \beta(X) \times \beta(Y)$. It turns out, although it is by no means obvious, that $\beta$ is according to this definition a _strict_ functor on $Rel$. 

The monad structure on $\beta: Set \to Set$, given by a unit $u: 1 \to \beta$ and multiplication $m: \beta \beta \to \beta$, extends not to a strict monad on $Rel$, but rather one where the transformations $u, m$ are op-lax in the sense of there being inequalities 

$$\array{
X & \stackrel{u_X}{\to} & \beta X & & & & & & \beta \beta X & \stackrel{m_X}{\to} & \beta X \\  
\mathllap{r} \downarrow & \leq & \downarrow \mathrlap{\beta(r)} & & & & & & \mathllap{\beta \beta (r)} \downarrow & \leq & \downarrow \mathrlap{\beta(r)} \\
Y & \underset{u_Y}{\to} & \beta Y & & & & & & \beta \beta Y & \underset{m_Y}{\to} & \beta Y
}$$ 

(while of course the monad associativity and unit conditions remain as equations: hold on the nose). 

Then a __relational $\beta$-module__ is a [[lax algebra]] (module) of $\beta$ on the [[2-poset]] $Rel$. In other words, a set $S$ equipped with a relation $\xi: \beta S \to S$ such that the following inequalities hold: 

$$\array{
S & \stackrel{u_S}{\to} & \beta S & & & & & & \beta \beta S & \stackrel{m_S}{\to} & \beta S \\
 & \mathllap{1_S} \searrow \; \leq & \downarrow \mathrlap{\xi} & & & & & & \mathllap{\beta(\xi)} \downarrow & \leq & \downarrow \mathrlap{\xi} \\ 
 & & S & & & & & & \beta S & \underset{\xi}{\to} & S
}$$ 

Arguably, it is better to consider $Rel$ as a [[proarrow equipment]] in this construction, in order to accommodate [[continuous functions]] between topological spaces as the apropriate notion of morphism between relational $\beta$-modules.  See [[generalized multicategory]].


### Concrete

A __relational $\beta$-module__ is a [[set]] $S$ and a [[binary relation]] $\to$ between [[ultrafilters]] on $S$ and [[elements]] of $S$ that satisfies a certain rule.

To explain this rule, we first define a [[subset]] $A$ of $S$ to be __[[open subset|open]]__ if $A \in \mathcal{U}$ whenever $\mathcal{U} \to x \in A$.  Then the requirement on $\to$ is a converse:

*  $\mathcal{U} \to x$ if $A \in \mathcal{U}$ whenever $A$ is open and $x \in A$.

...

This definition exhibits a topological space as a particular type of [[pseudotopological space]].  (A pseudotopological space is just a relational $\beta$-module which omits the "associativity" axiom.)


## Properties

We say that $\mathcal{U}$ __converges__ to $x$ if $\mathcal{U} \to x$.

As above, a [[subset]] $A$ of $S$ is __[[open subset|open]]__ if $A \in \mathcal{U}$ whenever $\mathcal{U} \to x \in A$.  On the other hand, $A$ is __[[closed subset|closed]]__ if $x \in A$ whenever $A \in \mathcal{U} \to x$.

A relational $\beta$-module is __[[compact space|compact]]__ if every ultrafilter converges to at least one point.  It is __[[Hausdorff space|Hausdorff]]__ if every ultrafilter converges to at most one point.  Thus, a __[[compactum]]__ is (assuming $UF$) precisely a relational $\beta$-module in which every ultrafilter converges to exactly one point, that is in which the action of the monad $\beta$ lives in $Set$ rather than in $Rel$; see [[ultrafilter monad]].

...


## Relation to nonstandard analysis

In [[nonstandard analysis]] (which implicitly relies throughout on $UF$), one may define a topological space using a relation between hyperpoints (elements of $S^*$) and standard points (elements of $S$).  If $u$ is a hyperpoint and $x$ is a standard point, then we write $u \approx x$ and say that $x$ is a __[[standard part]]__ of $u$ or that $u$ belongs to the __[[halo]]__ (or _monad_, but *not* the category-theoretic kind) of $x$.  This relation must satisfy a condition analogous to the condition in the definition of a relational $\beta$-module.  The nonstandard defintions of open set, compact space, etc are also analogous.  (Accordingly, one can speak of *the* standard part of $u$ only for Hausdorff spaces.)

So ultrafilters behave very much like hyperpoints.  This is not to say that ultrafilters *are* (or even can be) hyperpoints, as they don\'t obey the [[transfer principle]].  Nevertheless, one does use ultrafilters to construct the [[model]]s of nonstandard analysis in which hyperpoints actually live.  Intuitions developed for nonstandard analysis can profitably be applied to ultrafilters, but the transfer principle is not valid in proofs.


## Relation to other topological concepts

If $\beta$ is treated as a monad on $Set$ instead of on $Rel$, then its algebras are the [[compacta]] (the compact Hausdorff spaces), again assuming $UP$; see [[ultrafilter monad]].

One might hope that there would be an analogous treatment of [[uniform spaces]] based on an [[equivalence relation]] between ultrafilters.  (In nonstandard analysis, this becomes a relation $\approx$ of infinite closeness between arbitrary hyperpoints, instead of only a relation between hyperpoints and standard points.)  The description in terms of generalized multicategories is known to generalize to a description of uniform spaces, but rather than using relations between ultrafilters, this description uses pro-relations between points.


[[!redirects relational beta-module]]
[[!redirects relational beta-modules]]
[[!redirects relational ∞-module]]
[[!redirects relational ∞-modules]]
