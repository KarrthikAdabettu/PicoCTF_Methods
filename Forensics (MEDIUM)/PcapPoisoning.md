# Approach

1. Download the file from the challenge, we get a pcap file. Before moving forward, let us see what is a pcap extension.
2. "pcap" - It means PACKET CAPTURE FILE. A PCAP file is like a recording of internet traffic. It saves information about all the messages (packets) that travel
   between computers over a network, like when you visit a website or send a message.
   PCAP file is a special tool for "watching and saving" internet conversations, useful for fixing issues or solving mysteries like how someone hacked into a system.
   
3. To run this, we can use "WIRESHARK", a software tool that helps us in analyzing every single packet inside the file. We can individually keep scrolling through every packet until
   we find the flag, which is extremly time consuming and boring.
4. Instead I used the easier method, use the `strings` command. Even though there are numerous packets, `strings` will give me all the readable data from the file and using `grep`
   will get me the proper line on the flag.

   ```bash
   strings trace.pcap | grep "pico"
   ```
5. We then get the flag :  `picoCTF{P64P_4N4L7S1S_SU55355FUL_f621fa37}`




## Note

If `strings` doesn't work and show the flag, we need to manually use wireshark and analyze where the flag might be, because `strings` always doesn't give the answer.
