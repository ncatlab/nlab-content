## Idea## 
If you had a piece of string possibly tangled up, and could, at a crossing, pull one part of the string through the other, then, intuitively, repeating this enough times, the string would become unknotted. At the mathematical level, there is a corresponding notion of a _crossing change_ on a diagram

+--{: .un_defn}
######Definition######
A crossing change in a diagram exchanges an overpass and underpass at a crossing, as below:
=--
<svg
   xmlns="http://www.w3.org/2000/svg"
   width="295.28571"
   height="148.14285"
   viewBox="0 0 295.28571 148.14285">
  <defs>
    <marker
       id="arrowhead"
       markerWidth="10"
       markerHeight="10"
       refX="9"
       refY="3"
       orient="auto">
      <polygon points="0 0, 10 3, 0 6" fill="#000000" />
    </marker>
  </defs>
  <g transform="translate(-159.5,-163.59448)">
    <path
       style="fill:none;stroke:#000000;stroke-width:1px;"
       d="M 160,164.09448 L 257.14286,309.80877" />
    <path
       style="fill:none;stroke:#000000;stroke-width:1px;"
       d="M 207.85714,246.95163 L 165.71429,309.80877 M 254.28571,166.95163 L 215,236.95163" />
    <path
       style="fill:none;stroke:#000000;stroke-width:1px;"
       d="M 409.28571,244.09448 L 454.28571,311.23734 M 357.14285,165.52305 L 403.57142,234.80877" />
    <path
       style="fill:none;stroke:#000000;stroke-width:1px;"
       d="M 451.42856,168.3802 L 362.85714,311.23734" />
    <path
       style="fill:none;stroke:#000000;stroke-width:1.4;marker-end:url(#arrowhead);"
       d="M 271.42857,241.23734 L 345.71429,241.23734" />
  </g>
</svg>

Crossing changes will usually alter the isotopy type of the diagram. 

+--{: .un_lemma}
######Lemma
Let $D$ be a diagram with $c$ crossings, then changing at most $c/2$ crossings of $D$ produces a diagram of the unknot.
=--

+--{: .un_defn}
######Definition######
The unknotting number, $u(K)$, is the smallest number of crossing changes required to obtain the unknot from some diagram of the knot.
=--
Of course, we know that $u(K)\leq c(K)/2$, but the natural difficulty of calculating $u(K)$ is made worse by the following result of Beiler (1984).  

_The unknotting number of a knot does not necessarily occur in a minimal diagram._

Beiler gave an example of a minimal diagram for a 10 crossing knot, which cannot be unknotted with fewer than 3 crossing changes, yet for which there is a 14 crossing diagram, which is  isotopic to it, yet can be unknotted with just 2 crossing changes.  