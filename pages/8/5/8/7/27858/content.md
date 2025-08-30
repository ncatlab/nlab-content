
### Equivariant cell structure on 2-tori
 {#EquivariantCellStructureOf2Tori}

The following shows for the [[crystallographic groups|2D crystallographic groups]] ([[wallpaper groups]]) $S$

  \begin{tikzcd}[
    sep=small
  ]    
    &
    1
    \ar[d]
    &&
    1
    \ar[d]
    \\
    1 
    \ar[r]
    &
    \mathbb{Z}^2
    \ar[rr, hook, "{ \ell }"]
    \ar[d, hook]
    &&
    \mathbb{R}^2
    \ar[rr, "{ \mathrm{mod}\,\ell }"]
    \ar[d, hook]
    &&
    T^2
    \ar[r]
    &
    1
    \\
    & 
    S
    \ar[rr, hook]
    \ar[d]
    &&
    \mathrm{Iso}(\mathbb{R}^2)
    \ar[d]
    \\
    &
    G
    \ar[rr, hook]
    \ar[d]
    &&
    \mathrm{O}(\mathbb{R}^2)
    \ar[d]
    \\
    & 
    1
    &&
    1
    \mathrlap{\,,}
  \end{tikzcd}

the [[G-CW complex|$G$-CW complex]] [[structure]] on the resulting [[G-space|G-]][[tori]] $T^2 \coloneqq \mathbb{R}^2/_{\ell}\mathbb{Z}^2$ (graphics from [[schreiber:Crystalline Chern Phases|SS25]]).

The [[point groups]] $G$ arising are the [[cyclic groups]] $\mathbb{Z}_{/1} =$[[trivial group|$1$]], [[cyclic group of order 2|$\mathbb{Z}_{/2}$]], [[cyclic group of order 3|$\mathbb{Z}_{/3}$]], [[cyclic group of order 4|$\mathbb{Z}_{/4}$]], $\mathbb{Z}_{/6}$ and the [[dihedral groups]] $Dih_1$, $Dih_2$, $Dih_3$, $Dih_4$, and $Dih_6$ (making 9 distinct abstract [[point groups]] $G$, due to the isomorphism $\mathbb{Z}_{/2} \simeq Dih_1$, but several come with distinct [[group actions]] on $\mathbb{R}^2$).


| [[wallpaper group]] $S$  | [[point group]] $G$ | [[G-CW complex|G-cell structure]] on $G \curvearrowright \mathbb{R}^2/_\ell \mathbb{Z}^2 $ |
|--|--|--|
| p1  | $\mathbb{Z}_{/2}$ | Ex. \ref{TorusWithoutAction} |
| pm | $Dih_1$ | Ex. \ref{TorusWithReflectionAction} |
| cm | $Dih_1$ | Ex. \ref{cmTorusAction} |
| pg | $Dih_1$ | Ex. \ref{TorusWithpgGlideReflectionAction} |
| p2 | $\mathbb{Z}_{/2}$ | Ex. \ref{TorusWithC2RotationAction} |
| pmm | $Dih_2$ | Ex. \ref{TorusWithD2DihedralAction} |
| cmm | $Dih_2$ | Ex. \ref{cmmTorusAction} |
| pmg | $Dih_2$ | Ex. \ref{TorusWithPMGAction} |
| pgg | $Dih_2$ | Ex. \ref{TorusWithPGGAction} |
| p3 | $\mathbb{Z}_{/3}$ | Ex. \ref{TorusWithC3RotationAction} |
| p31m | $Dih_3$ | Ex. \ref{TorusWithD3DihedralAction} |
| p3m1 | $Dih_3$ | Ex. \ref{TorusWithp3m1Action} |
| p4 | $\mathbb{Z}_{/4}$ | Ex. \ref{TorusWithC4RotationAction} |
| p4m | $Dih_4$ | Ex. \ref{TorusWithD4DihedralAction} |
| p4g | $Dih_4$ | Ex. \ref{TorusWithP4GAction} |
| p6 | $\mathbb{Z}_{/6}$ | Ex. \ref{TorusWithC6RotationAction} |
| p6m | $Dih_6$ | Ex. \ref{TorusWithD6DihedralAction} |
 
\linebreak

\begin{example}\label{TorusWithoutAction}
**(p1)**
For completeness, here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with [[trivial group]]-action, corresponding to the $p 1$ [[wallpaper group]]:

\begin{imagefromfile}
    "file_name": "p1TorusCellStructure-20250722.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{TorusWithReflectionAction}
**(pm)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[dihedral group|$Dih_1$]] $\simeq$ [[cyclic group of order 2|$\mathbb{Z}_{/2}$]]-[[group action|action]] which [[reflection at a hyperplane|reflects]] one of the two [[coordinate]] axes, corresponding to the $p m$ [[wallpaper group]]:

