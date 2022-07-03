# DSN_Energy-Hackathon-TEAM-R
The CO2 emission model was built using dataset gotten from the Canada Government official open website. The dataset contains data over a period of 7 years. There are total 7385 rows and 12 columns. This dataset is used because the brand of cars are the most common. The data is void of null values. There are few abbreviations that has been used to describe the features as given in the data description sheet. There were duplicated rows and this rows were 1103. To about false conclusion from the dataset, these rows were dropped.
Data Analysis
1.	Vehicle Model: Some of the vehicle model in the dataset consists of the name and often the type of drive train or wheel base. The efficiency of the drivetrain has a significant impact on the overall efficiency of the vehicle. The higher the efficiency of the drivetrain, the lower the fuel consumption of the vehicle (also lower CO2). The link to the used data for the pie chart is [https://github.com/faithCoder1/DSN_Energy-Hackathon-TEAM-R/blob/main/20tstcar-2021-03-02.xlsx]
 
i.	    Front Wheel Drive (FWD): This is the most common drive train is the front-wheel. Vehicle which make use of this drive wheel channel their power to the front wheels. It is most employed due to its compact system. The majority of the weight is borne by the front wheels, thus allowing for good traction. Front wheel drives are also preferred because it offers better fuel efficiency and emits less CO2 due to this lower weight. From the data from the EPA, FWD vehicles have least CO2 emission
ii.	    Rear Wheel Drive (RWD): RWD transfer all their power to the rear wheels. RWD has the advantage of providing higher horsepower and higher vehicle weights. This drive train can be found on trucks and sport cars. They have higher fuel consumption due to the vehicle weights. 
iii.	All Wheel Drive (AWD): This drive train employs the use of both front and rear wheels.  AWD vehicles work by sending power from the engine to the center of the car. The differential in the center of the car distributes power evenly between the front and rear axles. Some vehicles will divide the power a little less equally to the front or rear axles based on road conditions and which wheels have the most traction. The pie chart above, was drawn from the data obtained. It shows that AWD vehicles has second least fuel consumption.
iv.	Four Wheel Drive (4WD): 4WD does not send power to the center of the vehicle before distributing it to the front and rear axles. With 4WD, both axles move at the same speed, making handling on normal roads very difficult when 4WD is engaged. The biggest advantage of a 4WD vehicle is that it provides the versatility and power to take on any terrain or weather condition. From the pie chart, 4WD vehicles have the highest fuel consumption.
Wheel Bases:  The wheelbase is the distance between the centre point of the front wheels and the center point of the rear wheels. It differs from the length of the vehicle. The length of a vehicle is calculated from the front-most point of the vehicle to the rearmost point. There is the short wheel base (SWB), extended wheel base (EWB) and long wheel base. From the pie chart extended wheelbase has the highest fuel consumption.
Flexible Fuel vehicles (FFV): Flex-fuel vehicles are those that have internal combustion engines designed to run on more than one type of fuel. For example gasoline and ethanol. It’s fuel consumption is 
 
2.	Fuel Type:
There are five groups of fuel types as given in the dataset: Premium gasoline (Z), Diesel (D), Regular gasoline (X), Ethanol (E85) (E), Natural gas (N).
 
The highest CO2 emission is from Ethanol fuel. Most of the cars in Nigeria make use of gasoline (commonly referred to as petrol), which is very high as that from Ethanol.
3.	Cylinders: A cylinder is a vital part of the internal combustion engine. It's a chamber where fuel is combusted and power is generated. The cylinder consists of a piston and two valves at the top; an inlet and exhaust valves. The piston moves up and down, and its reciprocating motion generates power that moves your vehicle. Generally, the more cylinders an engine has, the more power is produced. Most cars have a 4, 6, or 8 cylinder engine. The numbers indicate the number of cylinders, and they will either be laid out in a straight line, V-shaped or in a flat arrangement. From the graph below we can conclude that the higher the number of cylinders, the higher the fuel consumption and CO2 emission.
  

Number of cylinders against CO2 emission
 
4.	Fuel Consumption
No doubt, fuel consumption is directly proportional to CO2 emission. This was clearly illustrated from the dataset using the plot below:
 
5.	Engine Size: 
Engine size may also be referred to as ‘engine capacity’ or ‘engine displacement’ and is the measurement of the total volume of the cylinders in the engine. The bigger the engine size, the more space there is for air and fuel inside it.
Figure of Engine size against mean CO2 emissions
 

Machine learning
The algorithm used for training the model is random forest regression algorithm. Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. The (random forest) algorithm establishes the outcome based on the predictions of the decision trees. It predicts by taking the average or mean of the output from various trees. Increasing the number of trees increases the precision of the outcome. The dataset was split into 75% train and 25% test dataset using scikit-learn train-test split. The random forest algorithm was used to fit the train dataset and the train accuracy was 98.99% and test accuracy was 97.17%. RandomizedsearchCV and GridSearch was also tested. The average error of the default random forest algorithm had the least error as shown in the table below. Cross validation of 5 folds were also used. The result is shown in the jupyter notebook:
Prediction latency is measured as the elapsed time necessary to make a prediction (e.g. in micro-seconds) while Prediction throughput is defined as the number of predictions the software can deliver in a given amount of time. The main factors that influence the prediction latency are: Number of features, input data representation and sparsity, model complexity, feature extraction. The front end and the back end code can be found in site GitHub - msughterA/dsn. The webpage was hosted on Heroku platform using GitHub. Link to the webpage is http://dsncarbon.herokuapp.com/

Notebook on training and evaluation of CO2 emission model
