## IDEAS 
- I wanted to list possible alteration on architecture given in this(https://drive.google.com/open?id=1FNafY7eCUA1m7X4OUNpC5qdvRHiF6YIc). In this paper, explained architecture and results possibly are the most recent and have great performance. Therefore, I suggest taking this architecture our basis. I have tried to emphasize the key features of this model in the paper, also

## Paper Introduction
- As a brief introduction, the proposed architecture is a fully convolutional network which means that it does not include fully connected layer at the end. This choice stems from the nature problem. Since this is regression problem, the output is in very high dimensions. In case of participation of fully connected layer, this network requires very huge in terms of memory. On the other hand, fully convolutional networks reduces the number of parameters, significantly.(For numeric results, check the paper). 

- Another key feature of this architecture is residual networks. As a well known fact, deeper networks faces with the "vanishing gradients". Residual networks ,by "stacking" parts of convolutional layers, cures this problem.

- Also, increasing number of convolutional layers in a network lowers the output dimension. Therefore, emerge for "un-pooling layer" arises. Conventional method doing so is adding pixels with zeros to the output of previous layers and finally put another convolutional layer(5x5) to diffuse the information of non-zero pixel values. As explained in this paper, the computational problem here is dealing with zero valued pixels during this convolution is not meaningful. Therefore, they proposed another "fast up-convolution/up-projection" (Please check the paper again)

- Finally, as a loss function "BerHu" is employed and its main advantage is that it increases the effect of gradient with large residual. For being able to take derivative of this function, the "c" value is chosen such that the partial function becomes continous.


##Ideas
- Uppoolng Architecture: I think most possible case for us, is to attack on designing uppooling architecture. I think we can try different architecture by considering performance. 

- Loss Function: BerHu is okay about balancing large and small residuals. However, I think we can try to enhance this function with scale invarient error function as explained here(https://drive.google.com/open?id=1BMNSJkW-RrXSAWJ1RtVjaYYqUW5nWYyU) 

- Shape from shading input: This is an image processing method that iteratively solves the mathematical method between the lightning and object reflections by assuming lambertian surface and finally generates depth maps. This idea might not be doable and make sense :) but I thought that we can provide maps that are generated by this method to the residual networks as another additional term. 

Up to now, these are my ideas and I would like to discuss them face to face actually because I am aware that the descriptions are not so in details. 