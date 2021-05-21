
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A _crossed complex_ (of [[groupoid]]s) is a nonabelian and [[horizontal categorification|many object]] generalization of a [[chain complex]] of [[abelian group]]s.

Crossed complexes are an equivalent way to encode the information contained in [[strict ∞-groupoids]]: the groups appearing in the crossed complex in degree $n \geq 2$ are the source-fibers of the collection of $n$-morphisms of the $\omega$-groupoid.

See also [[homotopy n-type]]. 

One way to think of a crossed complex is as a chain complex in which the bottom part is a crossed module and the rest is a chain complex of modules over the fundamental group of the crossed complex (that is its cokernel).  This is easy to think of in the case where there is a single object (*crossed complex of groups*), and it is a simple step to extend to the many object case.

Later on we will look in a bit more detail at the fundamental crossed complex of a filtered space, and that is a good example to keep in mind.  For simplicity assume we have a CW-complex, or similar space, together with a filtration by some nice subspaces.  We have the fundamental groupoid, $\Pi_1(X_1,X_0)$, of the '1-skeleton' based at the vertices. For any vertex $x$, we then have $\pi_2(X_2,X_1,x)$, the relative homotopy group of the 2-dimensional stuff relative to the 1-dimensional stuff, based at $x$.  Varying $x$ we get a family of groups which we think of as a groupoid having just vertex groups without any arrows joining distinct vertices. In the next dimension we have $\pi_3(X_3,X_2,x)$, which is the relative homotopy group taking account of the 3-cells modulo the 2-cells, (which is abelian), and so on. Change of base point gives an action of  $\Pi_1(X_1,X_0)$ on all of these. It was studying these groups , actions etc. that gave the abstract definition that follows.

## Definition

### As sequences of groups and groupoids {#SequencesOfGroups}

+-- {: .un_defn}
###### Definition

A **crossed complex** ("of groupoids") $C$ is 

* a [[groupoid]]  $C_1 \stackrel{\overset{\delta_t}{\to}}{\underset{\delta_s}
{\to}} C_0$

* together with a sequence of [[skeleton|skeletal]] groupoids $(C_k)_{k = 2}^\infty$ over $C_0$, i.e. of  bundles $C_k = \coprod_{x \in C_0} (C_k)_x$ of groups over $C_0$, [[abelian group|abelian]] for $k \geq 3$,  sitting in a diagram 

$$
 \begin{array}{c}
   \cdots &\to& C_3 &\stackrel{\delta}{\to}& C_2
   &\stackrel{\delta}{\to}&
   C_1 &
  \stackrel{\overset{\delta_t}{\to}}{\underset{\delta_s}{\to}} &
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
 \end{array}
$$

* together with an [[action]] of $C_1$ on $C_k$ for $k \geq 0$

such that

* the morphisms $\delta_k$ for $k \geq 2$ are morphisms of groupoids over $C_0$, compatible with the action by $C_1$

* $im(\delta_2) \subset C_1$ acts by conjugation on $C_2$ and trivially on $C_k$ for $k \geq 3$

* $\delta_{k-1} \circ \delta_k = 0$ for $k \geq 3$.

There is an obvious notion of [[morphism]]s $f : C \to D$ of crossed complexes, being sequences of maps $(f_k : C_k \to D_k)$ preserving all the above structure. The resulting [[category]] is often denoted $Crs$ or $CrsCpx$. 

=--


### From strict $\infty$-groupoids

While the above definition of a crossed complex may seem slightly 'baroque', it can naturally be understood as being precisely the data obtained from a [[globular set|globular]] [[strict ∞-groupoid]] by retaining for $k \geq 2$ precisely only those [[k-morphism]]s whose source is a an identity $k-1$-morphisms on an object.


+-- {: .un_defn}
###### Definition
**(crossed complex associated to a strict $\infty$-groupoid)**

For $\mathcal{G}$ a [[globular set|globular]] [[strict ∞-groupoid]]

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

