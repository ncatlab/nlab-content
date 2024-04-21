
#Contents#
* table of contents
{:toc}

## Idea

The [[geometric infinity-stacks]] within all [[smooth infinity-groupoids]] are called _Lie $\infty$-groupoids_. These are equivalently those smooth $\infty$-groupoids which have a [[representable functor|presentation]] by [[Kan-fibrant simplicial manifolds]]. See there for more. 

In the language of groupoids,  the Kan conditions (see below) correspond to composing and inverting various morphisms. For example, the
existence of a composition for arrows is given by the condition
$\Kan(2,1)$, whereas the composition of an arrow with the inverse
of another is given by $\Kan(2,0)$ and $\Kan(2,2)$: 

\begin{imagefromfile}
        "file_name": "kan-mor.jpg",
        "width": 300,
        "unit": "px"
    \end{imagefromfile}




Here we recall that a simplicial set $X$ is *Kan* if any map from the horn
$\Lambda[m,j]$ to $X$ ($m\ge 1$, $j=0,\dots,m$), extends to a map from
$\Delta[m]$. Let us call $\Kan(m,j)$ the *Kan condition* for the horn
$\Lambda[m,j]$. A *Kan simplicial set* is therefore a simplicial set
satisfying $\Kan(m,j)$ for all $m\ge 1$ and $0\leq j\leq m$. 

Note that the composition of two arrows is in general not unique,
but any two of them can be joined by a $2$-morphism $h$ given by
$\Kan(3,2)$.

\begin{imagefromfile}
        "file_name": "composition.jpg",
        "width": 350,
        "unit": "px"
    \end{imagefromfile}

The associativity can be given by $\Kan(2, 1)!$ and $Kan(3, 2)$ illustrated below:


\begin{imagefromfile}
        "file_name": "ass-mor.jpg",
        "width": 350,
        "unit": "px"
    \end{imagefromfile}

In an $n$-groupoid, the only well-defined composition law is the one for $n$-morphisms. This motivates the following definition.

\begin{definition}\label{groupoid}
An $n$-groupoid ($n\in\N \cup \infty$) $X$ is a simplicial set
that satisfies $\Kan(m,j)$ for all $0\leq j\leq m \geq 1$ and
$\Kan!(m,j)$ for all $0 \leq j \leq m$ $\geq n+1$, where

$\Kan(m,j)$:  Any map $\Lambda[m,j]\to X$ extends to a map $\Delta[m]\to X$.

$\Kan!(m,j)$: Any map $\Lambda[m,j]\to X$ extends to a unique map $\Delta[m]\to X$.
\end{definition}


## Related $n$Lab entries

* [[Lie differentiation]]

[[!redirects Lie n-groupoids]] 

[[!redirects Lie infinity-groupoids]]
[[!redirects Lie-infinity-groupoid]]

[[!redirects infinity-Lie-groupoid]]
[[!redirects infinity-Lie-groupoids]]

[[!redirects infinity-Lie groupoid]]
[[!redirects infinity-Lie groupoids]]

[[!redirects Lie ∞-groupoid]]
[[!redirects Lie ∞-groupoids]]

[[!redirects ∞-Lie groupoid]]
[[!redirects ∞-Lie groupoids]]

[[!redirects ∞LieGrpd]]

[[!redirects Lie-infinity groupoid]]
[[!redirects Lie ∞-groupoids]]

