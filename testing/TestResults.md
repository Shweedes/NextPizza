# NextPizza — Test Results

| ID  | Purpose | Scenario | Expected Result | Actual Result | Pass/Fail |
|-----|---------|----------|-----------------|---------------|-----------|
| TC1 | User Registration | 1. Click "Register"<br>2. Enter valid email, name, password<br>3. Submit | Account created, user logged in, redirected to main page | Registration successful, automatic login working | ✅ Pass |
| TC2 | User Registration (Duplicate) | 1. Try to register with existing email<br>2. Submit | Error message displayed | Proper error message shown: "Email already exists" | ✅ Pass |
| TC3 | Guest Browsing | 1. Open app without login<br>2. Browse menu<br>3. Add items to cart | Can view menu and cart, but prompted to login at checkout | Functionality working as expected | ✅ Pass |
| TC4 | Add to Cart | 1. Select pizza<br>2. Customize size, toppings<br>3. Add to cart | Item appears in cart with correct customization and price | All customizations saved, price calculated correctly | ✅ Pass |
| TC5 | Cart Quantity Update | 1. Add item to cart<br>2. Increase quantity<br>3. Decrease quantity | Cart total updates correctly, item removed when quantity 0 | Quantity changes working, total recalculated | ✅ Pass |
| TC6 | Promo Code (Valid) | 1. Enter valid promo code in cart<br>2. Apply | Discount applied to total | Discount calculated and displayed correctly | ✅ Pass |
| TC7 | Promo Code (Invalid) | 1. Enter invalid promo code<br>2. Apply | Error message displayed | Proper error message: "Invalid promo code" | ✅ Pass |
| TC8 | Order Placement | 1. Login<br>2. Fill cart<br>3. Enter delivery address<br>4. Place order | Order confirmation shown with estimated delivery time | Order successfully placed, confirmation displayed | ✅ Pass |
| TC9 | Online Payment | 1. Place order with online payment<br>2. Complete payment flow | Payment processed, order status "Paid" | Payment gateway integration working | ✅ Pass |
| TC10 | Cash Payment | 1. Place order with cash payment<br>2. Complete order | Order status "Pending Payment" | Cash payment option working correctly | ✅ Pass |
| TC11 | Order Tracking | 1. Place order<br>2. Check order status in profile | Current status displayed with timeline | Status tracking working, updates visible | ✅ Pass |
| TC12 | Profile Update | 1. Edit profile information<br>2. Save changes | Profile updated successfully | Changes persisted correctly | ✅ Pass |
| TC13 | Order History | 1. View order history<br>2. Check past order details | Complete order history with details visible | History displayed correctly with all details | ✅ Pass |
| TC14 | Mobile Responsiveness | 1. Use app on mobile device<br>2. Test all major functions | All features accessible, touch-friendly interface | Responsive design working on mobile devices | ✅ Pass |
| TC15 | Browser Compatibility | 1. Test on Chrome, Firefox, Safari<br>2. Verify all functionality | Consistent experience across browsers | No major compatibility issues found | ✅ Pass |
| TC16 | Performance | 1. Test page load times<br>2. Test under simulated load | Pages load within 3 seconds, system responsive under load | Performance requirements met | ✅ Pass |
