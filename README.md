# INRIX Amazon University Hackathon 2023

This project looks at various features (speed limit and average historical speed of road), extracted from the SegmentSpeed Inrix API, and uses a neural network model to calculate the road congestion based on the these two features. Testing the road congestion outputted for various speed limits, the model allows a city planner to determine the optimal speed limit for the least road congestion. Also, by setting the speed limit at or above the historical average speed, we were able to determine that congestion will actually increase. So essentially, city planners can minimize road congestion by optimizing the speed limit on that road.

We built the model by first extracting data from the Inrix SegmentSpeed API and creating a dataset using the Pandas library. This data set contains the historical average speed, speed limit, and congestion. We calculated the congestion for these data values, and added a row to the data frame for each. Then, we created a neural network and utilized the average speed and speed limit as our two features, in order to calculate the congestion, which is the output. After fitting and scaling the model on this data, the model found the predicted congestion value. Lastly, we tested the model on various speed limits while keeping the historical average speed constant, and analyzed the predicted congestion values for these inputs.

In the future, we want to increase the number of features, such as adding an additional 'lane' variable, and use that to further increase the accuracy of the congestion value calculated.




