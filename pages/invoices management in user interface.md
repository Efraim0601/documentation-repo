## Help for Find Invoices

The default screen is for the Invoices tab is 'Find Invoices'. It is used to locate existing invoices that have been created automatically by the system or manually by the user. It can also be used to create a new Sales or Purchase Invoice.
- ### How do I view all invoices?
	- <li>Press the 'Search' button to view all invoices</li>
	-
- ### How do I locate an existing invoice?
	- <ol><li>Enter the 'Invoice ID' if known</li><li>Enter a word from the invoice description in the 'Description' field if known</li><li>Enter the 'Invoice Type' if known (NOTE: In most cases for a Sales Invoices this will be Company. For Purchase Invoice it will be the supplier party id)</li><li>Enter the 'From Party Id' if known</li><li>Enter the 'Billing Account Id' if known</li><li>Enter the invoice status in the 'Status Id' field if known</li><li>Enter the 'To Party Id' if known </li>(NOTE: In most cases for a Purchase Invoice this will be company. For Sales Invoices it will be the customer party id)<li>Press the 'Search' button to view all invoices</li><li>All invoices that meet the search criteria will be displayed.</li></ol>
	-
- ### How do I update an invoice?
- <ol><li>Locate the invoice using the 'Find Invoices' screen</li><li>sing the relevant sub menu make the required changes.</li></ol>
- ### How do I delete an invoice?
  
  Invoices cannot be deleted through the user interface. They can only be cancelled (eg if they have been entered or created by mistake).
- #+BEGIN_IMPORTANT
  They can probably be deleted using Entity Data Maintenance in the Webtools menu but this is not recommended for 2 reasons:
  1) It may cause data integrity problems.
  2) In case of audit it would be a problem.
  #+END_IMPORTANT
