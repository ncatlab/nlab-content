<div class="rightHandSide toc">
[[!include model category theory - contents]]
***
[[!include homotopy - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}

# Idea #

In great generality, a _homotopy limit_ is a way of constructing appropriate sorts of [[limit]]s in a [[higher category theory|(weak) higher category]] using some "presentation" of that higher category by a stricter structure.  The general study of such presentations is [[homotopy theory]].

In classical homotopy theory, the presentation is given by a [[category with weak equivalences]], possibly satisfying extra axioms such as those of a [[homotopical category]], a [[category of fibrant objects]], or a [[model category]].  Such structures are considered to present an $(\infty,1)$-[[(infinity,1)-category|category]], and homotopy limits give a way of constructing the appropriate sort of "$(\infty,1)$-limits" in an $(\infty,1)$-category.

In [[enriched homotopy theory]], the presentation is given by an [[enriched model category]] or an [[enriched homotopical category]], and it presents an "enriched $(\infty,1)$-category."  Here the appropriate notion is a [[weighted limit|weighted]] homotopy limit, which is expected to construct "weighted $(\infty,1)$-limits" in the presented "enriched $(\infty,1)$-category."  Note that as yet, no fully general notion of "enriched $(\infty,1)$-category" exists; see [[homotopical enrichment]].


#Definitions #

As for ordinary [[limit]]s,
there are two ways to define homotopy limits:

* with explicit constructions that satisfy a _local_ universal property: the homotopy limit object "represents homotopy-coherent cones up to homotopy."

* as [[derived functor]]s that satisfy a _global_ universal property: the homotopy limit _functor_ is "universal among homotopical approximations to the strict limit functor."

One of the central theorems of the subject is that in good cases, the two give equivalent results; see below.


## Global definition ##

Let $C$ be a [[category with weak equivalences]] and let $D$ be a (small) category.  Make the [[functor category]] $[D,C]$ into a category with weak equivalences by taking the weak equivalences to be those [[natural transformation]]s which are objectwise weak equivalences in $C$.

The **homotopy limit** of a functor $F : D \to C$ is the image of $F$ under the right [[derived functor]], if it exists, of the [[limit]] functor $lim_D : [D,C] \to C$ with respect to the given weak equivalences on $C$ and the objectwise weak equivalences on $[D,C]$:
$$
  holim_D F := (R lim_D)F
  \,.
$$
In the enriched case, this must be suitably modified to deal with [[weighted limit|weighted limits]] as well as enrichment of both $C$  and $D$.


## Local definition ##

The local definition requires making precise the notion of a _[[homotopy]] commutative cone_ over a diagram. 

For the case of [[SimpSet]]-[[enriched category|enrichment]] one elegant way to do so is in terms of suitable [[weighted limit]]s as described in the example section at [[weighted limit]]: a homotopy commutative cone with tip $c \in C$ over a diagram $F : K \to C$ in an $\Simp\Set$-enriched category $C$ is a natural transformation 
$W \Rightarrow C(c,F(-)) : K \to \Simp\Set$ where the _weight_ functor $W$ is not constant on the point, as for ordinary limits, but is given by $W : k \mapsto N(K/k)$.


The same idea works if we are enriched over a category $V$ that is not $\SimpSet$ but is itself enriched over $\Simp\Set$, such as [[topological space]]s or [[spectrum|spectra]], since then any $V$-category becomes a $\Simp\Set$-category as well in a natural way.  Finally, although a general [[model category]] need not be enriched over anything, it is always "almost" enriched over $\Simp\Set$, and so one can still make sense of this using the techniques of _framings_ and _resolutions_; see the books of Hirschhorn and Hovey.

Following the reasoning described in Example 1 of [[representable functor]] one then defines the homotopy limit $L$ of a functor $F: K \to C$ to be a representing object for such homotopy cones, in the sense that we have a (weak) equivalence
$$ Map(X,L) \simeq HoCones(X,F)$$
of [[hom-objects]] (spaces or simplicial sets in the classical context; enriched hom-objects in the enriched context).


## Global versus local ##

The global definition is formulated in terms of [[weak equivalence|weak equivalences]] only, while the local definition is formulated in terms of [[homotopy|homotopies]] only.  However, in practical cases, derived functors exist because their input objects (in this case, the diagram $F$) can be replaced by "good" (fibrant and/or cofibrant) objects in such a way that weak equivalences become _homotopy_ equivalences.  The derived functor of $lim$ at the input object $F$ is then computed by applying the ordinary functor $lim$ to a good replacement $R F$ of $F$.

It then turns out that the "good" (precisely, "fibrant") replacement $R F$ "builds in" precisely the right homotopies so that an ordinary cone over $R F$ is the same as a homotopy-commutative cone over $F$.  Therefore, $lim (R F)$, which is the global homotopy-limit of $F$, is a representing object for homotopy-commutative cones over $F$, and thus is also a local homotopy-limit of $F$.  There is a dual argument for colimits using cofibrant replacements.

Formal versions of this argument can be found in many places.  Perhaps the original statement can be found in XI.8.1 of:

* A. K. Bousfield and D. M. Kan, _Homotopy limits, completions, and localizations_.

(As was often the case with Kan's papers at that time, there are some details omitted from that treatment, but most are, as he claimed, quite easy to complete.)  For another approach in an algebraic context, there is a description in Illusie's thesis.

An abstract version in modern language, with proof, can be found in

* Michael Shulman, [Homotopy limits and colimits and enriched homotopy theory](http://arxiv.org/abs/math/0610194).


### Strictness ###

Another notable difference between the local and global definitions is that the global definition can only ever define the homotopy limit up to weak equivalence (isomorphism in the homotopy category), while in the local definition we _could_ require, if we wanted to, an actual isomorphism
$$ Map(X,L) \cong HoCones(X,F)$$
of hom-objects, rather than merely a weak equivalence.  By analogy with [[strict 2-limit|strict 2-limits]], we may call such an object a **strict homotopy limit**.

Frequently a strict homotopy limit does in fact exist, and can be constructed as a [[weighted limit]] in the ordinary (enriched) category in question.  In such cases, the strict homotopy limit may be easier to compute with than an arbitrary homotopy limit merely known to have the up-to-weak-equivalence universal property.  Thus, sometimes when people say [[generalized the|the]] homotopy limit they refer mean a _strict_ homotopy limit.

When a strict homotopy limit exists, an arbitrary homotopy limit may be defined as an object which is (weakly) equivalent to the strict homotopy limit.


# Homotopy limits versus higher categorical limits

As a special case of enriched homotopy theory, we may consider model categories or homotopical categories that are enriched over a notion of $n$-category as presentations for $(n+1)$-categories.  (Here we allow $n$ to also be of the form [[(n,r)-category|(n,r)]], with the obvious convention that $(n,r)+1 = (n+1,r+1)$ and $\infty+1=\infty$.)  For example:

* [[simplicial set]]s are models for $\infty$-[[infinity-groupoid|groupoids]] ($(\infty,0)$-categories), so [[simplicial model category|simplicial model categories]] are presentations for $(\infty,1)$-categories.  Of course, arbitrary model categories are also presentations for $(\infty,1)$-categories, but simplicial model categories are easier to work with, and in particular easier to construct homotopy limits in.

* A [[Cat]]-enriched category is just a [[strict 2-category]], so a [[model 2-category]] or [[homotopical 2-category]] is a presentation of a weak [[2-category]] (or [[bicategory]]).

* A $(2Cat,\otimes_{Gray}$)-enriched category is a [[Gray-category]], and a [[model Gray-category]] or [[homotopical Gray-category]] is a presentation of a weak [[3-category]] (or [[tricategory]]).

If $C$ is a category enriched over $(n-1)$-categories and we are considering it to _be_ an $n$-category (which happens to be strict at the bottom level), it is natural to define a "weak equivalence" in the underlying ordinary category of $C$ to be a morphism that is an $n$-category-theoretic [[equivalence of categories|equivalence]].  We call this the _natural_ or _trivial_ homotopical structure on $C$.  In certain cases (such as $n=2)$ it can be made into a model structure, also called _natural_ or _trivial_.

Since higher categorical limits are generally defined as representing objects for cones that commute up to [[equivalence]], it is unsurprising that if $C$ has a natural homotopical structure, locally-defined homotopy limits and $n$-limits coincide.  For $n=1$ this is trivial.  For $n=2$ it is proven in the paper of Gambino referenced below (particularly section 6).  For $n=(\infty,1)$ it is proven in (among other places) Lurie's book, section 4.2.4.  The case $n=3$ ought to be approachable in theory, but doesn't seem to have been done (probably partly because the general theory of 3-limits is fairly nonexistent).

On the other hand, we may also consider a category $C$ enriched over $n$-categories with a _larger_ class of weak equivalences than just the $n$-categorical equivalences.  Then $C$ presents an $n$-category (its "homotopy $n$-category") obtained by formally turing these weak equivalences into $n$-categorical equivalences.  Homotopy limits in $C$ with this homotopical structure should then present $n$-limits in its homotopy $n$-category.  In the case $n=(\infty,1)$ this is also essentially in Lurie's book; for other values of $n$ it may not be in the literature.


# Examples #

## Homotopy pullbacks ##

Let $D = \{ 1\to 0 \leftarrow 2\}$ be the pullback [[diagram]], so that limits over it compute [[pullback]]s, and assume that $F : D \to C$ is such that
$$
  F(1) \to F(0) \leftarrow F(2)
$$
satisfies
* $F(i)$ is fibrant for all $i$;
* and either $F(1) \to F(0)$ or $F(2) \to F(0)$ is a fibration;

then

* $holim_D F$ exists;
* and is weakly equivalent to the ordinary limit $holim_D F \stackrel{\simeq}{\to} lim_D F$.

Conversely this means that on an arbitrary pullback diagram  $holim_D F$ can be computed by finding a natural transformation $F \Rightarrow R F$ whose component morphisms are weak equivalences and such that $R F$ satisfies the above conditions.


## Based loop objects ##

Let $C$ be a [[category of fibrant objects]]. Then for $B$ any [[pointed object]] with point $pt \stackrel{pt_B}{\to} B$ we have

$$
  holim(  pt \stackrel{pt_B}{\to}  B \stackrel{pt_B}{\leftarrow} pt)
  \;\stackrel{\simeq}{\to}\;
  \Omega_{pt} B
  \,,
$$
where $\Omega_{pt} B$ is the based [[loop space object]] of $B$.

This follows from the above prescription by noticing that the [[generalized universal bundle]] $\mathbf{E}_{pt} B$ provides a fibrant replacement of the pullback diagram in that we have

$$
  \array{
     pt &\to& B &\leftarrow& pt
     \\
     \downarrow^{\simeq} && \downarrow^{Id} && \downarrow^{Id}
     \\
    \mathbf{E}_{pt}B &\to& B &\leftarrow& pt
  }
$$

with all vertical morphisms weak equivalences and with the left bottom horizontal morphism a fibration.


## Homotopy pullback of a point over a group / universal bundles ##

As a special case of the above general example we get the following.

Let $C =$ [[Grpd]] equipped with the [[folk model structure]]. Write $G$ for a [[group]] regarded as a discrete monoidal groupoid (elements of $G$ are the objects of the groupoids and all morphisms are identities) write and $\mathbf{B}G$ for the corresponding one-object [[groupoid]] (single object, one morphism per element of $G$). Write $pt$ for the terminal groupoid (one object, no nontrivial morphism). 
Notice that there is a unique functor $pt \to \mathbf{B}G$.
Then we have
$$
  holim
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       pt &\to& \mathbf{B}G
    }
  \right)
  \stackrel{\simeq}{\to}
  G
  \,.
$$
To see this, we compute using the above prescription by finding a weakly equivalent pullback diagram such that one of its morphisms is a fibration. This is achived in particular by the [[generalized universal bundle]]
$pt \stackrel{\simeq}{\to} \mathbf{E}G \to\gt \mathbf{B}G$, where $\mathbf{E}G$ is the [[action groupoid]] $G//G$ of $G$ 
acting on itself by multiplication from one side. So we have a weak equivalence of pullback diagrams
$$
  \array{
     pt &\to& \mathbf{B}G &\leftarrow& pt
     \\
     \downarrow^{\simeq} && \downarrow^= &&
     \downarrow^= 
     \\
     \mathbf{E}G &\to\gt& \mathbf{B}G &\leftarrow& pt 
  }
$$
and the homotopy limit in question is weakly equivalent to the ordinary limit over the lower diagram. That is directly seen to be $Disc(Obj(\mathbf{E}G)) = Disc(Obj(G//G)) = Disc(G)$ which we just write as $G$:
$$
  holim 
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       pt &\to& \mathbf{B}G
    }
  \right)
  \stackrel{\simeq}{\to}
  lim
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       \mathbf{E}G &\to\gt& \mathbf{B}G
    }
  \right)  
  = G
  \,.