\begin{imagefromfile}
    "file_name": "pmTorusCellStructure-20250722.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{cmTorusAction}
**(cm)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[dihedral group|$Dih_1$]] $\simeq$ [[cyclic group of order 2|$\mathbb{Z}_{/2}$]]-[[group action|action]] which [[reflection at a hyperplane|reflects]] along the coordinate diagonal, corresponding to the $c m$ [[wallpaper group]]:

\begin{imagefromfile}
    "file_name": "cmTorusCellStructure-20250722.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithpgGlideReflectionAction}
**(pg)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with glide reflection action corresponding to the [[wallpaper group]] $p g$:

\begin{imagefromfile}
    "file_name": "pgTorusCellStructure-20250726b.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}







\begin{example}\label{TorusWithC2RotationAction}
**(p2)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[cyclic group of order 2|$\mathbb{Z}_{/2}$]]-[[group action|action]] which rotates by multiples of $\pi$ around the origin, corresponding to the [[wallpaper group]] $p2$:

\begin{imagefromfile}
    "file_name": "p2TorusCellStructure-20250830.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{TorusWithD2DihedralAction}
**(pmm)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with  [[dihedral group|$Dih_{2}$]]-[[group action|action]] according to the [[wallpaper group]] pmm: 

\begin{imagefromfile}
    "file_name": "pmmTorusCellStructure-20250726.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{cmmTorusAction}
**(cmm)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with  [[dihedral group|$Dih_{2}$]]-[[group action|action]] according to the [[wallpaper group]] cmm: 

\begin{imagefromfile}
    "file_name": "cmmTorusCellStructure-20250722.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{TorusWithPMGAction}
**(pmg)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with rotation and glide reflection action corresponding to the [[wallpaper group]] $p m g$:

\begin{imagefromfile}
    "file_name": "pmgTorusCellStructure-20250730.png",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{TorusWithPGGAction}
**(pgg)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with rotation and glide reflection action corresponding to the [[wallpaper group]] $p g g$:

\begin{imagefromfile}
    "file_name": "pggTorusCellStructure-20250731.png",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}





\begin{example}\label{TorusWithC3RotationAction}
**(p3)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[cyclic group of order 3|$\mathbb{Z}_{/3}$]]-[[group action|action]] which rotates by multiples of $2\pi/3$ around the origin:

\begin{imagefromfile}
    "file_name": "p3TorusCellStructure-20250830.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithD3DihedralAction}
**(p31m)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with  [[dihedral group|$Dih_{3}$]]-[[group action|action]] corresponding to the $p31m$ [[wallpaper group]]:

\begin{imagefromfile}
    "file_name": "p31mTorusCellStructure-20250830.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithp3m1Action}
**(p3m1)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[dihedral group|$Dih_{3}$]]-[[group action|action]] corresponding to the $p3m1$ [[wallpaper group]]: 

\begin{imagefromfile}
    "file_name": "p3m1TorusCellStructure-20250722.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}


\begin{example}\label{TorusWithC4RotationAction}
**(p4)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[cyclic group of order 4|$\mathbb{Z}_{/4}$]]-[[group action|action]] which rotates by multiples of $\pi/2$ around the origin:

\begin{imagefromfile}
    "file_name": "p4TorusCellStructure-20250722.png",
    "width": 470,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithD4DihedralAction}
**(p4m)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with  [[dihedral group|$Dih_{4}$]]-[[group action|action]]: 

\begin{imagefromfile}
    "file_name": "p4mTorusCellStructure-20250722.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithP4GAction}
**(p4g)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with rotation and glide reflection action corresponding to the [[wallpaper group]] $p 4 g$:

\begin{imagefromfile}
    "file_name": "p4gTorusCellStructure-20250802.png",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}





\begin{example}\label{TorusWithC6RotationAction}
**(p6)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with the [[cyclic group|$\mathbb{Z}_{/6}$]]-[[group action|action]] which rotates by multiples of $\pi/3$ around the origin:

\begin{imagefromfile}
    "file_name": "p6TorusCellStructure-20250830.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}



\begin{example}\label{TorusWithD6DihedralAction}
**(p6m)**
Here is a $G$-CW complex structure for the [[torus]] $T^2 \,\equiv\, \mathbb{R}^2/\mathbb{Z}^2$ equipped with  [[dihedral group|$Dih_{6}$]]-[[group action|action]]:

\begin{imagefromfile}
    "file_name": "p6mTorusCellStructure-20250722.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 30,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{example}











