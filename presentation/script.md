KNN PRESENTATION SCRIPT FOR EAP CLASS

[ SLIDE 1: PROBLEM INTRODUCTION ]
Suppose you are watching over a natural reserve. It is known that two species of a small rodent live there, and some of your tasks are to count sightings of its individuals and make some visual measurements of them.

[ SLIDE 2: TRAINING DATA ]
The two species are clearly distinguishable by their fur color. Moreover, their body length and width are between the measurements you need to take with the assistance of a camera that can measure that.

[ SLIDE 3: DAY MEASUREMENTS ]
Good! During the day, you watched, labeled, and measured them. As part of your task, you plotted length vs. width and colored the samples according to their species. The result is the plot you can see here.

[ SLIDE 4: NIGHT MEASUREMENTS ]
At night, however, it's all dark, and you need to use the camera's night vision. You can take the measurements, but you can't distinguish the samples by fur color anymore. Not giving up, you plot the measurements to search for a hint. Here is what you get.

[ SLIDE 5: DATA SUPERPOSITION ]
When you superimpose the night data over the day data, it seems like the former follow the same distributions as the latter, as shown here. So, < attendant >, how would you label, let's say, this sample here? To which species do you think it belongs? Why? And we can follow the same reasoning for the remaining samples; do you agree? Of course, there are some regions in which we may have some doubt, like here and here. However, there is room for some error, and those fall within the tolerance.

[ SLIDE 6: VISUAL PREDICTION ]
This is what we get when we predict the species by visual inspection of the plot. If we assume that the species' body proportions don't change drastically from day to night, it seems pretty accurate. Great! We solved the classification problem and can go home. Is that right? Do you see any limitations of this method? Note that, in this task, we relied on using features of the data as coordinates and visualizing it in a plot. Can we always do that? What if two features are not enough to distinguish between the classes that interest us?

[ SLIDE 7: HIGHER DIMENSIONS ]
When we take more than three features as coordinates, we can't properly visualize the space on which the samples are placed. We still have the numbers and can make some sense of them, but it isn't as intuitive as before. João, as an engineer, tell me: What can we compute, in any dimension, with points' coordinates?

[ SLIDE 8: DISTANCE ]
Yes, distances! Good. Now, how can we use those distances to label the test point? Yeah, to assign to it the label of its nearest train sample is a great idea.

[ SLIDE 9: “CLOSENESS” RANKING ]
Here, we see the samples ranked by how close they are to the test sample.

[ SLIDE 10: NEAREST NEIGHBOR LABEL ]
This shows the test sample predicted with the label of its nearest neighbor.