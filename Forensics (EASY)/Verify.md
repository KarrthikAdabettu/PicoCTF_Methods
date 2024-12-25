# Approach

1. As mentioned in the challenge, use the command `ssh -p 53114 ctf-player@rhea.picoctf.net` to open the challenge space, then use the password provided.
2. You will get the following files: `checksum.txt`, `decrypt.sh`, and `files`.
3. First:
    - Use the `cat` command on the `checksum.txt` file and verify if the checksum ID matches the one provided in the challenge menu. If it matches, then the work is almost done.
    - If the checksum doesn't match, use the command `sha256sum *` to get the hash of all files in the `files` folder. This will produce a huge list, but no need to panic.
    - Use the `grep` command to filter for the specific hash you're looking for. For example in my case:
      
      ```bash
      sha256sum * | grep '3ad37ed6c5ab81d31e4c94ae611e0adf2e9e3e6bee55804ebc7f386283e366a4'
      ```
      After this, you'll see the hash with its associated file. For instance:
      
      ```
      3ad37ed6c5ab81d31e4c94ae611e0adf2e9e3e6bee55804ebc7f386283e366a4  e018b574
      ```

4. Now we have the file `e018b574` with its associated hash. Simply decrypt the file using the command given in the challenge menu. You will get the flag:  `picoCTF{trust_but_verify_e018b574}`

## Note
Make sure to use `sha256sum *` in the "files" folder, not anywhere else.   
