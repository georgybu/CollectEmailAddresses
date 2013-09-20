CollectEmailAddresses
=====================

Collect Email Addresses from MBOX and PST

Usage:
------
1. Export your outllok folder to PST file (outlook.pst)

2. Install libpst utils (http://www.five-ten-sg.com/libpst/)

```sh
    user@mac$ brew install libpst --pst2dii --with-python
    user@linux$ sudo apt-get install libpst4
```

3. Convert PST file to MBOX with libpst utils

```sh
    $ cd path/to/outlook.pst
    $ mkdir outlook
    $ readpst -D -b -d ./outlook.log -o ./outlook outlook.pst
    [optional] $ tail -f outlook.log
```
4. Collect all emails with collect_emails_from_mbox.py

```sh
    $ python collect_emails.py -s -d ./outlook
```

Author:
-------

Georgy Bunin
