+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Contents {: .clickToReveal}
### Contents {: .clickToHide tabindex="0"}
+-- {: .hide}
[[!include contents]]
=--
+-- {: .hide}
[[!include mathematicscontents]]
=--
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


+-- {: .query} 
$\,$ 
 <div align="center" >
 <em>Search the nLab ([[Searching the nLab|hints]])</em> 
 <form  name="gsearch" method="get" action="https://www.google.com/search"><input type="text" size="30" name="as_q"/><input type="hidden" name="as_sitesearch" value="https://ncatlab.org/nlab/"/></form>
</div>
$\,$
=-- 

[[About|This]] is a [wiki](http://en.wikipedia.org/wiki/Wiki) for collaborative work on _[[Mathematics]]_, _[[Physics]]_ and _[[Philosophy]]_ --- especially, but far from exclusively, from the [[n-point of view]]: with a sympathy towards the tools and perspective of [[category theory]] and [[higher category theory]].

\tableofcontents

## Purpose
{#purpose}

The nLab records and explores a wide range of mathematics, physics, and philosophy. Along with work of an expository nature, original material can be found in abundance, as can notes from evolving research. Where mathematics, physics, and philosophy arise in other fields, computer science and linguistics for example, the nLab explores these too.

If you take a little time to find something in the literature, or to work through a proof or example, or to find an intuitive or new way to think about something, add a note on it to the nLab! Others will benefit, and you may well find that it proves useful to you too.

A fundamental idea behind the nLab is that the linking between pages of a wiki is a profound way to record knowledge, placing it in a rich context.

For more, see Urs Schreiber's thoughts at [[schreiber:What is... the nLab|What is... the nLab?]]. Further details can be found at [[About]].


## nForum, discussion, comments, and questions
 {#Discussion}

Most nLab pages have a corresponding discussion thread at the [nForum](http://nforum.ncatlab.org), linked to in the menus at the top and bottom of the page. For all but the most trivial edits (correcting spelling or punctuation, etc), we ask that you announce your changes at the nForum using the box at the bottom of the edit page. Typically this would be a short note summarising what you have done, but it can also include what you plan to do, or what you would like others to do! See [[nlabmeta:Welcome to the nForum]] for more on the nForum.

If you have any questions about an nLab page, or would like to discuss or make a comment upon something in it, whether because you feel that something is wrong or missing or for any other reason, you are encouraged and very welcome to use the nForum discussion thread for the page for this purpose too. If the discussion thread does not yet exist, feel free to create it manually: use the 'nLab - Latest changes' category, and give it the same title (case-sensitive!) as the nLab page.

The pages of the nLab have almost always been edited by several people. In almost all cases, we recommend that you use the nForum rather than contact an author of an edit directly, but if you do have a reason to do this, the history of edits to the page with the details of who made them can be found by clicking on 'History' at the bottom of the page.

## Contributing to the $n$Lab
 {#Contributing}

If after looking around for a while you feel like contributing yourself, you are very welcome to do so! See [below](#SoftwareRequirements) for more on how to actually edit, as well as the [[HowTo]].

If you make any edits to the nLab, please follow the guidelines for announcing your changes at the [nForum](https://nforum.ncatlab.org) given [above](#Discussion). If you are unsure whether what you would like to contribute is appropriate, please ask at the nForum before making the edit.

## Viewing and editing the nLab
 {#SoftwareRequirements}

The nLab should be viewable and editable in any modern web browser on any device. For technical reasons, browsers which are able to render [MathML](http://en.wikipedia.org/wiki/MathML), such as Firefox, may render very large pages quicker than other browsers, but these pages are few and far between, and most people will be able to use the browser of their choice. 

Editing the nLab these days can be done more or less as in LaTeX. Macros are not currently available, but mathematics can be entered within dollar signs as usual, [theorem environments](https://ncatlab.org/nlab/show/HowTo#DefinitionTheoremProofEnvironments), sections and tables of contents can be defined as in LaTeX, [commutative diagrams](https://ncatlab.org/nlab/show/HowTo#diagrams) and figures can be created in Tikz or XyMatrix, and so on. For simple formatting, such as italics, and for some other things such as tables, [Markdown](https://en.wikipedia.org/wiki/Markdown) is used. 

See the [[HowTo]] for more on editing the nLab. 

## Making use of material from the $n$Lab
 {#TermsOfUse}

One goal of the $n$Lab is to help make information widely available and usefully related to other information.  In this users and contributors are expected to follow traditional academic practice:

* Using and distributing content obtained from the $n$Lab is free and encouraged if you acknowledge the source, as usual in academia.

  (There is currently no consensus on a more formal license statement, but if it matters check if relevant individual contributors state such on their $n$Lab homepages.)

  If you cite a page you may want to point to a specific version of it, because $n$Lab pages can change.  You can find a list of all the versions of a page by clicking on the **History** link at the bottom of the page itself.

* Conversely, any content contributed to the $n$Lab is publicly available and you should be aware that others may use your contributions (whatever you decide to do with their content elsewhere) and indeed may edit them. In the first case you trust that users will cite your contributions properly, in the second that they will respect and only improve on them. At the same time, you are expected to properly acknowledge sources of information for material entered into the $n$Lab. 

Usually this works well. If there is need for discussion, the 
[nForum](http://nforum.ncatlab.org) is the forum to turn to. If serious problems arise, the [steering committee](#SteeringCommitte) might intervene. 


## Server and setup
 {#Server}

The domain `ncatlab.org` is owned by [[Urs Schreiber]]. 

The $n$Lab server is currently hosted at Carnegie Mellon University, funded in the context of the [HoTT MURI grant](http://homotopytypetheory.org/2014/04/29/hott-awarded-a-muri/). 

> The nLab runs on a server at Carnegie Mellon University that is supported by MURI grant FA9550-15-1-0053 from the Air Force Office of Scientific Research. Any opinions, findings and conclusions or recommendations expressed on the nLab are those of the authors and do not necessarily reflect the views of the AFOSR.

However, we will imminently be moving to the cloud, to an account registered to the [Topos Institute](https://topos.institute/). For this, we rely on donations which have kindly been made to the nLab. See [[funding of the nLab]] for an overview of the financial side of things.

The development of the nLab software and technical administrative matters are currently in the hands of [[Richard Williamson]] and assistant [[Alexis Hazell]]. If you wish to lend a hand, please [contact us](https://nforum.ncatlab.org).

Much of the software behind the nLab has been written especially for the nLab: the latest source can be found at [GitHub](https://github.com/ncatlab/nlab). It was originally an instance of [Instiki](https://golem.ph.utexas.edu/wiki/instiki/show/HomePage), and the shell of it remains (for the moment). Bug reports or other software issues/requests for the nLab are currently best raised in the category _[nLab Technical Matters](https://nforum.ncatlab.org/21/)_ at the [nForum](https://nforum.ncatlab.org/), but can also be posted [on GitHub](https://github.com/ncatlab/nlab/issues).

The $n$Lab page style is due to [[Jake Bian]], originating with his [Kan browser extension](https://sites.google.com/keplr.io/kan) 

The $n$Lab logo is due to [[David Roberts]], inspired by Matisse's painting _[La Gerbe](https://collections.lacma.org/node/207557)_. Besides being an inside reference to [[schreiber:Higher Structures|higher structures]] known as _[[gerbes]]_, the logo represents maybe [[computational trinitarianism]] or the [[Science of Logic|progression of modalities]] or generally the unity of diverse mathematical phenomena revealed by the [[nPOV]]. 




\linebreak

## Steering Committee 
 {#SteeringCommitte}

The $n$Lab is a community undertaking. But for all matters that do require that the $n$Lab is represented to the outside by  an official decision-taking body, we have the [[nlabmeta:steering committee|steering committee]]. _Nobody "is in charge of the $n$Lab"._ But the steering committee is the closest approximation to a body being in charge that we have. 


category: meta

[[!redirects HomePage]]
[[!redirects Home Page]]
[[!redirects Homepage]]
[[!redirects Home page]]
[[!redirects homepage]]
[[!redirects home page]]
[[!redirects nLab]]
