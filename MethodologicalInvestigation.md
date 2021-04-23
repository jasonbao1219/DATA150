# Methodological Investigation
Word Count: 1341


## Introduction
Rapid urbanization is a central characteristic of the current world’s globalization and human development. The world’s population is now over 7.8 billion, and the adding of one billion of them only takes the world twelve years; What is more astonishing is that half of world’s population live in cities that only cover three per cent of the earth’s land surface. It is indisputable that the booming population has brought enormous economic prosperities and social changes; however, the skyrocketing number of citizens has also caused many problems that affected the urban environment, lowering the quality of living of citizens. It includes but is not limited to noise, traffic congestion, pollution, and littering. Since cities are a complex system in where millions behave and act differently, it is difficult for scientists and policy makers to extract the correct and right type of data from the population body in order to serve as references in policy making to tackle urbanization problems and optimize urban living environments.


## Problem Statement & Inquiry Type
The inherent nature of this problem is the people, but we can only change other factors for improvement as the victim is also people themselves. That is the reason why data science is particularly useful and applicable in solving problems like this for its ever-evolving techniques, methods, and models so we can understand the people and their actions better. In this paper, I will examine some of the geospatial technologies that are applicable under the urbanization context, identify the pros and cons, and discuss future improvements of the technologies in order to address the board research question that how can data science methods and technologies be practically applied to the field of urbanization study, help us understand the population trends and behaviors in this urban complex adaptive system, and finally offer solutions to optimize the urban living environment, contributing to the human development through expanding the environmental freedom of sustainability.

The type of inquiry would be evaluative, as this paper mainly focuses on evaluating the effectiveness of various data science research methods on its applications in the context of urban data extraction in order to provide useful data for improvements and optimizations of urban environment. Therefore, the three sub-questions will emphasize and highlight different perspectives of efficiency measurement. The three sub-questions are listed below:
1.	Which method has a higher rate of accuracy?
2.	Which method fits better in the urbanization context?
3.	What are the unique characteristics of each model?


## Machine Learning
The first introduced data science research method will be Machine Learning. By definition, machine learning uses computer algorithms that is able to improve itself through the use and experience of data. It constructs a model based on training data and is capable to make predictions or decisions without explicit programming for such functions. In its specific applications that utilizes geospatial datasets including VIIRS Nighttime Light and MODIS Daytime MDVI data, machine learning is able to measure the extents of urban areas with a high accuracy > 95% (Liu 2019). Since the dynamic of machine learning requires the researchers to build different models which classify the data by taking a weighted vote of the individual classifier predictions, in the study the author utilizes Random forest (RF), gradient boosting machine (GBM), neural network (NN), and their ensemble (ESB), with the same datasets of nighttime and daytime data as inputs, explores and compares their effectiveness. For each 500m location, there is a 2-dimension vector involving the two datasets:

Z (i, j) = (VIIRS (i, j), MODIS (i, j)), 

Where:

VIIRS (i, j) = VIIRS nighttime light luminosity at pixel (i, j)

MODIS (i, j) = MODIS NDVI at pixel (i, j)

Below is the entire workflow of this study, the sections highlighted in blue are the machine learning applications of it. As we can see, the three trained models give their own predictions of the degree of urban extent, then, a weighted vote (ESB) will be taken into account, generating modified result; finally, it will be compared with the sample to determine the accuracies of machine learning in this study.
![ML](https://github.com/[jasonbao1219]/[DATA150]/blob/[main]/ML.PNG?raw=true)


## Agent-Based Modeling
Now we have understood the mechanisms of machine learning’s role in urban data extraction. Another important research method that is often employed in urban-related studies is Agent-Based Modeling (ABM). An agent-based model is a class of computational models that simulating the actions and behaviors of autonomous individual to assess their effects on the system as a whole. In other words, it models behaviors of citizens and observe the consequence effects of their daily actions on the city itself. In a study that utilizes ABM to simulate human exposure to urban environmental stresses (Yang 2018). Although it does not completely align with our original research question of urban data extraction for city improvement, we are still able to gain valuable insights of the dynamics, mechanism and unique characteristics of Agent-Based Modeling. It first constructs the framework with three overlapping layers: “spatial data of the concerned urban environment, concentrations of environmental stress sources, and human activities.” Within this framework, environmental stress sources that vary by times of a day are seen as factors that influence the exposures of individual agents, who “dynamically follow their daily life according to predetermined rules that are set according to empirical studies and specific surveys.” During the simulation, the model collects and summarizes “both individual and collective exposure and inform relevant exposure reduction strategies,” so the pollution exposures to human beings can be measured and analyzed. Due to the fact that the urban population is extremely diversified and they all behave in their unique ways, the researchers “group people with similar attributes and behaviors” with all kinds of personal characteristics including “age, gender, work, income, education, living and working location, and access to cars or public transport, as well as the environmental conditions.” Below is an example of a 35 years old employed female’s daily routine, in which p is the priority of that action.
![ABM](https://github.com/[jasonbao1219]/[DATA150]/blob/[main]/ABM.PNG?raw=true)

Ei (x, t) = Ai (x, t) * H (x, t) is the mathematical exposure formula, in which H is a constant underlying stress vector while Ai depends on the activity performed at time-step t and the safety level assumed for this individual i. 


## Compare & Contrast
Finally, we will compare the two data science research methodologies, discuss how the methods can contribute to the central research question, identify the strengths and weaknesses of each, as well as detect the gaps in current methods. The first sub-question is concerned about accuracy. In the Machine Learning paper, the authors claimed it has an impressive high accuracy of 95% (>98% producer’s accuracy, >92% user’s accuracy); while the Agent-Based Modeling does not necessarily have an accuracy rate, but rather come up with the conclusion that lower winter temperatures cannot compensate for the pollutant exposure stresses, providing useful information to the policy makers in an idealized setting. The second question talks about the model’s adaptivity to the urban setting. A quick research on the academic databases has revealed that ABM has been applied much more frequently in urban setting than Machine Learning, primarily due to its strength of simulating the activities individuals (citizens) and monitoring its influences on the higher level of system (urban environment). The third sub-question regards uniqueness. Machine Learning is effective in analyzing and predicting, as it summarizes outcomes of different models and produces its own weighed prediction (particularly in the growth rate, direction of cities); while ABM performs well when imitating and demonstrating the existing effects and influences citizens have imposed on cities through their behaviors and actions.


## Gap Identification
One possible limitation of the proposed research methods is the inability to fully verify the accurateness of the commutated outcome. For example, the ABM model was successfully deployed to measure citizen’s exposure to environmental stressors in the city of Hamburg, but only reached an conclusion in an idealized situation; Although the accuracy rate for the Machine Learning study is high, it is calculated through inputting decades-old data and comparing the outcome with the current city development extent; The accuracy improved significantly compared with the 20-years-older GRUMP dataset, however the new dataset’s ability to predict future remains unknown.


References: 
Yang, L., Hoffmann, P., Scheffran, J., Rühe, S., Fischereit, J., & Gasser, I. (2018). An Agent-Based Modeling Framework for Simulating Human Exposure to Environmental Stresses in Urban Areas. Urban Science, 2(2), 36. doi:10.3390/urbansci2020036
Liu, X., de Sherbinin, A., & Zhan, Y. (2019). Mapping Urban Extent at Large Spatial Scales Using Machine Learning Methods with VIIRS Nighttime Light and MODIS Daytime NDVI Data. Remote Sensing, 11(10), 1247. doi:10.3390/rs11101247
