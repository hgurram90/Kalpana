% Improving Kalpana
% Jason Fleming, Seahorse Coastal Consulting, LLC
% June 2016

<!--  
~/.cabal/bin/pandoc -o improvingKalpana.pdf --variable mainfont=Georgia --latex-engine=xelatex --variable sansfont=Arial --variable fontsize=12pt --variable geometry:margin=1in improvingKalpana.md
-->

In the process of working on Kalpana, one of the deliverables was to clean
the code, where possible. The following improvements were made as part
of this deliverable: 

* Implemented command line options to replace the interactive menu driven interface.

* Allow the analyst to specify the file name separately from the file type while keeping the default file name the same as the file type.

* Enable the use of a custom logo in the kmz, to control its size either as a fraction of the display size or in pixels; and to completely omit the logo overlay.

* Generalized handling of the different file types, including differences between the handling of time varying output and the processing of min/max files, using python dictionaries. 

* Support for conversion to english units (e.g., ft instead of meters) via command line options instead of hard coding.
    
* Automate the previously hard coded labeling for the color scale, including the appropriate units.
    
* Allow the analyst to specify the datum for use in labeling the color scale.

* Added support for analyst-defined color scales using palette files.

* Tick labels on the color bar can now be specified on the command line, rather than always using the contour levels, which may cause issues when the contour levels are not evenly spaced (e.g., the blue green bathy/topo color scale).

* Enable analyst to specify the contour levels, either as a range of values and an increment, or to directly specify the individual contour levels to replace the hard coded contour levels for each
 data type.
 
* Fixed issue where the contour values themselves were not being used to interpolate the colors of the contours; the number of contour levels was used and the code assumed they were evenly spaced. The issue was corrected so that the actual contour values are now used to interpolate the colors of the specified contour levels from the palette. 

* When converting the colors from floating point RGB values to integers, replaced int() with numpy.around() to more accurately represent the integer values (int() simply truncates the decimal places). 
 
* Created reasonable default contour levels for each data type.
     
* Renamed variables, arrays, and command line arguments to be more intuitive and make Kalpana more sustainable and extensible.

* Added explanatory comments.

* Reduced repeated code in if/else/elif blocks through the use of python dictionaries to account for the differences between different file types.

* Corrected issues and incomplete implementations associated with repeated code while facilitating the extension to new file types.

* Reduced line count by 20%.
