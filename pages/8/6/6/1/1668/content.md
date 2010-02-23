Two operations, $\alpha$ and $\beta$, of an [[algebraic theory]] are said to __commute__ if for any matrix $M$ of elements, with the number of rows given by the arity of $\alpha$ and the number of columns by the arity of $\beta$, one gets the same result whether one

1. applies $\alpha$ to each column of $M$ and then $\beta$ to the resulting row, or
1. applies $\beta$ to each row of $M$ and then $\alpha$ to the resulting column.

(It is left as an exercise to the reader to formulate this notion in an element-free way.) Note that an operation of arity $0$ or $1$ always commutes with itself; this is not necessarily the case for higher arities. Commuting nullary operations are necessarily equal.

+-- {: #svgcommute style="text-align:center" }
<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw2" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <foreignObject x="4.891323" y="20.022943" id="svg_1" font-size="16" width="179.999992" height="110.999998">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mrow>
       <mo>[</mo>
       <mrow>
        <mtable rowspacing="0.5ex">
         <mtr>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>1</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>2</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <mo>&#8230;</mo>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mi>n</mi>
            </mrow>
           </msub>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>1</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>2</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <mo>&#8230;</mo>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mi>n</mi>
            </mrow>
           </msub>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mo>&#8942;</mo>
          </mtd>
          <mtd>
           <mo>&#8942;</mo>
          </mtd>
          <mtd>
           <mo>&#8945;</mo>
          </mtd>
          <mtd>
           <mo>&#8942;</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>1</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>2</mn>
            </mrow>
           </msub>
          </mtd>
          <mtd>
           <mo>&#8230;</mo>
          </mtd>
          <mtd>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mi>n</mi>
            </mrow>
           </msub>
          </mtd>
         </mtr>
        </mtable>
       </mrow>
       <mo>]</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\begin{bmatrix}
x_{1 1} &amp;amp; x_{1 2} &amp;amp; \dots &amp;amp; x_{1 n} \\
x_{2 1} &amp;amp; x_{2 2} &amp;amp; \dots &amp;amp; x_{2 n} \\
\vdots &amp;amp; \vdots &amp;amp; \ddots &amp;amp; \vdots \\
x_{m 1} &amp;amp; x_{m 2} &amp;amp; \dots &amp;amp; x_{m n}
\end{bmatrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="274.891323" y="19.022943" font-size="16" width="179.999992" height="110.999998" id="svg_2">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mrow>
       <mo>[</mo>
       <mrow>
        <mtable rowspacing="0.5ex">
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mi>n</mi>
            </mrow>
           </msub>
           <mo stretchy="false">)</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mi>n</mi>
            </mrow>
           </msub>
           <mo stretchy="false">)</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mo>&#8942;</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mi>n</mi>
            </mrow>
           </msub>
          </mtd>
         </mtr>
        </mtable>
       </mrow>
       <mo>]</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\begin{bmatrix}