the corresponding crossed complex $[\mathcal{G}]$ is defined as follows:

* the groupoid $[\mathcal{G}]_1 \stackrel{\to}{\to} [\mathcal{G}]_0$ 
  is just the groupoid 
    $\mathcal{G}_1 \stackrel{\to}{\to} \mathcal{G}_0$; 
  underlying $\mathcal{G}$ by forgetting all 
  [[k-morphism]]s for $k \geq 2$

* for $k \geq 2$ the bundle of groups $[\mathcal{G}]_k$ 
  is over
  $x \in \mathcal{G}_0$ the group of [[k-morphism]]s of $\mathcal{G}$
  whose source is the the identity on $x$:

  $$
    [\mathcal{G}]_k := \coprod_x s_k^{-1}(Id_x)
    \,,
  $$

  where the group operation is given by the horizontal composition of 
  [[k-morphism]]s (along objects). By the [[Eckmann-Hilton argument]] this
  is indeed an [[abelian group]] structure for $k \geq 3$.

* The [[action]] of $[\mathcal{G}]_1$ on $[\mathcal{G}]_k$ is given by [[whiskering]]/[[conjugation]] of [[k-morphism]]s by 1-morphisms in $\mathcal{G}$. 

* The boundary maps $\delta := t : [\mathcal{G}]_{k} \to [\mathcal{G}]_{k-1}$ are the restrictions of the target maps $t : \mathcal{G}_k \to \mathcal{G}_{k-1}$, sending a $k$-morphisms with source an identity on an object to its target $k-1$-morphism.


=--


Write $Str \infty Grpd$ for the 1-[[category]] of [[globular set|globular]] [[strict ∞-groupoids]]. The above construction defines an evident [[functor]]

$$
  [-] : Str \infty Grpd \to CrsCplx
  \,.
$$

+-- {: .un_prop}
###### Proposition

The functor

$$
 [-] : Str \infty Grpd \to CrsCplx
$$

is an [[equivalence of categories]].

=--


+-- {: .proof}
###### Proof

The idea of the proof is that a [[strict ∞-groupoid]] may completely be reconstructed from its objects, 1-morphisms and those $(k \geq 2)$-morphisms that start at an identity by using the action of the 1-morphisms on the higher morphisms induced by conjugation.

For instance a [[2-morphism]]

$$
  \array{
    & \nearrow  \searrow^{\mathrlap{f}}
    \\
    x &\Downarrow& y
    \\
    & \searrow \nearrow_{\mathllap{g}}
  }
$$

is, by the [[exchange law]], equal to the horizontal composite of the 2-morphism 


$$
  \array{
    & \nearrow  \searrow^{\mathrlap{f}}
    \\
    x &\Downarrow& y & \stackrel{f^{-1}}{\to} & x
    \\
    & \searrow \nearrow_{\mathllap{g}}
  }
$$

(whose source is the identity on $x$) with the 1-morphisms $f$.

A detailed proof is in 

* [[Ronnie Brown]], [[Philip Higgins]], _The equivalence of $\infty$-groupoids and crossed complexes_ , Cah. Top. G&#233;om. Diff. 22, 371-386, 1981. ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/x-comp.pdf)) 

Notice that this article says "$\infty$-groupoid" for _strict globular $\infty$-groupoid_ and "$\omega$-groupoid" for _strict cubical $\infty$-groupoid_ .


=--

This is a nonabelian and globular version of the [[Dold-Kan correspondence]].

### From chain complexes of modules

We describe a functorial construction of a crossed complex starting with a [[chain complex]] of [[modules over a groupoid]] $(A_n, \mathcal{H})$. As a special case it in particular gives an functor sending ordinary [[chain complex]]es of [[abelian group]]s into the category of [[crossed complex]]es, and hence into [[strict ∞-groupoid]]s. See also [[Nonabelian Algebraic Topology]]. 

