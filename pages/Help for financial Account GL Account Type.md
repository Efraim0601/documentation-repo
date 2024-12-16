- The FinAccount Type GL Account (Financial Account Type / GL Account Type) is used to specify the default account to be used for a specific type of Financial Account.
  This setup will translate to one side of the journal entry only.
- #+BEGIN_IMPORTANT
  There is a limitation that only one account can be specified per Financial Account type.
  Currently there are 6 types of Financial Account
  (Bank, Deposit, Investment, Gift Certificate, Replenish, Service Credit)
  so if you have more than one of these type of accounts that you need to track separately then there could be a problem.
  #+END_IMPORTANT
- This mapping is normally be triggered if something is paid or uses a Financial Account. Using the demo data this mapping is triggered when someone purchases a gift certificate, or pays money into a financial account.
-