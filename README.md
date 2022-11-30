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
4. [ ]Correlation between columns
5. [ ] PowerBi format input
6. [ ] PowerBi format output

## Process

* This project was developed as part of the EY-GDS Hackpions 4.0, where I was runner-up.
* This hack consists of extracting tabular data from pdf files, images (containing snapshots of excel spreadsheets), XML, and image tables in pdfs, and storing it in SQL or CSV files.
* Among the libraries used in this application are OpenCV (image extraction), Pandas, openpyxl (from XML), sqlalchemy (for storing data), Kraken (for detecting objects in images), and Camelot (for retrieving tables from PDF files).
* In Step 1, the file type is determined based on the MIME of the uploaded file after the user uploads it.
* Openpyxl is used to extract table data from XML files and convert it into pandas dataframes.
* A CSV file is directly converted into a data frame.
* In the case of a pdf, Camelot is used to convert it into a data frame.
* There were a few challenges with the image and pdf images of tables, and for table extraction, they could be tabular or non-tabular, like hotel receipts, etc., so I used OpenCV and Kraken to process those.
* binarization-greyscaling-otsu-image dilation-finding contours
* By using the cell names, the user can select the table range.
* Lastly, the data frame is converted to SQL or CSV according to the user's preference.
