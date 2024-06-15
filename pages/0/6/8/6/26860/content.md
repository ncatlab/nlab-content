
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



\tableofcontents



## Definition

First, the [[connected sum]] $ K_1 # K_2 $ of [[boxed knot|boxed]] [[knots]] $K_1$ and $K_2$ is obtained by joining the boxes containing them. 

\begin{imagefromfile}
    "file_name": "BoxedKnotSum.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Sossinsky 2023](#Sossinsky23))"
\end{imagefromfile}


From this one obtains a notion of connected sum for ordinary (oriented) knots by observing that:

\begin{proposition}

There is a canonical [[bijection]] between the [[equivalence
classes]] of [[boxed knots]] and the [[isotopy]] classes of oriented knots.

\end{proposition}

This bijection gives the connected sum of two ordinary knots.

## Properties

\begin{theorem}

The connected sum operation is [[associative]] and [[commutative]]:

* $ K_1 # K_2 = K_2 # K_1 $,

* $ ( K_1 # K_2 ) # K_3 = K_1 # ( K_2 # K_3 ) $.

There are no [[inverse elements]] under the connected sum operation,
i.e.,
$K # K' = \circ \implies K = K' = \circ $,
where $\circ $ is the [[unknot]].

\end{theorem}



## References

* {#Sossinsky23} [[Alexei B. Sossinsky]], §3 in: *Knots, Links and Their Invariants: An Elementary Course in Contemporary Knot Theory*, The Student Mathematical Library **101**, AMS (2023) &lbrack;[doi:10.1090/stml/101](https://doi.org/10.1090/stml/101)&rbrack;

Discussion in relation to [[Vassiliev knot invariants]]:

* {#BarNatan95} [[Dror Bar-Natan]], *On the Vassiliev knot invariants*, Topology **34** 2 (1995) 423-472 &lbrack;<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf)&rbrack;


[[!redirects knot sums]]

