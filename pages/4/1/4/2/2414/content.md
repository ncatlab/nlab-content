
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here indicates how 1-dimensional [[FQFT]]s (the [[superparticle]]) may be related to [[topological K-theory|topological]] [[K-theory]].

=--


> **raw material**: this are notes taken more or less verbatim in a seminar -- needs polishing




Previous:

* [[Axiomatic field theories and their motivation from topology]].

Next

* [[(2,1)-dimensional Euclidean field theories and tmf]]

#Contents#
* table of contents
{:toc}


## $(1,1)d$ EFTs

recall the **commercial for supergeometry**  with which we ended [[Axiomatic field theories and their motivation from topology|last time]]: the grading introduced by supergeometry makes it possible to have push-forward diagrams of the kind:

$$
  \array{
    (0|1)TFTs^n(X)/\simeq &\leftarrow& H^n_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    (0|1)TFT^0(X)/\simeq &\leftarrow&  H^0_{dR}(pt)
  }
$$


**Example** of 1-EFT

$$
  \sigma_1(M^n) = E : 1-EB  \to tV
$$

$$
  pt \mapsto \Gamma M
$$

$$
  (pt \stackrel{[0,t]}{\to}) 
  \mapsto 
  e^{- t \Delta}
$$

**Example** of $(1|1)-EFT$ associated to a [[Spin structure|spin manifold]], there is the [[spinor bundle]]

$$
  S = S^+ \oplus S^-
$$

a $\mathbb{Z}/2$-graded [[vector bundle]] and on this there is the [[Dirac operator]]

$$
  D : \Gamma(S) \to \Gamma(S)
$$

where $\Gamma(S) = \Gamma(S^+) \oplus \Gamma(S^-)$. So we can write

$$
  D =
  \left(
    \array{
       0 & D_-
       \\
       D+ & 0
    }
  \right)
$$

$$
  \sigma_{1|1}(M) : Bord_{1|1} \to TV
$$

$$
  \mathbb{R}^{0|1} \mapsto E(\mathbb{R}^{0|1}) = \Gamma(S)
$$

there is an involution $invol : \mathbb{R}^{0|1} \to \mathbb{R}^{0|1}$. It maps to

$$
  invol \mapsto grading involution
$$

we have the following [[moduli space]] of super [[interval]]s (super 1d-bordisms)

$$
  \mathbb{R}^{1|1}_+ \simeq
  \{super intervals I_{t,\theta}\}/\sim
$$

and these are mapped by the EFT as

$$
  I_{t,\theta} \mapsto e^{-t D^2 + \theta D}
$$

(here we are implicitly working in the [[topos]] of [[sheaf|sheaves]] on the category of [[supermanifold]]s and these equations have to be interpreted in that topos-logic, mapping [[generalized element]]s to [[generalized element]]s).



So we have for $E$ a $1|1$ EFT a _reduced_ non-susy field theory

$$
  \array{
     (1|1)EBord &\stackrel{E}{\to}& TV
      \\
     \uparrow & \nearrow_{E_{red}}
      \\
      EBord_1^{spin}
  }
$$

**Definition** $E \in (1|1)EFT$, the [[partition function]] $Z_E$ of $E$ is the function


$$
  Z_E : \mathbb{R}_+ \to \mathbb{C}
$$

$$
  t \mapsto Z_{E_{red}}(t) = E_{red}(S^1_t)
$$

that sends a length to the value of the EFT on the circle of that circumferene.


**Example** Consider from above the EFT

$$
  E = \sigma_{1|1}(M)
$$

look at its reduced part

$$
  z_E(t) = E_{red}(S^1_t)
$$

notice that by the above this assigns

$$
  [0,t] \stackrel{E_{red}}{\mapsto} e^{-t D^2}
$$

$$
  S^1_t \mapsto str(e^{-t D^2})
  = 
  tr(e^{-t D^2})|_{even} - tr(e^{-t D^2})|_{odd}
$$

where on the right we have the [[super trace]].

This evaluates to

$$
  str(e^{-t D^2})
  =
  \sum_{\lambda \in Spec(D^2)}
  e^{-t \lambda}
   sdim E_{\lambda}
$$

where the [[super dimension]] of the [[eigenspace]] $E_\lambda$ is

$$
 dim E^+_\lambda - dim E^-_\lambda
$$

and this vanishes for $\lambda \neq 0$ since there $D : E_\lambda^+ \stackrel{\simeq}{\to} E_\lambda^-$

is an [[isomorphism]].

So further in the computation we have

$$
  \cdots = dim ker D_+ - dim coker D_+
  = 
  \hat A(M)
$$

where the last step is the [[Atiyah-Singer index theorem]].

So **due to supersymmetry** , the [[partition function]] has two very special properties:

* it is constant -- in that it does not depend on $t$,

* it takes integer values $\in \mathbb{N} \subset \mathbb{R}$.

**recall** from $V \to X$ a [[vector bundle]] [[connection on a bundle|with connection]] $\nabla$ we get a 1d EFT

$$
  E_{(V,\nabla)} \in 1d EFT(X)
$$

given by the assignment

$$
  E_{(V,\nabla)} : 1s EB(X) \to TV
$$

$$
  (x : pt \to X) \mapsto V_x = fiber of V over x
$$

a morphism is an [[interval]] $[0,t]$ of length $t$ equipped with a map $\gamma : [0,t] \to X$, this is sent to the [[parallel transport]] associated with the [[connection on a bundle]]