$$
This example is important in the context of [[groupoidification]] and [[geometric function theory]], as described there.

## Homotopy pullback of a subgroup over a group ##

The above example generalizes straightforwardly
to the case where the trivial 
inclusion $pt \to \mathbf{B}G$ is replaced by any inclusion  $\mathbf{B}H \hookrightarrow \mathbf{B}G$ of any subgroup $H$ of $G$ pretty much literally by replacing $pt$ by $\mathbf{B}H$ throughout. 

One finds

$$
  holim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{B}H &\to& \mathbf{B}G
   }
  \right)
  \stackrel{\simeq}{\to}  H \backslash\backslash G//H
$$

where on the right we have the [[action groupoid]] of $H \times H$ acting on $G$ by multiplication from the left (first factor) and the right (second factor).

To see this, we again build a fibrant replacement of the pullback diagram. Following the constructions at [[generalized universal bundle]] consider first the groupoid $\mathbf{E}_{\mathbf{B}H}G$ given by the pullback diagram

$$
  \array{
    \mathbf{E}_{\mathbf{B}H}G &\to& \mathbf{B}H
    \\
    \downarrow && \downarrow
    \\
    [I, \mathbf{B}G] &\stackrel{d_0}{\to}& \mathbf{B}G
    \\
    \downarrow^{d_1} 
    \\
    \mathbf{B}G
  }
  \,.
