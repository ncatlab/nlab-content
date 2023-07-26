\tableofcontents 

## Idea 

In [[logic]], particularly in the syntactic notion of a (first-order) [[theory]], a *constant* is a term without free variables, modulo equivalence imposed by equational axioms of the theory. 

## Definition 

Recall that a [[signature]] $\Sigma$ of a theory (let us say a one-sorted theory, for the sake of simplicity) consists of constant symbols together with function symbols and relation symbols with assigned arities. Then 

* A constant symbol $c$ of $\Sigma$ is considered a constant term of the theory, and 

* If $f$ is a function symbol of arity $n$ and $c_1, \ldots, c_n$ are constant terms, then $f(c_1, \ldots, c_n)$ is a constant term of the theory. 

[Note that in some accounts, constant symbols are considered as function symbols of arity zero.] 

For instance, the theory of rings is typically presented by a signature $(R, +, -, \cdot, 0, 1)$ where $R$ denotes the sort, with binary operations $+, -, \cdot$ and constant (symbols) $0, 1$, whence other constant terms may be derived such as $(1 + 1) \cdot ((0-1) -1)$. 

Constant terms are syntactic expressions derived from the signature, but the axioms of the theory may impose equations between constant terms; for example, the equational axioms of ring theory force equations like 

$$(1 + 1) \cdot ((0-1) -1) = 0 - (1 + ((1 + 1) + 1))$$ 

so that what one is really after is equivalence classes of syntactic expressions. A *constant* of the theory is such an equivalence class of constant terms. 

\begin{example} 
Let $R$ be a fixed commutative ring. The theory of $R$-algebras may be presented just as the theory of rings, but including a constant symbol $c_r$ for each element $r \in R$, and adding equations $c_0 = 0$, $c_1 = 1$, $c_r + c_s = c_{r+s}$, $c_{r-s} = c_r - c_s$, and $c_r \cdot c_s = c_{r s}$. 
\end{example} 

## Constants of algebraic theories 

For a more semantic description, suppose $T$ is a [[Lawvere theory]], and let 

$$Set^T = \mathbf{Prod}(T, Set)$$ 

denote the category of $T$-algebras = [[product-preserving functors]] $T \to Set$. Then there is a forgetful functor 

$$U: Set^T \to Set,$$ 

and constants of $T$ may be identified, up to natural isomorphism, with natural transformations of the form 

$$1 \to U$$ 

(where $1 = U^0$ here denotes the terminal functor $Set^T \to Set$). Alternatively, constants of $T$ may be naturally identified with morphisms in the hom-set $T(i(0), i(1))$ where $i: FinSet^{op} \to T$ is the product-preserving functor given as one of the data for $T$. 

The same idea applies to any infinitary [[algebraic theory]]. 

From this point of view, identifying (equivalence classes of) $n$-ary operations of $T$ with natural transformations $f: U^n \to U$, one also often says that $f$ is constant if it factors through the unique map $U^n \to 1$, as in [[constant morphism]]. 

For example, for the Lawvere theory of commutative $R$-algebras, $n$-ary operations $U^n \to U$ are in natural bijection with polynomials $p \in R[x_1, \ldots, x_n]$, and such a $p$ is constant iff it belongs to the image of the canonical inclusion map $R \to R[x_1, \ldots, x_n]$. See also [[constant polynomial]]. 
