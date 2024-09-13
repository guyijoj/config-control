ЗАДАНИЕ 1
grep '.*' /etc/passwd | cut -d: -f1 | sort
<img width="733" alt="Screen Shot 2024-09-13 at 1 09 18 AM" src="https://github.com/user-attachments/assets/8c7a6f30-9610-45f1-a7d1-f3fba52ccbd7">

ЗАДАНИЕ 2
awk '{print $2, $1}' /etc/protocols | sort -nr | head -n 5
<img width="729" alt="Screen Shot 2024-09-13 at 1 15 03 AM" src="https://github.com/user-attachments/assets/340d4bc1-de7d-4aa6-bce5-7d8358716722">

ЗАДАНИЕ 3
 !/bin/bash

text=$*
length=${#text}

for i in $(seq 1 $((length + 2))); do
    line+="-"
done

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"

<img width="732" alt="Screen Shot 2024-09-13 at 1 54 37 AM" src="https://github.com/user-attachments/assets/86fc1980-24e5-41cb-abdb-99a0668e4f17">

