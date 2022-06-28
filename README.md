# <p align="center" width="100%"> <img src="./logo.png" width="250" height="250"> </p> 
# <p align="center" width="100%"> Craftboxx Plan it API OIH Connector </p>

## Description

A generated OIH connector for the Craftboxx Plan it API API (version 1.1.0).

Generated from: https://api.craftboxx.de/<br/>
Generated at: 2022-06-28T12:14:06+03:00

## API Description

# Welcome!<br/>
<br/>
Here you see the documentation of plan it api.<br/>
<br/>
- If you are searching for more information to the Craftboxx itself, see [https://www.craftboxx.de](https://www.craftboxx.de).<br/>
- If you want to log into the plan-it interface, visit [https://planit.craftboxx.de](https://planit.craftboxx.de).<br/>
<br/>
## General<br/>
<br/>
- In order to use the api, you need to generate a bearer-access token /plan-it/auth/create-token with your plan-it employee credentials.<br/>
- You have to pass the access token with every api call in the header so that you are authenticated and authorized as a plan-it employee.<br/>
- Your plan it permissions also take effect in the plan it api.<br/>
- This api mostly implements the REST api logic.<br/>
<br/>
## Get / Index Requests<br/>
<br/>
- For every index request you can add a 'q' parameter, which does a generic search over all entities (Example: /articles?q=Bosch Akkuschrauber)<br/>
- For every index request you can add a 'order_by' and a 'order_direction' parameter (Example: /articles?order_by=manufacturer&order_direction=desc)<br/>
- For every index request you can also use a 'id' parameter, which only delivers you specific ids (Example: /articles?id=50 or /articles?id[]=50&id[]=51)<br/>
- For every index request you can also use a 'exclude' parameter, which exclude specific ids (Examples: /articles?exclude=50 or /articles?exclude[]=50&exclude[]=51)<br/>
- For every index request you can use the 'per_page' and 'page' parameter for pagination (Example: /articles?per_page=100&page=3)<br/>
- For every index request you can filter using the attributes. You can search and combine in array or non array syntax. Non array syntax also supports sql-like placeholders (Examples: /articles?manufacturer=Bosch% or /articles?manufacturer[]=Bosch&manufacturer[]=Makita)<br/>
- See the post or put request to see all possible attributes, because those are mostly not documented in index request<br/>
- For every index request, you can also filter relations. If you want all articles, which are part of assignment id 50, you can use for example /articles?assignments=50 or /articles?assignments[]=50&assignments[]=51 for multiple). A '500' is returned if the relation does not exist.<br/>
- For every index request, you can also count relations. If you to know, how how articles are assigned to a worksheet, you can use for example /assignments?count=articles or /assignments?count[]=articles&count[]=employees.<br/>
- For every index request you can filter by the related model's property, the related model and the property must be devided by a hyphen sign (Example: /projects?customer-customer_number=123)<br/>
- Last but not least you can use a 'with' parameter and load relations. (Example: /articles/?with=assignments or /articles/?with[]=assignments , also loads worksheets [technically: assignments]). A '500' is returned if the relation does not exist.<br/>
<br/>
## Get / Show Requests<br/>
<br/>
- For every model you can also show a specific id. (Example: /articles/50)<br/>
- If the model does not exist, you receive a '404' error code.<br/>
<br/>
## Post / Put Requests<br/>
<br/>
- Creating / Updating models happens using the POST or PUT method.<br/>
- POST creates a new model and returns the resulting model.<br/>
- PUT updates a specific model and returns a '404' if the model does not exist.<br/>
- If validation fails a '422' error code is returned.<br/>
<br/>
## Delete Requests<br/>
<br/>
- You can delete a model using the DELETE method.<br/>
- A '404' error is returned if the model does not exist.<br/>

## Authorization

Supported authorization schemes:
- Bearer Token - Enter the token only.

## Actions

### Updates a absence recurring rule

*Tags:* `Absence recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - Recurring Rule id<br/>

### Returns a specific absence recurring rule

*Tags:* `Absence recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - RecurringRule id<br/>

### Add absence

*Tags:* `Absences`

### Update absence

*Tags:* `Absences`

#### Input Parameters
* `absenceId` - _required_ - Absence id<br/>

### Returns specific absence type

*Tags:* `Absence types`

#### Input Parameters
* `typeId` - _required_ - Type id<br/>

### Add new absence type

*Tags:* `Absence types`

### Remove absence type

*Tags:* `Absence types`

#### Input Parameters
* `typeId` - _required_ - Absence type id<br/>

### Add new article group

*Tags:* `Article groups`

### Create a absence recurring rule

*Tags:* `Absence recurring rules`

### Returns specific article group

*Tags:* `Article groups`

#### Input Parameters
* `groupId` - _required_ - Article group id<br/>

### Deletes a absence recurring rule

*Tags:* `Absence recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - Recurring rule id<br/>

### Add article

*Tags:* `Articles`

### Remove article

*Tags:* `Articles`

#### Input Parameters
* `articleId` - _required_ - Article id<br/>

### Update article group

*Tags:* `Article groups`

#### Input Parameters
* `groupId` - _required_ - Group id<br/>

### Returns a specific worksheet recurring rule

*Tags:* `Worksheet recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - RecurringRule id<br/>

### Updates a specific absence type

*Tags:* `Absence types`

#### Input Parameters
* `typeId` - _required_ - Tag id<br/>

### Add new label

*Tags:* `Worksheet labels`

### Removes a worksheet label

*Tags:* `Worksheet labels`

#### Input Parameters
* `labelId` - _required_ - Tag id<br/>

### Remove absence

*Tags:* `Absences`

#### Input Parameters
* `absenceId` - _required_ - Absence id<br/>

### Returns specific label

*Tags:* `Worksheet labels`

#### Input Parameters
* `tagsId` - _required_ - Tag id<br/>

### Returns specific worksheet

*Tags:* `Worksheets`

#### Input Parameters
* `worksheetId` - _required_ - Worksheet ID<br/>

### Updates a worksheet label

*Tags:* `Worksheet labels`

#### Input Parameters
* `labelId` - _required_ - Tag id<br/>

### Removes a worksheet

*Tags:* `Worksheets`

#### Input Parameters
* `worksheetId` - _required_ - Worksheet id<br/>

### Creates and returns an access token

*Tags:* `Authentication`

### Returns specific customer address

*Tags:* `Customer addresses`

#### Input Parameters
* `addressId` - _required_ - Address id<br/>

### Create a worksheet recurring rule

*Tags:* `Worksheet recurring rules`

### Add customer address

*Tags:* `Customer addresses`

### Updates a specific worksheet

*Tags:* `Worksheets`

#### Input Parameters
* `worksheetId` - _required_ - Worksheet ID<br/>

### Returns specific customer

*Tags:* `Customers`

#### Input Parameters
* `customerId` - _required_ - Customer id<br/>

### Remove customer address

*Tags:* `Customer addresses`

#### Input Parameters
* `addressId` - _required_ - Address id<br/>

### Update customer

*Tags:* `Customers`

#### Input Parameters
* `customerId` - _required_ - Customer id<br/>

### Update article

*Tags:* `Articles`

#### Input Parameters
* `articleId` - _required_ - Article id<br/>

### Returns specific absence

*Tags:* `Absences`

#### Input Parameters
* `absenceId` - _required_ - Absence id<br/>

### Update customer address

*Tags:* `Customer addresses`

#### Input Parameters
* `addressId` - _required_ - Address id<br/>

### Returns specific document

*Tags:* `Documents`

#### Input Parameters
* `documentsId` - _required_ - Document id<br/>

### Add new document

*Tags:* `Documents`

### Returns specific signature template

*Tags:* `Documentation signature templates`

#### Input Parameters
* `signatureTemplateId` - _required_ - Signature template id<br/>

### Remove signature template

*Tags:* `Documentation signature templates`

#### Input Parameters
* `signatureTemplateId` - _required_ - Signature template id<br/>

### Add documentation to specified assignment

*Tags:* `Documentations`

### Deletes a specific documentation

*Tags:* `Documentations`

#### Input Parameters
* `documentationId` - _required_ - Documentation ID<br/>

### Update document

*Tags:* `Documents`

#### Input Parameters
* `documentId` - _required_ - Document id<br/>

### Remove customer

*Tags:* `Customers`

#### Input Parameters
* `customerId` - _required_ - Customer id<br/>

### Deletes a worksheet recurring rule

*Tags:* `Worksheet recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - RecurringRule id<br/>

### Updates a documentation

*Tags:* `Documentations`

#### Input Parameters
* `documentationId` - _required_ - Documentation id<br/>

### Updates a signature template

*Tags:* `Documentation signature templates`

#### Input Parameters
* `signatureTemplateId` - _required_ - Signature template id<br/>

### Returns specific employee group

*Tags:* `Employee groups`

#### Input Parameters
* `groupId` - _required_ - Employee group id<br/>

### Remove document

*Tags:* `Documents`

#### Input Parameters
* `documentId` - _required_ - Document id<br/>

### Add new employee group

*Tags:* `Employee groups`

### Remove employee group

*Tags:* `Employee groups`

#### Input Parameters
* `groupId` - _required_ - Employee group id<br/>

### Update employee

*Tags:* `Employees`

#### Input Parameters
* `employeeId` - _required_ - Employee id<br/>

### Returns specific icon

*Tags:* `Icons`

#### Input Parameters
* `iconId` - _required_ - Icon id<br/>

### Returns specific employee

*Tags:* `Employees`

#### Input Parameters
* `employeeId` - _required_ - Employee id<br/>

### Update employee group

*Tags:* `Employee groups`

#### Input Parameters
* `groupId` - _required_ - Group id<br/>

### Add employee

*Tags:* `Employees`

### Returns a specific desktop notficiation

*Tags:* `My`

#### Input Parameters
* `notificationId` - _required_ - Notification id<br/>

### Save information of the logged in employee

*Tags:* `My`

### Removes desktop notificiation

*Tags:* `My`

#### Input Parameters
* `notificationId` - _required_ - Notification id<br/>

### Removes all desktop notificiation

*Tags:* `My`

#### Input Parameters
* `created_at_before` - _optional_ - If provided, only desktop notifications before this datetime will be deleted<br/>

### Add project

*Tags:* `Projects`

### Update project

*Tags:* `Projects`

#### Input Parameters
* `projectId` - _required_ - ProjectId ID<br/>

### Remove article group

*Tags:* `Article groups`

#### Input Parameters
* `groupId` - _required_ - Article group id<br/>

### Updates specific timesheet

*Tags:* `Timesheets`

#### Input Parameters
* `timesheetId` - _required_ - Timesheet ID<br/>

### Update project

*Tags:* `Projects`

#### Input Parameters
* `projectId` - _required_ - Project id<br/>

### Returns specific article

*Tags:* `Articles`

#### Input Parameters
* `articleId` - _required_ - Article id<br/>

### Returns specific project

*Tags:* `Projects`

#### Input Parameters
* `projectId` - _required_ - Project id<br/>

### Remove timesheet

*Tags:* `Timesheets`

#### Input Parameters
* `timesheetId` - _required_ - Timesheet id<br/>

### Returns specific tool group

*Tags:* `Tool groups`

#### Input Parameters
* `groupId` - _required_ - Tool group id<br/>

### Add time sheet

*Tags:* `Timesheets`

### Returns specific timesheet

*Tags:* `Timesheets`

#### Input Parameters
* `timesheetId` - _required_ - Timesheet id<br/>

### Update tool group

*Tags:* `Tool groups`

#### Input Parameters
* `groupId` - _required_ - Group id<br/>

### Remove tool group

*Tags:* `Tool groups`

#### Input Parameters
* `groupId` - _required_ - Tool group id<br/>

### Remove tool

*Tags:* `Tools`

#### Input Parameters
* `toolId` - _required_ - Absence id<br/>

### Returns specific vehicle

*Tags:* `Vehicles`

#### Input Parameters
* `vehicleId` - _required_ - Vehicle id<br/>

### Returns specific tool

*Tags:* `Tools`

#### Input Parameters
* `toolId` - _required_ - Tool id<br/>

### Update tool

*Tags:* `Tools`

#### Input Parameters
* `toolId` - _required_ - Tool id<br/>

### Updates vehicle

*Tags:* `Vehicles`

#### Input Parameters
* `vehicleId` - _required_ - Vehicle id<br/>

### Returns specific upload

*Tags:* `Uploads`

#### Input Parameters
* `uploadId` - _required_ - Upload id<br/>

### Add new tool

*Tags:* `Tools`

### Updates a worksheet recurring rule

*Tags:* `Worksheet recurring rules`

#### Input Parameters
* `recurringRuleId` - _required_ - Recurring Rule id<br/>

### Add new tool group

*Tags:* `Tool groups`

### Add worksheet

*Tags:* `Worksheets`

### Add new signature template

*Tags:* `Documentation signature templates`

### Remove employee

*Tags:* `Employees`

#### Input Parameters
* `employeeId` - _required_ - Employee id<br/>

### Add customer

*Tags:* `Customers`

### Remove vehicle

*Tags:* `Vehicles`

#### Input Parameters
* `vehicleId` - _required_ - Vehicle id<br/>

### Marks all desktop notificiation as read

*Tags:* `My`

#### Input Parameters
* `created_at_before` - _optional_ - If provided, only desktop notifications before this datetime will be marked as read<br/>

### Add vehicle

*Tags:* `Vehicles`

### Returns specific documentation

*Tags:* `Documentations`

#### Input Parameters
* `documentationId` - _required_ - Documentation id<br/>

## License

: Craftboxx<br/>
                    <br/>

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
