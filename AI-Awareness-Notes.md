# AI Awareness Notes

## AI Story
Yuval Noah Harari argues that humans became humans as they gathered around stories. Telling stories gave rise to a collective identity, a sense of purpose, and a foundation for cooperation. 

Now we have a new story, Artificial Intelligence (AI).

![](/attachments/brain-and-neural-network.png)

Science is not as compelling as stories...

The brain is much more complex than a network of neurons, even though neurons themselves are relatively simple. AI Neural Networks are inspired by the structure of the human brain's network of neurons, but they are vastly simplified.

Geoffrey Hinton, the godfather of AI, successfully advocated for a focus on solving specific tasks that work **mathematically**, rather than strictly mimicking the intricacies of biological neural networks when developing artificial neural networks (ANNs).

![](/attachments/neural-networks-and-mathematical-model.png)

Fei-Fei Li says that when building an airplane, it is aerodynamics and physics that govern the process of flying. If we ask for similar laws in the relationship between AI and the brain, it still feels like we are before Newton's laws. 

## AI Advantages
Our brain consumes 30 watts when learning, while an AI like ChatGPT consumes 30 megawatts when training (learning). You can find other numbers online, but let's just focus on these numbers. The order of magnitude of the power used is enormous, 1 to 1 million. But while this ratio is interesting, I don't think we are really impressed by that. I think, we humans have surpassed that point since the invention of the steam engine, which propelled the industrial revolution and the power of the machines took over hand labor.

So, we can naturally imagine that there are some very powerful computers, and a lot of them, working intensively to process any data they can find in the world. This is actually the core advantage of AI over the human brain: the scale at which AI can operate.

We also know that while biological intelligence is mortal, digital intelligence is immortal. We can copy ChatGPT to some other computers.

What is surprising, though, is that digital intelligence may have a better learning algorithm than the brain. 

## AI Learning Algorithm
Where is the Life we have lost in living?  
Where is the wisdom we have lost in knowledge?  
Where is the knowledge we have lost in information?
― T.S. Eliot, The Rock (1934)

These lines by T.S. Eliot are believed to have originated the idea of the DIKW (Data → Information → Knowledge → Wisdom) relationship, which has been a part of the language of information science for many years.

![](/attachments/DIKW-pyramid.png)

There are two main approaches to AI: a bottom-up approach, as suggested by the DIKW pyramid, and, by analogy, a top-down approach.

### Top-down approach
The bottom-up approach is implemented through artificial neural networks; ChatGPT employs this approach. On the other hand, Siri initially adopted a top-down approach and later incorporated features of the bottom-up approach.

A better way to understand what AI is about is to engage with it. For the broader audience, the most effective approach might involve just reading and contemplating AI concepts. Let's ask ourselves a simple question: when do I learn more (can I rate it?!) about AI, when I consume a lot of tech news about AI, or when I read articles that explain the principles of AI? 

People have mental models of how the world works; a kind of internal simulator that simulates the interesting aspect of the case we want to assess, enabling us to understand. For someone familiar with charts, the DIKW pyramid can be incredibly useful. For others working in media, tech news may be more helpful, and they might discover intriguing aspects of AI that a tech article didn't consider or that were out of scope. Both groups, however, are constructing new models based on their prior ones, combining their existing 'data/information' with new 'data/information,' and transforming them into AI knowledge. 

We can further explain that what constitutes knowledge for one model could be data/information for another model and so on. In any case, we need to find ways to nurture curiosity and remain receptive to AI's journey toward mimicking human intelligence.

This idea of data transformation and reshaping from layer to layer is important in understanding how AI works; like energy transformation is key in physics.

Let's now see how top-down and bottom-up approaches work in practice.

The early success of AI in the 2000s followed the top-down approach. Researchers focused on knowledge extraction from human beings and representing it in a computer-readable form. To transfer knowledge to a computer, you have to find a way to represent it. This is achieved through reasoning and logic, and symbols are eventually used to operate with logic.

