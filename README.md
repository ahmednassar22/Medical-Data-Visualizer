# Medical-Data-Visualizer
The rows in the dataset represent patients and the columns represent information like body measurements, results from various blood tests, and lifestyle choices. You will use the dataset to explore the relationship between cardiac disease, body measurements, blood markers, and lifestyle choices.

Create a chart similar to examples/Figure_1.png, where we show the counts of good and bad outcomes for the cholesterol, gluc, alco, active, and smoke variables for patients with cardio=1 and cardio=0 in different panels.

Use the data to complete the following tasks in medical_data_visualizer.py:

<ul>
  <li>Add an overweight column to the data. To determine if a person is overweight, first calculate their BMI by dividing their weight in kilograms by the square of their height in meters. If that value is > 25 then the person is overweight. Use the value 0 for NOT overweight and the value 1 for overweight.<\li>
  <li>Normalize the data by making 0 always good and 1 always bad. If the value of cholesterol or gluc is 1, make the value 0. If the value is more than 1, make the value 1.<\li>
  <li>Convert the data into long format and create a chart that shows the value counts of the categorical features using seaborn's catplot(). The dataset should be split by 'Cardio' so there is one chart for each cardio value. The chart should look like examples/Figure_1.png.<\li>
<li>Clean the data. Filter out the following patient segments that represent incorrect data:
    <ul>
      <li>diastolic pressure is higher than systolic (Keep the correct data with (df['ap_lo'] <= df['ap_hi']))<\li>
      <li>height is less than the 2.5th percentile (Keep the correct data with (df['height'] >= df['height'].quantile(0.025)))<\li>
      <li>height is more than the 97.5th percentile<\li>
      <li>weight is less than the 2.5th percentile<\li>
      <li>weight is more than the 97.5th percentile
  
<li>Create a correlation matrix using the dataset. Plot the correlation matrix using seaborn's heatmap(). Mask the upper triangle. The chart should look like examples/Figure_2.png.<\li>
