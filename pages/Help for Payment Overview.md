- The Payments Overview screen displays the summary details of the payment.
- On one side it shows information related to the payment transaction header (eg Payment Type, Status, Amount, Effective Date etc) and the other it shows if the payment has been applied (or matched) to an invoice or billing account etc.
- The following options are currently available from this screen:
-
- <ul><li>Create New (Create a new payment)</li><li>Status to 'Received' (Change the status of the current payment to 'Received.</li>NOTE: This will create the relevant accounting transactions and post them to the general ledger)<li>Status to 'Cancelled' (Change the status of the current payment to 'Cancelled')</li><li>tatus to 'Confirmed' (Change the status of the current invoice to 'Confirmed'.</li>NOTE: This status option will not appear until the status has been changed to 'Received')</ul>
- #+BEGIN_IMPORTANT
  The general ledger transactions generated as a result of the payment are based on the GL Account Type defaults for Company as follows:
  1) Debit Entry (GL Account Type defaults)
  2) Credit Entry (Payment Method Id / GL Account Id)
  #+END_IMPORTANT
-