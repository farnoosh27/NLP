There are several libraries to work with PDFs and parse them:
* PyPDF2

A Python library designed to handle PDF files. It provides a set of tools and functions that enable reading, modifying, and extracting data from PDF documents. With PyPDF2, you can perform tasks such as combining multiple PDFs, splitting a PDF into sections, extracting text and images, editing content, and encrypting or decrypting PDF files. By utilizing PyPDF2 in your Python programs, you can interact with PDF files programmatically and access their contents and structure.

* PDFplumber
  
A Python library that allows you to extract text, tables, and images from PDF files. It provides convenient methods for accessing and manipulating the content of PDF documents. With PDFplumber, you can extract text, identify and extract tables, manipulate pages, retrieve metadata and page information, and extract embedded images. It is a versatile tool that can be used for various PDF processing tasks, making it a valuable resource for working with PDF files in Python.

* PDFMiner
  
A robust library that enables the extraction of text and metadata from PDF files. It offers tools for analyzing PDF document structure and extracting text in different formats. With support for both layout-based and text-based extraction, PDFMiner is well-suited for a variety of PDF parsing requirements.


```
%pip install pdfminer
import io
from pdfminer.converter import TextConverter
from pdfminer.pdfinterp import PDFResourceManager, PDFPageInterpreter
from pdfminer.pdfpage import PDFPage
import requests
```
and then: 
```

def read_pdf_with_pdfminer(pdf_url):
    resource_manager = PDFResourceManager()
    output_string = io.StringIO()
    laparams = None

    response = requests.get(pdf_url)
    file = io.BytesIO(response.content)

    interpreter = PDFPageInterpreter(resource_manager, TextConverter(resource_manager, output_string, laparams=laparams))
    for page in PDFPage.get_pages(file):
        interpreter.process_page(page)

    return output_string.getvalue()
```
and next using the function:
```
pdf_url = 'https://www.africau.edu/images/default/sample.pdf'
first_page_text_pdfminer = read_pdf_with_pdfminer(pdf_url)
print(first_page_text_pdfminer)
```

* Camelot
  
 Camelot is a Python library built on top of PDFMiner that specializes in table extraction from PDFs. It provides high-level methods to detect and extract tables from PDF documents, even in the presence of complex layouts or merged cells. Camelot supports both text-based and image-based table extraction.

 * Tabula-py
   
   A specialized library that focuses on extracting tabular data from PDF files. It has the ability to automatically detect and extract tables, which can be conveniently saved as CSV or DataFrame objects. Tabula-py utilizes PDFPlumber internally and provides a more abstracted interface for streamlined table extraction tasks.
