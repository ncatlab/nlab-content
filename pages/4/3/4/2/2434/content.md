<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

***

[[!include supergeometry - contents]]


</div>


+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here is about the definition of $(2|1)$-dimensional [[super-cobordism]] categories where cobordisms are [[Euclidean supermanifold]]s, and about $the (2|1)$-dimensional [[FQFT]]s given by functors on these.

=--

Previous:

  * [[Axiomatic field theories and their motivation from topology]]

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]

  * [[bordism categories following Stolz-Teichner]]


#Contents#

* tic
{:toc}


#Idea#

Previously we had defined smooth categories of [[Riemannian cobordism]]s. Now we pass from [[Riemannian manifold]]s to [[Euclidean supermanifold]]s and define the correponding smooth [[cobordism category]]. Then we define $(d|\delta)$-dimensional Euclidean field theories to be smooth respentations of these categories.

As described at  [[(2,1)-dimensional Euclidean field theories and tmf]], the idea is that $(2|1)$-dimensional Euclidean field theories are a geometric model for [[tmf]] [[cohomology theory]]. While there is no complete proof of this so far, in the next and final session 

* [[modular forms from partition functions]]

it will be shows that the claim is true at least for the [[cohomology ring]] over the point: the [[partition function]] of a $(2|1)$-dimensional EFT is a modular form. Hence $(2|1)$-dimensional EFTs do yield the correct [[cohomology ring]] of [[tmf]] over the point.


#Details#

Let [[SDiff]] be the [[category]] of [[supermanifold]]s.

We will define a [[stack]]/[[fibered category]] on $SDiff$ called $E Bord_{2|1}$ whose morphisms are smooth families of (2|1)-dimensional [[super-cobordism]]s, and a [[stack]]/[[fibered category]] $sTV^{fam}$ of topological super vector bundles.


So recall

* [[supergeometry - contents|supergeometry]].

**question**: What is the right notion of Riemannian or Euclidean structure on [[super-cobordism]]s?

**strategy**: From the [[path integral]] perspective we need some structure on $\Sigma$ such that the "space" of maps $Maps(\Sigma,X)$ naturally carries some measure that allows to perform a [[path integral]].

This perspective suggests certain genralizations of the notion of [[Riemannian manifold]] to [[supermanifold]]s which may be a little different than what one might have thought of naively.

We want to define [[Euclidean supermanifold]]s as a genralization of [[Riemannian manifold]] with _flat_ Riemannian metric.

notice that there is a canonical bijection between

* flat [[Riemannian metric]]s on a $d$-dimensional [[manifold]] $X$

* a maximal [[atlas]] on $X$ consisting of charts such that all transition functions belong the the **Euclidean group** or **Galileo group** 

  $$
    Eucl(\mathbb{R}^d)
    :=
    \mathbb{R}^d \rtimes O(\mathbb{R}^d)
  $$

  (rigid translations and rotations)

In analogy to that we define:

Similarly a **Euclidean structure** on a $(d|\delta)$-dimensional [[supermanifold]] is defined using the Euclidean [[super Lie group]] given by the [[semidirect product]]

$$
  Eucl(\mathbb{R}^{d|\delta})
  :=
  \mathbb{R}^{d|\delta}
  \rtimes
  Spin(\mathbb{R}^d)
$$

where the [[Spin]] group acts on the translations in $\mathbb{R}^{d|\delta}$ in a way to be specified.


first recall the notion of

* [[complex supermanifold]]

**goal** replace the standard Euclidean group $(\mathbb{R}^d, Eucl(\mathbb{R}^d))$ by the [[super Euclidean group]]
$(X,G)$ where $X$ is a suitable [[supermanifold]]
and $G$ a suitable [[super Lie group]].

This leads to the notion of

* [[Euclidean supermanifold]].

The morphisms of the category $E Bord_{(2|1)}$ will be [[cobordism]]s that are [[Euclidean supermanifold]]s.

**goal** define the [[fibered category]]

$$
  \array{
    E Bord_{d|\delta}^{sfam}
    \\
    \downarrow
    \\
    cSDiff
  }
