<div class="rightHandSide toc">
[[!include categorification - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

The term _Grothendieck group_ has a restricted and a more general meaning.

In its restricted sense the _Grothendieck group completion_ of an abelian [[monoid]] $A$ is a certain [[group]] structure on a quotient of $A \times A$. This is such that applied to the additive monoid of [[natural number]]s $\mathbb{N}$ it produces the additive group of integers $\mathbb{Z}$.

The same procedure applied to [[decategorification|isomorphism classes]] of certain [[Quillen exact category|Quillen exact categories]] happens to compute a group that is called the [[algebraic K-theory]] of these categories. There is a very simple very general nonsense behind this, that is described at [[K-theory]].

Notably the Grothendieck group completion of the [[decategorification]] of the category of [[vector bundle]]s on some [[topological space]] $X$ produces the group known as the [[topological K-theory]] of $X$.

Given this one speaks more generally of the ([[algebraic K-theory|algebraic]]) [[K-theory]] group of a suitable category (one presenting a [[stable (∞,1)-category]] in some way) as its _Grothendieck group_ .

In that sense, the Grothendieck group of a ($\infty$-)category $C$ with a notion of [[fibration sequence|cofibration sequence]]s is the [[decategorification]] set $K(C)$ equipped with a notion of addition that is encoded in these homotopy exact sequences.


# Definition #

We first state the definition of "Grothendieck group completion" -- which is really just the _free group completion of an abelian [[monoid]]_ --  and then the definition of Grothendieck group in the sense of [[algebraic K-theory]]. Notice that a priori both concepts are entirely independent constructions on different entities. But in various special case both can be applied to specific objects so as to produce the same result.

## the group completion of a monoid ##

Every abelian [[group]] is in particular an abelian [[monoid]]. There is a [[stuff, structure, property|forgetful functor]]

$$
 F :  Grps \to Monoids
 \,.
$$

To go the other way around we may ask for a [[left adjoint]] to this forgetful functor. This will take an abelian monoid $A$ and send it to an abelian group $G(A)$ with the property that for every abelian group $K$ with underlying abelian monoid $F(K)$ every morphism of monoids $A \to F(K)$ corresponds to a morphism of groups $G(A) \to K$.

This $G(A)$ is called the **group completion** or the **Grothendieck group completion** of $A$.

There are several ways to describe this. A popular one is to realize $G(A)$ as the [[quotient object|quotient]] of the [[product]] abelian monoid $A \times A$ under the equivalence relation

$((a_1,b_1) \sim (a_2,b_2)) \Leftrightarrow \exists k : a_1 + b_2 + k = a_2 + b_1 + k$

+-- {: .un_remark}
###### Remark

The idea of the free group on an abelian monoid is a very simple algebraic idea that, at least for a cancellative monoid (so that the unit is monic and one can reasonably use the term 'completion') certainly predates Grothendieck. That $\mathbb{Z}$ is the group completion of $\mathbb{N}$ goes back at least to Kronecker.
=--


## the concept related to algebraic K-theory ##

Fundamentally a Grothendieck group is something assigned to a [[stable (∞,1)-category]]. It is the group structure 
$+ : K(C)\times K(C) \to K(C)$ on the [[decategorification]] $K(C)$ of $C$ defined by the rule that for every [[fibration sequence]] 

$$
  A \to X \to B
$$ 

in $C$ the equivalence classes $[A]$, $[B]$ and $[X]$ satisfy

$$
  [X] = [A] + [B]
  \,.
$$

In particular the inverse $-[A]$ of an element $[A]$ is the class of its [[loop space object]] $\Omega A$ or equivalently of its [[delooping]] $\mathbf{B} A$ called the _suspension_ $\Sigma A$, since by definition the sequences

$$
  \Omega A \to 0 \to A
$$

and

$$
  A \to 0 \to \Sigma A
$$

are [[fibration sequence]], so that

$$
  [A] + [\Omega A] = 0
$$

and

$$
 [A] + [\Sigma A] = 0
 \,.
$$

But there are many ways to _model_ a [[stable (∞,1)-category]] by an ordinary category. Essentially for each of these ways there is a seperate prescription for how to model the above general construction in terms of concrete 1-categorical constructions.

In particular from an

* [[abelian category]]

and a

* [[Quillen exact category]]

one obtains the corresponding [[category of chain complexes|categories of chain complexes]]. These are [[stable (infinity,1)-category|stable (∞,1)-categories]]. Below we list presciptions for how to compute the Grothendieck/K-theory groups of these in terms of the underlying 1-categories.

Apart from the case of abelian categories, this requires some handle on the fibration sequences. A tool developed to handle exactly this for the purpose of computing Grothendieck/K-theory groups is the notion of a [[Waldhausen category]]. That provides the sufficient extra information to get a hand on the homotopy exact sequences.


### of an abelian category ### 

Let $C$ be an [[abelian category]].  The **Grothendieck group** or [[algebraic K-theory]] group of $C$, denoted $K(C)$, is the [[abelian group]] generated by [[decategorification|isomorphism class]]es of objects of $C$, with relations of the form 

$$[X] = [A] + [B] $$

whenever there is a [[short exact sequence]] 

$$ 0 \to A \to X \to C \to 0 $$


### of a Quillen exact category ###

An exact category $C$ in the present sense is a full [[subcategory]]
of an [[abelian category]] $\hat C$ such that the collection
of all sequences $0 \to A \to X \to B \to 0$
in $C$ that are [[exact sequence]]s in $\hat C$ has the property that for every [[exact sequence]] $A \to X \to B$ in $\hat C$ with $A$ and $B$  \in $C$ also their "sum" $X$ is in $C$.

Given an exact category $C$ with the inherited notion of exact sequences this way, the definition of its Grothendieck group is as above.


### of a Waldhausen category ###


A [[Waldhausen category]] is a [[category with weak equivalences]] with an [[initial object]] -- called $0$ -- and equipped with the notion of auxiliary morphism called _cofibrations_. These satisfy some axioms which are such that the ordinary 1-categorical [[cokernel]] of a cofibration $A \hookrightarrow X $, i.e. the ordinary [[pushout]]

$$
  \array{
    A &\hookrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    0 &\to &  B 
  }
$$

computes the desired [[homotopy colimit|homotopy]] [[pushout]]. (This is exactly dual to the reasoning by which one computes [[homotopy pullback]]s in a [[category of fibrant objects]]. See there for details.)

Therefore in a Waldhausen category a [[fibration sequence|cofibration sequence]] is a [[pushout]] sequence

$$
 A \hookrightarrow X \to B
$$

where the first morphism is a cofibration.

The Grothendieck/[[K-theory]]-group of the [[Waldhausen category]] $C$ is then, as before, on the [[decategorification]] $K(C)$ the abelian group structure given by

$$
  [X] = [A] + [B]
$$

for all cofibration sequences as above.




##Examples##

* The Grothendieck group of the [[Quillen exact category]] of [[vector bundle]]s on a space $X$ is called the [[topological K-theory]] of $X$.

  Notice that vector bundles do not form an [[abelian category]].


* The Grothendieck group of the category of finite-dimensional complex-linear [[representations]] of a [[group]] is called its [[representation ring]].

These two examples illustrate a general fact: the Grothendieck group of a [[monoidal category|monoidal]] [[abelian category]] inherits a ring structure from the tensor product in this category, and thus becomes a ring, called the [[Grothendieck ring]]. See also the general discussion at [[decategorification]].

* Every [[Quillen exact category]] $C$ is canonically equipped with the structure of a [[Waldhausen category]]. The two different prescriptions for forming the Grothendieck group $K(C)$ of $C$ do coincide.


+-- {: .query}

[[Urs Schreiber]]: the category of vector bundles is not abelian, but just Quillen exact. I added a clause to that effect above. 

Generally, my feeling is that "Grothendieck group" refers to "Grothendieck group completion of a monoid". The first definition at the Wikipedia entry on Gorthendieck group. 

What is described here -- the group defined by sequences -- is the definition of the K-theory group in algebraic K-theory. This is described at the beginning of [[K-theory]]. 

I'd think that the logic is rather that in some cases both concepts happen to coincide: the algebraic K-theory of the category of bounded complexes of vector bundles on a space happens to coincide with the Grothendieck group completion of the monoid of isomorphism classes of vector bundles.

My feeling is that the Wikipedia entry is a bit suboptimal in its second part, where it effectively calls algebraic K-theory the "Grothendieck group completion". I'd think one shouldn't do that in this generality.

Another thing in this context is the statement about the exact sequences. It is really the _homotopy_ exact sequences namely the [[fibration sequence]]s that count. Of course some of them can be computed by ordinary exact sequences if these are sufficiently cofibrant. That's what the structure provided by a [[Waldhausen category]] structure provides: a realization of the homotopy exact sequences as pushouts of cofibration morphisms. 

So in summary my feeling is: the entry in its current form actually tries to define algebraic K-theory and not the Grothendieck group concept, and that description with a few subtleties taken care of is currently at [[K-theory]] and should eventually be copied/moved to [[algebraic K-theory]]. The entry titled "Grothendieck group" should discuss the concept where from a monoid $A$ a group structure on $A \times A$ is defined by dividing out the equivalence relation $(a_1,b_1) \sim (a_2,b_2) \Leftrightarrow \exists k : a_1 + b_2 + k = a_2 + b_1 + k$.

But maybe I am mixed up. Let me know what you think.

_Toby_:  Well, I\'ll say this: I always understood 'Grothendieck group' in the article text above, and I never understood 'K-theory'.  That may have been my fault, of course, and it may be telling that I was John\'s student.

[[Urs Schreiber]]: so Weibel in his book referenced below indeed says "Grothendieck group" synonomously for "algebraic K-theory group" and says just "group completion" (chapter to section 1) for what I suggested should properly be called "Grothendieck group completion". 

I added corresponding remarks to the beginning of the entry. And I created two subsections under "Definintion". One for plain group completion. The other for algebraic K-theory groups.

_Toby_:  The idea of the free group on an abelian monoid is a very simple algebraic idea that, at least for a cancellative monoid (so that the unit is monic and one can reasonably use the term 'completion') certainly predates Grothendieck. That $\mathbb{Z}$ is the group completion of $\mathbb{N}$ goes back at least to Kronecker.

[[Urs Schreiber]]: I copied that last paragraph of yours into the section above. I still think that many people will say "Grothendieck group" for this group completion. But maybe I am wrong and we should branch off another page on "free group completion".

=--

# References #

In 

* Charles Weibel, _The K-book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))

see

* section 2: _The Grothendieck group $K_0$_ ([pdf](http://www.math.rutgers.edu/~weibel/Kbook/Kbook.II.pdf))