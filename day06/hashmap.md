[1] 向hashmap添加，如果原本就有该key的话就value加一：
hashmap.put(key,hashmap.getOrDefault(key,0)+1)
[2] for简写：for (int i : nums1)
[3]toCharArray()
[4] hashmap修改原有的value就直接put(key,new value)
[5] 383：能用数组代替哈希表的，尽量用数组
[6] Collections.sort对list，Arrays.sort对数组
[7] 需要list有初始值：new ArrayList<>(Arrays.asList(x1,x2,x3))
[8] list.add(Arrays.asList(nums[k],nums[i],nums[j]));Arrays.asList把给出的转换为list
[9] 答案超范围（int最大大约是2.1*10的九次方），可以采用long：
long sum=(long)nums[a] + nums[b] + nums[i] + nums[j];