$$

As at [[generalized universal bundle]] one proves that the left vertical morphism
$\mathbf{E}_{\mathbf{B}H}G \to \mathbf{B}G$ is a fibration.

Now, notice (which was implicit in the above example) that since $[I,\mathbf{B}G]$ is a [[path object]] in a [[category of fibrant objects]] we have a [[section]]
$
  \mathbf{B}G \stackrel{\simeq}{\to}^\sigma  [I, \mathbf{B}G] 
$
of $[I,\mathbf{B}G] \stackrel{d_0}{\to} \mathbf{B}G$. In the above pullback diagram this induces a morphism 
$
  \mathbf{B}H \stackrel{\sigma}{\to} \mathbf{E}_{\mathbf{B}H}G
$ 
making the obvious diagram commute. Now, the latter morphism, being the pullback of an acyclic fibration is an acyclic fibration, so its right inverse $\sigma$ is a weak equivalence. This way we obtain the morphism of pullback diagrams

$$
  \array{
    \mathbf{B}H &\to& \mathbf{B}G &\leftarrow& \mathbf{B}H
    \\
    {}^\simeq\downarrow^{\sigma} && \downarrow^{Id} 
     && \downarrow^{Id} 
    \\
    \mathbf{E}_{\mathbf{B}H}G &\to \gt& \mathbf{B}G &\leftarrow& \mathbf{B}H
  }
