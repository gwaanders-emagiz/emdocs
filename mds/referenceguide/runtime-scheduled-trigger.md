---
id: runtime-scheduled-trigger
title: Runtime scheduled trigger
sidebar_label: Runtime scheduled trigger
---
#### Trigger when
Select the type of data to be evaluated

#### Evaluate only on 
Restrict the days and time when the trigger should be evaluated.

The restriction is based on the time that the monitored object sends the data, not on the time that the data arrives at the portal. Therefore, alerts may still be triggered outside the specified times.

This may be used to not trigger some alerts during the weekend or outside of working hours.

#### Trigger on
Select how to determine to which objects this triggers applies.

<b>1. all objects</b> Applies to all objects of the company in this environment.
<b>2. the following objects</b> Applies to all objects selected below.
<b>3. all objects, except for</b> Applies to all objects of the company in this environment, except for those selected below.

#### Check continuously
If checked, this trigger is evaluated continuously during the day.

If unchecked, the trigger is evaluated once a day at the specified time. Please be aware that this time is in UTC.


Enable trigger
If enabled, this trigger creates alerts for all events that match the specified rules.
The alerts are tagged with the specified tags.

These tags can be used for notification settings.

#### Auto generate summary?
If checked, the summary of this alert is automatically generated based on its attributes.

#### Auto generate short description?
If checked, the short description of this alert is generated automatically based on its attributes.

#### Auto generate description?
If checked, the description of this alert is generated automatically based on its attributes.

#### Auto generate summary?
If checked, the summary of this alert is automatically generated based on its attributes.

#### Auto generate short description?
If checked, the short description of this alert is generated automatically based on its attributes.

#### Auto generate description?
If checked, the description of this alert is generated automatically based on its attributes.

#### Auto generate summary?
If checked, the summary of this alert is automatically generated based on its attributes.

#### Auto generate short description?
If checked, the short description of this alert is generated automatically based on its attributes.

#### Auto generate description?
If checked, the description of this alert is generated automatically based on its attributes.

