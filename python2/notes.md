# 5/4/2018

### loop though a csv file and save it to another

Put the data with column headers in data.csv and the output will be in rows to write

```python
import csv 
rows_to_write = [] #where each mark is stored 

with open('data.csv') as csvfile:
    csvfile.readline() #skip first line
    for row in csv.reader(csvfile.readlines()):
        rows_to_write.append(row)

#now save the data to csv so it can be imported 
with open("output.csv",'wb') as resultFile:
    wr = csv.writer(resultFile, dialect='excel')
    wr.writerow(['Data','Column','Headers'])
    for item in rows_to_write:
        wr.writerow(item)

```
