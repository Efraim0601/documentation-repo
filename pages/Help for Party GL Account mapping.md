- The Party / GL Account mapping allows the translation of different account types (eg Accounts Receivable, Accounts Payable etc) for a party to be mapped to a separate general ledger account.
- The party role (eg Bill To Customer) is also used to define the mapping even further.
- APOGEE demo data setup comes with no entries here.
- It is used as a way of implementing subledger functionality in APOGEE. Subledger functionality is where a higher level account can be split into lower levels. In this case these lower levels can be by party.
- An example could be that a business may want to use the general ledger to track the Accounts Receivable (AR) by customer so the chart of account would be setup something like as follows:
- 120000 Accounts Receivable
- <ul>
      <li>120010 Accounts Receivable - Customer A</li>
      <li>120020 Accounts Receivable - Customer B</li>
      <li>120030 Accounts Receivable - Customer C</li>
  </ul>
-
- This has the main AR account is at the top of the hierarchy and 3 sub accounts below it.
- Entries for Customers A, B and C would be setup with a role of 'Bill From Customer' as this is a role associated with the customer when the Sales Invoice is generated.When a transaction matching the criteria is processed in the system then these mappings will control where it is posted to.In the case of Customer A any AR transactions with role 'Bill To Customer' are posted to '120010' instead of the standard '120000
-