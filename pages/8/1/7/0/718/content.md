<div style="float:left;margin:0 10px 10px 0;"><img src="http://www.j-paine.org/ish_bin_da_thumb.jpg" alt="Photo of Jocelyn Paine" /></div>

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Contents### {: .clickToReveal}
###Contents### {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include contents]]
=--
=--
=--

I am a <a href="http://www.j-paine.org/#consultancy">freelance programmer</a>, and spend too much time repairing Web servers and spreadsheets &mdash; or, in these hard times, looking for Web servers and spreadsheets to repair. <a href="http://www.j-paine.org/">My Website</a> says more about this and other things I do.

But I was tempted into category theory, not least by my friends Hendrik Hilberdink, <a href="http://www.imar.ro/~diacon/">R&#259;zvan Diaconescu</a>, Petros Stefaneas, and <a href="http://www.di.uminho.pt/~jbb/">Jos&#233; Bernardo Barros</a>. And their supervisor, <a href="http://www-cse.ucsd.edu/~goguen/">Joseph Goguen</a>.

Using experience gained from writing <a href="http://www.j-paine.org/#economics_and_distance_learning">Web-based simulations of the economy</a>, I have implemented some Web-based category theory demonstrations. Their main input page is <a href="http://www.j-paine.org/cgi-bin/webcats/webcats.php">here</a>; and there is <a href="http://www.j-paine.org/cgi-bin/webcats/set_prod_nlab.php">one more </a> that I've adapted to use the same notation as the nLab <a href="http://ncatlab.org/nlab/show/product">product</a> page. If I could get funding, I'd like to make these easier for novices to learn from. A week or two ago, <a href="http://www.comlab.ox.ac.uk/people/Jamie.Vicary/">Jamie Vicary</a> offered to host them on the Oxford Computing Lab's servers: a good next step would be to tidy up and document the whole system, then make the source publicly available.

I'd also like to popularise category theory through my <a href="http://www.j-paine.org/dobbs/index.html">blog at Dr Dobbs</a>. That's partly because I find it intrinsically fascinating; but also because I feel it has huge potential in Artificial Intelligence and cognitive science. I've written about that <a href="http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c018171">in an n-Category Caf&eacute; posting</a>. Places where I think category theory could benefit AI and cognitive science include <a href="http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c018173" title="Section on neural networks from the above posting">neural networks and their relation to logic and model theory</a>, <a href="http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c018180" title="Section on analogical reasoning from the above posting">analogical reasoning</a>, and <a href="http://golem.ph.utexas.edu/category/2006/11/a_categorical_manifesto.html#c018555" title="Comment on holographic reduced representations from the above posting">holographic reduced representations</a>.

One benefit is the tools category theory gives us to "achieve independence from the often overwhelmingly complex details of how things are represented or implemented". (I quote Goguen's <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.13.362"><cite>A categorical manifesto</cite></a>.) For example, holographic reduced representations represent symbolic structured data as high-dimensional vectors, storing and extracting items via operations similar to correlation and convolution. They can use the same operations to do analogical reasoning of the kind "What is to Sweden as Paris is to France?". This is important because any intelligent machine needs to do such reasoning; but it's something computers are notoriously bad at. If we could characterise HRRs categorically, it might help us discover which properties of their representational substrate are essential, and which merely accidental.

Perhaps &mdash; I don't know whether I'm joking or not &mdash; categorical characterisations could help us understand other phenomena. Could we find a universal property that a computational system satisfies if and only if it is conscious?! 

Or &mdash; a simpler question, and one that must be sensible &mdash; that it satisfies if and only if it can represent and reason about itself? The latter would be an interesting project in dynamical systems; but perhaps it's assuming too much to regard the reasoner as a dynamical system.

Category theory also gives us tools for unifying disparate mathematical and computational phenomena. AI and cognitive science, of course, are full of disparate mathematical and computational phenomena, usually ones whose relatedness is badly understood. That is why my n-Category Caf&eacute; posting above mentioned neural networks: in it, I cited Michael Healy's paper <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.32.2635"><cite> Category Theory Applied to Neural Modeling and Graphical Representations</cite></a>. He uses colimits, functors, and natural transformations to map concepts expressed as logic onto concepts represented in one kind of neural network.

As another example, I cited a paper by Goguen on analogical reasoning via "conceptual blending": <a href="http://citeseerx.ist.psu.edu/viewdoc/summary;jsessionid=E7800C5B8537F1A3E2AD33585E735831?doi=10.1.1.75.2277"><cite>Mathematical Models of
Cognitive Space and Time</cite></a>. He uses institutions and 3/2-colimits to (for example) represent the meaning of the word "houseboat" as an optimal blend of the meanings of "house" and "boat". Could we apply the same constructions to HRRs? That would unify two kinds of analogical reasoning implemented on very different representational substrates.
 
Read the following quote from
<a href="http://gregegan.customer.netspace.net.au/">Greg Egan</a>'s novel <a href="http://gregegan.customer.netspace.net.au/INCANDESCENCE/Incandescence.html"><cite>Incandescence</cite></a>. That's how I want category theory to unify cognitive science and AI:
<blockquote>
'Interesting Truths' referred to a kind of theorem which captured subtle unifying insights between broad classes of mathematical structures. In between strict isomorphism &#8212; where the same structure recurred exactly in different guises &#8212; and the loosest of poetic analogies, Interesting Truths gathered together a panoply of apparently disparate systems by showing them all to be reflections of each other, albeit in a suitably warped mirror. Knowing, for example, that multiplying two positive integers was really the same as adding their logarithms revealed an exact correspondence between two algebraic systems that was useful, but not very deep. Seeing how a more sophisticated version of the same could be established for a vast array of more complex systems &#8212; from rotations in space to the symmetries of subatomic particles &#8212; unified great tracts of physics and mathematics, without collapsing them all into mere copies of a single example.
</blockquote>

Incidentally, category theory also inspired me to invent a way of <a href="http://www.j-paine.org/#safe_spreadsheets_fast_with_excelsior">building spreadsheets from modules</a>, and of <a href="http://www.spreadsheet-parts.org/">storing these modules on the Web</a> for anyone to download into their own spreadsheets.

+--{: .query}
Note the Markdown method for block-level code (which cannot produce a blank line at the beginning or end of the block), now also at the [[Sandbox]].  ---[[Toby Bartels]]
=--

category: people