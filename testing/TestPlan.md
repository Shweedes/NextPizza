# NextPizza — Test Plan

## 1. Introduction
This document describes the test strategy, objectives, and scope for the NextPizza web application. The goal of this testing phase is to validate that the application meets its functional and non-functional requirements as specified in the SRS, ensuring a high-quality user experience for pizza ordering.

## 2. Test Items
The following components are subject to testing:
- **NextPizza Frontend**: Next.js-based user interface for customer interactions
- **Backend API**: REST API for menu, cart, orders, and authentication
- **Database**: User data, menu items, and order storage
- **Integrated System**: End-to-end workflow from UI to order completion

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
- Internet dependency for ordering and payment processing
- Cross-browser compatibility for the Next.js frontend
- Data integrity and user isolation
- Security risks related to authentication and payment data
- Integration risks with external payment gateways
- Real-time order status updates reliability

## 4. Features to Be Tested

### Functional:
- User Registration and Authentication
- Menu Browsing and Product Selection
- Product Customization (sizes, ingredients)
- Shopping Cart Management
- Promo Code Application
- Order Placement and Checkout Process
- Order Status Tracking
- User Profile Management
- Payment Processing (online/cash)
- Order History Viewing

### Non-Functional:
- UI Responsiveness across devices (mobile/desktop)
- Performance (page load times, interface responsiveness)
- Security (password hashing, JWT, HTTPS, payment security)
- Accessibility (keyboard navigation, screen readers)
- Error Handling and User Feedback
- Cross-browser Compatibility

## 5. Test Approach
- **Unit Testing**: Jest and React Testing Library for frontend components
- **Integration Testing**: API endpoint testing with Postman
- **System Testing**: End-to-end testing with Cypress
- **Usability Testing**: Manual testing of user workflows
- **Security Testing**: Authentication and data protection validation
- **Performance Testing**: Load time and responsiveness measurement
- **Compatibility Testing**: Cross-browser and mobile device testing

## 6. Pass/Fail Criteria

### Test Scenarios (Examples):

| ID  | Purpose | Scenario | Expected Result |
|-----|---------|----------|-----------------|
| TC1 | Guest Menu Browsing | Browse menu without login | Full menu accessible, can add to cart |
| TC2 | User Registration | Register with email, name, password | Account created, user logged in |
| TC3 | User Login | Login with valid credentials | Access to full features, redirect to main page |
| TC4 | Product Customization | Select pizza, choose size and toppings | Customized product added to cart with correct price |
| TC5 | Cart Management | Add/remove items, change quantities | Cart updates correctly, totals recalculated |
| TC6 | Promo Code Application | Apply valid/invalid promo codes | Discount applied or error message shown |
| TC7 | Checkout Process | Complete order with address and payment | Order confirmed, status shows "Accepted" |
| TC8 | Order Tracking | View order status in profile | Current status displayed with timeline |
| TC9 | Profile Management | Update user information | Changes saved and reflected immediately |
| TC10 | Payment Processing | Complete online payment | Payment processed, order confirmed |
| TC11 | Mobile Responsiveness | Use app on mobile device | All functions accessible, UI adapts correctly |

## 7. Suspension Criteria and Resumption Requirements
- Testing suspended if critical bugs prevent core functionality (ordering, payment)
- Resumption requires fix verification and smoke test passing
- Security vulnerabilities require immediate suspension

## 8. Test Deliverables
- Test Plan
- Test Cases
- Test Results Report
- Bug Reports
- Test Summary Report
