# Survey123 Choices to QR Codes
Dion Liddell, May 2020

## Overview
The [Survey123 Choices to QR Codes](https://github.com/localgovernment/Survey123-Choices-to-QR-Codes/blob/master/Survey123%20Choices%20to%20QR%20Codes.ipynb) Jupyter Notebook turns the Choices associated with a nominated Survey123 Dropdown Field into scannable QR Codes. Each QR Code generated represents one Choice in the Dropdown Field. Scan a generated QR Code with a modern smartphone camera, and the Survey will open in the smartphone's mobile web browser with the Dropdown Field correctly pre-populated.

The generated QR Codes could be used, for example, to help track building entry and exit movements.  Entry and Exit QR Codes could be placed on entranceways and exits: e.g. Libray Entry, Library Exit, Marketing Entry, Marketing Exit, etc...

## Procedure
This Notebook was created and tested in ArcGIS Online - [ArcGIS Online Notebooks Beta](https://www.esri.com/arcgis-blog/products/arcgis-online/analytics/arcgis-notebooks-public-beta/)

1. Create a [Survey123 survey](https://survey123.arcgis.com/) that contains a nominated Dropdown Field that has been populated with a number of Choices
2. Take note of the (random) Survey ID contained within the Survey123 URL. e.g. ```https://survey123.arcgis.com/surveys/```**{my random Survey123 ID}**```/someparameter``` 
3. When publishing the survey, before clicking Publish for the second time, click Modify Schema, and take note of the Dropdown Field's **Name** (not the label)
4. Login into your ArcGIS Online organisation, and upload the *Survey123 Choices to QR Codes* notebook. Set the notebook's runtime to *ArcGIS Notebook Python 3 Standard (3.0)*
5. Open the notebook and update the *survey_id* and *dropdown_field* settings under the *Mandatory Settings to Modify* section to reflect your Survey ID and Dropdown Field Name recorded in the steps above
6. Click the Add button within the notebook, and click the hosted feature layer related to the survey (**not** the fieldworker layer). Copy the ID of the feature layer within the generated *get* method to the *survey_flc_id* under the *Mandatory Settings to Modify* cell
7. Delete the Cell from the notebook that was created in the step above (click within the cell and then select *Edit* and then *Delete Cells*)
8. Save the changes to the notebook
9. Select *Cell* in the notebook menu and then select *Run All*
10. Scoll down below the *Main* cell to see a list of the QR Codes that have been generated
11. Select *Files* from the top toolbar, and then click on the *home* folder, and then click on each of the generated QR Codes in turn to open them in a seperate browser tab or window
12. The QR Codes can be copied, pasted and printed.  Scan each with a smartphone camera to test

## References
https://community.esri.com/groups/survey123/blog/2019/02/06/survey123-tricks-of-the-trade-web-form-url-parameters

https://pypi.org/project/qrcode/
