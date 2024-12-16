- The GL Account Defaults screens are are method to setup rules that are used to translate business transactions into accounting transactions. It currently is made up of 12 sub menus that can be used to map various transaction type codes to a specific general ledger account
- Accounting transactions are made up of a Debit Entry and a Credit Entry. The GL Account defaults screens help map which accounts are to be used to generate a each part of the transaction. This means that certain mappings will be used to generate the Debit (or DR) entry part of the transaction and others used to generate the Credit (or CR) entry part of the transaction.
- #+BEGIN_IMPORTANT
  Many of the accounting transactions are generated 'automatically' (or in the background) using the the accounting services SECAS / EECAS
  #+END_IMPORTANT
- The GL Account Type is used to specify the default account that certain transactions (eg Accounts Payable, Accounts Receivable, etc) are posted to.
  An accounting transaction (or journal entry) is made up of two parts - a Debit Entry and a Credit Entry that balance each other. The GL Account Type is used to translate one side of the journal entry.
- GL Account Types are stored in Entity GLAccountType which can be viewed via Entity Data Maintenance in the Webtools menu. There are currently 57 different GL Account Types that are part of the OFBiz demo data but only 19 of these are setup as mappings
- How the GL Account Type is used is best shown by an example.
- A very simple description of an online Sales Order Process could be as follows:
-
- Customer Orders a Product (and Creates a Sales Order)
  logseq.order-list-type:: number
- Customer Pays for Product (via Credit Card, Internet Banking etc)
  logseq.order-list-type:: number
- Vendor confirms Payment and Dispatches the Product to the Customer
  logseq.order-list-type:: number
-
- Let’s focus on the first part step of 3 in more detail.
-
- <ul>
      <li>The vendor has checked their bank statement and seen that the customer has paid.</li>
      <li>In OFBiz Order Manager they will then look up the relevant Sales Order and then click the 'Receive Payment' button to log the payment in the system.</li>
      <li>The 'Receive Payment' button is a trigger for an 'automatic' accounting transaction.</li>
      <li>The transaction type that is triggered is called 'Incoming Payment'.</li>
      <li>The accounting entries generated are: DR 112000 Undeposited Funds, CR 120000 Accounts Receivable.</li>
  </ul>
- The CR (or Credit) entry for the transaction is created by the GL Acccount Type mapping for 'Accounts Receivable' (which by using the demo data default will go the 120000 Accounts Receivable)
- The DR (or Debit) entry for the transaction is created by a different GL Account default, the Payment Method Id / GL Account Id mapping (eg Cash is setup as 112000 Undeposited Receipts)