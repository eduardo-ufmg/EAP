# KNN Presentation Script for EAP Class

## Slide 1: Problem Introduction
Suppose you are watching over a natural reserve. It is known that two species of a small rodent live there, and some of your tasks are to count sightings of its individuals and make some visual measurements of them.

---

## Slide 2: Training Data
The two species are clearly distinguishable by their fur color. Moreover, their body length and width are between the measurements you need to take with the assistance of a camera that can measure that.

---

## Slide 3: Day Measurements
Good! During the day, you watched, labeled, and measured them. As part of your task, you plotted length vs. width and colored the samples according to their species. The result is the plot you can see here.

---

## Slide 4: Night Measurements
At night, however, it's all dark, and you need to use the camera's night vision. You can take the measurements, but you can't distinguish the samples by fur color anymore. Not giving up, you plot the measurements to search for a hint. Here is what you get.

---

## Slide 5: Data Superposition
When you superimpose the night data over the day data, it seems like the former follow the same distributions as the latter, as shown here. 

So, <attendant>, how would you label, let's say, this sample here? To which species do you think it belongs? Why? And we can follow the same reasoning for the remaining samples; do you agree? 

Of course, there are some regions in which we may have some doubt, like here and here. However, there is room for some error, and those fall within the tolerance.

---

## Slide 6: Visual Prediction
This is what we get when we predict the species by visual inspection of the plot. If we assume that the species' body proportions don't change drastically from day to night, it seems pretty accurate. 

Great! We solved the classification problem and can go home. Is that right? Do you see any limitations of this method? Note that, in this task, we relied on using features of the data as coordinates and visualizing it in a plot. Can we always do that? What if two features are not enough to distinguish between the classes that interest us?

---

## Slide 7: Higher Dimensions
When we take more than three features as coordinates, we can't properly visualize the space on which the samples are placed. We still have the numbers and can make some sense of them, but it isn't as intuitive as before. 

João, as an engineer, tell me: What can we compute, in any dimension, with points' coordinates?

---

## Slide 8: Distance
Yes, distances! Good. Now, how can we use those distances to label the test point? Yeah, to assign to it the label of its nearest train sample is a great idea.

---

## Slide 9: “Closeness” Ranking
Here, we see the samples ranked by how close they are to the test sample.

---

## Slide 10: Nearest Neighbor Label
This shows the test sample predicted with the label of its nearest neighbor.

---

## Slide 11: 2D Set Recap
For us to get a better catch of the method, let's apply it to the dataset from the initial problem.

---

## Slide 12: Edges to the Nearest Neighbor
This figure shows each test sample connected by a black edge to its nearest training sample.

---

## Slide 13: 2D Nearest Neighbor Prediction
And this figure shows the samples predicted with the label of their nearest neighbor. 

Now, note something: to predict the label for a sample, we only need its position. So, we are also predicting points in the space. 

Say, <attendant>, which label you assign to this point, here? And this, here? Good. Now, we do this for a grid of points that cover this entire region and see what we get.

---

## Slide 14: Decision Boundary for 1NN
Here, each point is colored according to the class a sample in it is assigned. 

We can see that some regions do not seem correctly predicted and that the discrepancies between the obtained and the expected may be beyond tolerance. Can you explain why this happened? 

In the training stage, where our character labeled the samples' fur color, it's likely that some were misclassified. We can see that some train samples, like this and this, are part of a distribution that doesn't match its assigned label. In the prediction step, the samples that are closer to them than to the correctly labeled ones receive their labels, which are probably not correct according to the distribution.

---

## Slide 15: Prediction for 10NN
This figure shows how the test samples are predicted if we consider the ten train samples that are closest to it, or its ten nearest neighbors.

---

## Slide 16: Decision Boundary for 10NN
And, in this plot, the resulting decision boundary is shown. 

Note that it is really smoother and that the outliers' effect is drastically reduced. It indicates that this model achieved a better fit for the classes' pattern.

---

## Slide 17: Real Data
Now, we check it on real data. For that, the Pima Indians Diabetes dataset was chosen. This set consists of seven hundred and sixty-eight samples, split into two unbalanced classes, “Diabetic” or “Non-Diabetic.” 

There are five informative features: glucose, blood pressure, skin thickness, insulin, and body mass index.

---

## Slide 18: Results
That table shows that increasing the number of neighbors from one to three is enough to improve accuracy by seven percent.

---

## Slide 19: Thank You
That is it. Thank you! Questions?