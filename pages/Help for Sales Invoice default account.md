- The Sales Invoice sub menu is used to specify the default account to be used for the individual line items that appear on a Sales Invoice.
- The items are identified by a line description which can be mapped to a specific general ledger account.
- Sales invoices can be made up of a variety of items as well as the product that is being sold (eg discounts, promotions, work effort or labour costs etc). The majority of businesses will want to track these type of items separately in the general ledger and this screen will allow this type of setup.
- This setup will translate to one side of the journal entry only.
- A key mapping used is linked directly to the Product Type (eg Invoice Digital Good Item, Invoice Finished Good Item, Invoice Finished/Digital Good Item…​.). This controls where the sales revenue received from the sale of the product is stored in the general ledger
- Only a limited number of general ledger accounts that are available to be mapped. Currently this is 7 and limited to the accounts that have been assigned to the organisation from the Global Chart of Accounts that have a 'GL Account Class Id' = 'Revenue'
  (NOTE: You will see that Discounts on Sales is not available to be selected because it’s GL Account Class Id = 'Cost of Goods Sold Expense'. It appears as a default because it is setup in the Global GL settings that doesnt seem to have any limitations of the account.)
- #+BEGIN_IMPORTANT
  This screen is one of the screens where the default entries that are displayed here are entered via the Global GL Settings under the sub menu 'Invoice Item Type'.
  This screen allows users to override the global settings for the Sales Invoice item type.
  An example of why this could be necessary could be that a company many want to isolate the sales reporting of a specific department or business unit separately (eg subledgers etc) but still have the option of a 'catch all' global general ledger account.
  #+END_IMPORTANT
- If an override account is added it will appear in the Override GL Account column on the screen.
- The only mapping that seems a bit out of place here is Sales Tax. It is blank because Sales Tax is setup using Tax Authorities so dont know why you would want to override the Sales Tax account to a Sales Revenue Account.
- #+BEGIN_NOTE
  Also need to highlight that in the Global Settings it uses the ENUM description to select the item and there are duplicate descriptions between the Sales Invoice and the Purchase Invoice.
  Not too much of a problem here but it does cause problems in Agreements when setting up things like Commissions based on line items as you cant tell the difference between the description of a Sales Invoice item called 'Invoice Adjustment' and a Purchase Invoice item called 'Invoice Adjustment' …​.. except by trial and error
  #+END_NOTE
- How the Sales Invoice mappings are used is best shown by an example.
- A very simple description of an online Sales Order Process could be as follows:
-
- Customer Orders a Product (and Creates a Sales Order)
  logseq.order-list-type:: number
- Customer Pays for Product (via Credit Card, Internet Banking etc)
  logseq.order-list-type:: number
- Vendor confirms Payment and Dispatches the Product to the Customer
  logseq.order-list-type:: number
-
- Let’s focus on the second part step of 3 in more detail.
- <ul>
      <li>The vendor has verified that the customer payment has been received.</li>
      <li>In APOGEE Order Manager they will then look up the relevant Sales Order and then click the 'Quick Ship Entire Order' button to log the dispatch of the order in the system.</li>
      <li>The 'Quick Ship Entire Order' button is a trigger for an 'automatic' accounting transaction.</li>
      <li>The transaction type that is triggered is called 'Sales Invoice'.</li>
  </ul>
-
- Transaction Type: Sales Invoice DR 120000 Accounts Receivable, DR 410000 Discounts on Sales, DR 400000 Sales, CR 22????? Sales Tax Collected
- DR Sales is used for item promotions where product cost is simply reversed.
  Only order promotions are coded to Discounts.
  The Sales Tax account will be dependent on your sales tax setup.
  The demo data posts to tax accounts by US state.
