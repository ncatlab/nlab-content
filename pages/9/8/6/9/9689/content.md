
#Contents#
* table of contents
{:toc}


## Idea

A *tetrahedron* is the convex [[regular polyhedron]] with four faces, as such one of the [[platonic solids]].

Also known as the 3-dimensional *[[simplex]]*.


\begin{tikzpicture}[scale=1.5]
  \coordinate (a) at (.4,-.3);
  \coordinate (b) at (1.7,.4);
  \coordinate (c) at (.6,2);
  \coordinate (d) at (-.6,.6);

\draw (a) -- (d);

\draw[dashed]
  (d) -- (b);
  
\draw[
    line width=1.1,
]
    (d) -- (a) -- (c) -- cycle;
  
\draw[
    line width=1.1,
    fill=black!20, 
    fill opacity=.6
]
  (a) -- (b) -- (c) -- cycle;

\draw[fill=black] (a) circle (.07);
\draw[fill=black] (b) circle (.07);
\draw[fill=black] (c) circle (.07);
\draw[fill=black] (d) circle (.07);

\end{tikzpicture}



## Related concepts

[[!include ADE -- table]]

## Related concepts

* [[circle]]

* [[triangle]]

* [[square]]

## References

* {#Klein1884} [[Felix Klein]], chapter I.6 of _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)

See also:

* Wikipedia, *[Tetrahedron](https://en.wikipedia.org/wiki/Tetrahedron)*


[[!redirects tetrahedra]]

.