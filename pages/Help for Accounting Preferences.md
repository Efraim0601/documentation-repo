- Accounting Preferences are a set of configuration details that are related to a party. To appear on this screen the party must be setup with the role of 'Internal Organisation'. This means that you can add the internal organisation role to a party and they will be added to this screen and then can be configured.
-
- The master default party is 'Company' but preferences can also be setup for internal departments. The demo data shows some examples of this (eg Marketing, Accounting, Sales, Development etc). Unless overridden then then all other parties appearing on this screen will take their default setup from 'Company'
- #+BEGIN_NOTE
  The majority of the configuration information displayed in Accounting Preferences are taken from the Enumeration entity.
  #+END_NOTE
- It is used for setting specifying information related to the accounting setup for a specific organisation or parties that exist within an organisation such as business units, cost centres, departments ,subsidiaries etc.
- Information that can be setup include the following:
- <ul>
  <li>The start date of the Time Periods and Fiscal or Accounting Year (eg 1st April, 1st January, 1st June etc)</li>
  <li>Tax Return Form
  <br>(NOTE: Need TO CHECK how important this is and where it is used…​…​.possibly some kind of reporting???)</li>
  <li>The method to be used for calculating Cost of Goods Sold (COGS)</li>
  <li>Base Currency - eg USD, GBP, EUR etc
  <br>(NOTE: May have main company in USD but a subsidiary in EUR etc)</li>
  <li>Invoice prefix, numbering and sequencing (eg you may want each business unit / subsidiary to have its own invoice numbering or sequence etc)</li>
  <li>Quote prefix, number and sequencing</li>
  <li>Method to be used for refunds (eg cheque, direct bank credit, voucher credit etc…​)</li>
  <li>Specify which journal will be used to store error transactions.</li>
  </ul>
- #+BEGIN_NOTE
  Key things that are usually need to be amended include the base currency for the company, fiscal year information and invoice numbering prefix or sequencing.
  #+END_NOTE