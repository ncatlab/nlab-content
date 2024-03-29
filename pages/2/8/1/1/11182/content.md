
# Cogerm differential forms
* table of contents
{: toc}

## Idea

A cogerm differential form is a vast generalization of the usual exterior [[differential forms]], which includes also [[absolute differential forms]], as well as "higher" differential forms such as $d^2x$ and a commutative differential operator (at least in the case of 1-forms).


## Definition

Let $X$ be a [[set]].  Usually, $X$ will be a [[manifold]] or a [[generalized smooth space]], but the definition does not require this.

By a *[[curve]]* in $X$ we mean a function $c:(-\epsilon,\epsilon)\to X$ for some real number $\epsilon\gt 0$.  Two curves $c:(-\epsilon,\epsilon)\to X$ and $c':(-\epsilon',\epsilon')\to X$ have the same *[[germ]]* (at 0) if there exists $\epsilon'' \le min(\epsilon,\epsilon')$ such that $c$ and $c'$ agree when restricted to $(-\epsilon'',\epsilon'')$.  Let $C X$ denote the set of germs of curves in $X$, i.e. the [[quotient]] of the set of curves in $X$ by the [[equivalence relation]] "has the same germ as".

+-- {: .un_defn}
###### Definition
A (partial) **cogerm differential 1-form** on $X$ is a [[partial function]] $\omega : C X \to \mathbb{R}$.  We write the action of $\omega$ on a curve $c$ (or germ thereof) as $\langle \omega | c \rangle$.
=--


## Examples

* If $f: X\to \mathbb{R}$ is a function, then it defines a cogerm differential 1-form, also denoted $f$, by evaluation at $0$:
  $$ \langle f | c \rangle = (f\circ c)(0).$$
  This is defined on *all* germs.

* We also have the differential of $f$, denoted $\mathrm{d}f$, defined by
  $$ \langle \mathrm{d}f | c \rangle = (f\circ c)'(0)$$
  which is defined on all germs $c$ having the property that $f\circ c$ is differentiable at $0$.  In particular, if $f$ is smooth (for $X$ a [[smooth space]]), then $\mathrm{d}f$ is defined on all smooth germs.

  When $X$ is a [[differentiable manifold]], $ \langle \mathrm{d}f | c \rangle$ depends only on the [[tangent vector]] of $c$ at $0$.

* More generally, any real-valued function on the [[tangent bundle]] of $X$ can be regarded as a cogerm differential 1-form; this includes in particular all [[differential form|exterior differential 1-forms]].

* We also have the second differential $\mathrm{d}^2f$, defined by
  $$ \langle \mathrm{d}^2f | c \rangle = (f\circ c)''(0),$$
  which depends only on the 2-[[jet]] of $c$ at $0$.  We can similarly consider higher differentials which depend on higher jets.  A cogerm differential 1-form which depends only on the jet of $c$ may be called a *cojet differential 1-form*.

* For an example of a cogerm differential form that is not a cojet differential form, let $\langle{\omega|c}\rangle$ be $0$ or $1$ according as $c$ is or is not [[analytic function|analytic]] (say for $X$ the real line).  We do not know any more interesting examples.

* We can also apply arbitrary real functions: if $\phi:\mathbb{R}^n\to \mathbb{R}$ is a function (or even a partial function) and $\omega_1,\dots,\omega_n$ are cogerm differential 1-forms, then we have $\phi(\omega_1,\dots,\omega_n)$ defined by
  $$ \langle \phi(\omega_1,\dots,\omega_n) | c \rangle = \phi(\langle\omega_1|c\rangle,\dots,\langle\omega_n|c\rangle) $$
  
* For instance, any $\omega$ has an absolute value ${|\omega|}$.

* And if $X=\mathbb{R}^2$, then we have the "length element" $&#273; s = \sqrt{\mathrm{d}x^2 + \mathrm{d}y^2}$.

* Generalizing $&#273;s$, any [[absolute differential form|absolute differential 1-form]] can be regarded as a cogerm differential 1-form.

* Any [[symmetric bilinear form]] on tangent vectors can also be regarded as a [[quadratic form|quadratic]] covector form and therefore a quadratic cogerm form.  In particular, this applies to the [[Riemannian metric|metric]] $g$ on any (pseudo)-[[Riemannian manifold]].  We then have $g = &#273;s^2$ in the algebra of cogerm forms on a Riemannian manifold.

* For any function $f$, we have a cogerm differential form $\Delta f$, defined by $f(x+\mathrm{d}x)-f(x)$.  When $f$ is the [[Heaviside function]], $\Delta f$ is a candidate for the [[Dirac delta function]].

