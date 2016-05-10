<h1>HL7 C-CDA Viewer: Slidery (Intelsoft)</h1>

<h2>Features</h2>
-Users can control document layout via Section via hide/show, colapse/expand and re-ordering. 
-As user makes changes, layout adjusts to make best use of available screen space.
-All changes are saved as preferences that will apply across documents (ie open a new document and the same order/visibility preferences are applied against all sections).


<h2>Platform</h2>
-Runs in any modern browser (tested on PC FF 46.0, IE11 and Chrome 49, Safari. )
-Will run as a standalone local fileset (not in Chrome, due to security issues)
-Load onto any web file server to run on Chrome

<h2>Demonstration</h2>
A demonstration version is deployed here:
http://intelsoft.com.au/challenge/home.htm

<h2>Move and Re-Ordering</h2>
-Drag and Drop a section where you want it to go.
-Move a section up to the top of the list by clicking on the double-up arrow.
-Move a section down one by clicking on the single-down arrow.

<h2>Show/Hide Sections</h2>
-Hide sections by clicking on the cross, or from the Table Of Contents (TOC)

<h2>Collapse/Expand sections</h2>
-Click the collapse/expand icon on any section.
-Collapse/Expand all section with the Collapse/Expand all button.

<h2>TOC (Table Of Contents)</h2>
-Use the TOC to see all available sections in the document, and to show/hide or move sections.
-Reset all preferences to defaults.

<h2>Slidery Implementation</h2>
All scripts used have open source licences. Their licences are reference from their calling locations.

core.js: Most of the C-CDA specific processing is carried out in core.js.

xslt.js: a javascript library that performs xsl transformations in the browser. A transformation requires two input strings, an xml and xsl string. Both must be well formed xml.

The transformation is carred out in core.js:

new Transformation().setXml(cdaxml).setXslt('cda.xsl').transform("viewcda");

cdaxml is an xml string that is set in the script.
'cda.xsl' is a local xsl file.

Layout: packery javascript library. http://packery.metafizzy.co/

Icons: font-awesome standard icon set. https://fortawesome.github.io/Font-Awesome/icons/

Background css: purecss.io