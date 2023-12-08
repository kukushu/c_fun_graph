## 生成c函数调用关系图
```shell
sudo apt install cflow
sudo cp tree2dotx /usr/bin/
find . -name "*.c" | xargs cflow | tree2dotx > out.dot
xdot out.dot
awk !seen[$0]++ out.dot   #no repeat
```

tree3dotx 文件中filterstr用来指定要剔除的函数比如printf
