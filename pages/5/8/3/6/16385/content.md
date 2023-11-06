
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #HermitianForm}
###### Definition
**([[Hermitian form]] and [[Hermitian space]])**

Let $V$ be a [[real vector space]] equipped with a [[complex structure]] $J\colon V \to V$. Then a _[[Hermitian form]]_ on $V$ is 

* a complex-valued real-[[bilinear form]]

  $$
    h \;\colon\; V \otimes V \longrightarrow \mathbb{C}
  $$

such that this is _symmetric sesquilinear_, in that:

1. $h$ is complex-linear in the first argument;

1. $h(w,v) = \left(h(v,w) \right)^\ast$ for all $v,w \in V$ 

where $(-)^\ast$ denotes [[complex conjugation]].

A Hermitian form is _positive definite_ (often assumed by default) if for all $v \in V$

1. $h(v,v) \geq 0$

1. $h(v,v) = 0 \phantom{AA} \Leftrightarrow \phantom{AA} v = 0$.

A [[complex vector space]] $(V,J)$ equipped with a (positive definite) Hermitian form $h$ is called a (positive definite) _[[Hermitian space]]_.

=--

\begin{remark}
  A positive-definite and complete Hermitian vector space is called a *[[Hilbert space]]*.
\end{remark}


## Properties

### General properties

