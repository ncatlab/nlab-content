
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In full generality, we have the following definition of _gerbe_

+-- {: .un_defn}
###### Definition

Given an [[(∞,1)-topos]] $\mathbf{X}$, a **gerbe** in $\mathbf{X}$ is an [[object]] $\mathcal{G} \in \mathbf{X}$ that is

* 1-[[truncated]]

* 1-[[connective]] (= [[connected]]).

=--

We discuss a bit what this means.

The first condition says that a gerbe is an object in the [[(2,1)-topos]] $\tau_{\leq 1 } \mathbf{X} \hookrightarrow \mathbf{X}$ inside $\mathbf{X}$. This means that for $C$ any [[(∞,1)-site]] of definition for $\mathbf{X}$, a gerbe is a [[(2,1)-sheaf]] on $C$, $\mathcal{G} \in Sh_{(2,1)}(C)$: a [[stack]] on $C$.

The second condition says that  a gerbe is a stack that _locally_ looks like the [[delooping]] of a [[sheaf]] of [[group]]s. More precisely, it says that 

* the morphism $\mathcal{G} \to *$ to the [[terminal object in an (∞,1)-category|terminal object]] of $\mathbf{X}$ is an [[effective epimorphism in an (∞,1)-category|effective epimorphism)]];

* the 0th [[categorical homotopy groups in an (∞,1)-topos|categorical homotopy]] group $\pi_0 \mathcal{G}$ is isomorphic to the terminal object $*$ as objects in the [[sheaf topos]] $\tau_{\leq 0} \mathbf{X} = Sh_{(1,1)}(C)$. Here $\pi_0 \mathcal{G}$ is the [[sheafification]] of the presheaf of connected components of the groupoids that $\mathcal{G} : C^{op} \to Grpd \hookrightarrow \infty Grpd$ assigns to each object in the site.

Traditionally this is phrased before sheafification as saying that a gerbe is a stack that is _locally_  non-empty and _locally_ connected_ . This is the traditional definition, due to [Giraud](#Giraud).

Also traditionally gerbes are considered in the [[little topos|little (2,1)-toposes]] $\tau_{\leq 1} \mathbf{X}$ of a [[topological manifold]] or [[smooth manifold]] $X$ or a [[topological stack]] or [[differentiable stack]] $X$. One then speaks of a _gerbe over $X$_ .

More precisely, we may associate to any $X \in C :=$ [[Top]] or $X \in C :=$ [[Diff]] the corresponding [[big site]] $C/X$ and form the [[(2,1)-topos]] $\tau_{leq} \mathbf{X} := Sh_{(2,1)}(C/X)$. In terms of this a gerbe is given by a collection of groupoids assigned to patches of $X$, satisfying certain conditions.

Equivalent to this is the [[over-(∞,1)-topos|over-(2,1)-topos]] $\tau_{\leq 1} \mathbf{H}/j(X)$, where $\tau_{\leq 1}\mathbf{H} := Sh_{(2,1)}(C)$ is the [[big topos|big]] [[(2,1)-topos]] over $C$ (and $j$ denotes its [[(∞,1)-Yoneda embedding|(2,1)-Yoneda embedding]]).

Since this $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] we may think of its objects a general [[topological ∞-groupoid|continuous ∞-groupoid]]s or [[∞-Lie groupoid|smooth ∞-groupoid]]s. In large parts of the literatur coming after [Giraud](#Giraud) gerbes, or related structures equivalent to them, are described this way in terms of [[topological groupoid]]s and [[Lie groupoid]]s. This perspective is associated with the notion of a _[[bundle gerbe]]_ .



## Sub-entries

The material on _gerbes_ is split into several sub-entries:

* [[gerbe (as a stack)]]

* [[gerbe (in nonabelian cohomology)]]

* [[gerbe (in differential geometry)]]

* [[bundle gerbe]]

* [[gerbe (general idea)]]


## Related concepts

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / **gerbe** / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]] 

*  [[∞-gerbe]]


## References

The definition of _gerbe_ goes back to 

* J. Giraud, _Cohomologie non ab&#233;lienne_ , Springer  (1971)

The fully general definition (see [[∞-gerbe]]) is in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects gerbes]]
[[!redirects gerb]]
