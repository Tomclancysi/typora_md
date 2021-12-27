shell

- 按时间删除老文件：ls -lrt ./ | awk '{print $9}'| head -n 20000 | xargs rm   ls -lt按新到旧
- 

