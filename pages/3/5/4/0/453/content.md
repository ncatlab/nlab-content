A _regular category_ is a finitely complete category which admits a good notion of [[image]] factorization. A primary _raison d'etre_ behind regular categories $C$ is to have a decently behaved _calculus of relations_ in $C$. 

## Definition

A category $C$ is **regular** if 

* It is finitely complete; 

* The _kernel pair_ $p_1, p_2: e \stackrel{\to}{\to} d$ of any $f: d \to c$ admits a coequalizer; 

Here the "kernel pair" is the parallel pair of projection maps coming out of a pullback $e$ of the diagram 

$$d \stackrel{f}{\to} c \stackrel{f}{\leftarrow} d$$

The kernel pair is always an internal [[equivalence relation]] on $d$ in $C$; informally, $\ker(f)$ is the subobject of $d \times d$ consisting of pairs of elements which have the same value under $f$. The coequalizer above is supposed to be the "object of equivalence classes" of the equivalence relation $\ker(f)$. 

A map which is the coequalizer of its own kernel pair is called a _regular epi_. In fact, in any category satisfying the first two conditions above, every coequalizer is the coequalizer of its kernel pair. (See for instance Paul Taylor's Practical Foundations of Mathematics, Lemma 5.6.6.) 

Here is the last condition for a category to be regular: 

* The pullback of a regular epi along any map is a regular epi. 

(To be continued...)