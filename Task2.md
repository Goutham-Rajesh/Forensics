# Unzip the zip file using fcrackzip
## Bash Tasks
 ## Reverse
    * First i used file command to determine type of file it shows as data.
    * Then i used strings command
    * Then i found a long text in reversed order "}ss3ug_1_gn1sr3ver_t4_d00g_3ra_u0Y{ftcni"
    * Then i reversed the text in word and got the flag "inctf{Y0u_ar3_g00d_4t_rev3rs1ng_1_gu3ss}"
## E_challenge2.jpg
 * First i opened the image got nothing
 * Used exiftool find a comment of base64 encoded txt
 * Decoded the text using command echo "encoded txt" | base64 -d
 * Got the flag "inctf{3x1f700l_15_n1ce_!_gu3ss___!!!!}" :)
## s_challenge2.jpg
 * open the image it was a zebra
 * Then used strings on it
 * Got the flag "inctf{5tr1ng5_4r3_us3ful_1_gu3s5}"
 

 
