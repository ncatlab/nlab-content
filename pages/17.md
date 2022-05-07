+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Contents {: .clickToReveal}
### Contents {: .clickToHide tabindex="0"}
+-- {: .hide}
[[!include contents]]
=--
=--
=--

This page gives hints for how to edit [[nLab:HomePage|nLab]]-pages.

An easy introduction for elementary basics is

* [[How to get started]].

The following provides more details. For technical help with special features of Instiki (including peculiarities with itex), HTML and XML, and assorted specifics of the nLab, see also the [[FAQ]].

# Contents

* table of contents
{: toc}

## Getting Started

### How to edit the nLab

Hit "edit page" to see how pages are coded. Use the [[Sandbox|Sandbox]] to warm up.  The key point is that links to other pages are placed in <nowiki>[[double brackets]]</nowiki>.

There is no feature to preview your edits.  Instead, submit them and then edit again.  Two successive submissions with the same signature and made within 30 minutes of each other count as one.

### How to start a new page
{#newpage}

To create a new page on the $n$Lab first make an existing page request a link to it, and then click on that requested link. 

In detail:

1. **Create a link request.** 

   1. Identify any existing $n$Lab page which should eventually refer to your new page. 

      (At least one such page ought to exist, if your new page is related to anything, but if you just cannot think of any, use the _[[Sandbox]]_ page).

   1. Hit "edit" on that existing page. 

   1. In the resulting edit pane, add the string 

      <nowiki>[[your new page name]]</nowiki>

      at some sensible point in the source code. 

      (By default: in the "Related entries"-section.)

   1. Hit "submit" below the edit pane. 

   1. See the existing page render again, now with your edit included. If <nowiki>your new page name</nowiki> did not exist yet as a page, you will see that string appear, in the existing entry, in gray with a clickable question mark behind it.
     

2. **Satisfy the link request.**

   1. Click on that question mark to open the edit pane for the new page.

   1. Edit.

   1. Once you hit "Submit" below that edit pane, the new page will appear. 

   There is no preview mechanism: Just keep cycling through "Submit" and "Edit" until you are satisfied. 

_Watch out_: the name of a page is case sensitive, so make your link lowercase if it comes at the beginning of a sentence. (<nowiki>[[like this|Like this]]</nowiki>.) We loosely agreed to try to follow that and some other naming conventions; see [below](#naming).

Use [[redirects]] to allow for other casing to be used when linking to the page elsewhere in the nLab.


### Signing an edit

When you edit a page, you should put your name (with normal capitalisation and spacing) in the box after 'Submit as'. If you don't, then your contribution will be credited to 'Anonymous' (formerly the [[AnonymousCoward]]).

Once you edit a page for the first time, your name will appear at the bottom, grayed out with a question mark since there is no page with your name yet.  You may take this as an invitation to create a user page and tell us about yourself.  But if you don't want to or don't have the time right now, you can forget about this. If you just want to show up on [category: people](http://www.ncatlab.org/nlab/list/people), then you make a page containing only 'category: people' (or someone else may do this for you).

To create your user page, simply click the question mark that appears next to your name at the bottom of the page after making a modification and add content to the edit box that appears. If you'd like to make a user page prior to modifying an existing page, you can do so by making some trivial modification to the [[Sandbox]], which will put your name at the bottom of the page where you can click the question mark. (Or hack the URL.)


### Naming conventions
{#naming}

The following naming conventions for new entries are not set in stone, but we\'re following them for now. Changing page titles results in unnecessary work for the [[lab elves]], so you should try to follow these if possible (or dispute them if not).  It is most important to follow these in links to pages that don\'t yet exist, so that the pages will be created at the correct title (and only once).

* Page titles should contain only ASCII characters.
  * Examples: `<nowiki>[[omega-category]]</nowiki>` instead of `<nowiki>[[$\omega$-category]]</nowiki>` or `<nowiki>[[∞-category]]</nowiki>`.
  * {#tricks} Tricks: To produce '$\omega$-[[omega-category|category]]', try `<nowiki>$\omega$-[[omega-category|category]]</nowiki>`. To produce '[[omega-category|∞-category]]', try `<nowiki>[[omega-category|∞-category]]</nowiki>`.  (The former has proper math-mode formatting, while the latter has proper link scope.)  Unfortunately, `<nowiki>[[omega-category|$\omega$-category]]</nowiki>` does not work.  You can also use [[redirects]] to make `<nowiki>[[∞-category]]</nowiki>` produce '[[∞-category]]', but only when the page already exists.
  * Reason: It's possible to put non-ASCII characters in a name, but not ones generated by iTeX or &...; character entities, so this can be difficult, depending on your browser. To keep things easy, therefore, use only ASCII characters in links. This also helps with creating automatic redirects (which are found by removing accents on letters).
  * Exception: We tend to use common European letters (such as '&#246;', more or less the characters in Latin 1) in names, especially of people (such as [[Kurt Gödel]]), even though we're not really supposed to.

* Page titles should be singular nouns.

  * Examples: Use `<nowiki>[[category]]</nowiki>` instead of `<nowiki>[[categories]]</nowiki>`, `<nowiki>[[faithful functor]]</nowiki>` instead of `<nowiki>[[faithful]]</nowiki>`, and `<nowiki>[[categorification]]</nowiki>` instead of `<nowiki>[[categorify]]</nowiki>` or `<nowiki>[[categorified]]</nowiki>`.

  * Tricks: To produce '[[category|categories]]', try `<nowiki>[[category|categories]]</nowiki>`. To produce '[[faithful functor|faithful]] [[endofunctor]]', try `<nowiki>[[faithful functor|faithful]] [[endofunctor]] </nowiki>`.  Again, you can use redirects to make `<nowiki>[[categories]]</nowiki>` produce '[[categories]]', if the page already exists.

  * Reason: We want only one page on a given concept, regardless of variations in grammar.

  * Exception: Recently we have started to have page titles that are complete sentences (without capitalization or punctuation) that state a simple theorem (typically a universal affirmation in the Aristotelian sense) such as [[compact Hausdorff rings are profinite]] or [[derivations of smooth functions are vector fields]].

* {#PageTitlesShouldBeUncapitalized} Page titles should be uncapitalized, except for words that are always capitalized.

  * Examples: Use `<nowiki>[[homotopy theory]]</nowiki>` instead of `<nowiki>[[Homotopy Theory]]</nowiki>`, but use `<nowiki>[[Lie algebra]]</nowiki>`.

  * Tricks: To produce '[[homotopy theory|Homotopy theory]] is important!', try `<nowiki>[[homotopy theory|Homotopy theory]] is important!</nowiki>`.  If you do this a lot, then you can again create a redirect, if the page exists.

  * Reason: We want only one page on a given concept, regardless of variations in grammar.

* Except as contradicted above, use standard American English spelling conventions.

  * Examples: Use `<nowiki>[[center]]</nowiki>` instead of `<nowiki>[[centre]]</nowiki>` and hyphens as shown in the ASCII-only requirement.
  * Tricks: To produce '[[center|centre]]', try `<nowiki>[[center|centre]]</nowiki>`.  Or, again, make a redirect.

  * Reason: Much of this is written by [[Urs Schreiber]], who uses American English spelling (for the most part, at least).

* Regardless of the above, pages named after specific categories should use the capitalised singular abbreviated form.
  * Examples: Use `<nowiki>[[Set]]</nowiki>` instead `<nowiki>[[Sets]]</nowiki>` and `<nowiki>[[Cat]]</nowiki>` instead of `<nowiki>[[Category]]</nowiki>`.

  * Tricks: Although things like '$\Disc: \Set \to \Cat$' work best in math mode and even '$\Set$' alone looks most consistent that way (with proper math-mode formatting), you have to make the link '[[Set]]' outside of math mode.


### How to merge pages
{#merging}

Suppose we have two pages, named 'A' and 'B', and you decide that they ought to be merged into a single page, say 'A'.  Of course, you need to edit 'A' to contain the material from 'B' and make a coherent whole, but there are also some technical aspects.  We do *not* want to simply delete 'B', since it contains the history of the edits to that page, which might turn out to be useful.  However, we *do* want these two things:

1.  links to 'B' ought to send the reader to 'A';
2.  the old page 'B' should be clearly marked as archive material.

We accomplish (1) with a [[redirect]]; we accomplish (2) with a [[page move]].  If you do this too carelessly, then it will not work; in the worst case, links to 'B' will still go to the archive page, and that will look to the casual reader like a regular page.  So follow these steps:

1.  Edit 'A' so that it looks how you want, and add the line '[[!redirects B]]' to the bottom.  Submit.
2.  Open 'B' for editing.
3.  Click the checkbox 'Change page name.', which will bring up a new field 'New name:'.
4.  In that field, add ' > history' to the end, so that 'B' becomes 'B > history'.
5.  Click in the big edit box, which will automatically add '[[!redirects B]]' to the top.
6.  Change the line '[[!redirects B]]' into '< [[B]]' instead.
7.  Delete everything else (consisting of the material that you already merged into 'A').
8.  Submit.

The result is that links to 'B' will redirect to 'A' (not to 'B > history').  And if anyone does land on 'B > history', all that they will see is '<&#160;[[HomePage|B]]' with a link to 'B' (properly redirected to 'A').  But if they\'re really at 'B > history' on purpose to check the edit history, then that history is there for them. 


### How to remove a page 

Please make a request at the [nForum](https://nforum.ncatlab.org/). 

## How to organize and write content
 {#HowToOrganizeAndWriteContent}

### Page organization
 {#PageOrganization}

We encourage authors to structure pages by sections and subsections
as indicated in the 

* [[Template page]].

Every page starts out tiny and may not seem to need a structure by subsections. But it will grow and eventually the information it provides may be hard to _recognize_ without some global structure guiding the reader's attention. After all, the natural evolution of articles makes the $n$Lab function more like an encyclopedia than a novel.  Moreover, even with little material there in the beginning, a structure by subsections helps the collaborative process, as it makes it easer to decide for new authors where to add what.

### Definition-, Theorem-, Proof environments
 {#DefinitionTheoremProofEnvironments}

You should include actual mathematics in appropriate environments, as familiar from textbooks and research articles in mathematics.

#### LaTeX-style syntax
 {#LatexSyntax}

As of mid-2018, one can use environments exactly as in LaTeX.

For example the code

$$
  \array{
    \mathrlap{
      \backslash\text{begin}\{\text{theorem}\}  
    }
    \\
    & 
    \;\;
    \mathrlap{\backslash\text{label}\{\text{SomeTheorem}\}}
    \\
    & 
    \;\; 
    \mathrlap{\text{Some theorem.}}
    \\
    \mathrlap{\backslash\text{end}\{\text{theorem}\}}
  }
$$

produces:

> \begin{theorem} \label{SomeTheorem}
>   Some theorem.
> \end{theorem}

The available environments are listed below. Some environments can be specified in several ways.

<table>
  <thead>
    <tr><th>Environment</th><th>Syntax</th></tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Definition</td>
      <td>definition</td>
    </tr>
    <tr>
      <td>defn</td>
    </tr>
    <tr>
      <td rowspan="2">Theorem</td>
      <td>theorem</td>
    </tr>
    <tr>
      <td>thm</td>
    </tr>
    <tr>
      <td>Proof</td>
      <td>proof</td>
    </tr>
    <tr>
      <td rowspan="3">Proposition</td>
      <td>proposition</td>
    </tr>
    <tr>
      <td>prop</td>
    </tr>
    <tr>
      <td>prpn</td>
    </tr>
    <tr>
      <td rowspan="2">Remark</td>
      <td>remark</td>
    </tr>
    <tr>
      <td>rmk</td>
    </tr>
    <tr>
      <td rowspan="2">Corollary</td>
      <td>corollary</td>
    </tr>
    <tr>
      <td>cor</td>
    </tr>
    <tr>
      <td rowspan="2">Lemma</td>
      <td>lemma</td>
    </tr>
    <tr>
      <td>lem</td>
    </tr>
    <tr>
      <td rowspan="2">Notation</td>
      <td>notation</td>
    </tr>
    <tr>
      <td>notn</td>
    </tr>
    <tr>
      <td>Terminology</td>
      <td>terminology</td>
    </tr>
    <tr>
      <td rowspan="2">Conjecture</td>
      <td>conjecture</td>
    </tr>
    <tr>
      <td>conj</td>
    </tr>
    <tr>
      <td>Scholium</td>
      <td>scholium</td>
    </tr>
    <tr>
      <td rowspan="2">Assumption</td>
      <td>assumption</td>
    </tr>
    <tr>
      <td>assum</td>
    </tr>
    <tr>
      <td>Example</td>
      <td>example</td>
    </tr>
    <tr>
      <td>Exercise</td>
      <td>exercise</td>
    </tr>
    <tr>
      <td>Statement</td>
      <td>statement</td>
    </tr>
  </tbody>
</table>

Labels for the purpose of referencing work exactly as in LaTeX: put ```\label{SomeTheorem}``` anywhere inside the environment block. Later, one can reference it as Theorem \ref{SomeTheorem}. Again, see the [source](https://ncatlab.org/nlab/source/HowTo) of this page for how to produce this reference.  

#### Older syntax

An older syntax for this is described at [Instiki theorem environments](http://golem.ph.utexas.edu/wiki/instiki/show/Theorems):

A [[definition]] should be enclosed in 

     +-- {: .num_defn}
     ###### Definition

      (Definition goes here)

     =--

A [[proposition]] or [[theorem]] should be enclosed in 

     +-- {: .num_prop}
     ###### Proposition

      (Proposition goes here)

     =--

or

     +-- {: .num_theorem}
     ###### Theorem

      (Theorem goes here)

     =--

and their [[proof]] in 


     +-- {: .proof}
     ###### Proof


       (Proof goes here.)

     =--

A corollary in

     +-- {: .num_cor}
     ###### Corollary

      (Corollary goes here)

     =--

and a remark in 

     +-- {: .num_remark}
     ###### Remark

      (Remark goes here)

     =--

Beware, contrary to the behaviour with the LaTeX syntax described above, you do need to use the labels exactly as given above. That is, it needs to be `defn`, `thm`, and `cor`; neither `definition` nor `theorem` nor `corollary` (nor other abbreviations such as `def`) will be recognized by the software.

Use the LaTeX syntax where possible.

### Cross-links
 {#CrossLinks}


A central point of the $n$Lab is that information is _linked_. Little value is added to the world when information is added to an $n$Lab page if it is not interlinked there with other $n$Lab entries such as to make sure that users who might look for it will actually eventually find it by following some links.

Therefore you should hyperlink the central keywords in what you write, by enclosing them in square brackets. Ideally, each and every keyword would be hyperlinked, certainly when it occurs first. Don't assume that the reader has the same background as you have. If you explain something by invoking other technical terms, at least provide links to $n$Lab entries where these other terms are defined.

Analogously, when you create a new page, make sure that it is _linked to_ from at least one relevant other page. An entry on a new kind of _manifold_ deserves to be linked to from a list of "related entries" at _[[manifold]]_, for instance.

Apart from guiding users to your entry this way, notably this will also help search engines to index the $n$Lab and make your new entry appear listed when people search for something related.

### Mathematical conventions
 {#MathematicalConventions}

There is really no such thing as a "global convention on the $n$Lab" for ambiguous meaning of mathematical terms and symbols. Unlike in a text book by a single or a handful of authors, there is just no way that we can even try to enforce global conventions. Typically each author decides on his or her own. 

Therefore the general rule is: whatever you write in some entry, try to make sure that you provide enough context that the relevant conventions are clear. If you find yourself using some notation for the first time on a page and are worrying if readers will read it as intended, be sure to add a parenthetical remark (where we use here the convention that...) or similar. 

If you feel that you need to refer to a specific convention repeatedly over several $n$Lab pages, just create another page that states the convention, and then simply point to that page.

One example of this that we have is the _[[implicit infinity-category theory convention]]_-page.



## Special Typesetting Features

### How to make links to subsections of a page ##
 {#HowToMakeLinksToSubsections}

#### Links to sections

When you create a section header, you can add an HTML anchor tag to it with the following syntax:

     <nowiki>## Heading {#anchorname}</nowiki>

__Note that the tag must be placed at the end.__ Then you can make a link to it using the syntax:

     <nowiki>[[some page#anchorname|link text]]</nowiki>

If the link is to the same page then the page name can be omitted by using the syntax:

     <nowiki>[link text](#anchorname)</nowiki>

__Note that a single bracket link with only an anchor doesn't function correctly when viewing a particular revision or a difference between revisions.__

{#strange}Strangely single bracket link texts allow math expressions while double bracket texts don't. For example

    <nowiki>[$Set^\to$](Sierpinski+topos)</nowiki> vs <nowiki>[[Sierpinski topos|$Set^\to$]]</nowiki> vs <nowiki>[$Set^\to$](https://ncatlab.org/nlab/show/Sierpinski+topos).</nowiki>

produces

+-- {: .standout}
[$Set^\to$](Sierpinski+topos) vs [[Sierpinski topos|$Set^\to$]] vs [$Set^\to$](https://ncatlab.org/nlab/show/Sierpinski+topos) .
=--


Of course, you can link to it from outside the nLab by adding `http://ncatlab.org` at the beginning of the link.

Note that if you skip the first step, it is still *possible* to create a link to a subsection, since (at least if the page has a table of contents) every section on the page is automatically assigned an HTML anchor by Instiki.  However, using such links is *not* encouraged, since the automatically generated anchor names will change whenever the page is rearranged and go away if a manual anchor name is added, which will cause such links to break. 

{#thispgh}The same type of syntax enables one to link to arbitrary text blocks such as paragraphs or list elements, such as a [link](#thispgh) to this paragraph itself. __Note that these tags must be at the start of the text__. In particular, a bibliographic reference can be made by first by creating an anchor: 

     * {#xyz} Reference 

which can then be linked to from within the same page by writing 

     [link text](#xyz). 

#### Definition/Proposition/Theorem-numbering

When you write a numbered definition or proposition or theorem, you can also simultaneously create an anchor by writing:

     +-- {: .num_defn #definitionname}
     ###### Definition
     ...
     =--


     +-- {: .num_prop #propname}
     ###### Proposition
     ...
     =--


     +-- {: .num_theorem #theoremname}
     ###### Theorem
     ...
     =--

And then you can link to it in the same ways:

<nowiki>
     [[some page#theoremname|see this theorem]]
     [see this theorem](#theoremname)
</nowiki>

When you link to a theorem on the *same* page, however, it's better to use the syntax (without the space between `\ref` and `{`, it is present here just to avoid it being parsed:

     see Theorem <nowiki>\ref {theoremname}</nowiki>

(which inserts the number, as well as creates a hyperlink) since that will also work properly when the page is exported to LaTeX.



#### Equation numbering

To make an equation be automatically numbered use angular brackets instead of dollar signs

     \[
       \exp(\pi i) + 1 = 0 
     \]

To refer to this numbered equation, add a label

     \[
       \label{SomeEquation}
       \exp(\pi i) + 1 = 0 
     \]

and then refer to it later in the text by typing

     see equation <nowiki>(eq:SomeEquation)</nowiki>.


#### Table of contents

Since 2019, the recommended way to make a table of contents for a page (and almost any page should have a table of contents) is to write the following at the top of the page, or wherever the table of contents is to appear, without the space between the backslash and `tableofcontents`.

```
     \ tableofcontents
```

An older method is to write


```
     * table of contents 


     {: toc}

```

(including the line break!) at the position where the table of contents is to appear. You may want to label the table of contents by writing

     # Contents #
     * table of contents 
     {: toc}

or (at the top of the page)

     # [page title] #
     * table of contents 
     {: toc}

(which also gives the opportunity to use a more nicely formatted page title if special characters or mathematical formatting are wanted).

The items in the table of contents will be the section headlines marked by

     ## top level headline ##


     ### second level headline ###


     etc.

Instead of "table of contents" after the asterisk, you can write anything you like: this line will not be displayed but is still required to kick in the CSS that makes this possible. 

It is important that the section headings not contain anything that shouldn't go in the table of contents.  Whilst formatting is allowed, wiki-links are not (since then the entry in the table of contents would have a link inside of a link).


### How to cite and record references
 {#HowToCiteAndRecordReferences}

At the end of each $n$Lab entry should be a section 

      ## References

or sometimes

      ## Literature

which contains a bullet list of relevant references. A standard way to format an entry is this list is the following:

      * {#LastnameAnotherlastnameYear} <nowiki>[[Firstname Lastname]]</nowiki>, <nowiki>[[Anotherfirstname Anotherlastname]]</nowiki>, _Title_, Journal, volume, year (<nowiki>[arXiv:xxxx.yyyyy](https://arxiv.org/abs/xxxx.yyyyy)</nowiki>, <nowiki>[doi:xyz](http://doi.xyz)</nowiki>)

which comes out as

>  * {#LastnameAnotherlastnameYear} [[HowTo|Firstname Lastname]], [[HowTo|Anotherfirstname Anotherlastname]], _Title_, Journal, volume, year ([arXiv:xxxx.yyyyy](https://arxiv.org/abs/xxxx.yyyyy), [doi:xyz](http://doi.xyz))


Given such an item in the list of references, a standard way to reference it from the main text of the entry is as follows:

      see (<nowiki>[Lastname-Anotherlastname Year, theorem 1.3](#LastnameAnotherlastnameYear)</nowiki>)

which comes out at 

> see ([Lastname-Anotherlastname Year, theorem 1.3](#LastnameAnotherlastnameYear))

This produces a hyperlink, and in fact such that following it brings up the above bullet item highlighted by a gray box.


### How to make comments and ask questions {#query}

In general, the place to make comments and ask questions is at the [nForum](https://nforum.ncatlab.org/discussions/?CategoryID=0). Each page has a 'Discuss this page' link in the menu at the top. Clicking on this will take to the thread for discussion of the page in the 'Latest changes' category, if it already exists. Just add a comment to the thread. If it does not exist, you will be taken to the nForum home page. Just start a new discussion there, selecting 'Latest changes' as the category and with title the same as the nLab page, and make your comment/ask your question.

Whilst questions are answered and discussions are carried out at the nForum, the *conclusion* should often be recorded on an nLab page. If it's about a particular page, then of course put it on that page; if it's a general question then it could be recorded on [[HowTo|this How To]] or the [[FAQ]].  As this is a wiki, you can do this recording yourself when your question is answered.

That said, the wiki software does contain a mechanism for putting questions and comments on a wiki page itself: edit the page and put your comment or question in a __query block__ as shown in this example:

    +-- {: .query}
    How do I ask a question?
    =--

which produces

+-- {: .query}
How do I ask a question?
=--

In general, this is the wrong way to go about asking a question.  When you put a query box on a page, often none of the other contributors will notice it for a long time, so it will take a long time for the question to be answered, and in the meantime it makes the page cluttered and ugly for other readers.  However, *occasionally* it may be appropriate to record a brief question in a query box, if it has already been discussed at the nForum and the conclusion was not satisfactory.  In this case a link to the nForum discussion should be included in the query box in preference to any lengthy detail about the question and discussion.

(Before the nForum existed, it was much more common to ask questions using query boxes. Some such query boxes still remain undiscovered on various pages, but whenever we find one we generally migrate it to the n-Forum.)

### How to make a standout box
 {#standout}

If you want to make some text stand out (an important theorem, or slogan), you can do it using a __standout box__.  The mechanism is similar to a query box, although the purpose is different: while a query box is for a temporary question and should be removed once that question is resolved, a standout box is a permanent feature of a page that simply emphasizes a small amount of text.  To make a standout box, write:

    +-- {: .standout}
    First quantization is a mystery, but second quantization is a functor. 
    =--

which produces

+-- {: .standout}
First quantization is a mystery, but second quantization is a functor. 
=--




### How to include one page within another

If you have some material at a page called `foo` that you want to include directly in pages called `bar` and `baz`, then type <nowiki><code>[[!include foo]]</code></nowiki> in `bar` and `baz`.  For an example, see how [[contents]] is included at the tope of this page.  Also see how [[contents]] itself has been formatted so that it will appear as a sidebar when included.

Besides such sidebars that appear in many pages, you can also use inclusion to put in something that contains a bunch of ugly code (such as raw <abbr title="scalable vector graphics">SVG</abbr>, see [here](#IncludeSVG)) without mucking up the rest of the page.  That is, you put your messy code in `bar/foo` and then put <nowiki><code>[[!include bar/foo]]</code></nowiki> in `bar`.  Note that this is for something that, logically, should appear within `bar` itself, which is why `bar` appears in the name of the included page.

Note that the included page goes directly in where it is called with no surrounding whitespace.  This can mean that formatting rules are broken on the include.  For example, if the included file starts and ends with a `div` tag and is included with no surrounding blank lines then this breaks the rules and will generate an error.


### How to upload files
 {#HowToUploadFiles}

To upload a file, proceed as follows:

1. Type 

   `<nowiki>[[FileName.xyz:file]]</nowiki>`

   into the edit page for some entry, or

   `<nowiki>[[FileName.xyz:pic]]</nowiki>` 

   in the case of a picture;

1. hit "submit";

1. in the rendered entry, find a grayish link labeled "FileName.xyz" followed by a question mark;

1. click on the question mark to open an upload dialogue and follow the instructions there;

   notice that the dialogue field "Description" is asking for the text that will appear hyperlinked to your file. If you put no text here, no link to your file will appear by itself;
  
1. complete the dialogue by hitting "upload";

1. find in the rendered entry the previously grayish text "FileName.xyz" replaced by the text that you entered into the "Description"-box in the file upload dialogue, and hyperlinked to your file;

1. due to a bug, if you want that link to persist, you need to make any further edit to the entry (e.g. add a whitespace) and "submit" again.

After this, the file is now sitting at this URL:

      https://ncatlab.org/nlab/files/FileName.xyz 

Hints:

1. If you uploaded a picture using the `:pic` syntax and do not wish to tweak the displayed image in any way, there is no need to do anything. If you uploaded it using the `:file` syntax, you will probably want to _remove_ the file upload code 

           <nowiki>[[FileName.xyz:file]]</nowiki>
 

   (which renders to a link to the file) and instead add a line like

        \begin{imagefromfile}
            "file_name": "FileName.xyz"
        \end{imagefromfile}

   which makes the actual image show up in entry, There are a number of other posible parameters for an `imagefromfile` block, see {#ImageFiles}.
    

1. If you uploaded a pdf (or similar) for a reference, you will probably want to make sure that the "Description" text in the upload dialogue is "pdf" (or similar), so that the code

        A. Name, _A title_, A Journal, AYear ([[FileName.xyz:file]])

   renders to 

   "A. Name, _A title_, A Journal, AYear (pdf)"
 
   with "pdf" hyperlinked to your file.

1. There is a size limit for files to upload. The functionality is meant to be used for uploading _ingredients_ of $n$Lab entries (such as pictures or references) which are not available for linking elsewhere on the web, or not reliably so.

   If you try to abuse the file upload for archiving your personal files, the [[steering committee]] will intervene.

### How to use redirects

See [[redirects]].


### How to put parentheses in external links

Since the mechanism for inserting links uses parentheses to delimit the link, it's not obvious how to put parentheses actually in the link itself.  Since Wikipedia uses them a fair bit, it's worth knowing how to put them in.  The trick is to use the URL codes rather than the actual characters.  URL codes are generally used to send "unsafe" characters in URLs (safe characters are <nowiki>`a`-`zA`-`Z0`-`9$-_.+!\*'(),`</nowiki>).  Although parentheses are actually "safe", due to their special meaning for the markdown filter, to put them in URLs here they need to be treated as "unsafe".  URL codes have the syntax `%hex` where `hex` is the index of the character in the ASCII character set represented as a 2-digit hexadecimal.  Wikipedia (among other places) has a [table](http://en.wikipedia.org/wiki/ASCII#ASCII_printable_characters) of the character set from which one can read off the required hexadecimal.  In particular, we see that `(` is `%28` and `)` is `%29`.  Thus

    [Monad (category theory)#Monads and adjunctions](http://en.wikipedia.org/wiki/Monad_%28category_theory%29#Monads_and_adjunctions)

produces

:  [Monad (category theory)#Monads and adjunctions](http://en.wikipedia.org/wiki/Monad_%28category_theory%29#Monads_and_adjunctions)



### How to add a floating table of contents

Many pages include a "floating table of contents" at the top right-hand side with links to other pages on similar topics.  The lists of related pages are separate pages with names such as [[category theory - contents]]; if you want to create a new one, look at the syntax of existing ones.

To add a floating TOC to a new page, in such a way that it will be automatically collapsed until moused over, use code such as the following at the top of the page:

~~~
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category Theory
+-- {: .hide}
[[&excl;include category theory - contents]]
=--
=--
=--
~~~

If you want to include multiple contents pages, you can repeat the four lines from the one starting with `####` through the first `=--` line.


### How to draw commutative diagrams and pictures {#diagrams}

#### Tikz

As of 2019, one can use tikz or tikzcd exactly as one would in LaTeX. The only difference to LaTeX is that ```\usetikzlibrary``` lines should be put _inside_ the blocks. 

Under the hood, this works by running pdflatex and then generating an SVG from the resulting pdf, which is included in the HTML source of the rendered page.

##### Examples

Picture:

\begin{centre}
    \begin{tikzpicture}
      \draw[blue, ->] (0,0) -- (1,0) -- (1,-1);
    \end{tikzpicture}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{tikzpicture}
        \draw[blue, ->] (0,0) -- (1,0) -- (1,-1);
    \end{tikzpicture}
\end{centre}
</nowiki>
```

Single [[morphism]]:

\begin{centre}
    \begin{tikzcd}
        x \ar[r] & y
    \end{tikzcd}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{tikzcd}
        x \ar[r] & y
    \end{tikzcd}
\end{centre}
</nowiki>
```

Diagram of [[adjoint functors]] {#TypesetAdjointFunctors}:

\begin{centre}
    \begin{tikzcd}
        \mathcal{D} \arrow[r, shift right=7pt, "R"', "\bot"] & 
            \mathcal{C} \arrow[l, shift right=7pt, "L"']
    \end{tikzcd}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{tikzcd}
        \mathcal{D} \arrow[r, shift right=7pt, "R"', "\bot"] & 
            \mathcal{C} \arrow[l, shift right=7pt, "L"']
    \end{tikzcd}
\end{centre}
</nowiki>
```

#### Xymatrix

As of 2019 you can format commutative diagrams in the nLab using xymatrix command, almost as you would in a LaTeX document. The only significant differences are:

1. Use a `<nowiki>\begin{xymatrix} ... \end{xymatrix}</nowiki>` block rather than a `\xymatrix{...}` block. 

1. Some global parameters can be passed inside the `<nowiki>\begin{xymatrix}</nowiki>` tag. For example, as usual, one can use `@=1.5em` to increase row and column separation, replacing `@` by `@C` (resp. `@R`) for column (resp. row=) separation. Thus one writes: `<nowiki>\begin{xymatrix@=1.5em}</nowiki>`. In addition, unlike in LaTeX, one can pass parameters in square brackets: `<nowiki>\begin{xymatrix[font = \large, border = 2em]}</nowiki>` or `<nowiki>\begin{xymatrix@=1.5em[font = \large, border = 2em]}</nowiki>`. Here the value of `font` controls the font size throughout the diagram, and `border` adds some whitespace around the figure, which is sometimes needed when using curved arrows. One can use only one of the two parameters instead of both.

Under the hood, this works by running pdflatex and then generating an SVG from the resulting pdf, which is included in the HTML source of the rendered page.

Use Tikz rather than Xymatrix if you do not have a strong preference or have not used either before. But it is fine to use Xymatrix if this is what you are used to.

##### Examples

Triangle:

\begin{centre}
    \begin{xymatrix}
        A \ar[r] \ar[dr] & B \ar[d] \\ & C
    \end{xymatrix}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{xymatrix}
        A \ar[r] \ar[dr] & B \ar[d] \\ & C
    \end{xymatrix}
\end{centre}
</nowiki>
```

Bent arrows:

\begin{centre}
    \begin{xymatrix[border = 2pc]}
        A \ar@/^2.0pc/[r] \ar@/_2.0pc/[r] & B
    \end{xymatrix}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{xymatrix[border = 2pc]}
        A \ar@/^2.0pc/[r] \ar@/_2.0pc/[r] & B
    \end{xymatrix}
\end{centre}
</nowiki>
```

Parallel arrows:

\begin{centre}
    \begin{xymatrix}
        A \ar@<.6ex>[r] \ar@<-.6ex>[r] & B
    \end{xymatrix}
\end{centre}

Source:
  
```
<nowiki>\begin{centre}
    \begin{xymatrix}
        A \ar@<.6ex>[r] \ar@<-.6ex>[r] & B
    \end{xymatrix}
\end{centre}
</nowiki>
```

2-cell:

\begin{centre}
    \begin{xymatrix[font = \large]@C+2pc}
        A \rtwocell^f_g{\alpha} & B
    \end{xymatrix}
\end{centre}

Source:

```
<nowiki>\begin{centre}
    \begin{xymatrix[font = \large]@C+2pc}
        A \rtwocell^f_g{\alpha} & B
    \end{xymatrix}
\end{centre}
</nowiki>
```

#### Older workaround for commutative diagrams

An older workaround is to use use arrays or matrices.  For example,

       $$
       \begin{matrix}
         (f/g)& \to & A \\
         \downarrow&\underset{\alpha}{\swarr}&\, \downarrow f\\
         B &\underset{g}{\to} & C
       \end{matrix}
       $$

   produces

   $$
   \begin{matrix}
     (f/g)& \to & A \\
     \downarrow&\underset{\alpha}{\swarr}&\, \downarrow f\\
     B &\underset{g}{\to} & C
   \end{matrix}
   $$

   In many cases, you may wish to tweak the alignments (say, of vertical arrows), using `\mathrlap{}` or `\mathllap{}`:

   $$
   \begin{matrix}
   B^{\mathrlap{A}} & \longrightarrow & 1^{\mathrlap{A}} \\
   \mathllap{\scriptsize{\sigma^A}}\downarrow & & \downarrow \mathrlap{\scriptsize{t^A}} \\
P(B)^{\mathrlap{A}} & \underset{\chi_\sigma^A}{\longrightarrow} &  P(1)^{\mathrlap{A}}
   \end{matrix}
   $$

   is produced by
        
        \[
        \begin{matrix}
        B^{\mathrlap{A}} & \longrightarrow & 1^{\mathrlap{A}} \\
        \mathllap{\scriptsize{\sigma^A}}\downarrow & & \downarrow               \mathrlap{\scriptsize{t^\alpha}} \\
        P(B)^{\mathrlap{A}} & \underset{\chi_\sigma^A}{\longrightarrow} & P(1)^{\mathrlap{A}}
        \end{matrix}
        \]

   Matrix and array environments also accept certain options. Here is an example using a "\rowlines{solid}" option to hack a sequent derivation (much more nicely than by resorting to \frac commands): 

   $$
   \array{\arrayopts{\rowlines{solid}}
   X \times B \to P A\;\;\; in\; \mathbf{S} \\
   X \times B \nrightarrow A\;\;\; in\; Rel(\mathbf{S}) \\
   X \nrightarrow A \times B\;\;\; in\; Rel(\mathbf{S}) \\
   X \to P(A \times B)\;\;\; in \; \mathbf{S}
   }
   $$ 

   is produced by 

       $$
       \array{
       \arrayopts{\rowlines{solid}}
       X \times B \to P A\;\;\; in\; \mathbf{S} \\
       X \times B \nrightarrow A\;\;\; in\; Rel(\mathbf{S}) \\
       X \nrightarrow A \times B\;\;\; in\; Rel(\mathbf{S}) \\
       X \to P(A \times B)\;\;\; in \; \mathbf{S}
       }$$

But use Tikz wherever possible.

### Image files
  {#ImageFiles}


One can upload an image to the nLab as follows. 

1. Add `<nowiki>[[some_picture.jpg:pic]]</nowiki>` or `<nowiki>[[some text that you wish to display|some_picture.jpg:pic]]</nowiki>` to the page to which you wish to add the image. Save your edit.

2. Click on the `?` symbol that appears after 'some_picture.jpg' or 'some text that you wish to display' on the page. 

3. You will be sent to a page where you can upload the image.

Once uploaded, the picture should appear on the page. However, the `:pic` functionality does not allow much configuration. Instead, once it is uploaded one can replace it by an `imagefromfile` block, such as the following.

<nowiki>
        \begin{imagefromfile}
            "file_name": "FileName.xyz"
        \end{imagefromfile}
</nowiki>

The contents of the block must be a valid JSON, but without curly opening and closing braces. There are several possible parameters. A common case is the following, which sets the width of the image (the height is automatically adjusted correspondingly).

<nowiki>
        \begin{imagefromfile}
            "file_name": "FileName.xyz",
            "width": 300
        \end{imagefromfile}
</nowiki>

The default unit is pixels; to specify a different one, or to make it explicit, one uses the 'unit' parameter. Currently the only permitted values are "px" and "em", which correspond to pixels and 'em' respectively.

<nowiki>
        \begin{imagefromfile}
            "file_name": "FileName.xyz",
            "width": 300,
            "unit": "px"
        \end{imagefromfile}
</nowiki>

Another common case is the following, which puts the image to the right of the page with the other text fitting around it, with a nice margin in between. The 'unit' inside the 'margin' block behaves in the same way as the overall width/height, in particular defaulting to pixels, but applies only to the margin.

<nowiki>
        \begin{imagefromfile}
            "file_name": "FileName.xyz",
            "float": "right",
            "margin": {
                "top": -40,
                "right": 0,
                "bottom": 20,
                "left": 20
            }
        \end{imagefromfile}
</nowiki>

The full list of options is shown below. Except for "file_name", these are all either optional or have defaults.

<nowiki>
        \begin{imagefromfile}
            "file_name": "FileName.xyz",
            "web": "nlab",
            "width": 300,
            "height": 300,
            "unit": "px",
            "float": "right",
            "margin": {
                "top": -40,
                "right": 0,
                "bottom": 20,
                "left": 20,
                "unit": "px"
            },
            "alt": "Some picture",
            "caption": "This is some picture"
        \end{imagefromfile}
</nowiki>

These should be fairly self-explanatory. The `alt` parameter corresponds to the `<img>` attribute of the same name.

Note in particular that a caption can be added. If one is floating the graphic and one uses a negative value for `top` in the values for `margin`, which is quite often a good idea, then one typically will need a positive value for `bottom` in order for text wrapping around the image not to obscure the caption.

Be judicious when floating graphics. It may be easier to read a page, especially on a mobile phone, if the graphic is simply placed below a paragraph rather than floating to the side of it. 


### How to centre

Text or figures can be centred exactly as in LaTeX. For instance,

\begin{centre}
    Hello!
\end{centre}

is produced by

```
<nowiki>
    \begin{centre}
        Hello!
    \end{centre}
</nowiki>
```

or by the following (i.e. either UK or US spelling can be used).

```
<nowiki>
    \begin{center}
        Hello!
    \end{center}
</nowiki>
```

## Other Sources of Information

### Instiki HowTo

For general information and help with Instiki, see the [Instiki](http://golem.ph.utexas.edu/instiki/show/HomePage) wiki.

Here are some useful specifics:

* [Use basic Markdown syntax](http://daringfireball.net/projects/markdown/syntax)
* [Make tables, footnotes, etc](http://maruku.rubyforge.org/maruku.html#extra)
* [Add definitions and theorems](http://golem.ph.utexas.edu/instiki/show/Theorems)
* [Add metadata to your markup](https://golem.ph.utexas.edu/~distler/maruku/proposal.html)
* [Type itex equations](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)
* [Use wiki syntax](http://golem.ph.utexas.edu/instiki/show/Syntax#wiki)
* [Embed SVG in equations](http://golem.ph.utexas.edu/instiki/show/SVG)
* [Upload files](http://golem.ph.utexas.edu/instiki/show/File+Uploads)
* [Use keyboard shortcuts](http://golem.ph.utexas.edu/instiki/show/AccessKeys)

### Survey of available math typesetting commands

* [itex2MML Command Summary](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html) 
* [webTeX documentation](https://golem.ph.utexas.edu/~distler/WebTeX/docs/wtxsec5.html)

This is worth perusing carefully;
 for example, iTeX does not provide a command such as `\prescript` to generate left subscripts.
 Instead it contains the more general `\multiscripts` command to typeset subscripts and superscripts
 both to the left and right of an expression. For instance,
 the math mode text `\multiscripts{_0^2_1}{R}{_i^j_k}` produces

$$\multiscripts{_0^2_1}{R}{_i^j_k}$$ 

## Technical

### Software required to use the $n$Lab
{#software}

The $n$Lab serves mathematical symbols as [MathML](http://en.wikipedia.org/wiki/MathML). Presently the only browser with _native_ MathML support, and hence immediate rendering of the formulas, is [Firefox](http://www.mozilla.com/firefox/).

Essentially all other browsers fall back to rendering MathML formulas using the [MathJax](https://www.mathjax.org/) [polyfill](https://en.wikipedia.org/wiki/Polyfill_(programming%29). This works, but is slow.  On small pages it is fine, on larger pages with many formulas MathJax may take up to several minutes for rendering.
 
### How to search the nLab & nForum from firefox

(Firefox - and clones - specific)

Here are some search plugins for firefox that will let you search the nLab from the firefox search bar.  **EDIT:** These are old and may not work with recent versions of Firefox.  Instead you can use the [search engine creator plugin](https://addons.mozilla.org/en-US/firefox/addon/search-engine-creator/).  Someone should update these files to conform to [OpenSearch](https://developer.mozilla.org/en-US/Add-ons/Creating_OpenSearch_plugins_for_Firefox); then they might work with other browsers too.

* [[nlab-search.xml:file]]: searches the nLab (like the search box at the top of every page).
* [[nlab-goto.xml:file]]: takes you directly to the page with a given exact title (if it exists; otherwise it takes you to an edit box to create such a page).
* [[nlab-edit.xml:file]]: takes you directly to the "edit" page for a given title.
* [[nforum-topic-search.xml:file]]: searches the nForum Topics.
* [[nforum-comment-search.xml:file]]: searches the nForum Comments.

It would be nice if these had different icons.  To use one or more of these, drop them in the 'searchplugins' directory of your firefox profile.

Alternatively, you can try the [add to search bar](https://addons.mozilla.org/en-US/firefox/addon/add-to-search-bar/) add-on for Firefox.  This will let you right-click in the search box on any page and add it to your search bar.  (You can't duplicate the "goto" and "edit" plugins this way, though.)

If DuckDuckGo is your search engine, you can type "!nl" to search nLab, e.g. "!nl morphism".

### How to edit nLab pages in your favorite text editor

(Firefox - and clones - specific)

One way to do this is to install one of several firefox extensions, e.g. [for Emacs](https://addons.mozilla.org/en-US/firefox/addon/edit-with-emacs1/?src=search) or [for Sublime Text, Atom, VS Code, and Vim](https://addons.mozilla.org/en-US/firefox/addon/ghosttext/?src=search). There are also extensions which add some basic editor features to html text areas, for instance [Find & Replace for Text Editing](https://addons.mozilla.org/en-US/firefox/addon/find-replace-for-text-editing/?src=search) allows you to use regular expressions and text templates.

If your favorite editor is [Emacs](http://www.gnu.org/software/emacs/) with [AucTeX](http://www.gnu.org/software/auctex/), you may find the following snippet useful to put in your `.emacs` file:

    (add-to-list 'auto-mode-alist '("/\\(www.\\)?ncatlab.org" . latex-mode))
    (add-to-list 'auto-mode-alist '("/golem.ph.utexas.edu" . latex-mode))
    (defun nlab-latex-fixes ()
      (when (or (string-match "/\\(www.\\)?ncatlab.org" buffer-file-name)
                (string-match "/golem.ph.utexas.edu" buffer-file-name))
      (longlines-mode t)
      (set (make-local-variable 'TeX-open-quote) "\"")
      (set (make-local-variable 'TeX-close-quote) "\"")))
    (add-hook 'LaTeX-mode-hook 'nlab-latex-fixes)

This will tell Emacs to automatically edit nLab pages (and nCafe comments as well, for good measure) in LaTeX mode, with long lines wrapped using soft returns, and ordinary double-quotes rather than LaTeX ones.

### How to print a page from the nLab

If you just print it directly, the logo will become a huge blob that takes up the entire first page.  I know, we can and should fix this, but we haven\'t.  So for now, use the 'Print' link at the bottom of the page.  As a shortcut in most browsers on most operating systems, hit Alt-Shift-P while the focus is in the page to go to the printable page.

### How to customize the nLab

(Firefox - and clones - specific)

You may wish to customize the font scheme (both for math or text) on the nLab, as well as tweak things such as the small edit box for comments. Try using the Stylish add-on if you are using Firefox; Stylish is a plug-in for firefox enabling you to customize websites; it is available [here](https://addons.mozilla.org/en-US/firefox/addon/2108).

Currently, the following stylish themes are available:

* [nLab Stylish theme](http://userstyles.org/styles/17934) by [[Bruce Bartlett]].  This nLab theme changes the fonts on the nLab to a serif-style, and makes the edit box much bigger for an overall more pleasant experience!
* [nLab -- nCafe style](http://userstyles.org/styles/22800) by [[Daniel Schäppi]].  This is based on Bruce Bartlett's theme but changes the overall colour scheme somewhat to something a little more like the n-Cafe.

### How to download a local copy of the nLab 
  {#download}
 
It is possible to download an SQL dump of the nLab database, from which both the nLab and nForum can be reconstructed. Some of us are running cron jobs to do this regularly. The more the merrier: if you are interested, please request that we create a user for you to be able to do this in the [nForum](https://nforum.ncatlab.org/discussions/?CategoryID=21), say in [this thread](https://nforum.ncatlab.org/discussion/8991/nlab-database-backups/?Focus=71715#Comment_71715).

If you would like instead to download rendered nLab pages for local viewing, let us know as well at the nForum.

category: meta