# Financial Code Generator User Documentation

The Finacial Code Generator is a web application used for generating
state financial codes for tracking state expenses related to wildfire
incidents that the state has a financial interest in. The application
also displays information about each fire incident from the Integrated
Reporting of Wildland-Fire Information (IRWIN) service and provides
some reporting capability.

## Viewing Incident Information

All users of the site have access to basic incident information
without needing to login. There are two separate types of financial
codes: those that are generated during the fire year and may be
associated with an incident from IRWIN, and codes that are specified
at the beginning of the fire year.

The default page shows the list of codes generated throughout the fire
year. Click on an row to view more information about individual
incidents. A modal will appear that shows additional DNRC specific
information as well as more information about the associated IRWIN
incident if one is present. Click on the close button or outside of the
modal to close it.

The other page shows the preseason admin codes. This can be accessed
using the `Admin Codes` link on the application header bar. If there
are no pre-season codes added for the year, no categories will be shown.

## Requesting elevated permissions

In order to view full incident information and create new
finacial codes, you must login to the application and submit a request
to have access.

1. Login to the application using the login button to the right in the
   header. You will be directed to okta.loginmt.com where you can log
   in to the application using a choice of authentication providers.
2. Once logged in, go to your user profile by clicking on or hovering
   over your name on the header bar to the right where the login
   button was, then clicking on `View Profile`. This page shows your
   current application role and the permissions that you currently have.
3. Click on the `Request Elevated Role` button and fill out your
   desired application role and the reason why you need access. If you
   have already submitted a role request, this will show the
   information about your pending request.

Once you have submitted a request, one of the application
administrators will either approve or deny your request.
