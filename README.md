# Black-Box Alpha Divergence Minimization

Implementation of the black-box alpha divergence minimization as described in the paper by Hernández-Lobato J. M. et al., "Black-Box Alpha Divergence Minimization", presented at ICML 2016.

## Repository Structure

The repository is organized into two main folders: `boston_housing` and `mnist`, each containing code for experiments conducted on their respective datasets.

### Boston Housing

The `boston_housing` directory includes code to train a neural network with one hidden layer of 100 units on the Boston Housing dataset. There are two versions of the implementation:

- **Autograd Version:** Located in `boston_housing/autograd`, run the experiment using the following command:

  ```sh
  $ cd boston_housing/autograd/
  $ python experiment.py

- **Theano Version:** Located in boston_housing/theano, this can be run on a GPU or CPU. For GPU execution, use:

  ```sh
  $ cd boston_housing/theano/
  $ THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32 python experiment.py

- **For CPU execution, simply run:**
  ```sh
  $ python experiment.py

MNIST
The mnist folder contains Theano code to train a neural network with two hidden layers, each with 400 units, on the MNIST dataset. Due to the size of the network, GPU execution is recommended:

$ cd mnist/
$ THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32 python experiment.py


Results
The experiment.py script stores the results in a results folder within each respective directory.

Configuration
The alpha value is set to 0.5 by default. To modify this value, adjust the following lines:

Line 44 in boston_housing/autograd/black_box_alpha.py
Line 93 in boston_housing/theano/experiment.py
Line 117 in mnist/experiment.py

Dependencies
To run the code, you will need to have the following:

Python
Autograd
Theano (Optional, for GPU acceleration)

Citation
If you find this implementation useful in your work, please consider citing:

@inproceedings{hernandez2016black,
  title={Black-Box Alpha Divergence Minimization},
  author={Hern{\'a}ndez-Lobato, J. M. and Li, Y. and Rowland, M. and Bui, T. D. and Hern{\'a}ndez-Lobato, D. and Turner, R. E.},
  booktitle={International Conference on Machine Learning},
  pages={1511--1520},
  year={2016}
}

Contact
For any queries or discussions, feel free to open an issue in the repository or contact me directly at [qqaazz800624@gmail.com].

Thank you for your interest in this project!