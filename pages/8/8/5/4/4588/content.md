
# TITLE #
* the following line creates the automatic table of contents
{:toc}

## Ugly display of "pre" blocks ##

(I had to take wraping pre in <code>&lt;code;></code> to get title acceptible)

Display of <code>&lt;pre></code> is rather ugly with all the extra white space. It really needs some CSS styling.

(LETS SEE If I can directly put in a <code>&lt;style></code> block and change it)

<style>pre { white-space: pre-wrap; border-left-width-value: 6px;  border-left-style-value: solid; border-left-color-value: rgb(200, 200, 170); padding-top: 8px; padding-right-value: 8px; padding-bottom: 8px; padding-left-value: 16px; background-color: rgb(235, 236, 255); margin-top: 1em; margin-right-value: 0pt; margin-bottom: 1em; margin-left-value: 0pt;}</style>

(ANY BETTER?)

<pre>o = {a: 1,
     b: 2
    }</pre>

The <a href="http://golem.ph.utexas.edu/wiki/instiki/show/Syntax#SyntaxColouring">Javascript syntax coloring</a> is the same but only colored. (I recall that I had to put in a "The" at the start of this pgh so I wouldn't get a parse error.)

~~~~~~~~~~ {: lang=javascript}
o = {a: 1,
     b: 2
    }
~~~~~~~~~~~~~~~~~~~~~~~~

## Working Ampersand Escaping ##

Example showing correct ampersand escaping in ID attribute, td as textnode, td containg XML. Note that spaces are INCORRECTLY stripped from around QUOT APOS and the <code>code</code> item.

<table class='DBE' markdown='1'
 id='{"id":"NEW","type":"category","page":"[[Rod McGuire]]","!AsXML":{"junkX":"1"},"junk":"a &apos; b \" c &lt; d > e &amp; f","junkX":"a &apos; b \" c &lt;code>XxX&lt;/code> d &amp; e"}'>
<!-- 2c --><tr><td>id</td><td></td><td>NEW</td></tr><tr><td>type</td><td></td><td>category</td></tr><tr><td>page</td><td></td><td>[[Rod McGuire]]</td></tr><tr><td>!AsXML</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>junkX</td><td></td><td>1</td></tr></table></td></tr><tr><td>junk</td><td></td><td>a ' b " c &lt; d > e &amp; f</td></tr><tr><td>junkX</td><td></td><td>a ' b " c <code>XxX</code> d &amp; e</td></tr></table>
<span class='DBE'/>

## Captions in Tables ##

Giving table captions example. A caption property can be plain text (!Caption) where the characters "<" and ">" can appear but wind up being escaped, or XML (!XMLCaption) where those brackets if they appear are assumed to delimit XHTML entities such as <code>&lt;code></code>. 

<pre>{"!Caption": "top caption",
 id: "test1",
 a: "x",
 b: {c: {d: "y", e: "z", "!XMLCaption": "internal <code>XML</code> caption"},
     f: "w"},
 }

{"!Caption":"top caption","id":"test1","a":"x","b":{"c":{"d":"y","e":"z","!XMLCaption":"internal &lt;code>XML&lt;/code> caption"},"f":"w"}}
</pre>

(THE jso shown above may not have been correctly updated to reflect this example that works)

<table class='DBE' markdown='1'
 id='{"!Caption":"top caption","id":"test1","a":"x","b":{"c":{"d":"y","e":"z","!XMLCaption":"internal &lt;code>XML&lt;/code> caption"},"f":"w"}}'><caption>top caption</caption>
<!-- 2c --><tr><td>!Caption</td><td></td><td>top caption</td></tr><tr><td>id</td><td></td><td>test1</td></tr><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>c</td><td></td><td><table markdown="1"><caption>internal <code>XML</code> caption</caption>
<!-- 2c --><tr><td>d</td><td></td><td>y</td></tr><tr><td>e</td><td></td><td>z</td></tr><tr><td>!XMLCaption</td><td></td><td>internal &lt;code>XML&lt;/code> caption</td></tr></table></td></tr><tr><td>f</td><td></td><td>w</td></tr></table></td></tr></table>
<span class='DBE'/>

## 2 column vs. 1 column ##
3) 2 column vs 1 column-with-header display examples.

