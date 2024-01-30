
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of *essential fiber* of a [[functor]] is an enhancement of the naive notion of *[[fiber]]* which, for [[functors]], would violate the [[principle of equivalence]].  It is a [[category theory|category-theoretic]] version of a [[homotopy fiber]].

The essential fiber of a functor $p:E\to B$ over an [[object]] $b \in B$ can be thought of as the [[category]] of ways that $b$ can arise from applying $p$ to some object in $E$.

## Definition

\begin{definition}
\label{EssentialFiber}
For $p \colon E\to B$ be a [[functor]] and $b\in B$ an [[object]]  the **essential fiber** of $p$ over $b$ is the [[category]] whose:

* [[objects]] are [[pairs]] $(e,\phi)$ where $e\in E$ is an object and $\phi\colon p(e)\cong b$ is an [[isomorphism]],

* [[morphisms]] $(e,\phi)\to (e',\phi')$ are morphisms $f\colon e\to e'$ in $E$ such that $\phi' \circ p(f) = \phi$,

* [[composition]] operation is the evident one.

\end{definition}

\begin{remark}
The notion of essential fiber in Def. \ref{EssentialFiber} can be identified with that of the *[[pseudopullback]]* or "[[isocomma object]]" of $p$ along the functor $b\colon 1\to B$ from the [[terminal category]] which picks out the object $b$:

$$
  \array{
    E \times_B 1 
    &\longrightarrow&
    E
    \\
    \Big\downarrow 
    && 
    \Big\downarrow
    \mathrlap{{}_p}
    \\
    1 \!\!\!
    &\underset
      {b}
      {\longrightarrow}
    & 
    B
  }
$$

Moreover, the notion can also be identified with a [[homotopy fiber]] in the [[canonical model structure]] on [[Cat]].  

Finally, with [[groupoids]] identified as [[homotopy 1-types]], the essential fiber of a functor between groupoids and thought of as [[infinity-groupoids|$\infty$-groupoids]] actually coincides with its *[[homotopy fiber]]* in the classical sense of [[homotopy theory]] (well-defined up to [[weak homotopy equivalence]]).
\end{remark}


## Relationship to fibrations

If $p$ is an [[isofibration]], then any of its essential fibers (Def. \ref{EssentialFiber}) is [[equivalence of categories|equivalent]] to the corresponding strict [[fiber]].  This includes the case when $p$ is a [[Grothendieck fibration]].

