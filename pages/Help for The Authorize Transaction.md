- An authorization is a temporary transaction that shows a commitment to take money from an account.
- The 'Authorize' process is the first step in allowing a sales transaction payment to be accepted.
  In APOGEE a service would be defined to carry out the authorisation process each time for example, a credit card is used. It will perform specific validation tests before the payment can be classes as 'authorised'.
- When a payment is authorised it means that it has been validated and that the credit card or bank account has been checked to ensure that it has sufficient funds available to cover the proposed transaction.
  A number or code may be issued as evidence of the authorisation.
- #+BEGIN_IMPORTANT
  In the 'Payment' settings for a store as part of the Product Payment setup the user can specify various services that will process a payment transactions through to completion.
  #+END_IMPORTANT
- This includes the follozing:
- <ul><li>PaymentAuthorisation</li><li>PaymentCapture</li><li>PaymentCredit</li><li>PaymentAuthenticationVerification</li><li>PaymentRe-Authorisation</li><li>PaymentRefund</li><li>PaymentReleaseAuthorisation</li></ul>
-
- This is used to provide verification and approval for the first step of the sales transaction payment process.
- An 'Authorize' button is also displayed on Sales Order detail screen if a Credit Card payment was specified for a sales order. This is probably a more natural place for a payment transaction to be authorised.
- #+BEGIN_IMPORTANT
  Using OFBiz demo data if DemoCustomer uses their credit card for payment then an transaction is created that is automatically authorised and can be viewed using the Gateway Responses.
  #+END_IMPORTANT
-