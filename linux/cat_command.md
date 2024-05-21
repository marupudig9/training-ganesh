Allows us to cut parts of lines from specified files or piped data and print the result to standard output.
<br>Command:
<br>Command:```cut -c1 "file_name" --> List one character```
* eg:
  <br>ganesh
  <br>rajesh
  <br>naresh
  <br>output: g,r,n
  <br>Command: ```cut -c1,3,4 "file_name" --> list multiple characters```
* eg:
  <br>ganesh
  <br>rajesh
  <br>naresh
  <br>output: gne,rje,nre
  <br>Command:```cut -c1-5 "file_name" --> to list data```
* eg:
  <br>ganesh
  <br>rajesh
  <br>naresh
  <br>output: ganes,rajes,nares
  ```Command:cut -d: -f 1 "file_name" - d is a delimeter```
* eg:
  <br> Delimeter is kind of a seperator eg: ganesh:harika "Ganesh is filed1, ':' is delimeter"
  <br> when we give -d: -f 1 we get the value from field 1
  <br> Output: ganesh