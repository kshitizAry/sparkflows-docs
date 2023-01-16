Data Visualization
==========

Fire Insights provide a number of features for Data Visualization


Data Visualization Processors in Fire Insights
----------------------------------------


.. list-table:: Data Visualization Processors
   :widths: 30 70
   :header-rows: 1

   * - Title
     - Description
   * - BoxPlot
     - Represents variation between two series of data in Box Plot format
   * - Bubble Chart
     - Represents variation of data between series in Bubble Chart format
   * - Gauge
     - Represents data for different categories in Gauge format
   * - Graph Group By Column   
     - Represents count of different group of data in Graphical format
   * - Graph SubPlots
     - Represents variation between multiple pair of data series in one go in Graphical format
   * - Graph Values  
     - Represents variation between a pair of data series in Graphical format
   * - Print N Rows  
     - Prints rows from incoming dataset
   * - Print Rich Text
     - Prints output in Rich Format Text
     
Box Plot
----------------------------------------

Below is a sample workflow which contains ``Box Plot`` processor in Fire Insights. It demonstrates usage of ``Box Plot`` node to represent variation between two series of data in Box Plot format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents variation between two series of data in Box Plot format using ``Box Plot`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/boxplot-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/boxplot-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Box Plot Node configuration**

*	``Box Plot`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	X and Y Labels of the graph needs to be entered in ``X Label`` and ``Y Label`` boxes.
*	``Max Values To Display`` specifies the maximum data values to be displayed.
*	Column to be used to aggregate data is to be selected in ``Group By Column`` list.
*	Aggregated data that needs to be plotted in the graph is to be selected in ``Value Column`` list.
*	Output of this node would display variation of one data with other.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/boxplot-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Box Plot Node output**

Output of ``Box Plot`` node displaying variation of one data with other.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/boxplot-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   
Bubble Chart
----------------------------------------

Below is a sample workflow which contains ``Bubble Chart`` processor in Fire Insights. It demonstrates usage of ``Bubble Chart`` node to represent variation of data between series in Bubble Chart format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents variation between two series of data in Bubble Chart format using ``Bubble Chart`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/bubblechart-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/bubblechart-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Bubble Chart Node configuration**

*	``Bubble Chart`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	``Max Values To Display`` specifies the maximum data values to be displayed.
*	``Is Streaming`` needs to be selected as True if input is a Streaming data (Continuously generated data).
*	X and Y Labels of the graph needs to be entered in ``X Label`` and ``Y Label`` boxes.
*	Color Code needs to be selected in ``Chart Colors`` list to display data of different series in different colors.
*	Data Series that defines Bubble Label needs to be selected in ``Bubbles Label`` list.
*	Data Series that defines points of X-Coordinate needs to be entered in ``X Coordinate`` list.
*	Data Series that defines points of Y-Coordinate needs to be entered in ``Y Coordinate`` list.
*	Data Series that defines Bubble Color for each data series needs to be selected in ``Bubbles Color`` list.
*	Data Series that defines Bubble Size needs to be selected in ``Bubbles Size`` list.
*	Output of this node would display variation between data series represented in Bubble Chart format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/bubblechart-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Bubble Chart Node output**

Output of ``Bubble Chart`` node displaying variation between data series represented in Bubble Chart format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/bubblechart-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   

Gauge
----------------------------------------

Below is a sample workflow which contains ``Gauge`` processor in Fire Insights. It demonstrates usage of ``Gauge`` node to represent data for different categories in Gauge format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents data for different categories in Gauge format using ``Gauge`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/gauge-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/gauge-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Gauge Node configuration**

*	``Gauge`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	Column defining categorical data for which separate Gauge is to be displayed needs to be selected in ``Key Column`` list.
*	Column defining value in Gauge needs to be selected in ``Value Column`` list.
*	``RedFrom``, ``RedTo``, ``YellowFrom`` and ``YellowTo`` needs to be entered in the respective boxes defining Red and Yellow zone in the Gauge.
*	``MinorTicks`` defining Minor Ticks in the Gauge needs to be entered in the box.
*	Output of this node would display data for different categories in Gauge format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/gauge-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Gauge Node output**

Output of ``Gauge`` node displaying data for different categories in Gauge format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/gauge-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   
Graph Group By Column
----------------------------------------

Below is a sample workflow which contains ``Graph Group By Column`` processor in Fire Insights. It demonstrates usage of ``Graph Group By Column`` node to represent count of different group of data in Graphical format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents count of different group of data in Graphical format using ``Graph Group By Column`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphgrpbycol-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphgrpbycol-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Graph Group By Column Node configuration**

*	``Graph Group By Column`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	``X Label`` and ``Y Label`` needs to be entered with values that needs to be displayed in respective coordinates.
*	Number of Maximum data values to be displayed in the graph is to be entered in ``Max Values to Display`` box. 
*	Color Series to be used for Columns/Bars in the graph is to be selected in ``Chart Colors`` list.
*	Column that needs to be used to aggregate data is to be selected in ``Group By Column`` list.
*	Chart type to represent data in the output is to be selected in ``Chart Type`` list.
*	Output of this node would display count of different group of data in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphgrpbycol-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Graph Group By Column Node output**