A simple example of how you can extract knowledge using logic and symbols might look like this:

![](/attachments/and-or-tree.png)

This image can effectively illustrate how we can determine an animal based on its physical characteristics. However, does it perform well in practice? Can this model solve the following riddle?

'I am a creature of stripes, adorned like a canvas of art,
With black and white in harmony, running free with all my heart.
In the African grasslands, where the sun kisses the earth,
I roam with my herd, my beauty, and my worth.
What am I?' (Answer: Zebra)

The creative and metaphorical nature of the riddle makes it difficult for symbolic AI to interpret the poetic language and connect it to the specific answer 'zebra'. While the inability to solve a riddle doesn't define the quality of an AI model, it does highlight the limitations of the model.

The top-down approach, such as symbolic AI, excels at modeling precise and consistent knowledge, such as automating the movement and placement of items in a warehouse.

The main challenge with this approach is that wisdom, knowledge, and concepts are challenging to define scientifically, and creating highly accurate descriptions of anything is impossible.

These top-down models are effective managers of the knowledge we can extract from human life experiences and feed to them. However, they lack the ability to create their own artificial experiences.

So, if we can't rationally define what a zebra is, how can a computer define how to recognize a picture of a zebra?

The answer lies in artificial neural networks (ANNs), or as it's more commonly referred to in AI, deep learning.

### Bottom-up Approach / ANNs (deep learning)
Researchers have been developing ANNs for over 40 years, but it wasn't until the 2010s that enough data and processing power became available for ANNs to demonstrate surprising results.

While Symbolic AI needs a certain amount of data for optimization, it eventually reaches a point where adding more data doesn't enhance performance. On the other hand, ANNs require a substantial amount of data to show promising results, and the more data you provide, the better their performance becomes. This trend also drives a growing demand for AI computing power, sparking a competition among major tech companies to create more advanced AI chips.

![](/attachments/convolution-neural-networks.png)

This system, known as a Convolutional Neural Network (CNN), processes a large number of images as input and determines whether each image features a horse, a zebra, or a dog. In the initial step, labeled as Feature Extraction, special feature detectors (or filters, labeled as Kernel) slide across the image to extract features from various parts of the image. These feature detectors are similar to the filters found in applications such as Photoshop or other image processing software. Just as we use a red-eye removal tool that first identifies the eye feature before eliminating the red-eye effect, we can create feature detectors for skin patterns and more. 

All these relevant features are collected, and data is transformed in a way that the system can decide through it's learning algorithm, which features are important for recognizing different categories (horse, zebra, dog) and then the system can utilize more suitable feature detectors. Once all the data is reshaped and reduced to only meaningful data for our task, it is fed to our ANN.

This initial part of the CNN serves as a good example to illustrate that in real-world scenarios, these systems are complex and involve other components integrated with ANNs.

In our image, the ANN component is labeled as the "Fully Connected Layer", which is a version of an ANN where each neuron (represented by blue circles) in a layer (each column represents a layer) is connected to all neurons in the subsequent layer.

In the first layer, what's intriguing for the ANN is change—like the contrast between neighboring input values of -1 and 1—because change signifies the presence of an edge, which the ANN aims to identify. Thus, the first layer detects edges. The second layer may identify patterns formed by these edges, such as the curve of a stripe, a curved corner of the nose, or the circular shape of an eye. The third layer could identify a potential zebra's nose in the correct spatial relationship with a zebra's eye. This progression continues until the final layer makes the ultimate prediction: 0.2 (20%) horse, 0.7 (70%) zebra, and 0.1 (10%) dog.

The process is illustrated in the following image:

![](/attachments/CNN-data-to-features.png)

