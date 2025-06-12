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

