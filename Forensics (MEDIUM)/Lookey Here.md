# Approach

1. Download the challenge and use `exiftool` to see details.
2. It's a plain txt file with a lot of words to search from.
3. We use the command `grep` to find a particular set of words, the command here is :

   ```bash
   cat anthem.flag.txt| grep "pico"
   ```

4. This gives the line where the flag is present, the flag was :  `picoCTF{gr3p_15_@w3s0m3_4c479940}`
