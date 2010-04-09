#Contents#
* automatic table of contents goes here
{:toc}

## Idea
An __operator algebra__ is any subalgebra of the algebra of continuous linear operators on a [[topological vector space]], with composition as the multiplication. In most cases, the space is a separable [[Hilbert space]], and most attention historically has been paid to algebras of bounded linear operators. The operator algebras themselves are often equipped with their own topologies (e.g. norm topology, weak topology, weak$^*$ topology and so on) and sometimes involution. __$C^*$-[[C-star algebra|algebras]]__ are (in the complex case) norm-closed complex $*$-[[subalgebras]] of the algebra of the bounded linear operators on a Hilbert space. They can be however characterized structurally as a $*$-[[representation]] of a [[Banach algebra]] with involution satisfying some compatibility conditions; the latter could be called abstract $C^*$-algebras (or sometimes $B^*$-algebras). Every _commutative_ unital $C^*$-algebra can be realized as an algebra of functions on a Hausdorff compact space, which is obtained as its [[Gel'fand spectrum]].

Special class of $C^*$-algebras are __[[von Neumann algebra|von Neumann]]__ or $W^*$-algebras (see [wikipedia](http://en.wikipedia.org/wiki/Von_Neumann_algebra)), which are (in the complex case) _weakly closed_ (closed in the weak topology) $*$-subalgebras of the algebra of bounded linear operators on a Hilbert space. In structural theory, an important role among von Neumann algebras is played by so-called factors, characterized by the property that their center is trivial ($1$-dimensional, consisting of "scalars"). 

Operator algebras play major roles in [[functional analysis]], [[representation theory]], [[noncommutative geometry]] and [[quantum field theory]]. 

## Topics of interest for the understanding of AQFT
This paragraph will collect some facts of interest for the aspects of [[AQFT]] in the nLab. Unless stated otherwise all operator algebras will be assumed to be unital, i.e. having an identiy denoted by $\mathbb{1}$.

###States {#statesOfOperatorAlgebras}
The Heisenberg picture is sometimes formalized by describing the observables of a quantum system by an operator algebra, and the state of the system as a state of the algebra. The first "state" in the preceding sentence is the state the described physical system is in, the second one is the mathematical counterpart we are about to define, that inherited it's name from the physical concept.

* Definition: An operator A on a Hilbert space is called **positive** if it is self-adjoint and its spectrum is contained in $[0, \infinity)$. We write $A \ge 0$ and say that the set of all positive operators is the positive cone (of a given operator algebra).

* Definition: A linear functional $\rho$ of an operator algebra is **positive** if $A \ge 0$ implies that  $\rho(A) \ge 0$.

* Definition: A **state** of an unital operator algebra is linear functional $\rho$ such that $\rho$ is positive and $\rho(\mathbb{1}) = 1$.

Though the mathematical notion of state is already close to what physicists have in mind, they usually restrict the set of states further and consider normal states only. We let $\mathcal{R}$ be an operator algebra and $\pi$ an representation of $\mathcal{R}$ on a Hilbert space $\mathcal{H}$.
 
Combined definition and theorem: A **normal state** $\rho$ is a state that satisfies one of the following equivalent conditions (this list is not complete, i.e. there are more equivalent characterizations of normal states):

* $\rho$ is weak-operator continuous on the unit ball of $\pi(\mathcal{R})$.

* $\rho$ is strong-operator continuous on the unit ball $\pi(\mathcal{R})$.

* $\rho$ is ultra-weak continuous.

* There is an operator A of trace class of $\mathcal{H}$ with tr(A) = 1 such that $\rho(\pi(R)) = tr(A \pi(R))$ for all $R \in \mathcal{R}$.

The last one is most frequently used by physicists, in that context the operator $A$ is also called a density matrix or density operator.

Reference: Kadison and Ringrose, definition 7.1.11 and theorem 7.1.12.

Sometimes the observables of a system are described by an abstract operator algebra, in this case an important notion is the folium:

* Definition: The **folium** of a representation $\pi$ of an operator algebra $\mathcal{R}$ on a Hilbert space is the set of normal states of $\pi(\mathcal{R})$.

* Definition: A state $\rho$ of a representation is called a **vector state** if there is a $x \in \mathcal{H}$ such that $\rho(\pi(R)) = \langle \pi(R)x, x \rangle$ for all $R \in \mathcal{R}$.

* Theorem: Normal states are vector states if $\mathcal{R}$ is a von Neumann algebra with a seperating vector. More precisely: Let $\mathcal{R}$ be a von Neumman algebra acting on a Hilbert space $\mathcal{H}$, let $\rho$ be a normal state of $\mathcal{R}$ and $x \in \mathcal{H}$ be a separating vector for $\mathcal{R}$, then there is a $y \in \mathcal{H}$ such that $\rho(R) = \langle Ry, y \rangle$ for all $R \in \mathcal{R}$.

Reference: This is theorem 7.2.3 in the book of Kadison and Ringrose.

The set of states of an operator algebra is sometimes called the **state space**.

The state space is non-empty (define a state on the subalgebra $\mathbb{C} \mathbb{1}$ and extend it to the whole operator algebra via the [[Hahn-Banach theorem]]), convex and weak$^*$-compact, so it has extreme points. By the [Krein-Milman theorem] (http://en.wikipedia.org/wiki/Krein%E2%80%93Milman_theorem) it is the weak$^*$-closure of it's extreme points.

* Definition: A **pure state** is a state that is an extreme point of the state space.

The term "pure" originates from the notion of [[entanglement]], being an extreme point a pure state is not the sum of two other states.



## References

* [Wikipedia] (http://en.wikipedia.org/wiki/Operator_algebras)

There are a lot of textbooks about operator algebras, here are some examples:

The classic textbook is this:

* Kadison, Richard V.; Ringrose, John R.: "Fundamentals of the theory of operator algebras I" and II, (see [ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0888.46039&format=complete)) for the first.

These have two accompanying volumes (same title, numbers III and IV) which contain complete solutions to the extensive list of excercises. Highly recommended.

One of the founders of the Tomito-Takesaki modular theory has recently published a three volume treatise in the Encyclopaedia of Mathematical Sciences:

* Takesaki, M.: "Theory of operator algebras I, II and III" ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0990.46034&format=complete) of the first volume).

[[!redirects operator algebras]]