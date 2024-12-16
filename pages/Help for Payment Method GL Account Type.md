- The Payment Method GL Account Type Id is used to map the different payment methods (eg Cash, Cheque etc) to a specific GL Account Type Id. This will translate to one side of a GL entry only.
- A Payment Method is just a way to define the ways in which payments can be made.
  Each payment method can be linked to a different account in the general ledger.
  A main GL account used would be the one that represents the Company bank account.
  In the demo data mappings Electronic Funds Transfer, Company Account, Financial Account are all linked to the Company bank account GL account.
- APOGEE demo data defines 15 different payment methods as follows:
- <ul>
      <li>Cash</li>
      <li>Certified Cheque</li>
      <li>Company Account</li>
      <li>Company Cheque</li>
      <li>Electronic Funds Transfer (NOTE TO CHECK: Problem with definition or terminology - is this a Direct Debit…​. ?? A direct debit is controlled by the payee and an automatic payment via bank account is controlled by the payer)</li>
      <li>Billing Account</li>
      <li>Cash on Delivery (COD)</li>
      <li>eBay</li>
      <li>Offline Payment (NOTE: Is this ambiguous - since COD is an offline payment…​)</li>
      <li>PayPal</li>
      <li>WorldPay</li>
      <li>Financial Account</li>
      <li>Gift Certificate</li>
      <li>Money Order</li>
      <li>Personal Cheque</li>
  </ul>
- #+BEGIN_NOTE
  A point to note is that these payment methods dont include Credit Cards…​.(which I think is on purpose…​). The majority of these payment methods are linked to 'Undeposited Receipts' but an additional accounting transaction may be needed once the funds have cleared and are available in the Company bank account.
  #+END_NOTE
-