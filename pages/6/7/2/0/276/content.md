#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _crossed complex_ (of [[groupoid]]s) is a nonabelian and [[horizontal categorification|many object]] generalization of a [[chain complex]] of [[abelian group]]s.

Crossed complexes are an equivalent way to encode the information contained in [[strict ∞-groupoids]]: the groups appearing in the crossed complex in degree $n \geq 2$ are the source-fibers of the collection of $n$-morphisms of the $\omega$-groupoid.

See also [[homotopy n-type]]. 

One way to think of a crossed complex is as a chain complex in which the bottom part is a crossed module and the rest is a chain complex of modules over the fundamental group of the crossed complex (that is its cokernel).  This is easy to think of in the case where there is a single object (*crossed complex of groups*), and it is a simple step to extend to the many object case.



## History

Crossed complexes were defined by Blakers in 1948 (following a suggestion of [[Samuel Eilenberg]]) and developed by Whitehead in 1949 and 1950 (but these authors used different terminology). They were applied by [[Johannes Huebschmann]] to [[group cohomology]] in 1980. They were further developed in  series of articles by Ronnie Brown and collaborators in the context of [[nonabelian algebraic topology]], and partly because they were found equivalent to form of (strict) cubical $\omega$-groupoid with _connections_. This equivalence enabled a number of new results, including van Kampen type theorems and monoidal closed structures for crossed complexes. 

## Definition

A **crossed complex** $C$ is 

* a [[groupoid]]  $C_1 \stackrel{\overset{\delta_t}{\to}}{\underset{\delta_s}
{\to}} C_0$

* together with a sequence of skeletal groupoids $C_k$ of $C_0$ for $k \geq 0$ indexed by $C_0$, i.e. bundles of groups, [[abelian group|abelian]] for $k \geq 3$, sitting in a diagram 

  $$
    \array{
      \cdots &\to& C_3 &\stackrel{\delta}{\to}& C_2
      &\stackrel{\delta}{\to}&
      C_1
     \stackrel{\overset{\delta_t}{\to}}{\underset{\delta_s}
{\to}} 
     C_0
     \\
     && \downarrow && \downarrow && \downarrow^{\mathrlap{\delta_s}}
     && \downarrow^{\mathrlap{=}}
     \\
    \cdots &\to& 
    C_0
    &\stackrel{=}{\to}&
    C_0
    &\stackrel{=}{\to}&
    C_0
    &\stackrel{=}{\to}&
    C_0
    }
  $$

* together with an [[action]] of $C_1$ on $C_k$ for $k \geq 0$

such that

* the morphisms $\delta_k$ for $k \geq 2$ are morphisms of groupoids over $C_0$, compatible with the action by $C_1$

* $im(\delta_2) \subset C_1$ acts by conjugation on $C_2$ and trivially on $C_k$ for $k \geq 3$

* $\delta_{k-1} \circ \delta_k = 0$ for $k \geq 3$.

## Equivalence to strict $\infty$-groupoids

For $\mathcal{G}$ a globular [[strict ∞-groupoid]]

$$
  \cdots
  \stackrel{\overset{t}{\to}}{\underset{s}{\to}}   
  \mathcal{G}_3
  \stackrel{\overset{t}{\to}}{\underset{s}{\to}} 
  \mathcal{G}_2
  \stackrel{\overset{t}{\to}}{\underset{s}{\to}} 
  \mathcal{G}_1 
  \stackrel{\overset{t}{\to}}{\underset{s}{\to}} 
  \mathcal{G}_0
$$

the corresponding crossed complex $[\mathcal{G}]$ is defined by

* $[\mathcal{G}]_1 \stackrel{\to}{\to} [\mathcal{G}]_0$ :=
  $\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0$;

* for $k \geq 2$ $[\mathcal{G}]_k$ is the bundle of groups which over
  $x \in \mathcal{G}_0$ is the group of [[k-morphism]]s of $\mathcal{G}$
  that start at the identity on $x$:

  $$
    [\mathcal{G}]_k := \coprod_x s_k^{-1}(Id_x)
    \,.
  $$

The action of $[\mathcal{G}]_1$ on $[\mathcal{G}]_k$ is given by whiskering/conjugation of $k$-morphisms by 1-morphisms. The boundary maps $\delata : [\mathcal{G}]_{k} \to [\mathcal{G}]_{k-1}$ are the original target maps $t$, sending a $k$-morphisms with source an identity on an object to its target $k-1$-morphism.





## Examples

### In low degree

In low degrees crossed complexes are the following:

* A crossed complex of length 0 is a [[Set|set]].

* A crossed complex of length 1 is a [[groupoid]].

