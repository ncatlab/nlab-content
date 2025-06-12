## Idea 

The notion of skew lattice is that of [[lattice]] (as an algebraic structure $(L, \wedge, \vee)$), except that commutativity axioms are dropped. 

## Definition 

A *skew lattice* is a set $L$ equipped with two [[associative operations]] $\vee, \wedge$ that satisfy the following versions of absorption laws: 

$$x \wedge (x \vee y) = x = (y \vee x) \wedge x, \qquad x \vee (x \wedge y) = x = (y \wedge x) \vee x.$$ 

Observe that the notion of skew lattice is self-dual: a statement in the language of skew lattices holds iff the dual statement, obtained by swapping all instances of $\wedge$ with $\vee$ and vice-versa, also holds. 

## Properties 

\begin{proposition} 
In a skew-lattice, every element $x$ satisfies $x \wedge x = x$. Dually, $x \vee x = x$. 
\end{proposition} 

\begin{proof} 
We have 

$$x = x \wedge (x \vee (x \wedge x)) = x \wedge x$$ 

where the first equation is from the first absorption law and the second equation is from the second absorption law. 
\end{proof} 

It follows that a skew lattice is a [[band]] under either operation $\wedge$, $\vee$. Accordingly (see there), there is a natural preorder structure definable from either operation; call them $\preceq_\wedge$ and $\preceq_\vee$. These two preorder structures are opposite to one another, by the following results: 

\begin{lemma} 
In a skew lattice, $x = x \wedge y$ iff $y = x \vee y$. Similarly, $y = x \wedge y$ iff $x = x \vee y$. 
\end{lemma} 

\begin{proof} 
Immediate from the absorption laws. 
\end{proof}

\begin{proposition} 
In a skew lattice, we have $x \preceq_\wedge y$ iff $y \preceq_\vee x$. 
\end{proposition} 

\begin{proof} 
The two relations mean, by definition, $x = x \wedge y \wedge x$ and $y = y \wedge x \wedge y$. We are to show that these are equivalent. By duality, only the forward implication needs to be proven. 

By hypothesis $x = x \wedge (y \wedge x)$ and the lemma, we have $y \wedge x = x \vee (y \wedge x)$. Denote the last equation by $E$. 

Then 

$$\array{  
y \vee x & = & 
(y \vee x) \wedge ((y \vee x) \vee (y \wedge x)) 
& (absorption) \\
& = & 
(y \vee x) \wedge (y \vee (x \vee (y \wedge x)) 
& (associativity\; of\; \vee) \\ 
& = & (y \vee x) \wedge (y \vee (y \wedge x)) 
& (by\; E) \\ 
& = & (y \vee x) \wedge y & (absorption)
}$$ 

Then, from $y \vee x = (y \vee x) \wedge y$ and the lemma, we have $(y \vee x) \vee y = y$, as was to be shown. 
\end{proof} 