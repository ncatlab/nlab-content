
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The Goerss-Hopkins-Miller theorem ([Goerss-Hopkins A](#GoerssHopkinsA), [Goerss-Hopkins B](#GoerssHopkinsB)) as such establishes that the assignment to each [[elliptic curve]] of its [[elliptic cohomology|elliptic]] [[cohomology theory]] lifts in a [[coherence|coherent]] way to an assignment of the [[Brown representability theorem|representing]] [[spectra]] regarded as [[E-∞ rings]]. In summay this makes for a [[structure sheaf]] $\mathcal{O}_{\mathcal{M}^{der}}$ of the [[moduli stack of elliptic curves]] in [[derived algebraic geometry]], realizing that moduli stack  as a [[derived scheme]] $\mathcal{M}^{der}$ in [[E-∞ geometry]] ("spectral geometry") ([[A Survey of Elliptic Cohomology|Lurie]]).

In detail the theorem utilizes and establishes more general tools concerning the [[obstruction]] theory of lifting [[formal group laws]] to [[cohomology theories]] and homotopy associative/commutative [[spectra]] to [[A-∞ rings]] and to [[E-∞ ring]] structure, respectively. 

In the succinct and suggestive form of ([[A Survey of Elliptic Cohomology|Lurie, theorem 1.1]]) the Goerss-Hopkins-Miller theorem asserts the existence of the lift $\mathcal{O}_{\mathcal{M}^{der}}$ in the [[diagram]]

$$
  \array{
    && E_\infty Rings
    \\
    &{}^{\mathllap{\mathcal{O}_{\mathcal{M}^{der}}}}\nearrow& \downarrow^{\mathrlap{Brown\;representation}}
    \\
    \mathcal{M}(R)
    &\longrightarrow&
    MCTs
  }
  \,,
$$

where the bottom map sends ([[derived elliptic curve|derived]]) [[elliptic curves]] over a [[ring]] $R$ to their associated [[elliptic cohomology|elliptic]] [[multiplicative cohomology theory]] ("MTC") and where the right vertical map sends a [[spectrum]] to the cohomology theory which it [[Brown representability theorem|represents]].

### Hopkins-Miller theorem

For $n \in \mathbb{N}$, consider the [[category]] whose [[objects]] are [[pairs]] consisting of a [[perfect field]] $k$ of finite [[characteristic]] and of a [[formal group]] of [[height of a formal group|height]] $n$, and whose [[morphisms]] are base change of fields (as rings).

The **Hopkins-Miller theorem** says that there is a functorial assignment $(k,\Gamma) \mapsto E_{k,\Gamma}$ to such data of an [[A-∞ ring]] [[spectrum]] $E_{k,\Gamma}$ such that

1. $\pi_2 E_{k,\Gamma}$ contains a [[unit]] and $\pi_{2n+1} E_{k,\Gamma} = 0$, hence in particular $E_{k,\Gamma}$ is [[complex oriented cohomology theory|complex orientable]];

1. the corresponding [[formal group law]] over $\pi_0 E_{k,\Gamma}$ is the [[Lubin-Tate formal group|universal deformation]] of $(k,\Gamma)$.

In this form this appears as ([Rezk 97, theorem 2.1](#Rezk97)).

### Goerss-Hopkins theorem

(...)

## References


An introduction to and survey of the Goerss-Hopkins-Miller-Lurie theorem is in

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller, and Lurie)_ S&#233;minaire BOURBAKI Mars 2009 61&#232;me ann&#233;e, 2008-2009, no 1005(2009)([arXiv:0910.5130](http://arxiv.org/abs/0910.5130))

which has grown out of

* _[[Topological Algebraic Geometry - A Workshop]]._

* [pdf](http://www.math.uni-bonn.de/people/grk1150/Past_Events/AG-programm-SS07.pdf)

Details on the Hopkins-Miller theorem are in 

* {#Rezk97} [[Charles Rezk]], _Notes on the Hopkins-Miller theorem_, 1997 ([pdf](http://www.math.uiuc.edu/~rezk/hopkins-miller-thm.pdf))

and a survey is also in 

* [[Akhil Mathew]], _[Hopkins-Miller theorem I](https://amathew.wordpress.com/tag/hopkins-miller-theorem/)_

The Goerss-Hopkins theorem is laid out in 


* {#GoerssHopkinsA} [[Paul Goerss]], [[Michael Hopkins]], _Moduli spaces of commutative ring spectra_ ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/sum.pdf))

* {#GoerssHopkinsB} [[Paul Goerss]], [[Michael Hopkins]], _Moduli problems for structured ring spectra_ ([pdf](http://www.math.northwestern.edu/~pgoerss/spectra/obstruct.pdf))

A more abstract formulation of this is sketched in

* [[Jacob Lurie]], _[[Formal Moduli Problems and DG-Lie Algebras|Moduli problems for ring spectra]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/moduli.pdf))

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology]]_

See also at _[survey of elliptic curves -- Gluing of curves to a spectrum](A+Survey+of+Elliptic+Cohomology#gluingallellipticcohomologytheoriestothetmfspectrum)_


An exposition with indications of further developments in [[(infinity,1)-category theory]] is in 

* [[Aaron Mazel-Gee]], _Goerss-Hopkins obstruction theory for $\infty$-categories_, November 2013 ([pdf](http://math.berkeley.edu/~aaron/writing/thursday-cghost-beamer.pdf))


[[!redirects Goerss-Hopkins-Miller-Lurie theorem]]

[[!redirects Hopkins-Miller theorem]]
[[!redirects Goerss-Hopkins theorem]]