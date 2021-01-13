+ 处理器内部数据传输：  
					立即数到寄存器and寄存器到寄存器MOV  
					寄存器到特殊寄存器MRS--S>R(读特殊) MSR--R>S(写特殊)  
+ 存储器访问：  
	LDR Rd,[Rn,#offset] 从存储器Rn+offset的位置读数据存到Rd中
	STR Rd,[Rn,#offset] 将Rd中的数据写入到存储器Rn+offset的位置 
+ 压栈出栈：PUSH<reg list> POP<reg list>
+ 跳转指令：B BX BL(保存了地址可跳回) BLX
+ 逻辑：AND按位与  ORR按位或 BIC位清除 ORN按位或非 EOR按位异或
  