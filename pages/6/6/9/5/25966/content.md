\tableofcontents 

## Idea 

In [[logic]], particularly in the syntactic notion of a (first-order) [[theory]], a *constant* is a term without free variables, modulo equivalence imposed by equational axioms of the theory. 

## Definition 

Recall that a [[signature]] $\Sigma$ of a theory (let us say a one-sorted theory, for the sake of simplicity) consists of constant symbols together with function symbols and relation symbols with assigned arities. Then 

* A constant symbol $c$ of $\Sigma$ is considered a constant of the theory, and 

* If $f$ is a function symbol of arity $n$ and $c_1, \ldots, c_n$ are constants, then $f(c_1, \ldots, c_n)$ is a constant of the theory. 

[Note that in some accounts, constant symbols are considered as function symbols of arity $0$.] 

For instance, the theory of rings is typically presented by a signature $(R, +, -, \cdot, 0, 1)$ where $R$ denotes the sort, with binary operations $+, -, \cdot$ and constant (symbols) $0, 1$, whence other constants may be derived such as $(1 + 1) \cdot ((0-1) -1)$. 

This description is somewhat imprecise; for example, the equational axioms of ring theory force equations like 

$$(1 + 1) \cdot ((0-1) -1) = 0 - (1 + ((1 + 1) + 1))$$ 

so that what one is really after is equivalence classes of syntactic expressions. 