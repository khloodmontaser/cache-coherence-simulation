# Cache coherence simulation

> This simulation represents how the cache performs to maintain the coherence between two processors using the MSI protocol.
This simulation was performed using SMPCache which is a trace-driven simulator for the analysis and teaching of cache memory systems on symmetric multiprocessors.

### the transition diagram for the MSI protocol

> The basic MSI protocol with the ``Modified``, ``Shared``and ``Invalid`` state
![image](https://user-images.githubusercontent.com/113125527/218504967-3afdf9e9-509f-472e-8563-8854e8c96295.png)
------

### The Simulator configuration
* Open the simulator and from file menu choose Load Configuration.
* go to ``C:\PROGRAM FILES (X86)\ARCO\SMPCACHE\EXAMPLES\SMP\`` and choose ConfigMSI.cfg to load the MSI protocol pre-configured files.

![smp cache](https://user-images.githubusercontent.com/113125527/218513044-63a18c91-cbf3-44a0-9d85-d61275a1165f.jpg)
###### *this configugration contains 2 processes p0 and p1, their cache size 256 Bytes each has a block size 16 Bytes.*
* from file menu choose Open memory traces then go to ``C:\PROGRAM FILES (X86)\ARCO\SMPCACHE\EXAMPLES\SMP\`` and on top right corner make sure that ``P0`` and ``P1`` are loaded with MSI1.prg.
*  from View menu choose Cache Evolution and make sure Processor cache is 0.
------

# Results **for the first six times**

### **Accesses number 1**

![image](https://user-images.githubusercontent.com/113125527/218518016-7903c182-dfae-4d27-8f31-3f0a1df370fc.png)

```
As we can see, p0 sent a read requast because it wanted to read block 273.
first it searched in its cache and didn't find the data so it showed a miss in cache, then it sent a read request on the bus and the bus response with the data from the main memory.
```
### **p0 and p1 caches**
![image](https://user-images.githubusercontent.com/113125527/218720473-cd696ad8-cc20-4984-8208-d9a09f9d6165.png)
```
the state for p0 became ``shared``
```

### **State Transition**

![image](https://user-images.githubusercontent.com/113125527/218522167-b98926ca-7635-4503-8cb6-074ec680e8eb.png)
> ##### From ``invalid`` to ``shared``

------

### **Accesses number 2**
![image](https://user-images.githubusercontent.com/113125527/218524547-6c85eac3-24b8-4df8-a16b-41da35766f60.png)

```
p0 sent a read requast because it wanted to read block 273.
first it searched in its cache and found the data so it showed ``a hit in cache``.
```
### **p0 and p1 caches**
![image](https://user-images.githubusercontent.com/113125527/218721889-a7df51dd-a82c-4e8b-81f1-f06e84ca27a8.png)
```
the state for both p0 and p1 became shared.
```
### **State Transition**

![image](https://user-images.githubusercontent.com/113125527/218525033-e8aaa731-eeb5-4eeb-a7a7-58d6fb9c65d4.png)
> ##### From ``invalid`` to ``shared`` 
> and know the block is shared for both po and p1

------

### **Accesses number 3**
![image](https://user-images.githubusercontent.com/113125527/218525993-1de5ecd1-7648-47ef-bef2-0a3d12334a8e.png)

 ```
p0 sent a read requast because it wanted to read block 273.
first it searched in its cache and found the data so it showed a hit in cache
 ```
### **p0 and p1 caches**
![image](https://user-images.githubusercontent.com/113125527/218722279-93e66f88-d923-474f-a19e-9e5945668d49.png)
``` 
p1 modified the bloch so it became ``invalid`` for p0
```
### **State Transition**
![image](https://user-images.githubusercontent.com/113125527/218526459-831841c5-8155-4b8a-8921-b9ed6b63aa3d.png)

``` 
```
------

### **Accesses number 4**

 ```

 ```
### **p0 and p1 caches**

### **State Transition**


``` 
```
------

### **Accesses number 5**

 ```

 ```
### **p0 and p1 caches**

### **State Transition**


``` 
```
------

### **Accesses number 6**

 ```

 ```
### **p0 and p1 caches**

### **State Transition**


``` 
```
