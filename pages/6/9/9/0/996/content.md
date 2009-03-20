# Definition

A __generator__ in a category $C$ is an object $S$ such that the functor $h^S = C(S,-) : C\to\mathrm{Set}$ is [[faithful functor|faithful]]. This means that for any pair $f_1,f_2\in C(X,Y)$
there is a morphism $\theta\in C(S,X)$ which distinguishes
them in the sense that $f_1\circ\theta=f_2\circ\theta$.

One often extends this notion to a _generating family_ of objects, which is a (usually small) set $\lbrace S_a, a\in A\rbrace$ of objects in $C$ such that the family $C(S_a,-)$ is jointly faithful, that is for any pair $f_1,f_2\in C(X,Y)$
there is an $a\in A$ and a morphism $\theta\in C(S_a,X)$ which distinguishes them in the sense that 
$f_1\circ\theta=f_2\circ\theta$.

The dual notion is [[cogenerator]].


# Examples and applications

The standard example of a generator in the category of $R$-modules over a ring $R$ is any free module $R^I$ and $R$ in particular. If a generator is a finitely generated [[projective object]] in the category of $R$-modules, then we say that it is a progenerator. Progenerators are important in classical Morita theory, see [[Morita equivalence]].

+--{: .query}
[[Mike Shulman|Mike]]: The term "progenerator" seems unfortunate to me; it sounds to me like a [[pro-object]] that is a generator.  Is it well-established?  I've never heard it, though I have heard "projective generator" in the context of Morita theory.
=--

The existence of a small generating family is one of the conditions in [[Giraud's theorem]] characterizing [[Grothendieck topos]]es.

The existence of a small (co)generating family is one of the conditions in one version of the [[adjoint functor theorem]].


# Strengthened generators

If $C$ is [[locally small category|locally small]] and has small [[coproduct]]s, then a family $\{S_a\}_{a\in A}$  is a generating family if and only if for every $X\in C$, the canonical morphism
$$ \varepsilon_X: \coprod_{a\in A, f:S_a\to X} S_a \longrightarrow X $$
is an [[epimorphism]].

More generally, if $\mathcal{E}$ is a subclass of epimorphisms, we say that $\{S_a\}$ is an **$\mathcal{E}$-generator** if each morphism $\varepsilon_X$ is in $\mathcal{E}$.

Of particular importance is the notion of **strong generator** which is obtained by taking $\mathcal{E}$ to be the class of [[strong epimorphism]]s.  This can be expressed equivalently, without requiring local smallness or the existence to coproducts, by saying that  the family $C(S_a,-)$ is jointly faithful and jointly [[conservative functor|conservative]].

If the inclusion of the full subcategory on the objects $\{S_a\}$ is [[dense functor|dense]], sometimes $\{S_a\}$ is said to be a **dense generator**.  This is the strongest sort of generator.