$$
  \gamma \mapsto (V_{\gamma_x} \to V_{\gamma_y})
$$

Now refine this example to super-dimension $(1|1)$:

**example** of a $(1|1)$-EFT over $X$ consider

$$
  EBord_{(1|1)} \to EBord_{1}(X) \stackrel{E_{(V,\nabla)}}{\to}
  TV
$$

given by the assignment

$$
  (\Sigma^{(1|1)} \to X)(
  \mapsto 
  (\Sigma^{(1|1)}_{red} \to X)
  \mapsto 
  parallel transport as before
$$

so we just forget the super-part and consider the same [[parallel transport]] as before.

now to  [[K-theory]]:

$
  KO^0(X) = 
$ [[Grothendieck group]] of real [[vector bundle]]s over $X$

$$
  KO^{-n}(pt) = 
  \left\{
    \array{
         \mathbb{Z} & n = 0 mod 4
         \\
         \mathbb{Z}_2 & n = 1,2 mod 8
         \\
         0 & otherwise
    }
  \right.
$$

there is a [[Bott element]] $\beta \in KO^{-8}(pt)$

such that

$$
  KO^*(pt) \stackrel{\simeq_{\mathbb{Q}}}{\to}
  \mathbb{Z}[u,u^{-1}]
$$

$$
  \beta \mapsto u^2
$$

now the **push-forward in  [[topological K-theory]]**

$$
  p : X^n \to pt
$$

for $X$ a closed [[spin structure]] manifold

then there exists an embedding $X \hookrightarrow S^{n+m}$. Let $\nu$ be the [[normal bundle]] to this embedding.

then we define

$$
  \int_X : KO^k(X) \to KO^{k-n}(pt)
$$

as follows:

let $D(\nu)$ be the [[disk bundle]] and $S(\nu)$ be the [[sphere bundle]] of $\nu$. Then the [[Thom bundle]] is

$$
  T(\nu) := D(\nu)/S(\nu)
$$

we get a map

$$
  S^{n+m} \stackrel{C}{\to} T(\nu) := D(\nu)/S(\nu)
$$

involving the [[Thom isomorphism]]

$$
  C(X) = \left\{
   \array{
      X & if x \in D(\nu)
      \\
     * & otherwise
   }
  \right.
$$

then we set

$$
  \array{
      KO^k(X)
      && \stackrel{\int_X}{\to}&& KO^{k-n}(pt)
      \\
      & {}_{Thom iso}\searrow
      &&&
      \downarrow^{\simeq}_{suspension}
      \\
      && \tilde KO^{k+m}(T(\nu))
      &\stackrel{C^*}{\to}&
    
  }
$$

***

now start with $X^n$ again a [[spin structure|spin]] [[manifold]]

then

**theorem** (Stolz-Teichner): we have the horizontal isomorphism in the following diagram:

$$
  \array{
     && [E_{(V,\nabla)}]&& \stackrel{}{\leftarrow}
     && [V^+ - V^-]
     \\
     1 \in 
     &&(1|1)EFT^0(X)/_{conc}
     &&\stackrel{\simeq}{\to}&& KO^0(X) && \ni 1 
     \\
     \downarrow &&\downarrow^{quantization}
     &&&& \downarrow^{\int_X} && \downarrow
     \\
     \sigma_{(1|1)}(X)
     &&EFT^{-n}(pt)/_{conc}
     &&\stackrel{\simeq}{\to}&& KO^{-n} && \alpha(X)
     \\
     &\searrow&&{}_{partition func}\searrow&& 
    \swarrow_{\simeq} && \swarrow_{Atiyah's \alpha invariant}
     \\
     &&&&
     (\mathbb{Z}[u,u^{-1}])^{-n}
     \\
     &&&&
     index D = \hat A(X) u^{n/4}
  }
$$

**question** if we don't divide out [[concordance]], do we get [[differential K-theory]] on the right?

**answer** presumeably, but not worked out yet

## Related concepts

* [[supersymmetric quantum mechanics]]

* [[Euclidean quantum field theory]]

* [[spectral triple]]

* [[spectral action]]

* [[higher category theory and physics]]: <a href="http://ncatlab.org/nlab/show/higher+category+theory+and+physics#SpecStandModAndGravity">Spectral standard model and gravity</a>

* **(1,1)-dimensional Euclidean field theories and K-theory**
  
* [[(2,1)-dimensional Euclidean field theories and tmf]]

* [[2-spectral triple]]

## References
 {#References}

* [[Stephan Stolz]], [[Peter Teichner]], _[[What is an elliptic object?]]_ in _Topology, geometry and quantum field theory_ , London Math. Soc. LNS 308, Cambridge Univ. Press (2004), 247-343. ([pdf](http://web.me.com/teichner/Math/Reading_files/Elliptic-Objects.pdf))


* Pokman Cheung, _Supersymmetric field theories and cohomology_ ([arXiv:0811.2267](http://arxiv.org/abs/0811.2267))

* {#Stolz} [[Stefan Stolz]] (notes by Arlo Caine), _Supersymmetric Euclidean field theories and generalized cohomology_ Lecture notes (2009) ([pdf](http://www.cpp.edu/~jacaine/pdf/Lectures_complete.pdf))

* [[Stefan Stolz]], [[Peter Teichner]], _Supersymmetric Euclidean field theories and generalized cohomology_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011)