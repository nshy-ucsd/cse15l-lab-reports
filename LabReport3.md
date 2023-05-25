# Lab Report 3

## Task
> Consider the commands less, find, and grep. Choose one of them. Online, find 4 interesting command-line options or alternate ways to use the command you chose. For example, we saw the -name option for find in class. For each of those options, give 2 examples of using it on files and directories from ./technical. Show each example as a code block that shows the command and its output, and write a sentence or two about what it’s doing and why it’s useful.

## grep -l
searches for a specific pattern in one or more files and outputs the names of the files that contain a match, rather than displaying the matching lines themselves. It is particularly useful when you want to quickly identify the files that contain a specific pattern without displaying the actual content of those files. This option is often combined with other grep options to refine the search.

### example 1
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -l "while," technical/biomed/*.txt
technical/biomed/1471-2105-3-12.txt
technical/biomed/1471-2105-3-6.txt
technical/biomed/1471-2210-2-5.txt
technical/biomed/1471-2229-3-3.txt
technical/biomed/1471-2253-2-5.txt
technical/biomed/1471-2350-4-2.txt
technical/biomed/1472-6904-2-7.txt
technical/biomed/1475-925X-2-3.txt
technical/biomed/gb-2002-3-12-research0077.txt
nicholasshy@MacBook-Air-2 stringsearch-data % 
```
I looked for all files that contain the pattern "while," in the technical/biomed directory, this can be useful to find the filenames of the file that coontain our keyword, whether they are the topic we are looking for or typos we want to correct.

### example 2
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -l "viruses," technical/biomed/*.txt
technical/biomed/1471-2105-2-1.txt
technical/biomed/1471-2105-3-12.txt
technical/biomed/1471-2121-3-22.txt
technical/biomed/1471-213X-3-2.txt
technical/biomed/1471-2148-1-1.txt
technical/biomed/1471-2148-2-12.txt
technical/biomed/1471-2148-3-3.txt
technical/biomed/1471-2164-3-15.txt
technical/biomed/1471-2172-1-1.txt
technical/biomed/1471-2180-1-34.txt
technical/biomed/1471-2180-2-26.txt
technical/biomed/1471-2180-2-29.txt
technical/biomed/1471-2180-3-9.txt
technical/biomed/1471-2202-3-8.txt
technical/biomed/1471-2288-3-9.txt
technical/biomed/1471-230X-2-21.txt
technical/biomed/1471-2334-1-17.txt
technical/biomed/1471-2334-2-27.txt
technical/biomed/1471-2334-2-7.txt
technical/biomed/1471-2334-3-9.txt
technical/biomed/1471-2407-3-4.txt
technical/biomed/1471-2431-2-1.txt
technical/biomed/1471-2458-2-11.txt
technical/biomed/1471-2458-3-5.txt
technical/biomed/1471-2474-2-3.txt
technical/biomed/1472-6807-3-1.txt
technical/biomed/1476-511X-1-2.txt
technical/biomed/ar429.txt
technical/biomed/gb-2001-2-12-research0051.txt
technical/biomed/gb-2002-3-3-research0012.txt
technical/biomed/gb-2003-4-2-r11.txt
```
I looked for all files that contain the pattern "viruses," in the technical/biomed directory, this can be useful to find the filenames of the file that coontain our keyword, whether they are the topic we are looking for or typos we want to correct.

### 

## grep -n
searches for a specific pattern in one or more files and outputs the matching lines along with their line numbers. 

### example 1
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -n "while," technical/biomed/1475-925X-2-3.txt  
271:        inhibitory effect. Meanwhile, the alpha MNs are centrally
```
Since I found that the pattern "while," appeared in the file technical/biomed/1475-925X-2-3.txt, I used this command to find all the line numbers of where "while," appeared in the file. This can be heapful if we want to correct a typo and we know which file contains the typo.

### example 2
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -n "viruses," technical/biomed/gb-2003-4-2-r11.txt
98:        DNA viruses, positive-strand RNA viruses and certain
557:            and animal viruses, with the sole exception of a single
609:            picornaviruses such as human parechoviruses, Aichi
618:            including the forms from RNA viruses, clearly form a
```
Since I found that the pattern "viruses," appeared in the file technical/biomed/gb-2003-4-2-r11.txt, I used this command to find all the line numbers of where "viruses," appeared in the file. This can be heapful if we want to correct a typo and we know which file contains the typo.

## grep -C
Also known as grep --context, allows you to specify the number of lines of context to display before and after each match. It helps provide additional context around the matching lines, making it easier to understand the context in which the pattern occurs.

### example 1
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -C 2 "while," technical/biomed/1475-925X-2-3.txt  
        non-spindle muscle afferents have increased discharge rates
        with increasing fatigue, also contributing to the
        inhibitory effect. Meanwhile, the alpha MNs are centrally
        inhibited by group III and IV muscle afferents, activated
        by the accumulation of metabolites in the fatiguing muscle,
```
Find the specific number of lines (2 lines in this case) before and after all the lines that contain the pattern we give, "while,"(in this case, there is only one line that contain the pattern I provide), within the given file technical/biomed/1475-925X-2-3.txt. This can be useful to look at the surounding of a keyword that we have in mind in a file. 

### example 2
```
nicholasshy@MacBook-Air-2 stringsearch-data % grep -C 2 "viruses," technical/biomed/gb-2003-4-2-r11.txt
        We also show that members of the N1pC superfamily exist
        outside the bacterial superkingdom, in eukaryotes, large
        DNA viruses, positive-strand RNA viruses and certain
        archaea. In eukaryotes, one of the members of this family
        has been studied experimentally, and possesses LRAT
--
            viral particle.
            The LRAT family is thus far found only in eukaryotes
            and animal viruses, with the sole exception of a single
            member from the proteomes of 
            Vibrio cholerae and 
--
            subgroups.
            The viral homologs of H-rev107 were observed in
            picornaviruses such as human parechoviruses, Aichi
            virus and avian encephalomyelitis virus [ 63]. We also
            detected related proteins in human caliciviruses such
--
            that could modify some membrane component, like their
            cellular homologs. All the members of the LRAT family,
            including the forms from RNA viruses, clearly form a
            distinct family which excludes the YaeF/poxvirus G6R
            family, which shows a similar circular permutation. The
```
Find the specific number of lines (2 lines in this case) before and after all the lines that contain the pattern we give, "viruses,"(in this case, there are 4 matching lines that contain the keyword I provided), within the given file technical/biomed/gb-2003-4-2-r11.txt. This can be useful to look at the surounding of a keyword that we have in mind in a file. 


## grep -r
The -r stands for "recursive," and it allows you to search files and directories recursively.

### example 1

### example 2

