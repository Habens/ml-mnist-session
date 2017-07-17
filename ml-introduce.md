title: Machine Learning Introduce
speaker: speaker
transition: move

[slide]
# Machine Learning Introduce

[note]
this sharing is about the basic introduce how to implement a ML project, and I assume you guys didn't touch any ML project before.
[/note]

[slide]
# Why Machine Learning {:&.flexbox.vleft}
* There is no easily way to implement the function with normally algorithm: {:&.moveIn}
    - handwritten digits recognition {:&.moveIn}  
      <img src="/img/3.png" width="180">
      <img src="/img/8.png" width="180">
      
    - style transfer  
      <img src="/img/content.png" width="200"> &
      <img src="/img/style.png" width="200"> =>
      <img src="/img/style-transfer.png" width="200"> 

[note]
two problems:
1. handwritten digits recognition. for human that ability is not worth mentioned, but for program, it's hard.
2. apply the style to an image (content). after learning, I can using this algorithmic to any two images to generate 'art' image.

such above two problem, as a developer, even as a human, even though we know they has some relationship,
we don't know what's the exact logic, we can't define a function to accept the input img, and output the number.
so, we hope the machine can help us. let the machine himself to learning the relationship between the input and output.
[/note]

[slide]
# What is Machine Learning {:&.flexbox.vleft}
* It is the way let machine has the ability to learning. {:&.moveIn}  
  like human <span class="yellow">:）</span>

* It involved Probability theory, statistics, approximations, convex analysis, algorithmic complexity theory, etc...

* It can do lot of things:  
    - speech recognition {:&.moveIn}
    - face recognition
    - play game
    - product recommendation
    - medical analysis
    - ...

[note]
* has the ability to learning
* totally complexity theory
* can do lot of things
[/note]

[slide]
# How to implement {:&.flexbox.vleft}
1. assume an equation: <span class="green">y = f(x)</span> {:&.moveIn}  
   <span class="yellow">f(x) = Wx + B</span>
2. assume one pair of <span class="red">W</span>, <span class="red">B</span>
2. apply the <span class="green">X</span> (input) to this equation, got the <span class="blue">Y_</span> (output)
4. verify - compare the <span class="blue">Y_</span> (output) and <span class="green">Y</span> (exact one)
5. update the <span class="red">W</span>, <span class="red">B</span> (learning)
6. verify
7. update the <span class="red">W</span>, <span class="red">B</span> (learning)
8. ...
9. until the accuracy is good enough (acceptable)

[note]
obvious that is not easily work to implement.
let think about what exactly we want:
1. define an equation that means the relationship between of input and output
2. the equation can update itself though learning.
does that looks like to do the word problems in primary school:)
[/note]

[slide]
# Deep Neural Network {:&.flexbox.vleft}
* Neuron {:&.moveIn}  
  <img src="/img/neuron.png" width="400">
  
* Deep Neural Network  
  <img src="/img/deep-network.png">  
  the network more than two layers (input & output)

* loss function - verify  
  compare the network's output with the really label

* gradient descent algorithm - learning  
  update the W, B

[note]
DNN is one of the ways to implement the ML algorithm.
DNN actually is not really deep. if the NN's calculator layer is more than one, we call it DNN :）

introduce some technical terms
[/note]

[slide]
# Handwritten digit recognition {:&.flexbox.vleft}
* DNN {:&.moveIn}
    - input - 28 x 28 matrix {:&.moveIn}  
      <img src="/img/3.png" width="140">

    - output - possibilities array  
      [0.00, 0.01, 0.01, 0.9, 0.01, 0.01, 0.02, 0.00, 0.02, 0.02]  

    - verify - cross entropy  
      compare with exact possibility  
      [0, 0, 0, 1, 0, 0, 0, 0, 0, 0]
    
    - learning - Adam algorithm

* implementation in Tensorflow  
  refer on the <span class="green">mnist.py</span>

[note]
the possibilities array size is 10, and the sum of the possibilities is 1
[/note]

[slide]
# Thanks!
