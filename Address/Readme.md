
# Overview
Latest versions of datasets could be find in the shared google drive folder.

This process identies different components of an address like city, house no, county, street name. 
The process is only setup for 1850 mn cd directory. It identifies the 'H addresses' that either start with 'H' or has an 'H' idenfier in somewhere in the address record. 

### Process:
1. Create functions to identify city, street and county

2. Then City from a list NY, New Jersey and Connecticut cities is identified. 

3. Find if there is a house no just after the 'H' identifier. '.5' is removed in order to correctly identify house numbers

4. It is assumed that street name will exist even if there is no house number. So if unable to find street name from the remaining of the string include the identified house no as well to find the street name

5. While finding the street name: Identify special cases like Corner and Near identifiers where two street names are present instead of one

### Raw dataset inputs (in google drive)
https://drive.google.com/drive/u/3/folders/1BG3cgsQYclFNVrRyYiHogDhxVkc0nr9H

Output csv files from the occupation standarization process

Output_1850_mn

Output_1850_bk

Output_1880

### Scripts 
https://drive.google.com/drive/u/3/folders/1S406pBwdr4usIr1SEmL3yTntHqh3Ts2B

### Output datasets (available in google drive)
https://drive.google.com/drive/u/3/folders/1_BPIfGHIULPVKuLGTklfvbxIMfSBDc8n

### Other working/Intermediate files (in google drive)
https://drive.google.com/drive/u/3/folders/1hjvCURJV5uf9wGYYwXdu6u9hLZGsIN4f
