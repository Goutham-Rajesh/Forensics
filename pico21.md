# Forensics
## 1.information
**use exiftool and we will get a base64 encoded text**
**after decoding we will get** `picoCTF{the_m3tadata_1s_modified}`
## 2.Weird File
* its based on macro executable code embeded in documents
* it will auto process or run when it is opened
* To analyse this type of file first install following tools
* `sudo pip install -U oletools` 
* use this cmd to to extact embeded code `olevba -c weird.docm `
* we can see a base64 encoded text after decoding we get `picoCTF{m4cr0s_r_d4ng3r0us}`
## 3.Matryoshka doll
* its a type of challenge where we need to write shell script or python program to solve
* I'm still learning bash script so based on little knowledge i wrote this :]
 ```
    #!/bin/bash
    for i in {1..10}
    do
	    unzip *.jpg
	    cd base_images
    done
  ```  
* Its basicaly a zip file embeded in a png and inside that zip another png 
* After unzip all of them we get a text file containing flag `picoCTF{4f11048e83ffc7d342a15bd2309b47de}`
## 4.tunn3l v1s10n
## 5.Wireshark doo dooo do doo...
* Its a simple chall so i dont provide the flag just try out 
* I will give methods 
* In wireshark in files click on export html packets
* Where you can see a file containg the flag 
* PS:Actualy i did this chall and delete the file and lazy to re download sorry :\
## 6.MacroHard WeakEdge
* Use binwalk to extract embeded file in it and in hidden text file there is base64 after decoding  
* `picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
