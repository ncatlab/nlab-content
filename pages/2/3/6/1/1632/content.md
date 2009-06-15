A Banach algebra is a (usually associative, but often non-unital) algebra in the category of [[Banach space]]s. This means a Banach space $A$ equipped with a multiplication map 

$$m: A \otimes A \to A$$ 

where $\otimes$ is the standard tensor product for the symmetric monoidal closed category of Banach spaces, which again is usually taken to be associative. 

Since the norm of $a \otimes b \in A \otimes A$ is $\|a\| \cdot \|b\|$ where $\|a\|$ is the norm in $A$, and since morphisms in the category of Banach spaces are taken to be bounded linear maps of norm is $\leq 1$, it is automatic that 

$$\|a \cdot b\| \leq \|a\| \cdot \|b\|$$ 

where $a \cdot b = m(a, b)$. 

## Examples 

* A standard example is $L^1(\mathbb{R}, \mu)$, where $\mu$ is Lebesgue measure, and where the multiplication is taken to be convolution. This lacks a unit for the multiplication, since there is no $L^1$ function $e(x)$ that represents the Dirac functional 
$$f \mapsto f(0) = \int e(x)f(x) d\mu$$ 
on continuous functions $f: X \to \mathbb{C}$. (Of course, in the non-unital case, one can always formally adjoin a unit $e$, forming the Banach algebra $L^1 \oplus \langle e \rangle$ where $\|e\| = 1$.) One can generalize this example in straightforward fashion, replacing $\mathbb{R}$ by any [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological group]] $G$, and $\mu$ by a [[Haar measure]] on $G$. 

* For any [[measure space]] $(X, \mu)$, $L^{\infty}(X, \mu)$ is a unital Banach algebra with respect to pointwise multiplication. 

* If $A$ is a Banach space, the [[internal hom]] $hom(A, A)$ is a unital Banach algebra. 

* Any $C^*$-algebra is a Banach algebra. 
