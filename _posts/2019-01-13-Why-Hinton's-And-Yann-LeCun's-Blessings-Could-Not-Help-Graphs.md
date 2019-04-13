---
layout: post
title: Why Hinton's And Yann LeCun's Blessings Could Not Help Graphs
subtitle: How Deep Learning on graphs is different from Deep Learning on images.
---

Let me be honest, graphs are my favourite data structure and graph theory is just incredible. I love graphs so much that I regularly visit [Zachary's Karate Club](https://en.wikipedia.org/wiki/Zachary%27s_karate_club).

<img src="http://tkipf.github.io/graph-convolutional-networks/images/karate.png" width="300" height="300">


Deep Learning is good at extracting complex patterns from data. Data modelled as graphs- social networks, e-commerce networks, biology networks, traffic networks... are readily available, but they are the beyond what Yann LeCun's convolution can handle . Applying deep learning to the ubiquitous graph data is non-trivial because of the unique characteristics of graphs. This problem is nontrivial because several challenges exist for applying traditional deep learning architectures to graphs.

* Irregular domain

Unlike images, audio and text which have a clear grid structure, graphs lie in an irregular domain, making it hard to generalize some basic mathematical operations to graphs. For example, it is not straight-forward to define convolution and pooling operation for graph data, which are the fundamental operations in Convolutional Neural Networks (CNNs). This is often referred as the [Geometric Deep Learning](http://geometricdeeplearning.com/).

* Varying structures and tasks

Graph itself can be complicated with diverse structures. For example, graphs can be heterogeneous or homogeneous, weighted or unweighted,and signed or unsigned. In addition, the tasks for graphs also vary greatly, ranging from node-focused problems such as node classification and link prediction, to graph-focused problems such as graph classification and graph generation.The varying structures and tasks require different model architectures to tackle specific problems.

* Scalability and parallelization

In this era of Big data, real graphs can easily have millions of nodes and edges, such as social networks or e-commerce networks. As a result, how to design scalable models, preferably with a linear time complexity, becomes a key problem. In addition, since nodes and edges in the graph are interconnected and often need to be modelled as a whole, how to conduct parallel computing is another critical issue.

* Interdiscipline

Graphs are often connected with other disciplines, such as biology, chemistry or social sciences. The interdiscipline provides both opportunities and challenges: domain knowledge can be leveraged to solve specific problems, but integrating domain knowledge could make designing the model more difficult. For example, in generating molecular graphs, the objective function and chemical constraints are often non-differentiable, so gradient based training methods cannot be easily applied.

 
### But Graph Neural Networks are Neural Networks on steroids.
In ecommerce, a graph-based learning system will be able to exploit the interactions between users and products to make a highly accurate recommendations. In chemistry, molecules are modeled as graphs and their bioactivity needs to be identified for drug discovery. 


> Graph data are irregular.

Each graph has a variable size of unordered nodes and each node in a graph has a different number of neighbors, causing some important operations (e.g., convolutions), which are easy to compute in the image domain, but are not directly applicable to the graph domain any more. Furthermore, a core assumption of existing machine learning algorithms is that instances are independent of each other. However, this is not the case for graph data where each instance (node) is related to others (neighbors) via some complex linkage information, which is used to capture the interdependence among data, including citationship, friendship, and interactions.


### How is Image domain different from Graph Domain
> Image data is Euclidean data whereas graphs and manifolds are Non Euclidean data.

And what does this imply?

Taking image analysis as an example, an image can be represented as a regular grid in the Euclidean space. A convolutional neural network (CNN) is able to exploit the shift-invariance, local connectivity, and compositionality of image data, and as a result, CNN can extract local meaningful features that are shared with the entire datasets.

Non Euclidean data has
* No common system of coordinates
* No vector space structure
* No shift invariance


#### Basically, Deep Learning on graphs require all the building blocks of Hinton's Neural Networks to be redefined and reinvented.

<img src="https://i.ibb.co/tCJ3j77/Screenshot-86.png" width="100%" height="100%">

[Micheal Bronstein](https://people.lu.usi.ch/bronstem/) is to [Geometric Deep Learning](https://www.youtube.com/watch?v=ptcBmEHDWds) what Geoffrey Hinton is to Deep Learning. Simple as that !

If you made it here, probably you are into the idea of Graph Neural Networks and let me tell you we have a lot to cover(dropping a subtle hint that this is going to be a series of blog posts). 


<img src="https://i.ibb.co/g7JFYFr/Screenshot-89.png" width="100%" height="100%">
