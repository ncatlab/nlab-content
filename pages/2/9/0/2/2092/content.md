#Contents#
* automatic table of contents goes here
{:toc}

## Idea
An __operator algebra__ is any subalgebra of the algebra of continuous linear operators on a [[topological vector space]], with composition as the multiplication. In most cases, the space is a separable [[Hilbert space]], and most attention historically has been paid to algebras of bounded linear operators. The operator algebras themselves are often equipped with their own topologies (e.g. norm topology, weak topology, weak$^*$ topology and so on) and sometimes involution. __$C^*$-[[C-star algebra|algebras]]__ are (in the complex case) norm-closed complex $*$-[[subalgebras]] of the algebra of the bounded linear operators on a Hilbert space. They can be however characterized structurally as a $*$-[[representation]] of a [[Banach algebra]] with involution satisfying some compatibility conditions; the latter could be called abstract $C^*$-algebras (or sometimes $B^*$-algebras). Every _commutative_ unital $C^*$-algebra can be realized as an algebra of functions on a Hausdorff compact space, which is obtained as its [[Gel'fand spectrum]].

Special class of $C^*$-algebras are __[[von Neumann algebra|von Neumann]]__ or $W^*$-algebras (see [wikipedia](http://en.wikipedia.org/wiki/Von_Neumann_algebra)), which are (in the complex case) _weakly closed_ (closed in the weak topology) $*$-subalgebras of the algebra of bounded linear operators on a Hilbert space. In structural theory, an important role among von Neumann algebras is played by so-called factors, characterized by the property that their center is trivial ($1$-dimensional, consisting of "scalars"). 

Operator algebras play major roles in [[functional analysis]], [[representation theory]], [[noncommutative geometry]] and [[quantum field theory]]. 

## Topics of interest for the understanding of AQFT
This paragraph will collect some facts of interest for the aspects of [[AQFT]] in the nLab.

###Normal states
The Heisenberg picture is sometimes formalized by describing the observables of a quantum system by an operator algebra, and the state of the system as a state of the algebra. The first "state" in the preceding sentence is the state the described physical system is in, the second one is the mathematical counterpart we are about to define, that inherited it's name from the physical concept.

* Definition: A linear functional is **positive** if $A \ge 0$, that is A is a positive operator resp. is an element of the positive cone, implies that  $\rho(A) \ge 0$.

* Definition: A **state** of an operator algebra is linear functional $\rho$ such that $\rho$ is positive and $\rho(\mathbb{1}) = 1$.

Though the mathematical notion of state is already close to what physicists have in mind, they usually restrict the set of states further and consider normal states only. We let $\mathcal{R}$ be an operator algebra and $\pi$ an representation of $\mathcal{R}$ on a Hilbert space $\mathcal{H}$.
 
A **normal state** $\rho$ is a state that satisfies one of the following equivalent conditions:

* $\rho$ is weak-operator coninuous on the unit ball of $\pi(\mathcal{R})$.

* $\rho$ is strong-operator coninuous on the unit ball $\pi(\mathcal{R})$.

* $\rho$ is ultra-weak coninuous.

* There is an operator A of trace class of $\mathcal{H}$ with tr(A) = 1 such that $\rho(\pi(R)) = tr(A \pi(R))$ for all $R \in \mathcal{R}$.

The last one is most frequently used by physicists.

Sometimes the observables of a system are described by an abstract operator algebra, in this case an important notion is the folium:

* Definition: The **folium** of a representation $\pi$ of an operator algebra $\mathcal{R}$ on a Hilbert space is the set of normal states of $\pi(\mathcal{R})$.

## References

* [Wikipedia] (http://en.wikipedia.org/wiki/Operator_algebras)

There are a lot of textbooks about operator algebras, here are some examples:

The classic textbook is this:

* Kadison, Richard V.; Ringrose, John R.: "Fundamentals of the theory of operator algebras I" and II, (see [ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0888.46039&format=complete)) for the first.

These have two accompanying volumes (same title, numbers III and IV) which contain complete solutions to the extensive list of excercises. Highly recommended.

One of the founders of the Tomito-Takesaki modular theory has recently published a three volume treatise in the Encyclopaedia of Mathematical Sciences:

* Takesaki, M.: "Theory of operator algebras I, II and III" ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0990.46034&format=complete) of the first volume).

[[!redirects operator algebras]]