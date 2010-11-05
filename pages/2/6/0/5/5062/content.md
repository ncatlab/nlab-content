#Contents#
* automatic table of contents goes here
{:toc}


##Arrow frames, arrow languages, arrow models and arrow logics##

These structures are intended to allow one to talk about 'all such objects 
as may be represented in a picture by arrows', (Venema).

###Arrow frames###

+--{: .un_defn}
######Definition######
An **arrow frame** is a [[frame (modal logic)|frame]], $\mathfrak{F} = (W, C, R, I )$ such that $C$ is a ternary relation, (so $C\subseteq 
W \times W \times W$), $R$ is a binary relation, and $I$ a unary one, so $I\subseteq W$. 
=--
###Gloss###
The interpretation intended for these relations is similar to the structure of a [[groupoid]], but from a relational point of view.

*  For $C(a,b,c)$ think $a = b\star c$, 'the' _composite_ of $b$ and $c$, but, of course, $a$ need not be uniquely defined by this;

* For $R(a,b)$, think $b$ is a 'reverse' arrow for $a$;

* For $I(a)$ i.e. $a\in I$, think $a$ is an 'identity arrow'.

This defines a frame by a relational signature.  It does not specify any formulae to be satisfied, nor is there a [[geometric models for modal logics|valuation]] around  to give some 'meaning' to the structure.

###Arrow languages###
The arrow language follows the general form of the [[modal logic|modal languages]], but note that there are several 'arities' of relation in the structure, so we need several different types of modal operators.

+--{: .un_defn}
######Definition######
The **arrow language** is defined by the rule

$$\phi ::= p \mid \bot \mid \neg \phi \mid \phi_1 \vee \phi_2 \mid \phi\circ \psi \mid \otimes\phi\mid 1',$$  

where the $p$ are the propositional variables, as usual, and in addition

* $1'$ is 'identity' and is a nullary modality or modal constant;

* $\otimes$ (an unfortunate notation, but which seems fairly standard in the sources used for this) is the 'converse' operator and is a 'diamond', i.e. a unary operator, and

*  $\circ$ is the 'composition operator' and is a dyadic operator.
=--

The possible interpretations or readings of these include

$1'$ is SKIP;

$\otimes \phi$ is $phi$  conversely; and 

$\phi\circ \psi$ is 'first $\phi$ then $\psi$'.

###Arrow models###
The usual rules for modal semantics apply.  An **arrow model**, $\mathfrak{M}$, consists of an arrow frame, $\mathfrak{F} = (W, C, R, I )$, (and a valuation $V$, which plays a somewhat behind the scenes role in this general situation).  In what follows, $a\in W$, 

*  $\mathfrak{M},a \models 1'$ if and only if $Ia$;

*  $\mathfrak{M},a \models \otimes\phi$ if and only if $\mathfrak{M},b \models\phi$ for some $b$ with $R a b$;

*  $\mathfrak{M},a \models\phi\circ \psi$ if and only if $\mathfrak{M},b \models\phi$ and $\mathfrak{M},c \models\psi$ for some $b,c$ with $C a b c$.


[[!redirects arrow logic]]
[[!redirects arrow structures]]
[[!redirects arrow logics]]

##References##

A general treatment of these ideas can be found in 

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001,

whilst a short introduction is 

*  Y. [[Venema]], [_A crash course in Arrow Logic_](http://staff.science.uva.nl/~yde/papers/arrow.pdf),  in: M Marx, L P&#243;los and M Masuch (editors), Arrow Logic and Multi-Modal Logic,
Studies in Logic, Language and Information, CSLI Publications, Stanford (1996) 3--34.

