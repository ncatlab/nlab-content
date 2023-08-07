

\begin{tikzcd}[sep=0pt]
    \mathcal{C}_{T}
    \ar[
      rr,
      hook
    ]
    &&
    \mathcal{C}^{T}
    \\
    X 
    &\mapsto&
    \big(
      T(X)
      ,\,
      \mu_X
    \big)
    \\[+5pt]
    \mathcal{C}_{T}
    (X,\, Y)
    \ar[
      rr,
      <->,
      "{ \sim }"
    ]
    &&
    \mathcal{C}^{T}
    \Big(
      \big(T(X),\mu_X\big)
      ,\,
      \big(T(X'),\mu_{X'}\big)
    \Big)
    \\
    \Big(
      X
      \xrightarrow{
        \hspace{22pt}
        f
        \hspace{22pt}
      }
      \mathcal{E}(Y)
    \Big)
    &\mapsto&
    \Big(
      \mathcal{E}(X) 
      \xrightarrow{ \mathcal{E}(f)}
      \mathcal{E}\big(\mathcal{E}(Y)\big)
      \xrightarrow{ \mu_{Y} }
      \mathcal{E}(Y)
    \Big)
    \\
    \Big(
    X
    \xrightarrow{
      \eta^{\mathcal{E}}_{X} 
    }
    \mathcal{E}(X)
    \xrightarrow{ \phi }
    \mathcal{E}(Y)
    \Big)    
    \ar[rr, phantom, "{\mapsto}"{rotate=180}]
    &&
    \Big(
    \mathcal{E}(X)
    \xrightarrow{ 
      \hspace{39pt} 
      \phi 
      \hspace{39pt} 
    }
    \mathcal{E}(Y)
    \Big)
\end{tikzcd}



\linebreak


$$
  \underset{
    \color{blue}\text{given a potential thing}
  }{
  (D_\bullet, \rho_\bullet)
  \,\in\, 
  Type_W^{\lozenge_W}
  }
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  \underset{
   \color{blue} \text{which is possible}
  }{
    \lozenge_W D_\bullet 
  }
  \underset{
   \color{blue}\text{then}
  }{
    \phantom{\vert}
    \xrightarrow{\;\; \rho \;\;} 
    \phantom{\vert}
  }
  \underset{
   \color{blue}\text{it is actual}
  }{
    D_\bullet
  }
$$


$X \to Prop$

$$
  w \colon W
  \;\;
    \dashv
  \;\;
  (w'', w', d_{w'})
  \;\mapsto\;
  (w', d_{w'})
  \;\mapsto\;
  f_{(w, w', d_{w'})}
$$

$$
  w \colon W
  \;\;
    \dashv
  \;\;
  (w'', w', d_{w'})
  \;\mapsto\;
  \Big(
    w'', 
    f_{(w, w', d_{w'})}
  \Big)
$$

[[flavors of modal logics and relations -- table]]

\begin{tikzcd}
    W \ar[rr, "{ p_{{}_W} }"] && W/R
    \\
    \mathrm{Prop}_W
    \ar[out=180-42, in=180+42,
      <-,
      looseness=4.5, 
      shorten=0pt,
      shift right=3pt,
      "\scalebox{1.1}{${
          \hspace{1pt}
          \mathclap{
            {
              \Box
            }
          }
          \hspace{4pt}
        }$}"{
          pos=.5, 
          swap
        }
    ]  
    \ar[
      from=rr,
      shift right=7pt,
      "{ (p_{{}_W})^\ast }"{swap}
    ]
    \ar[
      rr,
      shift right=7pt,
      "{ (p_{{}_W})_\ast }"{swap}
    ]
    \ar[
      rr,
      phantom,
      "{ \scalebox{.7}{$\bot$} }"
    ]
    &&
    \mathrm{Prop}_{W/R}
\end{tikzcd}


***


$$
  Br_N
  \longrightarrow
  Aut\big(
    \pi(\Sigma \setminus N)
  \big)
  \longrightarrow
  Aut\Big(
    A\big(
      \Sigma \setminus N
    \big)
  \Big)
$$

blah [[affine Serre's theorem]] yy.


[[FileTest.abc:file]]
