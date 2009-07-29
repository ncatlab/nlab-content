Given a [[manifold]] (or [[generalized smooth space]]) $X$, the __cotangent bundle__ $T^*(X)$ of $X$ is the [[vector bundle]] over $X$ dual to the [[tangent bundle]] $T_*(X)$ of $X$.  A __cotangent vector__ or __covector__ on $X$ is an element of $T^*(X)$.  The __cotangent space__ of $X$ at a point $a$ is the [[fiber]] $T^*_a(X)$ of $T^*(X)$ over $a$; it is a [[vector space]].  A __covector field__ on $X$ is a [[section]] of $T^*(X)$.  (More generally, a [[differential form]] on $X$ is a section of the [[exterior algebra]] of $T^*(X)$; a covector field is a differential $1$-form.)

Given a covector $\omega$ at $a$ and a [[tangent vector]] $v$ at $a$, the pairing $\langle{\omega,v}\rangle$ is a scalar (a [[real number]], usually).  This (with some details about linearity and universality) is basically what it means for $T^*(X)$ to be dual to $T_*(X)$.  More globally, given a covector field $\omega$ and a [[tangent vector field]] $v$, the paring $\langle{\omega,v}\rangle$ is a scalar [[function]] on $X$.

Given a point $a$ in $X$ and a differentiable (real-valued) [[partial function]] $f$ defined near $a$, the __differential__ $\mathrm{d}_a f$ of $f$ at $a$ is a covector on $X$ at $a$; given a tangent vector $v$ at $a$, the pairing is given by
$$ \langle{\mathrm{d}_a f, v}\rangle = v[f] ,$$
thinking of $v$ as a [[derivation]] on differentiable functions defined near $a$.  (It is really the [[germ]] at $a$ of $f$ that matters here.)  More globally, given a differentiable function $f$, the __differential__ $\mathrm{d} f$ of $f$ is a covector field on $X$; given a vector field $v$, the pairing is given by
$$ \langle{\mathrm{d} f, v}\rangle = v[f] ,$$
thinking of $v$ as a derivation on differentiable functions.

One can also *define* covectors at $a$ to be germs of differentiable functions at $a$, modulo the [[equivalence relation]] that $\mathrm{d}_a f = \mathrm{d}_a g$ if $f - g$ is constant on some neighbourhood of $a$.  In general, a covector field won\'t be of the form $\mathrm{d} f$, but it will be a sum of terms of the form $h \mathrm{d} f$.  More specifically, a covector field $v$ on a coordinate patch can be written
$$ v = \sum_i v_i\, \mathrm{d} x^i $$
in local coordinates $(x^1,\ldots,x^n)$.


[[!redirects cotangent vector]]
[[!redirects covector]]
[[!redirects cotangent space]]
[[!redirects cotangent vector space]]
[[!redirects covector field]]
[[!redirects cotangent vector field]]