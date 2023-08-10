

### Relation between adjunctions and monads
 {#RelationBetweenAdjunctionsAndMonads}

There is a close relation between [[adjunctions]] ([[adjoint functors]]) and [[monads]]:

* [Monad induced by an adjunction](#MonadInducedByAnAdjunction)

* [Category of adjunction-resolutions of a monad](#CategoryOfAdjunctionResolutionsOfAMonad)

* [Semantics-Structure adjunction](#SemanticsStructureAdjunction)


#### Monad induced by an adjunction
 {#MonadInducedByAnAdjunction}

Every [[adjunction]] $(L \dashv R)$ induces a [[monad]] $R \circ L$ and a [[comonad]] $L \circ R$.

([Huber 1961, §4](monad#Huber61); see eg. [MacLane 1971, §VI.1 (p 134)](monad#MacLane71); [Borceux 1994, vol. 2, prop. 4.2.1](monad#Borceux94)).


In detail:

\begin{proposition}

Let $(\mathcal{C},\mathcal{D},F,U,\eta,\epsilon)$ be a pair of [[adjoint functors]] ie $F \dashv U$ are adjoint functors where $F \colon \mathcal{C} \rightarrow \mathcal{D}$, $U \colon\mathcal{D} \rightarrow \mathcal{C}$, $\eta_{A}:A \rightarrow U(F(A))$ is the [[unit of an adjunction|unit]] and $\epsilon_{B} \colon F(U(B)) \rightarrow B$ is the [[counit of an adjunction|counit]]. Then:

* $U \circ F$ is a [[monad]] on $\mathcal{C}$, with [[unit of a monad|unit]] $\eta$ and multiplication $U(\epsilon_{F(A)}):U(F(U(F(A)))) \rightarrow U(F(A))$.

* $F \circ U$ is a [[comonad]] on $\mathcal{D}$, with [[counit of a comonad|counit]] $\epsilon$ and comultiplication $F(\eta_{U(B)}):F(U(B)) \rightarrow F(U(F(U(B))))$.

\end{proposition}
\begin{proof}

We verify that we obtain a monad, the argument for the comonad is [[formal duality|formally dual]].

**(1)**
We know that this diagram commutes:

\begin{tikzcd}
  F(A) 
  \arrow[r, "F(\eta_{A})"] 
  \arrow[rd, "="'] 
  & 
  F(U(F(A)) 
  \arrow[d, "\epsilon_{F(A)}"] 
  \\
  & F(A)                                  
\end{tikzcd}
By applying $U$, we obtain the first part of the unitaly of the monad:
\begin{tikzcd}
U(F(A)) \arrow[r, "U(F(\eta_{A}))"] \arrow[rd, "="'] & U(F(U(F(A))) \arrow[d, "U(\epsilon_{F(A)})"] \\
                                                     & U(F(A))                                     
\end{tikzcd}

**(2)**
We know that this diagram commutes:
\begin{tikzcd}
U(B) \arrow[r, "\eta_{U(B)}"] \arrow[rd, "="'] & U(F(U(B))) \arrow[d, "U(\epsilon_{B})"] \\
                                               & U(B)                                   
\end{tikzcd}
By putting $B=F(A)$, we obtain the second part of the unitality of the monad:
\begin{tikzcd}
U(F(A)) \arrow[r, "\eta_{U(F(A))}"] \arrow[rd, "="'] & U(F(U(F(A)))) \arrow[d, "U(\epsilon_{F(A)})"] \\
                                                     & U(F(A))
\end{tikzcd}

**(3)**
The naturality of $\epsilon$ is written, for every $f:B \rightarrow B'$:

\begin{tikzcd}
F(U(B)) \arrow[d, "F(U(f))"'] \arrow[r, "\epsilon_{B}"] & B \arrow[d, "f"] \\
F(U(B')) \arrow[r, "\epsilon_{B'}"']                    & B'              
\end{tikzcd}

We apply it to $f=\epsilon_{F(A)}$ and it gives:

\begin{tikzcd}
F(U(F(U(F(A))))) \arrow[d, "F(U(\epsilon_{F(A)}))"'] \arrow[r, "\epsilon_{F(U(F(A)))}"] & F(U(F(A))) \arrow[d, "\epsilon_{F(A)}"] \\
F(U(F(A))) \arrow[r, "\epsilon_{F(A)}"']                                                & F(A)                                   
\end{tikzcd}

Finally apply $U$ to this diagram to obtain:

\begin{tikzcd}
U(F(U(F(U(F(A)))))) \arrow[d, "U(F(U(\epsilon_{F(A)})))"'] \arrow[r, "U(\epsilon_{F(U(F(A)))})"] & F(U(F(A))) \arrow[d, "U(\epsilon_{F(A)})"] \\
U(F(U(F(A)))) \arrow[r, "U(\epsilon_{F(A)})"']                                                   & U(F(A))                                   
\end{tikzcd}

which is exactly the associativity of the multiplication of the monad.

**(4)**
The naturality of the multiplication $U(\epsilon_{F(A)}):U(F(U(F(A)))) \rightarrow U(F(A))$ is obtained by two [[whiskerings]] of the counit $\epsilon_{B}:U(F(B)) \rightarrow B$.
\end{proof}

#### Category of adjunction-resolutions of a monad
 {#CategoryOfAdjunctionResolutionsOfAMonad}

An adjunction inducing a monad $T$ (as [above](#MonadInducedByAnAdjunction)) is also called a *resolution of $T$*. 

There is in general more than one such resolution, in fact there is a [[category]] of adjunctions for a given monad whose morphisms are "[[comparison functors]]" (eg. [MacLane 1971, §VI.3](#MacLane71)).

In this category:

* the [[initial object]] is the adjunction over the [[Kleisli category]] of the monad;

* the [[terminal object]] is that over the [[Eilenberg-Moore category]] of algebras, also called the _[[monadic adjunction]]_ (recognized by *[[monadicity theorems]]*). 

(e.g. [Borceux 1994, vol. 2, prop. 4.2.2](monad#Borceux94)) 


#### Semantics-structure adjunction
 {#SemanticsStructureAdjunction}

The above passage from [[adjunctions]] to [[monads]] and back to their [[monadic adjunctions]] constitutes itself an [[adjunction]], sometimes called the _[[semantics-structure adjunction]]_.



