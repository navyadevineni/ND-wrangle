# ND-wrangle 

This is an in-class challenge to apply the skills learnt during the class.

##  My assigned play - King Lear Play

- Speaker 1 - KENT
- Speaker 2 - ALBANY

### Question asked?

How many times did the two speakers speak?
Also calculate the combined result of the two speakers.

### List all commands used to answer the question. 

Used 'curl' command to fetch the html file into input.txt file
```
curl "http://shakespeare.mit.edu/lear/full.html" > input.txt
```

To view the list of files in the folder
```
ls
```

To transform text into lear.txt file
```
curl "http://shakespeare.mit.edu/lear/full.html" | sed 's/<\/*[^>]*>//g' > lear.txt
```

To view the list of files in the folder
```
ls
```

To find the match with speaker name 'KENT' in lear.txt file
```
grep "KENT" lear.txt
```

To find the number of times the speaker 'KENT' spoke 
```
grep "KENT" lear.txt -c
```

To redirect the output of the times KENT spoke to a KENTcount.txt
```
grep "KENT" lear.txt -c > KENTcount.txt
```

To find the match with speaker name 'ALBANY' in lear.txt file
```
grep "ALBANY" lear.txt
```

To find the number of times the speaker 'ALBANY' spoke
```
grep "ALBANY" lear.txt -c
```

To redirect the output of the times ALBANY spoke to a ALBANYcount.txt
```
grep "ALBANY" lear.txt -c > ALBANYcount.txt
```

### Tell us the answer




#### Input file:

[input.txt](https://github.com/navyadevineni/nd-wrangle/blob/main/input.txt)

#### Output files:

[]()

