Data Exploration
==========

Fire Insights provide a number of features for Data Exploration


Data Exploration Processors in Fire Insights
----------------------------------------


.. list-table:: Data Exploration Processors
   :widths: 30 70
   :header-rows: 1

   * - Title
     - Description
   * - ColumnsCardinality
     - Distribution of categorical data. Calculates the count of records for each unique value for the column specified
   * - Correlation
     - Computes and displays the correlation between two series of data
   * - CrossTab
     - Displays distribution of data for all combination of Categorical data series
   * - DistinctValuesInColumn   
     - Displays distinct combination data present in the select data series
   * - Flag Outlier
     - Flag the outlier based on the selected column using Box-and-Whisker technique
   * - GraphMonthDistribution  
     - This node displays monthly distribution of data
   * - GraphWeekDayDistribution  
     - This node displays weekday wise distribution of data     
   * - GraphYearDistribution  
     - This node displays yearly distribution of data     
   * - Histogram  
     - This node displays distribution of data spread across multiple bins     
   * - NullValuesInColumn  
     - Number of Null Values in Selected Columns
   * - Skewness And Kurtosis
     - Displays Skewness (measure of symmetry) and Kurtosis (measure of whether the data are heavy-tailed or light-tailed relative to a normal distribution)
   * - Summary Statistics
     - Summary statistics provide useful information about sample data. eg: measures of spread
 
Columns Cardinality
----------------------------------------

Below is a sample workflow which contains ``Columns Cardinality`` processor in Fire Insights. It demonstrates usage of ``Columns Cardinality`` node to display Categorical distribution of data. It displays count of rows for each distinct values in the selected columns (Categories).

It does following processing of data:

*	Reads incoming Dataset
*	Displays Categorical distribution of data using ``Columns Cardinality`` node. It displays count of rows for each distinct values in the selected columns (Categories). More than one column can be seclected to display distribution of data.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Columns Cardinality Node configuration**

*	``Columns Cardinality`` node is configured as below.
*	Input of this node is the incoming dataset.
*	``Max Values To Display`` specifies the maximum Categorical data to be displayed. It denotes maximum number of distinct values in the selected columns for which count needs to be displayed.
*	Columns for which distribution needs to be displayed is to be selected in ``Column Names`` list. More than one column can be selected. Data for each columns would be displayed separately.
*	Output of this node would contain count of each distinct values in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Columns Cardinality Node output**

Output of ``Columns Cardinality`` node displaying count of distinct values for each selected columns and categorical data (count of distinct values) for each selected columns in the node.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-printnode-output1.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   
.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-printnode-output2.png
   :alt: dataexploration_userguide
   :width: 90%       	 
   
.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/columnscardinality-printnode-output3.png
   :alt: dataexploration_userguide
   :width: 90%       	 
   
Correlation
----------------------------------------

Below is a sample workflow which contains ``Correlation`` processor in Fire Insights. It demonstrates usage of ``Correlation`` node to display correlation between data of selected columns.

It does following processing of data:

*	Reads incoming Dataset
*	Displays correlation between data of selected columns using ``Correlation`` node. More than two columns can be selected to identify correlation. It displays correlation in color codes along with scale to read highly and less correlated data series.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/correlation-workflow.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/correlation-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Correlation Node configuration**

*	``Correlation`` node is configured as below.
*	Input of this node is the incoming dataset.
*	All Numeric between whom correlation is to be identified are to be selected in ``Input Column For Correlation`` list.
*	Title of the Correlation Matrix needs to be entered in ``Title``.
*	Output of this node would display correlation between all the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/correlation-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Correlation Node output**

Output of ``Correlation`` node displaying correlation between all the selected columns along with the color code. Below output displays Correlation Matrix along with Color Code Scale. Green indicates highly correlated and Red less. From the below output we can identify that ``Customer Service Calls`` and ``Churn`` are correlated.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/correlation-printnode-output.png
   :alt: dataexploration_userguide
   :width: 70%       	    
   
Cross Tab
----------------------------------------

Below is a sample workflow which contains ``Cross Tab`` processor in Fire Insights. It demonstrates usage of ``Cross Tab`` node to display distribution of data between all possible combination of all distinct values of two series.

It does following processing of data:

*	Reads incoming Dataset
*	Displays distribution of data between all possible combination of all distinct values of two series using ``Cross Tab`` node. Distribution can be displayed between any two Categorical columns from incoming dataset.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/crosstab-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/crosstab-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Cross Tab Node configuration**

