
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A *Yang-Baxter equation* (YBE) is, in some form or other, an [[algebra|algebraic]] reflection of this [[isotopy]] of [[braids]]:

\linebreak

\[\label{TheIsotopy}\]
\begin{imagefromfile}
    "file_name": "3rdReidemeisterFramedLinks.png",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -50,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

which is also known as the *[2nd Artin braid relation](braid+group#2ndArtinRelation)* or the *[[3rd Reidemeister move]] for [[framed links]]*.

### Quantum YBE

#### Plain form

Interpreting the isotopy (eq:TheIsotopy) as an [[equality]] of [[string diagrams]] in a [[braided monoidal category]] $(\mathcal{C}, \otimes)$, with each strand/string labeled by the same given [[object]] $V \in \mathcal{C}$, it says that the [[braiding]] $R \colon\, V \otimes V \to V \otimes V$ satisfies

\[
  \label{PlainQuantumYBE}
  (R \otimes id) 
  \circ 
  (id \otimes R)
  \circ
  (R \otimes id) 
  \;\;
  =
  \;\;
  (id \otimes R)
  \circ
  (R \otimes id) 
  \circ
  (id \otimes R)
\]

as an [[equation]] in [[endomorphisms|$End(V \otimes V \otimes V)$]] (where we are notationally suppressing [[associators]], in full this is diagram B7 in [Joyal & Street 1985](braided+monoidal+category#JoyalStreet85) [p 7](https://ncatlab.org/nlab/files/JoyalStreet-BraidedMonoidal85.pdf#page=7)).

This equation (eq:PlainQuantumYBE) --- on any map $R$ of the form $R \,\colon\, V \otimes V \to V \otimes V$ (not necessarily the ambient [[braiding]] structure map) --- is called the plain *[[quantum Yang-Baxter equation]]*. 

If $V \otimes V$ is the [[tensor product of vector spaces|tensor product of]] a [[finite-dimensional vector space]] $V$ with itself, then any choice of [[linear basis]] $V \simeq k^d$ identifies the [[linear map]] $R$ with a [[matrix]] $(R_{n_1, n_2}^{m_1, m_2})_{n_i, m_i = 1}^{d}$, thus traditionally called an *[[R-matrix]]*.

In a [[symmetric monoidal category]] like [[Vect|$Vect$]], with symmetric [[braiding]] $\sigma \,\colon\, V \otimes V \to V \otimes V$, it is traditional to define

$$
  \check R
  \,\coloneqq\,
  \sigma \circ R
  \;\;\;\;
  \text{and}
  \;\;\;\;
  \check R_{i j}
  \,\coloneqq\,
  \phi_{i,j}(\sigma \circ R)
  \mathrlap{\,,}
$$

where 

$$
  \phi_{i,j}
  \,\colon\,
  End(V \otimes V)
  \hookrightarrow
  End(V \otimes V \otimes V)
  \;\;\;\;\;
  \text{for}
  \;
  1 \leq i \lt j \leq 3
$$

identifies $V \otimes V$ with the tensor product of the $i$th and the $j$th copy of $V$ in $V \otimes V \otimes V$ (inserting an [[identity morphism|identity]] on the remaining copy).

In terms of this "check-R matrix" $\check R$, the plain [[quantum Yang-Baxter equation]] (eq:PlainQuantumYBE) is equivalent to 

\[
  \label{PlainQuantumYBInParameterizedForm}
  \check R_{23}
  \circ
  \check R_{13}
  \circ
  \check R_{12}
  \;=\;
  \check R_{12}
  \circ
  \check R_{13}
  \circ
  \check R_{23}
  \,.
\]

In either form, any solution to the plain Yang-Baxter equation in [[Vect|$Vect$]] defines [[linear representations]] of the [[braid groups]] $Br_n$ ([[braid representations]]), by representing the $i$th [Artin braid generator](braid+group#ArtinGenerators) $b_i$ by 

$$
  b_i 
  \;\;
  \mapsto
  \;\;
  id^{\otimes_{i-1}} \otimes R \otimes id^{\otimes_{n-i-1}}
  \,.
$$

This is manifest from the *[Artin presentation](braid+group#ArtinPresentation)* of the [[braid group]], see there.



#### Parameterized form

The plain form (eq:PlainQuantumYBInParameterizedForm) of the Yang-Baxter equation generalizes to the case where $\check R_{i j}$ is taken to dependent on a [[pair]] of parameters $u, u' \in U$ (typically taken from $U = \mathbb{C}$ the [[complex numbers]]), in which case one says that the condition 

\[
  \label{ParameterizedQuantumYBEquation}
  \check R_{23}(u_2, u_3)
  \circ
  \check R_{13}(u_1, u_3)
  \circ
  \check R_{12}(u_1, u_2)
  \;=\;
  \check R_{12}(u_1, u_2)
  \circ
  \check R_{13}(u_1, u_3)
  \circ
  \check R_{23}(u_2, u_3)
\]

is the *parameterized quantum Yang-Baxter equation*.

In the special case of this generalization where $U \equiv \mathbb{C}^\times$ is the [[multiplicative group|multiplicative]] [[group of units|group of]] [[complex numbers]] and restricting the dependence to be on the [[quotient]] of the parameters 

$$
  \check R(u, u') \,=\, \check R( u/u')
  \,,
$$

the parameterized quantum Yang-Baxter equation (eq:ParameterizedQuantumYBEquation) becomes (identifying  $u \coloneqq u_1/u_2$ and $v \coloneqq u_2/u_3$)

\[
  \label{MultiplicativeSpectrallyParameterizedQuantumYBEquation}
  \check R_{23}(v)
  \circ
  \check R_{13}(u v)
  \circ
  \check R_{12}(u)
  \;=\;
  \check R_{12}(u)
  \circ
  \check R_{13}(u v)
  \circ
  \check R_{23}(v)
  \,,
\]

and one speaks of the parameterized quantum Yang-Baxter equation with "*multiplicative spectral parameter*".

Yet again redefining by passage to [[logarithms]] of the parameters, $u \mapsto ln u$ (or rather, understanding the previous parameters a [[exponential map|exponentials]]), 
the equation (eq:MultiplicativeSpectrallyParameterizedQuantumYBEquation) assumes the form with "*additive spectral parameter*":

\[
  \label{MultiplicativeSpectrallyParameterizedQuantumYBEquation}
  \check R_{23}(v)
  \circ
  \check R_{13}(u + v)
  \circ
  \check R_{12}(u)
  \;=\;
  \check R_{12}(u)
  \circ
  \check R_{13}(u + v)
  \circ
  \check R_{23}(v)
  \,.
\]

This spectral form (eq:MultiplicativeSpectrallyParameterizedQuantumYBEquation) is close to the historical origin of Yang-Baxter equation, whence some authors refer to this form by default as the "*the Yang-Baxter equation*" (cf. [Jimbo 1989 (2.1)](#Jimbo89)).


### Classical YBE

(...)


## Variants 
 {#Variants}

Beware that the term _Yang-Baxter equation_ can mean (or be interpreted in the context of) any of several related but different concepts:

[[!include Yang-Baxter equations -- contents]]



## References
 {#References}

> for more see at *[[quantum Yang-Baxter equation|quantum YBE]]*, *[[classical Yang-Baxter equation|classical YBE]]*, [etc.](#Variants)

The ([[quantum Yang-Baxter equation|quantum]]) *Yang-Baxter equation* was named (cf. [Perk & Au-Yang 2006](#PerkAu-Yang06)) by [[Ludwig Fadeev]] in the late 1970s, in honor of:

* [[Chen Ning Yang]]: *Some Exact Results for the Many-Body Problem in one Dimension with Repulsive Delta-Function Interaction*, Phys. Rev. Lett. **19** (1967) 1312 &lbrack;[doi:10.1103/PhysRevLett.19.1312](https://doi.org/10.1103/PhysRevLett.19.1312)&rbrack;

* [[Chen Ning Yang]]: *S Matrix for the One-Dimensional $N$-Body Problem with Repulsive or Attractive $\delta$-Function Interaction*, Phys. Rev. **168** (1968) 1920 &lbrack;[doi:10.1103/PhysRev.168.1920](https://doi.org/10.1103/PhysRev.168.1920)&rbrack;

and

* {#Baxter72} [[Rodney J. Baxter]]: *Partition function of the Eight-Vertex lattice model*, Annals of Physics **70** 1 (1972) 193-228 \[<a href="https://doi.org/10.1016/0003-4916(72)90335-1">doi:10.1016/0003-4916(72)90335-1</a>\]

* {#Baxter78} [[Rodney J. Baxter]]: *Solvable eight-vertex model on an arbitrary planar lattice*, Philos. Trans. Royal Society A **289** 1359 (1978) &lbrack;[doi:10.1098/rsta.1978.0062](https://doi.org/10.1098/rsta.1978.0062)&rbrack;

* {#Baxter82} [[Rodney Baxter]]: *Exactly Solved Models in Statistical Mechanics*, Academic Press (1982, 1984, 1989) &lbrack;[webpage](https://physics.anu.edu.au/research/ftp/mpg/baxter_book.php), [pdf](https://physics.anu.edu.au/research/ftp/_files/Exactly.pdf)&rbrack;
  > (who spoke instead of the "star-triangle relation").


Reviews:

* {#Jimbo89} [[Michio Jimbo]]: *Introduction to the Yang-Baxter Equation*,  International Journal of Modern Physics A **4** 15 (1989) 3717-3757 &lbrack;[doi:10.1142/S0217751X89001497](https://doi.org/10.1142/S0217751X89001497)&rbrack;

  reprinted in: *Braid Group, Knot Theory and Statistical Mechanics*, Advanced Series in Mathematical Physics **9**, World Scientific (1991) &lbrack;[doi:10.1142/0796](https://doi.org/10.1142/0796)&rbrack;

* {#PerkAu-Yang06} Jacques H. H. Perk, Helen Au-Yang: *Yang-Baxter Equations*, Encyclopedia of Mathematical Physics **5** (2006) 465-473 &lbrack;[arXiv:math-ph/0606053](https://arxiv.org/abs/math-ph/0606053)&rbrack;

Literature collection with focus on application to [[integrable systems]]:

* [[Michio Jimbo]] (ed.): *Yang-Baxter Equation in Integrable Systems*, Advanced Series in Mathematical Physics **10**, World Scientific (1990) &lbrack;[doi:10.1142/1021](https://doi.org/10.1142/1021)&rbrack;






See also:

* Wikipedia, _[Yang-Baxter equation](https://en.wikipedia.org/wiki/Yang%E2%80%93Baxter_equation)_

* [[eom]], *[Yang-Baxter equation](https://encyclopediaofmath.org/index.php?title=Yang-Baxter_equation)*



[[!redirects Yang-Baxter equations]]
