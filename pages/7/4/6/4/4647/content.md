
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of a _comonadic functor_ is the dual of that of a [[monadic functor]]. See there for more background.

## Definition

Given a pair $L\dashv R$ of [[adjoint functors]], $L\colon A \to B\colon R$, with counit $\epsilon$ and unit $\eta$, one forms a [[comonad]] $\mathbf{\Omega} = (\Omega, \delta, \epsilon)$ by $\Omega \coloneqq L \circ R$, $\delta \coloneqq L \eta R$. $\mathbf{\Omega}$-comodules (aka $\mathbf{\Omega}$-coalgebras) form a category $B_{\mathbf{\Omega}}$ and there is a natural comparison functor $K = K_{\mathbf{\Omega}}\colon A \to B_{\mathbf{\Omega}}$ given by $A \mapsto (L A, L A \stackrel{L(\eta_A)}\to L R L A)$. 

A functor $L\colon A\to B$ is __comonadic__ if it has a right adjoint $R$ and the corresponding comparison functor $K$ is an [[equivalence of categories]].  The adjunction $L \dashv R$ is said to be a **comonadic adjunction**.

## Properties

Beck's [[monadicity theorem]] has its dual, comonadic analogue. To discuss it, observe that for every $\Omega$-comodule $(N, \rho)$, 

+-- {: style="text-align:center"}
<svg width="284" height="85" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="37863">
 <g>
  <title>Layer 1</title>
  <foreignObject height="54" width="284" font-size="16" id="svg_37863_1" y="31.00003" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>N</mi>
      <munderover>
       <mo>&#8594;</mo>
       <mi>&#961;</mi>
       <mspace width="2em"/>
      </munderover>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <mi>N</mi>
      <munderover>
       <mo>&#8649;</mo>
       <mrow>
        <mspace width="thickmathspace"/>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>&#951;</mi>
         <mrow>
          <msub>
           <mi>Q</mi>
           <mo>*</mo>
          </msub>
          <mi>N</mi>
         </mrow>
        </msub>
        <mspace width="1em"/>
       </mrow>
       <mrow>
        <mspace width="thickmathspace"/>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>Q</mi>
         <mo>*</mo>
        </msub>
        <mi>&#961;</mi>
        <mspace width="1em"/>
       </mrow>
      </munderover>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <msup>
       <mi>Q</mi>
       <mo>*</mo>
      </msup>
      <msub>
       <mi>Q</mi>
       <mo>*</mo>
      </msub>
      <mi>N</mi>
     </mrow>
     <annotation encoding="application/x-tex">N\xrightarrow[\rho]{\qquad}Q^*Q_* N\underoverset{\; Q^* \eta_{Q_*N}\quad}{\;Q^* Q_* \rho\quad}{\rightrightarrows}Q^* Q_*Q^* Q_* N</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path marker-end="url(#se_marker_end_svg_37863_3)" id="svg_37863_3" d="m215,43.144531c-41,-26.024994 -82.000031,-25.020004 -123,0" stroke="#000000" fill="none"/>
  <path id="svg_37863_4" marker-end="url(#se_marker_end_svg_37863_4)" d="m65.5,42.644531c-16,-12.43103 -32,-11.950989 -48,0" stroke="#000000" fill="none"/>
  <foreignObject height="22" width="60" font-size="16" id="svg_37863_5" y="0" x="122.5">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#1013;</mi>
       <mrow>
        <msup>
         <mi>Q</mi>
         <mo>*</mo>
        </msup>
        <msub>
         <mi>Q</mi>
         <mo>*</mo>
        </msub>
        <mi>N</mi>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\epsilon_{Q^* Q_* N}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37863_6" height="22" width="20" font-size="16" y="10" x="32">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#1013;</mi>
       <mi>N</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\epsilon_{N}</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37863_3">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_37863_21"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37863_4">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_37863_22"/>
  </marker>
 </defs>
</svg>
=--

manifestly exhibits a [[split equalizer]] sequence.

...

## Examples 

If $T: Set \to Set$ is a monad on $Set$, with corresponding monadic functor $U: Set^T \to Set$, then the left adjoint $F: Set \to Set^T$ is comonadic provided that $F(!): F(0) \to F(1)$ is a regular monomorphism and not an isomorphism. In particular, if $T$ is given by an algebraic theory with at least one constant symbol and at least one function symbol of arity greater than zero, then the left adjoint is comonadic (because then $F(!): F(0) \to F(1)$ is a split monomorphism but not an isomorphism). 

More generally, let $A$ be a [[locally small category]] with small [[copower|copowers]], and suppose $a$ is an object such that $0 \to a$ is a regular monomorphism but not an isomorphism, then the copowering with $a$, 

$$- \cdot a: Set \to A$$ 

(left adjoint to $A(a, -): A \to Set$) is comonadic. See proposition 6.13 and related results in this [paper](http://www.tac.mta.ca/tac/volumes/16/1/16-01abs.html) by Mesablishvili. 

###Necessity

In the context of the treatment of modal operators given at [Possible worlds via first-order logic and type theory](necessity+and+possibility#InFirstOrderLogicAndTypeTheory), we find that base change along the terminal morphism from the type of worlds, $W$, and its right adjoint dependent product form a comonadic adjunction. $W^{\ast} \dashv \prod_W$.

For a type, $P$, in $\mathbf{H} = \mathbf{H}/*$, $W^{\ast} (P) = P \times W \to W$, projection on the second component. For $Q \to W$ in $\mathbf{H}/W$, $\prod_W (Q) = Q^W$. 

Hence the composite, a kind of necessity operator $\Box_W$ (an analog of the [[jet comonad]]), sends $Q \to W$ to $Q^W \times W \to W$.

Coalgebras for this comonad are the types in $\mathbf{H}$, or rather the types in $\mathbf{H}/W$ which are in the image of $W^{\ast}$. The coalgebra map then works by sending $P \times W$ to $\Box_W (P \times W) = P^W \times W$ over $W$, where the first component of the map sends $p: P$ to the constant map at $p$.

To see this as a equalizer, consider the two maps from $\Box_W (P \times W \to W)$ to $\Box_W  \Box_W (P \times W \to W)$. Over $W$, these are formed from the two ways of mapping $P^W$ to $P^{(W \times W)}$, by sending $f$ in $P^W$ to $g(w, w') = f(w)$ and to $h(w, w') = f(w')$. 

The equalizer of these two maps is formed from the $f$ for which $g = h$ for all $w, w'$ in $W$, that is, when $f$ is constant. So the equalizer is equivalent to  $W^{\ast} P = P \times W \to W$.

## Related concepts

* [[monadic functor]], **comonadic functor**

* [[monadicity theorem]]


[[!redirects comonadic functor]]
[[!redirects comonadic functors]]
[[!redirects comonadicity theorem]]
[[!redirects comonadic adjunction]]
[[!redirects comonadic adjunctions]]
