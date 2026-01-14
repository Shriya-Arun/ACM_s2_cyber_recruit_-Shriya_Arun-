Challenge Description : Analyze the html file given and find the hidden flag. 

Analysis : Used grep command to search for flag. Failed. Moved on to investigate the script section as flags can be hidden there and will not hinder the execution. 
Command used - grep "<script>" -A15 find_right_flag.txt ;
grep is used to search for line containing "<script>" and -A15 displays 15 lines following it. 
Found an encoded variable : var noise = "Z29vZC1ub2lzZQ==";
It is a base64 encoded data. Command to decode : echo "Z29vZC1ub2lzZQ==" | base64 --decode
Flag found. 

Final flag : {good-noise}
