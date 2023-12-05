# css-advanced-selectors

Common Selectors Overview ->
h1	Type Selector	Selects an element by its type
.tagline	Class Selector	Selects an element by the class attribute value, which may be reused multiple times per page
#intro	ID Selector	Selects an element by the ID attribute value, which is unique and to only be used once per page

Child Selectors ->

<h2>...</h2>
<article>
  <h2>This heading will be selected</h2>
  <div>
    <h2>This heading will be selected</h2>
  </div>
</article>

article h2 {...}

Direct Child Selector ->

<p>...</p>
<article>
  <p>This paragraph will be selected</p>
  <div>
    <p>...</p>
  </div>
</article>

article > p {...}

Sibling Selectors ->

<p>...</p>
<section>
  <p>...</p>
  <h2>...</h2>
  <p>This paragraph will be selected</p>
  <div>
    <p>...</p>
  </div>
  <p>This paragraph will be selected</p>
</section>

h2 ~ p {...}

Adjacent Sibling Selector ->

<p>...</p>
<section>
  <p>...</p>
  <h2>...</h2>
  <p>This paragraph will be selected</p>
  <div>
    <p>...</p>
  </div>
  <p>...</p>
</section>

h2 + p {...}

Attribute Present Selector ->

<a href="#" target="_blank">...</a>

a[target] {...}

Attribute Equals Selector ->

<a href="http://google.com/">...</a>

a[href="http://google.com/"] {...}

Pseudo-classes ->

a:link {...}
a:visited {...}

User Action Pseudo-classes ->

a:hover {...}
a:active {...}
a:focus {...}

User Interface State Pseudo-classes ->

input:enabled {...}
input:disabled {...}

:first-child, :last-child, & :only-child ->

<ul>
  <li>This list item will be selected</li>
  <li>
    <div>This div will be selected</div>
  </li>
  <li>
    <div>...</div>
    <div>...</div>
  </li>
  <li>This list item will be selected</li>
</ul>

li:first-child {...}
li:last-child {...}
div:only-child {...}

:nth-child(n) & :nth-last-child(n) ->

<ul>
  <li>...</li>
  <li>...</li>
  <li>This list item will be selected</li>
  <li>...</li>
  <li>...</li>
  <li>This list item will be selected</li>
</ul>

li:nth-child(3n) {...}