$$

where $cSDiff$ is the category of [[complex supermanifold]]s.

The objects of this fibered category are

$$
  \array{
    Y^{\pm} &\to& Y &\leftarrow& Y^c
    \\
    & \searrow & \downarrow & \swarrow
    \\
    && S
  }
$$

where $Y \to S$ is a family of [[Euclidean supermanifold]]s of dimension $(d|\delta)$.

For the non-super, non-family version of **Euclidean bordism** we require that the core $Y^c$ is totally geodesic in $Y$.

now for the superversion we require that there exist charts (in the open atlas) of $Y \to S$ covering all of $Y^c$ such that

$$
  \array{
    && S
    \\
    & \nearrow && \nwarrow
    \\
    Y \supset_{open} U &&\stackrel{\phi}{\to}&&
    V \subset S \times \mathbb{R}^{d|\delta}_{cs}
    \\
    \downarrow^{\supset} &&&& \downarrow^{\supset}
    \\
    Y^c \supset U \cap Y^c
    &&\stackrel{\simeq}{\to}&&
    V \cap S \times \mathbb{R}^{d-1|\delta}
    \subset S \times \mathbb{R}^{d-1|\delta}_{cs}
  }
$$

next, a **Euclidean superbordism** from $Y_0 \to S$ to $Y_1 \to S$ is a diagram

$$
  \array{
    Y_1 
     &\stackrel{i_1}{\to}& 
    \Sigma 
     &\stackrel{i_0}{\leftarrow}& Y_1
    \\
     & \searrow & \downarrow & \swarrow
    \\
    && S
  }
$$

where $i_0, i_1$ are morphisms (of families of $(X,G)$-spaces) satisfying the (+)-condition and the (c)-condition described at [[bordism categories following Stolz-Teichner]].

Now a morphism in $E Bord^{sfam}_{d|\delta}$ from $Y_0 \to S_0$ to $Y_1 \to S_1$ is a bordism fitting into a diagram

$$
  \array{
      \Sigma &\stackrel{i_1}{\leftarrow}&
      f^* Y_1 &\to& Y_1
     \\
     \uparrow^{i_0} &\searrow& \downarrow && \downarrow
     \\
     Y_1 &\to & S_0 &\stackrel{f}{\to}& S1
  }
$$

and we identify bordisms $\Sigma, \Sigma'$ if they are isometric -- namely isomorphic in the category of [[Euclidean supermanifold]]s --  "rel boundary".

**definition** A **$(d|\delta)$-dimensional Euclidean field theory** is a [[symmetric monoidal functor]]

$$
  E \in Fun_{csDiff}^\otimes(E Bord_{(d|\delta)}^{sfam},
  TV^{sfam})
$$

of [[symmetric monoidal category|symmetric monoidal]] [[fibered category|fibered cateories]] (i. [[symmetric monoidal functor]] as well as [[cartesian functor]] ) over the category $cSDiff$ of [[complex supermanifold]]s.

**Definition** (roughly) $TV^{sfam}$ is the category of families of topological vector spaces parameterized by [[complex supermanifold]]s.

Recall that the ordinary category $TV$ is the catgeory of complete [[Hausdorff space|Hausdorff]], locally convex [[topological vector space]].

define the [[projective tensor product]] of two such $V, W \in TV$. This is a certain completion of the algebraic tensor product $V \otimes_{alg} W$ with respect to the projective topology on $V \otimes_{alg} W$.

This will be the coarsest [[topology]] (the one with the least open sets) making the following maps $f'$

