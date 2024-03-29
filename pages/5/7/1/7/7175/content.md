
# Extrema
* table of contents
{: toc}

## Idea

In general, a __maximum__ is a [[top element]], a __minimum__ is a [[bottom element]], and an __extremum__ is either.  However, these terms are typically used in [[analysis]], where the [[order theory]] is secondary.  One also usually speaks of extrema of a [[function]], meaning a top or bottom element of the [[range]] of the function under its induced order as a [[subset]] of an ordered codomain.  In this context, one also considers *local* extrema of functions; a __local extremum__ of $f$ is an extremum of a [[restriction]] of $f$ to an [[open subspace]] of its original domain.  In any case, the extremum is __strict__ if the function takes the extreme value only once (in the relevant domain).


## Local extrema of differentiable functions

We list some sufficient and necessary conditions for a (nice) function $f$ on a [[smooth manifold]] to have a local extremum at a point $x$. As these are local conditions, we may assume $f$ is a function $U \to \mathbb{R}$ where $U$ is an [[open subset]] in a [[Cartesian space]] $\mathbb{R}^n$. These conditions fall under the rubric of "second derivative test". 

Assume $f$ to be a twice-[[differentiable function]], and let $x$ in its [[domain]] be a [[critical point]]: a point where its [[derivative]] / [[Jacobian]] vanishes. Let $H_x(f)$ be the [[Hessian matrix]] of the function. Recall that $x$ is a **nondegenerate** critical point if the symmetric [[matrix]] $H_x$ is nondegenerate; equivalently, if $0$ is not an [[eigenvalue]] of $H_x$. 

Let $x$ be a nondegenerate critical point. Then  

* For $x$ to be a **strict local minimum** within some neighborhood, it is necessary and sufficient that $H_x(f)$ be a [[positive definite form]]. 

* For $x$ to be a **strict local maximum** within some neighborhood, it is necessary and sufficient that $H_x(f)$ be a [[negative definite form]]. 

(The only other possibility left for a nondegenerate critical point is that $H_x(f)$ be an [[indefinite form]], having a mix of positive and negative eigenvalues. In this case, $x$ is a **saddle point**. For more on this, see [[Morse theory]].) 

If $x$ is a _degenerate_ critical point (so $0$ is an eigenvalue of $H_x$), we have: 

* For $x$ to be a **local minimum**, it is necessary that $H_x(f)$ be a [[positive semidefinite form]], i.e., that all eigenvalues are nonnegative.

* For $x$ to be a **local maximum**, it is necessary that $H_x(f)$ be a [[negative semidefinite form]], i.e., that all eigenvalues are nonpositive.

These conditions are not sufficient. For a simple example, the origin in $\mathbb{R}^2$ is a critical point of $f(x, y) = x^3 - y^3$, where the Hessian is the zero matrix (hence positive semidefinite and negative semidefinite), but clearly the origin is neither a local maximum nor a local minimum. 


[[!redirects extremum]]
[[!redirects extrema]]
[[!redirects minimum]]
[[!redirects minima]]
[[!redirects maximum]]
[[!redirects maxima]]

[[!redirects local extremum]]
[[!redirects local extrema]]
[[!redirects local minimum]]
[[!redirects local minima]]
[[!redirects local maximum]]
[[!redirects local maxima]]

[[!redirects strict extremum]]
[[!redirects strict extrema]]
[[!redirects strict minimum]]
[[!redirects strict minima]]
[[!redirects strict maximum]]
[[!redirects strict maxima]]

[[!redirects strict local extremum]]
[[!redirects strict local extrema]]
[[!redirects strict local minimum]]
[[!redirects strict local minima]]
[[!redirects strict local maximum]]
[[!redirects strict local maxima]]
