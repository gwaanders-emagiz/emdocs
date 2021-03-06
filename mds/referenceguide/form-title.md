---
id: form-title
title: Form Title
sidebar_label: Form Title
---
#### Alias (optional)
<i>Optional.</i> Name of the filter that will appear in the list with filtered elements. If empty a name will be generated based on the filter.

#### Select
Specify a filter to determine which element should be used.

#### Select
Specify a filter to determine which element should be used.


True for 'qualified'.
False for 'unqualified'


True for 'qualified'.
False for 'unqualified'

#### Input type:
<b>Input field</b>
Directly map a field of the input definition.

<b>Static value</b>
Use a constant value that will always be mapped. This value is not dependent on any value of the input definition.

<b>Variable</b>
Select or create a variable to map.

<b>Calculated from environment</b>
Use a value that is dependent on the environment instead of the input, such as the current date/time.

<b>Part of value</b>
Map a part of the value of a field of the input definition. Choose or configure a transformation method to apply on the field of the input definition.

<b>Value mapping</b>
Use a predefined mapping function to determine the value that should be mapped.

<b>Concatenate values</b>
Build up a string of various values separated by a constant symbol that should be mapped.

<b>Choice</b>
Use multiple conditional tests to determine which of the values should be mapped.

<b>Logical operation</b>
Use a condition to determine the value that should be mapped. <i>Can be used for boolean output only.</i>

<b>Mathematical operation</b>
Use a mathematical operation (such as multiplying, dividing) to determine the value that should be mapped.

<b>Custom XPath</b>
Manually specify the whole XPath query. Only use if none of the above options is appropriate.

#### List aggregation:
Choose the list aggregation method to use.

#### List aggregation:
Choose the list aggregation method to use.

Position of the value to use in the list.
The first value has position 1.

#### Select at position = 
Position of the value to use in the list.

The first value has position 1.


Specify whether the field should be mapped only if it meets the conditions. When set to <code>true</code> and it does not meet the conditions, the field will not be mapped.

#### Selected variable:
Select or create the variable to map.

#### XPath output type:
Output type of the XPath query.


The XPath query. You can use variables (if defined below) by the construct $name, where name is the variable name.


Add variables to use in the custom XPath query. Refer to the variable by the construct $name, where name is the variable name.

#### Selected Attribute:
Select the field of the input defintion to map.

#### Date format:
Specify the pattern in which the input date is given.

#### Custom format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.

#### DateTime format:
Specify the pattern in which the input date/time is given.

#### Custom format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.

#### Time format:
Specify the pattern in which the input time is given.

#### Custom format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.

#### Decimals:
The number of decimal places the round the input to. If empty it uses the number of decimals of the input.


Use comma as decimal separator
If <code>true</code> uses comma as a decimal separator (European format). Default is <code>false</code>, a dot will be used as decimal separator then.


Normalize spaces
If <code>true</code> removes leading and trailing spaces from the specified string, and replaces all internal sequences of white space with one.


Choose 'Add input' to specify an input for the concatenation.

Choose 'Addl ist' to add a list of values ot the concatenation.

Choose 'Add static value' to add an static value to the concatenation.

#### Separated by:
The separator to separate the input fields by.

#### Input:
Select the field of the input defintion to map a part of.

#### Transformation:
Choose the transformation to apply to the input. Click '+' to specify a new transformation. Click '...' to view or edit previously specified transformations.

#### Input 1:
Specify the first input of the mathematical operation.

#### Operation:
Choose the mathematical operation to apply.

Division by zero will return INF.

#### Input 2:
Specify the first input of the mathematical operation.


Add an input to the choice.

#### Otherwise:
Specify the value to map if none of the above inputs will be mapped due to their conditions.


Add a condition to the logical operation.


Specify whether all conditions (<code>and</code>) or minimal one condition (<code>or</code>) should be met.

#### Round
Choose the method to round the number.

#### Round
Choose the method to round the number.


Part of time
Map the hours, minutes or seconds portion of the input.

Hours as an integer between 0 and 23 inclusive.
Minutes as an integer between 0 and 59 inclusive.
Seconds as an integer between 0 and 60 inclusive.

#### Input:
Select the field of the input defintion to apply the value mapping on.


Choose the mapping function to use.


Choose the direction of the mapping function to use. You can choose whether the mapping:
1. Returns the CDM code, based on a system code given in the input ("Lookup CDM code"), or
2. Returns the system code, based on a CDM code given in the input ("Lookup system code").


#### System:
The system the code is specified for.

This value needs to match exactly the value used in the mapping web services that are made from eMagiz message flows.

#### Code type:
The code type of this system code.

This value needs to match exactly the value used in the mapping web services that are made from eMagiz message flows.

#### Exception on empty:
Whether to return an exception on empty or not.

#### Input date format:
Specify the pattern in which the input date is given.

#### Custom date format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.

#### Input dateTime format:
Specify the pattern in which the input date/time is given.

#### Custom dateTime format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.

#### Input time format:
Specify the pattern in which the input time is given.

#### Custom time format:
Use a string following the <a href="http://joda-time.sourceforge.net/api-release/org/joda/time/format/DateTimeFormat.html?is-external=true" target="_blank">DateTimeFormat pattern syntax</a>.


Next working day
If <code>true</code> the next working day of the input will be calculated.


Choose whether to check the existence of the field (field), the value of the field (value) or the length of the field (length).

Checking the value of a non-existing field returns <code>false()</code>.


Round
Choose the method to round the number.


Nr of decimals
The number of decimal places the round the input to.


Round
Choose the method to round the number.


Nr of decimals
The number of decimal places the round the input to.


Part of time
Map the hours, minutes or seconds portion of the input.

Hours as an integer between 0 and 23 inclusive.
Minutes as an integer between 0 and 59 inclusive.
Seconds as a decimal between 0 and 60 inclusive.

