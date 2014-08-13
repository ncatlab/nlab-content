## Idea

If $C$ is a [[small category]] (or even a [[topological category]]), one can define a $C$-torsor (or _torsor with structure category $C$_) which generalizes the [[torsor]] (principal bundle) with structure group(oid). We present two variants in slightly different context.  

## Moerdijk's definition

If $F$ is a [[sheaf]] over $X$, denote by $F_x$ its stalk over $x$ (cf. [[etale space]]). 

A __$C$-torsor__ $E$ over a topological space $X$ is given by a functor $E : C\to Shv(X)$ such that 

1. (**surjectivity**) every 'total stalk' $\cup_{c\in C_0} E(c)_x$, where $x\in X$, is nonempty;

1. (**transitivity**) for any two germs 'in the same total stalk', $\alpha\in E(c)_x$, $\alpha'\in E(c')_x$, there is a span $c\stackrel{u}\leftarrow b\stackrel{u'}\to c'$ and $\xi\in E(b)_x$ such that $E(u)(\xi)=\alpha$ and $E(u')(\xi)=\alpha'$;

1. (**freeness**) for a parallel pair $u_1,u_2: c\to c'$ of morphisms in $C$, $E(u_1)(\alpha)=E(u_2)(\alpha)$ for some $\alpha\in E(c)_x$ implies there is a morphism $w:b\to c$ and $\zeta\in E(b)_x$ such that $u_1\circ w = u_2\circ w$ and $E(w)(\zeta)=\alpha$. 


This definition is from the monograph

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Springer Lec. Notes Math. __1616__ (1995)

where it is shown that _the [[classifying space]] of a category $C$ classifies $C$-torsors_.

_[[David Roberts]]: This definition should be able to be restated in terms of [[flat functors]]_ 


## Street's definition

Suppose now $C$ is a finitely complete category with a [[calculus of left fractions]] whose morphisms are called *covers*.

Let $A$ be an [[internal category]] in $C$. An __$A$-torsor trivialized by a cover__ $e : V\to U$ is a [[discrete fibration]] $A\stackrel{p}\leftarrow E\stackrel{q}\to U$ for which there exist a morphism $a : V\to A$ and a commutative diagram

$$
\begin{svg}<svg width="164" height="200" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:math="http://www.w3.org/1998/Math/MathML" se:nonce="11550">
 <g>
  <title>Layer 1</title>
  <foreignObject height="200" width="160" font-size="16" id="svg_11550_1" y="0" x="7.878906">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mrow>
       <mtable rowspacing="0.5ex">
        <mtr>
         <mtd>
          <mi>A</mi>
          <mo stretchy="false">&#8595;</mo>
          <mi>a</mi>
         </mtd>
         <mtd>
          <mover>
           <mo>&#8594;</mo>
           <mrow>
            <mspace width="2em"/>
            <mi>q</mi>
            <mspace width="2em"/>
           </mrow>
          </mover>
         </mtd>
         <mtd>
          <mi>V</mi>
         </mtd>
        </mtr>
        <mtr>
         <mtd>
          <mo minsize="1.8em" maxsize="1.8em">&#8595;</mo>
         </mtd>
         <mtd/>
         <mtd>
          <mo minsize="1.8em" maxsize="1.8em">&#8595;</mo>
          <mpadded width="0">
           <mover>
            <mphantom>
             <mi>a</mi>
            </mphantom>
            <mstyle scriptlevel="1">
             <mi>e</mi>
            </mstyle>
           </mover>
          </mpadded>
         </mtd>
        </mtr>
        <mtr>
         <mtd>
          <mi>E</mi>
         </mtd>
         <mtd>
          <munder>
           <mo>&#8594;</mo>
           <mrow>
            <mspace width="2em"/>
            <mi>q</mi>
            <mspace width="2em"/>
           </mrow>
          </munder>
         </mtd>
         <mtd>
          <mi>U</mi>
         </mtd>
        </mtr>
        <mtr>
         <mtd>
          <mpadded lspace="-100%width" width="0">
           <mover>
            <mphantom>
             <mi>a</mi>
            </mphantom>
            <mstyle scriptlevel="1">
             <mi>p</mi>
            </mstyle>
           </mover>
          </mpadded>
          <mo minsize="1.8em" maxsize="1.8em">&#8595;</mo>
         </mtd>
         <mtd/>
         <mtd/>
        </mtr>
        <mtr>
         <mtd>
          <mi>p</mi>
         </mtd>
         <mtd/>
         <mtd/>
        </mtr>
       </mtable>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">\begin{matrix}
A\downarrow a &amp; \xrightarrow{\qquad q\qquad}&amp; V\\
\Bigl\downarrow &amp; &amp; \Bigl\downarrow\mathrlap{\overset{\scriptsize{e}}{\phantom{a}}}\\
E&amp;\xrightarrow[\qquad q\qquad]{}&amp; U\\
\mathllap{\overset{\scriptsize{p}}{\phantom{a}}}\Bigl\downarrow &amp;&amp;\\
p&amp;&amp;
\end{matrix}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path id="svg_11550_2" d="m30.070129,27c-35.572876,38.333313 -35.874329,106.666656 1.808777,148" marker-end="url(#se_marker_end_svg_11550_2)" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_11550_2">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>\end{svg}
$$

<center><img src="http://latex.codecogs.com/gif.latex?
\xymatrix{
A\downarrow{a}\ar[r]^q \ar@/_2pc/[dd]_{p} \ar@%3C-.5ex%3E[d]
%26 V\ar[d]^e \\
E\ar[r]_q\ar[d]_p%26 U\\
A%26
}" />
</center>
in which the square is a pullback. Street says __$A$-torsor at $U$__ for an $A$-torsor trivialized by some cover $e : V\to U$.

* [[Ross Street]], _Combinatorial aspects of descent theory_, [pdf](http://www.math.mq.edu.au/~street/DescFlds.pdf) (page 25 in the file)

[[!redirects torsors with structure category]]