- <!DOCTYPE html>
<html>
<head>
<title>markdown_cheat_sheet.md</title>
<meta http-equiv="Content-type" content="text/html;charset=UTF-8">

<style>
/* https://github.com/microsoft/vscode/blob/master/extensions/markdown-language-features/media/markdown.css */
/*---------------------------------------------------------------------------------------------
 *  Copyright (c) Microsoft Corporation. All rights reserved.
 *  Licensed under the MIT License. See License.txt in the project root for license information.
 *--------------------------------------------------------------------------------------------*/

body {
	font-family: var(--vscode-markdown-font-family, -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif);
	font-size: var(--vscode-markdown-font-size, 14px);
	padding: 0 26px;
	line-height: var(--vscode-markdown-line-height, 22px);
	word-wrap: break-word;
}

#code-csp-warning {
	position: fixed;
	top: 0;
	right: 0;
	color: white;
	margin: 16px;
	text-align: center;
	font-size: 12px;
	font-family: sans-serif;
	background-color:#444444;
	cursor: pointer;
	padding: 6px;
	box-shadow: 1px 1px 1px rgba(0,0,0,.25);
}

#code-csp-warning:hover {
	text-decoration: none;
	background-color:#007acc;
	box-shadow: 2px 2px 2px rgba(0,0,0,.25);
}

body.scrollBeyondLastLine {
	margin-bottom: calc(100vh - 22px);
}

body.showEditorSelection .code-line {
	position: relative;
}

body.showEditorSelection .code-active-line:before,
body.showEditorSelection .code-line:hover:before {
	content: "";
	display: block;
	position: absolute;
	top: 0;
	left: -12px;
	height: 100%;
}

body.showEditorSelection li.code-active-line:before,
body.showEditorSelection li.code-line:hover:before {
	left: -30px;
}

.vscode-light.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(0, 0, 0, 0.15);
}

.vscode-light.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(0, 0, 0, 0.40);
}

.vscode-light.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-dark.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 255, 255, 0.4);
}

.vscode-dark.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 255, 255, 0.60);
}

.vscode-dark.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-high-contrast.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 160, 0, 0.7);
}

.vscode-high-contrast.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 160, 0, 1);
}

.vscode-high-contrast.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

img {
	max-width: 100%;
	max-height: 100%;
}

a {
	text-decoration: none;
}

a:hover {
	text-decoration: underline;
}

a:focus,
input:focus,
select:focus,
textarea:focus {
	outline: 1px solid -webkit-focus-ring-color;
	outline-offset: -1px;
}

hr {
	border: 0;
	height: 2px;
	border-bottom: 2px solid;
}

h1 {
	padding-bottom: 0.3em;
	line-height: 1.2;
	border-bottom-width: 1px;
	border-bottom-style: solid;
}

h1, h2, h3 {
	font-weight: normal;
}

table {
	border-collapse: collapse;
}

table > thead > tr > th {
	text-align: left;
	border-bottom: 1px solid;
}

table > thead > tr > th,
table > thead > tr > td,
table > tbody > tr > th,
table > tbody > tr > td {
	padding: 5px 10px;
}

table > tbody > tr + tr > td {
	border-top: 1px solid;
}

blockquote {
	margin: 0 7px 0 5px;
	padding: 0 16px 0 10px;
	border-left-width: 5px;
	border-left-style: solid;
}

code {
	font-family: Menlo, Monaco, Consolas, "Droid Sans Mono", "Courier New", monospace, "Droid Sans Fallback";
	font-size: 1em;
	line-height: 1.357em;
}

body.wordWrap pre {
	white-space: pre-wrap;
}

pre:not(.hljs),
pre.hljs code > div {
	padding: 16px;
	border-radius: 3px;
	overflow: auto;
}

pre code {
	color: var(--vscode-editor-foreground);
	tab-size: 4;
}

/** Theming */

.vscode-light pre {
	background-color: rgba(220, 220, 220, 0.4);
}

