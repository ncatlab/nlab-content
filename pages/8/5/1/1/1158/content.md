
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 


## Idea
 {#Idea}

_Deligne cohomology_ -- or _[[Pierre Deligne|Deligne]]-[[Alexander Beilinson|Beilinson]] cohomology_ -- is an [[abelian sheaf cohomology]] that models [[ordinary differential cohomology]].

The _Deligne complex_ is like a truncated [[de Rham complex]] but, crucially, with the sheaf of 0-forms -- the [[structure sheaf]] $\mathcal{O}$ - replaced by the [[multiplicative group]] $\mathcal{O}^\times$ under the [[exponential map]]

$$
  \left[
     \mathcal{O}^\times
     \stackrel{d log}{\longrightarrow}
     \Omega^1
     \stackrel{d}{\longrightarrow}
     \Omega^2
     \stackrel{d}{\longrightarrow}
     \cdots
     \stackrel{d}{\longrightarrow}
     \Omega^n
  \right]
  \,.
$$

Deligne cohomology $H^{n+1}_{conn}(X, \mathbb{Z})$ in degree $(n+1)$ is the [[abelian sheaf cohomology]] with [[coefficients]] in this [[chain complex]] of [[sheaves of abelian groups]] ("[[hypercohomology]]"). 

This was introduced in ([Deligne 71](#Deligne71)) in the context of [[analytic geometry]] (hence using [[holomorphic differential forms]]) as a [[Hodge filtration|Hodge-filtered]] version of [[singular cohomology]], designed to be a target for the [[Beilinson regulator]] from [[motivic cohomology]]. But the form of the definition applies more generally, in particular also in smooth [[differential geometry]], a fact amplified and popularized in ([Brylinski 93](#Brylinski93)).

In smooth [[differential geometry]] the typical minor variant has the sheaf $\underline{U}(1) = C^\infty(-,U(1))$ of [[circle group]]-valued [[smooth functions]] in degree $n$:

$$
  \left[
     C^\infty(-,U(1))
     \stackrel{d log}{\longrightarrow}
     \Omega^1
     \stackrel{d}{\longrightarrow}
     \Omega^2
     \stackrel{d}{\longrightarrow}
     \cdots
     \stackrel{d}{\longrightarrow}
     \Omega^n
  \right]
  \,.
$$

Given any [[manifold]] $X$, then the resulting complex of abelian groups is, under the [[Dold-Kan correspondence]], the [[n-groupoid]] of [[circle n-bundles with connection]] whose underlying [[circle n-group|circle (n-1)-group]]-[[principal infinity-bundle]] is trivialized. Passing to the [[abelian sheaf cohomology]] implicitly corresponds to considering the [[infinity-stackification]] of this $n$-groupoid valued presheaf, and in this way Deligne cohomology computes equivalence classes of [[circle n-bundles with connection]]. Another way to say this is that under the [[Dold-Kan correspondence]] and [[infinity-stackification]], the above Deligne complex defines a [[smooth infinity-stack]] $\mathbf{B}^n U(1)_{conn}$ which is the [[moduli infinity-stack]] for [[circle n-bundles with connection]], and Deligne cohomology computes the [[homotopy classes]] of maps (of [[infinity-stacks]]) into this ([FSS 10](#FSS10))

$$
  H^{n+1}_{conn}(X,\mathbb{Z})
  \simeq
  \pi_0(X \to \mathbf{B}^n U(1)_{conn})
  \,.
$$

In this way Deligne cohomology, or rather the collection of Deligne [[cocycles]] with [[coefficients]] in the Deligne complex that defines it, is considerably richer than other models for [[ordinary differential cohomology]] such as [[Cheeger-Simons differential characters]], which see only the [[cohomology group]], but not the full [[moduli infinity-stack|moduli n-stack]].

Explicitly, computing the [[abelian sheaf cohomology]] with coefficients in the [[Deligne complex]] via [[Cech cohomology]] gives that a [[cocycle]] $\overline{A}$ on some [[space]] $X$ is represented with respect to a suitable [[covering]] $\{U_i \to X\}$ by a collection of [[differential forms]] and functions

$$
  \overline{A}
  = 
  \left\{
     A_{i_0, \cdots, i_k}
     \in \Omega^{n-k}(U_{i_0, \cdots i_k})
  \right\}_{k = 0}^{n}
  \cup
  \{
     g_{i_0, \cdots, i_n} \in \mathcal{O}^\times(U_{i_0, \cdots, i_{n+1}})
  \}
$$

such that the failure of the $(n-k+1)$-forms to glue on $(k+1)$-fold intersections of charts is given by the de Rham differential of the $(n-k)$-forms

$$
  \sum_{j = 0}^k
  (-1)^j
  A_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_{k+1}}
  =
  d_{dR} A_{i_0, \cdots, i_{k+1}}
  \,.
$$


This evidently generalizes the familiar Cech cocycle data for traditional [[line bundles with connection]].

As the notation indicates, Deligne cohomology is a [[differential cohomology]] refinement of [[ordinary cohomology]] with [[integer]] [[coefficients]], exhibited by a canonical forgetful map

$$
  \array{
    H^{n+1}_{conn}(X,\mathbb{Z})
    \\
    & \searrow
    \\
    && H^{n+1}(X,\mathbb{Z})   
  }
$$

which is induced by the evident morphism of [[chain complexes]]. This is one map in an exact [[differential hexagon]] which exhibits Deligne cohomology as the differential refinement of ordinary integral cohomology by closed [[curvature]] [[differential form]] data.

$$
  \array{
    0 & && && && & 0
    \\
    & \searrow && && &&  \nearrow 
    \\
    && \Omega^{n}(X)/\Omega^n(X)_{\mathbb{Z}} && \stackrel{\mathbf{d}}{\longrightarrow} &&  \Omega^{n+1}_{cl}(X)
    \\
    & \nearrow && \searrow^{\mathrlap{a}} && \nearrow && \searrow
    \\
    H^{n}(X, \mathbb{R})
    && &&
    H^{n+1}_{conn}(X,\mathbb{Z})
    && &&
    H^{n+1}(X,\mathbb{R})
    \\
    & \searrow && \nearrow && \searrow && \nearrow
    \\
    && H^{n}(X,U(1)) && \underset{}{\longrightarrow} && H^{n+1}(X,\mathbb{Z})
    \\
    & \nearrow && && &&  \searrow 
    \\
    0 & && && && & 0
    \\
    \\
    &&  connection\;forms\;on\;trivial\;bundles && \stackrel{de\;Rham\;differential}{\longrightarrow} && curvature\;forms
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{curvature}} && \searrow^{\mathrlap{de\;Rham\;theorem}}
    \\
    flat\;differential\;forms  && && geometric\;bundles\;with \;connection && && rationalized\;bundle
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{topol.\;class}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && geometric\;bundles\;with\;flat\;connection && \underset{comparison/regulator\;map}{\longrightarrow} && shape\;of\;bundle
  }
$$




## Definition

+-- {: .num_defn}
###### Definition

For $k \in \mathbb{N}$
write $\Omega^k(-) : U \mapsto \Omega^k(U)$ for the [[sheaf]] of smooth differential $k$-forms on $X$
and $C^\infty(-,V)$ for the sheaf of smooth $V$-valued functions on  $X$. 

The degree $(n+1)$ **Deligne complex** is the complex of sheaves

$$
  \mathbb{Z}(n+1)_D^\infty
  \;
    :=
  \;
  \left(
  \cdots \to 0 \to C^\infty(-,\mathbb{Z}) \hookrightarrow
   C^\infty(-,\mathbb{R}) \stackrel{d }{\to}
    \Omega^1(-) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(-)
  \right)
  \,.
$$

=--


Often it is useful to consider the [[quasi-isomorphism|quasi-isomorphic]] complex

$$
  \bar \mathbf{B}^n U(1)
  \;\;
  :=
  \;\;
  \left(
  \cdots 0 \to   C^\infty(-,U(1)) \stackrel{d log}{\to}
    \Omega^1(-) \stackrel{d}{\to} \cdots \stackrel{d}{\to}
    \Omega^n(-)
  \right)
$$

Here $C^\infty(-,U(1)) \stackrel{d log}{\to} \Omega^1(-)$ 
is the 
morphism of sheaves induced by regarding a $U(1) \simeq \mathbb{R}/\mathbb{Z}$-valued function locally
as a $\mathbb{R}$-valued function and applying the deRham differential $d$ to that.

The obvious morphism of complexes

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d log}{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow
    &&
    \downarrow^{(-)/\mathbb{Z}}
    &&
    \downarrow^{Id}
    &&
    &&
    \downarrow^{Id}
    \\
    0 
    &\to&
    C^\infty(-,U(1)) 
      &\stackrel{d log}{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
  }
$$

clearly induces isomorphism on [[homology]] groups: the homology in degree $n$ is locally constant $\mathbb{R}$-valued functions modulo locally constant $\mathbb{Z}$-valued functions in the first case and constant $U(1)$-valued functions in the second case, which is the same.

+-- {: .num_defn}
###### Definition

**Deligne cohomology** in degree $n+1$ of $X$ is the 
[[cohomology]] (which is [[abelian sheaf cohomology]] in this case) with coefficients in $\bar \mathbf{B}^n U(1)$.

=--

$$
  H(X, \mathbb{Z}(n+1)_D^\infty)
  \simeq 
  H(X, \bar \mathbf{B}^n U(1))
  \,.
$$

Here the notation on the right is motivated from the discussion at the end of [[motivation for sheaves, cohomology and higher stacks]].


## Properties

### Characteristic classes of Deligne cocycles 

There are two natural morphisms of abelian [[cohomology group]]s out of Deligne cohomology:

* the map to the underlying non-differential cocycle, the class of the underlying [[principal infinity-bundle]]:

 $$
  cl
  :
  H(X,\bar \mathbf{B}^n U(1))
  \to 
  H(X,\mathbf{B}^n U(1))
  \simeq
  H(X, \mathbf{B}^{n+1} \mathbb{Z})
  \simeq
  H^{n+1}(X,\mathbb{Z})
 $$

* the map to the curvature characteristic class

$$
  [F]
  :
  H(X,\bar \mathbf{B}^n U(1))
  \to 
  H_{dR}^{n+1}(X)
  \,.
$$

These are induced from the canonical morphisms of coefficient objects

$$
  \bar \mathbf{B}^n U(1) \simeq
  \mathbb{Z}(n+1)_D^\infty
  \to 
  \mathbf{B}^{n+1} \mathbb{Z}
$$

given by

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d }{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow^{Id}
    &&
    \downarrow^{0}
    &&
    \downarrow^{0}
    &&
    &&
    \downarrow^{0}
    \\
    C^\infty(-, \mathbb{Z})
    &\to&
    0 
      &\to&
     0
     &\to& 
       \cdots 
     &\to&
     0  }
$$

and

$$
  \bar \mathbf{B}^n U(1) \simeq
  \mathbb{Z}(n+1)_D^\infty
  \to 
  (\Omega^0(-)
   \stackrel{d}{\to}
   \Omega^1(-)
   \stackrel{d}{\to}
   \cdots
   \stackrel{d}{\to}
   \Omega^{n+1}(-)
  )
$$

given by

$$
  \array{
    C^\infty(-,\mathbb{Z})    
    &\hookrightarrow&
    C^\infty(-,\mathbb{R}) 
      &\stackrel{d }{\to}&
     \Omega^1(-) 
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^n(-)
    \\
    \downarrow^{0}
    &&
    \downarrow^d
    &&
    \downarrow^d
    &&
    &&
    \downarrow^d
    \\
    C^\infty(-,\mathbb{R}) 
     &\stackrel{d}{\to}&
      \Omega^1(-)
     &\stackrel{d}{\to}& 
      \Omega^2(-)
     &\stackrel{d}{\to}& 
       \cdots 
     &\stackrel{d}{\to}&
     \Omega^{n+1}(-)
}
$$

+-- {: .num_theorem }
###### Theorem

These two morphisms exhibit Deligne cohomology as a refinement in [[differential cohomology]] of ordinary (i.e. integral [[Eilenberg-MacLane spectrum|Eilenberg-MacLane]]) [[cohomology]], in that the diagram

$$
  \array{
    H(X,\bar \mathbf{B}^\bullet U(1))
    &\stackrel{[F]}{\to}&
    H^{\bullet+1}_{dR}(X)
    \\
    \downarrow^{cl} && \downarrow
    \\
    H^{\bullet+1}(X,\mathbb{Z})
    &\to&
    H^{\bullet + 1}(X,\mathbb{R})
  }
$$

is the cohomology of a homotopy pullback diagram, i.e. satisfies the axioms described at [[differential cohomology]].

=--


### Interpretation in terms of higher parallel transport

There is a natural way to understand the Deligne complex of sheaves as a sheaf which assigns to each patch the Lie $n$-groupoid of smooth [[higher parallel transport]] [[n-functor]]s. This perspective is helpful for understanding how Deligne cohomology relates to the bigger picture of [[differential cohomology]].

We start by discussing this in low degree.

There is [[path groupoid]] $P_1(X)$ whose smooth 
space of objects is $X$ and whose smooth space of morphisms is
a space of classes of smooth paths in $X$. 
Every smooth 1-form $A \in \Omega^1(X)$ induces 
a smooth [[functor]] $tra_A : P_1(X) \to \mathbf{B}U(1)$
from $P_1(X)$ to to the smooth [[groupoid]] $\mathbf{B} U(1)$
with one object and $U(1)$ as its smooth space of morphisms
by sending each path $\gamma : [0,1] \to X$
to $\exp (2 \pi i\int_0^1 \gamma^* A)$. This map 
from 1-forms to smooth functors turns out to be bijective:
every smooth functor of this form uniquely arises this way.
Similarly, one finds that smooth [[natural transformation]]
$\eta_f : tra_A \to tra_{A'}$ between two such functors
is in components precisely a 
smooth function $f : X \to U(1)$ such that $A' = A + d log f$.

Since the analogous statements are true for every open subset 
$U \subset X$ this defines a [[sheaf]] of [[Lie groupoid]]s 
$$
  Funct^\infty(P_1(-), \mathbf{B}U(1)) : Op(X)^{op} \to LieGrpd
  \,.
$$
By the [[Dold-Kan correspondence]] this sheaf of groupoids
corresponds to a sheaf of complexes of groups. This complex
of sheaves is nothing but the degree 2 Deligne complex

$$
  Funct^\infty(\Pi_1(-), \mathbf{B}U(1)) \simeq \mathbb{Z}(2)^\infty_D
  \,.
$$
 
This way Deligne cohomology is realized as computing the
[[(infinity,1)-sheafification|stackification]] of the pre-stack
$Funct^\infty(P_1(-), \mathbf{B}(1))$ of smooth $U(1)$-valued 
parallel transport functors.

The identification generalizes: for all $n$ there is a [[path n-groupoid]] $P_n(X)$ whose $k$-morphisms are 
$k$-dimensional smooth paths in $X$. Smooth $n$-functors
$tra_C : _n(X) \to \mathbf{B}^n U(1)$ are canonically identified
with smooth $n$-forms $C \in \Omega^n(X)$ and 
under the [[Dold-Kan correspondence]] the Deligne-complex in degree
$n+1$ is identified with the sheaf of $n$-groupoids of such smooth 
$n$-functors
$$
  n Funct^\infty(P_n(-), \mathbf{B}^n)
  \simeq
  \mathbb{Z}(n+1)^\infty_D
  \,.
$$

See

* John Baez, Urs Schreiber, _Higher Gauge Theory_ ([arXiv](http://arxiv.org/abs/math/0511710))

The full proof for $n=1$ this is in

* Urs Schreiber, Konrad Waldorf, _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452));

for $n=2$ in 

* Urs Schreiber, Konrad Waldorf, _Smooth functors versus differential forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

For more on this see [[infinity-Chern-Weil theory introduction]].

For higher $n$ there is as yet no detailed proof in the literature, but the
low dimensional proofs have obvious generalizations.


### Cup product

See [[Beilinson-Deligne cup-product]].

### Moduli and deformation theory

[[!include moduli of higher lines -- table]]

### GAGA
 {#GAGA}

The Deligne complex is naturally defined in smooth [[differential geometry]] as well as in [[complex analytic geometry]] as well as in [[algebraic geometry]] over the complex numbers. In the spirit of [[GAGA]] it is of interest to know how Deligne cohomology in these different settings relates.

One useful statement is: given an [[smooth scheme|smooth]] [[algebraic variety]] over the [[complex numbers]], then a sufficient condition for a complex-analytic Deligne cocycle over its [[analytification]] to lift to an algebraic Deligne cocycle is that its [[curvature form]] is an [[Kähler form|algebraic form]] ([Esnault 89, corollary 1.3](#Esnault89)). 


## Examples 

As described in some detail at [[electromagnetic field]] in abelian higher [[gauge theory|gauge theories]] the background field naturally arises as a [[Čech cohomology|Čech]]--Deligne cocycle, i.e. a [[Čech cohomology|Čech cocycle]] representative with values in the Deligne complex.

* Degree 2 Deligne cohomology classifies $U(1)$-[[principal bundle]]s [[connection on a bundle|with connection]]. The Deligne complex $\bar \mathbf{B}U(1)$ in this case coincides with the [[groupoid of Lie-algebra valued forms]] for the Lie algebra of $U(1)$.

  * In physics the [[electromagnetic field]] is modeled by a degree 2 Deligne cocycle. See there for a derivation of [[Čech cohomology|Čech]]--Deligne cohomology from physical input.

* Degree 3 Deligne cohomology classifies [[bundle gerbe]]s with connection.

  * In [[electromagnetism]], degree 3 Deligne cocycles (with compact support, possibly) model [[magnetic charge]]. In formal high energy physics the [[Kalb-Ramond field]] is modeled by a Deligne 3-cocycle.

* Degree 4 Deligne cohomology classifies [[bundle 2-gerbe]]s with connection. In particular Chern-Simons bundle 2-gerbes whose degree 4 curvature characteristic class is a multiple of the Pontryagin 4-form on some $SO(n)$-[[principal bundle]]. 

  * In formal high energy physics degree 4 Deligne classes model the [[supergravity C-field]].


## Related concepts

* [[intermediate Jacobian]] ([[self-dual higher gauge theory]])

* [[Abel-Jacobi map]]

* [[Beilinson regulator]]

* [[circle n-bundle with connection]]

* [differential cohomology diagram -- Examples -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)

## References
 {#References}

Deligne cohomology was introduced in [[complex analytic geometry]] (by a [[chain complex]] of [[holomorphic differential forms]]) in 

* {#Deligne71} [[Pierre Deligne]], _Th&#233;orie de Hodge II_ , IHES Pub. Math. (1971), no. 40, 5&#8211;57 ([pdf](http://www.math.jussieu.fr/~ai/d/Theory%20of%20Hodge%202.pdf))

with applications to [[Hodge theory]] and [[intermediate Jacobians]]. The same definition appears in 

* [[Barry Mazur]], [[William Messing]], _Universal extensions and one-dimensional crystalline cohomology_, Springer lecture notes 370, 1974

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], section III.1 of _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)

under the name "multiplicative de Rham complex" (and in the context of studying its [[deformation theory]] by [[Artin-Mazur formal groups]]). The theory was further developed in

* {#Beilinson85} [[Alexander Beilinson]] _[[Higher regulators and values of L-functions]]_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

with the application to [[Beilinson regulators]]. Later the evident version of the Deligne complex in [[differential geometry]] over [[smooth manifolds]] gained more attention and is still referred to as "Deligne cohomology".

Surveys and introductions in the context of [[differential geometry]] include

* {#Brylinski93} [[Jean-Luc Brylinski]], section 5 of _Loop Spaces, Characteristic Classes and geometric Quantization_, Birkh&#228;user 1993

* {#Bunke12} [[Ulrich Bunke]], section 3 of _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

Review with more emphasis on [[complex analytic geometry]] and the theory of ([Beilinson 85](#Beilinson85)) with more details spelled out is in

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

* {#Esnault89} [[Hélène Esnault]], _On the Loday-symbol in the Deligne-Beilinson cohomology_, K-theory 3, 1-28, 1989 ([pdf](http://www.mi.fu-berlin.de/users/esnault/preprints/helene/16-loday-symbol.pdf))

See also



* {#PetersSteenbrink08} [[Chris Peters]], [[Jozef Steenbrink]], section 7.2 of _[[Mixed Hodge Structures]]_, Ergebisse der Mathematik (2008) ([pdf](http://www.arithgeo.ethz.ch/alpbach2012/Peters_Steenbrinck))

* {#Voisin02} [[Claire Voisin]], section 12 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

Discussion of Deligne cohomology in terms of [[simplicial presheaves]] and [[higher stacks]] includes

* {#FSS10} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_, Journal of Geometry and Physics, Volume 74, 2013, Pages 130&#8211;163 ([arXiv:1207.5449](http://arxiv.org/abs/1207.5449))

* [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_, [arXiv:1212.2173](http://arxiv.org/abs/1212.2173).

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _A higher stacky perspective on Chern-Simons theory_, in Damien Calaque et al. (eds.) _Mathematical Aspects of Quantum Field Theories_, Mathematical Physics Studies, Springer 2014 ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))


See also the references given at _[differential cohomology hexagon -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)_.


[[!redirects Deligne complex]]

[[!redirects Deligne complexes]]

[[!redirects Deligne-Beilinson cohomology]]
[[!redirects Beilinson-Deligne cohomology]]