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
