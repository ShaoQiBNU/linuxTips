linux相关命令
============

# linux命令大全

http://www.runoob.com/linux/linux-command-manual.html


# 打乱文本文件行顺序

```linux
shuf input.txt -o output.txt

input.txt为输入文件，output.txt为输出文件
```


# 后台运行python脚本

```linux
nohup python -u librosa_mp4.py > librosa_mp4.log 2>&1 &
```

# awk指定分隔符
```shell
cat input.txt | awk -F, '{print $1, $3}' > output.txt

input.txt为输入文件，output.txt为输出文件
```

# sort排序和去重

```shell
sort -k1n,1 -k2n,2 input.txt -o input.txt

按照第一列和第二列数值排序

sort -t $'\t' -n -k1,1 untitled.txt | sort -u -k2,2

按照第一列数值排序，按第二列去重，重复的保留的是第一列数值小的
``` 

# uniq
```linux
uniq -d input.txt > output_repeat.txt

输出input.txt里重复的数据
```




