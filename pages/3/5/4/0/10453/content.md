
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### On Hilbert spaces

A _positive operator_ is a [[linear operator]] $A$ on a [[Hilbert space]] $(H, \langle -,-\rangle)$ such that the [[quadratic form]]

$$
  v \mapsto \langle v, A v\rangle
$$

for $v \in H$ is [[quadratic form|positive semi-definite]].

+-- {: .num_prop}
###### Proposition

Every positive operator $A$ on a Hilbert space is [[self-adjoint operator|self-adjoint]].

=--

+-- {: .proof}
###### Proof
Let $B = \frac{1}{2}(A + A^\dagger)$ and $C = \frac{1}{2}i(A^\dagger - A)$.
Then $B$ and $C$ are self-adjoint, and $A = B + iC$.  Now, $\langle v, A v \rangle = \langle v, B v \rangle + i \langle v, C v \rangle$ is real for any $v$, so $\langle v, C v \rangle = 0$ for all $v$.  Hence $C = 0$ and $A = B$.
=--

### In $C^\ast$-algebras

More generally:

+-- {: .un_defn}
###### Definition
An element $A$ of an (abstract) [[C*-algebra]] is called **positive** if it is [[self-adjoint operator|self-adjoint]] and its [[spectrum of an operator|spectrum]] is contained in $[0, \infinity)$.
=--

Here, 'positive' means positive semidefinite; see at [[inner product]] for the family of variations of this notion.  (The relevant inner product here is that associated with the quadratic form above: $v, w \mapsto \langle v, A w\rangle$.)

An element $a \in A$ is positive if and only if it is of the form $a = b^* b$. This statement is not true for more general [[star-algebra|*-algebras]] over the complex numbers.

### In dagger-categories

Yet more generally, in a [[dagger category]] a [[morphism]] $f$ is positive if it is of the form $f = g^\dagger \circ g$ for some morphism $g$.

(eg. [Selinger 2005 Def. 4.1](#Selinger05))


## Related concepts

* [[positive operator valued measure]]

* [[normal operator]]

* [[self-adjoint operator]]

* [[state on an operator algebra]]

* [[density matrix]]

* [[quantum effect]]

* [[quantum operation]]

## References

Discussion in [[dagger-compact categories]] with an eye twoards [[completely positive maps]] on spaces of [[density matrices]]:

* {#Selinger05} [[Peter Selinger]], *Dagger-compact closed categories and completely positive maps*, Electronic Notes in Theoretical Computer Science, **170** (2007) 139-163 &lbrack;[doi:10.1016/j.entcs.2006.12.018](https://doi.org/10.1016/j.entcs.2006.12.018), [[SelingerPositiveMaps.pdf:file]]&rbrack;



[[!redirects positive operator]]
[[!redirects positive operators]]

[[!redirects positive linear operator]]
[[!redirects positive linear operators]]
