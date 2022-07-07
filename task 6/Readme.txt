In the document, we have a folder containing generation_texts from from GPT-2 task 5. and a task_6_info.csv which get the titles and authors information from step 3 and GPT-2(title.txt and author_name.csv). We also have three ipynb files called task-6-info.ipynb, add_txt_to_csv.ipynb and to_pdf.ipynb. In addition, we combined the generation text into the csv file to new_combine.csv. Then used to_pdf.ipynb to change the csv file into a folder of fake pdf files named falsified_media.


Process:
1. Use the title.txt and author_name.csv to combine into a task_6_info.csv using task-6-info.ipynb.
2. get txt from generation_texts to combine txt into task_6_info.csv into new_combine.csv by add_txt_to_csv.ipynb.

new_combine.csv has 500 rows and 3 columns: author, title and text.

3. write to_pdf.ipynb refer to the downloaded paper from step 1 for the paper format and save the papers’ PDFs in a folder called “falsified_media”. 
In the to_pdf.ipynb, I automatically use LaTex to convert texts to PDFs: 
LatexContent = '''\\documentclass{scrartcl}
                        \\usepackage{graphicx}
                        \\begin{document}
                         
    
                            \\section{Title}
                            {\\LARGE %(TL)s}
                            \\section{Author}
                            {\\large authors: %(AT)s}
                                
                            %(Ot)s
                   \\end{document}'''  
                   
4. falsified_media folder comtains the 500 faked pdf which changed from the genered txt, author, and titles.