On the other hand, when $p$ is a [[Street fibration]] (the version of [[Grothendieck fibration]] which respects the [[principle of equivalence]]), then essential fibers do *not* coincide with strict fibers, and essential fibers are the more useful notion.  In particular, the [correspondence](Grothendieck+construction#EquivalenceBetweenFiberedCategoriesAndPsuedofunctors) between [[Grothendieck fibrations]] and [[pseudofunctors]] only goes through for Street fibrations if one defines the pseudofunctor using essential fibers.


## Properties

Some properties of a functor are reflected in properties of its essential fibers (Def. \ref{EssentialFiber}).   A good intuition is that the more a functor resembles an [[injective function]], the simpler its essential fibers are.

+-- {: .num_prop #essential_fibers_conservative}
###### Proposition

A functor $f \colon A \to B$ is [[conservative functor|conservative]] if and only if all its essential fibers are [[groupoids]].
=--

+-- {: .num_prop #essential_fibers_faithful}
###### Proposition

If the functor $p \colon E \to B$ is [[faithful]], all its essential fibers are [[preorders]].  (The converse is not true.)
=--

and thus:

+-- {: .num_prop #essential_fibers_faithful_and_conservative_1}
###### Proposition

If the functor $p \colon E \to B$ is [[faithful functor|faithful]] and [[conservative functor|conservative]] then all its essential fibers are [[equivalence of categories|equivalent]] to [[discrete categories]].  
=--

\begin{example}
There typically is a nontrivial [[preorder]] of ways that a [[set]] can arise as the [[underlying]] set of a [[topological space]], because the [[forgetful functor]] from [[Top|$\mathrm{Top}$]] to [[Set|$\mathrm{Set}$]] is [[faithful functor|faithful]] but not [[conservative functor|conservative]].  

On the other hand, there is a mere set (i.e., a [[discrete category]]) of ways that a set can arise as the [[underlying]] set of a [[group]], because the [[forgetful functor]] from [[Grp|$\mathrm{Grp}$]] to [[Set|$\mathrm{Set}$]], being [[monadic]], is both faithful and conservative.
\end{example}

\begin{remark}
The [[automorphism group]] of $b \in B$ always [[action|acts]] on the essential fiber of $b$.

For example, on objects, $\alpha \in \mathrm{Aut}_B(b)$ acts to send $(e,\phi)$ to $(e, \alpha \circ \phi)$.  
\end{remark}


When the essential fiber is essentially a set as in proposition \ref{essential_fibers_faithful_and_conservative_1}, this allows us to describe the essential fiber as a [[union]] of [[orbits]]:

+-- {: .num_prop #essential_fibers_faithful_and_conservative}
###### Proposition

If the functor $p \colon E \to B$ is [[faithful functor|faithful]] and [[conservative functor|conservative]], the essential fiber over $b \in B$ is [[equivalence of categories|equivalent]] to the [[discrete category]] on the set
$$ 
  \coprod_e 
  \big(
  \mathrm{Aut}_B (b) 
  / 
  \mathrm{Aut}_E (e) 
  \big)
  \, 
$$
where $e \in E$ ranges over one representative of each [[isomorphism class]] in $E$ whose [[image]] is the isomorphism class of $b$.
=--

When $p \colon E \to B$ is not only faithful and conservative but also [[injective]] on [[isomorphism classes]], there is at most one [[isomorphism class]] in $E$ whose [[image]] is the isomorphism class of $b$.  Thus the [[coproduct]] in proposition \ref{essential_fibers_faithful_and_conservative} has at most one summand, and the automorphism group of $b$ acts [[transitive action|transitively]] on the relevant set:

+-- {: .num_prop #essential_fibers_faithful_conservative_injective}
###### Proposition

If the functor $p \colon E \to B$ is [[faithful]], [[conservative functor|conservative]] and it is [[injective]] on [[isomorphism classes]], then for any $e \in E$, the essential fiber over $b = f(e)$ is [[equivalence of categories|equivalent]] to the [[discrete category]] on the set
$$    
  \mathrm{Aut}_B (b) 
  / 
  \mathrm{Aut}_E (e)
  \,. 
$$
Thus $\mathrm{Aut}_B (b)$ [[action|acts]] [[transitive action|transitively]] on this set.
=--

\begin{example}
The [[forgetful functor]] from [[complex vector spaces]] to [[real vector spaces]] is faithful, conservative and injective on isomorphism classes.  The essential fiber over a given real vector space is the set of [[complex structures]] on this vector space, and if this vector space is $\mathbb{R}^{2n}$, proposition \ref{essential_fibers_faithful_conservative_injective} implies that this set of complex structures is isomorphic to (the [[underlying]] set of) the [[coset space]]
$$     
  \mathrm{GL}(2n,\mathbb{R})/\mathrm{GL}(n,\mathbb{C})
\,.
$$
\end{example}

## Related entries

* [[fiber]]

* [[homotopy fiber]]

* [[fibered category]]

## References

The above results on essential fibers were proved in this discussion:

* Category Theory Community Server: *[Homotopy fibers](https://categorytheory.zulipchat.com/#narrow/stream/266967-general.3A-mathematics/topic/homotopy.20fibers/near/353365094)* (2023)

[[!redirects essential fibre]]
[[!redirects essential fibers]]
[[!redirects essential fibres]]
