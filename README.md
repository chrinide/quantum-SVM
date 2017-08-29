# quantum-SVM
The quantum version of support vector machine to recognize handwritten 6 and 9 using QuTip.

Demonstation for results:

![Alt text](./demo_4.png?raw=true "Title") ![Alt text](./demo_other_4.png?raw=true "Title")

Features are chosen as the vertical ratio and the horizontal ratio, calculated from the pixels in the left (upper) half over the right (lower) half. Thus features are two dimensional vectors. The two printed images of the standard fonts are represented by x1=(0.987; 0.159) for character 6 and x2 = (0.354; 0.935) for character 9.

The task for a classical SVM is to construct a hyperplane with $\frac{1}{2}$wx ~ þ b ¼ 0 so that w ~ · x ~ i þ b ≥ 1 for x ~ i in the positive class, and w ~ · x ~ i þ b ≤ −1 for x ~ i in the negative class.

The training data are only two standard printed 6 and 9. We used a quantum gate which rotates a qubit about Y-axis to encode the training data.

QuTip is a python package for quantum mechanics and quantum information. After installing QuTip, the files "circuit.py and gates.py" in folder qutip/models are replaced by the corresponding files in this repository.

Reference:
1) Li, Zhaokai, et al. "Experimental realization of a quantum support vector machine." Physical review letters 114.14 (2015): 140504.

2) Rebentrost, Patrick, Masoud Mohseni, and Seth Lloyd. "Quantum support vector machine for big data classification." Physical review letters 113.13 (2014): 130503.

If you have any questions, please feel free to contact me. I'm looking forward to hearing from any suggestions for further improvement. :) 

Jinlong(Darius) Huang
