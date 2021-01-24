# Forensics
## snow snow 
  * first i search about snow stegnography
  and came to know about whitespace stegnography 
  
  
  * learn about the tool stegsnow used to hide text in a text
  using that i decoded a unreadable string in a flag format
  
  
  * Then i noticed a shift of 8 character to the text 
  using a python program of cipher text i decrypt the text and got the flag 
  
## Detailed View
   * first i used strings file name and tried to grep flag
     but i could'nt find the flag.
     
   * Then i looked at the hint and see "Did you try to look at the data inside the image?"
     then i used exiftool and see a comment of a website
     
   * There is a unreadable text.And Decrypt the text and got the flag
   
## Con-The-Cat
  * first i file command to check the file
  
  * Then i used exiftool and i know that there is some file compressed inside it
  
  * Then i use binwalk tool and see that there is 3 jpeg file compressed inside it
  
  * from wiki.bi0s.in/stegnography/binwalk learned to extract image using carving
    tool dd.
  
  * from that image i got the flag

