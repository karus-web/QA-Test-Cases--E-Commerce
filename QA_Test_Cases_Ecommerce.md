# QA Test Cases – E-commerce Application

I created these test cases as part of my QA practice to understand how real-world e-commerce applications work and how to test them effectively.

---

## 🔐 Signup

### TC-01: Valid Signup
- Enter valid user details  
- Send signup request  

**Expected Result:**  
A new customer account is created and a customer ID is returned.

---

### TC-02: Signup with Existing Email
- Enter an email that already exists  
- Send request  

**Expected Result:**  
The system should reject the request or show that the email is already in use.

---

### TC-03: Signup with Missing Fields
- Leave required fields empty  
- Send request  

**Expected Result:**  
Validation error should be displayed and account should not be created.

---

## 🔑 Login

### TC-04: Valid Login
- Enter correct email and password  
- Send request  

**Expected Result:**  
User is logged in successfully and authentication token is generated.

---

### TC-05: Invalid Login
- Enter correct email and wrong password  

**Expected Result:**  
Login should fail and no token should be returned.

---

### TC-06: Login with Empty Fields
- Leave email or password blank  

**Expected Result:**  
System should return validation or authentication error.

---

## 🛒 Order Placement

### TC-07: Place Order with Valid Data
- Use valid customer ID and token  
- Send order request  

**Expected Result:**  
Order is created successfully and order number is generated.

---

### TC-08: Place Order without Token
- Remove authentication token  
- Send request  

**Expected Result:**  
Request should be rejected as unauthorized.

---

### TC-09: Place Order with Invalid Customer ID
- Use incorrect customer ID  

**Expected Result:**  
Order should not be created and error should be returned.

---

## 📦 Order Details

### TC-10: Add Order Details
- Use valid order number  
- Enter product details  

**Expected Result:**  
Order details are added successfully.

---

### TC-11: Invalid Product Code
- Enter incorrect product code  

**Expected Result:**  
System should return an error for invalid product.

---

## 💳 Payment

### TC-12: Valid Payment
- Enter valid payment details  

**Expected Result:**  
Payment is processed successfully.

---

### TC-13: Payment with Missing Amount
- Leave amount field empty  

**Expected Result:**  
Validation error should be returned.

---

## ❌ Cancel Payment

### TC-14: Cancel Existing Payment
- Use valid check number  

**Expected Result:**  
Payment is cancelled successfully.

---

### TC-15: Cancel Non-existing Payment
- Use invalid check number  

**Expected Result:**  
System should return an error.

---

## 🔁 End-to-End Flow

### TC-16: Full User Journey
- Signup → Login → Order → Payment → Cancel  

**Expected Result:**  
All steps should work correctly and data should remain consistent.

---

## 💡 Note

These test cases are based on API workflows and reflect real-world testing scenarios including authentication, transactions, and data validation.
