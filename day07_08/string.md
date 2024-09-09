[1] https://programmercarl.com/kama54.%E6%9B%BF%E6%8D%A2%E6%95%B0%E5%AD%97.html
要在原数组上替换的只能从后往前替换
[2] charAt
[3] append是stringbuffer的方法，stringbuffer要清零用setLength
[4] string判断是否为空：isEmpty()或者通过length
[5] string不能改变的，如果要修改建议新建stringbuffer
[6] string的题目建议中间过程都用stringbuffer（包括中间定义的函数形参）题目151：第一个函数入参为string，输出为stringbuffer，相当于新定义一个stringbuffer用于中间过程
[7] 反转类题目都可以尝试先整体反转再局部反转是否可以得到答案
[8] stringbuffer的函数setCharAt(位置，需要替换成的char)
[9] 28易错：不要忘记k要归零
[10] KMP算法：
            while(j>0&&needle.charAt(j)!=needle.charAt(i)){
                j=next[j-1];
            }
            if(needle.charAt(j)==needle.charAt(i))
            j++;
            （固定格式）
[11] 459题找规律