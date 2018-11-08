* <span class="md-element">Dates</span> <i class="fa fa-asterisk required" title="Required"></i> {**type**: control group; **default**: nil} - A set of controls to select and set the <span class="md-element">Start Date</span> and <span class="md-element">End Date</span> of a <span class="md-panel">Time Period</span>.  

  <span class="btn btn-primary btn-xs">Pick a Fiscal Year</span> Use this select control to set both the <span class="md-element">Start Date</span> and <span class="md-element">End Date</span> of a fiscal year.  To set both dates for a fiscal year use the control to select the desired starting year.  The <span class="md-element">Start Date</span> will be set to the first day of the month for the fiscal year and the <span class="md-element">End Date</span> will be the last day of the month twelve months later. The default starting month for the fiscal year is October.  The starting month can be changed on the Settings page and will used by mdEditor for all <span class="md-panel">Time Period</span> objects until changed.  Previously defined fiscal years will not be effected.

  See [Date-Time Control](../../controls/dateTime-control.md) for details on picking dates and times using the Date-Time control.

* <span class="md-element">Identifier</span> {**type**: string; **default**: nil} - A unique identifier for this <span class="md-panel">Time Period</span>.  

  The identifier must be alphanumeric and not include special characters.  It need only be unique within the metadata record. 
  
  {% hint style='info' %}
  ISO metadata records require time period IDs.  If one is provided here it will be used by mdTranslator when writing ISO metadata.  If the <span class="md-element">Identifier</span> is left blank mdTranslator will generate a unique identifier for the <span class="md-panel">Time Period</span>.  Note that the generated time period ID may not be consistent across multiple translations by mdTranslator.
  {% endhint %}

* <span class="md-element">Description</span> {**type**: string; **default**: nil} - A brief description of any relevant information for this <span class="md-panel">Time Period</span>.  

* <span class="md-element">Time Period Names</span> {**type**: array; **default**: empty} - An array of user assigned names for this time period.  Each name is a character string.

* <span class="md-element">Interval</span> {**type**: object; **default**: empty} - An object to specify a time interval for the resource. 

    * <span class="md-element">Interval Amount</span> <i class="fa fa-asterisk required" title="Required"></i> {**type**: real; **default**: nil} - A floating point or integer value representing the temporal length. 
    * <span class="md-element">Time Unit</span> <i class="fa fa-asterisk required" title="Required"></i> {**type**: string; **default**: nil} - A value for the units of time, e.g. year, month, day, hour, minute, second. 


* <span class="md-element">Duration</span> {**type**: object; **default**: empty} - An object to specify a time duration for the resource. 

    * <span class="md-element">Year</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    * <span class="md-element">Month</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    * <span class="md-element">Day</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    * <span class="md-element">Hour</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    * <span class="md-element">Minute</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    * <span class="md-element">Second</span> {**type**: integer; **default**: nil} - A value for the unit of time.
    
  {% hint style='info' %}
  At least one duration elements is required.  More than one may also be entered.  e.g. 18 Months or 1 year, 6 months.
  {% endhint %}