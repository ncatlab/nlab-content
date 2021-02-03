
> See also _[[differentiation]]_ and _[[derivative]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Differentiable maps
* table of contents
{: toc}

## Idea

A [[function]] (map) is *differentiable* at some point if it can be well approximated by a [[linear map]] near that point.  The approximating linear maps at different points together form the *derivative* of the map.

One may then ask whether the derivative itself is differentiable, and so on.  This leads to a hierarchy of ever more differentiable maps, starting with [[continuous maps]] and progressing through maps that are $n$ times (continuously) differentiable to those that are infinitely differentiable, and finally to those that are [[analytic map|analytic]].  Infinitely differentiable maps are sometimes called *smooth*.

Differentiability is first defined directly for maps between (open subsets of) a [[Cartesian space]].  These differentiable maps can then be used to define the notion of [[differentiable manifold]], and then a more general notion of differentiable map *between* differentiable manifolds, forming a [[category]] called [[Diff]].  We have a parallel hierarchy of ever more differentiable manifolds and ever more differentiable maps between them.  Since every more differentiable manifold has an [[underlying]] less differentiable manifold, we may always consider maps that are less differentiable than the manifolds between which they run.


## Definitions

In all of the following $\mathbb{R}$ denotes the [[real numbers]] and $\mathbb{R}^n$ for $n \in \mathbb{N}$ 
their $n$-fold [[Cartesian product]]. For $i \in \{1, \cdots, n\}$ we write

$$
  \array{
    \mathbb{R}^n &\overset{pr_i}{\longrightarrow}& \mathbb{R}
    \\
    \vec v = (v_1, \cdots, v_n) &\mapsto& v_i
  }
$$

for the [[projection]] map onto the $i$th factor.

When considering [[convergence]] of [[sequences]] of elements of these
sets we regard them as [[Euclidean space|Euclidean]] [[metric spaces]] with the [[Euclidean norm]]

$$
  {\Vert -\Vert} \;\colon\; \mathbb{R}^n \longrightarrow [0,\infty) \subset \mathbb{R}
  \,.
$$ 

The [[open subsets]] of the corresponding [[metric topology]] are the [[unions]] of [[open balls]] in $\mathbb{R}^n$.


### From a Cartesian space to the real numbers

+-- {: .num_defn #DerivativeOfFunctionFromRnToR}
###### Definition
**(differentiation of real-valued functions on Cartesian space)**

Let $n \in \mathbb{N}$ and let $U \subset \mathbb{R}^n$ be an [[open subset]].

Then a [[function]] $f \;\colon\; U \longrightarrow \mathbb{R}$ is called  **differentiable** at $x\in U$ 
if there exists a [[linear map]] $d f_x : \mathbb{R}^n \to \mathbb{R}$ such that the following [[limit of a sequence|limit]]
exists as $h$ approaches zero "from all directions at once":

$$ 
  \lim_{h\to 0} \frac{f(x+h)-f(x) - d f_x(h)}{\Vert h\Vert} = 0. 
$$

This means that for all $\epsilon \in (0,\infty)$ there exists an [[open subset]] $V\subseteq U$ containing $x$ such that whenever $x+h\in V$ we have $\frac{f(x+h)-f(x) - d f_x(h)}{\Vert h\Vert} \lt \epsilon$.

We say that $f$ is __differentiable on__ a [[subset]] $I$ of $U$ if $f$ is differentiable at every $x\in I$, and __differentiable__ (tout court) if $f$ is differentiable on all of $U$. We say that $f$ is **continuously differentiable** if it is differentiable and 
$d f$ is a [[continuous function]].

The map $d f_x$ is called the **derivative** or **differential of $f$ at $x$**.  

=--

+-- {: .num_remark}
###### Remark
**(Notation and Terminology)**

If $n=1$, as in classical one-variable calculus, then $d f_x$ in def. \ref{DerivativeOfFunctionFromRnToR} may be identified 
with a [[real number]], and that number is also called the derivative of $f$ at $x$ and often written $f'(x)$.  (In that case, the notation $d f$ is generally still reserved for the corresponding linear map, with its input denoted by $d x$, so that we have $d f = f'(x) d x$.)

=--

+-- {: .num_remark}
###### Remark
**(equivalent formulation)**

An equivalent way to state def. \ref{DerivativeOfFunctionFromRnToR} is to say that
$$ f(x+h) = f(x) + d f_x(h) + E(h){\Vert h\Vert} $$
where $E$ is a function such that $\lim_{h\to 0}E(h) = 0$.  This is easy to see; just let $E(h) = \frac{f(x+h)-f(x) - d f_x(h)}{\Vert h\Vert}$.

Another equivalent way to say it is that
$$ f(x+h) = f(x) + d f_x(h) + E_1(h) h_1 + \cdots + E_n(h) h_n $$
where $E_i$ are functions such that $\lim_{h\to 0}E_i(h) = 0$.  For if this is true, then $E(h) = \frac{1}{\Vert h\Vert}(E_1(h) h_1 + \cdots + E_n(h) h_n)$ satisfies the previous definition.  Conversely, if the previous definition holds, then defining $E_i(h) = \frac{h_i}{\Vert h \Vert} E(h)$ satisfies this definition.

=--

### Partial and directional derivatives



A weaker notion of differentiability is the following: 

+-- {: .num_defn #DirectionalDerivative}
###### Definition
**([[partial derivative|directional derivative]])**

Let $n \in \mathbb{N}$ and $U \subset \mathbb{R}^n $ an [[open subset]].

Then a [[function]] $f \colon U \longrightarrow \mathbb{R}$ is said to have **directional derivative**
in the direction of $v \in \mathbb{R}^n$ at $x\in U$ if the [[limit of a sequence|limit]]

$$ 
  \lim_{h\to 0} \frac{f(x+h v)- f(x)}{h}
$$


exists. Here $h$ is just a real number.  

=--

Historically, the term 'directional derivative' was reserved for when $v$ is a [[unit vector]] (or divide the derivative above by $\|v\|$), but the general concept involves less structure and is more important but has no other established name.  If $v$ is a standard basis vector $e_i$, then the directional derivative is called a **[[partial derivative]]** with respect to the corresponding coordinate, and often written $\frac{\partial f}{\partial x_i}$ or $f_{x_i}$.

If $f$ is differentiable at $x$ in the sense of def. \ref{DerivativeOfFunctionFromRnToR}, then $d f_x(v)$ is its directional derivative along $v$.  In particular, the coordinates of $d f_x$ are the partial derivatives of $f$.

In general, $f$ may have all partial derivatives, and even all directional derivatives, without being differentiable; 
see the examples [below](#DifferentiabilityOpposedToPartialDifferentiability).  However, if $f$ has all partial derivatives and they are *continuous* as functions of $x$, then in fact $f$ is differentiable (and indeed continuously differentiable).


### Functions between Cartesian spaces

+-- {: .num_defn #FunctionBetweenCartesianSpacesDifferentiation}
###### Definition
**(differentiation of functions between Cartesian spaces)**

Let $n_1, n_2 \in \mathbb{N}$ and let $U\subseteq \mathbb{R}^{n_1}$ be an [[open subset]]. 

Then a [[function]] $f \;\colon\; U \longrightarrow \mathbb{R}^{n_2}$ is _differentiable_ 
if for all $i \in \{1, \cdots, n_2\}$ the component function

$$
  f_i \;\colon\; U \overset{f}{\longrightarrow} \mathbb{R}^{n_2} \overset{pr_u}{\longrightarrow}  \mathbb{R} 
$$

is differentiable in the sense of def. \ref{DerivativeOfFunctionFromRnToR}.  

In this case, the derivatives $d f_i \colon \mathbb{R}^n \to \mathbb{R}$ of the $f_i$ assemble into a linear map 
of the form

$$
  d f_x \;\colon\; \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
  \,.
$$

=--

### Functions between differentiable manifolds

+-- {: .num_defn}
###### Definition

For $X$ and $Y$ [[differentiable manifolds]], then a [[function]] $f \colon X \longrightarrow Y$ is 
called _differentiable_ if for 
$\left\{ \mathbb{R}^{n} \underoverset{\simeq}{\phi_i}{\to} U_i \subset X\right\}$
an [[atlas]] for $X$
and
$\left\{ \mathbb{R}^{n'} \underoverset{\simeq}{\psi_j}{\to} V_j \subset X_2\right\}$
and atlas for $Y$ then for all $i \in I $ and $j \in J$ the function

  $$
     \mathbb{R}^n
     \supset
      \phantom{AA}
     (f\circ \phi_i)^{-1}(V_j)
       \overset{\phi_i}{\longrightarrow}
     f^{-1}(V_j)
      \overset{f}{\longrightarrow}
     V_j
       \overset{\psi_j^{-1}}{\longrightarrow}
     \mathbb{R}^{n'}
  $$

is differentiable in the sense of def. \ref{FunctionBetweenCartesianSpacesDifferentiation}.

=--

## Higher differentiability

### Iterated differentiability

For $U \subset \mathbb{R}^n$ an [[open subset]] and  $f \;\colon\; U\to \mathbb{R}^m$ a differentiable function (def. \ref{DerivativeOfFunctionFromRnToR}), we may regard its differential $d f$ as a function from a subset of $U$ (the points where $f$ is differentiable) to the space $L(\mathbb{R}^n,\mathbb{R}^m)$ of [[linear maps]].  Since $L(\mathbb{R}^n,\mathbb{R}^m) \cong \mathbb{R}^{n m}$ is again a Cartesian space, we may then ask whether $d f$ is differentiable.

We can then iterate, obtaining the following hierarchy of differentiability.  Because iterated differentiability by itself is not very useful, and a differentiable map is necessarily continuous, one generally includes continuity of the last assumed derivatives.

* The map $f$ is __continuous__ or __$C^0$__ if it is a [[continuous map]] between underlying [[topological spaces]].  We begin with this since a differentiable map is necessarily continuous.

* The map $f$ is __continuously differentiable__ or __$C^1$__ on $U$ if it is differentiable at all points of $U$ and the resulting map $d f$ is [[continuous map|continuous]].  (At this point, if we generalize to infinite-dimensional spaces, we get a variety of notions of when the differential is 'continuous'; see [[continuously differentiable map]] for discussion.)

* The map $f$ is __twice differentiable__ if it is differentiable and its derivative $d f$ is differentiable.  A twice differentiable map must be continuously differentiable.  Similarly, $f$ is __twice continuously differentiable__ or __$C^2$__ if it is twice differentiable and the second derivative $d d f$ is continuous.

* By [[recursion]], $f$ is __$n + 1$ times differentiable__ if $f$ is $n$ times differentiable and the $n$th derivative of $f$ is differentiable.  Similarly, $f$ is __$n$ times continuously differentiable__ or __$C^n$__ if $f$ is $n$ times differentiable and the $n$th derivative of $f$ is continuous.

* The map $f$ is __[[smooth map|smooth]]__ or __infinitely differentiable__ or __$C^\infty$__ if it is $n$ times differentiable for all $n$, or equivalently if it is $C^n$ for all $n$.  (There is no difference between infinite differentiability and infinite continuous differentiability.)  One may also define this notion [[coinductive definition|coinductively]]: $f$ is infinitely differentiable if it is differentiable and its derivative $d f$ is infinitely differentiable.

* One step higher, we may ask whether $f$ is [[analytic function|analytic]] or $C^\omega$.


### Uniform differentiability

Note that $f$ is differentiable on a set $U$ iff there is a function $f'$ on $U$ (necessarily unique, assuming that $U$ has no [[isolated points]]) such that

$$ \forall\, \epsilon \gt 0,\; \forall\, x \in U,\; \exists\, \delta \gt 0,\; \forall\, y \in U,\; {|{y - x}|} \lt \delta \;\Rightarrow\; {|{f(y) - f(x) - f'(x)(y - x)}|} \lt \epsilon \,{|{y - x}|} .$$

Reverse quantifiers, and $f$ is __uniformly differentiable__ on $U$ iff there is a function $f'$ on $U$ such that

$$ \forall\, \epsilon \gt 0,\; \exists\, \delta \gt 0,\; \forall\, x \in U,\; \forall\, y \in U,\; {|{y - x}|} \lt \delta \;\Rightarrow\; {|{f(y) - f(x) - f'(x)(y - x)}|} \lt \epsilon \,{|{y - x}|}.$$

In [[classical mathematics]], $f$ is uniformly differentiable if and only if $f$ is differentiable and its derivative $f'$ is [[uniformly continuous map|uniformly continuous]]; in other words, $f$ is uniformly differentiable iff $f$ is _uniformly-continuously differentiable_.  The same is true in [[constructive mathematics]] as long as one assumes [[dependent choice]]. In the absence of dependent choice, however, the argument only goes one way, and uniform differentiability is stronger.  Furthermore, just as pointwise continuity is not as well behaved constructively as uniform continuity, so pointwise differentiability is not as well behaved constructively as uniform differentiability.  For this reason, uniform differentiability is particularly important in constructive mathematics.


### Symmetry of higher derivatives

If $f:U\to \mathbb{R}^m$ is twice differentiable with $U\subseteq \mathbb{R}^n$, its second derivative
$$d(d f) : U \to L(\mathbb{R}^n,L(\mathbb{R}^n,\mathbb{R}^m)) \cong Bilin(\mathbb{R}^n,\mathbb{R}^n;\mathbb{R}^m)$$
is a function from $U$ into the space of [[bilinear maps]] from $\mathbb{R}^n\times \mathbb{R}^n$ to $\mathbb{R}^m$.

+-- {: .num_theorem}
###### Theorem
If $f:U\to \mathbb{R}^m$ is twice differentiable, then its second derivative $d(d f)$ lands in the space of *symmetric* bilinear maps, i.e. for any $x\in U$ and $v,w\in \mathbb{R}^n$ we have
$$ d(d f)_x(v,w) = d(d f)_x(w,v). $$
=--
+-- {: .proof}
###### Proof
It suffices to assume $m=1$; otherwise we just consider it componentwise.  Define a function $g:\mathbb{R}\to \mathbb{R}$ by
$$ g(\xi) = f(x+\xi v+w) - f(x+\xi v). $$
Then by the chain rule, $g$ is differentiable and
$$
\begin{aligned}
  g'(\xi) &= d f_{x+\xi v+w}(v) -  d f_{x+\xi v}(v)\\
  &= \Big(d f_{x+\xi v+w}(v) - d f_{x}(v)\Big) - \Big(d f_{x+\xi v}(v) - d f_x(v)\Big)\\
  &= d(d f)_{x}(v,\xi v + w) + E_1 |v|\,|\xi v + w| - d(d f)_x(v,\xi v) - E_2 |v|\,|\xi v|\\
  &= d(d f)_x(v,w) + E |v|\, (|v|+|w|)
\end{aligned}
$$
where $E_1, E_2, E \to 0$ as $(v,w)\to 0$.  Now the [[mean value theorem]] tells us that for some $\xi\in(0,1)$ we have
$$
\begin{aligned}
  f(x+v+w) - f(x+v) - f(x+w) + f(x)
  &= g(1) - g(0)\\
  &= g'(\xi)\\
  &= d(d f)_x(v,w) + E (|v|+|w|)^2.
\end{aligned}
$$
But the "second-order difference" $f(x+v+w) - f(x+v) - f(x+w) + f(x)$ is manifestly symmetric in $v$ and $w$, so we have
$$ d(d f)_x(v,w) - d(d f)_x(w,v) = E (|v|+|w|)^2 $$
where $\lim_{(v,w)\to 0} E = 0$.  But bilinearity of the LHS then implies that it is identically zero.
=--

The components of the bilinear map $d(d f)$ are the second-order partial derivatives $\frac{\partial^2 f}{\partial x_i \partial x_j}$ of $f$.  Thus, this theorem says that if $f$ is twice differentiable, then the *mixed partials* are equal,
$$\frac{\partial^2 f}{\partial x_i \partial x_j} = \frac{\partial^2 f}{\partial x_j \partial x_i}.$$

The second-order partial derivatives may *exist* without the mixed partials being equal; see below for a counterexample.  However, the theorem shows that if we require $f$ to actually be twice differentiable rather than merely having second-order partial derivatives, then this cannot happen.

In particular, we have the following corollary, which is more commonly found in textbooks.

+-- {: .num_cor}
###### Corollary
If $f$ has first and second-order partial derivatives, and the latter are continuous in a neighborhood of $x$, then the mixed partial derivatives are equal,
$$\frac{\partial^2 f}{\partial x_i \partial x_j} = \frac{\partial^2 f}{\partial x_j \partial x_i}.$$
=--
+-- {: .proof}
###### Proof
Continuity of the second-order partials implies that the first-order partials are differentiable, and hence so is the differential $d f$.
=--


### A direct definition of the second derivative

Note that the proof of the theorem implies that if $f$ is twice differentiable at $x$, then there exists a bilinear map $\partial^2 f_x : \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^m$ such that

$$f(x+v+w) - f(x+v) - f(x+w) + f(x) = \partial^2 f_x(v,w) + E(v,w) ({|v|+|w|})^2 $$

where $\lim_{v,w\to 0} E(v,w) = 0$.  This is a condition that makes sense as a condition on an arbitrary $f$ without assuming differentiability. and if it holds, then the bilinear map $\partial^2 f_x$ must be symmetric.

Moreover, as explained [here](http://mathoverflow.net/a/165733/49), if $f$ is differentiable in a neighborhood of $x$ and satisfies this condition at $x$, then it is in fact twice differentiable at $x$.  To see this, it suffices to show that each coordinate of $d f$ is differentiable, so let $w=\delta e_i$, with $e_i$ a unit basis vector and $\delta$ a real number $\neq 0$.  Then we have

$$ E(v,\delta e_i) = \frac{f(x+v+\delta e_i) - f(x+v) - f(x+\delta e_i) + f(x) - \partial^2 f_x(v,\delta w)}{{|v|}{\delta}}$$

Taking the limit as $\delta\to 0$ and using differentiability of $f$ at $x$ and $x+v$ (for sufficiently small $v$), we get

$$ \lim_{\delta \to 0} E(v,\delta e_i) = \frac{d f_{x+v}(e_i) - d f_x(e_i) - \partial^2 f_x(v,e_i)}{{|v|}}. $$

Now take the limit as $v\to 0$; on the left we get $0$ by assumption, so the function $y\mapsto d f_y(e_i)$ is differentiable at $x$ with derivative $\partial^2 f_x(-,e_i)$.  Thus, $d f$ is differentiable at $x$.

On the other hand, this condition by itself does not even imply that $f$ is continuous.  For instance, if $f$ is a $\mathbb{Q}$-linear map $\mathbb{R}\to \mathbb{R}$, then the second-order difference $f(x+v+w) - f(x+v) - f(x+w) + f(x)$ is identically zero.


### Higher differentiability on tangent spaces and the chain rule

Let $f:\mathbb{R}^n\to \mathbb{R}$ be differentiable.  Instead of asking whether $d f : U \to L(\mathbb{R}^n,\mathbb{R})$ is differentiable, we can ask whether its exponential transpose $d f : U\times \mathbb{R}^n \to \mathbb{R}$ is differentiable.  (Note that $U\times \mathbb{R}^n$ is the [[tangent bundle]] of $U\subseteq \mathbb{R}^n$.)  This amounts to asking that for $x\in U$ and $v\in \mathbb{R}^n$, we have
$$ d f_{x+w}(v+h) - d f_x(v) = d^2 f_{(x,v)}(w,h) + E(|w|+|h|) $$
for a linear map $d^2 f_{(x,v)}:\mathbb{R}^{2n} \to \mathbb{R}$, where $\lim_{(w,h)\to 0} E = 0$.  Setting $h=0$, we see that this implies that $d f : U \to L(\mathbb{R}^n,\mathbb{R})$ is differentiable, with differential $d(d f)_x = d^2 f_{(x,v)}(w,0)$ for any $v$.  And setting $w=0$, we obtain $d f_x(h) = d^2 f_{(x,v)}(0,h)$ for any $v$.  Thus, we can write
$$ d^2 f_{(x,v)}(w,h) = \partial^2 f_x(v,w) + d f_x(h) $$
where $\partial^2 f_x$ is the symmetric bilinear map from the previous section.  Conversely, if $f$ is twice differentiable, then using linearity and continuity of $d f$ it is easy to see that the above condition holds.

Therefore, these two kinds of twice-differentiability of $f$ are equivalent as *conditions* on $f$, but the resulting *second differential* is different.  In the second case, we get

$$d^2f = \partial^2 f + d f = \sum_{i,j} \frac{\partial^2f}{\partial x_i \partial x_j} d x_i \, d x_j + \sum_i \frac{\partial f}{\partial x_i} d^2 x_i. $$

rather than merely the first term $\sum_{i,j} \frac{\partial^2f}{\partial x_i \partial x_j} d x_i \, d x_j$.  There are two advantages to the second approach (asking that $d f : U\times \mathbb{R}^n \to \mathbb{R}$ be differentiable).

Firstly, we can reformulate it in terms of $f$ by asking that there exists a linear map $d f_x : \mathbb{R}^n \to \mathbb{R}^m$ and a bilinear map $\partial^2 f_x : \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^m$ such that

$$f(x+v+w+h) - f(x+v) - f(x+w) + f(x) = \partial^2 f_x(v,w) + d f_x(h) + E(v,w,h) \sqrt{{|v|}^2{|w|}^2 + {|h|}^2}.$$

where $\lim_{v,w,h \to 0} E(v,w,h) = 0$.  This holds if $f$ is twice differentiable, for then we can write
$$
\begin{aligned}
  f(x+v+w+h) &= f(x+v+w) + d f_{x+v+w}(h) + E {|h|}\\
  &= f(x+v+w) + d f_x(h) + d(d f)_x(v+w,h) + E {|v+w|}{|h|} + E{|h|}
\end{aligned}
$$
and $d(d f)_x(v+w,h)$ can also be incorporated into the error term.  Of course, setting $h=0$ we obtain the characterization of twice-differentiability from the previous section.  But setting $v=w=0$, we find that $f$ is differentiable at $x$ with derivative $d f_x$.  So here we have a direct characterization of the second derivative which also implies that the first derivative exists (although it seems that it doesn't imply differentiability in a neighborhood of $x$, so that the resulting "second derivative" may not actually be the derivative of the first derivative).

Secondly, the virtue of a second differential incorporating the first derivatives is that like the first differential $d f$, but unlike the bilinear map $\partial^2 f$, it satisfies [[Cauchy's invariant rule]].  This means that we can express the [[chain rule]] for second differentials of composite maps simply by substitution: if $y = f(u)$ and $u = g(x)$, then finding $d^2 y$ in terms of $d u$ and $d^2 u$, and $d u$ and $d^2 u$ in terms of $d x$ and $d^2 x$, and substituting, gives the correct expression for $d^2 y$ in terms of $d x$ and $d^2 x$.

In fact, this can be proven using the above direct characterization of the second differential, in essentially exactly the same way that we prove the ordinary chain rule for first derivatives.  We sketch the proof, omitting the explicit error terms.  We can write

$$g(f(x+v+w+h)) - g(f(x+v)) - g(f(x+w)) + g(f(x)) $$

as

$$ g(f(x) + v' + w' + h') - g(f(x) + v') - g(f(x) + w') + g(f(x)) $$

where $v' = f(x+v) - f(x)$ and $w' = f(x+w) - f(x)$ and $h' = f(x+v+w+h) - f(x+v) - f(x+w) + f(x)$.  Now by extra-strong twice differentiability of $g$, this is approximately equal to

$$ \partial^2 g_{f(x)}(v',w') + d g_{f(x)}(h'). $$

But by differentiability of $f$, we have $v' \approx d f_x(v)$ and $w' \approx d f_x(w)$, while by extra-strong twice differentiability of $f$ we have $h' \approx \partial^2 f_x(v,w) + d f_x(h)$.  Thus, we obtain approximately

$$ \partial^2 g_{f(x)}(d f_x(v), d f_x(w)) + d g_{f(x)}(\partial^2 f_x(v,w) + d f_x(h)) $$

which is exactly what we would get by substitution.


### For maps between manifolds

If $X$ and $Y$ are $C^k$-[[differentiable manifolds]], then we may define what it means for a map $f:X\to Y$ to be $n$ times differentiable, or $C^n$, for any $n\le k$, by asking that it yield such a map when restricted to any charts.  The most common case is when $X$ and $Y$ are smooth (infinitely differentiable) manifolds, so that we can define $C^n$ functions between them for all $n\le \infty$.  (Analytic manifolds, which are necessary in order to define analyticity of $f$, are somewhat rarer.)

A differentiable map between manifolds induces a map between their [[tangent bundles]] $d f : T X \to T Y$; this operation extends to a [[functor]] from $C^{k+1}$ manifolds and $C^{k+1}$ maps to $C^k$ manifolds and $C^k$ maps.  See [[differentiation]] for more.


## Examples and non-examples

### Differentiability versus partial differentiability
 {#DifferentiabilityOpposedToPartialDifferentiability}

The function $f:\mathbb{R}^2 \to \mathbb{R}$ defined by

$$ f(x,y) =
\begin{cases}
  \frac{y^3}{x^2+y^2} &\quad (x,y) \neq (0,0)\\
  0 &\quad (x,y) = (0,0)
\end{cases}
$$

is continuous everywhere, and has directional derivatives (def. \ref{DirectionalDerivative}) at $(0,0)$ in all directions, but is not differentiable at $(0,0)$ in the sense of def. \ref{DerivativeOfFunctionFromRnToR}.  Note that the (unnormalized) directional derivative along the vector $(a,b)$ is $\frac{b^3}{a^2+b^2}$, which is not linear.

One may wonder whether existence of a linear map $d f_x$ is enough, but this is also not the case.  The function $f:\mathbb{R}^2 \to \mathbb{R}$ defined by

$$ f(x,y) = \begin{cases} \frac{y^3}{x} &\quad x\neq 0\\ 0 &\quad x=0 \end{cases} $$

has all directional derivatives at $(0,0)$ equaling $0$, so that in particular there is a linear map $d f_{(0,0)}$ whose values are the directional derivatives.  But it is not differentiable at $(0,0)$; in fact, it is not even continuous at $(0,0)$.  (Thus it also provides an example of a discontinuous function which has all directional derivatives.)

The discontinuity kind of gives this last one away; maybe a continuous function with all directional derivatives must be differentiable?  But no, because if $W$ is a [[Weierstrass function]] (continuous everywhere but differentiable nowhere) from $\mathbb{R}$ to $\mathbb{R}$ with [[periodic function|period]] $2\pi$, and $\operatorname{atan2}$ is a $2$-argument [[arctangent]] function from $\mathbb{R}^2$ to $\mathbb{R}$ (so that $\sqrt{x^2+y^2} \,\sin\,\operatorname{atan2}(y,x) = y$ and $\sqrt{x^2+y^2} \,\cos\,\operatorname{atan2}(y,x) = x$ for all $x$ and $y$), then set

$$ f(x,y) = (x^2 + y^2) W(\operatorname{atan2}(y,x)) .$$

Then $f$ is, like $W$, continuous everywhere and differentiable nowhere, yet the directional derivatives through the origin are all $0$.  There are further examples (including one that is analytic except at the origin) at [Math StackExchange question 1497043](https://math.stackexchange.com/questions/1497043/is-there-a-function-thats-continuous-and-has-all-directional-derivatives-as-a-l).


### Differentiability versus continuous and higher differentiability

Let $k$ be a [[natural number]], and consider the function
$$ f_k(x) \coloneqq x^k \sin(1/x) $$
from the [[real line]] to itself, with $f(0) \coloneqq 0$.  Away from $0$, $f_k$ is smooth (even analytic); but at $0$, $f_0$ is not continuous, $f_1$ is continuous but not differentiable, $f_2$ is differentiable but not continuously differentiable, and so on:

*  If $k = 2 n$ is even, then $f_k$ is differentiable $n$ times but not continuously differentiable $n$ times;
*  If $k = 2 n + 1$ is odd, then $f_k$ is continuously differentiable $n$ times but not differentiable $n + 1$ times.

Similarly, in two dimensions we can consider functions such as
$$ f(x,y) = (x^2+y^2)\sin(\frac{1}{\sqrt{x^2+y^2}}).$$
together with $f(0,0) = 0$.  This is smooth away from $0$, and once differentiable at $0$, even in the strong sense that it is well-approximated by a linear function near $0$.  However, its derivative is not continuous at $0$.  In particular, this shows that the converse of the theorem "if the partial derivatives exist and are continuous at a point, then the function is differentiable there" fails, even in higher dimensions.

Uniform differentiability is stronger than continuous differentiability but independent of twice differentiability.  For an example that is uniformly differentiable but not twice differentiable, use $f_3$ again.  For an example that that is twice differentiable (and hence continuously differentiable) but not uniformly differentiable, use $x \mapsto x^3$.  However, on a [[compact set|compact]] domain, any continuously differentiable function (and a fortiori any twice differentiable function) must be uniformly continuous (at least in [[classical mathematics|classical]] and [[intuitionistic mathematics]]).


### Symmetry of the second partial derivatives

The function $f:\mathbb{R}^2 \to \mathbb{R}$ defined by

$$ f(x,y) = \frac{x y (x^2-y^2)}{x^2+y^2}$$

plus $f(0,0) = 0$, has partial derivatives $\frac{\partial^2f}{\partial x \partial y}$ and $\frac{\partial^2f}{\partial y \partial x}$ that both exist but are not equal at $(0,0)$ (nor are they continuous at $(0,0)$).  Therefore, by the theorem proven above, it is not twice differentiable at $(0,0)$.


### Twice differentiability versus quadratic approximation

While differentiability means approximability by a linear function, twice differentiability does *not* mean approximability by a quadratic function.  For example, the function

$$ f(x) = x^3 \sin(1/x) $$

(with $f(0) =0$, to make it continuous there) is not twice differentiable at $x=0$, but it is well-approximated by the quadratic polynomial $p(x) = 0$ in the sense that their difference is $o(x^2)$ as $x\to 0$.  Even worse, the function

$$ f(x) = e^{-1/x^2} \sin(e^{1/x^2}) $$

is not twice differentiable at $x=0$, but it is well-approximated by a polynomial of *any* finite degree $n$ (namely, the zero polynomial), in the sense that their difference is $o(x^n)$ as $x\to 0$.

In some contexts, it is useful to say that functions such as these have "pointwise second derivatives".  More precisely, we say that a function $f$ has a **pointwise $k^{th}$ derivative** at $a$ if it is continuous at $a$ and there exists a polynomial $p$ of degree $k$ such that

$$ \lim_{x\to a} \frac{f(x) - p(x)}{(x-a)^k} = 0. $$

(We have to state continuity explicitly in order to match the usual notion of differentiability when $k = 1$, since nothing in this limit constrains the value of $f(a)$.)  In this case, the pointwise $k^{th}$ derivative is $f^{(k)}_{pt}(a) = p^{(k)}(a)$ (and it follows that all lower-order pointwise derivatives match as well).  Thus we would say that while $f(x) = x^3 \sin(1/x)$ does not have a second derivative at $0$, it does have a *pointwise* second derivative at $0$, and $f_{pt}''(0) = 0$.  Similarly, $e^{-1/x^2} \sin(e^{1/x^2})$ is pointwise smooth.  See e.g. [this MSE answer](http://math.stackexchange.com/a/160383/91608).

The polynomial $p$ may be thought of as the $k$th-order [[Taylor polynomial]] of $f$ at $a$, and the limit above is Taylor's theorem with the Peano remainder.  (Thus the subscript $pt$ can be thought of as standing for &#8216;Peano--Taylor&#8217; as well as for &#8216;pointwise&#8217;.)  Note that while $k$-times pointwise differentiability is weaker than $k$-times differentiability for $k \gt 1$ and equivalent for $k = 1$, it is stronger for $k = 0$ (since even $0$-times pointwise differentiability requires continuity).


### The second derivative as a quadratic form

In the definition of strong twice-differentiability, we cannot replace the symmetric [[bilinear map]] $\partial^2 f_x(v,w)$ by the corresponding [[quadratic form]] $Q_x(v) = \partial^2f_x(v,v)$.  In other words, if we suppose that

$$f(x+2v) - 2 f(x+v) + f(x) = Q_x(v) + E(v) {|v|}^2 $$

where $\lim_{v\to 0} E(v) = 0$, for some quadratic form $Q_x$, it does not follow that $f$ is twice differentiable at $x$, even in one dimension.  The same old counterexample

$$ f(x) = x^3 \sin(1/x) $$

(with $f(0)=0$) works: we have

$$f(0+2v) - 2 f(0+v) + f(0)= 2v^3(4\sin(\frac{1}{2v}) - \sin(\frac{1}{v}))$$

so $E(v) = v (4\sin(\frac{1}{2v}) - \sin(\frac{1}{v})) \to 0$.


## Related concepts

* [[smooth function]]

* [[extremum]]

* [[chain rule]], [[total derivative]]

* [[continuous function]], **differentiable function**, [[continuously differentiable function]], [[smooth function]], [[analytic function]]

* [[derivative of distributions]]

* [[integrable function]], [[square-integrable function]]

* [[bounded function]]

* [[compactly supported function]]

* [[measurable function]]

* [[rapidly decreasing function]]


## References

Early account, in the context of [[Cohomotopy]], [[cobordism theory]] and the [[Pontryagin-Thom construction]]:

* {#Pontrjagin55} [[Lev Pontrjagin]], Chapter I of: _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/pont001.pdf))


[[!redirects differentiable map]]
[[!redirects differentiable maps]]
[[!redirects differentiable function]]
[[!redirects differentiable functions]]
[[!redirects differentiability]]

[[!redirects uniformly differentiable map]]
[[!redirects uniformly differentiable maps]]
[[!redirects uniformly differentiable function]]
[[!redirects uniformly differentiable functions]]
[[!redirects uniform differentiability]]

[[!redirects twice differentiable map]]
[[!redirects twice differentiable maps]]
[[!redirects twice-differentiable map]]
[[!redirects twice-differentiable maps]]
[[!redirects twice differentiable function]]
[[!redirects twice-differentiable functions]]
[[!redirects twice-differentiable function]]
[[!redirects twice differentiable functions]]
[[!redirects twice differentiability]]

[[!redirects C-n map]]
[[!redirects C-n maps]]
[[!redirects C-n function]]
[[!redirects C-n functions]]
[[!redirects C^n map]]
[[!redirects C^n maps]]
[[!redirects C^n function]]
[[!redirects C^n functions]]
[[!redirects C-k map]]
[[!redirects C-k maps]]
[[!redirects C-k function]]
[[!redirects C-k functions]]
[[!redirects C^k map]]
[[!redirects C^k maps]]
[[!redirects C^k function]]
[[!redirects C^k functions]]
