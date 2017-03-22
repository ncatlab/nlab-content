__Goldblatt-Thomason theorem__ is a theorem in [[modal logic]] which characterizes the elementary classes which are also modally definable classes. It says that if $K$ is an elementary class of Kripke frames, then $K$ is modally definable iff $K$ is closed under taking bounded morphic images, generated subframes, disjoint unions, and reflects ultrafilter extensions.

## Idea ##
The theorem is based on the duality between the category of [[Boolean algebras]] and Sets

$$
BA \stackrel{\overset{\Pi}{\leftarrow}}{\underset{\Sigma}{\to}} Set^{op}
$$

where $\Pi$ is the power set functor and $\Sigma$ assigns to a Boolean algebra the set of its [[ultrafilters]]. $\Sigma$ is left-adjoint to $\Pi$, but in general they do not form a dual equivalence of categories. This only holds in the finite case, where it is enough for $\Sigma$ to assign to a Boolean algebra the set of its atoms.

The idea of the proof is to translate between [[Kripke frames]] and Modal algebras, and obtain the above result by an application of [[Birkhoff's HSP theorem]].


## References ##

* _Brief summary of Goldblatt-Thomason theorem_, [pdf](https://users.soe.ucsc.edu/~btencate/esslli08course/esslli-fri1.pdf)

* _The Goldblatt-Thomason Theorem for Coalgebras_, [pdf](http://www.cs.le.ac.uk/people/akurz/Papers/CALCO-07/GTthm.pdf)


category: logic