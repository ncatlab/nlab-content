##Validity##

* tic
{: toc}

##Idea##
To judge whether a modal logic gives a good encoding of the properties of a particular relational structure, we need to put aside the valuations and to concentrate on the [[frame (modal logic)|frames]].  A formula will be **valid** on a frame $\mathfrak{F}$ if it is true at every state in every model that can be built from $\mathfrak{F}$.  More formally:

+--
{: .un_defn}
######Definition######
*  A formula $\phi$ is said to be _valid at a state_ $w$ is a frame $\mathfrak{F}= (W,R_1,\ldots, R_n)$ (notation $\mathfrak{F},w \models \phi$) if $\phi$ is true at $w$ in every model $\mathfrak{M} = (\mathfrak{F},V)$, based ion $\mathfrak{F}$.

*  A formula, $\phi$, is _valid in a frame_ $\mathfrak{F}$ (notation $\mathfrak{F}\models \phi$) if it is valid at every state of $\mathfrak{F}$.

*  If $\mathbb{F}$ is a class of frames (all of the same relational signature), then we say $\phi $ is _valid in $\mathbb{F}$_ (notation $\mathbb{F}\models \phi$ if $\mathfrak{F}\models \phi$ for all $\mathfrak{F}\in \mathbb{F}$, and is **valid**, $\models\phi$, if it is valid on the class of all frames.
=--