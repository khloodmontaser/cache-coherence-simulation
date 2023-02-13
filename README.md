###### Cache coherence simulation

> This simulation represents how the cache performs to maintain the coherence between two processors using the MSI protocol.
This simulation was performed using SMPCache which is a trace-driven simulator for the analysis and teaching of cache memory systems on symmetric multiprocessors.

###### the transition diagram for the MSI protocol

> The basic MSI protocol with the ``Modified``, ``Shared``and ``Invalid`` state
![image](https://user-images.githubusercontent.com/113125527/218504967-3afdf9e9-509f-472e-8563-8854e8c96295.png)

###### Simulator configuration
* Open the simulator and from file menu choose Load Configuration.
* go to ``C:\PROGRAM FILES (X86)\ARCO\SMPCACHE\EXAMPLES\SMP\`` and choose ConfigMSI.cfg to load the MSI protocol pre-configured files.
![smp cache](https://user-images.githubusercontent.com/113125527/218513044-63a18c91-cbf3-44a0-9d85-d61275a1165f.jpg)
###### *this configugration contains 2 processes p0 and p1, their cache size 256 Bytes each has a block size 16 Bytes.*
* from file menu choose Open memory traces then go to ``C:\PROGRAM FILES (X86)\ARCO\SMPCACHE\EXAMPLES\SMP\`` and on top right corner make sure that ``P0`` and ``P1`` are loaded with MSI1.prg.
*  from View menu choose Cache Evolution and make sure Processor cache is 0
