Range Slider Abstractor module for ProcessWire 2
=====================================================================

WHAT IT DOES
------------

This fieldtype let's you create slider input fields in the admin
using the built in jQuery UI Slider.
You can use it as a regular single or enable range slider.

In the template you can simply output the value using

If used as single value slider
echo $page->fieldname

if ranged slider is enabled
echo $page->fieldname[0]
echo $page->fieldname[1]


It comes with various settings. 

- range enable
- width of slider (%)
- min value
- max value
- default value
- step
- prefix for displayed value(s)
- suffix for displayed value(s)



HOW TO INSTALL
--------------

1. Download and place the RangeSLider folder in:
/site/modules/

2. In the admin control panel, go to Modules. At the bottom of the
screen, click the "Check for New Modules" button. 

3. Now scroll to the RangeSlider Fieldtype module and click "Install".

4. Create a new Field with the new "RangeSlider" Fieldtype. Once saved
you can configure the fieldtype, with various options under "Details" tab.