- ## Help for Invoice Overview
- The Invoice Overview screen is used to display the summary of an invoice in a single view. The screen is divided into sections that show various information related to the invoice (eg Roles, Status, Terms, Items, Payments Applied, etc).
- The following options are currently available from this screen:
- <ul><li>Create New (Create a new invoice)</li><li>Copy (Create a copy of the current invoice)</li><li>PDF (View a PDF of the current invoice)</li><li>PDF default currency</li>NOTE TO CHECK: Need to see how this is different from just the PDF view…​…​)<li>Status to 'Approved' (Change the status of the current invoice to 'Approved)</li><li>Status to 'Sent' (Change the status of the current invoice to 'Sent')</li><li>Status to 'Ready' (Change the status of the current invoice to 'Ready'.</li><li>NOTE: This will create the relevant accounting transactions and post them to the general ledger)</li><li>Status to 'Cancelled' (Change the status of the current invoice to 'Cancelled')</li><li>Save as Template</li>(NOTE TO CHECK: Save the current invoice format as a template)</ul>
- ### Help for Edit Invoice Header
- The Invoice Header screen is used to view or update details from the invoice header.
- Examples of the type of information that can be changed are Due Date, Description, Currency.
	- #### How do i update the header details for an invoice ?
	- <ol><li>Select the 'Header' sub menu and the header details of the invoice will be displayed</li><li>Update the fields required</li><li>Press the 'Update' button</li></ol>
- ### Help for New Invoice
- This screen allows the user to create a new Sales or Purchase Invoice.
  Sales Invoices are created when a customer buys something from you.
  Purchase Invoices are created when you buy something from a supplier.
	- #### How do i create a new sales invoices?
	- <ol><li>Press the 'Create New' button</li><li>The New Sales Invoice / New Purchase Invoice screen is displayed</li><li>Using the top part of the screen, leave Invoice type with its default of 'Sales Invoice'</li><li>Leave 'Organization Party Id' with its default of 'Company'</li><li>Enter or use the lookup to find the 'To Party Id' (eg DemoCustomer)</li><li>Press the 'Create' button in the top part of the screen</li><li>The invoice header has been created and the default header screen will be displayed</li><li>Details on the invoice will need to be entered via the other sub menus (eg Items, Time Entries etc)</li></ol>
	- #### How do i create a new Purchase invoice ?
	- <ol><li>Press the 'Create New' button</li><li>The New Sales Invoice / New Purchase Invoice screen is displayed</li><li>Using the bottom part of the screen, leave Invoice type with its default of 'Purchase Invoice'</li><li>Leave 'Organization Party Id' with its default of 'Company'</li><li>Enter or use the lookup to find the 'From Party Id' (eg DemoSupplier)</li><li>Press the 'Create' button in the bottom part of the screen</li><li>The invoice header has been created and the default header screen will be displayed</li><li>Details on the invoice will need to be entered via the other sub menus (eg Items, Time Entries etc)</li></ol>
- ### Help for Edit Invoice Applications
- The Invoice Applications sub menu is where payments that have been made (or received) can be linked or allocated to an invoice.
  The phrase 'applying' an amount to an invoice is often used to describe this.
- The screen is divided into 3 main areas as follows.
-
- <ul><li>Payments Applied (which shows details of the total amount 'Applied' and the total amount 'Open'.
  Note that 'Open' here means outstanding)</li><li>Possible Payments to Apply (which shows all the payments that have been sent from the same party id as the invoice, for a sales invoice this would be the customer party id)</li><li>Assign Payment to Invoice (which allows you to manually assign a specific payment id to this invoice)</li></ul>
- #+BEGIN_NOTE
  General Ledger accounting transactions are generated during the payment application process but unless your GL is setup with Unapplied Cash and Applied Cash accounts
  - I’m not sure that there will be any true accounting impact.
  In the Sales Order process the accounting transaction generated the following GL Accounting transaction is generated for 'Payment Applied' o add some text here.
  #+END_NOTE
- DR 120000 Accounts Receivable / CR 120000 Accounts Receivable - This transaction doesnt really do anything!
- It is used to link payments to invoices. It is also used to allocate which part of a payment is allocated or applied to a specific invoice. This is extremely useful if your customers pay multiple invoices with a single payment.
- #+BEGIN_EXAMPLE
  Example:
  - Acustomer could send a single payment of $1000 that can be used to pay for two invoices (eg $400 and $600)
  -  Using this applications sub menu allows you to allocate part of the $400 to one invoice and the balance ($600) to the other invoice
  #+END_EXAMPLE
-
- By default all 'unapplied' payments that have been entered into APOGEE from the customer will be available for selection even if they have not yet been flagged as formally 'Received'. This means that these are payments that have not already been linked to another invoice.
- If only part of a payment amount has been linked to an invoice then the remaining amount is left available to be allocated to another invoice.
  Also note that a single invoice could be paid by multiple payments being applied to it.
-
	- #### How do I apply a payments or (payments) to an invoice ?
	- <ol><li>Select the 'Applications' sub menu for the invoice</li><li>A list of unapplied payments for the party id will be displayed</li><li>Press the 'Apply' button next to the entry that needs to be applied to the invoice</li>(NOTE: More than one entry may be used. Also only part of a larger amount may be used)  
	   The Payments Applied total at the top of the screen will be updated with the amount selected. Also the Amount Open will be reduced by the amount selected.<li>Once the total invoice amount has been selected a message will be displayed and only the first part of the screen will be displayed</li><li>The top part of the screen will now be updated to show the 'Payments Applied' total is equal to the invoice total and the 'Amount Open' is zero.</li></ol>
-
	- #### How do I update an applied payment for an invoice?
	- <ol><li>Payments that have been applied to an invoice can be updated. This means that you can change the details of the payment transaction or adjust the amount that was applied to the invoice.</li><li>Select the 'Applications' sub menu for the invoice</li><li>A list of payments already applied to the invoice will be displayed in the top part of the screen</li><li>Enter or use the lookup to change the 'Payment Id' if required</li><li>Enter the updated amount in the 'Amount to Apply' field if required</li><li>Press the 'Update' button</li></ol>
-
- #### How do I remove an applied payment (or payments) from an invoice ?
- #+BEGIN_WARNING
  TO CHECK: It can be done before transaction has been posted to GL but also need to check if its can be done if the transaction has been posted.
  #+END_WARNING
	- <ol><li>Select the 'Applications' sub menu for the invoice</li><li>A list of payments already applied to the invoice will be displayed in the top part of the screen</li><li>Press the 'Remove' button next to the payment entry that needs to be removed</li><li>The entry will be removed and the top part of the screen will be update the 'Payments Applied' total and 'Amount Open'</li></ol>
-
- ### Help for Edit Invoice Items
- The Invoice Items screen displays the individual invoice line details and allows the user to update or remove an entry. As each invoice line is created it is allocated a specific sequence (or Item Number) which acts as a unique identifier.
-
	- #### How do I create a new invoice line item?
	  Note that only invoices that have specific statuses can have new line items created. This means that if an invoice has already been paid and processed APOGEE will not allow any amendments to it.
	-
	- <ol><li>Select the 'Items' sub menu for the invoice</li><li>The 'Add a new invoice item' screen will be displayed</li><li>Leave the 'Item No' field blank (as it will be automatically generated)</li><li>Select the 'Invoice Item Type' from the drop down box</li>(NOTE: A typical line using the demo could be 'Invoice Finished Good Item' but ensure that it corresponds with the type of products setup in your catalog)<li>Enter a description describing what the line item is</li>(NOTE: If you are going to enter a product in the Product Id field from the catalog then leave the 'Description' field blank as it will be used to show the product description)<li>Leave the 'Override GL Account Id' field blank as it will use the default account based on the Chart of Accounts setup</li><li>Use the lookup or enter a product code in the 'Product Id' field</li>(NOTE: This can be left blank if your invoice line is not related to a product in the catalog)<li>Enter a number in the 'Quantity' field</li><li>Enter a 'Unit Price' only if the Product Id field is blank</li>NOTE: If a Product Id has been entered then leave the 'Unit Price' field blank as it will pick up the product price from the catalog)<li>Leave the 'Inventory Item' field blank</li><li>Leave the 'Product Feature Id' field blank</li><li>Leave the 'UOM' field blank</li><li>Select 'Yes' for the 'Taxable Flag' field</li></ol>
