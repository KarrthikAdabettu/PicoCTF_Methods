# Approach

1. Use `wget` to download the file. We get a jpg file, but after opening it there isn't anything relevant.
2. I used `exiftool` to check whether I can find any hidden information but nothing again.
3. Looking at the hint, we need to open the file in a hex editor and then search for the flags amongst the binary files.  
4. After opening the file through :
   
   ```bash
   hexeditor garden.jpg
   ```

   I just searched for the flag from the search option provided, as we know the flag starts with "picoCTF" and then found it, but I had a better and easier alternative.
   

5. I instead used `strings` command, which is used to extract readable text from binary files. It scans through a file and displays any sequences of printable characters that appear within the binary data. 
6. The command I used was :

   ```bash
   strings garden.jpg | grep "picoCTF"
   ```

   And this resulted in me getting the line where the flag is present.

7. The flag is :  `picoCTF{more_than_m33ts_the_3y3eBdBd2cc}`


# Note
Even hexeditor works but why do something complicated when we have an easier option?

