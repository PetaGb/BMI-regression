The Obesity Risk Prediction Dataset aims to estimate obesity levels based on individuals' eating habits, physical condition, and demographic factors from Mexico, Peru, and Colombia. It consists of 2,111 records and 17 attributes, with a labelled class variable "NObesity" categorising individuals into the following obesity levels:

Insufficient Weight

Normal Weight

Overweight Level I

Overweight Level II

Obesity Type I

Obesity Type II

Obesity Type III

However, I decided to drop the "NObesity" attribute and replace it with the "BMI" (Body Mass Index) feature.  BMI provides a continuous metric for obesity that is more suited for regression-based models, offering a direct way to predict a numeric value associated with obesity rather than classifying it into categories.
Features:

Frequent consumption of high-caloric food (FAVC)

Frequency of consumption of vegetables (FCVC)

Number of main meals (NCP)

Consumption of food between meals (CAEC)

Daily water consumption (CH20)

Alcohol consumption (CALC)

Smoking status (SMOKE)

Calorie consumption monitoring (SCC)

Physical activity frequency (FAF)

Time using technology devices (TUE)

Mode of transportation (MTRANS)

