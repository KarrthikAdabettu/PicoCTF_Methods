# Approach

1. Download the file from the challenge, it's a gzip file so use `gunzip` to extract the file from it.
2. To analyze disk images, the tool named AUTOPSY is the best option, it is a digital forensics tool used to investigate and analyze data from computers, phones, and other storage devices. It's often used by investigators to:

  -Recover Deleted Files
  -Analyze Storage Devices

3. Run the command
   
   ```bash
   sudo autopsy
   ```

   Click on all the default things that are selected and then put in your path where the disk image is stored. In my case it's inside the Desktop of my system.

   ![Screenshot 2024-12-25 201718](https://github.com/user-attachments/assets/06975774-2902-4f3e-bac0-b1493a41547c)

4. After it's running, we see the below screen : 

  ![Screenshot 2024-12-25 201737](https://github.com/user-attachments/assets/0994614e-c468-4fbb-919b-2bb6e6666d69)

5. Check inside the mounts of `/1/` or `/3/`, as the others have RAW file system types. Upon checking the `/3/` directory, we see the below files :

   ![image](https://github.com/user-attachments/assets/07217058-7239-489c-b27a-15a3664bb5c2)


6. The files suggested that `innocuous-file.txt` had something to do with the flag, so I searched for the file name on the left hand search bar, but found no results. I was stuck on this for a while, even googling if innocuous meant something.
7. Turns out the answer was more easier, I just went back to the `/3/` directory, went to KEYWORD SEARCH and typed the file name, then I got the files as shown below :

   ![image](https://github.com/user-attachments/assets/4857c284-59f0-4860-b2bd-2630c51a1a4e)


As we keep checking every file, part of the flag is revealed. After combining all the words, the flag we get is :  `picoCTF{1_533_n4m35_80d24b30}`



## Note

1) Use `sudo autopsy`, as sometimes without `sudo` the tool doesn't work.
2) When we put the path of the disk image, make sure to put the correct path. In my case I first had it inside the picoctf/forensics folder, but for some reason there was an error, so installed it directly on Desktop.