\beta(x_{1 1}, x_{1 2}, \dots, x_{1 n}) \\
\beta(x_{2 1}, x_{2 2}, \dots, x_{2 n}) \\
\vdots \\
\beta(x_{m 1}, x_{m 2}, \dots, x_{m n}
\end{bmatrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="6.461462" y="198.022943" font-size="16" width="244.000003" height="110.999998" id="svg_84">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mrow>
       <mo>[</mo>
       <mrow>
        <mtable rowspacing="0.5ex">
         <mtr>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
          <mtd>
           <mo>&#8230;</mo>
          </mtd>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
         </mtr>
        </mtable>
       </mrow>
       <mo>]</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\begin{bmatrix}
\alpha\begin{pmatrix} x_{1 1} \\ x_{2 1} \\ \vdots \\ x_{m 1}\end{pmatrix} &amp;amp;
\alpha\begin{pmatrix} x_{1 2} \\ x_{2 2} \\ \vdots \\ x_{m 2}\end{pmatrix} &amp;amp;
\dots &amp;amp;
\alpha\begin{pmatrix} x_{1 n} \\ x_{2 n} \\ \vdots \\ x_{m n}\end{pmatrix}
\end{bmatrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="212.461462" y="348.022943" font-size="16" width="260.000003" height="110.999998" id="svg_166">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#946;</mi>
      <mrow>
       <mo>(</mo>
       <mrow>
        <mtable rowspacing="0.5ex">
         <mtr>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mn>1</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mn>2</mn>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
          <mtd>
           <mo>&#8230;</mo>
          </mtd>
          <mtd>
           <mi>&#945;</mi>
           <mrow>
            <mo>(</mo>
            <mrow>
             <mtable rowspacing="0.5ex">
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>1</mn>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mn>2</mn>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <mo>&#8942;</mo>
               </mtd>
              </mtr>
              <mtr>
               <mtd>
                <msub>
                 <mi>x</mi>
                 <mrow>
                  <mi>m</mi>
                  <mi>n</mi>
                 </mrow>
                </msub>
               </mtd>
              </mtr>
             </mtable>
            </mrow>
            <mo>)</mo>
           </mrow>
          </mtd>
         </mtr>
        </mtable>
       </mrow>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\beta\begin{pmatrix}
\alpha\begin{pmatrix} x_{1 1} \\ x_{2 1} \\ \vdots \\ x_{m 1}\end{pmatrix} &amp;amp;
\alpha\begin{pmatrix} x_{1 2} \\ x_{2 2} \\ \vdots \\ x_{m 2}\end{pmatrix} &amp;amp;
\dots &amp;amp;
\alpha\begin{pmatrix} x_{1 n} \\ x_{2 n} \\ \vdots \\ x_{m n}\end{pmatrix}
\end{pmatrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="409.891323" y="177.022943" font-size="16" width="179.999992" height="110.999998" id="svg_271">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>&#945;</mi>
      <mrow>
       <mo>(</mo>
       <mrow>
        <mtable rowspacing="0.5ex">
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>1</mn>
             <mi>n</mi>
            </mrow>
           </msub>
           <mo stretchy="false">)</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mn>2</mn>
             <mi>n</mi>
            </mrow>
           </msub>
           <mo stretchy="false">)</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mo>&#8942;</mo>
          </mtd>
         </mtr>
         <mtr>
          <mtd>
           <mi>&#946;</mi>
           <mo stretchy="false">(</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>1</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mn>2</mn>
            </mrow>
           </msub>
           <mo>,</mo>
           <mo>&#8230;</mo>
           <mo>,</mo>
           <msub>
            <mi>x</mi>
            <mrow>
             <mi>m</mi>
             <mi>n</mi>
            </mrow>
           </msub>
          </mtd>
         </mtr>
        </mtable>
       </mrow>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\alpha\begin{pmatrix}
\beta(x_{1 1}, x_{1 2}, \dots, x_{1 n}) \\
\beta(x_{2 1}, x_{2 2}, \dots, x_{2 n}) \\
\vdots \\
\beta(x_{m 1}, x_{m 2}, \dots, x_{m n}
\end{pmatrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_arrow_fw2)" fill="none" stroke-width="2" stroke="#000" id="svg_3" y2="70" x2="282" y1="71" x1="175"/>
  <line marker-end="url(#se_arrow_fw2)" fill="none" stroke-width="2" stroke="#000" id="svg_4" y2="197" x2="94" y1="132" x1="94"/>
  <line marker-end="url(#se_arrow_fw2)" fill="none" stroke-width="2" stroke="#000" id="svg_5" y2="172" x2="451" y1="133" x1="419"/>
  <line marker-end="url(#se_arrow_fw2)" fill="none" stroke-width="2" stroke="#000" id="svg_6" y2="348" x2="223" y1="311" x1="184"/>
  <line fill="none" stroke-width="2" stroke="#000" id="svg_7" y2="294" x2="472" y1="339" x1="443"/>
  <line id="svg_8" fill="none" stroke-width="2" stroke="#000" y2="296" x2="477" y1="341" x1="448"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_9" y="47" x="204">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#946;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\beta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_10" height="20" width="48" font-size="16" y="328" x="169">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#946;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\beta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_16" height="20" width="48" font-size="16" y="150" x="57">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#945;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\alpha</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_22" height="20" width="48" font-size="16" y="137" x="420">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#945;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\alpha</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
=--

The operations that commute with a given set of operations in an algebraic theory form a subtheory. The __centre__ of an algebraic theory is given by the operations that commute with all the operations of the theory. An algebraic theory is __commutative__ if every pair of its operations commute. Another way of describing the centre is to say that it consists of those operations which are also homomorphisms; an algebraic theory is commutative if all of its operations are homomorphisms.

If $f_1,\ldots , f_n$ are homomorphisms $A \to B$ of models (algebras) of a commutative algebraic theory, and $\omega$ is an n-ary operation of it, then the function $A \to B$ given by sending $a \in A$ to $\omega(f_1(a),\ldots ,f_n(a)) \in B$ is again a homomorphism, which is naturally called $\omega(f_1,\ldots ,f_n)$. In this way $Hom(A,B)$ is enriched as a model of the algebraic theory, and we have a [[closed category]] of models and homorphisms. Furthermore, this internal $Hom$ has a left adjoint $\otimes$ for which the free model on one generator is a unit, so we have a [[closed monoidal category]].

The notion of commutative algebraic theory was formulated in terms of [[monad]]s by Anders Kock.


### References ###

+-- {: .query}
Can we have some please!  This is something I want to use soon so it'd be nice to know where the details were originally worked out. ---Andrew 

=--

* Anders Kock, _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 

* Anders Kock, _Strong functors and monoidal monads_, Arhus Universitet, Various Publications Series No. 11 (1970). 

See also [here](http://home.imf.au.dk/kock/SFMM.pdf). 

Recently [[Nikolai Durov]] rediscovered that notion for the purposes of geometry (under the name __commutative algebraic monad__), constructed their spectra (generalizing the [[spectrum (geometry)|spectrum]] of Grothendieck) and theory of [[generalized scheme after Durov|generalized schemes on this basis]]. There is a generalized version of the [[Eckmann–Hilton argument]] concerning commutative finitary monads. Much detail including many examples and further constructions are in his thesis

* Nikolai Durov, _New approach to Arakelov geometry_, [arXiv:0704.2030](http://arXiv.org/math/abs/0704.2030)


[[!redirects commutative monad]]
[[!redirects commutative algebraic monad]]