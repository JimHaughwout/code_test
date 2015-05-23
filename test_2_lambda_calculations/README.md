# Lambda Calculation Code Test

#### Background
Many different customers have similar types of sensors and other data source. 
However, each has their own unique rules for processing.
To maximize re-usablity, we want to use soft-coding to apply different "custom" calculations by customer,
in-flight, as we use the data. 

#### What you have
You have a data set in JSON formats (array of JSON objects). Pick whichever one is easiest to use. 
This data set corresponds to a highly-simplified result of a mock query.

The data consists of sample sensor location reads. These data have been pre-processed from their original source data 
to something we can use for quick calculations. (We do this with DAG pre-processing). You can assume all the data are
valid, unique and in correct format.

Your processed data is mock location reads:
```json
TODO
```

Write a class that takes in this data and applies a soft-coded configurable 
Lambda function to produce different results for different customers. 
The results will be a net "Utilization KPI Score" for a given thing (as in "Internet of Things")

You have two customers:

###### Rental Company
This customer measures utility by how much a vehicle is used:
* Each data row is a measure
* Increment the `utility_score` by 10 for each data point where `engineStatus == 'ON' and gear > 1`
* Increment the `utility_score` by -1 (decrement by 1) for each data point where `engineStatus == 'ON' and gear == 1`
* Ignore all other points

Don't worry about wrapping this is a full-stack app (or streaming analytic entity like a Spark Driver). 
A simple Class with methods is fine. Just ensure the Lambda functions are soft-configured (storing in properties file is fine, no need to setup a metadata store). 

CONSIDERATIONS


#### Basics
Start with data set. Build HTML5 visualization with libraries of your choice
# Google Map showing the location of each sensor point. Connect all the points in a line.
# Normal line chart below this:
  - X-axis is Date-Time of the sensor read
  - Y-axis is cumulative distance travelled 
# Table of facts below that using following columns:
  - foo
  - bar

#### Bonus points
* Add some tool tips (to see all the data associated with any point)
* Link the visualization (i.e., I click on a map point and see highlights and tool tips on line chart and table)
* Use jQuery Data Tables to make the table sortable and filterable 


#### Really Impress
* Build this in a small web app (e.g., Bootstrap)
* Make this responsive (smartphone, tablet and desktop breakpoints)
* Look around at other interesting visualizations. Come up with a better way to show this data