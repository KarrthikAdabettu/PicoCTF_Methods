# Approach

1. Download the challenge file and unzip it.
2. You will see the start and end of the directories unzipped, let's go to the end to check the master file.

   ![image](https://github.com/user-attachments/assets/024df1c1-9e4d-4fee-8446-85c4aa795fae)

3. From the challenge, we see that `git checkout` command is going to help us get the flag, when we `cat` the master, we see the following image :

   ![image](https://github.com/user-attachments/assets/4c421333-7ab2-4b97-9599-77c28ffb49c3)

4. Copy the id for the create flag and go back to the initial `drop-in` directory and use the follwoing command :

     ```bash
     git checkout 7d3aa557ff7ba7d116badaf5307761efb3622249
     ```

5. You will then get an updated message.txt file which contains the flag, `picoCTF{s@n1t1z3_be3dd3da}`
