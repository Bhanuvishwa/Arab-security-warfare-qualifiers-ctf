# Description;
  Type : forensics
  Name : meownetwork
  Descreption : A hacker managed to get into meownetwork and leaked sensitive files of their  respected baord members. The hacker uses ancient floppy disk technology, however our security team managed to get a disk image of the files he leaked. Can you find out what really leaked?
  Points : 300
  
# Solution:
  We were given an image file after mounting it we will get 5 jpg files.
  In these 5 pics after using basic tools I used **steghide** with "empty password" which gave me not_the_flag_1.txt
  Same was happening for other pics except for one.
  
  After looking at the extracted data I got to know it's base64 encoded. But the question is we were not able to get that for one of the pics.
  The pic which gave no result is the pic of group of cats and in the description it's mentioned that the data of respected board members were leaked we have data extracted data from pics of all board members and this is group pic.
  So there might be not point on bothering about that pic. 
  As the extracted is data is long.I thought it would some file encoded in base64.
  
  Now after decoding and forming back into a file we get an image of a cat.
  Lets try all the tools on it So that we can get any important data. When **steghide** is used it says "Cannot extract any data with this passphrase".
  So we can try using other tools to get password. Finally, nothing was useful this way.
  
  So we can bruteforce to find password using **stegcracker** with any details.
  After cracking it we get a file again which has the flag.
  FLag is: **ASCWG{F10ppy_d1$k!!_th@t'$_s0m3_n0$t@1g!a_stuFF}**.
