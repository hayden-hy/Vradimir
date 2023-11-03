# Main Part
### function.py
Python code for CEC2013 Benchmark Function
- Only Unimodal & Multimodal Functions implemented, no Mixed Functions.
- initial it with specifying the dimensionality in the format of ```variable = funcname(d: dimension)```, like ```function = func1(10)```.
- run it with vector or matrix data as the parameter, like ```func1.run(vec)```
  
### CoordinateSystemTrans.py
Multi-dimensional Coordinates System Transformation
- polar2cartesian
  - input: cartesian vec $\[ x1,x2,...,x_n \]$
  - output: polar vec $\[ \rho ,\theta_1,\theta_2,..., \theta_n-1 \]$
- cartesina2polar
  - reversed as polar2cartesian
- ps: transformation with accuracy loss due to the byte digit limit of float type.
  
### JADE.py
Python Implementation of JADE according to the original paper.

### MultiformJADE.py
JADE Using the multiform evolution framework below.
- Basic idea: reconcile two different forms and allocate the computation resource to a dominant one.
- $t_1$ : control the independent evolution
- $t_2$ : control the dominant evolution
![Algorithm](https://github.com/hayden-hy/Vradimir/assets/54624140/abf64056-a43c-4836-875b-d115312d8e70)
- the code has been modified to fit in the multiform with 3 forms. namely polar and cartesian plus PCA transformation, you can edit the code by removing PCA transformation to fit for the polar-and-cartesian-based multiform again.

# Miscellaneous
There are some other multiform algorithms attempting to seek improvements for the multiform JADE, but they are all less effective than the polar-and-cartesian-based multiform JADE. 