*	``Cross Tab`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Any two categorical columns from incoming dataset can be selected as ``Firstcolumn`` and ``Secondcolumn``. All distinct values from ``Firstcolumn`` would be displayed as rows and all distinct values from ``Secondcolumn`` would be displayed as columns of the Table. Row count of Row and Column value combination would be displayed as distribution.
*	Output of this node would display table depicting distribution of data between two series.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/crosstab-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Cross Tab Node output**

Output of ``Cross Tab`` node displaying distribution between ``Firstcolumn`` and ``Secondcolumn`` in tabular format.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/crosstab-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Distinct Values In Column
----------------------------------------

Below is a sample workflow which contains ``Distinct Values In Column`` processor in Fire Insights. It demonstrates usage of ``Distinct Values In Column`` node to display distinct combination of values in the selected columns.

It does following processing of data:

*	Reads incoming Dataset
*	Displays distinct combination of values in the selected columns using ``Distinct Values In Column`` node. If only one column is selected then it displays Distinct values present in that column. If more than one column is selected then it displays distinct combination of values present in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/distinctval-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/distinctval-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Distinct Values In Column Node configuration**

*	``Distinct Values In Column`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Columns between which unique combination of data is to be identified are to be selected in ``Column Names`` list. One or more columns can be selected.
*	Output of this node would display distinct combination of values in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/distinctval-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Distinct Values In Column Node output**

Output of ``Distinct Values In Column`` node displaying distinct combination of values in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/distinctval-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Flag Outlier
----------------------------------------

Below is a sample workflow which contains ``Flag Outlier`` processor in Fire Insights. It demonstrates usage of ``Flag Outlier`` node to identify whether a data point is outlier in a series or not based on the lower and upper quantile set.

It does following processing of data:

*	Reads incoming Dataset
*	Identifies whether a data point is outlier in a series or not based on the lower and upper quantile set using ``Flag Outlier`` node. It can be checked against numeric columns only.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/flagoutlier-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/flagoutlier-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Flag Outlier Node configuration**

*	``Flag Outlier`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Numeric Column in which datapoints are to be identified as outlier needs to be selected in ``Input Column To Flag The Outlier`` list.
*	``Lowerquantile`` and ``Upperquantile`` values need to be entered in the respective boxes. Datapoint would be checked against these values to flag it as outlier.
*	Output of this node would display Outlier flag for the datapoint in the selected column.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/flagoutlier-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Flag Outlier Node output**

Output of ``Flag Outlier`` node displaying Outlier flag for datapoints in the selected column.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/flagoutlier-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Graph Month Distribution
----------------------------------------

Below is a sample workflow which contains ``Graph Month Distribution`` processor in Fire Insights. It demonstrates usage of ``Graph Month Distribution`` node to display monthly distribution of data.

It does following processing of data:

*	Reads incoming Dataset
*	Displays monthly distribution of data using ``Graph Month Distribution`` node. In this workflow it displays monthly distribution of count of trade executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphmthdist-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphmthdist-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Graph Month Distribution Node configuration**

*	``Graph Month Distribution`` node is configured as below.
*	Input of this node is the incoming dataset.
*	``Chart Type`` can be selected from the list based on the representation needed.
*	String columns representing Date Values need to be selected in ``Y Columns`` list. More than one value can be selected.
*	Output of this node would display monthly distribution of data present in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphmthdist-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Graph Month Distribution Node output**

Output of ``Graph Month Distribution`` node displaying monthly distribution of selected columns i.e. number of trades executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphmthdist-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   
Graph Weekday Distribution
----------------------------------------

Below is a sample workflow which contains ``Graph Weekday Distribution`` processor in Fire Insights. It demonstrates usage of ``Graph Weekday Distribution`` node to display weekday wise distribution of data.

It does following processing of data:

*	Reads incoming Dataset
*	Displays weekday wise distribution of data using ``Graph Weekday Distribution`` node. In this workflow it displays weekday wise distribution of count of trade executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphwkdaydist-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphwkdaydist-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Graph Weekday Distribution Node configuration**

*	``Graph Weekday Distribution`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output graph needs to be entered in ``Title`` box.
*	``Chart Type`` can be selected from the list based on the representation needed.
*	String columns representing Date Values need to be selected in ``Y Columns`` list.
*	Output of this node would display weekday wise distribution of data present in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphwkdaydist-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Graph Weekday Distribution Node output**

Output of ``Graph Weekday Distribution`` node displaying weekday wise distribution of selected columns i.e. number of trades executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphwkdaydist-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Graph Year Distribution
----------------------------------------

Below is a sample workflow which contains ``Graph Year Distribution`` processor in Fire Insights. It demonstrates usage of ``Graph Year Distribution`` node to display yearly distribution of data.

It does following processing of data:

