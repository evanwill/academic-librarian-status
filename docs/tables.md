# Table visualization

Powered by DataTables, https://datatables.net/ 

Using [DataTables Download](https://datatables.net/download/index), we package a variety of plugins/Extensions with the asset (Bootstrap 4 styling, Buttons + HTML5 export + JSZip, minified and concatenated).

`_config.yml` provides the basic options. 
The fields listed in the config will become the columns of the table.

DataTables is set up in `/_includes/js/table-sheets-js.html`. 
It loads the Google Sheet using ajax which optimizes initial page load time. 
Options are set to optimize for large data sets (deferRender, paging). 

DataTables Buttons extension with HTML5 Export and JSZip is used to add download/export buttons to the web table. 
Clicking the CSV or Excel button will export the current subset of metadata displayed on the web table. 
The export will automatically include a Link column with full link to the 
