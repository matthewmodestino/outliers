# outliers
Detect Numerical Outliers | .conf2017

Splunk searches to detect numerical outliers in time series metrics!

I have uploaded a sample app that contains simple dashboards depicting the timewrap and streamstats versions of the outlier searches. You will need to edit the searches in the panels to create a timechart that makes sense in your environment. 

For example, in the timewrap panels, my search begins with:

| tstats prestats=t count WHERE index=main by _time span=300s 
| timechart span=300s partial=f count 

Replace this with whatever timechart generating search makes sense for you!

I have also simply provided text files with the SPL for each method if you want to skip installing the sample app. 
