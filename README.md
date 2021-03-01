# NCU_linux_project2  
**加入wait queue進到kernel**  

enter_wait_queue.c(System code)  
在全域變數使用巨集 Declare_Wait_queue_head 宣告wait_queue的head  
設定flag為wait queue的wake up function  
![image](https://github.com/fallantbell/NCU_linux_project2/blob/main/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202021-03-01%20193836.png)  

clean_wait_queue.c(System code)  
將flag設為true  
並用wake up函式去將wait queue裡面的process叫醒  
![image](https://github.com/fallantbell/NCU_linux_project2/blob/main/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202021-03-01%20194437.png)  


執行程式後  
用ctrl z暫停  
然後用bg放到背景繼續執行  
用ps -t檢查每個process 的status  
可以看到STAT 為S  
代表TASK_INTERRUPTIBLE的睡眠狀態  

