# WooCommerce Gift Voucher System

## Overview:
This snippet creates a **custom gift voucher** system for WooCommerce, allowing customers to purchase a voucher of their desired amount (minimum €50). The voucher is then delivered to the recipient (via email) with a custom code. The functionality includes the ability to:
- Choose the voucher amount.
- Redirect to a custom checkout page.
- Ensure only one voucher per cart.
- Generate and email a gift voucher code after payment.
- Provide detailed recipient information and delivery via email.

## Features:
1. **Custom Voucher Amount:**
   - The buyer can choose a custom voucher amount, starting from €50.
   - Price is validated on the product page and checkout.

2. **Voucher Only Cart:**
   - Only one voucher can be added to the cart at a time. All other items are removed automatically.

3. **Redirect to Custom Checkout:**
   - After adding the voucher to the cart, the customer is automatically redirected to a special checkout page.

4. **Recipient's Email Field:**
   - An extra checkout field allows the buyer to enter the recipient's email for gift delivery.

5. **Voucher Creation:**
   - Upon order completion, a coupon code is generated automatically.
   - The coupon is saved in the order metadata for future reference.

6. **Email Notifications:**
   - The recipient or the buyer receives an email with the voucher code and details.
   - If the recipient's email is not provided, the voucher is sent to the buyer.

7. **Custom Styling:**
   - The gift voucher section and email notifications have custom styling to highlight the gift option.

8. **Voucher Expiry:**
   - The gift voucher expires after one year from the creation date.

9. **Admin Order Management:**
   - Details about the recipient (name, email) are saved in the order metadata and shown in the admin order screen.

## Installation:

1. **Add the Code to Functions.php:**
   - Copy and paste the entire snippet into your theme's `functions.php` file or use a plugin like **Code Snippets** to manage the code.

2. **Product Setup:**
   - Ensure that the **Gift Voucher** product exists in your store with the **ID `989232`**.
   - The product must be a simple product or a parent product for variations.

3. **Custom Checkout URL:**
   - Change the `CHECKOUT_URL` constant to your desired checkout page URL.

4. **Voucher Expiry Configuration:**
   - Modify the `VOUCHER_EXPIRY` constant to adjust the expiration period of the voucher (default is 1 year).

## How It Works:

1. **Product Page:**
   - The buyer chooses a custom voucher amount on the product page (minimum €50). 

2. **Checkout:**
   - The buyer can enter the recipient's name and email address.
   - Only one voucher can be added to the cart, removing any other products.

3. **Payment & Order Completion:**
   - After the payment is completed, the coupon code is automatically generated and saved in the order.
   - The recipient or the buyer receives an email with the voucher code.

4. **Admin:**
   - Admins can view the recipient details and voucher code from the order details page.

## Configuration Constants:

- **VOUCHER_PRODUCT_ID**: The ID of the gift voucher product (default is 989232).
- **VOUCHER_MIN_AMOUNT**: Minimum voucher amount (default is €50).
- **VOUCHER_EXPIRY**: Expiry period for the voucher (default is `+1 year`).
- **CHECKOUT_URL**: URL to redirect after adding the voucher to the cart (default is `https://butt.gr/checkout-2/`).

## Changelog:

#### 1.0.0:
- Initial release: Complete Gift Voucher functionality for WooCommerce.
