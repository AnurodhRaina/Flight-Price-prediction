# Flight-Price-Prediction <br> Predicting the fares of domestic flights across india

### Data Description

- **train.csv** :
It contains the training data with flight details as described in the last section<br>

- **test.csv** : It has flight details for checking the accuracy of the model on unseen data <br>


### Data Dictionary
<table>
<tr><th>Variable</th> 	      <th>Description</th>
<tr><th>Airline</th>  	      <th> The name of the airline</th>
<tr><th>source</th> 	       <th>  The date of the journey</th>
<tr><th>Destination</th>  	 <th>  The destination where the service ends.</th>
<tr><th>Route</th>  	       <th>  The route taken by the flight to reach the destination.</th>
<tr><th>Dep_Time</th>  	     <th>  The time when the journey starts from the source</th>
<tr><th>Arrival_Time</th>    <th> Time of arrival at the destination.</th>
<tr><th>Duration</th>  	     <th>  Total duration of the flight.</th>
<tr><th>Total_Stops</th>  	  <th> Total stops between the source and destination.</th>
<tr><th>Additional_Info</th>  <th> Additional information about the flight</th>
<tr><th>Price</th> 	         <th>Target, The price of the ticket</th>
</table>


---

### Evaluation Metric

Model was evaluated using the following metric(RMSE) between the predicted price(y_pred) and the observed price(y_true).: <br>
``` -np.sqrt(np.square(np.log10(y_pred +1) - np.log10(y_true +1)).mean()) ```

**Note:** The metric is a minimizing metric(i.e. lower the score, better the model) To counter that, we have added a negative (-) sign when calculating the score, thus inverting the final score(higher the score, better the model). This also means that the metric will only have values in the negative range, don't be puzzled by it

### Steps followed in this project
1. Loading and observing the data for any anomaly <br>
2. Processing the columns to a respective numeric base for analysis <br>
3. Examining the features to figure out importance <br>
4. Building a model through cross validation for an acceptable result <br>
