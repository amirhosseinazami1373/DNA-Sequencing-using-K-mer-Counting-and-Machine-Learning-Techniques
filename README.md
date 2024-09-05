# DNA-Sequencing-Using-K-mer-Counting-and-Machine-Learning-Techniques
Analyzing and reading gene sequence data is a hard task for a machine mainly because:

**1- Gene sequence data are in the form of basic nucleotide sequences (A, T, C, G), not numeric values.** 

**2- The length of the gene sequences are random.**

The variability in the length of gene sequence data will make their vectorization an arduous task. Uniform vector lengths are required, considering that vectorization and uniform-length vectors are necessary for feeding the data for classification. There are several
different ways to approach the pre-processing of sequencing
data, however, the most popular seems to be the **‘k-mer’**
approach. 

Using this method, we will split data sequences
into overlapping subsets of words of k length (usually
multiples of three as three nucleotides correspond to one amino
acid and are called a DNA sequence reading frame). Using the k-mer technique, we can create a **bag of words** for gene sequences. 
This bag of words will later be used to train different machine-learning algorithms. For this project, we aim to compare the performance of Neural Networks, Naïve Bayes, and Support Vector Machines for the detection of enzymes based on their sequence. 

# Gene types and distribution:

![image](https://github.com/user-attachments/assets/894780c2-8954-4948-bfc1-bf5623ed2920)

# ML methods: 

Here, **Naïve Bayes** is a probabilistic model of data that performs generative
classification rather than discriminative classification. According to the model, a class is
defined as a piece of data based on which is the most probable. Naïve Bayes, in particular, learns the
probability value for each piece of data independent
of other data in a given set and combines those probabilities to
estimate the total probability for the whole piece of data.

*Tunable parameters:* 

*1- Smoothing value*

**Support vector machines** are linear classifiers that can sort data into different classes based on their linear
separation. Each k-mer in a sequence is affected by a weight
value added up, and then the whole sequence is affected by a bias
value. The bias and weight values are then adjusted as the model
learns from the training data. 

*Tunable parameters:*

*1- Learning rate*

*2- Number of iterations*

*3- C parameter*

**Neural networks** are a machine learning algorithm that was
developed based on the human neural networks that make up
our brain and the way we process data. Neural networks take in
data and process it using a chosen number of ‘hidden’ layers that
alter the input data using weights, bias, and activation functions
to produce an output that can indicate the class of data that
was input into the algorithm. We made use of a
neural network with three hidden layers and one output layer that
all started with random weights and bias values that were
then tuned using backpropagation. The backpropagation
the algorithm makes adjustments to the weights and biases by going
backward through the network so that the algorithm’s output
will line up closer to the actual class of the data. We also
specifically made use of the ReLu activation function that has
become well known for its excellent accuracy by classifying any
value larger than 0 as itself, and any point less than 0 as zero.

*Tunable parameters:*

*1- Regularization value*

*2- Learning rate*

*3- Number of epochs*
