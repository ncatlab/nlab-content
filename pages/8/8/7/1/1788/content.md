
[[MetaLogicOfIdentifications-220925.jpg:file]]




<a href="https://ncatlab.org/nlab/files/BOZAPALIDES_theorie_formelle_bicategories.pdf">pdf</a>

\begin{tikzcd}
  \mathrm{Top}_{(0,1)}
  \ar[rr, "\mathrm{Sh}(-)"]
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \ar[drr, phantom, "{\#}"]
  &&
  \mathrm{Top}_{(1,1)}
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \\
  \mathrm{Cat}_{(0,1)}
  \ar[rr, hook]
  &&
  \mathrm{Cat}_{(1,1)}  
\end{tikzcd}

## Idea

In [[type theory]] -- where one understand every piece of data (every "[[term]]") to be assigned a specific [[type]] which specifies its operational behaviour -- *identity types* (maybe better: *identification types*) $Id_X$ are the types of those terms which serve as "witnesses" or "certitifcates" of identification of terms of type $X$. 

What exactly this means depends on the nature of the ambient [[type theory]] and the choices for the [[inference rules]] of the identity types (see at *[[extensional type theory|extensional]]* and *[[intensional type theory]]*). In some setups, having a term of identity type means much the same as having an [[equality]] in [[classical mathematics]], and for this (historical) reasons identity types are often denoted simply by equality signs, for better or worse.

But the power of the notion of identity types goes beyond this classical situation and results from the fact that they may give the notion of equality a [[constructive mathematics|constructive]] meaning. Taking this constructive principle of identity types to its logical conclusion, leads -- notably in [[Martin-Löf dependent type theory]] -- to identity types which themselves have identity types, reflecting identifications-of-identification, and so ever on, mimicking the structure of [[homotopies]] and [[homotopies of homotopies]] in [[homotopy theory]], whence one refers to type theories with such identity types also as *[[homotopy type theories]]*.

More in detail, the [[inference rules]] for identity types in [[Martin-Löf dependent type theory|Martin-Löf-]]/[[homotopy type theory]] may be understood as follows:

First, for every type $X$ and any [[pair]] $x_1, x_2 : X$ of its [[terms]], let's denote the *type of identifications* of $x_1$ with $x_2$ by $Id_X(x_1,x_2)$ (other common notation for identity types is "$x_1 =_{{}_X} x_2$" which, when adopted, requires authors to make up new symbols, like $\equiv$, for actual equalities).
In the jargon of [[dependent type theory]] this means that there is a [[type formation]] rule for identity types of the form:


spring


## Idea

play around with the editing functionality

## Definition

\begin{defn}(Title of defn). \label{defn_anchor} {#html_anchor} The **sandbox** is a box full of sand.
\end{defn}

One usually defines *waterboxes* analogous to  [[Sandbox#defn_anchor|this Definition]] (which could be on another page).

## A sandtable

| Sand | More sand |
| ----------- | ----------- |
| sand | sand |
| sand | sand |

How do "quotes" work? `quote', 'quote'.

How to do a list

- sand
- sand
- sand

* sand
* sand 
* sand

## Figures

make a responsive figure (that scales, but not too much):

<center>
<figure>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Hopf_Fibration.png/500px-Hopf_Fibration.png" alt="" style="width:80%; max-width: 400px; height:auto;">
<figcaption>Figure 1: The hopfy caption of the figure</figcaption>
</figure>
</center>

## Formulas

a $a \text{<} b$

## LaTeX punctuation

In view of Rembrandt, involutions on topological spaces are equivalently known as *[[topological G-spaces]]* for $G = $[[cyclic group of order 2|$\mathbb{Z}/2$]]. The 

<a href="http://ncatlab.org/nlab/show/HomePage"><div style="float:right;margin:0 20px 10px 20px;"><img width = "250" src="http://i.stack.imgur.com/1hvpz.png" alt="nLab banner" /></div></a>


