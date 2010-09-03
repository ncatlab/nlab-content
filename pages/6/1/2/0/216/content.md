#Contents#
* automatic toc goes here
{:toc}

## Definition

The **category algebra** $k[C]$ over a [[ground field]] $k$ of a small [[category]] $C$ is the [[vector space]] whose basis is  the morphisms of $C$, where the product of two morphisms $f$ and $g$ is defined to be their composite if [[composable pair|composable]], and $0$ otherwise:
$$
  f \cdot g := \left\lbrace
    \array{
      g \circ f & if composable
      \\
      0 & otherwise
    }
  \right.
 \,.
$$ 

## Remarks

If the category $C$ is a [[groupoid]] with a single object, which may be canonically identified with a group $G$, then the category algebra coincides with the familiar [[group algebra]] of $G$: 
$$
 k[C] = k[G]
  \,.
$$

## Weak colimit interpretation {#WeakColimit}

Apparently for $C$ a [[groupoid]] the 
category algebra of $C$ is the [[weak limit|weak colimit]] over $C$ of the functor $C \to Vect\text{-}Mod$
constant on the ground field algebra.

The 2-cell in the universal co-cone corresponding
to the morphism $f \in C$ is the $k\text{-}k[C]$-bimodule
homomorphism $f \cdot (-) :  A \to A$ that multiplies
by $f \in k[C]$ from the left.

This description should be compared with the analogous description of the [[action groupoid]] by a weak colimit. One sees that the groupoid algebra is a linear incarnation of the action groupoid in some sense.

This statement is for instance of great relevance (while very secretly hidden underneath the surface) in section 8.4 of 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv](http://arxiv.org/abs/0905.0731))



## Span composition interpretation 

The category algebra of a category $C$ is a special case of a general [[arrow theory|arrow-theoretic]] construction that appears in [[quantization]] and in the theory of [[bi-brane]]s. 

In order not to get distracted by inessential technicalities, consider the case of a finite [[category]] $C$, i.e. an [[internal category]] in [[FinSet]]. This is a [[span]]
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
  }
$$
equipped with a composition operation: a morphism
of spans from the composite span 
$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
     &&&&
     C_0
  }
$$
to the original one, i.e. a morphism 
$$
  comp : C_1 \times_{t,s} C_1 \to C_1
$$ 
which respects source and target morphisms. 

Given this, consider the trivial vector bundle on the set of objects $C_0$. This is nothing but an assignment
$$
  I : C_0 \to Vect_k
$$
of the [[ground field]] $k$ to each element of $C_0$. There are two different ways to pull this vector bundle on objects back to a vector bundle on morphisms, once along the source, once along the target map. 

Then notice that the set of natural transformations between these two vector bundles
$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
$$
whose elements are 2-arrows of the form
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$
are canonically in bijection with $k$-calued functions on $C_1$, hence with the vector space spanned by $C_1$, hence with the vector space underlying the category algebra
$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
  \simeq
  k[C]
  \,.
$$

The algebra structure on $k[C]$ is similarly encoded in the diagrammatics: given two elements
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }

  \;\;\;\; 
  and
  \;\;\;\;

  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$
their pre-composite is the diagram
$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & \searrow &&& 
     \downarrow &&& \swarrow
     \\
     && \to &&Vect_k&& \leftarrow  
  }
  \,.
$$

This is a composite transformation between three trivial vector bundles on the set $C_1 \times_{t,s} C_1$ of composable morphisms in $C$. As such, it is a function, which on the element consisting of the composable pair $\stackrel{r}{\to}\stackrel{s}{\to}$ takes the value $f(r)\cdot g(s)$.

In order to get back a transformation between vector bundles on $C_1$, hence a transformation between vector bundles on $C_1$, we _push forward_ along the composition map $comp: C_1 \times_{t,s} C_1 \to C_1$. This just means that we add up the values on the fibers of this map.

The result is the [[convolution product]]
$$
  (f\star g) : t \mapsto \sum_{s\circ r = t}
  f(r)\cdot g(s)
  \,.
$$
This is indeed the product in the category algebra.

### References on this arrow-theoretic picture

The claim is that this way of looking at category algebras realizes them as a puny special case of a bigger story which involves [[bi-brane]]s as morphisms between $n$-bundles/$(n-1)$-gerbes which live on spaces connected by correspondence spaces. This is related to a bunch of things,  such as T-duality, Fourier-Mukai transformations and other issues of quantization. A description of this perspective is in

