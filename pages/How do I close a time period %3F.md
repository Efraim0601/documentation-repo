- To close a time period select the 'Close' button next to the time period.
  logseq.order-list-type:: number
- The time period will be removed from the current open time periods area and re-displayed in the closed time periods section of the screen.
  logseq.order-list-type:: number
- Closing a time period is a trigger for an automatic accounting transaction as follows:
- <ul>
      <li>Transaction Type: Period Closing</li>
      <li>DR ?????? (based on the GL account type mapping for Profit Loss)</li>
      <li>CR 336000 Retained Earnings (based on GL account type mapping for Retained Earnings)</li>
  </ul>
- #+BEGIN_IMPORTANT
  Both sides of this accounting transaction uses the same GL account type default mapping.
  The account mapping for 'Profit Loss' is not setup as part of the demo data so this transaction will not automatically post to the general ledger but will instead be put in the ERROR_JOURNAL as an unposted transaction.
  The transaction value is zero for both sides of journal…​Even if it does have a value do we want to move it from P&L to Equity during the financial year? Normally this is done once at the end of the financial year.
  #+END_IMPORTANT
-