- One of the CR (or Credit) entries for the Sales Invoice transaction is created using the Sales mapping defined here in the Sales Invoice (and the other is created another GL Account default for 'Tax Authority GL Accounts')
- All of the the DR (or Debit) entries for the Sales Invoice transaction (except for Accounts Receivable which is comes from the GL Account Type defaults) are created using the mappings defined here in the Sales Invoice
- The Sales Invoice sub menu is used to specify the default account to be used for the individual line items that appear on a Sales Invoice.
- The items are identified by a line description which can be mapped to a specific general ledger account.
- Sales invoices can be made up of a variety of items as well as the product that is being sold (eg discounts, promotions, work effort or labour costs etc). The majority of businesses will want to track these type of items separately in the general ledger and this screen will allow this type of setup.
- This setup will translate to one side of the journal entry only.
- A key mapping used is linked directly to the Product Type (eg Invoice Digital Good Item, Invoice Finished Good Item, Invoice Finished/Digital Good Item…​.). This controls where the sales revenue received from the sale of the product is stored in the general ledger
- Only a limited number of general ledger accounts that are available to be mapped. Currently this is 7 and limited to the accounts that have been assigned to the organisation from the Global Chart of Accounts that have a 'GL Account Class Id' = 'Revenue'
  (NOTE: You will see that Discounts on Sales is not available to be selected because it’s GL Account Class Id = 'Cost of Goods Sold Expense'. It appears as a default because it is setup in the Global GL settings that doesnt seem to have any limitations of the account.)
- #+BEGIN_IMPORTANT
  This screen is one of the screens where the default entries that are displayed here are entered via the Global GL Settings under the sub menu 'Invoice Item Type'.
  This screen allows users to override the global settings for the Sales Invoice item type.
  An example of why this could be necessary could be that a company many want to isolate the sales reporting of a specific department or business unit separately (eg subledgers etc) but still have the option of a 'catch all' global general ledger account.
  #+END_IMPORTANT
- If an override account is added it will appear in the Override GL Account column on the screen.
- The only mapping that seems a bit out of place here is Sales Tax. It is blank because Sales Tax is setup using Tax Authorities so dont know why you would want to override the Sales Tax account to a Sales Revenue Account.
- #+BEGIN_NOTE
  Also need to highlight that in the Global Settings it uses the ENUM description to select the item and there are duplicate descriptions between the Sales Invoice and the Purchase Invoice.
  Not too much of a problem here but it does cause problems in Agreements when setting up things like Commissions based on line items as you cant tell the difference between the description of a Sales Invoice item called 'Invoice Adjustment' and a Purchase Invoice item called 'Invoice Adjustment' …​.. except by trial and error
  #+END_NOTE
- How the Sales Invoice mappings are used is best shown by an example.
- A very simple description of an online Sales Order Process could be as follows:
- Customer Orders a Product (and Creates a Sales Order)
  logseq.order-list-type:: number
- Customer Pays for Product (via Credit Card, Internet Banking etc)
  logseq.order-list-type:: number
- Vendor confirms Payment and Dispatches the Product to the Customer
  logseq.order-list-type:: number
- Let’s focus on the second part step of 3 in more detail.
- <ul>
      <li>The vendor has verified that the customer payment has been received.</li>
      <li>In APOGEE Order Manager they will then look up the relevant Sales Order and then click the 'Quick Ship Entire Order' button to log the dispatch of the order in the system.</li>
      <li>The 'Quick Ship Entire Order' button is a trigger for an 'automatic' accounting transaction.</li>
      <li>The transaction type that is triggered is called 'Sales Invoice'.</li>
  </ul>
- Transaction Type: Sales Invoice DR 120000 Accounts Receivable, DR 410000 Discounts on Sales, DR 400000 Sales, CR 22????? Sales Tax Collected
- DR Sales is used for item promotions where product cost is simply reversed.
  Only order promotions are coded to Discounts.
  The Sales Tax account will be dependent on your sales tax setup.
  The demo data posts to tax accounts by US state.
- One of the CR (or Credit) entries for the Sales Invoice transaction is created using the Sales mapping defined here in the Sales Invoice (and the other is created another GL Account default for 'Tax Authority GL Accounts')
- All of the the DR (or Debit) entries for the Sales Invoice transaction (except for Accounts Receivable which is comes from the GL Account Type defaults) are created using the mappings defined here in the Sales Invoice
-