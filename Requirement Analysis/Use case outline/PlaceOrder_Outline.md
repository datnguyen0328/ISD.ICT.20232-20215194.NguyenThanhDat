# "Place Order" Use Case

## Basic/Success Flow
1. **Review Cart:**
   - Customer reviews items and total price in the cart, including VAT.
   - The system notifies if inventory is insufficient for any product.
2. **Provide Delivery Information:**
   - Customer provides delivery information such as recipient name, email, phone number, and address.
   - The system recalculates the delivery fee and updates the invoice.
3. **Place Order Request:**
   - Customer requests to place an order.
   - The system checks inventory and confirms product availability.
4. **Invoice Display:**
   - The system displays an invoice with product list, quantities, prices, total excluding VAT, total including VAT, and delivery fee.
5. **Payment Information:**
   - Customer selects to pay the order, the use case "Pay Order" is inserted.
6. **End Place order**
   - The software records the transaction information and the successfully paid order.

## Alternative Flows
 **A1. Insufficient Inventory:**
   - Customer is prompted to update the cart if the inventory is insufficient.
   - Customer updates the cart and proceeds to place the order again.

 **A2. Invalid Delivery Information:**
   - If delivery information is invalid, the customer is asked to update it.

 **A3. Rush Order Delivery:**
   - If rush order delivery is selected, the use case "Place Rush Order" is inserted.

 **A4. Payment Failure:**
   - If payment fails, the customer is prompted to try a different payment method.

 **A5. Cancel Order:**
   - The customer can cancel the order through the provided link before it is approved.
   - The system processes the cancellation and refunds through VNPay.



# "Place Rush Order" Use Case

## Basic/Success Flow
1. **Select Rush Order Delivery:**
   - Customer selects the rush order delivery option during the checkout process.
2. **Eligibility Check:**
   - The system checks if the delivery address is within the inner city of Hanoi and if the selected products are eligible for rush delivery.
3. **Inform Customer:**
   - If eligible, the system informs the customer of the additional charge and the rush order delivery details.
4. **Additional Rush Order Information:**
   - Customer provides specific details for rush order delivery, including preferred delivery time and instructions.
5. **Delivery Fee Calculation:**
   - The system calculates the delivery fee, including any additional charges for rush delivery.
6. **Display Rush Order Invoice:**
   - The system updates and displays the invoice with separate delivery fees for rush order items and regular items if applicable.
7. **The "Place Order" use case continues**

## Alternative Flows
 **A1. Non-Eligible Address or Products:**
   - If either the address or products are not eligible, the system prompts the customer to update the delivery information or change the delivery method.

 **A2. Adjust Delivery Method or Items:**
   - Customer adjusts the delivery method or the items in the order, and the system recalculates delivery fees and updates the invoice accordingly.

 **A3. Customer Opts Out:**
   - If the customer decides not to proceed with the rush order due to ineligibility or additional costs, they can continue with the standard delivery options.




# "Pay Order" Use Case
## Basic/Success Flow
1. **Select Payment Method:**
   - Customer chooses VNPay as their payment method during the checkout process.
2. **Enter Payment Details:**
   - Customer is prompted to enter payment details such as card information or VNPay account details.
3. **Validate Payment Information:**
   - The software validates the provided payment information for completeness and correctness.
4. **Process Payment:**
   - VNPay processes the payment and returns the transaction status to the software.
5. **Display Transaction Details:**
   - The software displays the transaction ID, cardholder's name, deducted amount, transaction details, and date/time of the transaction.
6. **Email Confirmation:**
   - The software sends a confirmation email to the customer with the order and transaction details.
7. **The "Place Order" use case continues**

## Alternative Flows
 **A1. Payment Information Incomplete or Incorrect:**
   - If payment information is incomplete or incorrect, the customer is asked to provide the necessary details again.

 **A2. Payment Processing Failure:**
   - If the payment fails to process, the customer is informed of the failure and can choose to retry the payment or select a different payment method.

 **A3. Exit Payment Process:**
   - The customer has the option to cancel the payment and exit the payment process at any time before the transaction is completed.
