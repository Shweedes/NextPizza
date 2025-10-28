# NextPizza — Test Plan

## 1. Introduction
This document describes the test strategy, objectives, and scope for the NextPizza Web Application. The goal of this testing phase is to validate that the application meets its functional and non-functional requirements as specified in the SRS, ensuring a high-quality user experience for online pizza ordering.

## 2. Test Items
The following components are subject to testing:
- **NextPizza Frontend**: Next.js-based frontend for menu browsing, cart management, and order processing
- **Backend API**: REST API for menu management, order processing, and user authentication
- **Payment Integration**: Integration with payment gateway (Stripe/CloudPayments)
- **Map Integration**: Delivery address selection using maps API
- **Integrated System**: End-to-end workflow from menu browsing to order completion

**Key Quality Attributes (based on ISO 25010):**
- Functional Suitability
- Performance Efficiency
- Compatibility
- Usability
- Reliability
- Security
- Maintainability
- Portability

## 3. Risk Issues
- Payment gateway integration failures
- Real-time inventory synchronization issues
- Geolocation accuracy for delivery areas
- Cross-browser compatibility for responsive design
- Data privacy and payment security
- Performance under high load during peak hours

## 4. Features to Be Tested
### Functional:
- User Authentication (Registration, Login, Logout)
- Menu Browsing and Product Customization
- Cart Management (Add, Remove, Update Quantities)
- Promo Code Application
- Order Placement and Processing
- Payment Processing (Online/Cash)
- Order Status Tracking
- User Profile Management
- Order History Viewing
- Responsive UI (Mobile & Desktop)

### Non-Functional:
- UI Responsiveness across devices
- Security (Password Hashing, HTTPS, Payment Data Protection)
- Performance under load
- Accessibility (WCAG Compliance)
- Error Handling and User Feedback
- Cross-browser Compatibility
- Mobile App-like Experience on Web

## 5. Test Approach
- **Unit Testing**: Jest & React Testing Library for frontend; appropriate framework for backend
- **Integration Testing**: API endpoint testing with Postman; payment gateway integration testing
- **System Testing**: End-to-end testing with Cypress or Selenium
- **Usability Testing**: Manual testing of ordering workflow with real users
- **Security Testing**: Penetration testing for authentication and payment flows
- **Performance Testing**: Load testing for peak order periods

## 6. Pass/Fail Criteria
### Test Scenarios (Examples):

| ID  | Purpose | Scenario | Expected Result |
|-----|---------|----------|-----------------|
| TC1 | User Registration | Enter valid email, name, password | Account created successfully, user logged in |
| TC2 | Guest Browsing | Browse menu without login | Can view menu and add to cart, prompted to login at checkout |
| TC3 | Add to Cart | Select pizza, customize options, add to cart | Item appears in cart with correct options and price |
| TC4 | Cart Management | Update quantities, remove items | Cart total updates correctly, items properly managed |
| TC5 | Promo Code Application | Enter valid promo code | Discount applied to order total |
| TC6 | Order Placement | Complete order with delivery address and payment | Order confirmation shown, status "Accepted" |
| TC7 | Online Payment | Process payment with card | Payment successful, order confirmed |
| TC8 | Order Tracking | Check order status in profile | Current status displayed accurately |
| TC9 | Mobile Experience | Use app on mobile device | All functions accessible, touch-friendly interface |
| TC10 | Profile Management | Update user information | Changes saved successfully |

## 7. Exit Criteria
Testing will be considered complete when:
- All critical test cases pass
- No blocking issues remain
- Security review completed
- Performance benchmarks met
- Usability testing shows positive results

## 8. Conclusion
This test plan ensures comprehensive validation of the NextPizza application against both functional and non-functional requirements. Successful execution will confirm the system is secure, user-friendly, and reliable for commercial operation.
