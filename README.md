# ND-wrangle 

This is an in-class challenge to apply the skills learnt during the class.

##  My assigned play - King Lear Play
Chosen this play from the Tragedy section.
Link to my play : [King Lear](http://shakespeare.mit.edu/lear/full.html)

Told to choose any 2 speakers of individual choice.

The speakers I've chosen from the play are:

###  Speaker 1 
KENT
### Speaker 2 
ALBANY

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

To preview the last 20 lines in lear.txt file 
```
tail -20 lear.txt
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

This command helped me to calculate the combined result of the two speakers
```
paste KENTcount.txt ALBANYcount.txt | awk '{$0=$1+$2}1'
```

The combined result of the two speakers is saved into KASumCount.txt file
```
paste KENTcount.txt ALBANYcount.txt | awk '{$0=$1+$2}1' > KASumCount.txt 
```

### Tell us the answer

Speaker 1, KENT spoke  [154](https://github.com/navyadevineni/nd-wrangle/blob/main/KENTcount.txt) times. Speaker 2, ALBANY spoke [66](https://github.com/navyadevineni/nd-wrangle/blob/main/ALBANYcount.txt) times.


#### Input file:

[input.txt](https://github.com/navyadevineni/nd-wrangle/blob/main/input.txt)

By using stream editor using curl command, redirected a [lear.txt](https://github.com/navyadevineni/nd-wrangle/blob/main/lear.txt) file without any HTML opening and closing tags.

#### Output files:

1. [KENT Count](https://github.com/navyadevineni/nd-wrangle/blob/main/KENTcount.txt)
2. [ALBANY Count](https://github.com/navyadevineni/nd-wrangle/blob/main/ALBANYcount.txt)
3. [KA Count](https://github.com/navyadevineni/nd-wrangle/blob/main/KASumCount.txt)

