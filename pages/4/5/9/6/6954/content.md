
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Functional analysis
### Contents {: .clickToReveal}
### Contents {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# The Parallelogram Identity
* table of contents
{: toc}

## Idea

The **parallelogram identity** is an identity which characterises those [[norms]] which are the norms associated with [[inner products]].  An inner product can be considered as being the structure required to define the angle between two vectors and a norm can be considered as being the structure required to define the length of a vector.  From standard Euclidean geometry, lengths and angles (almost) determine each other so knowing one, we should be able to define the other.

If length is known, angle can be defined by the *cosine law*:

$$
c^2 = a^2 + b^2 - 2 a b \cos C
$$

Although this formula could be used to define "angle" for any length (that is, norm), not every length admits a *sensible* notion of an angle.  There are several ways to describe what the _fundamental properties_ of angles should be.  One is to say that angles should add:

$$
\theta(u,v) + \theta(v,w) = \theta(u,w)
$$

This needs careful interpretation since the angle between two vectors is slightly ambiguous: one can choose the internal angle or the external angle and it is not possible to make a consistent choice.  However, modulo that uncertainty, the above is a reasonable property to insist on.

A special case of this is when $w = -u$.  This leads to the following diagram.

+-- {: style="text-align: center"}
<svg width="356" height="155" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="59338">
 <g>
  <title>Layer 1</title>
  <path id="svg_59338_1" d="m41,145l195,-122l81,122l-276,0z" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_59338_2" y2="145" x2="178" y1="24" x1="236" stroke-width="2" stroke="#000000" fill="none"/>
  <path id="svg_59338_3" d="m197,108c14,10 19,19 21,36" stroke-width="2" stroke="#000000" fill="none"/>
  <path id="svg_59338_4" d="m191,116c-19,-14 -51,7 -51,29" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_59338_5" y="133" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo rspace="0em" lspace="verythinmathspace">&#8722;</mo>
      <mi>u</mi>
     </mrow>
     <annotation encoding="application/x-tex">-u</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59338_6" y="135" x="308">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>u</mi>
     </mrow>
     <annotation encoding="application/x-tex">u</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59338_7" y="0" x="211">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>v</mi>
     </mrow>
     <annotation encoding="application/x-tex">v</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59338_8" y="107" x="201">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#981;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\phi</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_59338_9" y="96" x="131">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#968;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\psi</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
=--

The cosine law for this special case leads to two formulae:

$$
\begin{aligned}
{\|u + v\|^2} &= {\|u\|^2} + {\|v\|^2} - 2{\|u\|}{\|v\|} \cos(\psi) \\
{\|u - v\|^2} &= {\|u\|^2} + {\|v\|^2} - 2{\|u\|}{\|v\|} \cos(\phi)
\end{aligned}
$$

By imposing the assumption that angles should add correctly, we deduce that $\psi = \pi - \phi$ and thus $\cos (\psi) = - \cos(\phi)$.  Summing the two lines above leads to the parallelogram identity:

$$
{\|u + v\|^2} + {\|u - v\|^2} = 2 {\|u\|^2} + 2 {\|v\|^2}
$$

If a norm satisfies this identity, then the definition of angle (using the cosine identity) satisfies all the basic properties of angles that one can consider.


## Inner Products

A [[norm]] which satisfies the parallelogram identity is the norm associated with an  [[inner product]].
Using the parallelogram identity, there are three commonly stated equivalent forumlae for the inner product; these are called the [[polarization identities]].  (The notation can vary a little, but it is usually some form of round or angled brackets.)  These formulae hold for vector spaces over $\mathbb{R}$; there are similar formulae for $\mathbb{C}$, but they have more terms.

$$
\begin{aligned}
\langle u, v \rangle &= \frac{1}{2} \left({\|u + v\|^2} - {\|u\|^2} - {\|v\|^2} \right) \\
&= \frac{1}{2} \left({\|u\|^2} + {\|v\|^2} - {\|u - v\|^2}\right) \\
&= \frac{1}{4} \left({\|u + v\|^2} - {\|u - v\|^2}\right)
\end{aligned}
$$

It is possible to show directly that this is an inner product.  Certain properties are easy to deduce directly from the formulae.

