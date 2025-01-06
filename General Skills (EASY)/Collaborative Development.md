# Approach

1. Download the challenge file and unzip it.
2. You will see the start and end of the directories unzipped, let's go to the end to check the feature file.

   ![image](https://github.com/user-attachments/assets/eb39eb5b-0220-4b9d-bbfb-5ffa665766f4)


3. From the challenge, we see that `git checkout` command is going to help us get the flag, when we `cat` the feature, we see the following image :

   ![image](https://github.com/user-attachments/assets/663f245f-575f-479f-9573-b28ce1de647f)


4. Copy the id for every commit and use `git checkout` in the initial `drop-in` directory.

5. You will then get an updated flag.py for every checkout you do, join the words to get the flag.


# Notes

1. The `git checkout` command won't work if you're not specifically in the drop-in directory.
