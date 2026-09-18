# Analysis-of-calcium-imaging-data
R code used in "Mycobacterial Phenolic Glycolipid Triggers ATP-Mediated Neuronal Signaling and Cough" for analysis of calcium imaging data. 
Description
The purpose of this project is to determine change in fluorescence data from neuronal cells stimulated with various compounds or bacterial lipid extracts. The input data are raw ratios from MetaFluor calcium imaging software (version 7.10.5.476) on an Olympus IX73 microscope. The code is designed to analyze 10 plates (or sheets) of calcium imaging data and up to 5 compounds per plate and generates an output file for Max dF/F0 values.


Getting Started:


Dependencies:


R


R studio


readxl package


writexl package


Installing:
download R package and R studio onto computer based on operating system


Executing program:

Create matrices for each group: baseline and treatment 1-5 using the first cell (top left) of the raw data excel sheet and the last cell (bottom right).


Input matrices into R studio using readxl function. Uncheck "first row as names". ensure "Name" matches the code exactly. ex: plate1baseline. Input range of the matrices generated for each group.


Copy and paste entire code into R studio console
Remove any parameters from the code which are not included in the raw data file. ex: if only 3 treatment groups are tested, remove "plate1fourth" and "plate1fifth" etc.


Add the location for saving the analysis file and run the code


Analysis file will be generated for each plate of the raw data


The analyzed matrix is organized as:


F/F0 (fluorescence of cell/baseline of the same cell) for each time point (in seconds)


Max F/F0 (maximum F/F0 value of that cell in the tested time period)


average of last 10 values for treatment group to establish new baseline


MaxdF/F0 (maximum F/F0 value of treatment- maximum F/F0 value of vehicle control)

Authors:
Code written by Christopher Xavier