+-- {: .num_lemma #lemipprop}
###### Lemma
The function $(u,v) \to \langle u, v\rangle$ satisfies the following properties:

1. $\langle u, u \rangle  \ge 0$
2. $\langle u, u \rangle = 0$ if and only if $u = 0$
3. $\langle u, 0 \rangle = 0$
4. $\langle u, v \rangle = \langle v, u \rangle$
5. $\langle \lambda u, \lambda v \rangle = \lambda^2 \langle u, v \rangle$
6. $\langle u, v + w \rangle = \langle u, v \rangle + \langle u, w\rangle$

=--

+-- {: .proof}
###### Proof
All but the last of these is a simple deduction from the formulae. The last is as well, but takes a little work to get it in the correct form.  We multiply by $4$ to simplify the notation.

$$
\begin{aligned}
4\langle u, v + w \rangle &= {\|u + v + w\|^2} - {\|u - v - w\|^2} \\
&={\left\|\left(\frac{1}{2}u + v\right) + \left(\frac{1}{2}u + w\right)\right\|^2} - {\left\|\left(\frac{1}{2}u - v\right) + \left(\frac{1}{2}u - w \right)\right\|^2} \\
&={\left\|\left(\frac{1}{2}u + v\right) + \left(\frac{1}{2}u + w\right)\right\|^2} + {\left\|\left(\frac{1}{2}u + v\right) - \left(\frac{1}{2}u + w\right)\right\|^2} \\
&\qquad -  {\left\|\left(\frac{1}{2}u - v\right) - \left(\frac{1}{2}u - w\right)\right\|^2} - {\left\|\left(\frac{1}{2}u - v\right) + \left(\frac{1}{2}u - w \right)\right\|^2} \\
&=2{\left\|\frac{1}{2}u + v\right\|^2} + 2{\left\|\frac{1}{2}u + w\right\|^2} -  2{\left\|\frac{1}{2}u - v\right\|^2} - 2{\left\|\frac{1}{2}u - w\right\|^2} \\
&= 2{\left\|\frac{1}{2}u + v\right\|^2}  -  2{\left\|\frac{1}{2}u - v\right\|^2} \\
&\quad+ 2{\left\|\frac{1}{2}u + w\right\|^2} - 2{\left\|\frac{1}{2}u - w\right\|^2}\\
&= 8\langle \frac{1}{2}u,v \rangle + 8\langle \frac{1}{2}u,w\rangle
\end{aligned}
$$

To get it as stated, we then apply this in the special case of $w = 0$ to deduce that $\langle u, v \rangle = 2\langle \frac{1}{2} u, v\rangle$.  Substituting this back in to the above, we obtain the form in the statement.
=--

The properties above were all reasonably straightforward deductions from the definition.  There is one more property that is needed which is a little more complicated.  First, we note a useful result about the continuity of the supposed inner product.

+-- {: .num_lemma #ipcts}
###### Lemma
The map $(u,v) \mapsto \frac{1}{2}({\|u + v\|^2} - {\|u\|^2} - {\|v\|^2})$ is continuous.
=--

+-- {: .proof}
###### Proof
This is a simple consequence of composition of continuous maps.
=--

Using that, we can prove the following property of the proposal for an inner product.

+-- {: .num_proposition #iplinear}
###### Proposition
The map $\langle u,v\rangle$ satisfies the identity

$$
\langle u,\lambda v \rangle = \lambda \langle u, v \rangle
$$

for all vectors $u$, $v$, and real numbers $\lambda$.
=--

+-- {: .proof}
###### Proof
We first use the formula $\langle u, v + w \rangle = \langle u, v \rangle + \langle u, w\rangle$ to prove that for any $n \in \mathbb{N}$

$$
\langle u, n v \rangle = n \langle u, v\rangle.
$$

We prove this by induction.  It is clearly true for the case $n = 1$.  Assume that it holds for $n$, then

$$
\langle u, (n+1)v \rangle = \langle u, n v + v \rangle = \langle u, n v\rangle + \langle u, v \rangle = n \langle u, v \rangle + \langle u, v \rangle = (n + 1)\langle u, v \rangle
$$

whence, by induction, it holds for all $n \in \mathbb{N}$.

Next we observe that it holds for all $n \in \mathbb{Z}$.  It clearly holds for $n = 0$, and for $n \in \mathbb{N}$ then

$$
0 = \langle u, 0 \rangle = \langle u, v - v \rangle = \langle u, v \rangle + \langle u, - v \rangle
$$

whence

$$
\langle u, -v \rangle = - \langle u, v \rangle.
$$

Next, we prove it for $\frac{p}{q} \in \mathbb{Q}$.  In fact, it is sufficient to prove it for $\frac{1}{n}$ with $n \in \mathbb{N}$.  For that we observe that

$$
\langle u, \frac{1}{n} v \rangle = \frac{n}{n} \langle u, \frac{1}{n} v \rangle = \frac{1}{n} \langle u, \frac{n}{n} v \rangle = \frac{1}{n} \langle u, v \rangle.
$$

To get to $\lambda \in \mathbb{R}$ we need to appeal to continuity.  We find a sequence $(q_n) \in \mathbb{Q}$ such that $(q_n) \to \lambda$ and see that by continuity

$$
\langle u, \lambda v \rangle = \langle u, (\lim q_n) v \rangle = \lim \langle u, q_n v \rangle = \lim q_n \langle u, v \rangle = \lambda \langle u, v \rangle.
$$
=--


+-- {: .num_corollary #scangip}
If ${\|{-}\|}$ is a norm on a vector space satisfying the parallelogram law then the  function

$$
(u,v) \mapsto \frac{1}{2}\left({\|u + v\|^2} - {\|u\|^2} - {\|v\|^2}\right)
$$

is an [[inner product]].
=--

## Isometries on inner product spaces 

Because lengths determine inner products, and because inner products respect linear structure, isometries must also respect linear (or affine) structure: 

+-- {: .un_thm}
######Theorem 
Let $V$ be a vector space with a norm satisfying the parallelogram law. Then an isometry (distance-preserving function) $f \colon V \to V$ is an injective linear affine map. 
=-- 

+-- {: .proof} 
######Proof 
Put $v = f(0)$. Then the map $x \mapsto f(x) - v$ is also an isometry, so that without loss of generality we may assume $f(0) = 0$, and prove that $f$ is a linear isomorphism. 

Letting $d(x, y)$ denote the distance between $x$ and $y$, we have 

$${\|x-y\|} = d(x, y) = d(f(x), f(y)) = {\|f(x)-f(y)\|}$$ 

and then, putting $y=0$, we have ${\|x\|} = {\|f(x)\|}$. Hence 

$$\array{
\langle x, y\rangle & = & \frac1{2}\left({\|x\|^2} + {\|y\|^2} - {\|x-y\|^2}\right) \\
 & = & \frac1{2}\left({\|f(x)\|^2} + {\|f(y)\|^2} - {\|f(x)-f(y)\|^2}\right) \\ 
 & = & \langle f(x), f(y) \rangle
}$$ 

i.e., $f$ preserves the inner product. 

Let $W$ be the linear subspace spanned by the image $f(V)$. Then $W$ inherits an inner product, and if $\{e_i\}$ is an orthonormal basis of $V$ (without restriction on cardinality), then $\{u_i = f(e_i)\}$ is also an orthonormal basis of $W$, since $f$ preserves the inner product. Next, for any linear combination $a x + b y$, 

$$\array{
\langle f(a x + b y), u_i \rangle_W & = & \langle a x + b y, e_i \rangle_V \\
 & = & a \langle x, e_i\rangle_V + b\langle y, e_i\rangle_V \\
 & = & a \langle f(x), u_i \rangle_W + b \langle f(y), u_i \rangle_W \\
 & = & \langle a f(x) + b f(y), u_i \rangle_W
}$$ 

for each $u_i$, whence $f(a x + b y) = a f(x) + b f(y)$. Thus $f$ is a linear map, and a linear isomorphism onto the subspace $W$ because it carries a basis $e_i$ of $V$ to a basis $u_i$ of $W$. 

Summarizing, any isometry $f \colon V \to V$ is of the form 

$$f(x) = M x + b$$ 

where $M$ is a linear injection and $b$ is a vector. 
=-- 

For information on related results, see [[isometry]] and [[Mazur-Ulam theorem]]. 


[[!redirects parallelogram identity]]
[[!redirects parallelogram law]]
