linux相关命令
============

# linux命令大全

http://www.runoob.com/linux/linux-command-manual.html


# 打乱文本文件行顺序

```linux
shuf input.txt -o output.txt

input.txt为输入文件，output.txt为输出文件
```


# 后台运行脚本

```linux
nohup python -u librosa_mp4.py > librosa_mp4.log 2>&1 &

nohup sh download_anet_dataset_1.sh 2>&1|tee ./download_anet_dataset_1.sh.log &
```

## 如果程序已经在前台运行，也可以通过以下命令放到后台执行
```
ctrl + z 暂停进程

bg

jobs

disown -h %jobs号
```

# awk指定分隔符
```shell
cat input.txt | awk -F, '{print $1, $3}' > output.txt

input.txt为输入文件，output.txt为输出文件


awk -F '\t' '{sum[$2]++}END{for(i in sum) print i "\t" sum[i]}' all.data

查看all.data中第2列标签个数，类似groupby然后count(*)


awk '$2=="天文"' all.data | head -10

查看all.data中第2列标签为天文的前10行数据


awk -F '\t' '{print substr($5,3)}' all.data | more

all.data中第5列数据，从第3个字符串开始截取到最后，输出

```

# sort排序和去重

```shell
sort -k1n,1 -k2n,2 input.txt -o input.txt

按照第一列和第二列数值排序

sort -t $'\t' -n -k1,1 input.txt | sort -u -k2,2 > output.txt

指定分隔符为\t，按照第一列数值降序排序，按第二列去重，重复的保留的是第一列数值小的
``` 

# uniq
```linux
uniq -d input.txt > output_repeat.txt

输出input.txt里重复的数据
```

# 权限授予
```
chmod -R 777 /ldap_home/qi.shao

777 是读、写、执行权限
```




