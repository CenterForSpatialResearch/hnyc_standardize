# Objective

# Methodology and approach

- Flagging Columns with 'Brooklyn' or 'Manhattan' only which are the page titles.
- Flagging columns with (refused) entries as names
- Finding titles like Capt. etc and moving them to titles
- Looking for numbers in names 


### Similar 

- Finally using the Split names to reconstruct the Full name 
- 

| Character 	| Count of Instances 	|                   Example Value                  	|                    Trend/Pattern                   	|                                       Method/Approach                                        	|
|:---------:	|:------------------:	|:------------------------------------------------:	|:--------------------------------------------------:	|:--------------------------------------------------------------------------------------------:	|
| (refused) 	|         21         	|                Pinteaux (refused)                	|              Mostly occurs in FN or LN             	| Flag it, but keep it                                                                         	|
|     M*    	|         54         	|                                                  	|                                                    	|                                                                                              	|
|     M'    	|        1518        	|                                                  	|                                                    	|                                                                                              	|
|     *     	|         90         	|               -*, M*Gunnelly James               	|                 Mosty occurs in LN                 	|                   If in FN then replace, if in LN find suitable replacement                  	|
|   â€”â€   	|         76         	|   â€”_â€”â€”= , M Dermot â€”â€”,Craven â€”â€”    	|                Mostly appears in FN                	|                                                                                              	|
|   [ or ]  	|         45         	|  ler [saac, Conklin W"i]liam N, To]ford William  	|                                                    	|                preceeded or succeeded by 'l' or 't' then replaced and repeated               	|
|   ( or )  	|         68         	| Bannon Danie), Winser Wi)liam,  Cam])bell Thomas 	|                                                    	|                preceeded or succeeded by 'l' or 't' then replaced and repeated               	|
|   { or }  	|         10         	|                                                  	|                                                    	| preceeded or succeeded by 'l' or 't' then replaced and repeated, if in MN or FN then remove, 	|
|     %     	|                    	|                                                  	|                                                    	|                                                                                              	|
|     &     	|        4523        	|     often the first name splitting LN and MN     	| OGG & DELAMATER, Golden & Gormly, Hubbell & Pattee 	| flag it as business                                                                          	|
|     @     	|          7         	|                                                  	|                                                    	|                                            remove                                            	|
|     ?     	|          8         	|                                                  	|                                                    	|                                            remove                                            	|
|     :     	|                    	|          Vandam :, Nassau :., Factory :          	|                                                    	|                        If the only character in first name then remove                       	|
|     ;     	|                    	|                                                  	|                                                    	|                                                                                              	|
|     ^     	|                    	|                                                  	|                                                    	|                                                                                              	|
|     -     	|                    	|                                                  	|                                                    	|                                                                                              	|
|    (Rev   	|         250        	|                                                  	|                                                    	|                                   Move it to title, remove                                   	|
|  (col'd)  	|         35         	|                                                  	|                                                    	|                              Remove the field and add a flag ()                              	|
|     jr    	|                428 	|                                                  	|                                                    	|                                                                                              	|
| Capt.     	|                 13 	|                                                  	|                                                    	|                                      use it as a title                                       	|
| van       	|                893 	|                                                  	|                                                    	|                                                                                              	|


# Input Files and Source

# Intermediary Files

# Output Files

# Summary of Objective Achieved

# Repo Map

# How to use the Outcomes?

# What can be done next? 