### 2 column ###

<pre>{a: "x",
 b: {c:         {d: "y", e: "z"},
     f:         "w"},
 }

{"a":"x","b":{"c":{"d":"y","e":"z"},"f":"w"}}</pre>

<table class='DBE' markdown='1'
 id='{"a":"x","b":{"c":{"d":"y","e":"z"},"f":"w"}}'>
<!-- 2c --><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>c</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>d</td><td></td><td>y</td></tr><tr><td>e</td><td></td><td>z</td></tr></table></td></tr><tr><td>f</td><td></td><td>w</td></tr></table></td></tr></table>
<span class='DBE'/>

### Some internal 1 columns ###
Example with some internal objects displayed in 1 column-with-header (full display)

<pre>{a: "x",
 b: {"!Columns": 1, 
     c:         {"!Columns": 1, d: "y", e: "z"},
     f:         "w"},
 }

{"a":"x","b":{"!Columns":1,"c":{"!Columns":1,"d":"y","e":"z"},"f":"w"}}

</pre>

<table class='DBE' markdown='1'
 id='{"a":"x","b":{"!Columns":1,"c":{"!Columns":1,"d":"y","e":"z"},"f":"w"}}'>
<!-- 2c --><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>!Columns</th></tr><tr><td></td><td>1</td></tr></table></td></tr><tr><td><table><tr><th>c</th></tr><tr><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>!Columns</th></tr><tr><td></td><td>1</td></tr></table></td></tr><tr><td><table><tr><th>d</th></tr><tr><td></td><td>y</td></tr></table></td></tr><tr><td><table><tr><th>e</th></tr><tr><td></td><td>z</td></tr></table></td></tr></table></td></tr></table></td></tr><tr><td><table><tr><th>f</th></tr><tr><td></td><td>w</td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>

### 1 column with !NoBang ###
3c) 1 column-with-header with top level <code>!NoBang: 1</code> that suppresses property names that start with bang (!).

<pre>{"!NoBang": 1,
a: "x",
 b: {"!Columns": 1, 
     c:         {"!Columns": 1, d: "y", e: "z"},
     f:         "w"},
 }

{"!NoBang":1,"a":"x","b":{"!Columns":1,"c":{"!Columns":1,"d":"y","e":"z"},"f":"w"}}

</pre>

<table class='DBE' markdown='1'
 id='{"!NoBang":1,"a":"x","b":{"!Columns":1,"c":{"!Columns":1,"d":"y","e":"z"},"f":"w"}}'>
<!-- 2c --><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>c</th></tr><tr><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>d</th></tr><tr><td></td><td>y</td></tr></table></td></tr><tr><td><table><tr><th>e</th></tr><tr><td></td><td>z</td></tr></table></td></tr></table></td></tr></table></td></tr><tr><td><table><tr><th>f</th></tr><tr><td></td><td>w</td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>


## !Label examples with sometimes !Atom wrappers ##

### !Label 2 column ###

