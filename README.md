# ND-wrangle 

##  My assigned play - King Lear Play

- Speaker 1 - KENT
- Speaker 2 - ALBANY

### Question asked?

How many times did the two speakers speak?
Also calculate the combined result of the two speakers.

### List all commands used to answer the question. 

```
curl "http://shakespeare.mit.edu/lear/full.html" > input.txt

ls

curl "http://shakespeare.mit.edu/lear/full.html" | sed 's/<\/*[^>]*>//g' > lear.txt

ls

grep "KENT" lear.txt

grep "KENT" lear.txt -c

grep "KENT" lear.txt -c > KENTcount.txt

grep "ALBANY" lear.txt

grep "ALBANY" lear.txt -c

grep "ALBANY" lear.txt -c > ALBANYcount.txt


```

### Tell us the answer




#### Input file:

[input.txt](https://github.com/navyadevineni/nd-wrangle/blob/main/input.txt)

#### Output files:

[]()

