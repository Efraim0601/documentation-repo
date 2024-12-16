- OFBiz comes with a master template for a very comprehensive chart of accounts. This can be found in 'Global GL Defaults' under the 'Accounting' tab.
- A couple of points to note
- <ul><li>You do not need to use all the accounts defined in this master template -but it may be simpler to look for the accounts that you can use or rename</li><li>You can create your own additional accounts if you dont want to use the ones in the master template</li></ul>
- The chart of accounts for the default organisation (Company) is built up by selecting the accounts that you want to use from the global chart of accounts master template.
- This means that if you want to create a new account then you need to create it first in the Global Chart of Accounts and then link (or assign) it to the chart of accounts for Company.
- Details of the Chart of Accounts can be exported as a CSV file or PDF using the buttons displayed.
-
- #+BEGIN_IMPORTANT
  You need to be careful if you do decide to create your own accounts that they contain all the details required and that they are linked into the relevant configuation for the setup of the GL defaults.
  This means that if you change an account (eg Inventory) to one of your own, you need to check the GL defaults setup and replace any reference to the Inventory account to the one you have created.
  #+END_IMPORTANT
- This Chart of Accounts screen is used to define the list of accounts (or chart) that will be actively used by the company. For example the Global chart of accounts may contain 100 different accounts but only 20 need to be used for your specific business. This means you need only to create assignments to the accounts that you actively want to use.
- The Chart of Accounts is a mixture of business needs (ie being able to track the information you need for your business) and tax requirements (i.e. legal or government requirements necessary for operating a business). The type of Chart that you setup will be dependent of your business type.
-