Recall the definition of the [semidirect product groupoid](#AdjointModule)  $\mathcal{H} \ltimes A_n$.

+-- {: .un_def}
###### Definition
**(crossed complex from a chain complex)**

For $A$ a [[chain complex]] of [[modules over a groupoid]] $\mathcal{H}$, let $\Theta A \in Crs$ be the [[crossed complex]]

$$
  \Theta A := \kappa^* \Theta' A
  \,,
$$

where

$$
  \Theta' A :=
  \left[
    A_n 
      \stackrel{\partial_n}{\to}
    A_{n-1}
     \stackrel{}{\to}
     \cdots
     \stackrel{}{\to}
    A_{3}
    \stackrel{\partial_3}{\to}
    A_2
    \stackrel{(0,\partial_2)}{\to}
    \mathcal{H}\ltimes A_1
  \right]
$$

and where 

$$
  \kappa : P(A_0, \mathcal{H}) \to \mathcal{H} \ltimes A_0
$$

is the [canonical covering morphism](#AdjointModule) from above.

$$
  \array{
    \cdots \to & 
    (\Theta A)_3
    &\to&
    (\Theta A)_2
    &\to&
    (\Theta A)_1
    &\to&
    P(A_0, \mathcal{H})
    \\
    & \downarrow && \downarrow && \downarrow && \downarrow
    \\
    \cdots \to & 
    A_3
    &\stackrel{\partial_3}{\to}&
    A_2
    &\stackrel{(0,\partial_2)}{\to}&
    \mathcal{H} \ltimes A_1
    &\stackrel{(1, \partial_1)}{\to}&
    \mathcal{H} \ltimes A_0    
  }
  \,.
$$

Here $\mathcal{H} \ltimes A_1$ acts on $A_n$ for $n \geq 2$ via the projection $\mathcal{H} \ltimes A_1 \to \mathcal{H}$, i.e. $A_1$ acts trivially.
(...)

Finally set $\Theta(A)_0 := A_0$.

=--

We spell out what this boils down to explicitly.

**Explicit description**

Let $A_\bullet$ be a [[chain complex]] of [[modules over a groupoid|modules over the groupoid]] $\mathcal{H}$. Then the [[crossed complex]] $\Theta(A)$ is the following.

* Its set of objects is $\Theta(A)_0 = A_0$.

  Remember that $A_0$ itself is a module over $\matcal{H} = (\mathcal{H}_1 \stackrel{\to}{\to} \mathcal{H}_0)$, so that $A_0 = \corpdod_{p \in \mathcal{H}_0} (A_0)_p$.

* For $x \in (A_0)_p$ and $y \in (A_0)_q$ a morphism in $\Theta(A)_1$ from $x$ to $y$ is labeled by $h \in \mathcal{H}_1$ and $a \in (A_1)_q$

  $$
    x \stackrel{(h,a)}{\to} (y = \rho(h)(x) - \partial a)
    \,,
  $$

  where $\rho$ denotes the [[action]] of $\mathcal{H}$ on $A_0$.

  The composition law is given by

  $$
    \array{
       && y
       \\
       & {}^{\mathllap{(h_1, a_1)}}\nearrow && \searrow^{\mathrlap{(h_2,a_2)}}
       \\
       x &&\stackrel{(h_1 \circ h_2, \rho(h_2)(a_1) + a_2)}{\to}&& z
    }
    \,.
  $$

* For $k \geq 2$ the family of groups $\Theta(A)_k$ is over $x \in (A_0)_p$ the group $(A_k)_q$

  $$
    \Theta(A)_{k \geq 2} = \coprod_{p \in \mathcal{H}_0} \coprod_{x\in (A_0)_q} (A_k)q
  $$

* The boundary maps and actions are the obvious ones...


+-- {: .un_example}
###### Example
**(ordinary abelian chain complex as crossed complex)**


Let $C_\bullet$ be an ordinary [[chain complex]] of abelian groups, i.e. a chain complex of [[module over a groupoid|modules over the trivial groupoid]].

Then $(\Theta C)_1$ is the groupoid with objects $C_0$ and morphisms $\{x \stackrel{b}{\to} (x + \partial b)\}$. And for $n \geq 2$ we have that $(\Theta C)_n$ is $\coprod_{x \in C_0} C_n$.


=--





+-- {: .un_prop}
###### Proposition

These form a pair of [[adjoint functor]]s

$$
  (\nabla \dashv \Theta)
  : 
  Chn
  \stackrel{\overset{\nabla}{\leftarrow}}{\underset{\Theta}{\to}}
  Crs
$$

where...

=--

This is proposition 7.4.29.

(...)


## Examples

### In low degree

Say that a crossed complex $C$ is $n$-[[truncated]] if $C_k$ is trivial for $k \gt k$. 

Then

* 0-[[truncated]] crossed complexes are canonically equivalent to [[set]]s, equivalent to [[homotopy n-type|homotopy 0-type]]s.

* 1-[[truncated]] crossed complexes are canonically equivalently to [[groupoid]]s, equivalent to [[homotopy n-type|homotopy 1-type]]s).

* 2-[[truncated]] crossed complexes are equivalent to strict [[2-groupoid]]s equivalent to [[homotopy n-type|homotopy 2-type]]s.

  2-[[truncated]] and 0-[[connected]] crossed complex, i.e. a 2-truncated one for which $C_0 = *$ is the point is the same as a [[crossed module]] of groups. The equivalence of these to [[strict 2-group]]s is due to

  R. Brown and C.B. Spencer, _G-groupoids, crossed modules and the fundamental groupoid of a  topological group_, Proc. Kon. Ned. Akad. v. Wet, 79, (1976), 296 &#8211; 302.)

A discussion of the kind of homotopy types generally modelled by crossed complexes, namely a _linear_ model is in [[homotopy n-type]]. 

### Abelian chain complexes

The notion of crossed complex generalizes the notion of [[chain complex]] of [[abelian group]]s. Clearly in degree $k \geq 3$ a crossed complex with $C_0 = *$ _is_ a chain complex of abelian groups. To regard the first 2 degrees $A_1 \stackrel{\delta}{\to} A_0$ of a chain complex of abelian groups as a crossed module, form the groupoid

$$
  A_0 \times A_1 \stackrel{\overset{p_1 + \delta}{\to}}{\underset{p_1}{\to}}
  A_0
$$

and take the action of this groupoid on all $C_k$ to be trivial. This yields a functor

$$
  \theta : ChainCplx(Ab) \to CrsCpl
$$

that embeds chain complexes of abelian groups into crossed complexes. 

### Complex of modules over a groupoid

The embedding of chain complexes of abelian groups into crossed complexes generalizes to an embedding of chain complexs of [[modules over a groupoid]]

$$
  \theta : ChainCplx(GrpdMod) \to CrsCplx
  \,.
$$

For details see _[[Nonabelian Algebraic Topology]]_, [section 7.4.v](#http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#CrsFromCh).


### Fundamental crossed complex

If $X_*$ is a [[filtered space]], there is a crossed complex $\Pi X_*$ -- the [fundamental crossed complex](http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#FundamentalCrossedComplex) which corresponds to a (filtered and) [[strict ∞-groupoid]] version of the [[fundamental ∞-groupoid]] of $X$. In degree 1 it is the subgroupoid $\Pi_1(X_1,X_0)$ of the [[fundamental groupoid]] $\Pi_1(X_1)$ of $X_1$ on objects in $X_0$. 
In degree $n \gt 1$ it is the family of [[relative homotopy group]]s $\{\pi_n(X_n,X_{n-1},p) : p\in X_0\}$.  

This gives a functor $\Pi$ from filtered spaces to crossed complexes, which may be used to construct the generalisation of the [[Dold-Kan correspondence]], which in this case goes between crossed complexes and [[simplicial T-complex]]es.  

### Fundamental crossed complex of the $n$-simplex

An important special case of the above is when the filtered space is a [[CW-complex]] and the filtration is by skeleta.  Particularly useful instances of this are the $n$-cubes and $n$-simplices, with their CW-filtration.  We obtain $\Pi(I^n)$ and $\Pi(\Delta^n)$.  These are used to define cubical and simplicial [[nerve]]s of a crossed complex and these in turn define the [[Dold-Kan correspondence]] mentioned above.  For instance if $C$ is a crossed complex, then its simplicial nerve is the simplicial set with $Ner(C)_n = 
Crs(\Pi(\Delta^n),C)$ in dimension $n$.


+-- {: .un_example}
###### Example
**(fundamental crossed complex of the $n$-simplex)**

The topological $n$-[[simplex]] $\Delta^n$ is canonically a [[filtered space]] with $(\Delta^n)_k$ being the union of its $k$-faces.

Then we have that $\Pi_1((\Delta^n)_1, (\Delta^n)_0)$ is the groupoid whose objects are the $n+1$ vertices of $\Delta^n$ and which has precisely one morphism $x_i \to x_j$ for each ordered pair $x_i,x_j \in (\Delta^n)_0$
(all of them being [[isomorphism]]s)

$$
  \Pi_1((\Delta^2)_1,(\Delta^2)_0) = 
  \left\{
     \array{
     && x_1
     \\
     & \nearrow\swarrow && \searrow \nwarrow
     \\
    x_0 &&\stackrel{\leftarrow}{\to}&& x_2
    }
  \right\}
  \,.
$$

At any $x_i$ the relative homotopy group $\pi_2((\Delta^n)_2,(\Delta^n)_1, x_i)$ is a group on the set of 2-faces that have $x_i$ as a 0-face: there is a unique homotopy class of disks in $\Delta^n$ that sits in the 2-faces $(\Delta^n)_2$, whose base point is at $x_j$ and whose boundary runs along the boundary of a given 2-face of $\Delta^n$.

So (using the equivalence of crossed complexes with strict $\omega$-groupoids) for instance $\Pi \Delta^2$ is generated from $\Pi_1((\Delta^2)_1,(\Delta^2)_0)$ as above and a 2-cell

$$
  \array{
     && x_1
     \\
     & \swarrow &\Downarrow& \nwarrow
     \\
    x_0 &&\to&& x_2
    }
$$

under whiskering and composition. For instance whiskering this with $x_1 \to x_2$ yields the 2-morphism

$$
  \array{
     && x_1
     \\
     & \swarrow &\swArrow& \searrow
     \\
    x_0 &&\to&& x_2
    }
  \,.
$$

One sees that $\Pi \Delta^2$ is the strict groupoidification of the second [[oriental]].

Generally, $\Pi \Delta^n$ is the $n$-groupoid freely generated from $k$-morphisms for each $k$-face of $\Delta^n$.

=--




## Crossed complexes as Moore complexes

Crossed complexes (of groups) correspond to [[group T-complex|group T-complexes]]. Any group $T$-complex is a simplicial group and in the entry for them it is mentioned that a simplicial group has a group $T$-complex structure if and only if $\mathcal{N}G\cap D$ is the trivial graded subgroup, where 
$D = (D_n)_{n\geq 1}$ is the graded subgroup of $G$ generated by the degenerate elements. If $G$ is such a group $T$-complex then its [[Moore complex]] has a natural structure of a crossed complex. In general the obstruction to a given simplicial group to have  Moore complex which is a crossed complex is exactly that graded subgroup, $\mathcal{N}G\cap D$. (The [[Whitehead product|Whitehead products]] for $G$ live in this graded subgroup, so this provides one way of showing that the homotopy types representable by crossed complexes have trivial  Whitehead products.)

Conversely, for any crossed complex, $C$, there is a simplicial group, $K(C)$, constructed using an analogue of the inverse in the [[Dold-Kan correspondence]], which is a group $T$-complex and whose Moore complex is isomorphic to $C$.

The generalisation to general crossed complexes (of groupoids) and simplicially enriched groupoids
is quite easy to do. We will usually state results below for the group case, leaving the general case to the 'reader'.


## From simplicial group(oid)s to crossed complexes

It is fairly clear that crossed complexes / group(oid) $T$-complexes correspond to [[simplicial group]](oid)s in which certain  equations hold.  It therefore is reasonable that they are equivalent to a variety / [[reflective subcategory]] in the category, $SSet Grpd$, of simplicially enriched groupoids.  (The discussion in the entry on [[group T-complex]] is relevant here.)

There is a functor $C(-)$ from simplicial groups to crossed complexes given by 

$${C}(G)_{n+1} = \frac{\mathcal{N}G_n}{(\mathcal{N}G_n\cap D_n)d_0(\mathcal{N}G_{n+1}\cap D_{n+1})},$$

in higher dimensions with at its 'bottom end', the crossed module,

 $$\frac{\mathcal{N}G_1}{d_0(\mathcal{N}G_2\cap D_2)} \to \mathcal{N}G_0$$ 

with $\partial$ induced from the boundary in the Moore complex.

The category of [[crossed complexes]] form a variety in the category of all [[hypercrossed complexes]]. Alternatively, groupoid T-complexes (the groupoid version of [[group T-complex]]) form
a variety in the category of all simplicial groups.


## Related concepts

* [[group]]

* [[2-group]], [[crossed module]], [[differential crossed module]]

* [[3-group]], [[2-crossed module]] / [[crossed square]], [[differential 2-crossed module]]

* [[n-group]]

* [[∞-group]], [[simplicial group]], **crossed complex**, [[hypercrossed complex]]

* [[model structure on crossed complexes]]


## References

Crossed complexes were defined by Blakers in 1948 (following a suggestion of [[Samuel Eilenberg]]) and developed by Whitehead in 1949 and 1950 (but these authors used different terminology). They were applied by [[Johannes Huebschmann]] to [[group cohomology]] in 1980. They were further developed in  series of articles by Ronnie Brown and collaborators in the context of [[nonabelian algebraic topology]], and partly because they were found equivalent to a form of (strict) cubical $\omega$-groupoid with _connections_. This equivalence enabled a number of new results, including van Kampen type theorems and monoidal closed structures for crossed complexes. 


Textbook treatment is in 

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_

* [[Tim Porter]], _[[timporter:crossed menagerie|Crossed Menagerie]]_ .

A survey of the use of crossed complexes is in 

* [[Ronnie Brown]], _Crossed complexes and homotopy groupoids as non commutative tools for higher dimensional local-to-global problems_,  to appear in Michiel Hazewinkel (ed.), Handbook of Algebra, volume 6, Elsevier, 2008/2009. ([arxiv:math.AT/0212274 v7](http://arxiv.org/abs/math.AT/0212274)).


The equivalence of [[strict omega-groupoid]]s and crossed complexes is discussed in 

* [[Ronnie Brown]], [[Philip Higgins]], _The equivalence of $\infty$-groupoids and crossed complexes_ , Cah. Top. G&#233;om. Diff. 22, 371-386, 1981. ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/x-comp.pdf)) 

Notice that this article says "$\infty$-groupoid" for _strict globular $\infty$-groupoid_ and "$\omega$-groupoid" for _strict cubical $\infty$-groupoid_ .


For the relation to [[group cohomology]] see

* [[Johannes Huebschmann]], _Crossed $n$-fold extensions and group cohomology_ ([web](http://dx.doi.org/10.1007/BF02566688))


[[!redirects crossed complexes]]

[[!redirects crossed complex of groupoids]]
[[!redirects crossed complexes of groupoids]]
