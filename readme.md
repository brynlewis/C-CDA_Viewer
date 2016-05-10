<h1>HL7 C-CDA Viewer: (Intelsoft)</h1>

<p>Complex C-CDA documents are rendered directly in the browser.</p>
<p>Document layout instantly and automatically adjusts to make optimum use of the available screen space.</p>
<p>Users can hide, collapse and move any section of a CDA document.</p>
<p>Document sections can be manipulated directly via button clicks, drag and drop or via a document Table Of Contents (TOC).</p>
<p>All user preferences are saved and automatically applied to <b>subsequent CDA documents opened</b>.</p>

<p>The result is an intuitive and easy to use document layout that users can control directly.</p>
<p>All this using simple deployment via a local fileset or web server.</p>
<p>Sample documents are included in the deployment. Any C-CDA document can be rendered via cut and paste of the document text.</p>

<h2>Platform</h2>
<li>Runs in any modern browser (tested on PC FF 46.0, IE11 and Chrome 49, Safari). </li>
<li>Will run as a standalone local fileset (not in Chrome, due to security issues)</li>
<li>Load onto any web file server to run on Chrome</li>

<h2>Demonstration</h2>
A demonstration version is deployed here:
http://intelsoft.com.au/challenge/home.htm

<h2>Features</h2>
<li>Users can control document layout via Section hide/show, collapse/expand and re-ordering. </li>
<li>As user makes changes, layout adjusts to make best use of available screen space.</li>
<li>All changes are saved as preferences that will apply across documents (ie open a new document and the same order/visibility preferences are applied against all sections).</li>

<h2>Move and Re-Ordering</h2>
<li>Drag and Drop a section where you want it to go.</li>
<li>Move a section up to the top of the list by clicking on the double-up arrow.</li>
<li>Move a section down one by clicking on the single-down arrow.</li>

<h2>Show/Hide Sections</h2>
<li>Hide sections by clicking on the cross, or from the Table Of Contents (TOC)</li>

<h2>Collapse/Expand sections</h2>
<li>Click the collapse/expand icon on any section.</li>
<li>Collapse/Expand all section with the Collapse/Expand all button.</li>

<h2>TOC (Table Of Contents)</h2>
<li>Use the TOC to see all available sections in the document, and to show/hide or move sections.</li>
<li>Reset all preferences to defaults.</li>

<h2>Deployment</h2>
<h3>Local Deployment</h3>
Download the fileset. Open 'index.htm'
<h3>Web Deployment</h3>
Download the fileset and save to a public directory (eg. C-CDA_Viewer). The viewer is available at:
<p>http://yoururl/<C-CDA_Viewer_path>/index.htm</p>

<h2>Implementation</h2>
All scripts used have open source licences. Their licences are reference from their calling locations.

core.js: Most of the C-CDA specific processing is carried out in core.js.

xslt.js: a javascript library that performs xsl transformations in the browser. A transformation requires two input strings, an xml and xsl string. Both must be well formed xml.
<p>The xslt.js library was updated as it would not work in IE11.</p>
The transformation is carred out in core.js:

new Transformation().setXml(cdaxml).setXslt('cda.xsl').transform("viewcda");

cdaxml is an xml string that is set in the script.
'cda.xsl' is a local xsl file.

Layout: packery javascript library. http://packery.metafizzy.co/

Icons: font-awesome standard icon set. https://fortawesome.github.io/Font-Awesome/icons/

Background css: purecss.io

<h2>Copyright</h2>
 * Copyright (c) 2016 Bryn Lewis (<mailto:brynlewis@intelsoft.com.au>)
 * <http://intelsoft.com.au>
 * 
 * Permission is hereby granted, free of charge, to any person obtaining a
 * copy of this software and associated documentation files (the "Software"),
 * to deal in the Software without restriction, including without limitation
 * the rights to use, copy, modify, merge, publish, distribute, sublicense,
 * and/or sell copies of the Software, and to permit persons to whom the
 * Software is furnished to do so, subject to the following conditions:
 * 
 * The above copyright notice and this permission notice shall be included
 * in all copies or substantial portions of the Software.
 * 
 * THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
 * OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
 * MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN
 * NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
 * DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
 * OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
 * USE OR OTHER DEALINGS IN THE SOFTWARE.
