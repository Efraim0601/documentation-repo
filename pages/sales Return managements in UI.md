### Quick Return
- While viewing an existing order, you can create a return from that order by clicking on the [Create Return] button (actions section).That will take you to the quickreturn screen, from where you identify which item(s) the customers wants to return.
- Be clear about the reason and the quantity to be returned. Also be sure that the Return Price does not exceed how much the customer actually paid for the item.
  Return Type is important because it is always to your advantage to have the purchase price applied as a credit towards another purchase rather than having to take money out of your business to pay a refund.
- When the information is correctly selected and entered, click the link[Return Selected Items] to create the Return.
  Next screen show you Return Request creation successful, and you can directly [Accept Return]
- That also takes you to the Returns tab, Return Items sub-tab, discussed further below.
- Notice you can:
	- select All (check box)
	  logseq.order-list-type:: number
	- choose **Return Qty**, just behind Order Qty
	  logseq.order-list-type:: number
	  Be sure this does not exceed the Order Qty. If that attempt ismade, have them return any surplus against another order from where they probably obtained it.
	- **Return Price**, just behind Unit Price
	  logseq.order-list-type:: number
	  The Price at which the customer will be credited. This is a mandatory field (*).
	  For example, if the customer received a promotional discount of 10% on a $100 item, you would not return $100 (the Unit Price) but only the discounted price of $90 which they originally paid for it.
	- **Return Reason**
	  logseq.order-list-type:: number
	  Select the best-stated reason for the return. Remember that Returns need to be approved. Some items may be sold with a re-shelving fee, others may be close-outs with no returns authorized.
	  If reason you want is not listed, Additional reasons can be programmed into the system as their need develops (or just added by a administrator via webtools if it’s only for better information).
	  Why is a reason needed? This information is used when receiving the return to help decide whether to put the item back into inventory,throw it out, schedule it for repairs, etc.
	  Choices in the drop-down box might include:
		- Defective Item
		  logseq.order-list-type:: number
		- Defective Item
		  logseq.order-list-type:: number
		- Miss-Shipped Item
		  logseq.order-list-type:: number
		- Digital Fulfillment Failed
		  logseq.order-list-type:: number
	- **Return Type**
	  logseq.order-list-type:: number
	  This establishes how the financial aspects of the return will be handled. Choices in the drop-down box might include:
		- Store Credit
		  logseq.order-list-type:: number
		- Refund
		  logseq.order-list-type:: number
		- Replacement
		  logseq.order-list-type:: number
		- Cross-Ship Replacement
		  logseq.order-list-type:: number
	- **Item Status**
	  logseq.order-list-type:: number
	  What is the current status of the Item?
	  The status could be one of the following:
		- <ul><li>---, the item status is unknown</li><li>On Order, the item was not yet shipped but is no longer wanted</li><li>Available, the item is in your facility</li><li>Promised, the item is committed to fulfilling another order</li>
		    <li>Delivered, the item is on its way to the Customer now wanting to return it</li><li>Being Transferred, the item is being moved from one location or section to another</li><li>Being Transferred (Promised), the item is being moved AND it has already been committed to fulfilling another order</li><li>Returned, the item has physically been sent back from the customer to your facilities</li><li>Defective, whatever the location or other status may be, the item itself is considered defective and should not be promised to fulfill another order</li></ul>
	- **Select a ship from address**
	  Click on the radio button corresponding with the address from which the items will be returned. This will generally match the ship-to address for the original Sales Order.
- ### Find Return
- In the status field, You can select multiple values.
- ### Create Return
- If you are not starting from View Order Screen, you can initiate the creation of a new Return from dedicate screen.
- *First screen* is for the header informations
- The Return process involves a coordinated effort with Facilities, Accounting, and the Order managers. The tab [Receive Return] is not visible on this screen until the Return has been Accepted. That tab actually takes you into the Facilities Manager for further processing of the Return.
- **Return ID** This is a number assigned by the system when the Return is first requested.
- Field **Needs Inventory Receive**: or Auto-Receive means that the item is already here and that when the Return is Accepted, it will be processed as an Auto Receive rather than through the normal steps in the facility.
- *Second screen, tabs* is for the return Items
- It’s not possible to add manually items, you should choose in the drop box Order Id on bottom to load directly Items from an existing order.
  After loading items from an order, select the one you want to add them to this return.
- For more details on field, look at [[Quick Return]].
- After loading items, update Status to accepted under Return Header, you now have a new link button [Receive Return]. When you click on that, you are taken to the Facility Manager > Facilities tab > [[Receive Return]] sub-tab.