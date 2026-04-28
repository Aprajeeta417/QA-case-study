# 🧪 QA Case Study – KeaBuilder Platform

**Candidate:** [Aprajeeta singh]  
**Role:** QA Engineer  
**Project:** VARYNT (AI SaaS)  
**Time Taken:** ~24 hours  

---

## 1. 🧠 Testing Approach

My approach focused on **risk-based testing and exploratory testing**, prioritizing critical user flows.

### 🔑 Core Flows Identified
- Landing page creation → publish  
- Form creation → lead capture  
- Funnel navigation → conversion flow  
- AI usage → content generation / chatbot  

### 🧩 Strategy
- Focus on **P0 (critical) flows first**
- Combine:
  - Functional testing
  - Edge case testing
  - Negative testing
- Ensure coverage of:
  - Data integrity
  - User experience
  - System reliability

---

## 2. ⚠️ Risk Analysis

### 🔴 High Risk (P0)
- Lead data not saved or lost  
- Funnel navigation breaks  
- Preview vs published mismatch  
- Form validation bypass  
- Security issues (XSS / unauthorized access)  
- Duplicate submissions due to missing control  

### 🟠 Medium Risk (P1)
- AI response delays or failures  
- Duplicate leads stored  
- Integration failures (CRM/email)  
- UI inconsistencies in builder  

### 🟡 Low Risk (P2)
- Minor UI misalignment  
- Cosmetic issues  
- Non-critical animation glitches  

---

## 3. 🐞 Sample Bugs Identified

### Bug 1: Form Validation Bypass
- **Severity:** High  
- Required fields are not validated properly  
- Invalid email formats are accepted  
- Leads stored with incorrect data  

---

### Bug 2: Preview vs Live Page Mismatch
- **Severity:** High  
- Published page does not match preview  
- Layout and styling differences observed  

---

### Bug 3: Funnel Break After Step Deletion
- **Severity:** High  
- Removing a funnel step breaks navigation flow  
- Users get stuck in funnel  

---

### Bug 4: AI Response Timeout
- **Severity:** Medium  
- Long prompts cause no response or timeout  
- Poor user experience  

---

### Bug 5: Duplicate Lead Creation
- **Severity:** Medium  
- Same form submitted multiple times creates duplicates  
- No deduplication logic  

---

## 4. ✅ Test Cases

### 🧾 Form Testing

| ID | Scenario | Expected Result | Priority |
|----|--------|----------------|----------|
| TC-01 | Valid form submission | Lead saved successfully | High |
| TC-02 | Empty required fields | Validation error shown | High |
| TC-03 | Invalid email format | Error message displayed | High |
| TC-04 | Rapid submissions | Rate limiting applied | High |
| TC-05 | Network failure | Retry/error handling shown | Medium |

---

### 🧱 Landing Page Builder

| ID | Scenario | Expected Result | Priority |
|----|--------|----------------|----------|
| TC-06 | Create page | Page saved successfully | High |
| TC-07 | Drag & drop elements | Proper rearrangement | Medium |
| TC-08 | Mobile view | Responsive layout | High |
| TC-09 | Large page load | No crash or lag | Low |

---

### 🔄 Funnel Testing

| ID | Scenario | Expected Result | Priority |
|----|--------|----------------|----------|
| TC-10 | Step navigation | Correct flow execution | High |
| TC-11 | Conditional logic | Proper branching | High |
| TC-12 | Page refresh mid-flow | State preserved | Medium |

---

### 🤖 AI Testing

| ID | Scenario | Expected Result | Priority |
|----|--------|----------------|----------|
| TC-13 | Content generation | Valid output generated | Medium |
| TC-14 | Unsafe prompts | Blocked or sanitized output | High |
| TC-15 | Large prompts | Handled without crash | Medium |

---

## 5. 🧠 Exploratory Testing Insights

- Multi-tab editing caused state conflicts  
- Slow network caused duplicate submissions  
- Complex funnels exposed logic inconsistencies  
- AI prompts sometimes returned unexpected outputs  

---

## 6. 🔐 Security Considerations

- XSS via input fields  
- SQL injection attempts  
- Unauthorized data access risks  
- AI prompt injection risks  
- API exposure vulnerabilities  

---

## 7. ⚡ Performance Considerations

- Landing page load under high traffic  
- AI response latency under load  
- Funnel execution delays  
- Large form submission handling  

---

## 8. 📊 Test Strategy Summary

### Automation Candidates
- Form validation  
- API testing  
- Funnel flows  

### Manual Testing Focus
- UI builder experience  
- AI output validation  
- Edge cases & usability  
 

---

## 🚀 Notes

- Focused on **real-world QA scenarios**
- Prioritized **business-critical flows**
- Balanced functional, UI, and backend testing
