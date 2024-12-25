# Approach

1. Use `wget` to download the file, then open it. Here we get the second part of the flag, so copy it and keep it aside.
2. According to the hint, opening the file in different ways can yield a new result. For this, use the `mv` command.
3. The `mv` command changes the format of the file into another file type. For example:

   ```bash
   mv flag2of2-final.pdf flag2of2-final.txt
   ```

  This converts the file from a PDF to a TXT file.
  
4. After running `cat` on the TXT file, the flag was still not visible. Noticing that it was supposed to be a PNG file, I used the command:

  ```bash
  mv flag2of2-final.txt flag2of2-final.png
  ```
This converted the file to a PNG format. 

5. Opening the PNG file provided the first part of the flag. Combining it with the previous part of the flag gives the full flag:  `picoCTF{f1u3n7_1n_pn9_&_pdf_724b1287}`


# Note

A tool named `tesseract` can be used to extract text from an image file. However, in most cases, it provides incorrect output. It is better to manually type the text in such scenarios.
