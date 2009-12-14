Recall that an [[isometry]] between two [[Riemannian manifolds]] $(M,g), (N,h)$ is a diffeomorphism $\phi: M \to N$ such that $\phi^* h = g$.  In other words, $\phi$ respects the Riemannian structure as well as the differentiable structure.  

It follows that if $d,d'$ are the metrics on $M,N$ induced by the Riemannian metrics $g,h$, then $d'(\phi(x),\phi(y)) = d(x,y)$ for $x,y \in M$---that is, $\phi$ is distance-preserving.
Interestingly, a version of  the converse is true, according to the Myers-Steenrod theorem:

_If $\phi: M \to N$ is distance-preserving and surjective, then it is an isometry (in particular, it is smooth)._

For notational simplicity, assume $N=M$.

$\phi$ is evidently a homeomorphism.  Now pick $p \in M$ and a neighborhood $D_r(p)$ such that for any $q \in D_r(p)$, there is a unique geodesic in that neighborhood connecting $p,q$.  Call it $\gamma$.   I claim that $\phi \circ \gamma$ is a geodesic in $N$.
 
The geodesic $\gamma$ can be assumed to be parametrized by unit length. We have for all $t$, 
\[ d(p,q) = d(\gamma(t),p) + d(\gamma(t), q).\]
Thus 
\[ d(\phi(p),\phi(q)) = d(\phi(\gamma(t)),\phi(p)) + d(\phi(\gamma(t)), \phi(q)) \ \ (*).\]
In other words, we have strict equality in the triangle inequality.  

##Geodesic preservation##

In a Riemannian manifold $M$, if $q,r$ lie in a small neighborhood of $p$ and 
\[ d(q,r) + d(r,p)  = d(q,p) ,\]
then $r$ lies on a geodesic betwen $p,q$.  
Indeed, draw a geodesic $\alpha$ from $q$ to $r$ and a geodesic $\beta$ from $r$ to $p$ that travel at unit speed and minimze the distances; we can do this locally even without the assumption of completeness.  The catenation $\alpha \beta$ minimizes the length from $q$ to $p$, so it is an unbroken geodesic.  Thus $r$ lies on the geodesic.

So, returning to the discussion above, we see that by (*) $\phi$ \emph{sends geodesics to geodesics.}

##Exponential coordinates##

Now fix open $U \subset T_p(M),V \subset T_q(N)$ containing the origin such that $\exp_p$ takes $U$ diffeomorphically to a neighborhood $D_r(p)$, and $\exp_q$ takes $V$ diffeomorphically to $D_r(q)$.  There is an expression for $\phi$ as a map $\tilde{\phi}: U \to V$ in these exponential coordinates.  
It is obtained as follows: if $v \in U$, take a geodesic $\gamma_v$ with $\gamma_v'(0) = v$ and consider $(\phi \circ \gamma_v)'(0)$.  In fact this induces more generally a map
\[ \tilde{\phi}: T_p(M) \to T_q(M).\]
Since $\gamma_v$ moves at constant speed $|v|$ and $\phi \circ \gamma_v$ moves at the same speed, it follows that
$\tilde{\phi}$ is norm-preserving.  Also $\tilde{\phi}(0) = 0$.  If we can show that $\tilde{\phi}$ is linear, then we'll get smoothness in this exponential coordinate system---hence smoothness in general.

##$\tilde{\phi}$ is an isometry##

It can be checked that
\[ \boxed{\lim_{A,B \to 0 \in T_p(M)} \frac{d(\exp_p(A),\exp_p(B)) }{|A-B|} } = 1.\]
We will postpone this for now.

This is what we will use to show that $\tilde{\phi}: T_p(M) \to T_q(M)$ is an isometry, where each tangent space is given the norm from the Riemannian metric.  Pick $A,B \in T_p(M)$ and consider the    geodesics $\gamma_{A},\gamma_{B}$ at $p$ and $\gamma_{A'}, \gamma_{B'}$ where $A'=\tilde{\phi}(A), B' = \tilde{\phi}(B)$.
Then $d(\gamma_{A}(t), \gamma_{B}(t)) = d( \gamma_{A'}(t), \gamma_{B'}(t))$.
So 
\[ 1=  \lim_{t \to 0} \frac{d(\exp_p(tA),\exp_p(tB)) }{t|A-B|} 
=  \lim_{t \to 0} \frac{d(\exp_q(tA'),\exp_q(tB')) }{t|A-B|}  = \frac{|A'-B'|}{|A-B|}.\]



To show that $\tilde{\phi}$ is linear, we appeal to a general fact:

 Let $X,Y$ be normed linear spaces and $T: X \to Y$ a map such that $|Tx - Tx'|  = |x-x'|$ for $x,x' \in X$. Then $T$ is linear if $T(0) = 0$.




##Conclusion of the proof##

Now we have seen that $\phi$ is smooth, and that for $v \in T_p(M)$, $|v|_p = |\phi_*(v)|_{\phi(p)}$, i.e. $\phi$ preserves lengths on tangent vectors.  By the polarization identity, $\phi$ preserves the inner product, and is thus an isometry.

  



##A   lemma##

We never proved a fact  about the exponential map---the equality 
\[ \lim_{A,B \to 0 \in T_p(M)} \frac{d(\exp_p(A),\exp_p(B)) }{|A-B|} = 1.\]
We will briefly sketch the idea here.  $|A-B|$ is the length of the linear  path from $A $ to $B$ in $T_p(M)$, so it will be sufficient to show:

_If $c:(0,1) \to T_p(M)$ is a path in $T_p(M)$, then as $c((0,1)) \to 0$ with the derivative $|c'|$ staying bounded, 
\[ \frac{ l(\exp_p(c))}{l(c)} = 1.\]
_

We are  abusing notation quite a bit here, but it should  not cause confusion.

The reason is that
\[ l(c) = \int |c'| \]
while
\[ l(\exp_p(c)) = \int | (\exp_p)_{*c(t)} c'(t) |_{\exp_p(c(t))} \]
where in the second equation we are referring to the norms induced by the metric on the various tangent spaces of $M$.
The difference between these two is $o(l(c))$, because $\exp_p$ has derivative the identity at $0 \in T_p(M)$, and the metric on $T_{\exp_p(c(t))}(M)$ is very close (say by a factor of $1 \pm \epsilon$) to that of $T_p(M)$ if we work in local coordinates and agree to identify the tangent spaces.