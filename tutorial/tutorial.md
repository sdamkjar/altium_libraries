<script>
	
  function resizeIframe(obj) {
    obj.height = obj.contentWindow.document.body.scrollHeight + 'px';
  }
</script> 

<a name="headerTop"></a>
# AlbertaSat Printed Circuit Board Design Guide

<b>Author: Stefan Damkjar (sdamkjar@ualberta.ca)</b>

## Licensing Notice
Copyright: 2018, 2019, 2020 Stefan Damkjar

This file and the information within it are licensed under the terms of the Apache License, Version 2.0 (the "License"); you may not use or redistribute this file except in compliance with the License. You may obtain a copy of the License at

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 0em; text-align:center;" >	
    <a target="_blank" href="http://www.apache.org/licenses/LICENSE-2.0">http://www.apache.org/licenses/LICENSE-2.0</a>
</blockquote><p></p>

Unless required by applicable law or agreed to in writing, content distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

## Introduction

The purpose of this document is to help AlbertaSat members, and users of AlbertaSat's open source content, access and contribute to AlbertaSat's printed circuit board designs. This document should help you with navigating AlbertaSat's Altium design projects, as well as with accessing AlbertaSat's open source repositories, and using and contributing to AlbertaSat's component database. If you have questions or concerns regarding this document, contact the author (sdamkjar@ualberta.ca).

## Table of Contents