+-- {: .num_prop #BasicPropertiesOfHermitianForms}
###### Proposition
**(basic properties of [[Hermitian forms]])**

Let $((V,J),h)$ be a positive definite [[Hermitian space]] (def. \ref{HermitianForm}). Then 

1. the [[real part]] of the [[Hermitian form]] 

   $$
     g(-,-) \;\coloneqq\; Re(h(-,-))
   $$
  
   is a [[Riemannian metric]], hence a symmetric positive-definite real-[[bilinear form]] 

   $$
     g \;\colon\; V \otimes V \to \mathbb{R}
   $$

1. the [[imaginary part]] of the [[Hermitian form]]

   $$
     \omega(-,-) \;\coloneqq\; -Im(h(-,-))
   $$

   is a [[symplectic form]], hence a non-degenerate skew-symmetric real-[[bilinear form]]

   $$
     \omega \;\colon\; V \wedge V \to \mathbb{R}
     \,.
   $$

hence

$$
  h = g - i \omega
  \,.
$$

The two components are related by

$$
  \label{RelationBetweennOmegaAndgOnHermitianSpace}
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

Finally 

$$
  h(J(-),J(-)) = h(-,-)
$$

and so the  Riemannian metrics $g$ on $V$ appearing from (and fully determining) Hermitian forms $h$ via $h = g - i \omega$ are precisely those for which

$$  
  \label{HermitianMetric}
  g(J(-),J(-)) = g(-,-)
  \,.
$$

These are called the _[[Hermitian metrics]]_.

=--


+-- {: .proof}
###### Proof

The positive-definiteness of $g$ is immediate from that of $h$. The symmetry of $g$ follows from the symmetric sesquilinearity of $h$:

$$
  \begin{aligned}
    g(w,v)
    & \coloneqq
    Re(h(w,v))
    \\
    & =
    Re\left( h(v,w)^\ast\right)
    \\
    & =
    Re(h(v,w))
    \\
    & =
    g(v,w)
    \,.
  \end{aligned}
$$

That $h$ is invariant under $J$ follows from its sesquilinarity

$$
  \begin{aligned}
    h(J(v),J(w))
    &=
    i h(v,J(w))
    \\
    & =
    i (h(J(w),v))^\ast
    \\
    & =
    i (-i) (h(w,v))^\ast
    \\
    & =
    h(v,w)
  \end{aligned}
$$

and this immediately implies the corresponding invariance of $g$ and $\omega$.


Analogously it follows that $\omega$ is skew symmetric:

$$
  \begin{aligned}
    \omega(w,v)
    & \coloneqq
    -Im(h(w,v))
    \\
    & =
    -Im\left( h(v,w)^\ast\right)
    \\
    & =
    Im(h(v,w))
    \\
    & = - \omega(v,w)
    \,,
  \end{aligned}
$$

and the relation between the two components:

$$
  \begin{aligned}
    \omega(v,w)
    & =
    - Im(h(v,w))
    \\
    & =
    Re(i h(v,w))
    \\
    & =
    Re(h(J(v),w))
    \\
    & = 
    g(J(v),w)
  \end{aligned}    
$$

as well as

$$
  \begin{aligned}
    g(v,w)
    & =
    Re(h(v,w)
    \\
    & =
    Im(i h(v,w))
    \\
    & =
    Im(h(J(v),w))
    \\
    & =
    Im(h(J^2(v),J(w)))
    \\
    & = 
    - Im(h(v,J(w)))
    \\
    & = \omega(v,J(w))
    \,.
  \end{aligned}
$$


=--

### Relation to Kähler spaces

+-- {: .num_prop #RelationBetweenKaehlerVectorSpacesAndHermitianSpaces}
###### Proposition
**(relation between [[Kähler vector spaces]] and [[Hermitian spaces]])**

Given a [[real vector space]] $V$ with a [[linear complex structure]] $J$, then the following are equivalent:

1. $\omega \in \wedge^2 V^\ast$ is a [[linear Kähler structure]] (def. \ref{KaehlerVectorSpace});

1. $g \in V \otimes V \to  \mathbb{R}$ is a [[Hermitian metric]] (eq:HermitianMetric)

where $\omega$ and $g$ are related by (eq:RelationBetweennOmegaAndgOnHermitianSpace)

$$
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

=--


### As Real complex modules
 {#AsRealComplexModules}

While a non-degenerate [[inner product]] $(-\vert-)$ on a [[finite-dimensional vector space|finite-dimensional]] [[real vector space]] $V$ is equivalently a [[linear isomorphism]] to its [[dual vector space]]

$$
  \array{
    V 
      &\overset{\sim}{\longrightarrow}& 
    V^\ast
      &\overset{\sim}{\longrightarrow}& 
    V
    \\
    v &\mapsto& (v\vert-) &\mapsto& v
  }
$$

the analogous statement for  Hermitian complex inner products $\langle - \vert - \rangle$ fails, since the corresponding maps

\[
  \label{AntiLinearIsomorphismWithDualVectorSpace}
  \array{
    H
      &\overset{\sim}{\longrightarrow}& 
    H^\ast
      &\overset{\sim}{\longrightarrow}& 
    H
    \\
    \vert \psi \rangle 
    &\mapsto& 
    \langle \psi \vert
    &\mapsto& 
    \vert \psi \rangle    
  }
\]

are now complex *[[anti-linear map|anti-linear]]* and hence not [[morphisms]] in the [[category]] of [[complex vector spaces]].

(What one does get is a complex-linear isomorphism to the [[anti-dual linear space]], eg. [Karoubi & Villamayor 1973, p. 58 (3 of 31)](#KaroubiVillamayor73); [Karoubi 2010, §1](#Karoubi10).)

But one may absorb this anti-linearity into an ambient category so that Hermitian/unitary structure regarded *[[internalization|internally]]* to that category looks just like Euclidean/orthogonal structure. Since this uses basic structures known from Atiyah's *[[Real K-theory]]* --- with capital "R", [[KR-theory]] --- it is suggestive and convenient to refer to "Real" structures, as follows:

\begin{definition}
Write 
\[
  \label{CategoryOfRealvectorBundlesWithInvolution}
  Mod_{\mathbb{R}}^{\mathbf{B}\mathbb{Z}_2}
  \;\;\;
    \coloneqq
  \;\;\;
  Func\big(
    \mathbf{B}\mathbb{Z}_2
    ,\,
    Mod_{\mathbb{R}}
  \big)
\]
for the category of [[real vector spaces]] equipped with a [[linear map|linear]] [[involution]] (equivalently the [[functor category]] from the [[delooping groupoid]] of the [[cyclic group of order two]] to the category [[Vect|$Mod_{\mathbb{R}}$]] of [[real vector spaces]]).

This becomes a [[monoidal category]] whose modoidal stucture $\otimes$ is the [[tensor product of vector spaces|tensor product]] of the [[underlying]] [[vector spaces]] equipped with the tensor product of their involutions.
\end{definition}
\begin{example}\label{RealComplexNumbers}
**(Real complex numbers)**
  The [[complex numbers]] regarded as a [[real vector space]] equipped with its real-linear involution given by [[complex conjugation]] is an object of (eq:CategoryOfRealvectorBundlesWithInvolution). Moreover, since complex-conjugation is actually an [[algebra homomorphism]] on the complex numbers, the usual product operation makes this a [[monoid object]] [[internalization|internal]] to (eq:CategoryOfRealvectorBundlesWithInvolution), which we will refer to as the *Real complex numbers*:

\[
  \label{RealComplexNumbersObject}
  \mathbb{Z}_2
  \curvearrowright
  \mathbb{C}
  \;\in\;
  Mon\big(
    Mod_{\mathbb{R}}^{\mathbf{B}\mathbb{Z}_2}    
  \big)
  \,.
\]

\end{example}

\begin{definition}
 **(Real complex modules)**
\label{CategoryOfRealComplexModules}
 We say that the [[category of modules|category of]] [[module objects]] over the Real complex numbers (eq:RealComplexNumbersObject) [[internalization|internal]] to (eq:CategoryOfRealvectorBundlesWithInvolution) is the category of *Real complex modules*:
$$
  Mod_{
    \mathbb{Z}_2 \curvearrowright \mathbb{C}  
  }
  \;\;\;\;
    \equiv
  \;\;\;\;
  Mod_{
    \mathbb{Z}_2 \curvearrowright \mathbb{C}
  }
  \big(
    Mod_{\mathbb{R}}^{\mathbf{B}\mathbb{Z}_2}
  \big)
  \,.
$$
\end{definition}
\begin{lemma}
\label{AntilinearInvolutionFromRealComplexModules}
  The category of Real complex modules (Def. \ref{CategoryOfRealComplexModules}) is [[equivalence of categories|equivalent]], as a [[symmetric monoidal category]], to the category of [[complex vector spaces]] equipped with *[[anti-linear map|anti-linear]]* [[involutions]]:
$$
  Mod_{
    \mathbb{Z}_2 \curvearrowright \mathbb{C}  
  }
  \;\;
  \simeq
  \;\;
  \big(
    V \,\colon\, Mod_{\mathbb{C}}
  \big)
  \times
  \big(
    \sigma 
    \,\colon\,
    V 
    \xrightarrow{
      \mathbb{C} antilinear 
    }
    V
  \big)
$$
\end{lemma}
\begin{proof}
By direct unwinding of the definitions, one finds that the module property enforces the anti-linearity of the involution:

\begin{imagefromfile}
    "file_name": "AntilinInvViaRealComplexModules-230905.jpg",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Moreover, to see that the [[tensor products]] agree one can argue that the relevant [[coequalizers]] (see [here](Introduction+to+Stable+homotopy+theory+--+1-2#TensorProductOfModulesOverCommutativeMonoidObject)) in $Mod_{\mathbb{R}}^{\mathbf{B}\mathbb{Z}}$ are [[colimits]] in a [[category of presheaves]] which [[limits of presheaves are computed objectwise|are computed objectwise]] --- hence here over the single object of $\mathbf{B}\mathbb{Z}_2$, where they agree with the usual [[tensor product of vector spaces|tensor product]] of the [[underlying]] [[complex vector spaces]]. 
\end{proof}

The following construction is essentially what is known as the *[[hyperbolic functor]]* with $\mathbb{Z}/2$-equivariance, establishing an equivalence between [[KR-theory]] and [[topological Hermitian K-theory]] (see the references [there](#ReferencesTopologicalHermitianKTheory)):

\begin{example}\label{HermtianSpacesAsRealComplexModules}
**(Complex Hermitian spaces as Euclidean Real complex modules)**
\linebreak

For $H, \langle-\vert-\rangle_H$ a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space|complex]] [[Hermitian form|Hermitian]] [[inner product space]] (assumed non-degenerate), its [[direct sum]] with its [[linear dual space]] carries the [[anti-linear map|anti-linear]] [[involution]] induced
(eq:AntiLinearIsomorphismWithDualVectorSpace) by the Hermitian form:

\begin{imagefromfile}
    "file_name": "HermitianSpaceAsRealComplexModule-230905.jpg",
    "width": 270,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Therefore the Hermitian space $H$ induces a Real complex module by Lem. \ref{AntilinearInvolutionFromRealComplexModules}, which we denote by the corresponding script symbol:
$$
  \mathscr{H}
  \;\coloneqq\;
  \mathbb{Z}_2 \curvearrowright 
  \big(
    H  \oplus H^\ast
  \big)
  \;\;
  \in
  \;\;
  Mod_{
   \mathbb{Z}_2 \curvearrowright \mathbb{C}
   \,.
  }
$$

Notice that the Real complex modules $\mathscr{H}$ arising this way have special properties:

1. $\mathscr{H}$ is a [[self-dual object]], via the following ([[coevaluation map|co]]-)[[evaluation maps]]

\begin{imagefromfile}
    "file_name": "SelfDualStructureOnRealComplexModule-230905.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


1. $\mathscr{H}$ carries an [[internalization|internal]] [[complex structure]], namely an [[automorphism]] (now of Real complex modules!) which squares to minus the [[identity morphism]]:

\begin{imagefromfile}
    "file_name": "ComplexStructureOnRealComplexModule-230905.jpg",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Due to this complex and [[self-dual object|self-dual]] structure we may think of $\mathscr{H}$ as being a *[[Euclidean space|Euclidean]]* (instead of Hermitian) complex linear space but now *[[internalization|internal to]]* Real complex modules.
\end{example}

\begin{proposition}
  Given a [[pair]] of ([[finite-dimensional vector space|finite-dimensional]], non-degenerate) complex Hermitian spaces $H, \langle-\vert-\rangle_H$ and $K, \langle-\vert-\rangle_K$, there the complex [[linear maps]] between them are in bijection to the [[homomorphisms]] between the corresponding Real complex modules according to Exp. \ref{HermtianSpacesAsRealComplexModules}, as follows:

1. the ordinary $\mathrm{i}$-complex linear maps $H \to K$ correspond to the $\mathrm{i}\beta$-complex homomorphism $\mathscr{H} \to \mathscr{K}$

1. the ordinary [[unitary maps]] $H \to K$ correspond to the [[orthogonal maps]] $\mathscr{H} \to \mathscr{K}$ (namely those which respect the [[evaluation maps]] on these [[self-dual objects]]).

\end{proposition}
\begin{proof}
  This follows by straightforward unwinding of the definitions:

First, for a homomorphism $\mathscr{H} \to \mathscr{K}$ to commute with $\mathrm{i}\beta$ its [[underlying]] complex linear map clearly needs to respect the [[direct sum]], structure $H \oplus H^\ast \to K \oplus K^\ast$, hence it needs to come from complex linear map $g \,\colon\,H \to K$. But then the respect for the complex involution uniquely fixes the action $H^\ast \to K^\ast$. Interestingly, it fixes them to be given by the linear dual of the [[adjoint operator|operator adjoint]] $g^\dagger$:


\begin{imagefromfile}
    "file_name": "ComplexLinMapsAsRealComplexHoms-230905.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}



Second: A unitary map is a complex linear map that preserves the Hermitian form. But with the first point above one sees that this is equivalent to preserving the evaluation map on the corresponding Real complex modules:

\begin{imagefromfile}
    "file_name": "UnitaryCLinMapIsOrthRealComplexMap-230905.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\end{proof}

In **summary**: After [[internalization]] as Real complex modules, complex Hermitian/unitary space look like complex Euclidean/orthogonal spaces: 

\begin{imagefromfile}
    "file_name": "HermitianSpAsEuclidRealComplexMods-230906.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak

<center>
<img src="/nlab/files/HermitianSpacesAsEquivariantModules-230901.jpg" width="780">
</center>

\linebreak


(...)

\linebreak



## Related concepts

* [[Hilbert space]]

* [[bilinear form]], [[quadratic form]], [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]]

* [[hermitian matrix]]

* [[Hermitian manifold]]

* [[quadratic form]]

* [[bra-ket]]

* [[Hermitian K-theory]]

## References

Hermitian forms are named in honor of the discussion of [[quadratic forms]] due to:

* [[Charles Hermite]], *Sur la théorie des formes quadratiques. Premier mémoire*,  Journal für die reine und angewandte Mathematik **47** (1854) 313-342 &lbrack;[doi:10.1515/crll.1854.47.343](https://doi.org/10.1515/crll.1854.47.343)&rbrack;

maybe starting with

* [[Luigi Bianchi]], *Forme definite di Hermite*, §24 in:  *Sui gruppi di sostituzioni lineari con coefficienti appartenenti a corpi quadratici immaginarî*, Mathematische Annalen **40** (1892) 332–412 &lbrack;[doi:10.1007/BF01443558](https://doi.org/10.1007/BF01443558)&rbrack;

see:

* Jürgen Elstrodt, Fritz Grunewald, Jens Mennicke: *Integral Binary Hermitian Forms*, Ch. 9 in *Groups Acting on Hyperbolic Space*, Springer (1998) &lbrack;[doi:10.1007/978-3-662-03626-6_9]( https://doi.org/10.1007/978-3-662-03626-6_9)&rbrack;

Discussion of Hermitian forms over the [[complex numbers]], as understood today, originates in the definition of [[Hilbert spaces]] (in laying of mathematical foundations of [[quantum mechanics]]):

* {#vonNeumann30} [[John von Neumann]], p. 64 in: *Allgemeine Eigenwerttheorie Hermitescher Funktionaloperatoren*, Math. Ann. **102** (1930) 49–131 &lbrack;[doi:10.1007/BF01782338](https://doi.org/10.1007/BF01782338)&rbrack;

* [[John von Neumann]]:

  p. 21 in: *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  pp. 38 in: *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

Textbook accounts in the context of [[operator algebras]]:

* [[Richard V. Kadison]], [[John R. Ringrose]], §2.1 in: *Fundamentals of the theory of operator algebras* Vol I *Elementary Theory*, Graduate Studies in Mathematics **15**, AMS (1997) &lbrack;[ISBN:978-0-8218-0819-1](https://bookstore.ams.org/gsm-15)&rbrack;

* [[Bruce Blackadar]], §I.1.1 in: *Operator Algebras -- Theory of $C^\ast$-Algebras and von Neumann Algebras*, Encyclopaedia of Mathematical Sciences **122**, Springer (2006) &lbrack;[doi:10.1007/3-540-28517-2](https://doi.org/10.1007/3-540-28517-2)&rbrack;

* {#Landsman17} [[Klaas Landsman]], §A.1 in: *Foundations of quantum theory -- From classical concepts to Operator algebras*, Springer Open (2017) &lbrack;[doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf)&rbrack;

See also:

* Wikipedia, _[Hermitian form](https://en.wikipedia.org/wiki/Sesquilinear_form#Hermitian_form)_

and see the references at *[[Hilbert space]]*.

Hermitian forms as isomorphisms to the [[anti-dual linear space]]:

* {#Karoubi10} [[Max Karoubi]], §1 in: *Le théorème de périodicité en K-théorie hermitienne*, Quanta of Maths **1**, AMS and Clay Math Institute Publications (2010) &lbrack;[arXiv:0810.4707](https://arxiv.org/abs/0810.4707)&rbrack;

  > (in the context of [[Hermitian K-theory]])

Hermitian forms in the generality over [[noncommutative ring|noncommutative]] [[ground rings]] (and discusssed in the context of [[Hermitian K-theory]]):

* {#KaroubiVillamayor73} [[Max Karoubi]], [[Orlando Villamayor]], Ex. 1 in: *K-théorie algébrique et K-théorie topologique II*, Math. Scand. **32** (1973) 57-86 &lbrack;[jstor:24490565](https://www.jstor.org/stable/24490565)&rbrack;

* [[C. T. C. Wall]], _On the axiomatic foundations of the theory of Hermitian forms_, Proc. Camb. Phil. Soc. **67** (1970) 243-250 &lbrack;[doi:10.1017/S0305004100045515](https://doi.org/10.1017/S0305004100045515), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/wall9.pdf)&rbrack;

* [[John Milnor]], [[Dale Husemöller]], *Hermitian forms*, Appendix 2 of: *Symmetric Bilinear Forms*,  Ergebnisse der Mathematik und ihrer Grenzgebiete **73**, Springer (1973) &lbrack;[doi:10.1007/978-3-642-88330-9](https://doi.org/10.1007/978-3-642-88330-9)&rbrack;

{#ReferencesViaDaggerCompactStructure} Hermitian forms expressed through [[dagger-compact category]]-[[structure]] (notably for [[quantum information theory via dagger-compact categories]]):

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], Def. 7.5 in: *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) $[$[arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)$]$

* {#AbramskyCoecke05} [[Samson Abramsky]], [[Bob Coecke]], p. 6 in: *Abstract Physical Traces*, Theory and Applications of Categories, **14** 6 (2005) 111-124. \[<a href="http://www.tac.mta.ca/tac/volumes/14/6/14-06abs.html">tac:14-06</a>, [arXiv:0910.3144](https://arxiv.org/abs/0910.3144)\]

* [[Bob Coecke]], Def. 2.5 in: *De-linearizing Linearity: Projective Quantum Axiomatics from Strong Compact Closure*, Proceedings of the [3rd International Workshop on Quantum Programming Languages (2005)](https://www.mathstat.dal.ca/~selinger/qpl2005/), Electronic Notes in Theoretical Computer Science **170** (2007) 49-72 \[<a href="https://doi.org/10.1016/j.entcs.2006.12.011">doi:10.1016/j.entcs.2006.12.011</a>, <a href="https://arxiv.org/abs/quant-ph/0506134">arXiv:quant-ph/0506134</a>\]

* [Duncan 2006](quantum+information+theory+via+dagger-compact+categories#Duncan06), [p. 31](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf#page=39)


[[!redirects Hermitian forms]]

[[!redirects hermitian form]]
[[!redirects hermitian forms]]

[[!redirects Hermitian space]]
[[!redirects Hermitian spaces]]

[[!redirects hermitian space]]
[[!redirects hermitian spaces]]

[[!redirects Hermitian vector space]]
[[!redirects Hermitian vector spaces]]

[[!redirects hermitian vector space]]
[[!redirects hermitian vector spaces]]


[[!redirects Hermitian metric]]
[[!redirects Hermitian metrics]]

[[!redirects hermitian metric]]
[[!redirects hermitian metrics]]

[[!redirects Hermitian inner product]]
[[!redirects Hermitian inner products]]
[[!redirects hermitian inner product]]
[[!redirects hermitian inner products]]

[[!redirects Hermitian inner product space]]
[[!redirects Hermitian inner product spaces]]
[[!redirects hermitian inner product space]]
[[!redirects hermitian inner product spaces]]