.vscode-dark pre {
	background-color: rgba(10, 10, 10, 0.4);
}

.vscode-high-contrast pre {
	background-color: rgb(0, 0, 0);
}

.vscode-high-contrast h1 {
	border-color: rgb(0, 0, 0);
}

.vscode-light table > thead > tr > th {
	border-color: rgba(0, 0, 0, 0.69);
}

.vscode-dark table > thead > tr > th {
	border-color: rgba(255, 255, 255, 0.69);
}

.vscode-light h1,
.vscode-light hr,
.vscode-light table > tbody > tr + tr > td {
	border-color: rgba(0, 0, 0, 0.18);
}

.vscode-dark h1,
.vscode-dark hr,
.vscode-dark table > tbody > tr + tr > td {
	border-color: rgba(255, 255, 255, 0.18);
}

</style>

<style>
/* Tomorrow Theme */
/* http://jmblog.github.com/color-themes-for-google-code-highlightjs */
/* Original theme - https://github.com/chriskempson/tomorrow-theme */

/* Tomorrow Comment */
.hljs-comment,
.hljs-quote {
	color: #8e908c;
}

/* Tomorrow Red */
.hljs-variable,
.hljs-template-variable,
.hljs-tag,
.hljs-name,
.hljs-selector-id,
.hljs-selector-class,
.hljs-regexp,
.hljs-deletion {
	color: #c82829;
}

/* Tomorrow Orange */
.hljs-number,
.hljs-built_in,
.hljs-builtin-name,
.hljs-literal,
.hljs-type,
.hljs-params,
.hljs-meta,
.hljs-link {
	color: #f5871f;
}

/* Tomorrow Yellow */
.hljs-attribute {
	color: #eab700;
}

/* Tomorrow Green */
.hljs-string,
.hljs-symbol,
.hljs-bullet,
.hljs-addition {
	color: #718c00;
}

/* Tomorrow Blue */
.hljs-title,
.hljs-section {
	color: #4271ae;
}

/* Tomorrow Purple */
.hljs-keyword,
.hljs-selector-tag {
	color: #8959a8;
}

.hljs {
	display: block;
	overflow-x: auto;
	color: #4d4d4c;
	padding: 0.5em;
}

.hljs-emphasis {
	font-style: italic;
}

.hljs-strong {
	font-weight: bold;
}
</style>

<style>
/*
 * Markdown PDF CSS
 */

 body {
	font-family: -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif, "Meiryo";
	padding: 0 12px;
}

pre {
	background-color: #f8f8f8;
	border: 1px solid #cccccc;
	border-radius: 3px;
	overflow-x: auto;
	white-space: pre-wrap;
	overflow-wrap: break-word;
}

pre:not(.hljs) {
	padding: 23px;
	line-height: 19px;
}

blockquote {
	background: rgba(127, 127, 127, 0.1);
	border-color: rgba(0, 122, 204, 0.5);
}

.emoji {
	height: 1.4em;
}

code {
	font-size: 14px;
	line-height: 19px;
}

/* for inline code */
:not(pre):not(.hljs) > code {
	color: #C9AE75; /* Change the old color so it seems less like an error */
	font-size: inherit;
}

/* Page Break : use <div class="page"/> to insert page break
-------------------------------------------------------- */
.page {
	page-break-after: always;
}

</style>

<script src="https://unpkg.com/mermaid/dist/mermaid.min.js"></script>
</head>
<body>
  <script>
    mermaid.initialize({
      startOnLoad: true,
      theme: document.body.classList.contains('vscode-dark') || document.body.classList.contains('vscode-high-contrast')
          ? 'dark'
          : 'default'
    });
  </script>
