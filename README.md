search a snippet with "apples" OR "oranges" characters
E is automatic escaping for "|", just remove to search for a "|"

grep -Erin 'apples|oranges' 

AND operator :
grep -Erin 'apples.*oranges' 

Create some alias in .bash

````sh
#search snippets in snippet database : ouput filename
function ss { grep -Erinl "$1" /Applications/MAMP/htdocs/snippets --exclude-dir=".git"; }

#search and open found snippets in vim
function sso { vim -o $(ss "$1");}

```
     

