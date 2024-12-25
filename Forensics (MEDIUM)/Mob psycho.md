# Approach

1. Download the file from the challenge, according to the hint, we can unzip the apk file we downloaded, go ahead and do that.
2. We get an extremely huge number of files to search from, no need to panic.
3. In many cases, the flag will most likely be stored in a file named "flag", so let us try to search for that.
4. Use the command `find` with the name of the word you want to find, in this case:

   ```bash
   find -name *flag*
   ```

   The result we get is the following : `./res/color/flag.txt`
   
5. Now `cd` to that folder and cat out the `flag.txt`. We see that there is an encoded text, which doesn't look like base64 or base32 text. After some searching, it was a hex encoded text. Use the following command :
   
   ```
   xxd -p -r
   ```

   The xxd -p -r command is used to convert hexadecimal-encoded text back into its raw binary format.
   
   -p: This flag tells xxd to operate in "plain hexdump" mode. It means the input or output will consist of plain hexadecimal text.
   
   -r: This flag stands for "reverse" and is used to convert a hexdump (or hexadecimal text) back into binary data.

7. The flag we get is as follows :  `picoCTF{ax8mC0RU6ve_NX85l4ax8mCl_a3eb5ac2}`



## Note

There is another way to solve this problem with the help of `strings` command, if you're interested in that you can check out other github repositories.
