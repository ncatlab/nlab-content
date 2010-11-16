# Contents
* automatic table of contents goes here
{:toc}

##Petri nets##
###Introduction###
Petri nets are a well known model of parallel computation, generalising [[transition systems]] by using a built in notion of resource.  Their use is widespread in modelling manufacturing systems, optimising control systems and in resource critical aspects of operational research, as well as being a useful model of computation.  Because of this they exist in many variants : colored, algebraic, probabilistic, timed, ..., and hence there are many forms of the basic definition, each thought best of that particular application.

The initial use, here, is for their links with [[transition systems]], [[event structures]], [[asynchronous automata]] etc., leading on to their comparison with [[higher dimensional automata]] and [[higher dimensional transition systems]], so the first definition we will use is that given by Winskel and Nielsen (see references below), but first we will attempt to give some idea of what a Petri net is and what is does.

##Idea##
The idea of a simple Petri net is based on a simple manufacturing shop.  You have various 'transitions' or manufacturing 'events' that form part of the various process occurring in the 'shop'. These typically take parts (of the final object), do something to them, such as combining two or more different parts to make a more complicated one, (for instance, putting the wheels on a car).

Parts, represented by 'tokens' are stored in 'places' and the assembly process are known, as above, as 'events' or 'transitions' (depending on the source being used for the theory).  The relationships are typically represented graphically.  For instance:

<svg width="294" height="253" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="60508">
 <g>
  <title>Layer 1</title>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m23.007811,27c0,-14.36464 11.635359,-26 25.999998,-26c14.364643,0 26.000004,11.63536 26.000004,26c0,14.364639 -11.635361,26 -26.000004,26c-14.364639,0 -25.999998,-11.635361 -25.999998,-26z" id="svg_60508_1"/>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m222.007813,27c0,-14.36464 12.082886,-26 27,-26c14.917114,0 27,11.63536 27,26c0,14.364639 -12.082886,26 -27,26c-14.917114,0 -27,-11.635361 -27,-26z" id="svg_60508_2" transform="rotate(3.74069e-06, 320.272, -74)"/>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m120.007813,226c0,-14.364624 12.082886,-26 27,-26c14.917114,0 27,11.635376 27,26c0,14.364624 -12.082886,26 -27,26c-14.917114,0 -27,-11.635376 -27,-26z" transform="rotate(3.74069e-06, 320.272, -74)" id="svg_60508_3"/>
  <rect fill="#ffffff" stroke="#000000" stroke-width="2" x="100.007808" y="117" width="98" height="21" id="svg_60508_4"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="68.00782" y1="46.999999" x2="148.00782" y2="118.000002" id="svg_60508_5"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="230.007808" y1="47.000002" x2="149.007807" y2="116.000003" id="svg_60508_6"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="147.007813" y1="139" x2="148.007813" y2="199" id="svg_60508_7"/>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="105.008" y="65" id="svg_60508_8" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="188.008" y="67" id="svg_60508_9" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="157.008" y="170" id="svg_60508_10" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="212.008" y="128" id="svg_60508_11" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">e</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="8.00781" y="26" id="svg_60508_12" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">A</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="286.008" y="27" id="svg_60508_13" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">B</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="187.008" y="226" id="svg_60508_14" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">C</text>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="36.007813" cy="23" id="svg_60508_15" rx="4" ry="4"/>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="60.007813" cy="24" rx="4" ry="4" id="svg_60508_16"/>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="247.007813" cy="23" rx="4" ry="4" id="svg_60508_17"/>
 </g>
</svg>

represents a system with three places (labelled $A$, $B$, and $C$) and one event/ transition (labelled $e$).  Shown is a situation represented by an initial 'marking' where there are two tokens in $A$, one in $B$, and none in $C$. (The convention is that places are shown as circles and events as rectangles.)

Suppose that the 'event' takes one 'part' of type $A$, one of type $B$ and produces one of type $C$.  (This is indicated on the diagram by the labels on the edges.  Clearly with the available  resources the even $e$ is able to be performed.  (The usual Petri net jargon for this is that '$e$ is enabled'.) In this case, $e$ can be 'fired' and the result will yield a marking of one token in $A$, none in $B$ and one in $C$.  This sort of structure gets abstracted as follows:

+--{: .un_defn}
######Definition######
A **Petri net** $N$ consists of

* a set $P$ of _places_;

* an _initial marking_ $M_0 \in \mathbb{N}^P$, so $M_0 : P \to \mathbb{N}$;

* a set $E$ of _events_; and

* two functions 

  *  $pre: P\times E\to \mathbb{N}$, and

  *   $post:  P\times E\to \mathbb{N}$.

=--


##References##

* [[G. Winskel]] and M. Nielsen, Models for concurrency. vol. 3, Handbook of Logic in Computer Science, pages 100 - 200, Oxford Univ. Press, 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).


For an introduction to Petri nets (en francais, which is very clear and accessible) look at

* Robert Valette, [Les R&#233;seaux de Petri](http://homepages.laas.fr/robert/enseignement.d/cour01.pdf).