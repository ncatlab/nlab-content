[[!redirects modal logics]]



#Contents#
* table of contents
{:toc}

## Modal Logics ## 

(From the preface to the book by Blackburn et al.)

_'Ask three modal logicians what modal logic is, and you are likely to get at least three different answers'_.


(under construction)

## Idea## 
The modal logics are the logic of [[relational structures]].  They are built on **modal languages**.
It is usual to classify them using their axiom systems, but also in terms of the type of general interpretation applied to them, such as :

*  [[temporal logic|temporal logics]];

*  [[epistemic logics]];

*  [[dynamic logic]];

*  [[arrow logics]];

(this list may get added to later).

Modal logics have semantics given in terms of [[frame (modal logic)|Kripke frames]], which are simply [[relational structures]]. For instance, [[temporal logic|temporal logics]] have [[posets]] as models.

The modal languages add one or more modal operator, often denoted $\square$ or $\Diamond$ in to the usual propositional logics. (For the moment, these will be unary operators and we will not be considering operators that have more than one input. The general case will be considered later on, but in any case is discussed in detail in some of the books on modal logic listed below.)

## Modal Languages## {#modal+language}

We will give a modal language with $n$ modal operators, $\Diamond_i$, $i = 1,\ldots, n$, which can  be applied to propositions of the language to form new propositions.  If $n=1$, we will refer to the language, defined below,  as the _basic modal language_.

+--{: .un_defn}
######Definition ######
We suppose given a set of variables, the _$n$-operator basic modal language_, $\mathcal{L}_\omega(n)$, given by  

$$\phi ::= p_\lambda \mid \bot \mid \neg \phi \mid \phi_1 \vee \phi_2 \mid \Diamond_i\phi,$$  

where the $p_\lambda$ are the propositional variables ordered by finite ordinals, $\lambda$, and, as usual, $\Diamond_i$ is a modality for each  $i=1, \ldots , n$.  

=--
####Gloss####
1. This form of definition needs a bit of interpreting if you have not met it before.  It gives a way of deciding if a formula is 'well-formed'.  The well formed formulae of  $\mathcal{L}_\omega(n)$ are defined as follows: A formula is either

   * a proposition variable, 

   * the propositional constant $\bot$, that is _falsum_, 

   * a negated formula,

   * a disjunction of two formulae, or

   * a formula prefixed by one of the diamonds / modal operators.

1. The basic modal language will be $\mathcal{L}_\omega(1)$.  We will sometimes write $Prop$ for the set of propositional variables / atomic formulae or whatever other reasonable term is used in a context.

1. The interpretation of $\Diamond \phi$ depends on the context (to some extent), but in the initial form here it is usually said to mean 'possibly $\phi$'.

1. Some authors use an equivalent generation rule using $\square \phi$, which is $\neg \Diamond \neg \phi$. Of course, this interprets as 'necessarily $\phi$' in this initial form.  In [[epistemic logic]] the basic modal language interprets $\square \phi$ as saying 'the agent knows that $\phi$'.


1. Other formulations replace $\vee$ and $\neg$ by implication $\phi_1\to \phi_2$, or by $\wedge$ and $\neg$.


##Modal logics##
+--{: .un_defn}
######Definition ######
A **modal logic** in $\mathcal{L}_\omega(n)$ is any set $\Lambda$ of $\mathcal{L}_\omega(n)$-formulae such that   

* $\Lambda$ includes all $\mathcal{L}_\omega(n)$-formulae that are instances of tautologies, 
 
and

* $\Lambda$ is closed under the inference rule 
_if $\phi$, $\phi\to \psi \in \Lambda$ then $\psi \in \Lambda$_ , i.e. detachment or __modus ponens__.

The logic is **uniform** if it is closed under the rule of uniform substitution of $\mathcal{L}_\omega(n)$-formulae for propositional variables and is **normal** if it contains the schemata:
  
(K)  $\Diamond_i(\psi \vee \chi) \to \Diamond_i(\psi)\vee \Diamond_i(\chi)$  
  
(N) $\neg \Diamond_i(\bot)$

and monotonicity (for each $i$):
 
if $\psi \to \chi \in \Lambda$ then $\Diamond_i \psi \to \Diamond_i \chi \in \Lambda$.  
 
=--
## Semantics## 
The usual semantics of modal languages is in terms of [[frame (modal logic)|frames]]. (These are quite often called 'Kripke frames' as Kripke was one of the first to use relational semantics in this context. A discussion of the history can be found in  the book by Blackburn, de Rijke and Vedema, (see below) page 42.) (As there is another sense to [[frame]] as the dual of a [[locale]], we need to consider the terminology here and where necessary will use [[frame (modal logic)]] as the entry name.) A more detailed discussion of [[frame (modal logic)|frames]], models and the whole question of the semantics of modal logics is to be found at that entry. 


## References## 

General books on modal logics include

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* M. Kracht, _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.

and more particularly on epistemic logics and their applications,

* J.- J. Ch. Meyer and W. Van der Hoek, _Epistemic logic for AI and Computer Science_, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995. 