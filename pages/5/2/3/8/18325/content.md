# Contents 
* table of contents
{:toc} 

## Fillers of commutative squares 

If

$$ \array {
O_{0,1} & \overset{f_1}{\longrightarrow} & O_{1,1} \\
\downarrow h_0 & & \downarrow h_1 \\
O_{0,0} & \overset{f_0}{\longrightarrow} & O_{1,0} \\
}
$$

is a commutative diagram in a category $\mathcal{C}$, then a _filler_ (synonyms:  *diagonal fill-in*, [[lift]]) is:

* morphism $j\colon O_{0,0}\rightarrow O_{1,1}$ in $\mathcal{C}$ making both triangles created commute. 
(That is, $f_0 = h_1 j$ and $f_1 = j h_0$.)

In certain contexts, the problem of whether there exists a filler in this sense is called a *lifting problem*.

If $j$ is uniquely determined (in an appropriate sense), then $h_0$ is said to be _orthogonal_ to $h_1$: see [[orthogonality]]. 

The concept of filler plays an important role in homotopy theory; see for example [[model category]]. 

## Horn fillers for simplicial sets 

The term is used in the context of [[horns]] in simplicial sets and related structures. The term makes it possible to summarize the definition of a [[Kan complex]] in one sentence: a Kan complex is a simplicial set in which every horn has a filler. 

Of course this is a special case of the preceding notion of filler: a horn filler for a horn $f: \Lambda_n^j \to X$ in a simplicial set $X$ is a diagonal fill-in of a commutative square 

$$\array{
\Lambda_n^j & \hookrightarrow & \Delta_n \\ 
\mathllap{f} \downarrow & & \downarrow \\ 
X & \to & 1
}$$ 

going from $\Delta_n$ to $X$. 


## Related concepts  

[[factorization system]]

[[homotopy lifting property]]

[[orthogonality]]


[[!redirects fill-in]]
[[!redirects diagonal fill-in]]