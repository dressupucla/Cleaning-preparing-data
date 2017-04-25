Importing: Uploading Spreadsheet
---------------------

1.  Open OpenRefine

    1.  The url <http://127.0.0.1:3333/> should lauch automatically in
        the default browser. If it doesn’t manually go to address

2.  Create Project

3.  Upload files

4.  Click **Next**

5.  Make sure fields are formatted correctly and then click **Create
    Project**

History: Undoing Changes
---------------

1.  Click on **Undo / Redo** tab (located on the left sidebar)

2.  Choose change you want to undo (the image below will show the under
    undoing adding .jpg to the filename column.

    <img src="./media/image1.png" width="297" height="404" /><img src="./media/image2.png" width="319" height="402" />

Filtering/Faceting: Normalizing values (i.e. USA and US)
---------------------------------------

1.  Click on Arrow of desired column (blue arrow)

2.  Choose **Facet &gt; Text Facet**

3.  In the right column all facets will appear

4.  Click on **Cluster** (red arrow)
    
    <img src="./media/image3.png" width="623" height="218" />

5.  For **Keying Function** choose from dropdown based on results

6.  Change **New Cell Value** if necessary (green arrow)

7.  Check the boxes under the **Merge?** Column if you want the values
    in a cluster merged into one value (yellow arrow)

    <img src="./media/image4.png" width="624" height="366" />

8.  Click on **Merge Selected & Re-Cluster** (**orange** arrow)

    1.  This will allow you to make sure no cells have been missed, the
        below image shows the results after the first cluster, a
        different **Keying Function** yielded more results

        <img src="./media/image5.png" width="624" height="366" />

Filtering/Faceting: Normalizing Values which are not shown with the Cluster Method
-----------------------------------------------------------------

1.  If a like value is not being grouped correctly with **Cluster** rows
    can be manually changed to match

2.  In the right side column, find the facet to change.

3.  Click **edit**

4.  Change facet to correct value, **Apply.**

5.  All facets with that Value will be changed.

> The example below shows steps 3, 4 and 5. The Facet **Alejandro
> Fornes** was edited to be **Alejandro Rodriguez Fornes (Alucho).**
> Then applied. As the third picture shows, the facets have been
> combined (the number of rows with the facet increased from 4 to 7)

<img src="./media/image6.png" width="358" height="255" /><img src="./media/image7.png" width="298" height="251" />

<img src="./media/image8.png" width="691" height="238" />

Filtering/Faceting: Creating Custom Text Facets
---------------------------

Openrefine allows for uses to create custom facets, using functions. The
functions allow users to view transformed facets. For example, if you
want to view only the first names of the autors in the image above, a
custom facet can be built to view. To see other expressions, go to
<https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Users#reference>

1.  Click on column arrow

2.  Choose **Facet &gt; Custom text facet…**
<img src="./media/image9.png" width="471" height="194" />

3.  Enter the expression needed. (The example below splits at spaces,
    and chooses the first value)

4.  Click OK.

    <img src="./media/image10.png" width="515" height="296" />

    <img src="./media/image11.png" width="550" height="370" />

5.  The facets will allow the user to exclude or include facets

    <img src="./media/image12.png" width="686" height="301" />

Filtering/Faceting: Searching through Facets
------------------------

Openrefine allows users to search through facets, an allows for multiple
facets to be searched at once.

1.  Click on arrow

2.  Choose **Text Filter**

3.  In sidebar type in search

4.  Repeat as many times as needed (see image 2)

> <img src="./media/image13.png" width="453" height="275" />
>
> <img src="./media/image14.png" width="621" height="231" />

Editing Cells: Transforming Cells
------------------

This section outlines how to mass edit one column. This example will add
the file extension to the filename.

1.  Click on the column arrow

2.  Choose **Edit cells &gt; Transform…**
<img src="./media/image15.png" width="345" height="290" />

3.  Enter expression to transform cell. Same expression documentation as
    **Creating Custom
    Text Facets.**<https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Users#reference>

4.  Click **OK**

> <img src="./media/image16.png" width="325" height="258" /><img src="./media/image17.png" width="390" height="170" />

Editing Cells: Split multi-valued Cells
------------------
This method splits cells at a specific given seperator (,:).  It will the values in the cells into their own row.

1. Click on column arrow

2. Choose **Edit cells > Split multi-valued cells…**

<img src="./media/image32.png" width="400" height="438" />

3. Enter the correct separator value (a , for this example)

4. Click Ok

<img src="./media/image33.png" width="345" height="170" /><img src="./media/image34.png" width="400" height="190" />

Editing Cells: Join multi-valued Cells
------------------
This examples uses split cells from the previous example and rejoins the cells.

1. Click on column arrow

2. Choose **Edit cells > Join multi-valued cells…**

<img src="./media/image35.png" width="400" height="283" />

3. Choose the separator the values should be separated by (this example uses a ;)

4. Click OK

<img src="./media/image36.png" width="345" height="196" /><img src="./media/image37.png" width="400" height="122" />



Editing Cells: Trim whitespace, change cells to lowercase, uppercase, etc.
-----------------------------------------------------------

There are a number of common transformation that openrefine offers its
user. They are shown in the image below.

1.  Click on column arrow

2.  Choose **Edit cells &gt; Common transforms &gt; \[Selected
    Transform\]**

    <img src="./media/image21.png" width="317" height="378" />

Editing Columns: Copying and Transforming Columns
--------------------------------

This section allows for the section on **Transforming Cells** to be
performed by copying and transforming in another column, instead of
overwriting the original column.

1.  Choose **Edit column &gt; Add column based on this column…**

2.  Add **New column name**

3.  Add expression
    (<https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Users#reference>)

4.  Click **OK**

    <img src="./media/image18.png" width="442" height="334" />

    <img src="./media/image19.png" width="318" height="234" /><img src="./media/image20.png" width="384" height="287" />


Editing Cells: Fill Down
--------------------------------
This method allows for empty cells to be filled with the previously filled cell's value.

1. Choose column arrow

2. Choose **Edit cells > Fill down**

<img src="./media/image38.png" width="300" height="258" /><img src="./media/image39.png" width="300" height="367" />

Reconcilination: Matching Cells to Controlled Vocabularies
-----------------------------------------

There are a number of vocabularies that can be reconciled against cells
including LCSH, VIAF and Wikipedia. These are the basic instructions.
Info reconcilable databases is found here:
<https://github.com/OpenRefine/OpenRefine/wiki/Reconcilable-Data-Sources>

**IMPORTANT NOTE:** A better **VIAF** matching service can be found
here: <http://refine.codefork.com/>

Matching url: **http://refine.codefork.com/reconcile/viaf**

**LCSH:** http://freeyourmetadata.org/reconciliation/

**Wikipedia** matching url:
<https://tools.wmflabs.org/openrefine-wikidata/en/api>

https://github.com/OpenRefine/OpenRefine/wiki/Reconciliation-Service-API

1.  For LCSH follow instructions on freeyourmetadata.org, for other
    services follow the following instructions

2.  In openrefine, choose column arrow

3.  Choose **Reconcile &gt; Start reconciling…**

    <img src="./media/image22.png" width="303" height="326" />

4.  Click **Add Standard Service…** (blue arrow)

5.  Put matching url in box, this example uses VIAF’s
    [**http://refine.codefork.com/reconcile/viaf**](http://refine.codefork.com/reconcile/viaf)
    **(green** arrow)

6.  Click **Add Service** (purple arrow)

    <img src="./media/image23.png" width="714" height="373" />

7.  Click **Start Reconciling**

    <img src="./media/image24.png" width="588" height="484" />

8.  After the program has finished reconciling the program should look
    like the image below.

9.  Two things can happen: these topics can be matched to their cells or
    the best matches can be put into another column. This will show both

### Matching with cells.

1.  Click the check to match with the single cell, the double check will
    match to all identical cells (see image below)

2.  Matched cells will be shown in sidebar, additionally, the records are
    hyperlinks, so the information contained can be viewed.
    
    <img src="./media/image25.png" width="615" height="351" />

<img src="./media/image26.png" width="626" height="363" />

### Adding matches to columns

1.  Click on Column arrow

2.  Chosoe **Edit column &gt; Add column based on this column…**

3.  Name the column

4.  Use the following documentation to choose
    <https://github.com/OpenRefine/OpenRefine/wiki/Variables>

5.  This example chooses the cell, grabs the best match, and chooses the
    name

6.  Click **OK**

    <img src="./media/image27.png" width="624" height="472" />

<img src="./media/image28.png" width="679" height="440" />

Extension Installation 
-----------------------

Extension installation is covered in the first \_\_ steps.

1.  Download extension, this example downloads from here:
    http://software.freeyourmetadata.org/ner-extension/

2.  Go to openrefine home page

3.  Click **Open Project (blue arrow)**

4.  At the Bottom of the page click on **Browse Workplace directory
    (red arrow)**

<img src="./media/image29.png" width="699" height="397" />

5.  A file folder window should open

    <img src="./media/image30.png" width="484" height="349" />

6.  If there is no folder named **extensions** create one

7.  Open the **extensions** folder

8.  Copy the downloaded extension into the folder

    1.  Make sure to unzip the file

<img src="./media/image31.png" width="646" height="427" />

1.  Restart openrefine

Named Entity Extraction
-----------------------

Named Entity Extraction will pull named entities (like names) from
description fields. Install instructions can be found here:
<http://freeyourmetadata.org/named-entity-extraction/> and below.

1.  Preform Extension Installation (seen above).  Download extension from: <http://software.freeyourmetadata.org/ner-extension/>

2. Once OpenRefine has been restarted, in the upper right hand corner under extensions: click on Named-entity recognition

3. Configure API services (note: some links are dead, new links below)
    Zemanta = <http://www.zemanta.com/?oppistid=aLSUtbXYbGt>
    dataTXT = <https://dandelion.eu/docs/api/datatxt/nex/getting-started/>

4. Click Update
    
5. Click on column arrow

6. Choose **Extract named entities...**

7. Click on proper API's.  DBpedia does not require an API key

8. **Start Extraction**
