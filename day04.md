### 第四天

如果程序报错并且报出错误的位置，你想快速定位到错误行n的话，使用`vi xxx.py +n`即可

#### if-elif

```
if 条件1
    xxxx111
elif 条件2
    xxxx222
elif 条件3
    xxxx333
```
#### 程序的三大执行流程
- 顺序执行
- 选择执行
- 循环执行


##### while
```
num=1
while num<=10:
    num=num+1
    print(num)
```
##### if嵌套
```
if xxx1:
    print("----")
    if xxx2
        print("****")
```

##### while嵌套
```
while 条件:
    条件满足时候做的事情1
    条件满足时候做的事情2
```

##### print打印自动换行
如果想使得print打印不换行`print("*",end="")`即可

##### 自加一
- 别的语言
  - i++
  - ++1
  - i=i+1
  - i+=1
- Python
  - i=i+1
  - i+=1

##### for循环

```
name="itgoyo"

for temp in name:
    print("---")
    print(temp)
```


| 命令     | 含义     |
| :------------- | :------------- |
| not    | 取反       |
