[[!redirects quantum operation]]

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

Remarkably (from the discussion at *[[quantum decoherence]]*) one finds that such a measurement channel (eq:MeasurementChannelInIdeaSection) may equivalently be understood as the result of a unitary evolution (eq:UnitaryChannelInIdeaSection) of the state $\rho$ coupled to an environment state $\omega$ *followed by* the [[partial trace]] over the environment's Hilbert space. This observation turns out to generally lead to yet another characterization of quantum channels:

Quantum channels equivalently act on a density matrix $\rho$ by 

1. tensoring it to another state $\omega$

   (coupling the system to an environment/"bath")

1. sending the tensor state through a unitary channel (eq:UnitaryChannelInIdeaSection) 

   ([[Schrödinger equation|Schrödinger evolution]] of the couplesystem)

1. applying the [[partial trace]] over the Hilbert space of $\omega$

   (averaging the outcome over all states of the environment/bath).

In this perspective, quantum channels are understood as a kind of unitary quantum gates after all, but acting on [[open quantum systems]] including their environment with the stochasticity induced (only) by (deliberate) ignorance of the environment's state.

This is discussed below at:

* *[In terms of partial traces](#InTermsOfartialTraces)*

In this last form, the formulation of quantum gates lends itself to formulation in the [[string diagram]]-calculus of [[quantum information theory via dagger-compact categories]]. 

This is discussed below at :

* [In terms of dagger-compact closed categories](#InTermsOfCompactClosedCategories)


\linebreak


## Definition

### In terms of positivity conditions
 {#InTermsOfPositivityConditions}

> old material, to be adjusted...

Notice that the identity map is clearly completely positive and trace preserving, and that the composite of two maps that preserve positivity and trace clearly still preserves positivity and trace. Therefore we obtain a [[category]] $QChan \subset Vect$ -- a [[subcategory]] of [[Vect]]${}_{\mathbb{C}}$ -- whose

* objects are the vector spaces $Mat(n \times n, \mathbb{C})$ for all $n \in \mathbb{N}$;

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.





### In terms of Kraus decompositions
 {#InTermsOfKrausDecompositions}

> old material, to be adjusted...

+-- {: .num_theorem}
###### Theorem

A map $\Phi$ as above is _completely positive_ precisely if there exists a [[set]] $I$ and an $I$-family $\{E_i \in Mat(k \times n, \mathbb{C}| i \in I)\}$ of matrices, such that for all $A \in Mat(n \times n, \mathbb{C})$ we have

$$
  \Phi(A) = \sum_{i \in I} E_i A E_i^\dagger
  \,.
$$

Moreover, such $\Phi$ preserves the trace of matrices precisely if 

$$
  \sum_{i \in I} E_i^\dagger E_i = Id_{Mat(n \times n, \mathbb{C})}
  \,.
$$

=--

This is originally due to [Stinespring 1955](#Stinespring55). The decomposition in the theorem is called _Kraus decomposition_ after [Kraus 1971](#Kraus71). See also ([Choi 75, theorem 1](#Choi75)). Review includes [Nielsen & Chuang 2000, Thm. 8.1](#NielsenChuang00, [Kuperberg 2005, Thm. 1.5.1](#Kuperberg05). A general abstract proof in terms of [[dagger category|†-categories]] is given by [Selinger 2005](#Selinger05). A characterization of completely positive maps entirely in terms of $\dagger$-categories is given in [Coecke 2007](#Coecke07).

The matrices $\{E_i\}$ that are associated to a completely positive and trace-preserving map by the above theorem are called **Kraus operators**.

In the physics literature the above theorem is then phrased as: _Every quantum channel can be represented using Kraus operators_  .


### In terms of partial traces 
 {#InTermsOfartialTraces}

(...)



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

This fits a physical intuition as follows. Suppose that the isometries are a model of reality, as in the the many worlds interpretation and the Church of the larger Hilbert space. But in practice the observer cannot access the entirety of reality, and so some bits are hidden. The canonical way to model this hiding is to do it freely, which is to form the semicartesian reflection.


## Examples
 {#Examples}

### Quantum measurement and POVMs

A [[quantum measurement]] is formally represented by a quantum operation that is induced by a [[positive-operator valued probability measure]] (POVM).

### Decoherence and partial traces
 {#DecoherenceExample}

For the moment see the references at *[[quantum decoherence]]*.

### Noise channels

Examples of [[quantum noise]] channels:

* [[bit flip channel]]

## Related concepts

* [[extremal quantum channel]] 

* [[quantum information theory via dagger-compact categories]]

[[!include states and observables -- content]]
  

## References

The Kraus-decomposition characterization of completely positive maps is due to

* {#Stinespring55} [[W. Forrest Stinespring]], *Positive functions on $C^\ast$-algebras*, Proc. Amer. Math. Soc. **6** 2 (1955) 211-216 &lbrack;[doi:2032342](https://www.jstor.org/stable/2032342), [doi:10.2307/2032342](https://doi.org/10.2307/2032342)&rbrack;
 
* {#Kraus71} [[Karl Kraus]], *General state changes in quantum theory*, Ann. Physics **64** 2 (1971) 311-335 &lbrack;<a href="https://doi.org/10.1016/0003-4916(71)90108-4">doi:10.1016/0003-4916(71)90108-4</a>&rbrack;
 
* {#Choi75} M. Choi, _Completely positive linear maps on complex matrices_, Linear Algebra and its Applications Volume 10, Issue 3, (1975), Pages 285-290

* {#Kraus} [[Karl Kraus]], *States, Effects, and Operations -- Fundamental Notions of Quantum Theory*, Lecture Notes in Physics **190** Springer (1983) &lbrack;[doi:10.1007/3-540-12732-1](https://doi.org/10.1007/3-540-12732-1)&rbrack;
 
The terminology "quantum operation" for linear maps on the linear dual of a [[C-star algebra|$C^\ast$-algebra]] which preserve the subset of [[states on a star-algebra]]:

* {#HaagKastler64} [[Rudolf Haag]], [[Daniel Kastler]], pp. 850 in: *An algebraic approach to quantum field theory*, Journal of Mathematical Physics, **5** (1964) 848-861 &lbrack;[doi:10.1063/1.1704187](https://doi.org/10.1063/1.1704187), [spire:9124](https://inspirehep.net/literature/9124)&rbrack;


Review and survey:

In the context of [[quantum computation]]:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], §8.2 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[John Preskill]], §3.2 in: *Measurement and Evolution*, chapter 3 of: *Quantum Information*, lecture notes, since 2004 &lbrack;[pdf](http://www.theory.caltech.edu/~preskill/ph219/chap3_15.pdf), [web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;

* {#Selinger04} [[Peter Selinger]], §6.3 in: _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], §1.5 of _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

and in [[quantum information theory]]:

* [[Mark M. Wilde]], *Quantum Information Theory*, Cambridge University Press (2013) &lbrack;[doi:10.1017/CBO9781139525343](https://doi.org/10.1017/CBO9781139525343), [arXiv:1106.1445](https://arxiv.org/abs/1106.1445)&rbrack;

* [[Sumeet Khatri]], [[Mark M. Wilde]], §3.2 in: _Principles of Quantum Communication Theory: A Modern Approach_ &lbrack;[arXiv:2011.04672](https://arxiv.org/abs/2011.04672)&rbrack;


Further:

* [[Ingemar Bengtsson]], [[Karol Życzkowski]], Chapter 10 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048)&rbrack;


* [[Robert B. Griffiths]], *Quantum Channels, Kraus Operators, POVMs* (2012) &lbrack;[pdf](https://quantum.phys.cmu.edu/QCQI/qitd412.pdf), [[Griffiths-QuantumChannels.pdf:file]]&rbrack;

* [[Stéphane Attal]], *Quantum Channels*, Lecture 6 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Channels.pdf), [[Attal-QuantumChannels.pdf:file]], [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;


See also

* Caleb J. O'Loan (2009), _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))


* Christian B. Mendl, Michael M. Wolf, _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))


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

[[!redirects quantum measurement channel]]
[[!redirects quantum measurement channels]]

[[!redirects unital quantum channel]]
[[!redirects unital quantum channels]]


