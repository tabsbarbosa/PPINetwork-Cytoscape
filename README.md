# Introductory guide to Cytoscape

In this tutorial we are going to learn how to create a Protein-Protein Interaction Network in Cytoscape from a matrix of data which contains in Column A and Column B a list of proteins interacting with each other, and in a third column an interaction score between these proteins.

## Requirements
+ Cytoscape v3.8.2 or more recent.
+ Input file: T1T2T3-interacting-with-T4.xlsx

### Network Creation
1. In order to create a network from scratch from an .csv or .xlsx file we are going to use the function _Import Network from File_ or using Ctrl + L
2. In the pop-up window we are going to select the saved file, in this case T1T2T3-interacting-with-T4.xlsx.
3. Now we get a preview of the file we selected, in this moment is important to asign to each column the type of information that can be found there by clicking the name of each column and selecting the attribute. Taking into consideration that the file we are using contains undirected interaction between proteins, it does not matter if column A or B, containging a list of proteins is the Target Node or the Source Node. After this selection, we click OK.

<img src=".\media\1.png" style="zoom:60%;" />

### Data Enrichment from Uniprot Database and Modification of Network Style 
Now the resulting network has a predetermined style, ans should look like this:

<img src=".\media\2.png" style="zoom:60%;" />


Now we are going to change the style of the nwtwork according to new variables, for which we are going to make an enrichment from Uniprot Database using the Retrieve/ID mapping tool (https://www.uniprot.org/uploadlists/). Once you paste the list of proteins that you want to analyze, click on submit. At this point you can choose which information you want in your enrichment using the tool _Columns_ and checking those variables that you want to include.

<img src=".\media\3.png" style="zoom:60%;" />

You can dowload the results as an uncompressed Excel file. This file will be load into Cytoscape following these steps: _File > Import > Table from File_ and selecting the file with the enrichment information obtained from Uniprot. Now, in the pop-up window you can have a pre-visualization of the table. In this step it is important to set as a Key Column from the network "shared name"

<img src=".\media\pic3.png" style="zoom:60%;" />

## Network visualization

Customizing the style of the network can make it easier to identify nodes based on certain variables that are of interest. For this, colors, shapes or sizes can be assigned to the nodes of the network by assigning discrete or continuous variables recorded in the nodes table.

<img src=".\media\pic4.png" style="zoom:60%;" />

Cytoscape offers multiple default styles, those described as size_rank have the particularity of being able to set size ranges for nodes from a column of the nodes table.After choosing size_rank as style, in node properties there is the Size category. By double clicking you can choose the column that will be reflected in the size of the node (in this case Target Score), the type of mapping that will be done, whether continuous or discrete, and a graph that indicates the minimum and maximum size of the node.

<img src=".\media\pic5.png" style="zoom:60%;" />
 
To define the color define the color of the nodes according to some characteristic, initially the column of interest is chosen, in this case Target group, the type of mapping either continuous or discrete. Finally, for discrete mapping, the color is chosen for each group.

## Apps installation and use
Using the Apps > App Manager path, the installation and control menu for the apps offered by Cytoscape is opened. In this menu you will find information on all the apps that can be used for various functions or analyses. Depending on the Tag or label that each app has, you can find folders compiling similar apps. A brief description of the selected app is displayed in the right panel. From this panel you can install these apps, and review the complete documentation available on the Cytoscape page using the View on App Store button (http://apps.cytoscape.org/).

<img src=".\media\pic6.png" style="zoom:60%;" />
