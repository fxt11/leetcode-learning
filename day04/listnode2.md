[1] 19：可以用双指针法，让fast和slow指针差n
[2] 交叉链表：https://leetcode.cn/problems/intersection-of-two-linked-lists-lcci/description/
原版：while(!(curA==null&&curB==null)){
            // System.out.println(curA.val);
            // System.out.println(curB.val);
            if(curA==curB){
                result=curA;
                break;
            }
            if(curA==null)curA=headB;
            else curA=curA.next;
            if(curB==null)curB=headA;
            else curB=curB.next;

        }
改进：可以发现while条件和if(curA==curB)有相同部分，其实就是当curA==curB时就跳出循环
    while(curA!=curB){
        curA=curA==null?headB:curA.next;
        curB=curB==null?headA:curB.next;
    }
    return curA
[3] 142:（法一）哈希表遍历，找到第一个重复的；
（法二）通过数学证明，通过fast和slow找到重合点后，再定义一个cur指针从head出发，slow继续以一个单位的速度遍历，当重合时就是答案。
[4] 易错：用fast和slow方法while不能放（slow==fast）因为都是从head出发所以初始一定相等。