$$
which is objectwise a weak equivalence and such that the horizontal morphism on the bottom left is a fibration. By the above statement the ordinary limit of the lower horizontal diagram is weakly equivalent to the homotopy limit we are looking for. But this is manifestly the desired action groupoid:

$$
  holim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{B}H &\to& \mathbf{B}G
   }
  \right)
  \stackrel{\simeq}{\to}
  \lim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{E}_{\mathbf{B}H} G &\to& \mathbf{B}G
   }
  \right)
  \simeq
  \lim\left(
   \array{
     && [I,\mathbf{B}G]
     \\
     && \downarrow^{d_0 \times d_1}
     \\
     \mathbf{B}H \times \mathbf{B}H 
     &\to& \mathbf{B}G \times \mathbf{B}G
   }
  \right)
  =
  H \backslash\backslash G//H
  \,.
$$

This example, too, is important at [[geometric function theory]].



## Homotopy span traces ##

* see the homotopy span traces discussed at 
  [[span trace]] for more examples of homotopy pullbacks

## Descent objects ##

_Descent objects_ as they appear in [[descent|descent and codescent]] are naturally conceived as homotopy limits. See also [[infinity-stack]].

# References #

* A. K. Bousfield and D. M. Kan, _Homotopy limits, completions, and localizations_.  Springer LNM 304.  The classical reference; see in particular chapter XI.

