# data-forecast
A chart on Youtube Video views &amp; prediction
<h1>YouTube Channel Views Forecast</h1>

<p>This repository provides a forecast for a YouTube channel's daily views, including predicted view counts and confidence intervals to help understand future trends. The data includes actual recorded views, forecasted views, and a confidence interval range for future dates.</p>

<h2>Dataset Overview</h2>

<p>The forecast data is organized into multiple sheets with relevant information for past and future views. Here is a breakdown:</p>

<ul>
  <li><strong>Historical Data and Forecast (Sheet3)</strong>:
    <ul>
      <li><strong>Date</strong>: The date of the data entry.</li>
      <li><strong>Views</strong>: Actual daily view count for the channel.</li>
      <li><strong>Forecast(Views)</strong>: Predicted daily views based on historical trends.</li>
      <li><strong>Lower Confidence Bound (Views)</strong>: The lower boundary of the forecasted views, providing a range for uncertainty.</li>
      <li><strong>Upper Confidence Bound (Views)</strong>: The upper boundary of the forecasted views.</li>
    </ul>
  </li>
  <li><strong>Additional View Records (Sheet1)</strong>:
    <p>Contains additional or unprocessed view data which can be used for comparison or extended analysis.</p>
  </li>
  <li><strong>Data Validation</strong>:
    <p>Contains validation checks and formulas to verify forecast accuracy and view predictions over time.</p>
  </li>
</ul>

<h2>Project Structure</h2>

<ul>
  <li><strong>Forecast data.xlsx</strong>: The primary dataset, including past view records and future forecasted values with confidence intervals.</li>
  <li><strong>Scripts Folder</strong>: (Optional) You can add analysis scripts here to automate the processing or updating of forecasts.</li>
</ul>

<h2>Analysis Methodology</h2>

<p>The forecast was created by analyzing historical view trends and applying a forecasting model to predict future view counts. Confidence intervals were calculated to provide a range of uncertainty, giving a more realistic prediction for future views.</p>

<h2>Usage</h2>

<ol>
  <li>Clone the repository and download the dataset.</li>
  <li>Use the data in <code>Sheet3</code> for the most complete and organized forecast information.</li>
  <li>Visualize and analyze the forecast trends using any data analysis tool (such as Python with Pandas and Matplotlib).</li>
</ol>

<h2>Example Visualization</h2>

<p>To create a simple plot of historical and forecasted views:</p>

<pre>
<code>
import pandas as pd
import matplotlib.pyplot as plt

# Load data from Excel
data = pd.read_excel('Forecast data.xlsx', sheet_name='Sheet3')

# Plot actual views and forecasted views
plt.plot(data['Date'], data['Views'], label='Actual Views')
plt.plot(data['Date'], data['Forecast(Views)'], label='Forecasted Views')
plt.fill_between(data['Date'], data['Lower Confidence Bound(Views)'],
                 data['Upper Confidence Bound(Views)'], color='gray', alpha=0.3, label='Confidence Interval')
plt.xlabel('Date')
plt.ylabel('Views')
plt.title('YouTube Channel Views Forecast')
plt.legend()
plt.show()
</code>
</pre>

![image](https://github.com/user-attachments/assets/e0f609ae-b083-468e-b5aa-6d4b84398574)
![image](https://github.com/user-attachments/assets/5f654fbe-96b0-4175-afc4-393fab7dce79)



<p>Feel free to open issues or submit pull requests if you would like to add additional features or improve the forecast accuracy.</p>

<h2>License</h2>

<p>This project is open source and available under the MIT License.</p>