$$
  \array{
     V \otimes_{alg} W &\to& Z
     \\
     & \nearrow_{f'}
     \\
     V \times W
   }
$$

continuous. 

**Remark**

$$
  \array{
    C^\infty(M \times N)
    &\leftarrow&
    C^\infty(M) \otimes_{alg} C^\infty(N)
    \\
    & {}_{\simeq}\nwarrow & \downarrow^{\subset}
    \\
    && C^\infty(M) \otimes C^\infty(N)
  }
$$

**Definition** the objects of $TV^{sfam}$ are pairs $(S,V)$ for $S$ a [[supermanifold]] and $V$ is a [[sheaf]] of locally complex $\mathbb{Z}_2$-graded [[topological vector space]] with the structure of a sheaf of modules of the [[structure sheaf]] $O_S$.

**goal** define the [[partition function]] of of a $(2|1)$-dimensional Euclidean field theory.

**definition** Let $E$ be an EFT as above.

We may think of $\mathbb{R}_+ \times h$ (positive axis times upper half plane) as moduli space of Euclidean tori, where for $(\ell, \tau) \in \mathbb{R}_+ \times h$ we get a torus (regarded as a [[cobordism]]) denoted $T_{\ell,\tau}$. This is the torus given by the lattice spanned by $(1,0)$ and $\ell Re(\tau) + Im(\tau)$ in the upper half plane. Then for the ordinary EFT we would define

$$
  Z_E : \mathbb{R}_+ \times h \to \mathbb {C}
$$

  


$$
  (\ell,\tau) \mapsto E(T_{\ell,\tau})
$$

For the superversion we put

$$
  Z_{E} := Z_{E_{red}}
$$

where

$$
  \array{
    && E Bord_{2|1}^{sfam}
    \\
    & {}^{\rho}\nearrow
    &&
    \searrow^{E}
    \\
    E Bord_{2, Spin}^{fam}
    &\stackrel{E_{red}}{\to}&
    TV^{fam}
    &
     \hookrightarrow
    &
    TV^{sfam}
  }
$$

# Examples #

## explicit description of $E Bord_{1}^{fam}$ ##

See [[bordism categories following Stolz-Teichner]].

The category $E Bord_1^{fam}$ is generated from

*  the _family of right elbows__

   $$
   \array{
     1-E Bord_{\mathbb{R}_+}^{fam}(\emptyset, pt \coprod pt)
     & \ni&  R  & :=  \mathbb{R}_+ \times \mathbb{R}
     \\
     && \downarrow
     \\
     && S := \mathbb{R}_+
    }
   $$

* the point-family of the left elbox
  $$
    \array{
      L_0
      \\
      \downarrow
      \\
      S := pt
    }
  $$

* the family of intervals in $E Bord^{fam}_{\mathbb{R}^+}(pt,pt)$

  $$
    \array{
      I
      \\
      \downarrow
      \\
      \mathbb{R}_{\geq 0}
    }
  $$
  

Because:

$
  E \in Fun^{\otimes}_{Diff}(E Bord^{fam}, TV^{fam})$
$

is determined by 

$$
  E(pt) =: V \in TV
$$



$$
  E(L_0) =: \lambda : V \otimes V \to \mathbb{R}
$$

$$
  E(R) =:  \rho \in TV_{\mathbb{R}^+}(\mathbb{R}, V \otimes V) \simeq C^\infty(\mathbb{R}_+, V \otimes V)
$$

$$
  E(I) =: e^{-t H} \in C^\infty(\mathbb{R}_{\geq}, End(V))
$$

forms a _smooth_ semigroup under composition generated by 

$$
  H \in End(V)
$$

(the [[Hamiltonian operator]])

$$
  \array{
    V \otimes V &&\stackrel{\lambda}{\hookrightarrow}&&
    End(V)
    \\
    & {}_{\rho}\nwarrow && \nearrow_{e^{- t H}}
    \\
    && \mathbb{R}_+
  }
$$

so due to smoothness the data collapses to the infinitesimal data

$$
  (V, \lambda, H)
$$

**example -- ordinary quantum mechanics** Let $M$ be a [[Riemannian manifold]]. Then  set

* $H:= \Delta$ the corresponding [[Laplace operator]];

* $V := C^\infty(M) \subset L^2(M)$;

* $\lambda$ is the restriction of the $L^2(M)$ inner product to $V$

where $e^{-t H}$ is "trace class" in the non-standard sense described above in that it makes the above diagram commute.

So everything as known from standard [[quantum mechanics textbooks]], except that we don't use the full [[Hilbert space]] of states, but just the [[Frechet space]] of smooth functions.

## explicit description of $E Bord_{2}$ ##

The category $E Bord_{2}_{oriented}^{fam}$ has the following generators:

objects are generated from

* the **circle** $K_\ell := \mathbb{R}^2/\mathbb{Z}\cdot \ell$  of length $\ell \gt 0$ (with collars!! that's why it looks like a cylinder of circumference $\ell$)

  notice that we may think of $\ell $ as parameteriing translation by $\ell$ in $\mathbb{R}^2 \rtimes SO(2) = Eucl_{or}(\mathbb{R}^2)$

  and the circle with $(+)$/$(-)$-collars reversed

morphisms are generated from 

* **cylinders** $C_{\ell,\tau}$ which as a manifold is $\simeq \mathbb{R}^2/\mathbb{Z}\cdot \ell$ where $\tau$ parameterizes the embedding of the outgoing circle: the incoming circle is embedded in the canonical way (the identity map on the cylinder, really), while the outgoing circle is embedded by translating the cylinder by $\ell \cdot Re(\tau)$ upwards and rotated by $\ell \cdots Im(\tau)$. 

* **right elbows** which are the same as the cylinder, except that now the second circle is embedded after reflection so that it becomes an ingoing circle.

* the **thin left elbow** $L_\ell$, similar to the above, with arbitrary $\ell$ but $\tau = 0$

* the **torus** $T_\tau$ obtained from the cylinder by gluing incoming and outgoing

**notice** the **pair of pants** is not a morphism in the category at all! since, recall, we require all bordisms to be _flat_ and all boundaries to be _geodesics_ . There is no way to put such a flat metric on the trinion.

satisfying the relations

$$
  L_\ell \circ R_{\ell, \tau}
  =
  T_{\ell, \tau}
$$

as for the non-family version, but now also with the new relations

$$
  T_{\ell', \tau'} = T_{\ell, \tau}
$$

whenever $\ell' = \ell \cdot|c \tau + d|$ and $\tau' = \frac{a \tau + b }{c \tau + d}$

for $\left(\array{a & b \\ c & d }\right) \in SL_2(\mathbb{Z})$.

Notice that $SL_2(\mathbb{Z})$ is generated by

* translation $(\ell, \tau) \mapsto (\ell, \tau + 1)$

* S-matrix $(\ell, \tau) \mapsto (\ell \cdot |\tau|, - \frac{1}{\tau})$

and now there is **one more relation** 

$$
  T_{\ell, \tau}
  =
  T_{\ell |\tau|, - \frac{1}{\tau}}
$$

as usual write $q := e^{2 \pi  i \tau}$ which is on the pointed unit disk since $\tau$ is half plane since $\tau$ 

## explicit description of $E Bord_{2}^{fam}$ ##

thwe category $E Bord_{2, oriented}^{fam}$ is generated from

objects:

* $\array{K \\ \downarrow \\ S = \mathbb{R}_+}$ 

* morphisms 

  $$
    \array{
      L \\ \downarrow \\ \mathbb{R}_+
    }
  $$

  $$
    \array{
      R \\ \downarrow \\ \mathbb{R}_+ \times h/\mathbb{Z}
    }
  $$

  $$
    \array{
      C \\ \downarrow \\ \mathbb{R}_+ \times (h \cup \mathbb{R})/\mathbb{Z}
    }
  $$

subject to the relations

... as before (homework 3, problem 4).. and the furhter one:

for

$$
  \array{
    T  && \alpha^* T
    \\ 
    \downarrow && \downarrow
    \\ 
    \mathbb{R}_+ \times h
    &\stackrel{\alpha}{\leftarrow}&
    \mathbb{R}_+ \times h
    \\
    \\
    (\ell\cdot |\tau|, -\frac{1}{\tau})
    &\stackrel{}{\lt\leftarrow}&
    (\ell, \tau)
  }
$$

the relation is

$$
  \alpha^* T  = T
  \,.
$$