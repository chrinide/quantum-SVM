# quantum-SVM
The quantum circuit version of support vector machine to recognize handwritten 6 and 9 using QuTip.

Demonstation for results:

![Alt text](./demo_4.png?raw=true "Title") ![Alt text](./demo_other_4.png?raw=true "Title")

Features are chosen as the vertical ratio and the horizontal ratio, calculated from the pixels in the left (upper) half over the right (lower) half. Thus features are two dimensional vectors. The training data are only two printed images of the standard fonts, which are represented by x1=(0.987, 0.159) for character 6 and x2 = (0.354, 0.935) for character 9. The 8 test data comes from reference 1, which is a subset of https://github.com/damiles/basicOCR. 

The task for a classical SVM is to construct a hyperplane with w·x+b=0 so that w·x_i+b≥1 for x_i in the positive class, and w· x_i+b≤−1 for x_i in the negative class. The optimization objective is to find the optimal hyperplane which could maximize the distance between two classes.

To encode the two training vectors into the qubits, we used two quantum gates, where each one of them rotates a qubit about Y-axis to a certain degree. The process of optimizing the hyperplane parameters is done by calculating the matrix inversion. At last we read some matrix elements for the total quantum circuit to distinguish 6 and 9.

![Alt text](./circuit.png?raw=true "Title")

One possible application that I'm interested in is to further apply this QSVM to data set MNIST.

QuTip is a widely used python package for quantum mechanics and quantum information. After installing QuTip, the files "circuit.py and gates.py" in folder qutip/models are replaced by the corresponding files in this repository.

Reference:
1) Li, Zhaokai, et al. "Experimental realization of a quantum support vector machine." Physical review letters 114.14 (2015): 140504. (main reference that I used.)

2) Rebentrost, Patrick, Masoud Mohseni, and Seth Lloyd. "Quantum support vector machine for big data classification." Physical review letters 113.13 (2014): 130503. (The orignal theoretical paper.)

If you have any questions, please feel free to contact me. I'm looking forward to hearing from any suggestions for further improvement. :) 

Jinlong(Darius) Huang
