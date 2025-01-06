# Approach

1. Download the file and unzip it, we get an extremely huge number of files and directories.
2. `cd` into the first directory and use the command :

   ```bash
   grep -r "pico"
   ```

3. The `-r` in grep is used to search for the particular string in all files and folders recursively.
4. You get the file where the flag is stored, `picoCTF{gr3p_15_m4g1c_ef8790dc}`


