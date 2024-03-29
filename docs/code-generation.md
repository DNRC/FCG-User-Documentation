# Financial Code Generation

New financial codes can be generated by logged in users with the
`Primary`, `Manager`, or `Owner` application roles. This is done on
the  `New Code` page, which can be reached by the `New Code` link in
the header menu. The link only appears when a user is logged in and
has the permission to generate financial codes.

## Information Gathered

For each financial code, there are two separate groups of
information. The first contains details about the fire incident itself, such
as its name, the state it occurred in, and the date the fire was
discovered. This information is automatically populated from IRWIN,
and is entered in the `IRWIN Information` section of the form.

The second set of information contains the information that is required by
Montana DNRC business practices and are generated by the FCG user. This
information is entered in the `Agency Information` section of the form.

## Generating A New Financial Code

Before any information can be entered, the fire year of the IRWIN
incident that the financial code will be generated for must be
selected using the `Fire Year` dropdown box at the top of the
form. Since this defaults to the current fire year, most users won't
be able to change it; it will be the only option available to
them. For users with the Owner role however, they can use this
dropdown to select a previous fire year. This ensures that the agency
information and IRWIN incidents for that year will appear as the only
options in the form.

### Searching and Selecting the IRWIN Incident

In the IRWIN Information section, there is a search bar that can be
used to search by either the incident name or unique fire
identifier. After pressing the search button, if there is only one
incident that matches the given criteria, it will automatically be
selected. If there is more than one result,
a dialog will appear listing the search results. After a incident is
selected, the search controls will disappear, and some data
fields from IRWIN will be displayed in its place. If the selected
incident needs to be changed, press the `Choose Another Incident`
button to clear out the current selection and make the search controls
appear again.

#### Assigning Multiple Financial Codes to one IRWIN Incident

If the selected IRWIN incident already has one or more financial codes
assigned to it, a message will be displayed listing the assigned codes
and some basic information about them. If current user doesn't have
the correct permissions to assign an additional financial code to an
incident, the message will have a red background, and the user will be unable to
submit the form. To help color-blind users distinguish between
warnings and errors, the icons displayed next to the message will be a
triangle if it is a warning and a circle if it is an error.

### Entering Agency Information

DNRC-specific information is entered using the `Agency Information` section
of the form. Here's a brief explanation of what each field should
contain:

Name
: A short title for what this financial code will be used for. This
  field will auto-fill and become uneditable if an IRWIN incident is
  selected. For administrative codes that don't have an IRWIN
  incident, this field must be manually filled in.

Activity Role
: The activity role type that will be associated with the
  incident. This field is required to generate a financial code.

  + __Fire Response and Support Orgs__: Fire response and support orgs
    are used to segregate costs related to the suppression of wildland
    fire incidents.  A sequential SABHRS org will be assigned in the
    90yxxx number series. All suppression incidents will have unique
    IRWIN ID’s and will pull information from INFORM.
    Examples:

    + Mutual Aid General Support
    + Direct Protection
    + Federal Support and County Assist responses
    + NRCC out of area incident response
    + NWC mobilizations
    + Severity and Staffed Station responses

  + __Fire Administrative Orgs__: Fire administrative orgs are used to
    segregate specific costs incurred by the Fire Protection Bureau and
    Forestry Division Office related to non-suppression activities.  A
    sequential SABHRS org will be assigned in the 71yxxx number
    series.  The administrative activities under this role may or may
    not have incident information in IRWIN that will be pulled from
    INFORM.
    Examples:
    + GACC wide cost shares for IMT Staging costs
    + NRCC Expanded Support and GMAC Support
    + FDO costs incurred in FEMA Fire Management Assistance Grant
      administration
    + FPB General Support to the NR GACC

  + __All Hazard Orgs__: All Hazard orgs are used to segregate costs
    related to All Hazard incidents under DES tasking, search and
    rescue requests and natural disaster FEMA missions. All hazard
    mobilizations and activities are wildland fire related. The Northern
    Rockies Coordination Center with approval from the Fire Protection
    Bureau Deputy Chief of Fire Operations, will assign orgs in the
    40yxxx number series.  All Risk incidents will have unique IRWIN
    ID’s and will pull information from INFORM.

Area
: The DNRC area that is handling the incident.

Unit
: The DNRC unit that is handling the incident.

Business Action
: A specific type of business action that can be associated with an
  incident. This field is required. The business actions available are:

  + __Direct Protection__: Incidents where DNRC is the protecting agency.
  + __Mutual Aid__: Aid provided to another protecting unit or
	jurisdiction where DNRC does not intend to recover expenses
	incurred.
  + __County Assist__: A formal request to DNRC for fire suppression
    assistance from the Board of County Commissioners within a
    Cooperating County.

  + __Other Agency__: Support/Assistance provided to another protecting
    unit or jurisdiction (in-state or out of state) where DNRC intends
    to recover expenses incurred.

  + __Severity__: Preposition incidents established to support DNRC
    staffing and wildfire preparedness efforts.

Remarks
: This text box should contain any general remarks to be associated
  with the IRWIN incident.

### Submitting the Form

Once all of the required information has been entered, the submit
button at the bottom of the form will become active and clickable. If
there are any errors when creating the form, they will be displayed in
a box above the submit button. Otherwise, the code edit dialog will
open showing the information for the incident that was just created,
including the financial code that was generated.

## Editing Existing Financial Codes

After a financial code has been created, all fields except the code's
activity role can be updated to reflect the latest changes in the
fire. To do so, open the code edit dialog by clicking on the incident
on the code list page, make the required changes, then press the
Submit button to save. On successful save, the dialog will close;
otherwise, an error message will appear detailing why the code could
not be updated.

### Voiding Financial Codes

If a code was created that should not be used for some reason, the
code can be voided and removed from the default code list view. Once
voided, the code remains in the system and can still be viewed or
reactivated. Only users with the Manager or Owner application roles
can void a financial code.

To void a code, open the code edit dialog for the code, type in a
reason why the code has being voided, then press the Void Code
button. In order to void a code, the remarks field must be updated. If
there is a problem voiding the code, an error message will appear
detailing why the code could not be voided.

To re-activate a code, use the Activate Code button that appears
instead of the Void Code button in the dialog.

### Viewing Financial Code Modification History

If a user has the Primary application role or higher, they can view
if a financial code has changed over time, and what edits were
made. To view the changes, click on the `Modification History` text
that is at the bottom of the code edit dialog to view a summary of
all of the changes made to the financial code. If a more detailed
report is needed, contact the developers to get a full report.


<!--  LocalWords:  Orgs orgs wildland SABHRS NRCC NWC GACC IMT GMAC FDO FEMA FPB DES
 -->