Output of ``Graph Group By Column`` node displaying count of different group of data in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphgrpbycol-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   

Graph SubPlots
----------------------------------------

Below is a sample workflow which contains ``Graph SubPlots`` processor in Fire Insights. It demonstrates usage of ``Graph SubPlots`` node to represent variation between multiple pair of data series in one go in Graphical format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents variation between multiple pair of data series in one go in Graphical format using ``Graph SubPlots`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphsubplots-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphsubplots-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Graph SubPlots Node configuration**

*	``Graph SubPlots`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	Number of Maximum data values to be displayed in the graph is to be entered in ``Max Values to Display`` box. 
*	Color Series to be used in the chart is to be selected in ``Chart Colors`` list.
*	Details of the graph that needs to be plotted is to be entered in the ``Variables List``. A separate row needs to be added to each additional graph.
*	``X-Columns``, ``Y-Columns``, ``GraphTypes``, ``X Labels`` and ``Y Labels`` needs to be entered for each graph.
*	Output of this node would display variation between multiple pair of data series in one go in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphsubplots-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Graph SubPlots Node output**

Output of ``Graph SubPlots`` node displaying variation between multiple pair of data series in one go in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphsubplots-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   

Graph Values
----------------------------------------

Below is a sample workflow which contains ``Graph Values`` processor in Fire Insights. It demonstrates usage of ``Graph Values`` node to represent variation between a pair of data series in Graphical format.

It does following processing of data:

*	Reads incoming Dataset
*	Represents variation between a pair of data series in Graphical format using ``Graph Values`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphvalues-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphvalues-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Graph Values Node configuration**

*	``Graph Values`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	Text that needs to be displayed along the coordinates are to be entered in ``X Label`` and ``Y Label``
*	Number of Maximum data values to be displayed in the graph is to be entered in ``Max Values to Display`` box. 
*	Format of the output needs to be selected in ``Chart Type`` list.
*	Color Series to be used in the chart is to be selected in ``Chart Colors`` list.
*	``Is Streaming`` needs to be selected based on whether data is a continuous feed one.
*	Data Series to be displayed along X-Coordinate is to be selected in ``X Column`` list.
*	Data Series to be plotted along Y-Coordinate is to be selected in ``Y Columns`` list. Multiple data series can be selected.
*	Output of this node would display variation between a pair of data series in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphvalues-config1.png
   :alt: datavisualization_userguide
   :width: 90%
   
.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphvalues-config2.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Graph Values Node output**

Output of ``Graph Values`` node displaying variation between a pair of data series in Graphical format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/graphvalues-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   

Print N Rows
----------------------------------------

Below is a sample workflow which contains ``Print N Rows`` processor in Fire Insights. It demonstrates usage of ``Print N Rows`` node to print incoming data.

It does following processing of data:

*	Reads incoming Dataset
*	Prints incoming data using ``Print N Rows`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printnrows-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printnrows-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Print N Rows Node configuration**

*	``Print N Rows`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Title of the output needs to be entered in ``Title`` box.
*	Number of Rows to Print is to be entered in ``Num Rows To Print`` box. 
*	``Display Data Type`` needs to be set based on the need to display datatype of columns in the output.
*	Output of this node would display incoming data.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printnrows-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Print N Rows Node output**

Output of ``Print N Rows`` node displaying incoming data.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printnrows-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   

Print Rich Text
----------------------------------------

Below is a sample workflow which contains ``Print Rich Text`` processor in Fire Insights. It demonstrates usage of ``Print Rich Text`` node to print data in Rich Text format.

It does following processing of data:

*	Reads incoming Dataset
*	Print data in Rich Text format using ``Print Rich Text`` node.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printrichtxt-workflow.png
   :alt: datavisualization_userguide
   :width: 60%
   
**Incoming dataset**

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printrichtxt-incoming-dataset.png
   :alt: datavisualization_userguide
   :width: 90%

**Print Rich Text Node configuration**

*	``Print Rich Text`` node is configured as below.
*	Input of this node is the incoming dataset.
*	Text Data to be printed in the output is to be entered in ``Text`` box.
*	Format of the text needs to be set using the tool bar of the Text Box.
*	Output of this node would display incoming data in Rich Text format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printrichtxt-config.png
   :alt: datavisualization_userguide
   :width: 90%
   
**Print Rich Text Node output**

Output of ``Print Rich Text`` node displaying incoming data in Rich Text format.

.. figure:: ../../_assets/user-guide/data-exploration/data-visualization/printrichtxt-printnode-output.png
   :alt: datavisualization_userguide
   :width: 90%       	    
   
