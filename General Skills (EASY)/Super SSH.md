# Approach

1. We need to use `ssh` to login to a remote machine to find the flag.
2. Here is an extremely brief explanation on SSH for anyone new : ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine. It is intended to replace rlogin and rsh, and provide secure encrypted communications between two untrusted hosts over an insecure network.
3. The format to put the details after `ssh` is : `targetusername@targetmachineip -p portnumber`
4. After launching the challenge from the challenge menu, you can get all the details from it.
   
   ![image](https://github.com/user-attachments/assets/59064ccc-e77c-4a98-b5bc-2d93a87dd642)

5. After logging in, you get the flag. 
