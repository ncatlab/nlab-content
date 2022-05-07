
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[classical model structure on topological spaces]] $Top_{Qu}$ restricts to [[compactly generated topological spaces]] and further to [[weak Hausdorff spaces]] among these, to yield [[Quillen equivalence|Quillen equivalent]] model structures $k Top_{Qu}$  and $h k Top_{Qu} $there. Since these model structures on k-spaces are Cartesian monoidal closed as model categories (Prop. \ref{CartesianMonoidalModelClosureOfkTop} below) while $Top_{QU}$ is not, they provide a more [[convenient category of topological spaces|convenient]] foundations for much of [[homotopy theory]] in terms of [[model categories]].



## Statement

Recall (from [here](compactly+generated+topological+space#SequencesOfCoReflections)) the sequence of [[adjoint functors]]

\[
  \label{SequenceOfAdjunctions}
  h k Top
  \underoverset
    {\underset{}{\hookrightarrow}}
    {\overset{ h }{\longleftarrow}}
    {\;\;\;\; \bot \;\;\;\; }
  k Top
  \underoverset
    {\underset{k}{\longleftarrow}}
    {\overset{}{\hookrightarrow}}
    {\;\;\;\; \bot \;\;\;\;}
  Top
\]

exhibting the [[coreflective subcategory]] inside all of [[Top]] of [[compactly generated topological spaces]] and further the [[reflective subcategory]] of [[weak Hausdorff spaces]] among these.

### On k-Spaces

\begin{proposition}\label{ClassicalModelStructureOnCompactlyGeneratedSpaces}
**(classical model structure on compactly generated topological spaces)**
\linebreak
  The [[classical model structure on topological spaces]] $Top_{Qu}$ restricts along $k Top \xhookrightarrow{\;} Top$ (eq:SequenceOfAdjunctions) to a [[cofibrantly generated model category]] structure $k Top_{Qu}$ on [[compactly generated topological spaces]], and the [[coreflective subcategory|coreflection]] becomes a [[Quillen equivalence]]:

$$
  k Top
  \underoverset
    {\underset{k}{\longleftarrow}}
    {\overset{}{\hookrightarrow}}
    {\;\;\;\; \simeq_{\mathrlap{Qu}} \;\;\;\;}
  Top
$$
\end{proposition}
(e.g. [Hovey 1999, Thm. 2.4.23](#Hovey99))
A **proof** is spelled out with [this Thm.](classical+model+structure+on+topological+spaces#ModelStructureOnTopcg) at *[[classical model structure on topological spaces]]* (which is [this Thm.](Introduction+to+Homotopy+Theory#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces) at *[[Introduction to Homotopy Theory]]*).

\begin{prop}\label{CartesianMonoidalModelClosureOfkTop}
  The model structure on compactly generated topological spaces from Prop. \ref{ClassicalModelStructureOnCompactlyGeneratedSpaces} is a [[Cartesian monoidal category|cartesian]] [[monoidal model category]];
 
\end{prop}
(e.g. [Hovey 1999, Prop. 4.2.11](#Hovey99))
A **proof** is given with [this Prop.](classical+model+structure+on+topological+spaces#PushoutProductInTopCGSendsCofCofToCof) at *[[classical model structure on topological spaces]]* (which is [this Prop.](Introduction+to+Homotopy+Theory#PushoutProductInTopCGSendsCofCofToCof) at *[[Introduction to Homotopy Theory]]*).


### On weakly Hausdorff k-Spaces

Similarly:

\begin{proposition}\label{ClassicalModelStructureOnCompactlyGeneratedSpaces}
**(classical model structure on compactly generated weak Hausdorff spaces)**
\linebreak
  The [[model structure on compactly generated topological spaces]] $k Top_{Qu}$ from Prop. \ref{ClassicalModelStructureOnCompactlyGeneratedSpaces} restricts along $h k top \xhookrightarrow{\;} k Top $ (eq:SequenceOfAdjunctions) to a [[model category]] structure on [[weak Huasdorff space|weakly Hausdorff]] k-spaces $h k Top_{Qu}$, and the [[reflective subcategory|reflection]] is a [[Quillen equivalence]]: 

$$
  h k Top_{Qu}
  \underoverset
    {\underset{}{\hookrightarrow}}
    {\overset{ h }{\longleftarrow}}
    {\;\;\;\; \simeq_{\mathrlap{Qu}} \;\;\;\; }
  k Top_{Qu}
$$

\end{proposition}
(e.g. [Hovey 1999, Thm. 2.4.25](#Hovey99))

Again, this is a [[Cartesian monoidal category|Cartesian]] [[monoidal model category]] (e.g. [Hovey 1999, Thm. 2.4.23](#Hovey99)).


## Related concepts


* [[model structure on topological spaces]]

  * [[classical model structure on topological spaces]] ([[classical model structure on pointed topological spaces|on pointed spaces]])

    * [[model structure on compactly-generated topological spaces]]

    * [[model structure on Delta-generated topological spaces]]

  * [[Strøm model structure]]

* [[model structure on diffeological spaces]]


## References

Textbook accounts:

* {#Hovey99}  [[Mark Hovey]], *[[Model Categories]]*, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))


Lecture notes:

* [[J. F. Jardine]], *Serre fibrations and the model structure for CGWH* ([pdf](https://www.uwo.ca/math/faculty/jardine/courses/homth/homth-lecture002a.pdf))


[[!redirects model structure on compactly-generated topological spaces]]

[[!redirects model structure on compactly generated weak Hausdorff spaces]]
[[!redirects model structure on compactly-generated weak Hausdorff spaces]]


