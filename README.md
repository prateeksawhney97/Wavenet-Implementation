# Wavenet-Implementation

#### Starting with Wavenet

#### Main Features:

##### 1. When "Regular CNN's" are used, and suppose if I have a network 4 layers deep, one can get 4 layers back in time or 4 time steps back in time. So, if one wants to go 1000 time steps back in time, he would be needing a network with 1000 layers. So, this becomes computationally a challenge. This is called Linear Footprint.

##### To outcome this, one may use "DILATED CNN'S", in which there is exponential footprint. Using that, if we have a 10 layer deep neural network, one can go 1000 steps back in time.

##### -- Very long look back.
##### -- Train Faster.

##### 2. Each of the nodes that are left behind in between the connected nodes leading to the output; they are not just simply multiply and add. 

#### Link to the Research Paper: https://arxiv.org/pdf/1609.03499.pdf
