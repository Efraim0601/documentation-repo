- <ol><li>Enter the 'Order Id' of the sales order for which payment is being made</li><li>Enter the 'Order Payment Preference Id'</li>(NOTE: This is automatically generated at sales order creation and may be difficult to find out…​
  I found it by initially doing an order and then paying by DemoCustomer’s credit card and checking Gateway Responses for what was displayed in that field for the order)<li>Select the 'Payment Method Type'</li>(NOTE TO CHECK: What happens if you use other selections not just credit card?)<li>Enter the 'Amount'</li><li>Press the 'Authorize' button</li><li>A new transaction should be displayed with the status of authorised</li></ol>
-
- #+BEGIN_IMPORTANT
  The demo data payment settings for the Payment authorisation Service is set to always approve so no transactions will display here because of this.
  TO CHECK: Need to test and maybe try removing the 'always approve' to see if the transaction will be created as 'unauthorised'
  #+END_IMPORTANT
-