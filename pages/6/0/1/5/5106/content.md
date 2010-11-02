##Validity##

# Contents
* table of contents
{:toc}


##Idea##
To judge whether a modal logic gives a good encoding of the properties of a particular relational structure, we need to put aside the valuations and to concentrate on the [[frame (modal logic)|frames]].  A formula will be **valid** on a frame $\mathfrak{F}$ if it is true at every state in every model that can be built from $\mathfrak{F}$.  More formally:

+--
{: .un_defn}
######Definition######
*  A formula $\phi$ is said to be _valid at a state_ $w$ is a frame $\mathfrak{F}= (W,R_1,\ldots, R_n)$ (notation $\mathfrak{F},w \models \phi$) if $\phi$ is true at $w$ in every model $\mathfrak{M} = (\mathfrak{F},V)$, based ion $\mathfrak{F}$.

*  A formula, $\phi$, is _valid in a frame_ $\mathfrak{F}$ (notation $\mathfrak{F}\models \phi$) if it is valid at every state of $\mathfrak{F}$.

*  If $\mathbb{F}$ is a class of frames (all of the same relational signature), then we say $\phi $ is _valid in $\mathbb{F}$_ (notation $\mathbb{F}\models \phi$ if $\mathfrak{F}\models \phi$ for all $\mathfrak{F}\in \mathbb{F}$, and is **valid**, $\models\phi$, if it is valid on the class of all frames.
=--
Fixing a given set $P$ of atomic formulae and the [[signature (in logic)|relational signature]] that we are considering:
+--
{: .un_prop}
######Proposition######
The set of formulae that are valid on a class,$\mathbf{F}$, of frames of that signature forms a logic.
=--

(We restrict to Kripke frames (i.e. to binary relations) for simplicity of exposition, and refer to the sources, such as Blackburn et al, for a fuller discussion.)

We denote the logic thus specified by $\Lambda_\mathbf{F}$.

## References## 

Generally this entry is based on

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

(any mistakes or errors of interpretation are due to ....!)
