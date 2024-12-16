- This screen allows the user to search for and locate Sales Invoices based on their due date.
- The 'Due Date' can be defined as the last possible date that payments can be received for the invoice without triggering late payment penalties.
- The 'Invoice Date' can be defined as the date that the invoice was created and this is normally based on when products were shipped or services were provided.
- #+BEGIN_IMPORTANT
  TO CHECK: There appears to be a minor bug here as if the Invoice 'Due Date' is different to the Invoice Date (eg. Invoice Creation Date) then the Invoice Date is used as the Due Date in this screen which I dont think is correct…​…​
  #+END_IMPORTANT
- A Sales Invoice may be due to be paid immediately or as in some cases the customer is given a 'grace period' after which the invoice is generated and becomes due.
- Examples of this include only generating a customer invoice after a certain amount of time after the dispatch of their order.
  (NOTE: There are several ways this can be achieved in OFBiz including the use of agreements and billing accounts).
- This screen can be used to locate Sales Invoices as follows:
- <ul><li>Thatwillbecomeduewithinafixedtimeframe(egthenext5days)</li><li>Thatmayalreadybeoverdue</li><li>Thathavebeenautomaticallygeneratedbythesystem(egasaresultofAgreementsbasedonpaymentin30days,etc…​.TOCHECK)</li></ul>
-
- #+BEGIN_IMPORTANT
  	TO CHECK See details from Jacopo below regarding future work regarding Find Sales Invoice by Due Date and Find Purchase Invoice by Due Date functionality:
  - The two links are used to search invoices' due dates for payments - there are plans to add links to quickly create payments for them etc.
  - So they are somewhat in the middle between an invoice thing and a payment thing.
  - By the way, for now I will close this issue because the best spot to place them is in the AR and AP applications, but there is still a lot of work to do to make them usable.
  #+END_IMPORTANT