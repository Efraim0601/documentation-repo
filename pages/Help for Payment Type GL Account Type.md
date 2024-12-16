- The Payment Type GL Account Type Id is used to translate (or map) the different payment types to a specific GL Account Type Id. The GL Account Type Id is then used via the 'GL Account Type Id' defaults to translate to one side of a journal entry.
- #+BEGIN_NOTE
  This GL Account default is used to link to another one of the GL Account defaults.
  #+END_NOTE
- A Payment Type is just a way to categorize transactions.
- Examples of Payment Types could be as follows:
- <ul>
      <li>Commission Payments</li>
      <li>Customer Payments</li>
      <li>Vendor (or Supplier) Payments</li>
      <li>Customer Refunds</li>
      <li>Customer Prepayments or Deposits</li>
  </ul>
- These payment types can then be mapped to the required account type in the Chart of Account.
- Examples of these type of mappings could be as follows:
- <ul>
      <li>Customer Payments are mapped to Account Receivable.</li>
      <li>Vendor (or Supplier) Payments are mapped to Account Payable.</li>
      <li>Customer Refunds are mapped to Customer Credits.</li>
  </ul>