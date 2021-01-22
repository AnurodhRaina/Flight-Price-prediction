# Flight-Price-prediction
<b><u><h2>Predicting the fares of domestic flights across india</h2></u></b><br><br>

<u>Data Description</u><br>

<u>train.csv</u> -<br>
It contains the training data with flight details as described in the last section<br>


<u>Data Dictionary</u> -<br>
<b>Variable</b> 	         Description<br>
<b>Airline</b> 	       The name of the airline<br>
<b>source</b> 	         The date of the journey<br>
<b>Destination</b> 	   The destination where the service ends.<br>
<b>Route</b> 	         The route taken by the flight to reach the destination.<br>
<b>Dep_Time</b> 	       The time when the journey starts from the source<br>
<b>Arrival_Time</b>     Time of arrival at the destination.<br>
<b>Duration</b> 	       Total duration of the flight.<br>
<b>Total_Stops</b> 	   Total stops between the source and destination.<br>
<b>Additional_Info</b>  Additional information about the flight<br>
<b>Price</b> 	         Target, The price of the ticket()<br>
<br>

<u>test.csv</u> -<br>
It has flight details for checking the accuracy of the model on unseen data <br>

<br>
<u>Evaluation Metric</u> - <br>
Model was evaluated using the following metric(RMSE) between the predicted price(y_pred) and the observed price(y_true).: <br>
<i>-np.sqrt(np.square(np.log10(y_pred +1) - np.log10(y_true +1)).mean())</i> <br><br>
<b>Note:</b> The metric is a minimizing metric(i.e. lower the score, better the model) To counter that, we have added a - sign when calculating the score, thus inverting your final score(higher the score, better the model). This also means that your metric will only have values in the negative range, don't be puzzled by it

<u>Steps followed in this project</u> -<br>
1. Loading and observing the data for any anomaly <br>
2. Processing the columns to a respective numeric base for analysis <br>
3. Examining the features to figure out importance <br>
4. Building a model through cross validation for an acceptable result <br>
