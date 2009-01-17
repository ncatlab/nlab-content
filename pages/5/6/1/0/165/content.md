#Idea#

The **fundamental groupoid** of a space $X$ is a [[groupoid]] whose objects are the points of $X$ and whose morphisms are paths in $X$.  

#Definition#



The **fundamental groupoid** $\Pi_1(X)$ of a toplogical space  $X$ is the [[groupoid]] whose set of objects is $X$ and whose morphism from $x$ to $y$ are the [[homotopy]]-classes $[\gamma]$ of continuous maps $\gamma : [0,1] \to X$ whose endpoints map to $x$ and $y$. Composition is by concatenation of representative maps. Under the [[homotopy]]-[[equivalence relation]] this becomes an associtive and unital composition with respect to which every morphism has an inverse.


#Remarks#

* For any $x$ in $X$ the first homotopy group $\pi_1(X,x)$ of $X$ based at $X$ arises as the automorphisms in $\Pi_1(X)$ at $x$:
$$
  \pi_1(X,x) = Aut_{\Pi_1(X)}(x)
  \,.
$$
So the fundamental groupoid is an improvement of the idea of the fundamental group, which gets rid of the choice of basepoint.

* In parts of the literature the fundamental groupoid and in particular the [[fundamental infinity-groupoid]] of a space is called the **Poincar&#233;-groupoid**.

* The fundamental groupoid and its higheer generalization play a fundamental role in [[Trimble'ss notion of weak n-cateory]].

* Following Trimble's definition, it is possible to generalize the notion of fundamental $n$-groupoids from [[Top]] to other [[closed monoidal homotopical category|closed monoidal homotopical categories]] using the concept of categories with [[interval object]].