* A crossed complex of length 2 is a [[crossed module]], which is equivalent to a strict kind of [[2-group]] by the Brown-Spencer Theorem,
(R. Brown and C.B. Spencer, _G-groupoids, crossed modules and the fundamental groupoid of a  topological group_, Proc. Kon. Ned. Akad. v. Wet, 79, (1976), 296 &#8211; 302.)


+--{.query}
[[Tim Porter|Tim]]: One of many terminological problems that arise in this stuff is whether 'length' of a chain complex or crossed complex refers to the number of transitions/arrows or the number of nodes /groups or whatever?

(Alex Nelson): I think that the "length" refers to the number of morphisms. I suspect this since a length 0 chain complex is a set, which makes intuitive sense if it's just a single object without any morphisms...but I may be (and probably am) wrong.
=--

A discussion of the kind of homotopy types modelled by crossed complexes, namely a _linear_ model, and a conjecture as to how to extend this, is in [[homotopy n-type]]. 

### Specific examples

If $X_*$ is a [[filtered space]], then there is a crossed complex $\Pi X_*$ which in dimension 0 is $X_0$, in dimension 1 is the [[fundamental groupoid]] $\pi_1(X_1,X_0)$ and   in dimension $n \gt 1$ is the family of relative homotopy groups $\{\pi_n(X_n,X_{n-1},p) : p\in X_0\}$.  This gives a functor $\Pi$ from filtered spaces to crossed complexes, which may be used to construct the generalisation of the [[Dold-Kan correspondence]], which in this case goes between crossed complexes and [[simplicial T-complex]]es.  

An important special case of the above is when the filtered space is a CW-complex and the filtration is by skeleta.  Particularly useful instances of this are the $n$-cubes and $n$-simplices, with their CW-filtration.  We obtain $\Pi(I^n)$ and $\Pi(\Delta^n)$.  These are used to define cubical and simplicial nerves of a crossed complex and these in turn define the [[Dold-Kan correspondence]] mentioned above.  For instance if $C$ is a crossed complex, then its simplicial nerve is the simplicial set with $Ner(C)_n = 
Crs(\Pi(\Delta^n),C)$ in dimension $n$.

## Crossed complexes as Moore complexes

Crossed complexes (of groups) correspond to [[group T-complex|group T-complexes]]. Any group $T$-complex is a simplicial group and in the entry for them it is mentioned that a simplicial group has a group $T$-complex structure if and only if $\mathcal{N}G\cap D$ is the trivial graded subgroup, where 
$D = (D_n)_{n\geq 1}$ is the graded subgroup of $G$ generated by the degenerate elements. If $G$ is such a group $T$-complex then its [[Moore complex]] has a natural structure of a crossed complex. In general the obstruction to a given simplicial group to have  Moore complex which is a crossed complex is exactly that graded subgroup, $\mathcal{N}G\cap D$. (The [[Whitehead product|Whitehead products]] for $G$ live in this graded subgroup, so this provides one way of showing that the homotopy types representable by crossed complexes have trivial  Whitehead products.)

Conversely, for any crossed complex, $C$, there is a simplicial group, $K(C)$, constructed using an analogue of the inverse in the [[Dold-Kan correspondence]], which is a group $T$-complex and whose Moore complex is isomorphic to $C$.

The generalisation to general crossed complexes (of groupoids) and simplicially enriched groupoids
if quite easy to do. We will usually state results below for the group case, leaving the general case to the 'reader'.


## From simplicial group(oid)s to crossed complexes

It is fairly clear that crossed complexes / group(oid) $T$-complexes correspond to [[simplicial group]](oid)s in which certain  equations hold.  It therefore is reasonable that they are equivalent to a variety / [[reflective subcategory]] in the category, $SSet Grpd$, of simplicially enriched groupoids.  (The discussion in the entry on [[group T-complex]] is relevant here.)

There is a functor $C(-)$ from simplicial groups to crossed complexes given by 

$${C}(G)_{n+1} = \frac{\mathcal{N}G_n}{(\mathcal{N}G_n\cap D_n)d_0(\mathcal{N}G_{n+1}\cap D_{n+1})},$$

in higher dimensions with at its 'bottom end', the crossed module,

 $$\frac{\mathcal{N}G_1}{d_0(\mathcal{N}G_2\cap D_2)} \to \mathcal{N}G_0$$ 

with $\partial$ induced from the boundary in the Moore complex.

The category of [[crossed complexes]] form a variety in the category of all [[hypercrossed complexes]]. Alternatively, groupoid T-complexes (the groupoid version of [[group T-complex]]) form
a variety in the category of all simplicial groups.

## References

Textbook treatment is in 

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_

* [[Tim Porter]], _[[timporter:crossed menagerie|Crossed Menagerie]]_ .

A survey of the use of crossed complexes is in 

* [[Ronnie Brown]], _Crossed complexes and homotopy groupoids as non commutative tools for higher dimensional local-to-global problems_,  to appear in Michiel Hazewinkel (ed.), Handbook of Algebra, volume 6, Elsevier, 2008/2009. ([arxiv:math.AT/0212274 v7](http://arxiv.org/abs/math.AT/0212274)).


The equivalence of [[strict omega-groupoid]]s and crossed complexes is discussed in 

* [[Ronnie Brown]], P. J. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_ , Cah. Top. G&#233;om. Diff. 22, 371-386, 1981. ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/x-comp.pdf)) 

Notice that this article says "$\infty$-groupoid" for _strict globular $\infty$-groupoid_ and "$\omega$-groupoid" for _strict cubical $\infty$-groupoid_ .


For the relation to [[group cohomology]] see

* [[Johannes Huebschmann]], _Crossed $n$-fold extensions and group cohomology_ ([web](http://dx.doi.org/10.1007/BF02566688))


[[!redirects crossed complexes]]
