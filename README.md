# formatting_medical_records
This datapipeline is capable of delaing with csv, json, pkl files
FUTURE SCOPE: Implementation of cosine similarity to remove similar sentences(repeated similar sentences).
 
To run this pipeline, we have to pass path to
data directory as an input :
EXAMPLE : python main.py path_to_data_folder ( python main.py /Users/saigarimella/Downloads/candidate/data)
This input directory can contain a mixture of individual files and sub directory of files in it, data pipeline is 
designed to handle such casesData pipeline is segregated into multiple files:

main.py -> acts like a control file, goes through each input file path and triggers the preprocessing from here

read_and_write_data.py -> contains functions that read data from file and writes data to same file after preprocessing

remove_unwanted_data.py -> contains functions to remove sequential punctuations, spaces between decimals call reports

transform_data.py -> contains functions that adds ['item'] infront of individual lines/statements in a record, remove 
numbers which doesn't indicate any measurement, to converter dictionary to string and vice verse, and a preprocess 
function that calls other functions.
