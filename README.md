
# Salesforce Interview Preparation

## Security Models

Salesforce offers several security models to control access and permissions within the platform. These include:

- Organization-Wide Defaults (OWD): Determines the default level of access users have to records in Salesforce. Options include Private, Public Read Only, Public Read/Write, and Public Read/Write/Transfer.

- Role Hierarchy: Defines a hierarchy of roles within an organization, where users at higher levels can access the records owned by users below them in the hierarchy.

- Sharing Rules: Allows administrators to extend sharing access to users in public groups or roles based on criteria.

- Manual Sharing: Allows users to share individual records with other users.

- Object-Level Security (OLS): Controls the visibility of objects to users based on their profiles.

- Field-Level Security: Controls the visibility and editability of fields on objects to users based on their profiles.

- Record-Level Security: Controls the visibility and editability of individual records to users based on criteria.

## Object-Level Security (OLS)

Object-Level Security (OLS) determines which objects users can see and interact with in Salesforce based on their profiles and permission sets.

## Organization-Wide Defaults (OWD)

OWD sets the baseline level of access for records in Salesforce, which can then be further refined using sharing rules and manual sharing.

## Lookup Relationships

Lookup Relationships are a type of relationship between two objects in Salesforce where one object has a field that holds a reference to a record in another object.

## Role Hierarchy Needs

A well-designed role hierarchy ensures that users have appropriate access to records based on their position in the organization.

## Custom Objects OWD

Custom Objects OWD allows administrators to set the organization-wide default sharing settings for custom objects.

## Sharing Rules

Sharing Rules extend sharing access to users in public groups or roles based on criteria.

## Validation Rules

Validation Rules enforce data quality standards by specifying criteria that a record must meet to be saved or updated.

## Flows/Triggers

Flows/Triggers are automation tools in Salesforce that allow you to perform actions based on predefined criteria.

## Rollups

Rollups are a way to calculate values from related records and display the results on a master record.

## Master-Detail Relationships vs Lookup Relationships

Master-detail relationships are tightly coupled and have cascading delete and security features, while lookup relationships are more loosely coupled and do not have these features.

## Custom Objects vs Custom Settings

Custom objects are used to store data, while custom settings are used to store settings or configuration data that is not frequently updated.

## Types of Custom Settings

There are two types of custom settings: hierarchy and list.

## Custom Metadata

Custom metadata allows you to create custom metadata types to store application configuration data.

## Page Layouts

Page Layouts define the layout and organization of fields, custom links, and related lists on record detail and edit pages.

## Record Type

Record Type allows you to define different sets of picklist values, page layouts, and business processes for different users.

## Picklist

Picklist is a field type in Salesforce that allows users to select a value from a list of options.

## Formula Fields

Formula Fields are fields in Salesforce that calculate their values based on specified formulas.

## Different Types of Flows

Different types of flows include screen flows, auto-launched flows, and trigger flows.

## Cascade Delete in Salesforce

Cascade delete is the automatic deletion of related records when a parent record is deleted.

## Different Types of Triggers

Different types of triggers include before triggers and after triggers.

## Trigger.old Map vs Triggers.new Map

Trigger.old contains the old versions of the records being processed, while triggers.new contains the new versions.

## After Trigger Read-Only Exception

After triggers cannot make changes to the records that fired the trigger.

## Best Practices to Write Triggers

Best practices to write triggers include using bulkified code, limiting the number of queries and DML statements, and following the trigger handler pattern.

## Why One Trigger for One Object

Having one trigger for one object helps maintain code clarity and reduces the risk of hitting governor limits.

## Null Pointer Exception

Null Pointer Exception occurs when a variable that is expected to have a value is null.

## IsBlank vs IsNull

IsBlank checks for both null and empty strings, while IsNull only checks for null.

## Async vs Sync

Async operations are performed in the background and do not block the main thread, while sync operations are performed in real-time and can block the main thread.

## Methods in Async in Apex

Methods in async in Apex include future methods and queueable methods.

## Batch Apex

Batch Apex allows you to process large sets of records asynchronously.

## Sync Apex

Sync Apex is code that is executed in real-time, in response to a user action or request.

## Different Methods in Batch Apex (Start, Execute, Finish)

In batch apex, the start method prepares the batch job, the execute method processes the records, and the finish method cleans up after the job is done.

## Default Size of Chunks

In batch apex, Salesforce processes records in chunks of 200.

## Callout Using Batch Apex

You can perform callouts from batch apex by implementing the Database.AllowsCallouts interface.

## Why We Can't Callout with Triggers (Sync)

Callouts are not allowed in synchronous operations (like triggers) because they can cause long-running transactions.

## Future Methods vs Queueable Methods

Future methods are asynchronous and executed in a separate thread, while Queueable methods allow for chaining of jobs and more control over job execution.

## Batch Apex from Future Methods

You can initiate a batch job from a future method by calling the Database.executeBatch method.

## Batch from Batch Apex

You can chain batch jobs by starting a new batch job from the finish method of another batch job.