On the other hand, this [web page](https://adamharley.com/nn_vis/cnn/2d.html) provides a simpler example (limited to numbers) that better visualizes data transformation.

The artificial neuron mimics the mechanism of **brain neurons**, which is simple. In the brain, a neuron becomes charged primarily through root-like structures known as dendrites. If the collective signals received by these dendrites surpass a particular threshold, the neuron initiates an electrical impulse through its axon. This impulse can then be intercepted by neighboring neurons through their respective dendrites.

![](/attachments/brain-artificial-neuron.png)

Thus, the **artificial neuron** sums all the inputs or **weights** and passes the result to a function that makes slight adjustments before transmitting the outcome to neurons in the subsequent layer.

> The mechanism of the artificial neuron is our closest attempt to emulate the functioning of brain neurons. However, the collaborative behavior of artificial neurons within a layer only partially mirrors the cooperative interactions observed among neighboring neurons in the brain's neural network.

##### How ANNs Learn
Systems of this kind aim for a minimum accuracy of 90%, which means the current predictions of the system (0.2=20% horse, 0.7=70% zebra, and 0.1=10% dog) indicate that the system is still in the learning or training phase, as per AI terminology. During training, we input images for which we already know the true identity. In this specific case, knowing that the input is a zebra, we should obtain probabilities like: 92% zebra, 7% horse, 1% dog. Thus, there's an error of 92% (target) - 70% (current) = 22% = 0.22. Since we calculated all these numbers using mathematics, (quite a lot of it, in fact), we recalibrate the weights accordingly to achieve the desired output of 0.92 = 92% zebra. Done, our system is now trained! Despite the simplicity of the concept, it took many years, to make a practical implementation of the concept. 

A simpler challenge easy to understand by a broader audience lies in determining the quantity of images required to train our system effectively. If we set the desired target output at 92%, it implies that our system will derive nearly all of its learning from that final image. Therefore, opting for a smaller target, say 71%, allocating around 1% (or 2%?!) of learning from each individual image may seem reasonable. In practice, these systems often demand thousands, if not tens of thousands, of images for training. Hence, some serious mathematics is required just to come up with the optimal number of images needed to properly train the system.

How many zebra images does a child need to see in order to learn to recognize a zebra? How many minutes of a movie with a zebra are required? And how many minutes does a child need to spend seeing, hearing, touching, and smelling a zebra in a zoo, while their mother or father explains?

Google is currently developing Gemini, a multimodal AI that combines Bard with Vision AI. The question is: can it match the intelligence of a child?

Yann LeCun, the godfather of AI and father of CNNs, currently leading AI at Meta, suggests that before we reach human-level AI, we will first attain cat-level AI. He believes that true intelligence is rooted in observation, much like how infants learn. Language comes later, and for animals, language is unnecessary. Intelligence is highly multidimansional and the essence of human intelligence is the ability to construct models of the world by simulation and analogy.

Computers have come this far thanks to the concept of using binary representation ("zeros" and "ones"), inspired by just simple light bulbs, which is unrelated to how the human brain functions. Now, with Artificial Neural Networks (ANNs), we are at least on the right path to represent intelligence much closer to the way our brain functions. Consequently, there is a substantial difference between computers and ANNs: computers are deterministic in nature, while ANNs are stochastic (introducing an element of randomness into their functioning). Photos in our mobile phone do not change even if we restart the system, while ChatGPT can give us slightly different answers for the same question.

This controlled randomness in the outcome can be viewed as a clear disadvantage when assessing ANN-based systems as simple apps, like a calculator app. In fact, when we control and direct the stochastic nature of ANNs, by adjusting randomness in ANNs, we generate various responses, akin to experiences. By filtering out unlikely or invalid outcomes, we curate a set of "artificial experiences" from which the AI can learn. 

Typically, only the following verses of T.S. Eliot are cited in data and information processing contexts:

Where is the wisdom we have lost in knowledge?
Where is the knowledge we have lost in information?

Could AI's potential to solve global problems lead us to a future where technology empowers us to live more meaningful and fulfilling lives? Do we need to consider including the first line as well?

Where is the Life we have lost in living?

### AI and ChatGPT
