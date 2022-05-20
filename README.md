## How to run

* Open [Colab notebook link](https://colab.research.google.com/drive/1GJPdFMjb049-ylHyng_M1MaLtF2R9gOa?usp=sharing)
* Run the first cell for dependencies.
* Upload the files in folder test_files to colab env.
* About Cells
	- First Cell is imports
	- Second Cell are helper functions
	- Third Cell is for image processing
	- Fourth Cell is for data to convert in pandas dataframe and sqlite database as well as pdf, excel, csv parsing tabular data.
	- Fifth Cell is for executing the program
* Execute all the cell one by one.
* On execution of fifth cell it will ask for input from user, enter the filename (should be in same directory, otherwise enter path).
* Upon successful execution *.db would be visible in directory.


## Working steps

1. Identify the file types
	- Extract table data from image
	- three parts
		* table cell detection
		* maintaining row and columns
		* extract data from cell
2. Write functions for basic extraction for simple/common file types. (excel, pdf-text, pdf-images)
3. Need for a flat-table according to user selection
4. Correlation between columns
X. PowerBi format input
X. PowerBi format output
