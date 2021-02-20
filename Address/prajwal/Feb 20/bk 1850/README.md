Instructions for cleaning BK 1850 (the same instructions are also valid for MN 1850 and MN 1880)-

1) All code is in the ‘lib’ folder. Code for cleaning the address 2 column is found in the ‘address 2/lib’ folder.
2) All data files are in the ‘data’ folders. The ‘data2’ folder within the ‘address2’ folder contains the data from the second time I ran the workflow to clean address2.
3) The workflow should be run in the order that the files are named in, i.e. 	
00_remove special characters.ipynb, 
01_doubt-Copy1.ipynb, 
01.5_code for address 2.ipynb, 
02_CRF_1880-Copy2.ipynb, 
03_Final_Output_1880.ipynb, 
04_address_standarization_code-Copy1.ipynb, 
05_combine-new3.ipynb, 
06_Street clean.ipynb, 
07_before address builder-Copy1.ipynb, 
08_Address Builder.Rmd,
09_after running workflow.ipynb, 
10_Street clean - rerun.ipynb,
11_Address Builder copy.Rmd

Be sure to track the names of the files that are being written at each step so that the next step can take the proper file as its input. I may have changed the names of the CSV’s that are being written after each step to something other than what the files in the ‘data’ are named, so please modify the names of the CSV’s according to your own naming scheme.

4) The following files should be run in google colab:
02_CRF_1880-Copy2.ipynb
04_address_standarization_code-Copy1.ipynb
06_Street clean.ipynb
10_Street clean - rerun.ipynb

5) The file 05_combine-new3.ipynb takes 3 files as input, be sure to properly set these before running the notebook. The 3 files are-
df1: The output from 04_address_standarization_code-Copy1.ipynb
d: The .pkl output file from 02_CRF_1880-Copy2.ipynb
df1_original: The output from 01_doubt-Copy1.ipynb

6) Before running 10_Street clean - rerun.ipynb make sure to rename the columns of the output file from the previous step to ‘hn_1’ and ‘best_match’. Also be sure to uncomment any lines that prevent the output from being generated (I may have commented out the last line in the notebook for debugging purposes).

7) A brief description of the notebooks are as follows:

00_remove special characters.ipynb

Removes special characters and typing mistakes from the address and creates columns that are necessary to extract address2. Takes the output from tesseract as its input (BK_1850_final_output_tesseract.csv).

01_doubt-Copy1.ipynb

Removes more typing mistakes and adds functionality for near and corner cases

01.5_code for address 2.ipynb
2.
Creates the input for the address2 folder

02_CRF_1880-Copy2.ipynb, 03_Final_Output_1880.ipynb, 04_address_standarization_code-Copy1.ipynb

Uses NLP to split the address into multiple columns

05_combine-new3.ipynb

Merges the NLP output from the 3 files in the above step with the output for the near and corner cases from 01_doubt-Copy1.ipynb to create one CSV with all columns generated so far

06_Street clean.ipynb

Uses the Street cleaning R code to standardize street names

07_before address builder-Copy1.ipynb

Combines the data in all the columns into 2 columns (hn_1 and best_match) for the address builder

08_Address Builder.Rmd

Address builder for the geocoder

09_after running workflow.ipynb

Replaces occurrences of nan’s in the address builder’s output and changes instances like ‘255 255 Fulton’ to ‘255 Fulton’. Takes the output from 08_Address Builder.Rmd and 03_Final_Output_1880.ipynb as its input (be sure to point to the correct file names).

10_Street clean - rerun.ipynb

Running the street clean code again for the address builder step that is next

11_Address Builder copy.Rmd

Final instance of running the address builder

8) The steps for cleaning address 2 are the same, except you start with the output generated from 01.5_code for address 2.ipynb. Code for cleaning address2 is in the address2/lib folder.
