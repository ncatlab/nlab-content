### What this page is for ###

This Sandbox is specifically for mucking about with SVGs.  The point is that these pictures can get rather large (particularly if automatically generated - does anyone write their own?).  A Sandbox, such as [[Sandbox|this one]] is for trying things out.  Usually those are little things, such as getting the correct syntax for something, so if the Sandbox gets really big and takes ages to load and resubmit, it gets difficult to try out lots of little changes.  One SVG, such as my original one, can easily swamp the 'box.  However, as I've found out, getting SVGs to work in Instiki can take a little tweaking so this 'box is for that.

One shouldn't leave an SVG here for long.  I don't think that there's much to be learnt from looking through someone else's SVG code (unlike in the original [[Sandbox]] where it can be useful to scan through and see how something is done).  Rather, you should muck about with your SVG, get it right, and then transfer it across to the requisite page.

A reasonable rule would be that the author should delete it when they are finished with it, and that the maximum lifespan of a picture here is, say, 1 week.  To make this easier to police, please timestamp your SVGs.

Obviously as we play with these then we'll learn various strategies.  These should be added to the [[FAQ]] or [[HowTo]] pages as appropriate.  Maybe we should have a list of SVGs in the n-Lab so that people can find examples of what can be done and how to do it, this could be commented with what has had to be done to get it to work in Instiki.  If someone has a particularly nice example, or one they're particularly proud of, but doesn't really fit into an "honest" page on the n-Lab then may I suggest they put it on their userpage (I'll probably do that with the "map of manifolds" one since it doesn't really fit anywhere else).


##### Original import from the [[Sandbox]] #####

Testing tikzpicture to svg capability.

###### Timestamp: 2009-05-08 ######

(removed; see [revision 10](http://ncatlab.org/nlab/revision/SVG+Sandbox/10))

Not bad!  Thanks to Jacques, the sphere is fine now.  This picture is probably a little too big to leave in the sandbox so I'll remove it soon - just want to show off a little first!  For the original, see [Comparative Smootheology at Ottawa](http://www.math.ntnu.no/~stacey/Seminars/ottawa.html).


+-- {: .query}
Been a while since I thought about getting a good graphics engine here in inStiki, but these pictures have got me excited again. Right now I am thinking that the following procedure could work well:

* You draw a picture using your favourite method (TikZ, Inkscape, etc.)

* You export it as an svg file.

* You copy and paste this svg text into the nLab page you are editing.

* Now you click "Submit" as usual. 

* Here's the trick: the next time someone clicks "Edit page" in the nLab, the Instiki software is intelligent and displays the SVG text as a javascript "expand box". In other words, there's a little command in the text "Expand SVG code (+)" and if you click the (+), it expands all the code out. If you click "(-)", the code collapses again. This way we don't get large swathes of SVG code cluttering up the text area.

* Perhaps the software can be more advanced and remember if someone has altered any of the SVG segments of code. If not, it shouldn't be resubmitted when someone clicks "Submit",  otherwise it will make for slow uploads.

[[Bruce Bartlett]]

One method that would solve a lot of that would be to have the SVGs as external files that are then included at the appropriate point.  I don't know whether or not that is possible, though.

Another thing is that exported files can often contain a lot of "junk" (cafeful examination of my picture will reveal that it uses 5 decimal places; perhaps slightly over-accurate).  Some way of automatically trimming this down would be helpful.

I think it's okay to add another step into your scheme, between the export and copying into Instiki, but it needs to be an easy one, say a script that modifies things a little to be acceptable to Instiki.  However, what that needs to do will only become apparent with a little experimentation.

[[Andrew Stacey]]

Well, you can certainly upload files here in Instiki, and I think that method would be possible. But then we're back to the Fundamental Conundrum: 

_If we're going to start including files, you might as well export your graphic as a png file and include it the old-fashioned way._

It's the old problem: SVG and MathML have not been built so that one can use them both simultaneously (I think).

[[Bruce Bartlett]]


=--

Doing a quick LaTeX -> Inkscape -> SVG -> nLab test [[Bruce Bartlett]]: 

###### Timestamp: 2009-05-08 ######

(removed; see [revision 10](http://ncatlab.org/nlab/revision/SVG+Sandbox/10))

As you can see, the trouble with this method is that Inkscape is exporting the text as spline primitives... which takes up way too much space. I guess that just returns to the old problem: you can't mix MathML and SVG. Now I remember (I _knew_ there was some kind of nasty problem with this MathML, SVG and Instiki thing... and now 
I remember).  [[Bruce Bartlett]]

Ok, I'm giving it another go. Now I'm trying Andrew's method --- you do a diagram:

(removed; see [revision 10](http://ncatlab.org/nlab/revision/SVG+Sandbox/10)) 


_Mike_: Here is a little diagram produced from the following TikZ code:

    \begin{tikzpicture}[auto,scale=2]
      \node (A) at (0,0) {$A^2$};
      \node (B) at (2,0) {$\int B$};
      \node (C) at (1,1) {$\sum_0^\infty C$};
      \draw[->] (A) to node[swap] {$\phi$} (B);
      \draw[->] (A) to node {$\psi$} (C);
      \draw[->] (C) to node {$\theta$} (B);
      \draw[->] (1,0.5) to node {$\mu$} (1,0.3);
    \end{tikzpicture}

run through htlatex, and with the `<tspan>`s then manually replaced by the appropriate foreignObject tags:

(removed; see [revision 10](http://ncatlab.org/nlab/revision/SVG+Sandbox/10)) 

_Bruce_ : Hey, this is great Mike! For anyone reading this thread, who wants to contribute, don't forget about the [nForum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=20&page=1#Comment_95) page where we are discussing this stuff. 

_Toby_:  Here\'s the diagram again, but *without* the SVG code in the edit box, thanks to the magic of inclusions!

[[!include Inclusion Sandbox]]

(This is included from the new [[Inclusion Sandbox]].)

_Bruce_: The files I received from Olivier Binda, which includes a nice comprehensive test suite of how his patch to htlatex (which changes ordinary text in SVG into foreignobject tags) performs, are available here: [[LD@Svg@Tests_files.zip]]

category: meta