* A somewhat better way to represent the [[Dirac delta function]] as a cogerm differential form is
  $$ \delta =
  \begin{cases}
    \frac{1}{|\mathrm{d}x|} &\qquad x=0 \;and\; \mathrm{d}x\neq 0\\
    0 &\qquad otherwise.
  \end{cases}
  $$
  In the section on integration below we will see why this deserves the name "delta function".

## The cogerm differential

For any curve $c$ and real number $h$, let $c_h$ be the curve defined by $c_h(t) = c(t+h)$.  If $\omega$ is any cogerm differential 1-form, then we define its **differential** $\mathrm{d}\omega$ by

$$ \langle \mathrm{d}\omega | c \rangle = \lim_{h\to 0} \frac{\langle \omega | c_h \rangle - \langle \omega | c\rangle}{h}. $$

Note that while the fraction on the right-hand side only makes sense for a specific representative curve $c$ and a sufficiently small $h$, the limit depends only on the germ of $c$.

Of course, in general, $\mathrm{d}\omega$ may not be defined on as many curves as $\omega$ is.

+-- {: .un_defn}
###### Definition
If $X$ is a smooth space, so that we have a notion of *smooth curve*, then we say that a cogerm differential 1-form $\omega$ is **smooth** if 

1. $\omega$ is defined on all germs of smooth curves, and
2. $\mathrm{d}\omega$ is smooth ([[coinductive definition|coinductively]]).
=--

For example, if $f:X\to \mathbb{R}$ is a [[smooth function]], then it is also a smooth cogerm differential 1-form, and its differentials $\mathrm{d}^n f$ are those mentioned above.  By stopping the coinduction at an appropriate point and requiring only [[continuous function|continuity]], we obtain an analogous definition of $k$-times [[continuously differentiable function]] $C^k$; for example, $\omega$ is $C^2$ if $\omega$, $\mathrm{d}\omega$, and $\mathrm{d}^2\omega$ are defined on all smooth curves and the last of these is continuous.  (But the obvious definition of [[differentiable function]] without continuity is too weak, even if we require $\mathrm{d}\omega$ to be defined on all differentiable germs, as the classic example of $x y^2/(x^2 + y^2)$ shows; extended continuously to the origin, this and its differential are defined on all smooth curves, although the differential is not continuous, but this function is not differentiable, which we know because its differential is not linear as a covector form.)

Note that the cogerm differential $\mathrm{d}$ is *not* the same as the exterior differential, except when applied to $0$-forms.  In particular, $\mathrm{d}^2 \neq 0$.

We have the expected multivariable chain rule:

+-- {: .un_theorem}
###### Theorem
If $\phi:\mathbb{R}^n\to \mathbb{R}$ is a [[differentiable function]] and $\omega_1,\dots,\omega_n$ are cogerm differential 1-forms, then
$$ \mathrm{d}(\phi(\omega_1,\dots,\omega_n)) = \partial_1\phi(\omega_1,\dots,\omega_n) \mathrm{d}\omega_1 + \cdots +  \partial_n\phi(\omega_1,\dots,\omega_n) \mathrm{d}\omega_n $$
where $\partial_i\phi$ denotes the partial derivative with respect to the $i^{th}$ variable.
=--

In particular, taking $\phi(x,y) = x y$, we have the product rule:

$$ \mathrm{d}(\omega\eta) = \omega \mathrm{d}\eta + \eta \mathrm{d}\omega. $$

This also enables us to calculate the iterated cogerm differentials of functions.  If $x:X\to \mathbb{R}$ is a "coordinate" and $f:\mathbb{R}\to \mathbb{R}$ is a function, so that $f(x) : X\to \mathbb{R}$ is a function of that coordinate, then by the theorem we have

$$\mathrm{d}f(x) = f'(x) \mathrm{d}x.$$

Thus, by the product rule, we have

$$ \mathrm{d}^2 f(x) = f''(x) \mathrm{d}x^2 + f'(x) \mathrm{d}^2x $$

and so on.  Note that the first formula justifies the common notation $\frac{\mathrm{d}f(x)}{\mathrm{d}x}$ for the derivative $f'(x)$, while the second *almost* justifies the common notation $\frac{\mathrm{d}^2f(x)}{\mathrm{d}x^2}$ for the second derivative $f''(x)$ --- it would be correct only if $\mathrm{d}^2x=0$, which is not generally the case.  Instead it would be better to write $f''(x) = \frac{\partial^2f(x)}{\partial x^2}$, indicating that $f''(x)$ is the coefficient of $\mathrm{d}x^2$ in a canonical expansion of $\mathrm{d}^2 f(x)$.


## Integration

Let $c:[a,b] \to X$ be a curve and $\omega$ a cogerm differential 1-form; we would like to integrate $\omega$ over $c$.  There are at least two possible definitions.

