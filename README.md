
# RangeSlider module for ProcessWire 2.+

Forum thread:
[RangeSlider Thread](http://processwire.com/talk/topic/972-jquery-ui-range-slider-fieldtype/page__hl__rangeslider)

## How does it work

This fieldtype let's you create slider input fields in the admin
using the built in jQuery UI Slider. You can use it as a regular
single value slider, or enable range which gives you two number.

### Output the values in templates

If used as single value slider
    `echo $page->fieldname`

If ranged slider is enabled
    `echo $page->fieldname->min`
    `echo $page->fieldname->max`

### Use in selectors strings

With a regular single value slider
    `$pages->find("range=120");`

If range slider is enabled
    `$pages->find("range.min>=100, range.max<120");`


## It comes with various settings.

- range enable
- width of slider (%)
- min value
- max value
- default value
- step
- prefix for displayed value(s)
- suffix for displayed value(s)



## How to install

1. Download and place the FieldtypeRangeSlider folder in:
/site/modules/

2. In the admin control panel, go to Modules. At the bottom of the
screen, click the "Check for New Modules" button.

3. Now scroll to the RangeSlider Fieldtype module and click "Install".

4. Create a new Field with the new "RangeSlider" Fieldtype. Once saved
you can configure the fieldtype, with various options under "Details" tab.

## Upgrade Notes

from **1.0.3** to **1.0.4**

Value type of the field has changed from RangeSlider object to array. This only affects how you would set values to the field or inputfield from the API. So if you used RangeSlider previous 1.0.4 and have custom code to modify values via API, either in modules or template files, you should modify it to account for the changes.

**Before 1.0.4**

```
$page->of(false);
$page->myslider->min = 42;

$page->myrange->min = 10;
$page->myrange->max = 40;
```

**After**

```
$page->of(false);
$page->myslider = array('min' => 91);

$page->myrange->min = array('min' => 10);
$page->myrange->max = array('max' => 40);
```

Accessing the value hasn't changed and is still the same as in prior versions.


## Changelog

* __1.0.4__ : Changed value type from RangeSlider object to array. Updated Inputfield to make it work as module config field (where Fieldtype isn't used).
