[1] 每次使用cur.next时都要保证cur不为null
[2]  while (cur != null) {
            if (cur.val == val) {
                while (cur != null && cur.val == val) {
                    cur = cur.next;
                }
                pre.next = cur;
            }
            if (cur != null) {
                pre = cur;
                cur = cur.next;

            }

        }
这样两段while嵌套不建议，每次都要保证cur不为null；
建议while(cur.next!=null){
            if(cur.next.val==val){
                cur.next=cur.next.next;
            }
            else cur=cur.next;
        }
能用一段while最好，这样只用判断一次cur不为null
[3] 203:cur表示最近的那个不等于val的节点，每次判断的都是cur.next
[4] 双链表定义时一定要：       head.next=tail;
                             tail.pre=head;