### Naive integration

The **naive integral** of $\omega$ over $c$ is defined to be

$$\int_c \omega = \int_{t=a}^b \langle \omega | c_t \rangle \mathrm{d}t. $$

if this exists.  If $\omega$ is an exterior differential $1$-form or an absolute differential $1$-form, then this agrees with its usual line integral over $c$.


### Genuine integration

The **(genuine) integral** of $\omega$ over $c$ is defined as follows.  Given a [[tagged partition]] $a = t_0 \lt t_1 \cdots \lt t_{n-1} \lt t_n = b$ with tags $t^*_i \in [t_{i-1},t_i]$, we define the corresponding [[Riemann sum]] to be

$$ \sum_{i=1}^n \langle \omega | \Delta t_i \cdot c_{t^*_i} \rangle $$

Here $\Delta t_i = t_i - t_{i-1}$, and for a curve $c$ and a number $h$ the curve $h\cdot c$ is defined by $(h\cdot c)(t) = c(h t)$.  Now we take the limit as the tagged partitions shrink.

It is convenient to do this in the manner of the [[Henstock integral]].  That is, we consider *gauges* $\delta : [a,b] \to \mathbb{R}_{\gt 0}$ and say that a tagged partition is *$\delta$-fine* if $[t_{i-1},t_i] \subset (t^*_i - \delta(t^*_i), t^*_i + \delta(t^*_i))$ for all $i$.  Then we say that a number $I$ is the integral $\int_c \omega$ if for all $\epsilon\gt 0$ there exists a gauge $\delta$ such that the Riemann sum of any $\delta$-fine tagged partition is within $\epsilon$ of $I$.

The genuine integral also agrees with the usual integral for exterior 1-forms, and probably also for absolute differential forms.  However, in other cases it disagrees with the naive integral.  In particular, it "detects only the degree-1 part" of a form, in a way that we can make precise as follows.


### Integration of negligible forms

Let us say that $\omega$ is **$o(dx)$** if $\lim_{h\to 0} \frac{\langle \omega | h\cdot c \rangle}{h} = 0$ for any curve $c$.  Some examples of forms that are $o(dx)$ are $\mathrm{d}x^2$ and $\mathrm{d}^2x$.

+-- {: .un_theorem}
###### Theorem
If $\omega$ is $o(dx)$, then $\int_c \omega = 0$ for any curve $c$.
=--
+-- {: .proof}
###### Proof
Suppose $\epsilon\gt 0$; then for any $t\in [a,b]$ there is a $\delta(t)$ such that ${\langle \omega {|} h \cdot c_t\rangle} \lt \frac{\epsilon}{b-a} h$ for any $0\lt h\lt \delta(t)$. This defines a gauge $\delta$ on $[a,b]$. Now suppose we have a $\delta$-fine tagged partition $a = x_0 \lt \cdots \lt x_n = b$ with tags $t_i \in [x_{i-1},x_i]$, so that $\Delta x_i = x_i - x_{i-1} \lt \delta(t_i)$. Then the corresponding Riemann sum is, by definition, $\sum_{i} \langle \omega {|} \Delta x_i \cdot c_{t_i}\rangle $. Since $\Delta x_i \lt \delta(t_i)$, each $\langle \omega {|} \Delta x_i \cdot c_{t_i}\rangle \lt \frac{\epsilon}{b-a} \Delta x_i$. Thus, when we sum them up, we get something less than $\frac{\epsilon}{b-a} \sum_i \Delta x_i = \frac{\epsilon}{b-a} (b-a) = \epsilon$. Thus, for any $\epsilon$ there is a gauge $\delta$ such that the Riemann sum over any $\delta$-fine tagged partition is $\lt\epsilon$; so the integral is zero.
=--

Thus, for instance, $\int_c \mathrm{d}^2 x = 0$ according to the genuine integral, while according to the naive integral it would be (by the fundamental theorem of calculus) $\langle \mathrm{d}x | c_b \rangle - \langle \mathrm{d}x|c_a \rangle = (x\circ c)'(b) - (x\circ c)'(a)$.

The answer $0$ given by the genuine integral is preferable if we regard $\mathrm{d}x$ as a "first-order change in $x$", so that $\mathrm{d}x^2$ or $\mathrm{d}^2x$ are "second-order" quantities and hence ought to be negligible.  For instance, we usually compute the area under a curve $y=f(x)$ between $x=a$ and $x=b$ by dividing the interval $[a,b]$ into subintervals of width $\Delta x$ and approximating the area for each subinterval using a rectangle, obtaining $f(x) \Delta x$.  This leads us to integrate the differential form $f(x) \mathrm{d}x$.