* Wojciech Chacholski and Jerome Scherer, _Homotopy theory of diagrams_ ([arXiv](http://arxiv.org/abs/math.AT/0110316)) includes a global definition of homotopy (co)limit as [4.1, p. 14](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=19), and discusses how to compute them (co)limits concretely using local constructions.  For instance the above statement on the computation of homotopy pullbacks is proposition [2.5, p. 15](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=20)

* Philip Hirschhorn, _Model categories and their localizations_.  Defines and studies (local) homotopy limits in model categories.

* Dwyer, Hirschhorn, Kan, Smith, _Homotopy limit functors in model categories and homotopical categories_.  Defines global homotopy limits in homotopical categories and computes them using local constructions.

* Michael Shulman, [Homotopy limits and colimits and enriched homotopy theory](http://arxiv.org/abs/math/0610194).  Constructs and compares local and global weighted homotopy limits in enriched homotopical categories.

* Nicola Gambino, _Homotopy limits for 2-categories_ ([pdf](http://www.lacim.uqam.ca/~gambino/homotopy.pdf)), published as: Mathematical Proceedings of the Cambridge Philosophical Society 145 (2008) 43-63.)  Proves that homotopy limits in a 2-category with its natural model structure coincide with 2-categorical [[strict 2-limit|pseudo-limits]], and hence give [[2-limit]]s.

* [[Jacob Lurie]], [[Higher Topos Theory]].  Lots of stuff about $(\infty,1)$-categories, including the computation of homotopy limits (section 4.2.4).

* Andre Hirschowitz, Carlos Simpson.  [Descent pour les n-champs](http://arxiv.org/abs/math.AG/9807049).  Probably there is some good stuff in here about homotopy limits and limits in $(\infty,n)$-categories.


+--{.query}
[[Tim Porter|Tim]]  Mike, are you intending to treat the case of when the domain category, $D$ is the above, is enriched as well? This would handle the example of homotopy limts of homotopy coherent diagrams, both in Vogt's sense and in the simplicially enriched case looked at by Bourn and Cordier. This would also allow the $G$ in one of the examples to be a simplicial or topological group, or to be (?) and A-infinity category. (Some of those examples may be already dealt with in others of the entries as different people classify things in different ways.)

Perhaps some of the more classical referencs, Vogt, Bousfield-Kan etc. might be included for completeness.

[[Mike Shulman|Mike]]: Yes, certainly; my paper referenced above deals with the case when $D$ is enriched as well.  There are cofibrancy technicalities, of course.  I'm not against including the classical references, although I find them fairly impenetrable myself.

=--

[[!redirects homotopy limits]]
[[!redirects homotopy colimit]]