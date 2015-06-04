+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

[[!redirects graphic monoid]]
[[!redirects graphics]]

##Idea
A simple class of finite [[monoids]] and [[categories]] that permit an effective graphic display via their [[presheaf]] categories.


##Definition
A finite monoid $M$ is called _graphic_ if all $x,y\in M$ satisfy the so called _graphic identity_ $x y x=x y$. A finite category $\mathcal{G}$ is called _graphic_ if the endomorphism monoid $End(x)$ is a graphic monoid for all objects $x$.

##Example

The principal example of a graphic category is $\Delta_1$ the three element monoid $\{\delta_1,\delta_2,1\}$ with $\delta_i\delta_j=\delta_i$, or its [[Cauchy completion]] $\overline\Delta_1$. The presheaf topos $\mathcal{S}^{\Delta_1^{op}}$ is the topos of reflexive graphs.

To see this, recall that a **reflexive graph** consists of a set of vertices $V$, a set of edges $E$, source and target maps $s, t : E \to V$, and a map $i : V \to E$ assigning to each vertex an 'identity edge' from that vertex to itself, so that $s(i(v)) = t(i(v)) = v$.  

We can describe a reflexive graph without ever mentioning its vertices by using the identity edge $i(v)$ as a stand-in for $v$.  To do this, we 
define operations $\delta_1, \delta_2 : E \to E$ by 

$$  \delta_1(e) = i(s(e)), \qquad \delta_2(e) = i(t(e)) $$

and note that

$$ \delta_1(\delta_1(e)) = \delta_2(\delta_1(e)) = \delta_1(e) $$

$$ \delta_1(\delta_2(e)) = \delta_2(\delta_2(e)) = \delta_2(e) $$

Thus, the reflexive graph determines a functor $F : \Delta_1^{op} \to \Set$, where we think of the monoid $\Delta_1$ as a one-object category.  In other words, it gives a presheaf on $\Delta_1$.  Conversely, any presheaf on $\Delta_1$ determines a reflexive graph.

##Properties

* Lawvere (1989b, p.53) calls the graphic identity _'the least common generalization of constant (x=c) and identity (x=1)_'.

* In a graphic monoid every element is [[idempotent]] as can be directly seen from the graphic identity with $y=1$.

* It follows that a commutative graphic monoid is the same as a [[semilattice]], or equivalently, a commutative monoid where every element is idempotent.

**Theorem.**  A graphic monoid is the same as a **unital [[left shelf]]**, meaning a set equipped with a binary operation that obeys the left self-distributive law

$$  a (b c) = (a b)(a c) $$

and has an element $1$ serving as a left and right unit:

$$  1 a = a = a 1$$

**Proof.** First start with a unital left shelf.  Note that

$$ a  b = a  (1  b) = (a  1)  (a  b) = a  (a  b) $$

and similarly

$$ a  b = (a  b)  a $$

We can thus deduce the associative law as follows:

$$\begin{aligned}
a  (b  c) &= (a  b)  (a  c) \\
&= ((a  b)  a)  ((a  b)  c) \\
&= (a  b)  ((a  b)  c) \\
&= (a  b)  c
\end{aligned}$$

Conversely, suppose we have a graphic monoid.  Then we can prove the left self-distributive law as follows:

$$ a (b c) = (a b) c = (a b a) c = (a b)(a c) \qquad \qed $$

For more background see the comments on:

* [The origin of the word "quandle"](https://golem.ph.utexas.edu/category/2015/05/the_origin_of_the_word_quandle.html#c049149), $n$-Category Caf&#233;.


##Related Pages

* [[graphic topos]]

* [[Aufhebung]]

* [[graph]]

##References

* N. Kimura, _The structure of idempotent semigroups I_ , Pacific
Journal of Mathematics **8** no.2 (1958) pp.257-275. ([pdf](http://msp.org/pjm/1958/8-2/pjm-v8-n2-p07-p.pdf))

* F. W. Lawvere, _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* F. W. Lawvere, _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_ , Proceedings of the first international conference on algebraic methodology and software technology University of Iowa, May 22-24 1989, Iowa City, pp.51-74. 

* F. W. Lawvere, _More on Graphic Toposes_ , Cah. Top. G&#233;om. Diff. Cat. **XXXII** no. 1 (1991) pp.5-10. ([pdf](archive.numdam.org/article/CTGDC_1991__32_1_5_0.pdf))
&#8206;
* F. W. Lawvere, _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.

* M. P. Sch&#252;tzenberger, _Sur certains treillis gauches_ , C. R. Acad. Sci. Paris, **225** pp.277&#8211;278, 1947. ([pdf](http://igm.univ-mlv.fr/~berstel/Mps/Travaux/A/1947TreillisGauchesCras.pdf))