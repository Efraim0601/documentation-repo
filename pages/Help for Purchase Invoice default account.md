- The Purchase Invoice sub menu is used to specify the default account to be used for the individual line items that appear on a Purchase Invoice.
- The items are identified by a line description which can be mapped to a specific general ledger account.
- Purchase invoices can be made up of a variety of items as well as the product that is being bought (eg discounts, promotions, work effort or labour costs etc). The majority of businesses will want to track these type of items separately in the general ledger and this screen will allow this type of setup.
- This setup will translate to one side of the journal entry only.
- #+BEGIN_IMPORTANT
  This screen is one of the screens where the default entries that are displayed here are entered via the Global GL Settings under the sub menu 'Invoice Item Type'. This screen allows users to override the global settings for the Purchase Invoice item type.
  An example of why this could be necessary could be that a company many want to isolate the sales reporting of a specific department or business unit separately (eg subledgers etc) but still have the option of a 'catch all' global general ledger account.
  #+END_IMPORTANT
- #+BEGIN_IMPORTANT
  TO CHECK: Need to do more investigation but the it looks like these Purchase Invoice mappings dont work when used as part of the Purchase Order to Purchase Invoice Process. (Have been doing some tests to try and get it to post to a different account than 'Uninvoiced Shipment Receipts' and 'Inventory' but hasnt worked so far.) We need to be able to specify things such as Sales Tax, Freight and any Purchase Order adjustments.
  #+END_IMPORTANT
- These override mappings do work if there is no Purchase Order just a Purchase Invoice as shown in the simple process below.
- How the Purchase Invoice mappings are used is best shown by an example.
- A very simple description of a Purchase Invoice Process could be as follows:
-
- logseq.order-list-type:: number
  
  You have ordered something from a supplier (eg indirect purchasing such as stationery etc via phone)
- logseq.order-list-type:: number
  
  The Supplier ships the products to you
  (NOTE: as they are not stored in the Warehouse but in your offices - so dont need an Inventory Receive…​..????)
- logseq.order-list-type:: number
  
  You receive the product and an invoice from the Supplier (Purchase Invoice)
- You enter the Purchase Invoice pay the Supplier the amount invoiced
  logseq.order-list-type:: number
-
- Let's focus on step of 4 in more detail.
- <ul>
      <li>You have received the product from the supplier with an invoice.</li>
      <li>In APOGEE you enter the Purchase Invoice using 'Create New' in the 'Invoices' menu of Accounting Manager.</li>
      <li>Using the 'Items' sub menu you can create individual items on the Purchase Invoice (e.g., Paper, Pens, Sales Tax, etc., and they don't need to have a Product ID associated with them).</li>
      <li>When you add a new invoice item to the Purchase Invoice, it is the 'Invoice Item Type' that is affected by the Purchase Invoice override mappings.</li>
      <li>The Purchase Invoice can then be moved to various statuses (Approved, Received, Ready, or Cancelled).</li>
      <li>When the status is moved to 'Ready,' this is a trigger for an 'automatic' accounting transaction.</li>
      <li>The transaction type generated is called 'Purchase Invoice' and it uses the Purchase Invoice override mappings.</li>
  </ul>
- Transaction Type: Purchase Invoice, DR 516100 Purchase Order Adjustments , DR ????? Sales Tax, CR 210000 Accounts Payable
-