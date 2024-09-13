# ЗАДАНИЕ 1
Вывести отсортированный в алфавитном порядке список имен пользователей в файле passwd.   
**РЕШЕНИЯ:**
```bash
grep '.*' /etc/passwd | cut -d: -f1 | sort
```
<img width="733" alt="Screen Shot 2024-09-13 at 1 09 18 AM" src="https://github.com/user-attachments/assets/8c7a6f30-9610-45f1-a7d1-f3fba52ccbd7">

# ЗАДАНИЕ 2

Вывести данные /etc/protocols в отформатированном и отсортированном порядке для 5 наибольших портов, как показано в примере ниже:
<img width="946" alt="Screen Shot 2024-09-13 at 2 24 09 AM" src="https://github.com/user-attachments/assets/8533b94c-da17-4350-9abe-4e5869203e9b">  
**РЕШЕНИЯ:**
```bash
awk '{print $2, $1}' /etc/protocols | sort -nr | head -n 5
```
<img width="729" alt="Screen Shot 2024-09-13 at 1 15 03 AM" src="https://github.com/user-attachments/assets/340d4bc1-de7d-4aa6-bce5-7d8358716722">

# ЗАДАНИЕ 3
Написать программу banner средствами bash для вывода текстов, как в следующем примере (размер баннера должен меняться!):
<img width="964" alt="Screen Shot 2024-09-13 at 2 25 25 AM" src="https://github.com/user-attachments/assets/1ed23bd4-36e0-49b1-8754-4d4df1f458f0">
**РЕШЕНИЯ:**
```bash
 !/bin/bash

text=$*
length=${#text}

for i in $(seq 1 $((length + 2))); do
    line+="-"
done

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"
```
<img width="732" alt="Screen Shot 2024-09-13 at 1 54 37 AM" src="https://github.com/user-attachments/assets/86fc1980-24e5-41cb-abdb-99a0668e4f17">

# ЗАДАНИЕ 4
Написать программу для вывода всех идентификаторов (по правилам C/C++ или Java) в файле (без повторений).  
**РЕШЕНИЯ:**
 ```bash
     #!/bin/bash

text=$*
length=${#text}

for i in $(seq 1 $((length + 2))); do
    line+="-"![Uploading Screen Shot 2024-09-13 at 2.07.15 AM.png…]()

done

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"
```
<img width="658" alt="Screen Shot 2024-09-13 at 2 07 08 AM" src="https://github.com/user-attachments/assets/8bef1c2e-53f9-4ee8-af58-f3f2585588ac">
