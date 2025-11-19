# combinePdfs.py

**Code Analysis: combinePdfs.py**

**Overview**

The `combinePdfs.py` script combines all PDF files in the current working directory into a single PDF file named `allminutes.pdf`.

**Functionality**

1. **PDF File Retrieval**: The script uses the `os` module to list all files in the current directory and filter them to only include files with the `.pdf` extension. The resulting list of PDF files is sorted alphabetically.
2. **PDF Writer Initialization**: A `PdfFileWriter` object is created to write the combined PDF.
3. **PDF Loop**: The script loops through each PDF file in the list:
	* Opens the PDF file in binary read mode (`'rb'`) using `open()` and creates a `PdfFileReader` object to read the file.
	* Loops through all pages (excluding the first page) and:
		+ Retrieves the page object using `getPage(pageNum)`.
		+ Adds the page