However, a *better* approximation would be to replace the rectangle with a trapezoid, having an area of $\frac{1}{2}(f(x+\Delta x) + f(x))\Delta x$.  At least if $f$ is differentiable, we can approximate $f(x+\Delta x)$ by $f(x) + f'(x) \Delta x$, and thus approximate the area by 
$$ \frac{1}{2}(f(x) + f'(x)\Delta x + f(x))\Delta x = f(x) \Delta x + \frac{1}{2} f'(x) (\Delta x)^2. $$
This would lead us to integrate the form $f(x) \mathrm{d}x + \frac{1}{2} f'(x) \mathrm{d}x^2$.  Since this is based on a better approximation, we should expect it to give at least as good an answer.  And with the genuine integral it does give the same answer, since the additional term $\frac{1}{2} f'(x) \mathrm{d}x^2$ is $o(dx)$ and hence has vanishing integral.  But with the naive integral, it does not.


### The fundamental theorem of calculus

The naive integral satisfies a fundamental theorem of calculus for all cogerm forms: for any $\omega$ we have

$$\int_c \mathrm{d}\omega = \langle \omega| c_b\rangle - \langle \omega | c_a \rangle. $$

This follows directly from the definition of the naive integral and the cogerm differential $\mathrm{d}$.

The genuine integral does not satisfy as general a fundamental theorem of calculus as the naive integral.  It does, however, satisfy FTC for differentials of *functions*:
$$ \int_c \mathrm{d}f = f(c(b)) - f(c(a))$$
This can be proven in exactly the same way as the usual FTC for (line) integrals.

The restriction of FTC to differentials of functions is fairly natural if we recognize that FTC is a special case of the generalized [[Stokes' theorem]], which is about *exterior* differentials of forms, not the commutative cogerm differential.  It just so happens that if $f$ is a function, then the exterior differential of $f$ regarded as a 0-form agrees with the cogerm differential of $f$ regarded as a cogerm 1-form.


### Existence of integrals

The existence of naive integrals is fairly easy to verify, since they are just defined in terms of ordinary 1-variable integrals.  But the existence of genuine integrals is rather less obvious.  Here we prove that they exist for at least one reasonably general class of forms.

Recall that a *1-cojet differential 1-form* is a cogerm 1-form that depends only on the 1-jet of a curve, i.e. its value and its tangent vector.  A 1-cojet form is equivalently just a function (not necessarily linear) on the [[tangent bundle]] $T X$; we may write it as $\omega(\mathbf{x},\mathrm{d}\mathbf{x})$, where $\mathbf{x}$ is a point of $X$ (with coordinates $x$, $y$, $z$, ...) and $\mathrm{d}\mathbf{x}\in T_{\mathbf{x}}X$ a tangent vector at $\mathbf{x}$ (with coordinates $\mathrm{d}x$, $\mathrm{d}y$, $\mathrm{d}z$, ...).

+-- {: .un_theorem}
###### Theorem
Suppose $\omega$ is a 1-cojet differential form and that

1. $\omega(\mathbf{x},0) = 0$ for all $\mathbf{x}$.

2. For each $\mathbf{x}\in X$ and $\mathrm{d}\mathbf{x}\in T_{\mathbf{x}}X$ the function $\lambda h.\omega(\mathbf{x},h \, \mathrm{d}\mathbf{x}):\mathbb{R} \to \mathbb{R}$ is differentiable from the right at $h=0$, and the derivative of the above function is continuous as a function on $T X$.

Then the genuine integral of $\omega$ over any differentiable curve exists.
=--
+-- {: .proof}
###### Proof
The Riemann sums in the definition of the genuine integral simplify in the case of a 1-cojet form to
$$ \sum_{n=1}^\infty \omega(c(t^*_i), \Delta t_i \cdot c'(t^*_i)). $$
Note that $\Delta t_i = t_i - t_{i-1}$ is always positive.
By the assumptions, for any positive $h$ we can write
$$\omega(\mathbf{x}, h\cdot \mathrm{d}\mathbf{x}) = f(\mathbf{x}, \mathrm{d}\mathbf{x})\, h + g(\mathbf{x}, \mathrm{d}\mathbf{x},h)\,h  $$
where $f$ is continuous and $\lim_{h\to 0} g(\mathbf{x},\mathrm{d}\mathbf{x},h) = 0$.  Therefore the Riemann sum is
$$ \sum_{n=1}^\infty f(c(t^*_i), c'(t^*_i))\,\Delta t_i + g(c(t^*_i), c'(t^*_i),\Delta t_i)\,\Delta t_i. $$
Now, essentially the same argument as in the proof that $o(dx)$ forms have zero integral shows that the second term can be neglected; thus we may as well consider only
$$ \sum_{n=1}^\infty f(c(t^*_i), c'(t^*_i))\,\Delta t_i $$
However, this is just an ordinary Riemann sum for computing the integral
$$ \int_{t=a}^b f(c(t),c'(t)) \, \mathrm{d}t. $$
Since $f$ is assumed continuous, this integral exists.
=--

The hypotheses of this theorem are a bit restrictive, but they include both the usual exterior 1-forms and [[absolute differential forms]] such as ${|\mathrm{d}x|}$ and $&#273;l = \sqrt{\mathrm{d}x^2+\mathrm{d}y^2}$.  The latter are not differentiable at $\mathrm{d}\mathbf{x}=0$, but they do have one-sided derivatives along any line approaching the origin.  It is also necessary to *exclude* forms such as the following:

* A function on $X$, regarded as a cogerm differential form.  If such a function is nonzero on any region, then its genuine integral will diverge.  These are excluded by requirement (1).

* Forms such as $\sqrt{\mathrm{d}x}$, whose genuine integral also diverges.  These are excluded by requirement (2).

There are, however, some cogerm forms that are not 1-cojet forms, nor are they $o(dx)$, yet their geniune integrals exist.  An example is $\sqrt{\mathrm{d}^2x}$, whose genuine integral over a curve $c:[a,b]\to X$ is essentially $\int_{t=a}^b \sqrt{(x\circ c)''(t)} \,\mathrm{d}t$.  There is probably a generalization of the above existence theorem to $k$-cojet forms, involving somewhat more complicated vanishing and differentiability conditions.


### Parametrization invariance

Since both naive and genuine integrals agree with ordinary line integrals when restricted to exterior 1-forms, such integrals are invariant under orientation-preserving reparametrization.  However, for general cogerm 1-forms, neither integral is so invariant.  Nevertheless, we may ask for conditions under which they are.

The naive integral is very much not invariant under reparametrization.  This is most obvious when $\omega$ is just a function, in which case its integral is just its ordinary integral.  Similarly, a naive integral like $\int_c \mathrm{d}^2 x$, which equals $(x\circ c)'(b) - (x\circ c)'(a)$ by FTC, is not invariant under reparametrization since it involves the derivative of the coordinate function of $c$.

The genuine integral is somewhat more invariant under reparametrization.  For instance,

* Since the genuine integral $\int_c \omega = 0$ whenever $\omega$ is $o(dx)$, independently of whatever $c$ might be, any such integral is parametrization-independent.

* The genuine integral of any form along any curve is invariant under orientation-preserving *affine* reparametrization.  This follows fairly directly from its definition.

There are forms whose genuine integral exists, but is not parametrization-invariant, such as $\sqrt{\mathrm{d}^2x}$.  However, we can isolate a useful class of forms, including both exterior forms and absolute forms, whose genuine integral is so invariant.  This is most easily done by reformulating the integral, as follows.


### Affine integration 

For 1-cojet differential 1-forms satisfying a weak sublinearity condition, there is an equivalent definition of the genuine integral that is more obviously parametrization-invariant.

A 1-cojet form can be considered as a function on tangent vectors $(x,v)$ where $v\in T_x X$.  Let us say that such a form $\omega$ is **tangent-Lipschitz** if for each $x\in X$ there is a constant $L\gt 0$ such that
$$ {|\omega(x,v) - \omega(x,w)|} \lt L \,\Vert v-w\Vert $$
for all $v,w\in V$.  Here we are using a [[norm]] on the tangent space $T_x X$.  Since this vector space is finite-dimensional, the notion of tangent-Lipschitz is independent of the norm chosen (although the numerical value of $L$ will vary with the norm).

Note that this says nothing at all about the continuity of $\omega$ as a function of $x$.  In particular, if each $\omega(x,-)$ is separately either linear or absolute, then $\omega$ is tangent-Lipschitz.  Thus, tangent-Lipschitz is a weak replacement for linearity in the tangent variable.

To define our new version of the integral, suppose first that $X$ is a finite-dimensional real [[affine space]], regarded as a smooth manifold.  Then we can canonically identify all its tangent spaces with the same vector space $V$.

Let $c:[a,b]\to X$ be a curve in such an affine space $X$, and $\omega$ a 1-cojet differential 1-form on some open subset $U\subseteq X$ containing the image of $c$.  Then we can regard $\omega$ as a function $U\times V\to \mathbb{R}$.  Now for any [[tagged partition]] $a = t_0 \lt t_1 \cdots \lt t_{n-1} \lt t_n = b$ with tags $t^*_i \in [t_{i-1},t_i]$, we define the corresponding [[Riemann sum]] to be

$$ \sum_{i=1}^n \omega(c(t^*_i), \Delta c_i) $$

where $\Delta c_i = c(t_i) - c(t_{i-1})$, the subtraction being the usual way to subtract points in an affine space and obtain a vector.  We then take the limit of such Riemann sums in the Henstock way, as before; let us call this the **affine integral**.

Note that this Riemann sum manifestly depends only on the points $c(t_i)$ and $c(t^*_i)$ (and the order in which they occur).  Thus, any increasing bijection $\phi:[a',b'] \to [a,b]$ induces a bijection between tagged partitions which respects their Riemann sums.  It also maps intervals to intervals, so any gauge on one interval induces one on the other interval.  Thus the limits also coincide (in the strong sense that one exists if and only if the other does, and in that case they are equal), and so the affine integral is completely parametrization-independent.

We now show that the affine integral agrees with the genuine integral.  

+-- {: .un_theorem}
###### Theorem
If $\omega$ is a tangent-Lipschitz 1-cojet form on an open subset of an affine space $X$, then its genuine and affine integrals over any differentiable curve agree, in the strong sense that each exists if and only if the other does and in that case they are equal.
=--
+-- {: .proof}
###### Proof
Let $c:[a,b]\to X$ be differentiable.  Then by definition of differentiability, for any $t_1 \lt t^*\lt t_2$ in $[a,b]$ we can write
$$ c(t_2) - c(t_1) - c'(t^*)(t_2-t_1) = g(t^*,t_1,t_2)(t_2-t_1) $$
where $g(t^*,t_1,t_2) \to 0$ as $t_2-t_1 \to 0$.  Thus, since $\omega$ is tangent-Lipschitz, for any tagged partition we have
$$ {|\omega(c(t^*_i), \Delta c_i) - \omega(c(t^*_i),\Delta t_i \cdot c'(t^*))|} \lt L \Vert g(t^*,t_1,t_2) \Vert \cdot \Delta t_i. $$
Since $g(t^*,t_1,t_2) \to 0$ as $t_2-t_1 \to 0$, we can choose gauges to make this difference vanish in the limit, just as we did for integrating $o(dx)$ forms.  But $\omega(c(t^*_i), \Delta c_i)$ and $\omega(c(t^*_i),\Delta t_i \cdot c'(t^*))$ are exactly the terms in the Riemann sums for the affine and genuine integrals.
=--

Finally, a similar argument shows that the affine integral can be extended to all finite-dimensional smooth manifolds by local charts.

+-- {: .un_theorem}
###### Theorem
Let $U\subseteq X$ and $V\subseteq Y$ be open subsets of affine spaces and $\phi:U\to V$ be differentiable.  Let $\omega$ be a tangent-Lipschitz 1-cojet form on $V$ and $c:[0,1]\to U$ a differentiable curve.  Then for the affine integrals we have
$$ \int_c \phi^*\omega = \int_{\phi c} \omega. $$
=--
+-- {: .proof}
###### Proof
By definition, $\phi^*\omega(x,v) = \omega(\phi(x),d_x\phi(v))$.  Thus, the LHS is a limit of Riemann sums of the form
$$ \sum_i \omega(\phi(c(t^*_i)),d_{c(t^*_i)}\phi(\Delta c_i)). $$
while the RHS is a limit of sums of the form
$$ \sum_i \omega(\phi(c(t^*_i)),\Delta (\phi c)_i). $$
Since $\phi$ is differentiable, for any point $c(t^*_i)$ we have
$$ \Delta (\phi c)_i = \phi(c(t_{i})) - \phi(c(t_{i-1})) = d_{c(t^*_i)}\phi(\Delta c_i) + E(c(t^*_i),\Delta c_i)\cdot {\Vert \Delta c_i \Vert } $$
where $E(c(t^*_i),\Delta c_i)\to 0$ as $t_i - t_{i-1} \to 0$.  Since $\omega$ is tangent-Lipschitz, this gives
$$  \Big\Vert \omega(\phi(c(t^*_i)),\Delta (\phi c)_i) - \omega(\phi(c(t^*_i)),d_{c(t^*_i)}\phi(\Delta c_i)) \Big\Vert \lt L \cdot E(c(t^*_i),\Delta c_i) \cdot {\Vert \Delta c_i \Vert }. $$
Now $L$ and $E$ depend on the point chosen, but nevertheless, we can choose gauges as before to make this term vanish in the limit.  Thus, the two integrals agree.
=--


### Stieltjes integrals, $\delta$-functions, and distributions

An alternative approach to proving FTC would be to observe that essentially by definition of $\mathrm{d}f$, the form
$$ f(x+\mathrm{d}x) - f(x) - \mathrm{d}f $$
is $o(dx)$.  Therefore, $\int_c \mathrm{d}f = \int_c (f(x+\mathrm{d}x)-f(x))$ if either exists.  If the latter integral can be calculated using only partitions tagged by their left endpoint, then it is obviously $f(c(b))-f(c(a))$ --- but it is not clear that such partitions suffice.

In the list of examples above, we denoted $f(x+\mathrm{d}x)-f(x)$ by $\Delta f$.  More generally, we might expect that integration of $\Delta f$ (perhaps multiplied by another function $g$) is a sort of [[Stieltjes integration]].  However, it is again not clear whether left endpoints suffice.

We can, at least, show that the second definition of the [[Dirac delta function]] has its expected properties.  Recall that this was
$$ \delta =
  \begin{cases}
    \frac{1}{|\mathrm{d}x|} &\qquad x=0 \;and\; \mathrm{d}x\neq 0\\
    0 &\qquad otherwise.
  \end{cases}
$$

+-- {: .un_theorem}
###### Theorem
For any function $f:\mathbb{R}\to \mathbb{R}$, if $a\le 0 \le b$ then we have $\int_a^b f(x)\, \delta \,\mathrm{d}x = f(0)$ for the affine integral.
=--
+-- {: .proof}
###### Proof
We define a gauge, denoted $\eta$ (since the letter $\delta$ is already in use) as follows:
$$\eta(x) =
\begin{cases}
  \infty &\qquad x=0\\
  {|x|} &\qquad x\neq 0.
\end{cases}
$$
Then in any $\eta$-fine tagged partition, $0$ must be the tag of the subinterval containing it.  Therefore, the Riemann sum of $f(x)\, \delta \,\mathrm{d}x$ over any such tagged partition is simply
$$ f(0) \frac{1}{|\mathrm{d}x|} \mathrm{d}x $$
where $\mathrm{d}x$ is the width of the subinterval containing $0$.  But this is positive, so the Riemann sum is simply $f(0)$.  Thus, the integral equals $f(0)$.
=--

One might instead define $\delta$ to be $1$ if $x=0$, so that we would integrate $f(x)\, \delta$ rather than $f(x) \,\delta \,\mathrm{d}x$.  Our choice matches more closely the common informal notation "$\int f(x)\, \delta(x)\,\mathrm{d}x$", although of course here $\delta$ is a function of $\mathrm{d}x$ as well as $x$.  Our choice also gives $\delta$ the usual scaling and precomposition properties, usually written as

$$ \delta(\alpha x) = \frac{\delta(x)}{|\alpha|}$$

$$ \delta(g(x)) = \sum_{g(c)=0} \frac{\delta(x-c)}{|g'(c)|}$$

In our notation, instead of $\delta(g(x))$ we would write $\delta(g(x),\mathrm{d}g)$, which is how we precompose a differential form with a function; the above formulas then follow from $\mathrm{d}g = g'(x)\,\mathrm{d}x$.

Note that $\delta$-functions are usually defined as measures or distributions, which are integrated over *unoriented* regions.  Since our integrals are oriented, we have to specify that $[a,b]$ is traversed left-to-right (as in the notation $\int_a^b$) in order to get $f(0)$ as the answer; if we integrated $\int_b^a$ instead we would get $-f(0)$.

We can, of course, avoid the minus sign by integrating against $\delta\,|\mathrm{d}x|$ instead of $\delta \,\mathrm{d}x$.  (We could also omit the absolute value in the definition of $\delta$, but this would break the usual scaling properties.)

Since we have successfully represented the $\delta$-distribution as a cogerm differential form, one may wonder whether other distributions can also be so represented.  It is unclear to me whether this is possible.  For instance, if $\phi_\epsilon$ are test functions converging to a distribution $\theta$ as $\epsilon\to 0$, we could consider a differential form such as $\theta(x,\mathrm{d}x) = \phi_{\mathrm{d}x}(x)$, but it's not clear whether this would have the right behavior under integration.


## Higher forms

One can define a **cogerm differential $k$-form** to be a function on germs of $k$-dimensional hypersurfaces in $X$.  These include in particular the usual [[differential form|exterior]] differential $k$-forms as well as [[absolute differential form|absolute]] differential $k$-forms.  And they can be integrated over $k$-dimensional hypersurfaces, by a similar formula as above.

There is a sort of "**exterior differential**" acting from cogerm $k$-forms to cogerm $(k+1)$-forms, which we denote by $(\mathrm{d}\wedge -)$ to avoid confusion with the commutative cogerm differential $\mathrm{d}$.  When $k=1$, the definition is

$$ \langle \mathrm{d}\wedge \omega {|} c \rangle = \lim_{A \to 0} \frac{1}{\Vert A \Vert} \oint_{c(\partial A)} \omega. $$

Here the limit is over some neighborhoods $A$ of $0\in\mathbb{R}^2$ whose areas $\Vert A \Vert$ shrink to zero, and the integral over the boundary is defined as above.  The definition for general $k$ is similar.

This limit can only exist if the integral $\oint_{c(\partial A)} \omega$ is invariant under oriented reparametrization of $\partial A$.  Moreover, if $\omega$ is an absolute form, then usually there will not be enough cancellation to make the limit above finite (it would be analogous to defining a 1-dimensional "derivative" as $\lim_{h\to 0} \frac{f(x+h)+f(x)}{h}$ rather than $\lim_{h\to 0} \frac{f(x+h)-f(x)}{h}$).  Thus, this "exterior differential" seems barely (if at all) more general than the usual one acting on exterior $k$-forms.

It is unclear whether there is a notion of exterior differential which is significantly more general.  Similarly, it is unclear whether the wedge product of exterior forms can be sensibly extended to cogerm ones, or whether there is a sensible commutative cogerm differential $\mathrm{d}$ acting on cogerm $k$-forms for $k\gt 1$.


## Nonsymmetrized version

More general than cojet forms (but analytic), we have the _coflare differential forms_, in which there are any number of differentials (or higher differentials) $\mathrm{d}_{0}x$, $\mathrm{d}_{1}x$, $\mathrm{d}_{1,0}x = \mathrm{d}_{1}\mathrm{d}_{0}x$, etc.  Whereas jets are based on the [[tangent bundle]] $T X$, flares (of rank, say, $3$) are based on the iterated tangent bundle $T (T (T X))$.  Both cojet forms and [[exterior differential forms]] are included in the calculus of coflare forms, as are nonlinear versions of exterior forms such as [[absolute differential forms]].  The differentials in cojet forms always have the subscript $0$ (which we may take to be the default), while the exterior form $\mathrm{d}x \wedge \mathrm{d}y$ is really $\mathrm{d}_{0}x \mathrm{d}_{1}y - \mathrm{d}_{1}x \mathrm{d}_{0}y$ (possibly divided by $2!$, depending on your conventions).

A more abstract version of coflare forms (including both cogerm forms and the coflare forms of the previous paragraph) may be based on germs of maps with domain $\mathbb{R}^p$ instead of only curves (with domain $\mathbb{R}$).  To fix notation, number the coordinates on $\mathbb{R}^p$ from $0$ to $p - 1$; if $\phi$ is a partial function from $\mathbb{R}^p$ to $\mathbb{R}$ and $U$ is the subset of $\dom \phi$ on which $\phi$ is (say) $3$-times differentiable, then write $\mathrm{D}_{i,j,k}\phi\colon U \to \mathbb{R}$ for the third partial derivative of $\phi$ with respect to variable $i$, variable $j$, and variable $k$ (in any order).  Then if $c$ is a thrice-differentiable function to $X$ from a neighbourhood of the origin in $\mathbb{R}^p$ and $f$ is a thrice-differentiable function to $\mathbb{R}$ from a neighbourhood of $c(0)$ in $X$, then we have $\langle \mathrm{d}_{i,j,k}f | c \rangle \coloneqq \mathrm{D}_{i,j,k}(f \circ c)(0)$, etc.

Even more abstractly, there is no reason to limit the domain of $c$ to $\mathbb{R}^p$, although it\'s not clear if the forms on more general classes of germs correspond to anything of independent interest.


## References

* nForum discussions: [I](http://nforum.ncatlab.org/discussion/5402/what-is-a-variable/), [II](http://nforum.ncatlab.org/discussion/5518/differentials/), [III](http://nforum.ncatlab.org/discussion/5700/cogerm-forms/) (merged into [the page discussion](https://nforum.ncatlab.org/discussion/8552/)), [IV](http://nforum.ncatlab.org/discussion/5817/cojet-differential-forms/), [V](http://nforum.ncatlab.org/discussion/5941/higher-differentials-again/), [VI](https://nforum.ncatlab.org/discussion/7636/coflare-differential-forms/).

Historical reference saved for later reading:

* Henk Bos (1973). Differentials, Higher-Order Differentials and the Derivative in the Leibnizian Calculus. Archive for History of Exact Sciences 14:1--90. [DOI](http://dx.doi.org/10.1007%2FBF00327456). [PDF](http://www.tau.ac.il/~corry/teaching/toldot/download/Bos1974.pdf) hosted by Leo Corry.


[[!redirects cogerm differential form]]
[[!redirects cogerm differential forms]]
[[!redirects cogerm form]]
[[!redirects cogerm forms]]

[[!redirects cojet differential form]]
[[!redirects cojet differential forms]]
[[!redirects cojet form]]
[[!redirects cojet forms]]
