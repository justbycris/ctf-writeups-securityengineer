# Search Souce - PicoCTF challenge
At the beginning of the CTF I went through my usual:
1. Inspect
2. View page source code
3. I tried robots.txt file and nothing and all my steps on the list I have for CTFs...
4. I did look at the hint and seeing it said: 'How could you mirror the website on your local machine so you could use more powerful tools for searching?'
5. I figure the word mirror was a cue so I did a google search into what mirroring a website was. **Mirror a Site: is downloading the files of a computer server that has been copied to another computer server.**
6. Then I google search for the command that would get me there: **wget -mkxKE -e robots=off domain**. The **wget** command is used to get files from various web servers.
7. After I have download and mirror the website's files into my VM, I used the command **grep -r pico** to search the flag within the downloaded files.<img width="754" alt="Screenshot 2023-11-12 at 4 43 34 PM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/a629e619-8732-4639-ab8e-94e7bd07e80e">
8. I found the flag at the bottom of the results in the 'index.html' file: picoCTF{1n5p3t0r_0f_h7ml_fd5d57bd} yet when I submit the flag it says is not a valid flag. Weird...
9. I try displaying the 'index.html' file using the cat command and the same flag shows: <img width="621" alt="Screenshot 2023-11-12 at 4 44 22 PM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/fd18eb0d-1012-4a9b-b558-25df0ec921b1">
10. Feeling a bit confused, I decide to go back into the source code and see if I've missed anything. I go through the files and looking into the CSS file I realized I skipped a line that had a different flag on it:<img width="797" alt="Screenshot 2023-11-12 at 4 46 18 PM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/d259b9be-e2ba-4052-bd46-16aa08835628">
11. THAT was the correct flag. 