-
- #+BEGIN_WARNING
  TO CHECK: Need to do some tests to see what line item type needs to be used for 'Sales Tax'.
  I think that it could be 'Invoice Item Sales Tax' since tax is currently calculated at invoice item line level.
  Also the automatically generated invoices from Order Entry and E-Commerce show taxes at the invoice item line level (think there may be some work going on - see JIRA on to consolidate entries).
  Need to do some tests using 'Invoice Sales Tax' to see how it works…​…​
  #+END_WARNING
	- #### How to I update an invoice line items?
	- Not all the fields on the invoice item line can be updated. For example Taxable Flag and Inventory Item cannot be updated.
	- If these fields need to be amended then the invoice item will need to be removed and then re-created.
	- <ol><li>Select the 'Items' sub menu for the invoice</li><li>Any existing line items will be displayed in the 'Items' box</li><li>Amend the details in the line item that needs to be updated (eg Quantity, Invoice Item Type, Product Id, Description, Override GL Account, Unit Price)</li><li>Press the 'Update' button displayed at the end of the line item that has been updated</li></ol>
	- #### How do I delete Invoice?
	- <ol><li>Select the 'Items' sub menu for the invoice</li><li>Any existing line items will be displayed in the 'Items' box</li><li>Press the 'Remove' button displayed at the end of the line item that needs to be deleted</li></ol>
	-
- ### Help for Edit Invoice Time Entries
- he Time Entries screen displays any time logged against the invoice. For example these time entries can be from employee or external supplier timesheets that are tracked within APOGEE. It is used to track any individual work or billable hours against an invoice.
	- #### How do I add a new time entry for an invoice?
	- <ol><li>Add time entry to a new invoice and add time entry to an existing invoice.</li><li>Timesheet entries can be added to an existing invoice from Workeffort Manager.</li></ol>
	-
	- #### How do I update a time entry for an invoice?
	- #+BEGIN_WARNING
	  To CHECK if this can only be done via timesheets.
	  #+END_WARNING
	- #### How do I remove a time entry from an invoice?
	- #+BEGIN_WARNING
	  TO CHECK if this is done via timesheets
	  #+END_WARNING
- ### Help for Send Per Email
- This is used to send a copy of the invoice details to one or more email addresses. The invoice is included as an attachment and the user can add a simple accompanying email message.
	- #### How do I send a copy of an invoice via email ?
	- <ol><li>Select the 'Send per Email' sub menu</li><li>The 'Send per Email' default screen will be displayed</li><li>Enter the 'From Email Address'</li>(NOTE TO CHECK: Shouldnt this be defaulted from the user login…​..????)<li>Leave the 'To Email Address' as it is as this will be defaulted using the customer details from the invoice</li><li>If required enter the 'Copy Email address' for anyone that needs to be copied on the email</li><li>Leave the 'Subject' as the default of 'Please find attached invoice'</li><li>Leave the 'Other Currency' box blank</li>(NOTE TO CHECK: Investigate what effect this has on the email…​..)<li>Enter a short email message in the 'Email Body'</li><li>Press the 'Submit' button</li></ol>
	-
- ### Help for invoice Roles
- The Invoice Roles screen allows parties with specific roles to be associated with and invoice. If the e-commerce or Sales Order entry route has already been used then the invoice generated will already contain the relevant roles from the various parties.
- For a Sales Order examples of roles will include Bill From Customer, Bill To Customer, End User Customer,Ship To Customer etc.
	- #### How do I add a party role to an invoice ?
	- Party roles will automatically be added to an invoices that have been generated as a result of E-Commerce order entry or Sales Order entry.
	  They can also be added be added manually.
	- <ol><li>Select the 'Roles' sub menu</li><li>Enter or use the lookup to enter the party to be added to the invoice in the 'Party Id' field</li><li>Use the drop down box to select the 'Role Type Id'</li><li>Leave the 'Date Time Performed' field blank</li>(NOTE: This field is optional and can be used to indicate the date and time this role was performed by the party for this invoice)<li>Leave the 'Percentage' field blank</li>(NOTE: This field is optional and can be entered if required. If roles are shared then this field can be used to indicate the assigned percentage for this role)<li>Press the 'Submit' button</li></ol>
- The new role entry will be displayed on the bottom part of the screen
  id:: 674f5c7f-40c9-4f4d-8ac5-0c036f30e01e
	- #+BEGIN_IMPORTANT
	  If you select a role that is not associated with the party that has been entered an error message will be displayed. To fix it you will need to add the role to the party or choose another party that already has that role associated with it.
	  #+END_IMPORTANT
	- #### How do I update a party role on an invoice
	- A party role cannot be updated via the current user interface. It can only be removed. If a party role needs to be updated then the entry must be deleted and then re-created.
	- #### How do I remove a party role from an invoice ?
	- <ol><li>Locate the entry that needs to be removed</li><li>Press the 'Remove' button next to the entry that needs to be deleted</li><li>The entry is now removed from the list of invoice roles</li></ol>
-