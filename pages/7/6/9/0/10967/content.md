
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[quantum physics]] the _no-cloning theorem_ is the statement that there cannot be physical processes which produce "copies" of [[quantum states]] in the way known from [[classical physics]].

Quantum theoretically, this effect is ultimately due to the non-[[cartesian monoidal category|cartesian]] nature of the [[tensor product]] [[tensor product of vector spaces|of vector]]/[[tensor product of Hilbert spaces|Hilbert spaces]] [[space of quantum states|of quantum states]] ([[category theory|category theoretically]] it refers to this tensor product lacking [[natural transformation|natural]] [[diagonal morphisms]]) and as such is a direct cousin of the fundamental phenomenon of [[quantum entanglement]].

In other words when [[quantum physics]] is axiomatized by [[quantum logic]] in the guise of [[linear logic]]/[[linear type theory]], the content of "no-cloning" and "no-deleting" is the very "linearity" of this logic, the absence of a [[diagonal]] map and of a [[projection]] map for the non-[[cartesian monoidal category|cartesian]] [[tensor product]] in the [[categorical semantics]] given by non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal categories]] such as that of Hilbert spaces. See also at _[[quantum information theory via dagger-compact categories]]_.


## Details

#### Elementary explanation
 {#ElementaryExplanation}

In its original formulation, the statement of the "no-cloing theorem" is that given a quantum system with [[Hilbert space]] $H$ and with a chosen initial pure [[quantum state]] $e \in H$, then there is no [[unitary operator]] on the [[tensor product]] $H \otimes H$ which would take states of the form $(\psi, e)$ to $(\psi,\psi)$. 

Of course this cannot exist, because such a map would not even be [[linear map|linear]]. 

Often the statement is relaxed to observing that if there is a unitary that takes $(\psi,e)$ to $(\psi,\psi)$ and $(\phi,e)$ to $(\phi,\phi)$ for any two states $\phi,\psi \in H$, then either $\phi = \psi$ or $\phi \perp \psi$ (since it follows from unitarity that in this case $\langle\phi | \psi \rangle  = \langle\phi | \psi \rangle^2 $).

#### Category theoretic explanation

More [[category theory|category theoretically]], the no-cloning theorem comes down to the statement that the [[tensor product of vector spaces]] (and similarly its refinement  [[tensor product of Hilbert spaces|to Hilbert spaces]]) which makes [[VectorSpaces]] a [[symmetric monoidal category|symmetric]] [[monoidal category]]

$$
  (-) \otimes (-)
  \;\colon\;
  Vect \times Vect
  \longrightarrow
  Vect
$$

does not admit a *[[natural transformation|natural]]* transformation of the form

\[
  \label{WouldBeDiagonal}
  A \xrightarrow{\;\;} A \otimes A
\]

satisfying basic properties expected of the [[diagonal morphisms]] in a [[cartesian monoidal category]].

Without even requiring [[projection]] maps and hence "deleting" operations (which are part of a [[cartesian product]]) two such properties that the would-be diagonal (eq:WouldBeDiagonal) would have to satisfy are [[coassociativity]] and [[cocommutativity]] -- and one finds that such cannot hold in [[VectorSpaces]] &lbrack;[Abramsky (2009), Thm. 11](#Abramsky09)&rbrack;.

\begin{remark}\label{RelationToQuantumMeasurement}
**(relation to classical outcomes of [[quantum measurement]])**
\linebreak
Notice that the condition that (eq:WouldBeDiagonal) be a *[[natural transformation]]* is crucial for the above conclusion of "no cloning":

Namely, for a *fixed* [[vector space]] $\mathscr{H}$, any choice of [[linear basis]] $\big\{ \vert b \rangle \big\}_{b \colon B}$ does induce a single [[linear map]] of the required form, given by duplicating (hence "cloning") the *fixed basis* elements:

\[
  \label{CoalgebraStructureInducedByLinearBasis}
  \array{
    \mathscr{H}
      &\longrightarrow&
    \mathscr{H}
    \otimes
    \mathscr{H}
    \\
    \vert b \rangle 
      &\mapsto& 
    \vert b \rangle 
      \otimes 
    \vert b \rangle
  }
\]

On the other hand, beware that, by the laws of [[linear maps]], this means that *no other* elements except the basis elements are exactly cloned even by this operation; for example the [[superposition]] of two distinct basis elements goes to:

\[
  \label{ExampleOfNonCloningOfCoalgebraMap}
  \begin{array}{lcl}
  \vert b \rangle + \vert b' \rangle
  &\mapsto&
  \vert b \rangle \otimes \vert b \rangle
  +
  \vert b' \rangle \otimes \vert b' \rangle
  \\
  &=&
  \big(
    \vert b \rangle + \vert b' \rangle
  \big)
  \otimes
  \big(
    \vert b \rangle + \vert b' \rangle
  \big)
  \,-\,  
  \underset{correction}{
    \underbrace{
      \vert b \rangle \otimes \vert b' \rangle
      \,+\,  
      \vert b' \rangle \otimes \vert b \rangle
    }
  }
  \end{array}
\]

Nonetheless, the linear map (eq:CoalgebraStructureInducedByLinearBasis) does satisfy [[coassociativity]] and [[cocommutativity]] in the evident sense; in fact it also satisfies [[counitality]] with respect to the [[unit]] element $1 \,\coloneqq\, \underset{b \colon B}{\sum} \vert b \rangle \;\in\; \mathscr{H}$. In summary this means that (eq:CoalgebraStructureInducedByLinearBasis) defines a [[cocommutative coalgebra]]-[[structure]] on $\mathscr{H}$, which hence certainly exists on *any* ([[finite-dimensional vector space|finite-dimensional]]) [[space of quantum states]]. 

While such structures exist, they do not represent a *general* process of "cloning" of quantum states: Due to effects as in (eq:ExampleOfNonCloningOfCoalgebraMap), these structures are not [[natural transformations]] and hence they "clone" not arbitrary quantum states, but just the chosen [[linear basis]]-states that define them.

Conversely, such [[coalgebra]]-[[structure]] (at least when regarded as the special symmetric [[Frobenius algebra]]-[[structure]] to which they always extend) in fact *define* a choice of [[linear basis]] of a quantum space of states. Since such a choice may encode the set of possible classical state outcomes under a [[quantum measurement]], these "restricted cloning"-operations are also known as "[[classical structures]]" (at least in the literature on [[quantum information theory in terms of dagger-compact categories]]).

In summary: While a *natural* cloning operation on quantum states does not exist, *enforcing* one on a select [[linear basis]] of quantum states is tantamount to "turning these into classical states" (in a sense that can be made more precise, see discussion at *[[quantum reader monad]]* and *[[quantum circuits via dependent linear types]]*).

\end{remark}

\begin{remark}
**(Converse statement)**
\linebreak
One may turn the issue around asks which conditions are imposed on a [[symmetric monoidal category]] if its [[tensor product]] is assumed to admit a [[diagonal map]] (for "cloning") or [[projection]] maps (for "deleting") or both. These turn out to be very strong conditions, asserting that the category must be "essentially classical":

For instance in order for a [[diagonal]] to exist for the tensor product of a [[compact closed category]] implies that every [[endomorphism]] on every [[object]] in the category is a multiple of the [[identity]] &lbrack;[Abramsky (2009), Thm. 11](#Abramsky09) in generalization of "[Joyal's lemma](dualizing+object+in+a+closed+category#InACartesianClosedCategory)"&rbrack;. This is clearly false in any category in which one could find interesting [[quantum mechanics]], certainly in that of (finite dimensional) [[Hilbert spaces]].
\end{remark}

### No broadcasting

There is a  slightly more substantial generalization of the no-cloning theorem to [[mixed quantum states]], then called the _no-broadcasting theorem_. Dually, there is also a _no-deleting theorem_.





## Related concepts

* [[deferred measurement principle]]

* [[quantum superposition]]

* [[entanglement]]

* [[Bell's inequalities]]

* [[Gleason's theorem]]

* [[interpretation of quantum mechanics]]

* [[quantum cryptography]]

## References

The original articles:

* [[Dennis Dieks]], _Communication in EPR devices_, Physics Letters A 92, 271-272 (1982)

* [[William Wooters]], [[Wojciech Zurek]], *A single quantum cannot be cloned*, Nature **299** (1982) 802-803 &lbrack;[doi:10.1038/299802a0](https://doi.org/10.1038/299802a0)&rbrack;

See also:

* Wikipedia, _[No-cloning theorem](http://en.wikipedia.org/wiki/No-cloning_theorem)_

Discussion from the point of view of [[monoidal category]]-theory ([[quantum information theory via dagger-compact categories]]):

* {#Abramsky09} [[Samson Abramsky]], *No-Cloning in categorical quantum mechanics*, in: I. Mackie, S. Gay (eds.), *Semantic Techniques for Quantum Computation*, Cambridge University Press (2009) 1-28 &lbrack;[arXiv:0910.2401](http://arxiv.org/abs/0910.2401), [doi:10.1017/CBO9781139193313.002](https://doi.org/10.1017/CBO9781139193313.002)&rbrack;

The original suggestion to use the no-cloning theorem for [[quantum cryptography]]:

* [[Stephen Wiesner]], *Conjugate Coding* circulated in the 1960s, finally published in ACM SIGACT News **15** 1 (1083) 78–88 ([original pdf](http://users.cms.caltech.edu/~vidick/teaching/120_qcrypto/wiesner.pdf), [doi:10.1145/1008908.1008920](https://doi.org/10.1145/1008908.1008920))


[[!redirects non-broadcasting theorem]]
[[!redirects no-deleting theorem]]