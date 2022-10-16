asd 

Let $\VBun$ be the category having objects pairs $(M,V)\in\Man\times\Man$ where $q:V\longrightarrow M$ is a [[vector bundle|vector bundle]] over $M$. A morphism $(M_{1},V_{1})\longrightarrow (M_{2},V_{2})$ is a [[commutative square|commutative square]]: 

\begin{center}
\begin{tikzcd}
V_{1} \arrow[r, "g"] \arrow[d, "q_{1}"'] & V_{2} \arrow[d, "q_{2}"] \\
M_{1} \arrow[r, "f"']                    & M_{2}                   
\end{tikzcd}
\end{center}

where $f$ is a smooth map, and $g$ is a smooth map such that $g\mid_{q_{1}^{-1}(m)}:q_{1}^{-1}(m)\longrightarrow q_{2}^{-1}(f(m))$ is linear for every $m\in M_{1}$. Composition is given as in the [[arrow category|arrow category]]. There is a forgetful functor $\mathcal{P}:\VBun\longrightarrow\Man$ which projects onto the base data. To see that this functor is a Grothendieck fibration, first consider a morphism of the form: 

\begin{center}
\begin{tikzcd}
f^{*}M_{2} \arrow[r] \arrow[d] & V_{2} \arrow[d, "q_{2}"] \\
M_{1} \arrow[r, "f"']                      & M_{2}                   
\end{tikzcd}
\end{center}

given by the [[pullback bundle|pullback bundle]] of a vector bundle $V_{2}\longrightarrow M_{2}$ along a smooth map $M_{1}\longrightarrow M_{2}$. Certainly, the [[universal construction|universal property]] of the [[pullback|pullback]] will supply the conditions for this square to define a [[Cartesian morphism|cartesian morphism]] in $\VBun$ with respect to the the functor $\mathcal{P}$. We show that these are in fact all the cartesian morphisms in $\VBun$.

Let $e' = (V_{1},M_{1})$, $e = (V_{2},M_{2})$, and $e'' = (V,M)$, then by applying the definition from above directly, we see that a morphism $\phi:e'\longrightarrow e$ in $\VBun$, i.e., a square:

\begin{center}
\begin{tikzcd}
V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M_{1} \arrow[r]                    & M_{2}                   
\end{tikzcd}
\end{center}

is cartesian, if given any morphism $\psi:e''\longrightarrow e$ in $\VBun$, i.e., a square (which we draw around the first):

\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"']   &                           &                 \\
                                      & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}

and any morphism $g:\mathcal{P}(e'')\longrightarrow \mathcal{P}(e')$ in $\Man$ such that $\mathcal{P}(\phi)\circ g = \mathcal{P}(\psi)$, i.e. a smooth map $g:M\longrightarrow M_{1}$ that fills in the above diagram to a commuting diagram:

\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"']             &                           &                 \\
                                                & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] \arrow[r, "g"] & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}

then there exists a unique morphism $\chi:e''\longrightarrow e'$ in $\VBun$ such that $\psi = \phi\circ\chi$ and $\mathcal{P}(\chi) = g$, i.e., there exists a unique morphism $V\longrightarrow V_{1}$ that further fills the diagram to a commuting diagram:
\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"'] \arrow[rd, dashed] &                           &                 \\
                                                       & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] \arrow[r, "g"]        & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}

