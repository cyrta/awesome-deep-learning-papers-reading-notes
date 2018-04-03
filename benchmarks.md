
# Benchmarks


[Demystifying Parallel and Distributed Deep Learning: An In-Depth Concurrency Analysis (2018)](
https://spcl.inf.ethz.ch/Publications/.pdf/distdl-preprint.pdf)
- GPUs	are	still	faster	than	CPUs	in	general
- CPU	is	very	comparable	to	GPU	for	DNN	Training	workloads	if	
appropriate	optimizations	are	exploited
- KNL	beats	P100	for	one	case	but	P100	beats	KNL	for	most	cases

## GPU

**cuDNN** (for	GPUs by nvidia)
and cuBLAS, NCCL	

- NVidia-Caffe
- OSU-Caffe (multi-node	 multi-GPU)
- BVLC-Caffe

# CPU 
  
  **MKL-DNN**,	just	like	cuDNN,	has	definitely	rekindled	this!!
Coupled	with	Intel	Xeon	Phi	(Knights	Landing	or	KNL)	and	MC-DRAM,	the	landscape for	CPU-based	DL	looks	promising..
	
- [An In-depth Performance Characterization of CPU- and GPU-based DNN Training on Modern Architectures](mvapich.cse.ohio-state.edu/static/media/talks/slide/awan-mlhpc17.pdf)
([paper](https://dl.acm.org/citation.cfm?id=3146356))
  - Usually,	we	hear	CPUs	are	10x-100x slower	than GPUs?	[1-3]
    - https://dl.acm.org/citation.cfm?id=1993516
    - http://ieeexplore.ieee.org/abstract/document/5762730/
   - https://dspace.mit.edu/bitstream/handle/1721.1/51839/MIT-CSAIL-TR-2010-013.pdf?sequence=1
   
   - x24 times faster with MKL-DNN http://www.techenablement.com/accelerating-python-deep-learning/
   
   ![](http://www.techenablement.com/wp-content/uploads/2017/02/2017-02-20-figure03-1024x469.png)
   ![](http://www.techenablement.com/wp-content/uploads/2017/02/2017-02-20-figure04-1024x419.png)
   ![](http://www.techenablement.com/wp-content/uploads/2017/02/2017-02-20-figure05-1024x412.png)
  
- Intel-Caffe	is	optimized	for	CPU-based	Deep	Learning



----


   
The [Intel Distribution for Python](https://software.intel.com/en-us/distribution-for-python)
    and [Intel Performance Libraries](https://software.intel.com/en-us/performance-libraries) (2018Q1 now freely available for Compute Engine on GCP. )
    - Intel® Advanced Vector Extensions-512 (AVX-512) 
    -  Intel® Mesh Architecture
    ![](https://2.bp.blogspot.com/-JANAVdamHPA/WgvPqPUAUdI/AAAAAAAAEwA/0zOFhMRJtY8L64jcfyVtaixIGR6VdJR0QCLcBGAs/s640/supercomputing-3.png)
   
https://software.intel.com/en-us/distribution-for-python/features
![](https://software.intel.com/sites/default/files/managed/68/1e/Python2018-Math-Functions-Xeon.jpg)
   https://software.intel.com/en-us/articles/intel-optimized-packages-for-the-intel-distribution-for-python
   
   
use Docker image from `hub.docker.com/u/intelpython/`
    - For the intelpython3_core Docker image, enter    
    
    `docker run -it intelpython/intelpython3_core ()`
    - For Jupyter Notebooks*, enter: 
    
    `docker run -p 8888:8888 intelpython/intelpython3_full jupyter notebook --ip='*' --port=8888 --no-browser`
    
    or just
    `conda install  -y -q intelpython3_full=2018.0.1 python=3`
----

Intel Data Analytics Acceleration Library ([Intel DAAL](https://software.intel.com/en-us/blogs/daal))

![](http://www.techenablement.com/wp-content/uploads/2017/02/2017-02-20-figure07-1024x406.png)

- code at https://github.com/01org/daal.
 - https://github.com/intel/daal/tree/daal_2018_update2/samples/cpp/neural_networks/sources
 - https://github.com/intel/daal/tree/daal_2018_update2/samples/cpp/neural_networks/sources
 
 - https://software.intel.com/en-us/articles/building-a-native-application-for-intel-xeon-phi-coprocessors
  
   - Intel	Machine	Learning	Scaling	Library	(higher	level	library	built	on	top	of	MPI) 
   - [MVAPICH2](http://mvapich.cse.ohio-state.edu/)
