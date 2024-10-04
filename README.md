This tool provides a simple interface for counting crop harvests based on selected crop, harvest month, and year. It integrates with QGIS, using existing layers such as 'Plot Information Table' and a crop cycle layer ('1'), to calculate the total number of crops to be harvested and estimate their yields.

Features
Dropdown menu for selecting crops, harvest month, and year.
Displays the total number of crops to be harvested within the specified period.
Estimates the total yield based on crop type and plot area.
Lists the plot owners/tenants responsible for harvesting, along with the estimated yield from their plots.
Prerequisites
QGIS 3.x installed.
PyQt5 installed.
The following layers should be loaded in the QGIS project:
'1': Crop Cycle Layer (contains crop planting and harvest data).
'Plot Information Table': Plot Information Layer (contains plot area and owner/tenant information).
Usage
Run the script in the QGIS Python console or as a standalone PyQt5 application.
The interface will allow you to select:
A crop from the dropdown list.
The harvest month and year.
Click the "Count Crops" button to see:
The number of crops scheduled for harvest.
The estimated total yield (in kg).
A list of plot owners/tenants with their estimated yield.
Click "Close" to safely exit the tool.
Example Layers
The tool uses two layers in QGIS:

Crop Cycle Layer ('1'): Contains fields like CROP_PLANTED, DATE_OF_HARVEST, and PLOT_ID.
Plot Information Table: Contains fields like ID, AREA, owner/tenant, and brgy.
Functions Overview
clear_memory(): Resets the global references to layers to avoid crashes.
count_crops(): Processes the selected crop, month, and year, then retrieves relevant data from QGIS layers to calculate the total harvest and yield.
close_app(): Safely closes the application without crashing QGIS.
create_window(): Creates the user interface with dropdown menus, buttons, and labels.
