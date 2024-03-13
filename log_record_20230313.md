# 20240313 log record



|       **Batch size**        |                           **128**                            |
| :-------------------------: | :----------------------------------------------------------: |
| **Learning rate optimizer** | **optim.Adam(net_model.parameters(), *lr*=0.0001, *betas*=(0.9, 0.999), *eps*=1e-8)** |
| **Learning rate schedule**  | **CosineScheduler(int(epochs*0.95), *warmup_steps*=0, *base_lr*=0.001, *final_lr*=1e-6)** |
| **Total number of epochs**  |                           **1000**                           |
|          **Model**          |                          **HiCNN**                           |
|        **Criterion**        |                **L1 loss and SmoothL1 loss**                 |
|   **Down-sampling rate**    |         **'16x' =1/16 and 'mixed' = (1/2,  1/32)****         |



## **HiCNN & L1 & mixed:**

### **loss (~epoch 589):**

![image-20240313160207325](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313160207325.png)

### predict (epoch = 560):

![image-20240313162650245](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313162650245.png)

### evalution (epoch = 560):

![image-20240313162125522](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313162125522.png)



































## HiCNN & SmoothL1 & mixed:

### loss(~593 epoch):

![image-20240313163159077](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313163159077.png)

### predict (epoch = 560)：

![image-20240313164114189](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313164114189.png)

### evaluation (epoch = 560)：

![image-20240313164147738](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313164147738.png)



## **HiCNN & L1 & 16x :**

### loss (~241 epochs  ！left half):

![image-20240313161825820](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313161825820.png)

### predict (epoch = 240):

![image-20240313165038077](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313165038077.png)

### evaluation (epoch = 240):

![image-20240313164834610](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313164834610.png)









## **HiCNN & SmoothL1 & 16x :**

### loss (~241 epochs  ！right half):

![image-20240313165124024](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313165124024.png)



### predict (epoch = 240):

![image-20240313165739988](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313165739988.png)



### evaluation (epoch = 240):

![image-20240313165807595](C:\Users\23068\AppData\Roaming\Typora\typora-user-images\image-20240313165807595.png)

