# Advanced Bash Commands
Specific actions on Unix

## Get all running processes
`ps aux | grep <MY_PROCESS>`

`ps` - List process status
  - `a` All users
  - `u` Show user
  - `x` Dead processes
  - `--forest` Visual map

`grep` - Advanced search


## Manipulate file without opening
`sed` or Stream Editor used to find and replace

Usage: `sed <script> <file.txt>`


### Replace text with other text
\<script\> `[-i edit in place] [line#] s/<find>/<replace>/[scope: g or nth occurence]`

`sed s/find_text/replace_text/3 file.txt` Find 'find_text' and replace with 'replace_text', the third occurence in 'file.txt'.  


## Delete text
\<script\> `[line#|$ last line|/pattern/|x,y]d`



`awk`


`sed`
