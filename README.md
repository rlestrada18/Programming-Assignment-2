# Programming-Assignment-2

Normalization Problem

I knew I needed a random 5 x 5 matrix, so i used np.random.rand(5, 5). This function generates numbers between 0 and 1. in this case, (5, 5) produced the right size.

The normalization equation is given in the problem, where X is the data and the mean is subtracted to it then divided by the standard deviation.
I realized that this meant subtract the mean from every element (centering) and then divide everything by the standard deviation (scaling).

In numpy, .mean() and .std() are the straightforward way to het the mean and standard deviation. I stored them in variables, then applied the formula.

This then gave me the normalized array.

Finally, I used np.save("X_normalized.npy", X_normalized) to store the normalized array in a .npy file. That way, the data can be reloaded later with np.load.


Division by 3 Problem

In numpy, I know that np.arange(1, 101) creates an array from 1 up to 100. Since the problem requires squares, I simply sqaured the array with **2. This gave me all the squares 1 to 100.

The problem statement showed a 10x10 matrix. Since I had exactly 100 numbers, I reshaped my 1D array into shape (10,10) using .reshape(10, 10). THis gave me a matrix form similar to the one shown in the instructions.

To extract numbers divisible 3, I remebered that the modulo operator is useful. By checking A%3 == 0, Numpy returned a boolean mask where True means the element is divisible by 3.

Finally, I had to save the filtered array by using np.save("div_by_3.npy", div_by_3) function, which saves arrays in .npy format. This makes it easy to reload later if needed with np.load.
