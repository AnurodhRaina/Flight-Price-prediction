# Flight-Price-prediction
Predicting the fares of domestic flights across india<br><br>

Data Description<br>

train.csv -<br>
It contains the training data with flight details as described in the last section<br>


Data Dictionary -<br>
Variable 	         Description
Airline 	       The name of the airline<br>
source 	         The date of the journey<br>
Destination 	   The destination where the service ends.<br>
Route 	         The route taken by the flight to reach the destination.<br>
Dep_Time 	       The time when the journey starts from the source<br>
Arrival_Time     Time of arrival at the destination.<br>
Duration 	       Total duration of the flight.<br>
Total_Stops 	   Total stops between the source and destination.<br>
Additional_Info  Additional information about the flight<br>
Price 	         Target, The price of the ticket()<br>


test.csv -<br>
It has flight details for checking the accuracy of the model on unseen data<br>


Evaluation Metric - <br>
Model was evaluated using the following metric(RMSE) between the predicted price(y_pred) and the observed price(y_true).:<br>
-np.sqrt(np.square(np.log10(y_pred +1) - np.log10(y_true +1)).mean())<br>

Steps followed in this project -<br>
1. Loading and observing the data for any anomaly <br>
2. Processing the columns to a respective numeric base for analysis<br>
3. Examining the features to figure out importance<br>
4. Building a model through cross validation for an acceptable result <br>
