# Wavenet-Implementation

## It is a Text to Speech 
#### Starting with Wavenet

#### Main Features:

##### 1. When "Regular CNN's" are used, and suppose if I have a network 4 layers deep, one can get 4 layers back in time or 4 time steps back in time. So, if one wants to go 1000 time steps back in time, he would be needing a network with 1000 layers. So, this becomes computationally a challenge. This is called Linear Footprint.

![imresizer com (1)](https://user-images.githubusercontent.com/34116562/65320014-987b5700-dbbe-11e9-8dd9-68102355caa5.jpg)


##### To outcome this, one may use "DILATED CNN'S", in which there is exponential footprint. Using that, if we have a 10 layer deep neural network, one can go 1000 steps back in time. The dilation is doubled for every layer up to a limit and then repeated. Like in this research paper, dilation is of the order of 1, 2, 4, . . . , 512, 1, 2, 4, . . . , 512, 1, 2, 4, . . . , 512 and so on.


![imresizer com (2)](https://user-images.githubusercontent.com/34116562/65319984-8a2d3b00-dbbe-11e9-9e12-c82a1859c881.jpg)

##### -- Very long look back.
##### -- Train Faster.

##### 2. Each of the nodes that are left behind in between the connected nodes of the dilated cnn, leading to the output; they are not just simply multiplied and added. Each of the nodes has some complexity shown below. There is tan on one side, sigmoid on the other side, and then multiplied together. After that, the result is fed into the 1x1 convolution and then added. And, this is for one node! This is also called Extra Complexity or Gated Unit.

#### SIDE CHAINS

#### Apart from this, each of the nodes have side chain. Every node has feeds into this long chain of 1x1 convolutional layers. At the end, softmax is applied to get the output.

#### Hence, actual output is fed from "sidways connections" from all layers.

![imresizer com](https://user-images.githubusercontent.com/34116562/65319989-8bf6fe80-dbbe-11e9-9b1b-b650b389a82e.jpg)

#### Output:

#### Output is a distribution rather than a single prediction or number. It prints all the distribution of what it thinks at each time step of what the next prediction is going to be.

#### Training is quick because at each time step it knows what the next sample is going to be.

#### https://github.com/ibab/tensorflow-wavenet This approach requires a dataset download of 10 gb.
#### https://github.com/peustr/wavenet Colab disconnects again and again in this.
#### Link to the Research Paper: https://arxiv.org/pdf/1609.03499.pdf
