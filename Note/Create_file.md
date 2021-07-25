```
Tạo 10 file (file1.txt, file2.txt...) sử dụng vòng for 
Tìm tất cả các file trong thư mục và ghi vào file log.txt

#!/bin/bash
for (( i=1 ; i<=10 ; i++ ))
do
touch "file$i.txt"
done
a=$(find /root/test_shell -type f -name 'file*.txt')
touch log.txt
echo "$a" > log.txt
echo "Finish!"
```
