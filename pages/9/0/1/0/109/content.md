The following lists  some detailed examples for [[BV theory|Lagrangian BV formalism]].


#BV integration on cylinder modulo rotation#

(... warning, this is unpolished and unfinished at the moment, I am running out of time...)

To illustrate the BV integration method, 
choose an example which is trivial as an 
ordinary integration problem and 
artificially add a bit of redundancy to see how
the BV machinery in turn gets rid of that.

So consider the real line
by regarding it as the quotient of the 
action  

$$
  a : (\mathbb{R}\times S^1) \times U(1)
   \to (\mathbb{R}\times S^1)
$$

of $U(1)$
on the cylinder $X := \mathbb{R} \times S^1$ by rotation
around the main axis.

The corresponding action [[Lie groupoid]] is

$$
  (\mathbb{R}\times S^1)//U(1)
  :=
  (X \times U(1)
  \stackrel{\stackrel{s := p_1}{\to}}{\stackrel{\to}{t:= a}}
  )
  \,.
$$

Its [[Lie algebroid]] is given by the anchor map

$$
  \mathfrak{g}
  :=
  \array{
     X \times \mathbb{R}
     &\hookrightarrow&
     T x
     \\
     & \searrow \swarrow
     \\
     & X
  }
$$

which includes the bundle of vectors that circle around the
cylinder into the full tangent bundle of the cylinder.

The Lie algebra on the sections restricts over 
each point of $\mathbb{R}$ to the Lie algebra of vector
fields on $S^1$.

The [[Chevalley-Eilenberg algebra]] of functions on 
this [[[Lie algebroid]] is generated over 
$C^\infty(X)$ from a single 
generator $\theta$ in degree 1, which we can think
of as a multiple of the the canonical 1-form on $S^1$
pulled back along the canonical projection
$p_2 : \mathbb{R} \times S^1 \to S^1$:

$$
  \mathrm{CE}(\mathfrak{g})
  =
  ( \wedge^\bullet_{C^\infty(X) \langle \theta\rangle}, d_{\mathfrak{g}})
  =
  ( C^\infty(X) \oplus C^\infty(X)\otimes \theta, d_{\mathfrak{g}})
  \,.
$$

If we write  $v \in \Gamma(T X)$ 
for the canonical vector field running around the
cylinder, i.e. the push-forward of the canonical vector
field on $S^1$ along the action $a$, then the differential
here is given by

$$
  d_{\mathfrak{g}} f = v(f) \cdot \theta
$$

for all $f \in C^\infty(X)$, and

$$
  d_{\mathfrak{g}} \theta = 0
  \,.
$$

We say

* $f \in C^\infty(X)$ are the **fields**

* $\theta$ is the **ghost**

* $d_{\mathfrak{g}}$ is the **BRST operator** 

* $\mathrm{CE}(\mathfrak{g})$ is the **BRST complex**

Next there is the corresponding [[Weil algebra]],
equivalently 
the algebra of differential forms on our Lie algebroid,
equivalently the algebra of [[differential forms in supergeometry|functions on the shifted
tangent bundle on our Lie algebroid]]:

$$
  \mathrm{W}(\mathfrak{g})
  :=
  \Omega^\bullet(\mathfrak{g})
  :=
  C^\infty(T[1]\mathfrak{g})
  :=
  (
    \Omega^\bullet(X)\otimes_{C^\infty(X)}
    (\langle \theta\rangle \oplus \langle d\theta\rangle) 
    ,
    d_{\mathrm{W}(\mathfrak{g})}
  )
  \,,
$$

whose differential acts as

$$
  d_{\mathrm{W}(\mathfrak{g})} f = v(f)\theta + d_{\mathrm{dR}}f 
$$
$$
  d_{\mathrm{W}(\mathfrak{g})} d f = 0
$$

for all $f \in C^\infty(X)$ and

$$
  d_{\mathrm{W}(\mathfrak{g})} \theta = d\theta
$$

$$
  d_{\mathrm{W}(\mathfrak{g})} d\theta = 0
$$

The ordinary canonical form on the cylinder, 
$\omega \in \Omega^2(X)$ corresponds here to the
element

$$
  \omega = d x\wedge \theta
$$

in $\mathrm{W}(\mathfrak{g})$ (with $x$ the canonical coordinate function
pulled back from $\mathbb{R}$). This, however, is not
a closed form in $\mathrm{W}(\mathfrak{g})$, as we have

$$
  d_{\mathfrak{g}} (dx \wedge \theta) = - dx \wedge d\theta
  \neq 0
  \,.
$$

To do BV integration we need to choose some closed form
$\mu \in \mathrm{W}(\mathfrak{g})$.
A given choice will allow us to integrate $\mu$ or any
form obatained from it by contraction with a multivector field,
over suitable sub-supermanifolds.

We want to recover from all this machinery the ordinary integral of a function 
$$
  \exp(S_0) \in C^\infty(\mathbb{R})
$$
on the quotient $\mathbb{R}$, but regarded now as a function on the cylinder, but independent -- gauge invariant-- of the canonical coordinate running around the cylinder. 

This can be done by
choosing as a reference 2-form the closed form
$$
  \mu := dx \wedge d\theta
  \,.
$$

We regard the exponentiated action, which is really just a function on the line,
now as a function on the cylinder

$$
  \exp(S_0) \in C^\infty(X) \subset \mathrm{CE}(\mathfrak{g})
  \,.
$$

The fact that this is really just a function on the line
is remembered by its gauge invariance, namely the exponentiated
action is invariant under rotation of the cylinder.

More precisely, 
let $\theta^\# := \frac{\partial}{\partial \theta}$ be the
multivector field coming from differentiation by the canonical
coordinaty running along the circle. Then the gauge invaariance
of the exponentiated action is expressed by the fact that

$$
  \theta^\# \exp(S_0) = 0
$$


(... to be continued ...)