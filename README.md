# PS3-Save-Decrypter
A save decrypter for PS3.  
Download [here](./build/GSecPs3Decrypter.exe). 
 
![demo](./demo/demo.gif)  

Uses games.conf (downloaded from public url). If it doesn't contains info for the game, there might be more comprehesive versions with it.  

_ todo:
- read games.conf from file, not url; 
- fix parsing issue of some versions; 

<details>
  <summary>Changelog</summary>

- ReadConfigFromtext2, auto-releases.  
better games.conf parsing code.  
builds generated in ./build/  

- fix game search algo
match by TitleID.Substring(0,9) or Title  
optimize: only per dir load - new SavMan and key search ; make ps3SaveManager public   
refactor Form1.cs  
switch output to console, add logging.  

- universality fix (1)  
get SecureFileID from games.conf (2) based on titleID from SFO   
Param.SFO -> TitleID-> games.conf -> SecureFileID  
(1) restore and fix cut feature  
(2) downloads if not presented  
minor: add .gitignore

</details>