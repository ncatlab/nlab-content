
#effective epimorphism#
* automatic table of contents goes here
{:toc}

## Definition ##

An **effective epimorphism** is a [[morphism]] $f : c \to d$ (in a given [[category]]) that has a [[kernel pair]] $c \times_d c$ and is the [[quotient object]] of this kernel pair in that 

$$
  c \times_d c \stackrel{\to}{\to} c \stackrel{f}{\to} d
$$

is a [[colimit]] diagram (a [[coequalizer]]).  The reader should be aware, however, that some writers use "effective epimorphism" to mean what is here called a [[strict epimorphism]].

In other words this says that $f : c \to d$ is effective if $d$ is the [[coimage]] of $f$.

Sometimes we say that such morphism $f$ is an [[effective quotient]].

## Remarks ##

The [[duality|dual]] concept is that of [[effective monomorphism]].

An effective epimorphism is necessarily a [[regular epimorphism]].  Conversely, any regular epimorphism that has a kernel pair is an effective epimorphism.

In [[Set|the category of sets]], every [[epimorphism]] is effective. Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using effective epimorphisms.


## definition for $(\infty,1)$-categories ##

Notice that we may equivalently reinterpret the condition that

* a morphism $\pi : U \to X$ is the [[quotient object]] of its [[kernel pair]] $U \times_X U \stackrel{\to}{\to} U$

by saying that $X$ is the [[colimit]] over the entire [[Čech nerve]] 

$$
  \cdots
  U \times_X U \times_X U
  \stackrel{\to}{\stackrel{\to}{\to}} 
  U \times_X U \stackrel{\to}{\to} U
$$

of $\pi$.

This is the formulation that generalizes to [[higher category theory|higher categorical context]].


In an $(\infty,1)$-[[(infinity,1)-category|category]] $C$, an _effective epimorphism_ 
$f : U \to X$ is a morphism such that its [[Čech nerve]] $U_\bullet$
is a [[simplicial resolution]] of $X$.

This is defined in [[HTT]] only for an $(\infty,1)$-[[semitopos]], but seems to be correct in general.

+-- {: .un_theorem}
###### Conjecture

In any $(\infty,1)$-category, an effective epimorphism is precisely a [[regular epimorphism]] that has a &#268;ech nerve.
=--
+-- {: .proof}
No serious attempt has been made to check this; it may be obvious ... or obviously false.
=--

+-- {: .query}

Presumably, we get the general definition in an arbitary $(\infty,1)$-[[(infinity,1)-category|category]] by simply including the requirement that $f$ *have* a &#268;ech nerve.  In an $(\infty,1)$-topos, is there any distinction to be drawn between an effective epimorphism and a regular epimorphism?  (There isn\'t in a [[topos]].)

[[Urs Schreiber]]: my understanding is that the effective epimorphisms are equivalently to be thought of as the regulkar epimorphisms in an $(\infty,1)$-topos, indeed. 

In HTT the notion of regular epimorphism is defined more generally in the context of a "semi $(\infty,1)$-topos".

The notion of [[groupoid object in an (infinity,1)-category]] is the categorification of [[equivalence relation]]. With that in mind the relation between regular/effective epimorphisms and equivalence relations/groupoid objects is the same.

_Toby_:  I would like to define both 'effective epimorphism' and 'regular epimorphism' in the general context of an $(\infty,1)$-category, rather than in two contexts that only partially overlap (a category, and an $(\infty,1)$-topos or $(\infty,1)$-semitopos).  Since Lurie doesn\'t do that, do we at least get a theorem (in an $(\infty,1)$-topos) that a regular epimorphism (as defined in a semitopos) is the same as an effective one (not just 'to be thought of' as that)?  If so, ...

I would like to say that a regular epimorphism in an $(\infty,1)$-topos is a morphism that is a simplicial resolution, and that an effective epimorphism is a morphism that has a &#268;ech nerve and is a simplicial resolution of that &#268;ech nerve.  I would like this to agree with Lurie\'s definition in the cases that he gives, and I would like Lurie\'s proof of the hypothetical theorem above to generalise to a theorem that an effective epimorphism is precisely a regular epimorphism that has a &#268;ech nerve.  Does that work?

[[Urs Schreiber]]: yes, I agree, that's how it should be (regular = is simplicial resolution, effective=that simplicial resolution is given by the Cech nerve)

As far as I can see Lurie doesn't define the term "regular epimorphism" at all.

It's very late here and I shouldn't be working anymore, but apart from that I'd say you'd be safe with doing what you propose to do. I am not sure which hypothetical theorem you mean. Seems like just a definition is needed for that particular statement. 

_Toby_:  Ah, I see, it\'s 'effective epimorphism' that Lurie defines for an $(\infty,1)$-semitops, while 'regular epimorphism' is never defined.

=--


[[!redirects effective epi]]
[[!redirects effective epimorphisms]]