## 生成c函数调用关系图
```shell
sudo apt install cflow
sudo cp tree2dotx /usr/bin/
find . -name "*.c" | xargs cflow | tree2dotx > out.dot
xdot out.dot
```

tree3dotx 文件中filterstr用来指定要剔除的函数比如printf
