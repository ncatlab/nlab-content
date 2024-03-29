
# An Initial SVG editor HowTo

1. Before creating an SVG using the editor, you need to choose where it will be placed in a page.  So first you need to be editing a page, then click in the source text where you want your SVG to appear.  The SVG editor will now launch.

3. To insert some mathematics, you need to use the "foreign object" tool.  The icon for this is a $\Phi$ (currently bottom on the menu at the left-hand side).  Click on this and then click where you want the mathematics to be.  The menu across the top will now change to the "foreign object" menu.  The icon with a pencil and some MathML code in the background brings up an editor for the content of this "foreign object".  At the moment, this has to be put in as true MathML.  There are several ways to generate this, the simplest being to install `itex2MML` on your computer and use that to parse itex.  A slightly more complicated route would be to use the [[Sandbox]] and write in the itex, send it off to the nLab for processing, then use the "View Source" option on your browser. But, most likely, the symbols you need already appear on the page you are editing. So just "View Source", and grab the snippet of MathML that you need.  You may have to adjust the size of the "foreign object" to be able to see all of your amazing mathematics.  Either drag the appropriate side of the blue box or manually adjust the numbers in the "foreign object" menu across the top. (In some browsers, the blue box is, confusingly, not anywhere near where the text actually is; that's a bug in your browser, and you may be able to fix it by updating to the latest version.) It's important to make sure that the boxes are big enough, text outside a box doesn't get shown.  Leave a little room around as things may be seen differently on different browsers.

4. The tool which you are using defaults to "select" so if you want to lay out the diagram roughly first and then go back and edit each piece, you have to keep selecting the corresponding tool each time.  Sometimes.

5. You put arrows on afterwards.  So draw the lines first, then select them and put arrows on as desired.

6. There are a couple of ways of making curved arrows.  One is to draw a straight line and convert it to a path.  So draw a straight line, select it, and click the button at the top that is a red quarter-circle with some blue bits.  That converts it to a path.  Ensure that it is selected and click it again (it can take a couple of clicks to get this right: the line should go cyan).  Now change the menu "Straight" to "Curve".  You can adjust the curviness by dragging the control points around.

7. Just because you've put a path in doesn't mean it will get shown.  Paths need to be "stroked" to be visible (or they can be filled).  If your paths aren't visible, make sure that the "stroke" settings (bottom of the screen) are something sensible.  Click "wireframe mode" (the "circle-square" icon at the top) if you think you've drawn something that you can't see.


category: meta