*	Reads incoming Dataset
*	Displays yearly distribution of data using ``Graph Year Distribution`` node. In this workflow it displays yearly distribution of count of trade executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphyeardist-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphyeardist-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Graph Year Distribution Node configuration**

*	``Graph Year Distribution`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output graph needs to be entered in ``Title`` box.
*	``Chart Type`` can be selected from the list based on the representation needed.
*	String columns representing Date Values need to be selected in ``Y Columns`` list.
*	Output of this node would display yearly distribution of data present in the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphyeardist-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Graph Year Distribution Node output**

Output of ``Graph Year Distribution`` node displaying yearly distribution of selected columns i.e. number of trades executed.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/graphyeardist-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   
Histogram
----------------------------------------

Below is a sample workflow which contains ``Histogram`` processor in Fire Insights. It demonstrates usage of ``Histogram`` node to display distribution of data spread across multiple bins.

It does following processing of data:

*	Reads incoming Dataset
*	Displays distribution of data spread across multiple bins using ``Histogram`` node. In this workflow it displays distribution of traded volume spread across multiple bins.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/histogram-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/histogram-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Histogram Node configuration**

*	``Histogram`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output graph needs to be entered in ``Title`` box.
*	Input Column whose distribution needs to be displayed is to be selected in ``Column Name`` list.
*	Number of equally spaced bins that needs to be created is to be entered in ``Number Of Bins`` box.
*	Output of this node would display distribution of data present in the selected column spread across multiple bins.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/histogram-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Histogram Node output**

Output of ``Histogram`` node displaying distribution of data present in the selected column spread across multiple bins.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/histogram-printnode-output1.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   
.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/histogram-printnode-output2.png
   :alt: dataexploration_userguide
   :width: 90%       	    

Null Values In Column
----------------------------------------

Below is a sample workflow which contains ``Null Values In Column`` processor in Fire Insights. It demonstrates usage of ``Null Values In Column`` node identify number of Null values and its percentage against the total data length in the selected columns.

It does following processing of data:

*	Reads incoming Dataset
*	Identifies number of Null values and its percentage against the total data length in the selected columns using ``Null Values In Column`` node. 

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/nullvalincol-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/nullvalincol-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Null Values In Column Node configuration**

*	``Null Values In Column`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Columns in which null values need to be identified are to be selected in ``Column Names`` list. Multiple columns can be selected.
*	Output of this node would display number of Null values and its percentage for the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/nullvalincol-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Null Values In Column Node output**

Output of ``Null Values In Column`` node displaying number of Null values and its percentage for the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/nullvalincol-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Skewness And Kurtosis
----------------------------------------

Below is a sample workflow which contains ``Skewness And Kurtosis`` processor in Fire Insights. It demonstrates usage of ``Skewness And Kurtosis`` node to identify Skewness (measure of symmetry) and Kurtosis (measure of whether the data are heavy-tailed or light-tailed relative to a normal distribution) in the selected columns.

It does following processing of data:

*	Reads incoming Dataset
*	Identifies Skewness and Kurtosis in the selected columns using ``Skewness And Kurtosis`` node. 

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/skewness-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/skewness-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Skewness And Kurtosis Node configuration**

*	``Skewness And Kurtosis`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Columns for whom Skewness And Kurtosis need to be computed are to be selected in ``Column Names`` list. Multiple columns can be selected.
*	Output of this node would display Skewness And Kurtosis values for the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/skewness-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Skewness And Kurtosis Node output**

Output of ``Skewness And Kurtosis`` node displaying Skewness And Kurtosis values for the selected columns.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/skewness-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   

Summary Statistics
----------------------------------------

Below is a sample workflow which contains ``Summary Statistics`` processor in Fire Insights. It demonstrates usage of ``Summary Statistics`` node to compute Statistical Summary such as count, mean, min, max and so on for the selected columns.

It does following processing of data:

*	Reads incoming Dataset
*	Computes Statistical Summary such as count, mean, min, max and so on for the selected columns. using ``Summary Statistics`` node. 

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/summarystats-workflow.png
   :alt: dataexploration_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/summarystats-incoming-dataset.png
   :alt: dataexploration_userguide
   :width: 90%

**Summary Statistics Node configuration**

*	``Summary Statistics`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	Columns for whom Summary need to be computed are to be selected in ``Column Names`` list. Multiple columns can be selected.
*	Output of this node would display Statistical Summary of the columns selected.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/summarystats-config.png
   :alt: dataexploration_userguide
   :width: 90%
   
**Summary Statistics Node output**

Output of ``Summary Statistics`` node displaying Statistical Summary of the columns selected.

.. figure:: ../../_assets/user-guide/data-exploration/data-exploration/summarystats-printnode-output.png
   :alt: dataexploration_userguide
   :width: 90%       	    
   