1. [Getting Started Tutorials.](#header01)<br>
	1.1. [Installing Altium and CMC CADpass](#header01_01)<br>
	1.2. [Introductory Altium Tutorials](#header01_02)<br>
2. [Using the AlbertaSat SVN Repository](#header02)<br>
	2.1. [Checkout the SVN Repository using TortoiseSVN](#header02_01)<br>
    2.2. [Accessing the SVN Repository using a Web Browser](#header02_02)<br>
	2.3. [Updating your Files from the SVN Repository – SVN Update](#header02_03)<br>
    2.4. [Commiting your Files to the SVN Repository – SVN Commit](#header02_04)<br>
3. [Using the AlbertaSat Component Database](#header03)<br>
	3.1. [Using the Database in an Altium Project](#header03_01)<br>
	3.2. [Adding New Content to the Database](#header03_02)<br>
4. [How to Edit this document](#header04)<br>

### Appendices

1. [Appendix A - Manufacturer Abbreviations](#headerA)<br>
2. [Appendix B - Acronyms](#headerB)<br>

<a name="header01"></a>
## 1. Getting Started Tutorials

<a name="header01_01"></a>
### 1.1. Installing Altium and CMC CADpass

<iframe src="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/cmc.html" frameborder=0 scrolling="no" align="middle" allowfullscreen onload="resizeIframe(this)" width="100%">
    <blockquote style="background-color: rgb(255, 153, 153);border-radius: 5px;border-color: red; font-size: 100%;margin: 0;padding: 1em 1em; text-align:center;" >	
	<a style="color: rgb(200, 0, 0);"><b>There was an error displaying this section. Please report this issue to <a href = "mailto: sdamkjar@ualberta.ca">sdamkjar@ualberta.ca</a></b></a>
	</blockquote>
</iframe>

[Back to top...](#headerTop)

<a name="header01_02"></a>
### 1.2. Introductory Altium Tutorials

The official getting started tutorial published by Altium:

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 1em; text-align:center;" >	
    <a target="_blank" href="https://www.altium.com/documentation/19.0/display/ADES/From+Idea+to+Manufacture+-+Driving+a+PCB+Design+through+Altium+Designer">https://www.altium.com/documentation/19.0/display/ADES/From+Idea+to+Manufacture+-+Driving+a+PCB+Design+through+Altium+Designer</a>
</blockquote><p></p>

A brief (less than 4 hours) video series for Altium Beginners, published by Robert Feranec (a well known creator of Altium Tutorial content):

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 1em; text-align:center;" >	
    <a target="_blank" href="https://www.youtube.com/watch?v=KpgTud1iQ-4&list=PLXvLToQzgzdfKKQn2wmpuSXz6sROQmO6R">https://www.youtube.com/watch?v=KpgTud1iQ-4&list=PLXvLToQzgzdfKKQn2wmpuSXz6sROQmO6R</a>
</blockquote><p></p>

[Back to top...](#headerTop)

<a name="header02"></a>
## 2. Using the AlbertaSat SVN Repository

<a name="header02_01"></a>
### 2.1. Accessing the SVN Repository using TortoiseSVN – SVN Checkout

Apache Subversion (abbreviated <a target="_blank" href="https://en.wikipedia.org/wiki/Apache_Subversion" title="Subversion" style="color: purple;">SVN</a>) is a software versioning and revision control system. It is very similar to Git. AlbertaSat's <a target="_blank" href="https://en.wikipedia.org/wiki/Printed_circuit_board" title="Printed Circuit Board" style="color: purple;">PCB</a> projects are stored on an <a target="_blank" href="https://en.wikipedia.org/wiki/Apache_Subversion" title="Subversion" style="color: purple;">SVN</a> server on campus. Each time you `commit` a new version of a file to the server, that version is saved with a revision number. If you change your mind about something or lose some files, you can always go back and retrieve your previous versions.

The best way to access the <a target="_blank" href="https://en.wikipedia.org/wiki/Apache_Subversion" title="Subversion" style="color: purple;">SVN</a> repository is using an <a target="_blank" href="https://en.wikipedia.org/wiki/Apache_Subversion" title="Subversion" style="color: purple;">SVN</a> client such as TortoiseSVN which can be downloaded here:

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 0em; text-align:center;" >	
    <a target="_blank" href="https://tortoisesvn.net/downloads.html">https://tortoisesvn.net/downloads.html</a>
</blockquote><p></p>

There are other suitable <a target="_blank" href="https://en.wikipedia.org/wiki/Apache_Subversion" title="Subversion" style="color: purple;">SVN</a> clients and you can choose a different one if you wish. TortoiseSVN is only compatible with Windows computers. After TortoiseSVN is installed, some lines should appear in the right-click menu in your file explorer as shown in the screenshot below.

<div style="text-align:center"><img id="myImg" src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/004.png" ></div>
<div id="myModal" class="modal"><span class="close">&times;</span><img class="modal-content" id="img01"><div id="caption"></div></div> 
<div style="text-align:center"><font color="grey"><i>Fig. 4: Using the AlbertaSat SVN Repository: Right click menu</i></font></div><p></p>

Right click where you want your files to be stored and select `SVN Checkout...`. You should see a menu like in the screenshot below.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/005.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 5: Using the AlbertaSat SVN Repository: Checkout menu</i></font></div><p></p>

Enter `svn://pd-srv-vbird-03.physics.ualberta.ca/albertasat` under `URL of repository:`, and click `OK`. You should see something similar to the screenshot below as the files are downloaded from the server. It may take a few minutes to complete.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/006.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

There are two main folders in the <a title="Subversion">SVN</a> repository

* [libraries/](http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/libraries/)
* [projects/](http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/projects/)

The `libraries/` folder contains the [AlbertaSat Component Database](#header03) which contains the design files and information regarding all components used on AlbertaSat <a target="_blank" href="https://en.wikipedia.org/wiki/Printed_circuit_board" title="Printed Circuit Boards" style="color: purple;">PCBs</a>.

The `projects/` folder contains current and completed <a target="_blank" href="https://en.wikipedia.org/wiki/Printed_circuit_board"  title="Printed Circuit Board" style="color: purple;">PCB</a> projects. If you are creating a new project, you should create a new folder within the `projects/` folder for your project.

[Back to top...](#headerTop)

<a name="header02_02"></a>
### 2.2. Accessing the SVN Repository using a Web Browser

The AlbertSat SVN repository

[Back to top...](#headerTop)

<a name="header02_03"></a>
### 2.3. Updating your Files from the SVN Repository – SVN Update

To update your local copy of the [AlbertaSat SVN Repository](#header02), follow these Instructions

If either are open, quit both Altium and Microsoft Access. This is because both Altium and Microsoft Access actively use the component database file `libraries/AlbertaSat.mdb` while they are open. If you attempt to use the `update` function while Altium or Microsoft Access are open, then you might get an error message like the one pictured below. See [Section 2.3.2](#header02_03_02) for instructions about recovering from this error.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/009.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

Right-click somewhere in the repository folder and select `SVN Update`.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/012.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

If the update was succuessful, you should see a something like the picture below.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/013.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

<a name="header02_03_01"></a>
#### 2.3.1 Resolving or Reverting Conflicts

If you attempt to update a file that you have already made local changes to, then you will see an error message telling you there is a conflict. To resolve this conflict, you have two choices:

1. `Resolve` will keep your local copy and overwrite the copy in the repository. The old copy that was in the repository will still be saved as a previous revision and can be retrieved later if necessary. (this part is unfinished....)
2. `Revert` will overwrite your local, uncommited work. Generally, there is no way to undo this so take care when using the revert command. First, if either are open, quit both Altium and Microsoft Access. If you get a write access error, see [Section 2.3.2](#header02_03_02) for instructions about recovering from this error. To revert the file, right click the conflicting file and select `TortoiseSVN>Revert...`. Click OK in the window that appears. You should see a message telling you the operation was successful.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/019.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Reverting Conflicts</i></font></div><p></p>

[Back to top...](#headerTop)

<a name="header02_03_02"></a>
#### 2.3.2 Fixing an "Access is Denied" or "Run Cleanup" Error

If you attempted to update the component database file `libraries/AlbertaSat.mdb` while Altium or Microsoft Access were open, then you likely got an error message saying something along the lines of `Access is denied` or `Run Cleanup`. To fix this error, double check that Altium and Microsoft Access are both closed, and then right-click somewhere in the repository folder and select `TortoiseSVN>Clean up...`. 

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/010.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

Check the only the first 6 boxes and then click OK. You should then see a message telling you the cleanup was successful.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/011.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

[Back to top...](#headerTop)

<a name="header02_04_01"></a>
### 2.4. Commiting your Files to the SVN Repository – SVN Commit

Files stored on the AlbertaSat SVN Server are intended to be open source and are freely accessible to anyone with an internet connection. Writing to the server on the other hand, requires a username and password.

If you would like an account to be created for you, email `sdamkjar@ualberta.ca`.

Once you have a username and password set up, you will be able to `commit` to the server. Every time changes are written to the server, a new revision number is made. You can always role back to a previous revision if you accidently overwrite a file, or if you change your mind about some changes. This is essentially the purpose of using a version control system like SVN.

Files or folders that have been changed since you updated them from the server should be indicated with a red excelamation mark symbol.

To commit your changes, simply right click the file or folder you want to commit and click `SVN Commit...` as shown in the screenshot below.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/014.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

You should then see a window like the one shown below. Make sure the files you want to commit have a checkmark beside them, and write a brief comment in the `Message` field describing the changes you made.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/015.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

When you are ready to commit, click `OK`. You should should see some messages fly by in a window like the one shown below, following by a message telling you whether or not the commit was successful.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/016.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 6: Using the AlbertaSat SVN Repository: Checkout loading window</i></font></div><p></p>

<a name="header03"></a>
## 3. Using the AlbertaSat Component Database (ACD)

<a name="header03_01"></a>
### 3.1. Using the Database in an Altium Project

Before you can start using the AlbertaSat Component Database (ACD) in Altium, you must:

1. Have the 64-bit version of Microsoft Access installed on your computer. Current University of Alberta students can get this software for free using an `Office 365 ProPlus` license from OnTheHub. **Make sure that you select the 64-bit version when downloading it!**

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 0em; text-align:center;" >    
    <a target="_blank" href="https://ualberta.onthehub.com">https://ualberta.onthehub.com</a>
</blockquote><p></p>
 
2. Have the `64-bit Microsoft Access Database Engine` installed on your computer. The Microsoft Access Database Engine can be downloaded using the link below.

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 0em; text-align:center;" >	
    <a target="_blank" href="https://www.microsoft.com/en-us/download/details.aspx?id=54920">https://www.microsoft.com/en-us/download/details.aspx?id=54920</a>
</blockquote><p></p>

3. Include the database file `libraries/database.DbLib` in your Altium Project

To include the `libraries/database.DbLib` file in an Altium project, right click the `.PrjPcb` file in the `Projects` pane in Altium and select `Add Existing to Project...`

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/002.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 2: Using the component database: Select "Add Existing to Project..."</i></font></div><p></p>

Navigate to the `libraries/database.DbLib` file in your local copy of the [AlbertaSat SVN Repository](#header02), select it, and click `Open`.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/003.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Using the component database: Choose the .DbLib file</i></font></div><p></p>

Now, the database is included in your Altium project and you should be able to add pieces from it to your Altium schematics. Open or create a schematic (`.SchDoc`) file, and then open the `Components` pane. In Altium 18 and earlier, it is the `Libraries` pane. If you have added the database correctly, you should see a list of component manufacturers in this pane as shown below.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/007.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Using the component database: Choose the .DbLib file</i></font></div><p></p>

You can show and hide different columns to help search for components by right clicking around the column headers and selecting `Select Columns...` as shown below.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/008.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Using the component database: Choose the .DbLib file</i></font></div><p></p>

For general purpose resistors, look under Panasonic. For general purpose capacitors, look under `TDK Corporation` or `Taiyo Yuden`. Do not use components small than 0402 size because they will be too difficult to solder.

[Back to top...](#headerTop)

<a name="header03_02"></a>
### 3.2. Adding New Components to the Database

If you want to use a component that is not already in the AlbertaSat Component Database, then you must add it. This typically involves three steps:

1. [Add component information to the `libraries/AlbertaSat.mdb` file.](#header03_02_01)
2. [Create a symbol to represent the component in your schematics.](#header03_02_02)
3. [Create a footprint that will appear in your PCB layout.](#header03_02_03)

<a name="header03_02_01"></a>
#### 3.2.1 Adding Component Information

Information about each component must be entered in the `libraries/AlbertaSat.mdb` file. To avoid conflicting changes caused by two people editing this file at the same time, you must ensure you have the latest version of the file from the [AlbertaSat SVN Repository](#header02) and then run `Get Lock` on the file before making changes.

See [Section 2.3](#header02_03) for instructions about updating SVN files to ensure you have the latest version.

Once your files are up-to-date, right click on the `libraries/AlbertaSat.mdb` file and select `TortoiseSVN>Get lock...`

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/017.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 1)</i></font></div><p></p>

Click OK. You should then see a message telling you the cleanup was successful.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/018.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 2)</i></font></div><p></p>

If you see an error message saying that someone else has the file locked, the you must wait for that person to finish making changes and release the lock by commiting their changes. If it seems the person has forgetten to commit there changes, attempt to contact them. If they do not reply, contact (sdamkjar@ualberta.ca).

In general, commiting the file will automatically release the lock. See [Section 2.4](#header02_04) for instructions about commiting SVN files.

In some cases, TortoiseSVN will show that the `libraries/AlbertaSat.mdb` file has local changes, even though you have not made any changes. To fix this issue, simply revert you local copy. See [Section 2.3.1](#header02_03_01) for instructions on reverting conflicting changes.

Once you have updated and locked the `libraries/AlbertaSat.mdb` file, open the file using Microsoft Access. You should see a list of tables, each for a specific manufacturer. Within each table, there is information for components from that manufacturer.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/020.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 1)</i></font></div><p></p>

The component(s) you are looking for may already be listed. If not, you will need to add them. There is already a table in the database for the manufacturer of the component you want to add, then skip to [Adding a New Component to the Database](#header03_02_01_02). Otherwise, you will need to add a new table for the manufacturer.

<a name="header03_02_01_01"></a>
##### Adding a New Manufcaturer Table to the Database

1. In the Tables Pane on the left side of the window, right-click `__Template` and select Copy

2. Right click anywhere in the Tables Pane and select Paste

3. In the Paste Table As window, enter the name of the component manufacturer in the Table Name field, select Structure Only from the Paste Options field, and then click OK

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/021.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 1)</i></font></div><p></p>

4. Open the newly created table by double clicking it in the Tables pane.

5. Select Design View using the View Button on the left side of the toolbar.

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/022.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 1)</i></font></div><p></p>

6. Select Index in the Field Name column then modify Format in the Field Properties pane at the bottom of the window by replacing XXXX with a suitable 3 or 4 letter abbreviation of the component manufacturer's name. The abbreviation should not be the same as any others used. This ensures that every component in the database has a unique identifier. A list of all abbreviations currently being used can be found in [Appendix A](#headerA).

<div style="text-align:center"><img src ="http://pd-srv-vbird-03.physics.ualberta.ca/svn/albertasat/tutorial/pics/023.png" ></div>
<div style="text-align:center"><font color="grey"><i>Fig. 3: Adding Component Information: Locking the database file (Step 1)</i></font></div><p></p>

7. Select Part Number in the Field Name column then modify Default Value in the Field Properties pane at the bottom of the window by replacing XXXX with the same 3 or 4 letter abbreviation of the component manufacturer's name used in the previous step.

8. Select Library Path in the Field Name column then modify Validation Rule in the Field Properties pane at the bottom of the window by replacing XXXXXXXXX with the name of the  manufacturer. This specifies the file-path of the corresponding Schematic Library Altium file and must be exactly correct!

9. Select Footprint Path in the Field Name column then modify Validation Rule in the Field Properties pane at the bottom of the window by replacing XXXXXXXXX with the name of the component manufacturer. This specifies the file-path of the corresponding Footbrint Library Altium file and must be exactly correct!

10. Save the table and use the View Button on the left side of the toolbar to return to Datasheet View. The new table is now added.

11. Altium occassionally has trouble updating the list of tables in the `libraries/AlbertaSat.mdb` file. To fix this problem, open the `libraries/AlbertaSat.mdb` file in Altium and make a benign chance such as unchecking and rechecking the `Store Path Relative to Database Library` check box, and then save the `libraries/AlbertaSat.mdb` file and restart Altium.

12. In Altium select File > New > Library > Schematic Library. After the new file opens, select File > Save and save the new file in libraries\SCH_libs (at the top of the SVN repository). Enter the name of the component manufacturer as the File Name

13. In Altium select File > New > Library > PCB Library. After the new file opens, select File > Save and save the new file in libraries\PCB_libs (at the top of the SVN repository). Enter the name of the component manufacturer as the File Name

<a name="header03_02_01_02"></a>
##### Adding a New Component to the Database

1. In Microsoft Access, ensure the table you want to edit is open and in Datasheet View mode (select the view mode using the View button on the left side of the toolbar)

2. In the last line of the table (with (New) in the Index column), replace XX with the appropriate IEEE reference designator (such as R for resistor or C for capacitor).

3. In the same cell, replace 00000 with the 5 digit number that is generated in the Index column after step 17

4. Fill in the Manufacturer Part Number and Supplier Part Number 1 columns by copy-and-pasting these values from the vendor web page. The Supplier Part Number should be the internal part number used by the vendor. This is (usually) different from the Manufacturer Part Number. For Digi-key, this number ends with -ND. If possible, use Digi-key for Supplier 1. If the component is not available from Digi-key, use the most convenient vendor instead.

`TODO` More information about suppliers

5. If possible, find a second vendor for the component and enter that vendors name and their part number for the component under the Supplier Part Number 2 and Supplier 2 columns. This allows quick substitutions incase the component becomes out of stock at one vendor but not the other. If possible, use Mouser as Supplier 2. Octopart.com is a convenient tool for finding vendors for a component.

6. If the component has a generic symbol (such as resistors, capacitors, inductors, etc.) enter SCH_libs\Miscellaneous Devices.SchLib in the Library Path column. If the component requires a custom symbol, replace Miscellaneous Devices with the name of the component manufacturer


`TODO` Background about symbols and footprints

7. In the Library Ref column, enter a unique identifier such as the Manufacturer Part Number. In some cases, a series of components may use exactly the same symbol. In these cases you may use a more general identifier (such as the first half of the Manufacturer Part Number), but ensure that it will not conflict with other components or cause confusion in the future. If has a generic symbol (such as resistors, capacitors, inductors, etc.), open the Miscellaneous Devices.SchLib in the libraries\SCH_libs folder in the SVN repository and find a suitable symbol. For polar components or components with more than 2 pins, ensure the pin numbers are correct. If you can not find a suitable symbol, create a custom one. If pin numbers is the only problem, copy paste the symbol to the custom symbol and modify the pin numbers. 

8. In the Footprint Ref column, enter an identifier with the prefix XXXX- where XXXX is replaced with the manufacturer abbreviation used in the Index and Part Number columns. After the prefix, enter a unique identifier for the component footprint. If the manufacturer has a size code or something similar in the component datasheet, use that value

9. In the PackageReference column, enter a human readable identifier for the footprint type, such as 8-WFDFN Exposed Pad. This will help when selecting components to add to the schematic.

`TODO` Discuss IPC wizard

10. In the PackageDescription column, enter a brief but detailed text string describing the package. If the component footprint is created using the IPC footprint wizard, use the automatically generated Footprint Description value.

11. In the Description column, copy paste the component description from the vendor's website. If this value is not available or is not appropriate, enter a brief text string describing the component

12. In the Supplier Link column, enter the URL to the product page from Supplier 1

13. In the Comment column, enter the name of the name of the product series such as INA220. Make this value descriptive so someone reviewing the schematic could locate the same or similar component, but try to keep the value short (6 to 10 letters)

14. In the remaining columns, fill in technical details where applicable. If appropriate, add new columns using Clock to Add > Short Text.

15. Save AlbertaSat.mdb in Microsoft Access and close Microsoft Access. Right click AlbertaSat.mdb in the libraries folder of the SVN repository and select SVN Commit. Click OK on the window that appears.

<a name="header03_02_02"></a>
#### 3.2.2 Creating a Schematic Symbol

`TODO` Add content here

<a name="header03_02_03"></a>
#### 3.2.3 Creating a Footprint

`TODO` Add content here

<a name="header04"></a>
## 4. How to Edit this document

This document was created in Markdown. The source file is stored in the SVN repository as `tutorial/tutorial.md`. Before editing, please contact (sdamkjar@ualberta.ca). 

Markdown is a plain-text formatting syntax. It allows you write documents in plain text, readable by others in plain text, and optionally rendered into nicely formatted HTML (like this tutorial). A quick reference for markdown syntax can be found here:

<blockquote style="background-color: rgba(27,31,35,.05);border-radius: 5px;font-size: 100%;margin: 0;padding: 1em 1em; text-align:center;" >    
    <a target="_blank" href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet">https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet</a>
</blockquote><p></p>

To convert the file to html, use the build system included with the 'MarkdownPreview' package in 'Sublime Text'.

Make sure to commit your changes like you would for anything you edit in the SVN repository. Changes can always be reverted as long as an earlier version exists in the repository.

<a name="headerA"></a>
## Appendix A - Manufacturer Abbreviations

`TODO` Finish creating this list

| Manufacturer                | Abbreviation |
| -------------------------   | ------------ |
| Abracon LLC                 | AB           |
| Allegro MicroSystems        |              |
| Alliance Memory             |              |
| Alpha Omega                 | AO           |
| American Technical Ceramics |              |
| Amphenol                    |              |
| Analog Devices              |              |
| Anaren                      |              |
| Asix Electronics            |              |
| AVX Corporation             | AVX          |
| Azurspace                   |              |
| Bourns                      | BRN          |
| Broadcom                    |              |
| BK Precision                | BK           |
| CK Switches                 |              |
| Cmosis                      |              |
| Coilcraft                   |              |
| Connor Winfield             |              |
| CTS-Frequency Controls      | CTS          |
| CUI                         |              |
| Diodes Incorporated         | DIOD         |
| Energy Micro                | EM           |
| FTDI                        |              |
| Fujitsu                     |              |
| Grayhill                    |              |
| Hamamatsu                   |              |
| Harwin Incorporated         |              |
| Hillcrest Laboratories      |              |
| Hirose Electric             |              |
| Honeywell                   | HMC          |
| Infineon                    |              |
| Intel                       |              |
| International Rectifier     | IR           |
| ISSI                        |              |
| IXYS                        |              |
| Johanson Technology Inc     |              |
| JST                         | JST          |
| Kemet                       | KEM          |
| Keystone                    | KS           |
| Linear Technology           | LT           |
| Linx Technology Inc         |              |
| Maxim Integrated            | MAX          |
| Memory Protection Devices   | MPD          |
| Microchip                   | MTC          |
| Microsemi                   | uSEM         |
| Mill-Max Manufacturing      |              |
| Mini Circuits               |              |
| Molex                       |              |
| Murata                      | MUR          |
| Nanolog                     |              |
| NDK America                 |              |
| Nexperia                    |              |
| NXP Semiconductors          | NXP          |
| Ohmite                      | OHM          |
| ON Semiconductor            |              |
| On Shore Technology         | OST          |
| Orbtronic                   |              |
| Panasonic                   | PANA         |
| Phoenix Contact             |              |
| PUI Audio                   | PUI          |
| Qorvo                       |              |
| Richtek                     |              |
| Riedon                      |              |
| Rohm Semiconductors         |              |
| Samtec                      | SAM          |
| Seiko Instruments           | SKI          |
| SII Semiconductors          | SII          |
| Silicon Labs                |              |
| Silonex                     |              |
| SkyWorks                    |              |
| Sparkfun                    |              |
| Spectrolab                  |              |
| STMicroelectronics          | STM          |
| Sullings                    |              |
| Susumu                      |              |
| Taiyo Yuden                 | TY           |
| TDK Corporation             | TDK          |
| TE Connectivity             | TEC          |
| Teensy                      |              |
| Texas Instruments           | TI           |
| Toshiba                     |              |
| Trenz Electronic            |              |
| TT Electronics              |              |
| Vishay                      | VSH          |
| Wurth Elecronics            | WL           |
| Xilinx                      |              |

<a name="headerB"></a>
## Appendix B - Acronyms

Mouse-over acronyms shown in <a style="color: purple;">purple</a> to see the definition.

`TODO` Create a table of acronym definitions

 <!-- Trigger the Modal -->
<img id="myImg" src="https://www.w3schools.com/howto/img_snow.jpg" alt="Snow">
<div id="myModal" class="modal"><span class="close">&times;</span><img class="modal-content" id="img02"><div id="caption"></div></div> 

<style>

body {font-family: Arial, Helvetica, sans-serif;}

#myImg {  border-radius: 5px;  cursor: pointer;  transition: 0.3s; }

#myImg:hover {opacity: 0.7;}

/* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  padding-top: 100px; /* Location of the box */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.9); /* Black w/ opacity */
}

/* Modal Content (image) */
.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
}

/* Caption of Modal Image */
#caption {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
  text-align: center;
  color: #ccc;
  padding: 10px 0;
  height: 150px;
}

/* Add Animation */
.modal-content, #caption {  
  -webkit-animation-name: zoom;
  -webkit-animation-duration: 0.6s;
  animation-name: zoom;
  animation-duration: 0.6s;
}

@-webkit-keyframes zoom {
  from {-webkit-transform:scale(0)} 
  to {-webkit-transform:scale(1)}
}

@keyframes zoom {
  from {transform:scale(0)} 
  to {transform:scale(1)}
}

/* The Close Button */
.close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

/* 100% Image Width on Smaller Screens */
@media only screen and (max-width: 700px){
  .modal-content {
    width: 100%;
  }
}
</style>

<script>
  
// Get the modal
var modal = document.getElementById('myModal');

// Get the image and insert it inside the modal - use its "alt" text as a caption
var img = document.getElementById('myImg');
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
  modal.style.display = "block";
  modalImg.src = this.src;
  captionText.innerHTML = this.alt;
}

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
  modal.style.display = "none";
}
</script>