# wandb代码运行问题
报错：wandb.sdk.lib.service.service_port_file.ServicePollForTokenError: Failed to read port info after 30.0 seconds.
解决方案：win11下wandb 0.25.1版本初始化时service读取端口失败，改offline模式也报相同错误，谷歌搜索官方回复如下，更新wandb版本至0.26.0版本即可解决报错，命令行输入：
```
pip install wandb==0.26.0
```

![[Pasted image 20260415124626.png]]
解决此问题后，运行train.py完成，结果及wandb记录参数图如下：
![[Pasted image 20260415124036.png]]
![[Pasted image 20260415125633.png]]
运行model.py结果如下：
![[Pasted image 20260415125946.png]]