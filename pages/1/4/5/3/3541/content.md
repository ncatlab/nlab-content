

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents
* table of contents
{:toc}

## Idea
 {#Idea}

In [[quantum physics]] -- and specifically in [[quantum information theory]] and [[quantum probability theory]] -- by a *quantum operation* or *quantum channel* one means any physically reasonable operation on, or transformation of *[[mixed states]]* (in contrast to *[[quantum gates]]* operating on [[pure states]]), notably such as sending information through a "communication channel" (in the sense of [[information theory]]), whence the terminology *quantum channel*.

More concretely, the physical nature of quantum channels is that they unify "loss-less" [[unitary operator|unitary]] transformations on [[quantum states]] (as known [[Schrödinger equation|Schrödinger evoluation]] and [[quantum gates]]) with stochastic effects such as due to [[quantum noise]] and [[quantum state collapse]] due to [[quantum measurement]].

In short, just as the notion of [[mixed states]] generalizes the notion of [[pure state|pure]] [[quantum states]] with their objective, intrinsic and fundamental stochasticity (expressed the [[Born rule]]) to include also subjective, [[thermodynamics|thermodynamical]] [[probability distribution|classical stochasticity]], so quantum channels generalize [[quantum gates]] from pure to mixed states.

Mathematically, with [[mixed states]] represented by [[density matrices]] and generally by [[positive linear operators]], a quantum channel is just a suitable [[map]] between spaces of such [[matrices]] or [[linear operators]], whence they are sometimes also called *[[superoperators]]* (in the sense of "operators operating on operators").

But in the context of [[quantum information theory]] the relevant [[spaces of quantum states]] are all [[finite-dimensional Hilbert space|finite-dimensional]], in which case quantum channels are traditionally discussed as (special) [[linear maps]] between [[vector spaces]] of [[square matrix|square]] [[matrices]]:

$$
  chan
  \;\colon\;
  Mat_{n_1}(\mathbb{C}) 
    \longrightarrow
  Mat_{n_2}(\mathbb{C})
  \,.
$$

Slightly more abstractly, such as in the formulation of [[quantum information theory via dagger-compact categories]], these are certain [[morphisms]] in a [[compact closed category]] of the form

$$
  chan
  \;\colon\;
  \mathscr{H}_1 \otimes \mathscr{H}_1^\ast
    \longrightarrow
  \mathscr{H}_2 \otimes \mathscr{H}_2^\ast
$$

(where above $n_i = dim(\mathscr{H}_i)$ is the [[dimension of a vector space|dimension]] of the given [[finite-dimensional Hilbert space]]).

The key point is that such linear maps are to qualify as quantum channels iff they suitably restrict to maps between the *[[convex set|convex]]* [[subsets]] of [[density matrices]] (the [[mixed states]]) inside $\mathscr{H}_i\otimes\mathscr{H}_i^\ast$, which is a non-linear condition.

There is slight variation in the exact list of properties demanded of a quantum channel, but the key demand is that it  be a "*positive map*" in that it takes [[positive operators]] (such as [[density operators]]) to positive operators --- and in fact a *completely positive map*, meaning that it remains positive after [[tensor product of vector spaces|tensoring]] with any [[identity map|identity transformation]].

This is discussed below at:

* *[In terms of positivity conditions](#InTermsOfPositivityConditions)*


Often demanded is also that a quantum channel preserves the [[trace]] of matrices, which in [[quantum probability]] means that it preserves total probability, hence that it is the quantum analog of a *[[stochastic map]]*  --- through what fundamentally matters is that a quantum channel at most lowers the probability (the channel need not describe all possible outcomes, but it must not make new outcomes appear out of nowhere).

Less often demanded (but usually the case anyway) is that a quantum channel also preserves the [[identity matrix]], in which case it is the quantum analog of a [[doubly stochastic map]].

Beyond these abstract characterizations, the [[Stinespring factorization theorem]] characterizes quantum channels more explicitly as those maps on matrices arising as [[sums]] of [[conjugations]] 
$$
  chan
  \;\colon\;
  \rho 
  \;\mapsto\;
  \underset{w}{\sum}
  E_w \cdot \rho \cdot E_w^\dagger
$$
by certain [[tuples]] $(E_w)_{w \colon W}$ of linear operators ("*Kraus operators*"). Much of the discussion of quantum channels in the literature proceeds by manipulating such *Kraus decompositions* of quantum channels.

This is discussed below at:

* *[In terms of Kraus decompositions](#InTermsOfKrausDecompositions)*

For example, a [[unitary quantum channel]] describing a loss-less [[quantum gate]] is given by a single [[unitary operator|unitary]] Kraus operator as

\[
  \label{UnitaryChannelInIdeaSection}
  chan_U
  \;\colon\;
  \rho 
  \;\mapsto\;
  U \cdot \rho \cdot U^\dagger
  \,,
\]

which on [[pure states]] among [[mixed states]], $\rho_{|\psi\rangle} \coloneqq \left\vert \psi \right\rangle \left\langle \psi \right\vert$, restricts to an ordinary [[quantum gate]]

$$
  chan_U
  \;\colon\;
  \rho_{\vert\psi \rangle}
  \;\mapsto\;
  \rho_{ U \vert \psi \rangle }
  \,.
$$

On the other extreme, a [[quantum measurement]] in a measurement [[basis of a vector space|basis]] $W$, $\underset{W}{\oplus} \mathbb{C}  \simeq \mathscr{H}$ is given by the corresponding [[projection operators]] $P_w$ as

\[
  \label{MeasurementChannelInIdeaSection}
  meas_W
  \;\colon\;
  \rho 
  \;\mapsto\;
  \underset{w}{\sum}
  P_w \cdot \rho \cdot P_w
  \,.
\]

Remarkably (from the discussion at *[[quantum decoherence]]*) one finds that such a measurement channel (eq:MeasurementChannelInIdeaSection) may equivalently be understood as the result of a unitary evolution (eq:UnitaryChannelInIdeaSection) of the state $\rho$ coupled to an environment state $\omega$ *followed by* the [[partial trace quantum channel|partial trace]] over the environment's Hilbert space. This observation turns out to generally lead to yet another characterization of quantum channels:

Quantum channels equivalently act on a density matrix $\rho$ by 

1. tensoring it to another state $\omega$

   (coupling the system to an environment/"bath")

1. sending the tensor state through a unitary channel (eq:UnitaryChannelInIdeaSection) 

   ([[Schrödinger equation|Schrödinger evolution]] of the couplesystem)

1. applying the [[partial trace quantum channel|partial trace]] over the Hilbert space of $\omega$

   (averaging the outcome over all states of the environment/bath).

In this perspective, quantum channels are understood as a kind of unitary quantum gates after all, but acting on [[open quantum systems]] including their environment with the stochasticity induced (only) by (deliberate) ignorance of the environment's state.

This is discussed below at:

* *[Quantum channels and Decoherence](#QuantumChannelsAndDecoherence)*

In this last form, the formulation of quantum channels lends itself to formulation in the [[string diagram]]-calculus of [[quantum information theory via dagger-compact categories]]. 

This is discussed below at :

* [In terms of dagger-compact closed categories](#InTermsOfCompactClosedCategories)


\linebreak


## Definition
 {#Definition}

### In terms of positivity conditions
 {#InTermsOfPositivityConditions}



Let $\mathscr{H}_i$ be a [[complex vector space|complex]] [[finite-dimensional Hilbert space]], with 

$$
  Mat(\mathscr{H}_i) 
  \,\simeq\, 
  \mathscr{H}_i
  \otimes
  \mathscr{H}_i^\ast
$$

the corresponding space of [[matrices]]  --- including as a [[convex set|convex]] [[subset]] the [[density matrices]] representing the [[mixed states]] of the [[quantum system]] described by $\mathscr{H}$.

\begin{definition}\label{PositiveMaps}
  A $\mathbb{C}$-[[linear map]]
$$
  \Phi
  \;\colon\;
  \mathscr{H}_1
  \otimes
  \mathscr{H}_1^\ast
  \longrightarrow  
  \mathscr{H}_2
  \otimes
  \mathscr{H}_2^\ast
$$
is called

* *hermitian* iff it preserves [[Hermitian matrices]],

* *positive* iff it preserves [[positive operator|positive matrices]],

* *$n$-positive* if $\Phi \otimes Id_{\mathbb{C}^n}$ is positive for $n \in \mathbb{N}$,

* *completely positive* if $\Phi$ is $n$-positive for all $n \in \mathbb{N}$. 

A positive $\Phi$ is furthermore called:

* *[[stochastic map|stochastic]]* if it preserves the [[trace]] of matrices

* *doubly stochastic* if it preserves also the identity matrix.

Finally, a completely positive $\Phi$ is called:

* a *quantum channel* if it is stochastic,

* a *[[unital quantum channel]]* if it is doubly stochastic.
 
\end{definition}

&lbrack;[Arveson 1969 §1](#Arveson69), [Landau & Streater 1993 p. 107-108](#LandauStreater93)&rbrack;


### In terms of operator-sum decompositions
 {#InTermsOfKrausDecompositions}


\begin{theorem}
\label{OperatorSumDecompositionOfQuantumChannels}
**(operator-sum decomposition of quantum channels)**
\linebreak
For $\mathscr{H}_i$ [[finite-dimensional Hilbert spaces]], a  [[linear map]] 

$$
  chan
  \;\colon\;
  \mathscr{H}_1 \otimes \mathscr{H}_1^\ast
  \longrightarrow
  \mathscr{H}_2 \otimes \mathscr{H}_2^\ast
$$

is completely positive (Def. \ref{PositiveMaps}) precisely if there exists an [[indexed set]]

\[
  R \,\colon\, FinSet
  ,\;\;
  r \,\colon\, R
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  E_r \,\colon\, \mathscr{H}_1 \longrightarrow \mathscr{H}_2
\]

of [[linear operators]] such that $chan$ is the sum of [[conjugation actions]] with these operators ("Kraus form"):

\[
  \label{OperatorSumDecompositionFormula}
  chan(\rho)
  \;=\;
  \underset{r}{\sum}
  \,
  E_r \cdot \rho \cdot E_r^\dagger.
\]
\end{theorem}
Accordingly, in addition:

* $chan$ preserves the [[trace]] and is hence a quantum channel iff 

  $$
  \sum_r \, E_r^\dagger \cdot E_r \,=\, id_{\mathscr{H}_1}
  $$

* $chan$ preserves also the identity matrix and is hence a [[unital quantum channel]] iff (in addition)

  $$
  \sum_r \, E_r \cdot E_r^\dagger \,=\, id_{\mathscr{H}_2}
  \,.
  $$


The idea goes back to [Stinespring 1955](#Stinespring55). The decomposition (eq:OperatorSumDecompositionFormula) is also called *Kraus decomposition* by *Kraus operators*, after [Kraus 1971](#Kraus71). The fully explicit statement of Thm. \ref{OperatorSumDecompositionOfQuantumChannels} is due to [Choi 1975 Thm. 1](#Choi75). 

Review includes: [Nielsen & Chuang 2000 Thm. 8.1](#NielsenChuang00), [Kuperberg 2005 Thm. 1.5.1](#Kuperberg05). 

A general abstract proof in terms of [[dagger category|†-categories]] is claimed by [Selinger 2005](#Selinger05). A characterization of completely positive maps entirely in terms of $\dagger$-categories is given in [Coecke 2007](#Coecke07).

\begin{proposition}\label{CanonicalKrausDecomposition}
**(canonical operator sum-decomposition)**
\linebreak
The operator-sum decomosition $(E_r)_{r \colon R}$ in Thm. \ref{OperatorSumDecompositionOfQuantumChannels} may always be chosen such as to be [[orthogonality|orthogonal]] under the [[trace]]:
$$
  r,r' \,\colon\, R
  \;\;\;\;
  \vdash
  \;\;\;\;
  trace^{ \mathscr{H} }\big(
    E_{r'}^\dagger \cdot E_{r}
  \big)
  \;=\;
  d_r \delta_{r}^{r'}
$$
([[Kronecker delta]]) for some [[non-negative number|non-negative]] [[real numbers]] $(d_r)_{r \colon R}$.

Moreover, this *canonical Kraus form* is unique up to [[permutation]] of $R$. 
\end{proposition}
[Bengtsson & Życzkowski 2006 p. 256](#BengtssonŻyczkowski06)



[[!include quantum channels and decoherence -- section]]





### In terms of $\dagger$-compact closed categories
 {#InTermsOfCompactClosedCategories}

... due to ([Selinger 05](#Selinger05)) ... see for instance ([Coecke-Heunen 11, section 2](#CoeckeHeunen11)) for a quick summary ...


## Properties



### Universal property

The [[category]] whose [[objects]] are indexed by [[natural numbers]] $n,m, \cdots$ and whose [[morphisms]] are quantum operations from $n \times n$ to $m \times m$ matrices is a [[semicartesian monoidal category]] with the [[monoidal category|monoidal structure]] given by multiplication of numbers. Being semicartesian, the monoidal [[tensor unit]] (the number $1$) has a unique morphism to it from any object: this morphism is the trace. 

In fact, this category has the [[universal property]] of the semicartesian reflection of the monoidal category of [[isometries]]. This is the category whose objects are natural numbers, considered as [[Hilbert spaces]], and whose [[morphisms]] are isometries between them, where an [[isometry]] $m\to n$ is an $m\times n$ complex matrix $V$ such that $V V* = I$. 

In detail, the [[universal property]] says that for any strict semicartesian monoidal category $\mathcal{D}$ and any monoidal functor $\mathbf{Isometries}\to \mathcal{D}$, there is a unique symmetric monoidal functor making the following diagram commute:
$$
\array{
{Isometries} &\rightarrow& {Quantum Channels} \\
&\searrow&\downarrow\\
&& \mathcal{D}
}
$$

This fits a physical intuition as follows. Suppose that the isometries are a model of reality, as in the many worlds interpretation and the Church of the larger Hilbert space. But in practice the observer cannot access the entirety of reality, and so some bits are hidden. The canonical way to model this hiding is to do it freely, which is to form the semicartesian reflection.


## Examples
 {#Examples}

### Unitary quantum channels

A *[[unitary quantum channel]]* is a quantum channel whose restriction to [[pure states]] acts by a [[unitary transformation]] just as a loss-less [[quantum gate]] does.

Concretely, in terms of [operator-sym decomposition](#InTermsOfKrausDecompositions), a quantum channel 

$$
  \array{
    \mathscr{H}_1
    \otimes
    \mathscr{H}_1^\ast
    &
    \longrightarrow
    &
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    \\
    \rho
    &\mapsto&
    ch(\rho)
  }
$$

is unitary iff there exists a [[unitary operator]] $U \,\colon\, \mathscr{H}_1 \longrightarrow \mathscr{H}_2$ such that $ch$ is given by [[conjugation]] with this operator:

$$
  ch(\rho) \;=\; U \cdot \rho \cdot U^\dagger
  \,.  
$$

### Mixed unitary quantum channels

More generally, a *[[mixed unitary quantum channel]]* is given by an $S$-[[indexed set]] of [[unitary operators]] $(U_s)_{s \colon S}$ and a [[probability distribution]] $p \,\colon\, S \to [0,1]$ as

$$
  \rho 
    \,\mapsto\,
  \underset{s}{\sum}
  \,
  U_s \cdot \rho U_s^\dagger
  \,.
$$

This class includes for instance the [[bit-flip quantum channels]].

### Averaging quantum channels
 {#DecoherenceExample}

For $\mathscr{B}$ a [[finite-dimensional Hilbert space]], the operation of [[partial trace quantum channel|partial trace]] over $\mathscr{B}$ is a quantum channel, the *[[averaging quantum channel]]*.

$$
  \array{
    \mathscr{H}
    \otimes
    \mathscr{B}
    \otimes
    \mathscr{B}^\ast
    \otimes
    \mathscr{H}^\ast
    &
    \xrightarrow{
      trace^{\mathscr{B}}
    }
    &
    \mathscr{H} \otimes \mathscr{H}^\ast
    \\
    \left\vert \psi, \beta \right\rangle
    \left\langle \beta', \psi' \right\vert
    &\mapsto&
    \left\vert \psi \right\rangle
    \left\langle \beta' \vert \beta \right\rangle
    \left\langle \psi' \right\vert
    \mathrlap{\,.}
  }  
$$

See also at *[[quantum decoherence]]*.




### Quantum measurement channels
 {#QuantumMeasurementAndPOVM}

Consider 

$$
  \mathscr{H} 
     \,\equiv\, 
  \underset{w \colon W}{\oplus} \mathscr{H}_w
$$ 

a [[Hilbert space]] exhibited as the [[direct sum]] of subspaces $\mathscr{H}_w$ [[indexed set|indexed]] by a [[finite set]] $W \,\colon\, FinSet$, 
and write

$$
  P_w 
  \,\colon\,
  \mathscr{H}
  \twoheadrightarrow
  \mathscr{H}_w
  \hookrightarrow
  \mathscr{H}
$$

for the corresponding [[projection operator]].

By construction this is such that

$$
  \underset{w}{\sum} P_w
  \;=\;
  \mathrm{id}_{\mathscr{H}}
  \,,
$$

whence one also refers to the [[tuple]] $( w \mapsto P_w )$ aas  *[[projection valued measure]]* (here: on the [[finite set]] $W$).

If now $W$ is a [[quantum measurement]]-[[linear basis|basis]] on $\mathscr{H}$, then the [[quantum state collapse|collapse postulate]] of [[quantum mechanics]] says that after measuring $w \,\colon\, W$ for a quantum system previously in [[pure state]] $\left\vert \psi \right\rangle\,\colon\, \mathscr{H}$, the state will have collapsed (up to normalization) according to
$$
  \left\vert \psi \right\rangle
  \;\mapsto \;
  P_w \left\vert \psi \right\rangle
  \,,
$$

hence any [[mixed state]] ([[density matrix]]) will have evolved according to 

$$
  \rho \;\mapsto\; P_w \cdot \rho \cdot P_w
  \,.
$$

But if one now in addition considers classical [[probability theory|probabilistic]] uncertainty* as to which measurement result $w$ was actually found (say due to ignorance of the experimentor or imperfection of the measurement device) then all of the resulting pure states $P_w \left\vert \psi \right\rangle$ above are equivally likely and as such constitute the [[mixed state]] which is represented by the [[density matrix]]

$$
  \left\vert \psi \right\rangle
  \left\langle \psi \right\vert
  \;\;\mapsto\;\;
  \underset{w}{\sum}
  \,
  P_w \left\vert \psi \right\rangle
 \left\langle \psi \right\vert P_w
  \,.
$$

In general, if the initial state was [[mixed state|mixed]] to start with, then the stochastic quantum measurement process will be represented by

$$
  \array{
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
    &\overset{meas_W}{\longrightarrow}&
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
    \\
    \rho
    &\mapsto&
    \;\;\;\;\;
    \mathclap{
    \underset{w}{\sum}
    \,
    P_w \cdot \rho \cdot P_w
    \mathrlap{\,.}
    }
  }
$$

This is a quantum channel, and quantum channels of this form are called *[[quantum measurement channels]]*.



[[!include environment rep of quantum measurement channel - section]]






### Noise channels

Examples of [[quantum noise]] channels:

* [[bit flip channel]]

## Related concepts

* [[extremal quantum channel]] 

* [[quantum information theory via dagger-compact categories]]

[[!include states and observables -- content]]
  

## References

The operator-sum decomposition characterization of completely positive maps is due to:

* {#Stinespring55} [[W. Forrest Stinespring]], *Positive functions on $C^\ast$-algebras*, Proc. Amer. Math. Soc. **6** 2 (1955) 211-216 &lbrack;[doi:2032342](https://www.jstor.org/stable/2032342), [doi:10.2307/2032342](https://doi.org/10.2307/2032342)&rbrack;
 
* {#Kraus71} [[Karl Kraus]], *General state changes in quantum theory*, Ann. Physics **64** 2 (1971) 311-335 &lbrack;<a href="https://doi.org/10.1016/0003-4916(71)90108-4">doi:10.1016/0003-4916(71)90108-4</a>&rbrack;
 
* {#Choi75} [[Man-Duen Choi]], *Completely positive linear maps on complex matrices*, Linear Algebra and its Applications **10** 3 (1975) 285-290 &lbrack;<a href="https://doi.org/10.1016/0024-3795(75)90075-0">doi:10.1016/0024-3795(75)90075-0</a>&rbrack;

with early review in:

* [[David E. Evans]], [[John T. Lewis]],  *Dilations of irreversible evolutions in algebraic quantum theory*, Communications of the Dublin Institute for Advanced Studies, Series A: Theoretical Physics **24** (1977) &lbrack;[eprint:34031](https://orca.cardiff.ac.uk/id/eprint/34031), [pdf](https://orca.cardiff.ac.uk/id/eprint/34031/1/Evans_Lewis_DIAS.pdf)&rbrack;

* {#Kraus} [[Karl Kraus]], *States, Effects, and Operations -- Fundamental Notions of Quantum Theory*, Lecture Notes in Physics **190** Springer (1983) &lbrack;[doi:10.1007/3-540-12732-1](https://doi.org/10.1007/3-540-12732-1)&rbrack;

See also 

* {#Arveson69} [[William B. Arveson]], *On subalgebras of $C^\ast$-algebras*, Bull. Amer. Math. Soc. **75** (1969) 790-794 &lbrack;[doi:1969-75-04/S0002-9904-1969-12293-7](https://www.ams.org/journals/bull/1969-75-04/S0002-9904-1969-12293-7), [pdf](https://www.ams.org/journals/bull/1969-75-04/S0002-9904-1969-12293-7/S0002-9904-1969-12293-7.pdf)&rbrack; 
 
The [environmental representation](#QuantumChannelsAndDecoherence) of completely positive maps originates with


* {#Lindblad75} [[Göran Lindblad]], *Completely positive maps and entropy inequalities*,  Commun. Math. Phys. **40** (1975) 147–151 &lbrack;[doi:10.1007/BF01609396](https://doi.org/10.1007/BF01609396)&rbrack;

and was then eventually rediscovered for the special case of [[quantum measurement channels]] following the 1980s discussion of *[[decoherence]]*.
     

The terminology "quantum operation" for linear maps on the linear dual of a [[C-star algebra|$C^\ast$-algebra]] which preserve the subset of [[states on a star-algebra]]:

* {#HaagKastler64} [[Rudolf Haag]], [[Daniel Kastler]], pp. 850 in: *An algebraic approach to quantum field theory*, Journal of Mathematical Physics, **5** (1964) 848-861 &lbrack;[doi:10.1063/1.1704187](https://doi.org/10.1063/1.1704187), [spire:9124](https://inspirehep.net/literature/9124)&rbrack;

The terminology "quantum channel":

* {#ŻyczkowskiBengtsson04} [[Karol Życzkowski]], [[Ingemar Bengtsson]], Section 3 of: *On Duality between Quantum Maps and Quantum States*, Open Systems & Information Dynamics **11** 01 (2004) 3-42 &lbrack;[doi:10.1023/B:OPSY.0000024753.05661.c2](https://doi.org/10.1023/B:OPSY.0000024753.05661.c2)&rbrack;

* [[Teiko Heinosaari]], [[Mário Ziman]], Section 4 of: *The Mathematical Language of Quantum Theory -- From Uncertainty to Entanglement*, Cambridge University Press  (2011) &lbrack;[doi:10.1017/CBO9781139031103]( https://doi.org/10.1017/CBO9781139031103)&rbrack;


Analysis of [[extremal quantum channels]]:

* [Choi 1975. Thm. 2.11](#Choi75)

* {#LandauStreater93} [[L. J. Landau]], [[Raymond F. Streater]],  *On Birkhoff's theorem for doubly stochastic completely positive maps of matrix algebras*, Linear Algebra and its Applications **193** (1993) 107-127 &lbrack;<a href="https://doi.org/10.1016/0024-3795(93)90274-R">doi:10.1016/0024-3795(93)90274-R</a>&rbrack;

* [[Christian B. Mendl]], [[Michael M. Wolf]], *Unital Quantum Channels -- Convex Structure and Revivals of Birkhoff's Theorem*, Commun. Math. Phys. **289**  (2009) 1057-1096 &lbrack;[arXiv:0806.2820](http://arxiv.org/abs/0806.2820)&rbrack;

* James Miller, S. T. da Silva, *On the Extremality of the Tensor Product of Quantum Channels* &lbrack;[arXiv;2305.05795](https://arxiv.org/abs/2305.05795)&rbrack;

Review and survey:

* {#Warner10} [[Garth Warner]]: *Positivity*, University of Washington (2010) &lbrack;[pdf](https://sites.math.washington.edu//~warner/Positivity_Warner.pdf), [[Warner-Positivity.pdf:file]]&rbrack;

In the context of [[quantum computation]]:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], §8.2 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[John Preskill]], §3.2 in: *Measurement and Evolution*, chapter 3 of: *Quantum Information*, lecture notes, since 2004 &lbrack;[pdf](http://www.theory.caltech.edu/~preskill/ph219/chap3_15.pdf), [web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;

* {#Selinger04} [[Peter Selinger]], §6.3 in: _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], §1.5 of _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

in the context of [[quantum probability]]:

* [[Rolando Rebolledo]], *Complete Positivity and the Markov structure of Open Quantum Systems*, chapter in: [[Stéphane Attal]], [[Alain Joye]], [[Claude-Alain Pillet]] (eds.), *Open Quantum Systems II -- The Markovian approach*,  Lecture Notes in Mathematics **1881**, Springer (2006) 149-182 &lbrack;[doi:10.1007/b128451](https://doi.org/10.1007/b128451)&rbrack;

and in [[quantum information theory]]:

* [[Mark M. Wilde]], *Quantum Information Theory*, Cambridge University Press (2013) &lbrack;[doi:10.1017/CBO9781139525343](https://doi.org/10.1017/CBO9781139525343), [arXiv:1106.1445](https://arxiv.org/abs/1106.1445)&rbrack;

* [[Joseph M. Renes]], 4.32 in: *Quantum Information Theory* (2015) &lbrack;[pdf](https://edu.itp.phys.ethz.ch/hs15/QIT/renes_lecture_notes14.pdf)&rbrack; De Gruyter (2022) &lbrack;[doi:10.1515/9783110570250](https://doi.org/10.1515/9783110570250)&rbrack;


* [[Sumeet Khatri]], [[Mark M. Wilde]], §3.2 in: _Principles of Quantum Communication Theory: A Modern Approach_ &lbrack;[arXiv:2011.04672](https://arxiv.org/abs/2011.04672)&rbrack;


Further:

* {#BengtssonŻyczkowski06} [[Ingemar Bengtsson]], [[Karol Życzkowski]], Chapter 10 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048), [ResearchGate](https://www.researchgate.net/publication/266435541_Geometry_of_Quantum_States_An_Introduction_to_Quantum_Entanglement)&rbrack;


* [[Robert B. Griffiths]], *Quantum Channels, Kraus Operators, POVMs* (2012) &lbrack;[pdf](https://quantum.phys.cmu.edu/QCQI/qitd412.pdf), [[Griffiths-QuantumChannels.pdf:file]]&rbrack;

* {#AttalLectureNotes} [[Stéphane Attal]], *Quantum Channels*, Lecture 6 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Channels.pdf), [[Attal-QuantumChannels.pdf:file]], [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;


See also

* Caleb J. O'Loan, *Topics in Estimation of Quantum Channels*, PhD thesis, University of St. Andrews (2009) &lbrack;[arXiv:1001.397](http://arxiv.org/abs/1001.3971)&rbrack;




* John A. Smolin, Frank Verstraete, Andreas Winter, *Entanglement of assistance and multipartite state distillation*, Phys. Rev. A **72** (2005) 052317 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* John Watrous, _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ (2008) ([arXiv](http://arxiv.org/abs/0807.2668))

* Wikipedia, *[Quantum Operation](https://en.wikipedia.org/wiki/Quantum_operation)*


The description of completely positive maps in terms of [[dagger-categories]] (see at _[[quantum information theory via dagger-compact categories]]_) goes back to

* {#Selinger05} [[Peter Selinger]], *Dagger-compact closed categories and completely positive maps*, Electronic Notes in Theoretical Computer Science, **170** (2007) 139-163 &lbrack;[doi:10.1016/j.entcs.2006.12.018](https://doi.org/10.1016/j.entcs.2006.12.018), [[SelingerPositiveMaps.pdf:file]]&rbrack;

* {#Coecke07} [[Bob Coecke]], _Complete positivity without compactness_, 2007 ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 
 

This is further explored in:

* [[Bob Coecke]], [[Eric Paquette]], [[Dusko Pavlovic]], *Classical and quantum structures* (2008) &lbrack;[pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf), [[Coecke-Paquette-Pavlovic-CQS.pdf:file]]&rbrack;

* {#CoeckeHeunen11} [[Bob Coecke]], [[Chris Heunen]], _Pictures of complete positivity in arbitrary dimension_, EPTCS 95, 2012, pp. 27-35 ([arXiv:1110.3055](http://arxiv.org/abs/1110.3055))
 

* [[Bob Coecke]], [[Chris Heunen]], [[Aleks Kissinger]], _Categories of Quantum and Classical Channels_ ([arXiv:1305.3821](http://arxiv.org/abs/1305.3821))

For the universal property, see

* Mathieu Huot, Sam Staton, _Universal properties in quantum theory_ (QPL 2018) ([pdf](https://www.mathstat.dal.ca/qpl2018/papers/QPL_2018_paper_68.pdf)).

On quantum channel capacity:

* Alexander S. Holevo, *Quantum Systems, Channels, Information -- A Mathematical Introduction*, Studies in Mathematical Physics **16**, De Gruyter (2013) &lbrack;[doi:10.1515/9783110273403](https://doi.org/10.1515/9783110273403)&rbrack;

* Alexander S. Holevo, *Quantum channel capacities*, Quantum Electron. **50** 440 (2020) &lbrack;[doi:10.1070/QEL17285/meta](https://iopscience.iop.org/article/10.1070/QEL17285/meta)&rbrack;

[[!redirects quantum channel]]
[[!redirects quantum channels]]
[[!redirects quantum operation]]
[[!redirects quantum operations]]
[[!redirects quantum operations and channels]]

[[!redirects completely positive map]]
[[!redirects completely positive maps]]

[[!redirects Kraus decomposition]]
[[!redirects Kraus decompositions]]


