# Extract Text from PDF to a CSV list using Python

Overview

  This project provides a Python-based solution to extract text from a PDF document and save the extracted content into a CSV file. The main goal is to automate the process of extracting     structured data, such as company names or other information from a PDF, and converting it into a clean and usable format for further processing or analysis.

Features
  PDF Text Extraction: The program extracts all text from a given PDF file.
  Text Cleaning: It provides basic functionality to clean the extracted text, including removing unwanted rows and keeping only the relevant data.
  CSV Output: After cleaning the data, it converts the list into a CSV format for easy manipulation and storage.
  Error Handling: Includes handling for non-existent indices, preventing crashes when some rows to be dropped aren't found.

Prerequisites

  Before running the script, make sure you have Python 3.x installed along with the following libraries:
  
  pypdf: For extracting text from PDF files.
  pandas: For data manipulation and converting the text into a DataFrame, which is then saved as a CSV file.
  To install the required libraries, you can use pip:
  
    pip install pypdf pandas


Prepare your PDF:

  Place the PDF file you wish to process into the project directory.
  Update the script to point to the correct file name in the PdfReader() method.
  Run the Script:
  For this example I'll be using Money2020_USA_2024_-_Final_Attending_Companies_List.pdf, you can find it in https://us.money2020.com/attend/who-attends?aliId=eyJpIjoiZnMzUmdFYWdralA2Yzd6UyIsInQiOiJUcjFuanZETUVuQ1ZZYml2YzN5ZU93PT0ifQ%253D%253D#2024-attendee-list


How It Works
The script follows these steps:

  Extract Text: The PdfReader from the pypdf library is used to read the PDF file. The text from each page is concatenated into a single string.
  Clean the Data: The extracted text is cleaned by removing the first 4 lines (which may contain headers or unwanted information) and the last 2 lines (which may contain additional instructions or footer content).
  Store in CSV: After cleaning the data, the relevant text (such as company names) is stored in a CSV file. The CSV file is created using the pandas library, with the company names in a single column.
