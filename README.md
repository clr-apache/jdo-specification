# How to Edit the JDO Specification
## Overview
The JDO Specification is maintained in Apache OpenOffice format. It consists of 
a master document JDO_master.odm, a template JDO_spec.ott, and a file 
for each chapter and appendix.

The following sections explain each of these document types and how to work with them.
## Getting Started
Download Apache OpenOffice 3.4 from https://www.openoffice.org/download/ 
and then download and install the Template Changer extension 
https://extensions.services.openoffice.org/project/templatechanger. 
The template changer is needed if you  make style changes to the template. 
Next, check out the specification from the JDO subversion repository 
(see https://db.apache.org/jdo/svn.html for more information).
## Editing
When editing the specification, record changes so it is easy for others to find 
the changes you have made. "Edit" "Changes" "Record". When ready to commit the changes, 
go through the document and accept all changes for a particular activity.
## Master Document
The master document JDO_master.odm contains the text of the front matter 
and back matter, the automatically-generated table of contents and index, 
and references to the chapters and appendices. File order and pagination 
are determined by the master document. The navigator, whose display 
is toggled by the F5 key, lists the file, text, and generated elements of 
the document. Although the text of the referenced files is displayed in the 
master document, it cannot be directly edited.
Use the master document to do any of the following tasks:
- Navigate to sub-documents and open them.
- Edit front matter and back matter.
- Edit header and footer content
- Regenerate the table of contents and index.
- Generate PDF output.
- Print the specification.
See https://www.openoffice.org/documentation/manuals/oooauthors/MasterDocs.pdf 
for detailed information about master documents.
### Chapters and Appendices
Chapters and appendices are ordinary OpenOffice Writer documents, with 
the extension .odt. They may be opened for editing from the operating system, 
from the OpenOffice File menu, or by double-clicking the entry on the master 
document's navigator. Entering content is as simple as typing the text. To change 
formatting, place the cursor in the paragraph whose style you want to change and 
select the style you want to apply from the paragraph styles combo box on 
the formatting toolbar. If the desired style is not there, click More... and then 
double-click it from the Styles and Formatting window that opens.
### Assertions
Testable assertions in the specification are numbered by chapter, section, and 
sequential identifier and bracketed in the text. The markers are assigned the 
Assertion character format, which makes them hidden, or blue when visible. Use 
the paragraph icon on the tool bar to toggle between hide and unhide. To add and 
mark assertion markers:
1. Display the style window using the top menu Format → Styles and Formatting.
1. Click the character styles icon (capital A) to display the available character styles.
1. Enter the marker text, e.g. A23.5.1[ specification text... ].
1. Select or multi-select marker text and double-click Assertion in the style window.
### Index Entries
New specification content may require new index entries. To add an index entry to a chapter:
1. Select the text that you wish to make an index entry for.
1. From the Insert menu, select Indexes and Tables / Entries...
1. On the Insert Index Entry dialog, make the following selections:
- From the Index combo box , select Alphabetical Index.
- Leave 1st key empty.
- Check Main entry
- Check Apply to all similar texts.
- Check Whole words only

Your selected text appears in the Entry text box. Click Insert to insert index entries.
#### To make additional entries in the same chapter:
1. Select the next entry text.
1. Click in the Entry text box. Your selected text will appear in the box.
1. Click Insert. 
### Template
Templates contain all of the styles used in a document. A template may also contain 
content, but our template does not. Using a limited, predefined set of styles and 
organizing them in a template provides consistency and maintainability for the format 
of the document. This benefit comes at the expense of some overhead in managing 
the template. 

To make changes to the template, such as modifying a style, you must 
always edit the template directly and then apply the changes to all of the files. 
Any changes made to a style from within a file will apply to that file alone. 
They do not propagate to the template or to other files using the template, even if 
made in the master file. To avoid problems, follow the procedures below.
#### Editing the template
1.  From OpenOffice Writer, choose File > Templates > Edit and navigate to 
JDO_spec.ott in your local spec repository.  In Windows, you may also open 
JDO_spec.ott by navigating to it in Windows Explorer, right-selecting it and 
choosing Open from the context menu. Do not double-click the file, as that 
brings up a new document file, not the template. 
1. Modify the template as desired.
1. To save changes, choose File > Save or click the save icon, as with an ordinary document.
1. Apply the template to all of the documents in the spec. (See below.)
#### Applying changes in the template
1. Close the master file and all spec document files.
1. From OpenOffice Writer, choose File > Templates > Assign template (folder).
1. In the Assign Template to Documents dialog, fill the text boxes labeled Template file, 
Document folder, Destination folder by navigating to those items in your JDO spec local 
repository. Use the same location for document and destination folder to modify the files in place.
1. Check the first and fourth Document types boxes (.odt and .odm) and uncheck the second and third.
1. Click OK.
### Creating a new chapter or appendix document
1. Choose File > New > Templates and Documents.
1. In the box on the left, click the Templates icon if it is not already selected.
1. Double-click My Templates and select JDO_spec.ott. Alternatively, you may 
double-click JDO_spec.ott in your file explorer. A new document based on the 
JDO specification template opens and you may begin editing.

#### To add the new chapter to the master document:
1. Open the master document and select the chapter below the location where 
you want to add the new chapter.
1. Right-click and select Insert > File.
1. In the File chooser dialog, select the new chapter and click OK.
See https://www.openoffice.org/documentation/manuals/oooauthors/working_with_templates.pdf 
for more information about templates. Some of the procedures described in this document differ 
from the OpenOffice documentation, to allow working with the template file directly from a 
local repository rather than having to copy it into the OpenOffice standard template directory.
## Publication as PDF
1. Open JDO_master.odm. Reply Yes to (Update all links?)
1. Choose File > Export as PDF
1. On the Initial View tab, select Bookmarks and page panes.
1. On the User Interface tab Bookmarks section, select visible bookmark levels and choose 1 level.
Click Export and enter a name for the pdf document.
## Cross-references between sub-documents
A technique for using cross-references between sub-documents of a master document is described 
in https://www.openoffice.org/documentation/manuals/oooauthors/MasterDocs.pdf.
## Auto-lettering of Appendix headings
In order to get Appendices to use letters for numbering and to get the heading auto-numbering 
to work properly, we use different heading styles in the appendices. The following briefly 
describes the procedure that was used to set up the appendix headings.

- Define a numbering style called Appendix Numbering that configures the numbering for all 
levels of headings in the appendices. The top level uses "A, B, C, ..." and the sub levels 
use "1, 2, 3, ..." to give sub-heading numbers like A.1.1. Use the Position and Options tabs 
to configure this style.

- For the appendix, define a specific paragraph style for each level of heading: Appendix Heading1, 
Appendix Heading 2, and Appendix Heading 3. Configure the heading styles to use the 
custom numbering style we defined above. Each separate heading style will point to the 
same numbering style. 
- To get Appendix headings to appear in the TOC, right click the TOC and select Edit. 
On the Index/Table tab, Check Additional Styles under Create from. Click the ellipsis box 
to select the appendix heading styles and use the arrows to align them with 
the correct outline level.
## References
Excellent documentation for OpenOffice is available at 
https://www.openoffice.org/documentation/manuals/oooauthors/ in the Writer Guide section.
