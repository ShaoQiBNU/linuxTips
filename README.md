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
