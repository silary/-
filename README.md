# python 2.7
# -*- coding:utf-8 -*-
from random import randint 
b = randint(1,100)
t = 0
c = 0
while True:
   choose = raw_input("(1)继续 或者 (2)退出\n")
   if choose == "1":
    t += 1
	
    print "猜一个1-100之间的数字："
    while True:	
     a = input()
     c += 1
     if a < b:
       print "%d 太小了?" % a
     elif a > b:
        print "%s 太大了?" % a
     else:      	 
	 # 如何将程序统计复原 ？
      print "很好，你猜对了，这局您猜了%s次。"% c
	 #跳出循环
      break 
   if choose == "2" :
	 print "游戏结束！！！"
	 break 
print "感谢您的参与，您总共猜了 %s 轮，平均%.1f 次猜对。" % (t,c/t)