<pre>{"a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}</pre>

<table class='DBE' markdown='1'
 id='{"a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}'>
<!-- 2c --><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td>pp</td><td><table markdown="1">
<!-- 2c --><tr><td>!Label</td><td></td><td>pp</td></tr><tr><td>c</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>d</td><td></td><td>y</td></tr><tr><td>e</td><td>qq</td><td><table markdown="1">
<!-- 2c --><tr><td>!Atom</td><td></td><td>z</td></tr><tr><td>!Label</td><td></td><td>qq</td></tr></table></td></tr><tr><td>f</td><td></td><td>w</td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>

### !Label 2 column !NoBang ###
<pre>{"!NoBang":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}</pre>

<table class='DBE' markdown='1'
 id='{"!NoBang":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}'>
<!-- 2c --><tr><td>a</td><td></td><td>x</td></tr><tr><td>b</td><td>pp</td><td><table markdown="1">
<!-- 2c --><tr><td>c</td><td></td><td><table markdown="1">
<!-- 2c --><tr><td>d</td><td></td><td>y</td></tr><tr><td>e</td><td>qq</td><td>z</td></tr><tr><td>f</td><td></td><td>w</td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>

### !Label 1 column ###
<pre>{"!Columns":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}</pre>

<table class='DBE' markdown='1'
 id='{"!Columns":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}'>
<!-- 1c --><tr><td><table><tr><th>!Columns</th></tr><tr><td></td><td>1</td></tr></table></td></tr><tr><td><table><tr><th>a</th></tr><tr><td></td><td>x</td></tr></table></td></tr><tr><td><table><tr><th>b</th></tr><tr><td>pp</td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>!Label</th></tr><tr><td></td><td>pp</td></tr></table></td></tr><tr><td><table><tr><th>c</th></tr><tr><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>d</th></tr><tr><td></td><td>y</td></tr></table></td></tr><tr><td><table><tr><th>e</th></tr><tr><td>qq</td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>!Atom</th></tr><tr><td></td><td>z</td></tr></table></td></tr><tr><td><table><tr><th>!Label</th></tr><tr><td></td><td>qq</td></tr></table></td></tr></table></td></tr></table></td></tr><tr><td><table><tr><th>f</th></tr><tr><td></td><td>w</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>

### !Label 1 column !NoBang ###
<pre>{"!Columns":"1","!NoBang":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}</pre>

<table class='DBE' markdown='1'
 id='{"!Columns":"1","!NoBang":"1","a":"x","b":{"!Label":"pp","c":{"d":"y","e":{"!Atom":"z", "!Label":"qq"},"f":"w"}}}'>
<!-- 1c --><tr><td><table><tr><th>a</th></tr><tr><td></td><td>x</td></tr></table></td></tr><tr><td><table><tr><th>b</th></tr><tr><td>pp</td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>c</th></tr><tr><td></td><td><table markdown="1">
<!-- 1c --><tr><td><table><tr><th>d</th></tr><tr><td></td><td>y</td></tr></table></td></tr><tr><td><table><tr><th>e</th></tr><tr><td>qq</td><td>z</td></tr></table></td></tr><tr><td><table><tr><th>f</th></tr><tr><td></td><td>w</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table>
<span class='DBE'/>

## Array example ##

It looks here that JSON.stringify and JSON.parse really don't know how to handle arrays.

<pre>
x = {a: [['b', 'c'], ['d', 'e']]};

x.a[0];
=> b,c

s = JSON.stringify(x)
=>  {"a":"[[\"b\", \"c\"], [\"d\", \"e\"]]"}

os = JSON.parse(s)
=> [object Object]

uneval(os)
=> ({a:"[[\"b\", \"c\"], [\"d\", \"e\"]]"})

os.a[0]
=> [
</pre>

<table class='DBE' markdown='1'
 id='{"a":[[\"b\", \"c\"], [\"d\", \"e\"]]"}'>
<!-- 2c --><tr><td>a</td><td></td><td>[["b", "c"], ["d", "e"]]</td></tr></table>
<span class='DBE'/>

### hand fed example to show the GM script is working ###

<pre>
x = {a: [['b', 'c'], ['d', 'e']]};

genEntry(x) =>
</pre>

<table markdown="1"> <!-- 2c --><tr><td>a</td><td></td><td><table markdown="1"> <!-- 2c --><tr><td>0</td><td></td><td><table markdown="1"> <!-- 2c --><tr><td>0</td><td></td><td>b</td></tr><tr><td>1</td><td></td><td>c</td></tr></table></td></tr><tr><td>1</td><td></td><td><table markdown="1"> <!-- 2c --><tr><td>0</td><td></td><td>d</td></tr><tr><td>1</td><td></td><td>e</td></tr></table></td></tr></table></td></tr></table>

## Types with Recursive Structure ##

### type "pair" in full ###
Define "pair".

<pre>
p = {Type:      {"!Atom": "pair < structure",
                 "!Label": "t"}, 
     "!Label":  "pair",
     part:     {1: {"!Label": "p1",
                    Type:     "< structure"},
                2: {"!Label": "p2",
                    Type:     "< structure"},
                },
     swapped:  {Type: {},
                part: {},
                swapped: {},
               },
     Notes:   "See [[ordered pair]].",
     };

p.swapped.Type = p.Type;
p.swapped.part[1] = p.part[2];
p.swapped.part[2] = p.part[1];
p.swapped.swapped = p;

pn = eval(uneval(p)); // clone it
pn['!NoBang'] = 1;
</pre>

Generated ID for pn:

<pre>
rEsc(pn) =>

#4={Type:#1={&apos;!Atom&apos;:"pair &lt; structure", &apos;!Label&apos;:"t"}, &apos;!NoBang&apos;:1, &apos;!Label&apos;:"pair", part:{1:#3={&apos;!Label&apos;:"p1", Type:"&lt; structure"}, 2:#2={&apos;!Label&apos;:"p2", Type:"&lt; structure"}}, swapped:{Type:#1#, part:{1:#2#, 2:#3#}, swapped:#4#}, Notes:"See [[ordered pair]]."}

</pre>

Generated table for p:

<table class='DBRE' markdown='1' id='#4={Type:#1={&apos;!Atom&apos;:"pair &lt; structure", &apos;!Label&apos;:"t", &apos;!Seen&apos;:1}, &apos;!NoBang&apos;:0, &apos;!Label&apos;:"pair", part:{1:#3={&apos;!Label&apos;:"p1", Type:"&lt; structure", &apos;!Seen&apos;:1}, 2:#2={&apos;!Label&apos;:"p2", Type:"&lt; structure", &apos;!Seen&apos;:1}, &apos;!Seen&apos;:1}, swapped:{Type:#1#, part:{1:#2#, 2:#3#, &apos;!Seen&apos;:1}, swapped:#4#, &apos;!Seen&apos;:1}, Notes:"See [[ordered pair]].", &apos;!Seen&apos;:1}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">!Atom</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Label</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">t</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!NoBang</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">0</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Label</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">pair</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">!Label</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">p1</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">!Label</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">p2</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Notes</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">See [[ordered pair]].</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">!Seen</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">1</td></tr></table></td></tr></table></td></tr></table></table> 

Generated table for pn:

<table class='DBRE' markdown='1' id='#4={Type:#1={&apos;!Atom&apos;:"pair &lt; structure", &apos;!Label&apos;:"t"}, &apos;!NoBang&apos;:1, &apos;!Label&apos;:"pair", part:{1:#3={&apos;!Label&apos;:"p1", Type:"&lt; structure"}, 2:#2={&apos;!Label&apos;:"p2", Type:"&lt; structure"}}, swapped:{Type:#1#, part:{1:#2#, 2:#3#}, swapped:#4#}, Notes:"See [[ordered pair]]."}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Notes</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">See [[ordered pair]].</td></tr></table></td></tr></table></td></tr></table></table><span class='DBE'/>

### Various types ###

### "pair" ###

A pair has two parts. The map "swapped" (aka. "transpose") switches the parts, and $swapped(swapped(p)) = p$. 

<table class='DBRE' markdown='1' id='#4={Type:#1={&apos;!Atom&apos;:"pair &lt; structure", &apos;!Label&apos;:"t"}, &apos;!NoBang&apos;:1, &apos;!Label&apos;:"pair", part:{1:#3={&apos;!Label&apos;:"p1", Type:"&lt; structure"}, 2:#2={&apos;!Label&apos;:"p2", Type:"&lt; structure"}}, swapped:{Type:#1#, part:{1:#2#, 2:#3#}, swapped:#4#}, Notes:"See [[ordered pair]]."}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p2</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Notes</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">See [[ordered pair]].</td></tr></table></td></tr></table></td></tr></table></table> 

### "twin", a subtype of "pair" ###

A twin is a pair in which both components are the same.

<pre>
t = eval(uneval(p)) // clone "pair"
t.Type['!Atom'] = "twin < pair < structure";
t.part[2] = t.part[1];
t.swapped = t;
</pre>

Essentially $twin = pair \wedge (?p1 = ?p2)$, though this formulation doesn't notice that "swapped" is now an identity.

<table class='DBRE' markdown='1' id='#2={Type:{&apos;!Atom&apos;:"twin &lt; pair &lt; structure", &apos;!Label&apos;:"t", &apos;!Seen&apos;:1}, &apos;!NoBang&apos;:1, &apos;!Label&apos;:"pair", part:{1:#1={&apos;!Label&apos;:"p1", Type:"&lt; structure", &apos;!Seen&apos;:1}, 2:#1#, &apos;!Seen&apos;:1}, swapped:#2#, Notes:"See [[ordered pair]].", &apos;!Seen&apos;:1}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?t</td><td class="T0r0d1">twin &lt; pair &lt; structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; structure</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p1</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?pair</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Notes</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">See [[ordered pair]].</td></tr></table></td></tr></table></td></tr></table></table> 

### any "structure" can be twinned ###

A small definition of this is:

<table class='DBRE' markdown='1' id='#1={Type:"structure", &apos;!NoBang&apos;:1, &apos;!Label&apos;:"s", twinned:{Type:"&lt; twin", &apos;!Label&apos;:"tw", part:{1:#1#}}}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">twinned</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?tw</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; twin</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></table> 

Then with type inference from "twin", essentially $s.twinned = s.twinned \wedge twin$, this becomes:

<pre>
s1 = eval(uneval(s0)); // clone
s1.twinned.part[2] = s1.twinned.part[1];
s1.twinned.swapped = s1.twinned;
</pre>

as

<table class='DBRE' markdown='1' id='#1={Type:"structure", &apos;!NoBang&apos;:1, &apos;!Label&apos;:"s", twinned:#2={Type:"&lt; twin", &apos;!Label&apos;:"tw", part:{1:#1#, &apos;!Seen&apos;:1, 2:#1#}, &apos;!Seen&apos;:1, swapped:#2#}, &apos;!Seen&apos;:1}'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">structure</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">twinned</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?tw</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; twin</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">swapped</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?tw</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></table>

### cartesian product as a type ###

#### take 1 ####

<pre>
c1.from.part[1].generic_member.in = c1.from.part[1]; c1.from.part[2].generic_member.in = c1.from.part[2]; c1.to.generic_member.in = c1.to; c1.to.generic_member.part[1] = c1.from.part[1].generic_member; c1.to.generic_member.part[2] = c1.from.part[2].generic_member; c1.projection[1].from = c1.to; c1.projection[1].to = c1.from.part[1]; c1.projection[2].from = c1.to; c1.projection[2].to = c1.from.part[2]; 
</pre>

<table class='DBRE' markdown='1' id='({Type:"cartesian product &lt; isomorphism &lt; arrow", &apos;!NoBang&apos;:1, from:{Type:"&lt; pair", part:{1:#1={Type:"&lt; set", &apos;!Label&apos;:"s1", generic_member:#4={&apos;!Label&apos;:"m1", quant:"any", in:#1#}}, 2:#2={Type:"&lt; set", &apos;!Label&apos;:"s2", generic_member:#5={&apos;!Label&apos;:"m2", quant:"any", in:#2#}}}}, to:#3={Type:"&lt; set", &apos;!Label&apos;:"p", generic_member:{Type:"&lt; pair", quant:"any", in:#3#, part:{1:#4#, 2:#5#}}}, projection:{1:{from:#3#, to:#1#}, 2:{from:#3#, to:#2#}}, Notes:"See [[cartesian product]]."})'><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">cartesian product &lt; isomorphism &lt; arrow</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">from</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; pair</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; set</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">generic_member</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?m1</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">quant</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">any</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">in</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s1</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s2</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; set</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">generic_member</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?m2</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">quant</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">any</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">in</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s2</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">to</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p</td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; set</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">generic_member</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">Type</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">&lt; pair</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">quant</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">any</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">in</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">part</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?m1</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?m2</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">projection</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">1</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">from</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">to</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s1</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">2</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1"><table markdown='1' class='TT1' border='0'><tr class="T1rN"><td class="T1rNd0">from</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?p</td><td class="T0r0d1">...</td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">to</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0">?s2</td><td class="T0r0d1">...</td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr></table></td></tr><tr class="T1rN"><td class="T1rNd0">Notes</td><td class="T1rNd1"><table class='TT0' markdown='1' border='1'><tr class="T0r0"><td class="T0r0d0"></td><td class="T0r0d1">See [[cartesian product]].</td></tr></table></td></tr></table></td></tr></table></table> 

The END.


category: people

[[!redirects Rod Mc Guire]]
[[!redirects Rod McGuire]]
[[!redirects RodMcGuire]]