* [[schreiber:Nonabelian cocycles and their quantum symmetries]].

This is related to observations such as described here:


* John Baez, [_Quantization and Cohomology (Week 17)_](http://golem.ph.utexas.edu/category/2007/03/quantization_and_cohomology_we_16.html)

* Urs Schreiber, [_QFT of Charged n-Particle: T-Duality_](http://golem.ph.utexas.edu/category/2007/02/qft_of_charged_nparticle_tdual.html)


###Discussion: Terminological Nitpicking

I use $k[S]$ to stand for the free vector space on the set $S$.  This is compatible with the notation $k[G]$ for group algebra of $G$.  Urs' notation $k[C]$ for the category algebra is also compatible, but in a different way.  

Why is my notation better?  First, because I don't like the clunky notation $span_k(C)$ for the free vector space on the set $S$.   Second, because the equation $k[B G] = k[G]$ is inconsistent unless Urs is finally willing to admit that $B G = G$. <img src = "http://math.ucr.edu/home/baez/emoticons/tongue2.gif" alt = ""/>

So what would _I_ call the category algebra of $C$?  I guess $k[C_1]$ or $k[Mor(C)]$.  You might complain that <i>this</i> notation is clunky, and I'd see your point. However, it's a fact that whenever the category algebra is important, its representation on $k[C_0] = k[Ob(C)]$ also tends to be important --- so I think the benefits of a notation that handles both structures outweigh the disadvantages of a slight clunkiness. -- [[John Baez|John]] 

_[[Urs Schreiber|Urs]] says_: It is good that you said this, because we need to talk about this: I am puzzled by your attitude towards $\mathbf{B}G$ vs $G$. It is not the least a remark in your lecture notes with Mike that it is important to _distinguish_ between a $k$-tuply monoidal structure and the corresponding $k$-tuply degenerate category, even though there is a map identifying them. The issue appears here for instance when discussing the universal $G$-bundle in its groupoid-incarnation. It is 
$$
  G \to \mathbf{E}G \to \mathbf{B}G
$$
(where $\mathbf{E}G = G//G$ is the action groupoid of $G$ acting on itself). On the left we crucially have $G$ as a monoidal 0-category, on the right as a once-degenerate 1-category. In your notation you cannot even _write down_ the universal $G$-bundle! ;-)

Or take the important difference between group representations and group 2-algebras, the former being functors $\mathbf{B}G \to Vect$, the latter functors $G \to Vect$. This is important all over the place, as you know better than me.

Or take an abelian group $A$ and a codomain like $2Vect$. Then there are 3 different things we can sensibly consider, namely 2-functors

$$
  A \to 2Vect
$$
$$
  \mathbf{B}A \to 2Vect
$$
$$
  \mathbf{B}^2A \to 2Vect
  \,.
$$
All of this is different. All of this is needed. The first one is the group 3-algebra of $A$. The second is pseudo-representations of the group $A$. The third is representations of the 2-group $\mathbf{B}A$. We have notation to distinguish this, and we should use it.

Finally, writing $\mathbf{B}G$ for the 1-object $n$-groupoid version of an $n$-monoid $G$ makes notation behave nicely with respect to nerves, because then realization bars $|\cdot|$ simply commute with the $B$s in the game: $|\mathbf{B}G| = B|G|$.  I think this makes for instance your theorem with Danny appear in a prettier way.

This behaviour under nerves shows also that, generally, writing $\mathbf{B}G$ gives the right intuition for what an expression means. For instance, what's the "geometric" reason that a group representation is an arrow $\rho : \mathbf{B}G \to Vect$? It's because this is, literally, equivalently thought of as the corresponding classifying map of the vector bundle on $\mathbf{B}G$ which is $\rho$-associated to the universal $G$-bundle:

the $\rho$-associated vector bundle to the universal $G$-bundle is, in its groupoid incarnations,
$$
  \array{
    V
    \\
    \downarrow
    \\
    V//G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
  \,,
$$
where $V$ is the vector space that $\rho$ is representing on, and this is classified by the representation $\rho : \mathbf{B}G \to Vect$ in that this is the pullback of the universal $Vect$-bundle
$$
  \array{
    V//G
    &\to&
    Vect_*
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{B}G
    &\stackrel{\rho}{\to}&
    Vect
  }
  \,,
$$

In summary, I think it is important to make people understand that groups can be identified with one-object groupoids. But next it is important to make clear that not everything that can be identified is actually equal.

For instance concerning the crucial difference between the category in which $G$ lives and the 2-category in which $\mathbf{B}G$ lives. 

_Toby says_: John said:
>I use $k[S]$ to stand for the free vector space on the set $S$.  This is compatible with the notation $k[G]$ for group algebra of $G$.  Urs' notation $k[C]$ for the category algebra is also compatible, but in a different way.
Wait, are you claiming that $k[S]$ and $k[C]$ are incompatible? I disagree! Just as a [[set]] may be seen as a [[discrete category]], so a vector space (or [[module]]) may be seen as an algebra where all multiplication is zero. (This is well known in the theory of [[Lie n-algebroid]]s, where a vector space is a twice monoidal Lie 2-algebroid, that is a commutative Lie algebra.) Then $k[S] = k[D S]$ (where $D S$ is the discrete category on $S$), just as $k[B G] = k[G]$.

_[[Mike Shulman|Mike]] says_: Urs, I'm definitely with you about $G$ and $B G$, for all the reasons that you give and more.  (For instance, in classical homotopy theory, it is essential to distinguish between the two, for similar reasons.)  I'm not sure exactly what remark you're referring to in "n-categories and cohomology," but it's possible that it can be blamed on me rather than John.  In particular, anything in section 5 is my fault.

_Toby_: John, I\'m afraid that, despite the compatibility of $k[S]$ and $k[C]$, on the general issue (as at [[action]]), Urs and Mike have convinced me too.

_[[John Baez|John]] says_: Okay, fine.  I personally find it tiresome to use a notation that distinguishes between groups and one-object groupoids.  To me, having 'light notation', with a minimum of symbols, is incredibly important.  Every extra symbol makes my work look more complicated, reduces how many people will read it, and distracts attention from the actual ideas.  So, I don't want to write $B G$ unless I really need to.  For example, I agree with Urs that if I'm simultaneously discussing functors 
$$
  A \to 2Vect
$$
$$
  \mathbf{B}A \to 2Vect
$$
and
$$
  \mathbf{B}^2A \to 2Vect
$$
then I need to carefully distinguish between these.  (I actually use $A[n]$ to mean the $\infty$-category or chain complex with the abelian group $A$ as $n$-morphisms; this is pretty standard in homological algebra.)  But if in some passage of text I'm only taking about a functor like 
$$ \mathbf{B}^2A \to 2Vect$$
I prefer to say "think of $A$ as a 2-category with only one object and one morphism", and then write this functor as $A \to 2Vect$, to avoid polluting the page with tons of $B^2$'s.  

This probably isn't worth arguing about.  Some people prefer logically precise notation, while other people (like me) are always focused on maximizing readership.  These are different goals.  My ideal math paper would be mainly words with just a few equations per page, because that's the most fun to read.  But I don't expect everyone else to agree.

While we're nitpicking: do we really want the product $f\cdot g$ of morphisms $f$ and $g$ in the category algebra to equal $g \circ f$?  This seems designed to trip people up.

_[[Mike Shulman|Mike]]_: Here's another argument I just thought of, although it's still along the lines of "logically precise" so given what you just said, I guess it's unlikely to convince you.  What we are discussing is, in general, a functor from [[k-tuply monoidal n-category|k-tuply monoidal n-categories]] to $(k-1)$-tuply monoidal $(n+1)$-categories.  The delooping hypothesis says that it's an equivalence onto its image (at least as long as "0-tuply monoidal" means "pointed"), so from that point of view it's natural to want to leave it nameless and think of its domain as a subcategory of its codomain.

However, there is also another functor from $k$-tuply monoidal $n$-categories to $(k-1)$-tuply monoidal $(n+1)$-categories which adds identity $(n+1)$-cells and forgets one level of monoidal structure.  This one is not in general an equivalence onto its image.  But in the particular case $k=n=\omega$, in which case the domain and codomain of these functors are _both_ the category of stably monoidal $\omega$-categories, it is the _second_ functor that is the identity functor, not the first one.
