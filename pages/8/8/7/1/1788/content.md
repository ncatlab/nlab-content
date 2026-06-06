> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\linebreak


[[chord orbifold -- section]]

## Chord orbifolds in music theory

### Idea

In [[music theory]], the configuration space of unordered musical *chords*, [[global quotient orbifold|quotentied]] by *acoustic equivalences* like *octave repetition* and *voice permutation*, may be thought of &lbrack;[Tymoczko 2006](#Tymoczko2006), [Calender, Quinn & Tymoczko 2008](#CalenderQuinnTymoczko2008)&rbrack; as an [[orbifold]] (specifically a [[toroidal orbifold]]) whose singular strata correspond to distinct *voices*, as follows:


**Pitch-Class Space as a Circle.** In Western music, *pitch* may be modeled continuously as a [[real number]] $p\in\mathbb{R}$, where [[integers]] represent semitones (e.g., piano keys). However, human hearing exhibits *octave equivalence*: a "C" played in one octave sounds functionally equivalent to a "C" played in the next octave, 12 semitones away. Therefore considering pitches modulo octave equivalent yields the *pitch-class* [[quotient space]], topologically a [[circle]]:
 
\[
  \label{PitchClassSpace}
  \mathbb{R}/12\mathbb{Z}
    \cong 
  S^{1}
  \mathrlap{\,.}
\]


**Ordered Chords Space as a Torus.** An ordered $n$-note chord  is an [[n-tuple|$n$-tuple]] of such pitch classes. The space of all such ordered $n$-note chords is therefore the [[Cartesian product]] of $n$ circles, which is the [[n-torus|$n$-torus]]:

\[
  \label{OrderedChordSpace}
  T^{n}
    =
  \big(S^1\big)^{\times_n}
  \mathrlap{\,.}
\]

**Unordered Chord Space as an Orbifold.** But music theory typically treats chords as unordered [[sets]]. For example, the chord $\{C, E, G\}$ is functionally the same chord as $\{E, G, C\}$. To formalize this [[permutation]] [[invariance]], one is to consider the further quotient of the torus $T^{n}$ (eq:OrderedChordSpace) by the [[permutation]] [[group action|action]] of the [[symmetric group]] $Sym_{n}$. But since this action is not [[free action|free]] (it has [[fixed points]]), the proper incarnation of this is as the *[[global quotient orbifold]]*

$$
  T^n \sslash Sym_n
  \,.
$$

The [[orbifold singularity|singular]] [[strata]] of this [[orbifold]] correspond to the chords where voices merge (cross).

**Further Symmetries.** There are further [[symmetries]] that may be quotiented out: 


* *Transposition*: Shifting all notes up or down by a constant interval $c$. This acts as a continuous translation along the main diagonal of $T^{n}$. Factoring out transposition yields a space locally isomorphic to $\mathbb{R}^{n-1}$.

* *Inversion*: Reflecting pitch space ($p\mapsto-p$), which corresponds to turning chords upside down.

The [[global quotient orbifold]] of the $n$-torus by permutation, transposition, and inversion simultaneously results in a farily complex orbifold. For example, the space of 3-note chords modulo transposition and inversion is a [[Möbius strip]] with a [[boundary]] of [[singular points]].

\linebreak

Of course, there is mathematical idealization involved in this, which may not necessarily always be reflected in musical practice (cf. [Tymoczko 2007](#Tymoczko2007))

### Applications

These orbifolds are used to study *voice leading* --- the transition from one chord to another over time. A piece of music can be modeled as a continuous path winding through this orbifold. Efficient voice leading (where voices move by the smallest possible intervals) translates to finding [[geodesics]] on this [[Riemannian orbifold]], where [[orbifold singularity|singular]] boundaries act like acoustic "mirrors"; paths that bounce off the singularities represent musical voices crossing or temporarily merging into a unison.



### References

The original articles:

* {#Tymoczko2006} [[Dmitri Tymoczko]]: *The Geometry of Musical Chords*, Science **313** 5783 (2006) 72--74 &lbrack;[doi:10.1126/science.1126287](https://doi.org/10.1126/science.1126287), [pdf](https://dmitri.mycpanel.princeton.edu/voiceleading.pdf)&rbrack;

* {#CalenderQuinnTymoczko2008} Clifton Callender, Ian Quinn, [[Dmitri Tymoczko]]: *Generalized Voice-Leading Spaces* Science **320** 5874 (2008) 346--348 &lbrack;[doi:10.1126/science.1153021](https://doi.org/10.1126/science.1153021), [pdf](https://dmitri.mycpanel.princeton.edu/files/publications/science2.pdf)&rbrack;

Further discussion: 

* {#Tymoczko2007} [[Dmitri Tymoczko]]: *Response to Comment on "The Geometry of Musical Chords"*, Science **315** 5810 (2007) 330 &lbrack;[doi:10.1126/science.1134163](https://doi.org/10.1126/science.1134163)&rbrack;

Exposition:

* [[Dmitri Tymoczko]]: *[Mathematical Moments: Putting Music on the Map](https://www.ams.org/publicoutreach/mathmoments/mm57-music-podcast)*, AMS News & Outreach (July 2006) &lbrack;audio:[mp3](https://www.ams.org/samplings/mathmoments/podcast-mom-music.mp3)&rbrack;

* Mattia G. Bergomi: *Musical modeling through graphs and orbifolds* (2014) &lbrack;[pdf](http://repmus.ircam.fr/_media/moreno/MMIM_Bergomi_Tonnetz.pdf)&rbrack;

* Jon Latané: *[Topologica: Jazz, Orbifolds, and Your Event-Sourced, Flux-Driven Dream Code](https://medium.com/fully-automated-luxury-robot-music/topologica-jazz-orbifolds-and-your-event-sourced-flux-driven-dream-code-f8e24443a941)*, blog post (2017)

---


$\esh$



$$
  J 
    \;=\;
    \sum_i f_i \theta_i 
      + 
    \sum_j g_j d \theta_j 
    f_i, g_j \in C^\infty(X)
  \,.
$$


\begin{xymatrix}
Q B \ar[d] \ar[r] & Q A \sqcup Q B \ar[d] \ar[r] & A \sqcup Q B \ar[d]\cr
  B        \ar[r] & Q A \sqcup   B        \ar[r] & A \sqcup   B       \cr
\end{xymatrix}


_________


Jun4 730 DeanYoung testing ...



## Using the cellular cohomology of complex projective space
 {#ViaCellularCohomology}

There is a proof using that the [[cellular cohomology]] of [[complex projective space]] $\mathbb{CP}^{n-1}$ is (see [there](complex+projective+space#Cohomology))

$$
  H^i(\mathbb{CP}^{n-1}, \mathbb{Z}) \cong \mathbb{Z}^{a_i}
  \mathrlap{\,,}
$$ 

where 
$$
  a_i 
    =
  \left\{ 
  \begin{array}{ll}
    1 & \text{if}\; i \in \{ 2j \vert 0 \leq j \leq n-1 \}
    \\
    0 & \text{otherwise}
  \end{array}
  \right.
$$

and in which the cup product induces a ring-isomorphism 

$$
H^* (\mathbb{CP}^n, \mathbb{Z}) \simeq  \mathbb{Z}[c] / c^n \mathbb{Z}[c]
$$

where $c$ is the integral first Chern class (see [here](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)

\begin{theorem} 
Let $K$ be a [[finite dimensional vector space]] over $\mathbb{C}$ with $\mu \colon K \otimes_{\mathbb{C}} K \rightarrow K$ a $\mathbb{C}$-[[linear map]] and an element designated by $\eta : \mathbb{C} \rightarrow K$ satisfying the following two properties:

* ([[unitality]]) $\mu \circ \left( \eta \otimes Id_{K} \right) \circ \eta_1 \ = \ Id_K \ = \ \mu \circ \left( Id_K \otimes \eta \right) \circ \eta_2$ where $\eta_1 : \{ * \} \times \mathbb{CP}^{n-1}  \rightarrow \mathbb{CP}^{n-1}$ and $\eta_2 : \mathbb{CP}^{n-1} \times \{ * \} \rightarrow \mathbb{CP}^{n-1}$ are the unit isomorphisms with respect to the cartesian closed category induced by [product](cartesian+product#InAGeneraCategory).

* (no [[zero-divisors]]) for $a, b \in K$, if $\mu (a \otimes b) = 0$, then either $a = 0$ or $b = 0$.

Then $K$ is [[isomorphism|isomorphic]] to $\mathbb{C}$ itself as a [[complex vector space|$\mathbb{C}$-vector space]], i.e. $\text{dim}(K) = 1$.
\end{theorem}

Note that we obtain such a nonassociative $\mathbb{C}$-algebra as the [[splitting field]] of any complex [[irreducible  polynomial]].

\begin{proof}
Using the second property we obtain a [[continuous function]] 

$$ 
 \mu |_{ \mathbb{C}^n - \{ 0 \} }  \ : \ \left( \mathbb{C}^{n} - \{ 0 \} \right) \times \left( \mathbb{C}^{n} - \{ 0 \} \right)\ \rightarrow\ \mathbb{C}^{n} - \{ 0 \}
$$

Bilinearity implies that $\pi \circ  \mu|_{ \mathbb{C}^n - \{ 0 \} }$ factors through the product $\mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1}$ where $\pi :  \mathbb{C}^{n} - \{ 0 \} \rightarrow \mathbb{CP}^{n-1}$ is the quotient map. We get a continuous function

$$
 [ \mu|_{ \mathbb{C}^n} ] \ : \ \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1} \rightarrow \mathbb{CP}^{n-1}
$$

We obtain two equations by applying degree-2 [[integral cohomology]] to the two unit laws in the first property, irrespective of any associativity or commutativity of $K$:

$$ 
  H^2 \left( 
    \mu 
      \circ 
    \left( 
      \eta \times Id_{\mathbb{CP}^{n-1}} 
    \right) , 
    \mathbb{Z} 
  \right)   
  =  
  Id_{H^2 \left( \mathbb{CP}^{n-1} , \mathbb{Z} \right) }
  =   
  H^2 \left( 
    \mu 
    \circ 
    \left( 
      Id_{\mathbb{CP}^{n-1}} \times \eta 
    \right) , 
    \mathbb{Z} 
  \right)
  \mathrlap{\,.}
$$

Let $y \in H^2(\mathbb{CP}^{n-1})$ be the generator of the [[cohomology ring]] $H^* ( \mathbb{CP}^{n-1} )$. We have:

$$
  H^2\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1}; 
    \mathbb{Z}
  \big) 
   \cong 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
   \oplus 
  H^2\big(
    \mathbb{CP}^{n-1}; \mathbb{Z}
  \big) 
  \mathrlap{\,.}
$$

We can write 

$$
  H^2(\mu,\mathbb{Z})(y) 
    = 
  a \cdot (1 \otimes y) + b \cdot (y \otimes 1)
$$

for some $a, b \in \mathbb{Z}$.

The two equations obtained from the unit laws for $K$ imply that:

$$
  a = 1, 
  \,
  b = 1
  \mathrlap{\,.}
$$

There is an [[isomorphism]] of [[Hopf algebras]] in [[integral cohomology]] of 

$$
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big) 
    \otimes_{\mathbb{Z}}
  \big(
    \mathbb{Z}[x]/x^n\mathbb{Z}[x]
  \big)  
    \cong  
  H^*\big(
   \mathbb{CP}^{n-1};
   \mathbb{Z}
  \big) 
    \otimes_{\mathbb{Z}} 
  H^*\big(
    \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)  
    \cong  
  H^*\big(
    \mathbb{CP}^{n-1} \times \mathbb{CP}^{n-1};
    \mathbb{Z}
  \big)
  \mathrlap{\,.}
$$

But $H^*(\mu,\mathbb{Z})$ is a [[ring homomorphism]], so

$$
  H^*(\mu,\mathbb{Z})(y^n) 
    = 
  (1 \otimes y + y \otimes 1)^n 
    = 
  \sum_{i = 0}^n {\binom{n}{i}} (1 \otimes y)^i \cdot (y \otimes 1)^{n-i} 
    = 
  \sum_{i = 0}^n y^{n-i} \otimes y^{i}
$$

as elements of the commutative Hopf-algebra

$$
  H^*(\mathbb{CP}^{n-1},\mathbb{Z}) 
    \otimes_{\mathbb{Z}} 
  H^*(\mathbb{CP}^{n-1},\mathbb{Z})  
   \;\cong\; 
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right) 
   \otimes  
  \left( 
    \mathbb{Z}[x]/x^n \mathbb{Z}[x] 
  \right)
  \mathrlap{\,.}
$$

The left-hand side is $0$.

The right hand side is 

$$ 
   \sum_{i = 1}^{n-1} y^{n-i} \otimes y^{i} 
  \mathrlap{\,.}
$$

By way of [[proof by contradiction|contradiction]], suppose that $n = \text{dim}(K)$ is greater than $1$. In this case, each of the terms $y^i \otimes y^{n-i}$ is nonzero for $0 \lt i \lt n$, and their sum is as well.

This implies that 

$$
  \sum_{i= 1}^{n-1} {\binom{n}{i}}  y^{n-i} \otimes y^{i}$$

is not zero, which contradicts that $y^n$ is zero using the above equation.

This implies $n = 1$ and hence the claim.
\end{proof}



## Using the complex topological $K$-theory of complex projective space
 {#ViaComplexTopologicalK-Theory}





