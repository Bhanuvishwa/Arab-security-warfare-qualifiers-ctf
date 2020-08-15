# Description;
Type : Forensics
Name : Finger Print
Descreption : Can You Spoof My Finger Print ???
Points : 300

# Solution;
  In this Challenge we were given 6 jpgs and pngs.
  As it was a level-1 chall we tried starting from basic tools on all tools.
  We can observe some data when **strings** or **xxd** applied. The data will be at end of everything.
  The base64 data is:
      .....NTI2MTcyMjExQTA3MDEwMDg1QTg2MkI0MjEwNDAwMDAwMTBGQkRDN0NEMTc3Q0RFQjAwN0VGOTA0
      OEI2NUQwNDE4OEQzRTRDQkU0MTJGOTNFMTkzNzg5QkIyQTBBMTIxQkEwREIwQUQzRDE5ODJDM0NC
      RkIzNEUzQUNDRjE5RkE1MTAwNDY3Qjk0RTMxNkQyN0Y2RUM5OTJCQzUxMkYwMDM3RkFFRTI5RUVG
      RkY4QkE5QzdEMjYzN0FCMTk3NDMwRUEyQjlCNjAyQjBGMkVDRTY4NUM3OUNFM0Y5QTIzODNCMDlG
      NjlDQjk3QjkwNkI3RTQxQzc3NUNFRTkzREZERjNFRDUwMkM0RDZEOUI1MkM0REI2ODE5NEM5MkI3
      NTg3NTVFMDZGODc0ODIyRDgxNEFEMTY5OEYzM0ExM0ZCMzM1Q0JFMjA4ODBBOEI3RTRFNEI2MjQ1
      OUU0QzEwNjZGRTMwQUJEMUJFNjQxRjJERTVFNkU4QTE2OTkwOURGMzJBRDBDQUUwRjg0NzE5NTdE
      ODBFMTY4QkYzN0M4OTYyQUNEREUxNEM4NUJGN0EzRDYyRUNGMTE0NEFGMTEzODBFQkExNzg1ODVF
      MjJEMDQwNjRCQjlBM0EyOTQxMTM3MUVERDUwRjdCOTA0RjY1MDAzODI1MDY1MDQ3MTU2Mjk0QkE0
      OTQ2OEUyOEVGODMzMThEMTJGNzUxQjc2QUY1Cg==
  After decoding this data we get hex data:
      526172211A07010085A862B421040000010FBDC7CD177CDEB007EF9048B65D04188D3E4CBE412F93E193789BB2A0A121BA0DB0AD3D1982C3CBFB34E3ACCF19FA5100467B94E316D27F6EC992BC512F0037FAEE29EEFFF8BA9C7D2637AB197430EA2B9B602B0F2ECE685C79CE3F9A2383B09F69CB97B906B7E41C775CEE93DFDF3ED502C4D6D9B52C4DB68194C92B758755E06F874822D814AD1698F33A13FB335CBE20880A8B7E4E4B62459E4C1066FE30ABD1BE641F2DE5E6E8A169909DF32AD0CAE0F8471957D80E168BF37C8962ACDDE14C85BF7A3D62ECF1144AF11380EBA178585E22D04064BB9A3A29411371EDD50F7B904F65003825065047156294BA49468E28EF83318D12F751B76AF5
  Again after decoding hex data we see:   
      Rar!�¨b´!��½ÇÍ|Þ°ïH¶]>L¾A/áx² ¡!º
      °­=ÃËû4ã¬ÏúQ�F{ãÒnÉ¼Q/�7úî)îÿøº}&7«t0ê+`+.Îh\yÎ?#°iË¹·äw\îßß>ÕÄÖÙµ,M¶É+uUàoH"Ø­ó:û3\¾ 
      ~NKbELfþ0«Ñ¾d-åæè¡ió*ÐÊàøGWØó|b¬ÝáL¿z=bìñJñë¡xX^"Ð@d»:)AqíÕ{Oe�8%PGbºIF(ï1÷Q·jõ
  Well this is not hex but thing is we can see Rar! at top. So lets try to convert this into file and see;
    We are getting a rar file but it is protected and no where passwords were given.
    Let's try cracking it with **john** then we get the password is "komputer".
    In the rar file we directly get a txt.txt which is the flag.
    Flag is: **ASCWG{F0Ren$ics_I$_FUn_;)}**.