<h1 id="1-contents">1. Contents</h1>
<p><a href="#1-headings">1-headings</a><br>
<a href="#2-block-of-words">2-Block-of-words</a><br>
<a href="#3-line-breaks">3-line-breaks</a><br>
<a href="#4-combine-two-things">4-combining-2-things</a><br>
<a href="#5-face-of-text">5-text-face</a><br>
<a href="#6-bullet-points--numbering">6-bullets</a><br>
<a href="#7-page-breaks">7-page-breaks</a><br>
<a href="#8-links-and-hyperlinks">8-links</a><br>
<a href="#9-images-and-figures-with-links">9-images/figures</a><br>
<a href="#10adding-a-code-or-code-block">10-code/codeblocks</a><br>
<a href="#11-adding-tables">11-tables</a></p>
<h1 id="2-headings">2. Headings</h1>
<h1 id="heading-1">Heading 1</h1>
<h2 id="heading-2">Heading 2</h2>
<h3 id="heading-3">Heading 3</h3>
<h4 id="heading-4">Heading 4</h4>
<h5 id="heading-5">Heading 5</h5>
<h6 id="heading-6">Heading 6</h6>
<h1 id="3-block-of-words">3. Block of words</h1>
<p>This is normal text</p>
<blockquote>
<p>this is a block of special text</p>
<p>this another line</p>
<p>it can be done by adding &quot;&gt;&quot; sign</p>
<p>to change line you press &quot;enter&quot;</p>
<p>to change line <em>and</em> be in the same block, you press &quot;&gt; in the new entered line&quot;</p>
</blockquote>
<h1 id="4-line-breaks">4. Line breaks</h1>
<p>I am wiriting a paragraph.If i want to change line or go to the next line, i can press enter, like this:
look i am on the next line</p>
<p>Now I am writing the next paragraph .Now if I want to change the line or go to the next one, i can do that by pressing a reversed slash and one enter. Now look. I am on the next line.    (check this one's error)</p>
<h1 id="5-combine-two-things">5. Combine two things</h1>
<p>Block of words + heading</p>
<blockquote>
<h3 id="heading-3">Heading 3</h3>
</blockquote>
<h1 id="6-face-of-text">6. Face of text</h1>
<h2 id="using-esteric">using esteric : *</h2>
<p><strong>Bold</strong></p>
<p><em>Italic</em></p>
<p><em><strong>Bold &amp; Italic</strong></em></p>
<h2 id="using-underscore">using underscore: _</h2>
<p><strong>Bold</strong></p>
<p><em>Italic</em></p>
<p><em><strong>Bold &amp; Italic</strong></em></p>
<h1 id="7-bullet-points--numbering">7. Bullet Points / Numbering</h1>
<blockquote>
<h3 id="bullet-points">Bullet Points :</h3>
</blockquote>
<h2 id="using-dashes">- using dashes: -</h2>
<ul>
<li>day 1</li>
<li>day 2</li>
<li>day 3
<ul>
<li>day 3a</li>
<li>day 3b
<ul>
<li>(sub list)</li>
</ul>
</li>
</ul>
</li>
<li>day 4</li>
<li>day 5</li>
</ul>
<h2 id="using-esterics">- using esterics: *</h2>
<ul>
<li>ajwa</li>
<li>abdullah</li>
<li>zainab</li>
<li>hira</li>
<li>ahsan</li>
</ul>
<h2 id="using-plus-sign">- using plus sign: +</h2>
<ul>
<li>green</li>
<li>blue</li>
<li>red</li>
<li>purple</li>
<li>yellow</li>
</ul>
<blockquote>
<h3 id="numbering">Numbering:</h3>
</blockquote>
<ol>
<li>happy</li>
<li>sad</li>
<li>angry</li>
<li>excited</li>
<li>depressed</li>
<li>gloomy</li>
<li>joyful</li>
</ol>
<h1 id="8-page-breaks">8. Page breaks</h1>
<h2 id="i-am-ajwa-ahsan">I am Ajwa Ahsan.</h2>
<p>I am a good girl.</p>
<hr>
<p>I like reading books.</p>
<hr>
<p>I live in Pakistan.</p>
<h1 id="9-links-and-hyperlinks">9. Links and Hyperlinks</h1>
<p><a href="https://www.youtube.com/results?search_query=karissaeats+">https://www.youtube.com/results?search_query=karissaeats+</a></p>
<p><a href="https://www.youtube.com/results?search_query=karissaeats+">Click here to open Youtube</a></p>
<p>I you want to open Youtube, click <a href="https://www.youtube.com/results?search_query=karissaeats+">here</a></p>
<h1 id="10-images-and-figures-with-links">10. Images and Figures with Links</h1>
<h2 id="qr-code">QR code:</h2>
<p>To open a picture of a castle, please scan the following QR code:</p>
<p><img src="QR_code.png" alt="QR"></p>
<h2 id="online-picture">Online Picture:</h2>
<p><img src="https://ph.pinterest.com/pin/305189312263992992/" alt="aesthetic"></p>
<h1 id="11adding-a-code-or-code-block">11.Adding a Code or Code Block</h1>
<p>If you want to write a code in a text you do it like this, <code>print(I am a code)</code> or you can use a code block like this:</p>
<pre class="hljs"><code><div>x = 5-3+6
y = 70-43-9
z = x + y + 87
</div></code></pre>
<blockquote>
<p>This block of code will show the code according to python language syntax:</p>
</blockquote>
<pre class="hljs"><code><div>x = <span class="hljs-number">5</span><span class="hljs-number">-3</span>+<span class="hljs-number">6</span>
y = <span class="hljs-number">70</span><span class="hljs-number">-43</span><span class="hljs-number">-9</span>
z = x + y + <span class="hljs-number">87</span>
</div></code></pre>
<blockquote>
<p>This block of code will show the code according to R language syntax:</p>
</blockquote>
<pre class="hljs"><code><div>x = <span class="hljs-number">5</span>-<span class="hljs-number">3</span>+<span class="hljs-number">6</span>
y = <span class="hljs-number">70</span>-<span class="hljs-number">43</span>-<span class="hljs-number">9</span>
z = x + y + <span class="hljs-number">87</span>
</div></code></pre>
<h1 id="12-adding-tables">12. Adding Tables</h1>
<table>
<thead>
<tr>
<th style="text-align:center">species</th>
<th style="text-align:right">petal_length</th>
<th style="text-align:left">sepal_length</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">virginica</td>
<td style="text-align:right">18</td>
<td style="text-align:left">43</td>
</tr>
<tr>
<td style="text-align:center">setosa</td>
<td style="text-align:right">45</td>
<td style="text-align:left">56</td>
</tr>
<tr>
<td style="text-align:center">versicolor</td>
<td style="text-align:right">09</td>
<td style="text-align:left">87</td>
</tr>
<tr>
<td style="text-align:center">virginica</td>
<td style="text-align:right">18</td>
<td style="text-align:left">43</td>
</tr>
<tr>
<td style="text-align:center">setosa</td>
<td style="text-align:right">45</td>
<td style="text-align:left">56</td>
</tr>
<tr>
<td style="text-align:center">versicolor</td>
<td style="text-align:right">09</td>
<td style="text-align:left">87</td>
</tr>
</tbody>
</table>
<h1 id="13-install-extensions">13. Install Extensions</h1>
<p><strong>bold</strong>  (ctrl+b)<br>
<em>italic</em> (ctrl+i)<br>
<strong><em>italic and bold</em></strong> (ctrl+b and ctrl+i)<br>
<a href="https://chatgpt.com/">link</a> (ctrl+l)<br>
<img src="QR_code.png" alt="image"> (ctrl+shift+i)<br>
<s>stikethrough</s> (right click, toggle strikethrough)</p>
<pre class="hljs"><code><div>x = 34
y = 56      (ctrl+M ctrl+C)
z = x + y
</div></code></pre>
<p><code>x = 3, y = 5, z = x + y </code>   (ctrl+M ctrl+L)</p>

</body>
</html>
