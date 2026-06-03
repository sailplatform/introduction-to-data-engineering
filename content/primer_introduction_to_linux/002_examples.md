$$info
title: Assume that you use the folder with files inside as explained below

The examples in this section take the below structure into consideration.

Our directory has a folder named "data" with files data1.txt, data2.txt, ... data9.txt, temp.csv.
Each file has data in the form of:
"THIS is data 1-1 file." --> data1.txt
"THIS is data 2-2 file" --> data2.txt
....
"THIS is data 9-9 file" --> data9.txt

You are assumed to be in the directory where the "data" folder exists
$$

# Sample 1

**Goal:**  To find the files that contains the string "this"

**Command:**
```
grep -i -r this data/*.txt
```

**Output:**
```
data/data1.txt:THIS is data 1-1 file
data/data2.txt:THIS is data 2-2 file
```

# Sample 2

**Goal:**  to list the files ______

**Command:**
```
grep -i -r -l this data/*.txt
```

* `-i` option ignores the case sensitive "this" and looks for all cases.
* `-r` option is required when you want to recursively look into a folder consisting a lot of files.
* `-l` option lists all the filenames from the result.

**Output:**
```
data/data1.txt
data/data2.txt
```


# Sample 3
**Goal:** to count the files that contains the words "this"

**Command:** 
```
grep -i -r -l this data/*.txt | wc -l
```

* `|` is a pipe symbol that takes the output from the left and works on it using the command followed by the symbol. You can add as many pipes as you want as per the requirements of your code.
* `wc -l` counts the number of lines in the output of grep.  

**Output:**
```
100
```

# Sample 4
**Goal:** to find the pattern "<single_digit><any_non_word><single_digit>" in all the files(Example: 9[9 but not 90*90)

**Command:**
```
grep -P -r -l '\b\d{1}[\W]*\d{1}\b' data/*.txt | wc -l
```

**Output:**
```
9
```

$$info
title: Assume that you use the file explained below

./temp.csv file contains the following data:

**id    title                   level**
1     Python2           Beginner
2     Python3           Intermediate
3     Blockchain       Beginner
4     Blockchain2.0  Intermediate


You are assumed to be in the directory where this file exists
$$

# Sample 5
**Goal:** to print all the column(s) in a csv file where **title** contains "Python" and **level** is "Intermediate"

**Command:**
```
awk -F '\t' '$2 ~ /Python/ && $3 == "Intermediate" {print $2}' temp.csv
```

* `-F` option to split values in a line based on the separator.

**Output:**
```
Python3
```

# Sample 6
**Goal:** to replace the pattern "<single_digit><any_non_word><single_digit>" with "\<TEST>" 

**Command:**
```
mkdir anon_data
for file_name in data/*.txt; do
    sed -r 's/\b[0-9]\W*[0-9]\b/<TEST>/gI' "$file_name" > anon_"$file_name";
done
```

**Output:**
```
#Check the files in anon_data directory.
data1.txt -> THIS is data <TEST> file
..
data9.txt -> THIS is data <TEST> file
```
