<h1>HL7 C-CDA Viewer</h1>

<h2>Synopsis</h2>
Easy to use rendering of complex C-CDA documents directly in any web browser.
Responsive document layout automatically adjusts to make optimum use of the available screen space.
Users can hide, collapse and move any section of a CDA document.
<p>Document sections can be manipulated directly via button clicks, drag and drop or via a document Table Of Contents (TOC).</p>
<p>All user preferences are saved and automatically applied to <b>subsequent CDA documents opened</b>.</p>
<p>Ability to detect and hide/show duplicates.</p>
<p>The result is an intuitive and easy to use document layout that users can control directly.</p>
<img src="https://cloud.githubusercontent.com/assets/17036351/15345667/5f24a74a-1cf4-11e6-8739-374faa221a35.gif" />

<p>All this using simple deployment via a local fileset or web server (and its very pretty).</p>
<p>Sample documents are included in the deployment. Any C-CDA document can be rendered via cut and paste of the document text.</p>
<p>Winner of the <a href="http://blog.hl7.org/hl7ccdachallenge" target="_blank">HL7 C-CDA Tooling Challenge</a></p>

<h2>Platform</h2>
<ul>
<li>Runs in any modern browser (tested on FF 46.0, IE11 and Chrome 49, Safari). PC, tablet or mobile. </li>
<li>Will run as a standalone local fileset (not in Chrome, due to security issues)</li>
<li>Load onto any web file server to run on Chrome</li>
</ul>

<h2>Demonstration</h2>
A demonstration version is deployed here:
http://intelsoft.com.au/challenge/index.htm

<h2>Features</h2>
<ul>
<li>Users can control document layout via Section hide/show, collapse/expand and re-ordering. </li>
<li>As user makes changes, the layout adjusts to make best use of available screen space.</li>
<li>All changes are saved as preferences that will apply across documents (ie open a new document and the same order/visibility preferences are applied against all sections).</li>
<ul>
	<li>Sections are identified via coding applied across documents.</li>
	<li>eg. If 'Procedures' has been moved to the top of the document, then 'Procedures' will be at the top of the next document opened.</li>
</ul>
Sample documents are available, or you can cut and paste the xml of a C-CDA document into the text box, then click 'View'.
<li>Duplicate entries in tables are detected. The user can decide whether these are hidden or shown.</li>
</ul>

<h2>Move and Re-Ordering</h2>
<ul>
<li>Drag and Drop a section where you want it to go.</li>
<li>Move a section up to the top of the list by clicking on the double-up arrow.</li>
<li>Move a section down one by clicking on the single-down arrow.</li>
</ul>

<h2>Show/Hide Sections</h2>
<ul>
<li>Hide sections by clicking on the cross, or from the Table Of Contents (TOC)</li>
</ul>

<h2>Collapse/Expand sections</h2>
<ul>
<li>Click the collapse/expand icon on any section.</li>
<li>Collapse/Expand all section with the Collapse/Expand all button.</li>
</ul>

<h2>TOC (Table Of Contents)</h2>
<ul>
<li>Use the TOC to see all available sections in the document, and to show/hide or move sections.</li>
<li>Reset all preferences to defaults.</li>
</ul>

<h2>Deployment</h2>
<h3>Local Deployment</h3>
Download the fileset. 
Open 'index.htm' in a web browser.
<h3>Web Deployment</h3>
Download the fileset and save to a public directory (eg. C-CDA_Viewer). The viewer is then available at:
<p>http://yoururl/[C-CDA_Viewer_path]/index.htm</p>

Enjoy.


<h2>Implementation</h2>
core.js: C-CDA specific processing is carried out in core.js.

xslt.js: a javascript library that performs xsl transformations in the browser. A transformation requires two input strings, an xml and xsl string. Both must be well formed xml.
<p>The xslt.js library was updated as it would not work in IE11.</p>
The transformation is carred out in core.js:

<code>
new Transformation().setXml(cdaxml).setXslt('cda.xsl').transform("viewcda");
</code>

cdaxml: xml string that is set in the script.
cda.xsl: local xsl file.
viewcda: target div

XSL: cda.xsl is an extension of ANSI/HL7 CDAR2, v.3 (cda.xsl), which provides provision of narrative content. The extensions allow the dynamic layout functionality.

Layout: packery javascript library. http://packery.metafizzy.co/

Icons: font-awesome standard icon set. https://fortawesome.github.io/Font-Awesome/icons/

Background css: purecss.io

<h2>Copyright</h2>
 Copyright (c) 2016 Bryn Lewis (<mailto:brynlewis@intelsoft.com.au>)
<http://intelsoft.com.au>
 
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
