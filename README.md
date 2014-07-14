dna.js Template Cloner
======================
DOM Templating Engine for jQuery
--------------------------------

dna.js is the world's easiest to use DOM templating engine.

Current release: **v0.2.0**

### 1. Bookstore Example
Designate DNA templates with the `dna-template` class, and put the templates directly into the HTML of your web page.&nbsp;  Use the element's `id` to indicate the name of the template.&nbsp;  Enclose data fields in double tildes `~~` (a.k.a. DNA strands).

#### a) HTML for book template
    <h1>Featured Books</h1>
    <div id=book class=dna-template>
       <div>Title:  <span>~~title~~</span></div>
       <div>Author: <span>~~author~~</span></div>
    </div>

Then call the `dna.clone()` function to insert a copy of the template into the DOM.&nbsp;  The supplied JSON data object will be used to populate the fields of the template.

#### b) JavaScript call to add book node
    dna.clone('book', { title: 'The DOM', author: 'Jan' });

The new element is a DNA clone, and it is appended to the template's parent element (the original template is detached from the DOM and kept for additional cloning).

#### c) Resulting HTML with DNA clone
    <h1>Featured Books</h1>
    <div class=book>
       <div>Title:  <span>The DOM</span></div>
       <div>Author: <span>Jan</span></div>
    </div>

Clones can alternatively be generated by providing a URL to a REST resource.

#### d) JavaScript call to load data from a REST call
    dna.load('book', 'http://dnajs.org/rest/book/3');

### 2. Additional Information
* [dnajs.org](http://dnajs.org) &mdash; (see the "Try It Out" section for a live example)
* [Documentation](http://dnajs.org/manual.html)
* [Release Notes](https://github.com/dnajs/dna.js/wiki/Release-Notes)
