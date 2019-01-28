
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition


A [[fork]]

\begin{center}\begin{tikzcd}
A \ar[r,"e"] & B \ar[r,shift left,"f"] \ar[r,shift right,"g"'] & C
\end{tikzcd}\end{center}

is **split** if it can be embedded into a diagram

\begin{center}\begin{tikzcd}
A \ar[r,"e"'] &
B \ar[r,shift left,"f"] \ar[r,shift right,"g"'] \ar[l,bend right=40,"s"']
 & C \ar[l,bend right=40,"t"']
\end{tikzcd}\end{center}

in which $s e = id_A$, $t g = id_B$ and $t f = e s$. 

Of course, $f$ and $g$ can be interchanged in the definition.

## Properties

Every split fork is an [[absolute limit|absolute]] [[equalizer]], but not conversely.  

## Related concepts

See also [[split coequalizer]].


[[!redirects split equalizer]]
[[!redirects split equalizers]]
[[!redirects split equaliser]]
[[!redirects split equalisers]]
[[!redirects split fork]]
[[!redirects split forks]]