It immediately follows from the above unfolding of the definition that $\VBun(e'',e')\cong\VBun(e'',p)$ naturally in $e''$, where $p$ is the pullback bundle of $V_{2}\longrightarrow M_{2}$ along $M_{1}\longrightarrow M_{2}$, and thus by the [[Yoneda lemma#YonedaCorollaries|Yoneda lemma]] $e'\cong p$, and thus $V_{1}\cong\mathcal{P}(e')^{*}V_{2}$. Note that the isomorphisms $e'\cong p$ preserve the commutativity of the diagrams we have drawn above by the universal property of the pullback, and by the definition of a cartesian morphism. Now that we have identified the cartesian morphisms, the statement that $\mathcal{P}:\VBun\longrightarrow\Man$ is a Grothendieck fibration is equivalent to the statement that vector bundles can be pulled back along smooth maps. This is of course true, and thus $\mathcal{P}:\VBun\longrightarrow\Man$ is a Grothendieck fibration.

The associated functors $f^{*}$ are the [[pullback#PullbackFunctor|pullback psuedofunctors]] $f^{*}:\VBun_{M_{2}}\longrightarrow \VBun_{M_{1}}$ that pullback vector bundles over a manifold $M_{2}$ to vector bundles over a manifold $M_{1}$ along a smooth map $f:M_{1}\longrightarrow M_{2}$.

## Test

| [[logic]] | [[set theory]] | [[category theory]] | [[type theory]] |
|-----------|---------------------|-----------------|-----------------|
| [[true]]  | [[singleton]] | [[terminal object]]/[[(-2)-truncated object]] | [[h-level 0]]-[[type]]/[[unit type]] | 
| [[false]] | [[empty set]] | [[initial object]] | [[empty type]] |
| [[proposition]], [[truth value]] | [[subsingleton]] | [[(-1)-truncated object]] | [[h-proposition]], [[mere proposition]] |
| [[proof]] | [[element]] | [[generalized element]] | [[program]] |
| [[cut rule]] |  | [[composition]] of [[classifying morphisms]] / [[pullback]] of [[display maps]] | [[substitution]] |
| [[cut elimination]] for [[implication]] | | [[counit]] for hom-tensor adjunction | [[beta reduction]] |
| introduction rule for [[implication]] | | [[unit]] for hom-tensor adjunction | [[eta conversion]] |
| [[logical conjunction]] | [[cartesian product]] of [[subsingletons]] |[[product]] | [[product type]] |
| [[disjunction]] | [[support]] of [[disjoint union]] of [[subsingletons]] |[[coproduct]] ([[(-1)-truncation]] of) | [[sum type]] ([[bracket type]] of) |
| [[implication]] | [[function set]] of [[subsingletons]] | [[internal hom]] | [[function type]] |
| [[negation]] | [[function set]] into [[empty set]] | [[internal hom]] into [[initial object]] | [[function type]] into [[empty type]] |
| [[universal quantification]] | indexed [[cartesian product]] | [[dependent product]] | [[dependent product type]] |     
| [[existential quantification]] | [[support]] of indexed [[disjoint union]] | [[dependent sum]] ([[(-1)-truncation]] of) | [[dependent sum type]] ([[bracket type]] of) |
| | [[equivalence]] |[[path space object]] | [[identity type]]/[[path type]] |
|  | [[support]] | [[support object]] | [[propositional truncation]]/[[bracket type]]
| | [[equivalence class]] | [[quotient]] | [[quotient type]] |
| | [[induction]] | |[[colimit]] | [[inductive type]], [[W-type]], [[M-type]] |
| | higher [[induction]] | [[(infinity,1)-colimit|higher colimit]] | [[higher inductive type]] |
| - | |  [[0-truncated]] [[(infinity,1)-colimit|higher colimit]] | [[quotient inductive type]] |
| [[coinduction]] | |[[limit]] | [[coinductive type]] |
| [[preset]] | | | [[type]] without [[identity types]] |
| | [[completely presented set]] | [[discrete object]]/[[0-truncated object]]  | [[h-level 2]]-[[type]]/[[set]]/[[h-set]] |
| | [[set]] | [[groupoid object in an (infinity,1)-category|internal 0-groupoid]] | [[Bishop set]]/[[setoid]] with its [[pseudo-equivalence relation]] an actual [[equivalence relation]] |
| | [[set]] of [[truth values]] | [[subobject classifier]] | [[type of propositions]] |
| | [[universe]] | [[object classifier]] | [[type universe]] |
| [[modality]] |  |[[closure operator]], ([[idempotent monad|idempotent]]) [[monad]] | [[modal type theory]], [[monad (in computer science)]] |
| [[linear logic]] |  |([[symmetric monoidal category|symmetric]], [[closed monoidal category|closed]]) [[monoidal category]] | [[linear type theory]]/[[quantum computation]] |
| [[proof net]] |  |[[string diagram]] | [[quantum circuit]] |
| (absence of) [[contraction rule]] | | (absence of) [[diagonal]] | [[no-cloning theorem]] |
| | | [[synthetic mathematics]]  |  [[domain specific embedded programming language]] |