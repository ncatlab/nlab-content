
# TITLE #
* the following line creates the automatic table of contents
{:toc}

## Ugly display of "pre" blocks ##

(I had to take wraping pre in <code>&lt;code;></code> to get title acceptible)

Display of <code>&lt;pre></code> is rather ugly with all the extra white space. It really needs some CSS styling.

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





The END.

category: people

