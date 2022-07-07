Description: To train the GPT-2 model, we need to feed the text of research papers in .txt file format for unformatted text 
as it cannot work on PDF files directly. Thus to extract the text from the PDF files of the papers, we use Apache tika for Python. 
It parsed each PDF and returned its associated metadata and text content. We displayed the metadata on console during runtime and save 
the text content into separate files for each paper. Then to make it more useful for the training process later, 
we combined all the text files into one large text file while also removing lines with sparse and spurious characters 
which are artifacts of PDF parsing due to fancy formatted PDF blocks.

Requirements:
The Python modules used for this are the standard inbuilt os module and the tika module. To install the tika package we used the command:-
pip install tika

Data Sources:
Bik dataset comprising of 210 scientific research paper PDF files

Running the code file named task 2.ipython:
I just run the file cell by cell to directly. The outputs are- 1) Individual text files each corresponding to one research paper PDF. 
2) A combined and cleaned text file for model training purpose.
