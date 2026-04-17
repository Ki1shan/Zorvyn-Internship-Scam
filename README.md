# 🚨 Zorvyn Internship Scam – Technical Investigation Report

## 👨‍💻 Author
Kishan N

---

# 📌 Overview

This report documents a detailed investigation into a suspicious internship opportunity provided by a company named "Zorvyn FinTech Pvt. Ltd."

What initially appeared to be a legitimate cybersecurity internship was later identified as a **well-structured scam system** involving:
- Fake dashboards
- Simulated company infrastructure
- Client-side manipulated systems
- A reimbursement-based payment trap

This report explains step-by-step how the system was analyzed and exposed.

---

# 🎯 Objective

To verify:
- Whether the platform is legitimate  
- Whether backend systems exist  
- Whether reimbursement flow is real  
- Whether user data is securely handled  

---

# 🧠 Investigation Approach

Instead of blindly trusting the system, I approached this like a penetration tester:

- Observed system behavior  
- Analyzed URL structures  
- Tested parameter manipulation  
- Verified backend presence  
- Cross-checked email workflow  

---

# 🧪 Step-by-Step Findings

## 1️⃣ Suspicious Reimbursement Requirement

The company required purchasing software first and promised reimbursement later.

⚠️ Red Flag:
- Legit companies NEVER ask interns to pay upfront

---

## 2️⃣ URL-Based Data Injection

Reimbursement links contained full user data in URL:


/reimbursements/approved?full_name=...&email=...&employee_id=...


### 🔍 Observation:
- Changing values in URL directly changed data on page

### 🚨 Conclusion:
- No backend validation  
- Fully client-side controlled system  

---

## 3️⃣ Parameter Tampering (CRITICAL)

Test performed:
- Modified name, email, and software fields in URL

### ✅ Result:
- Changes reflected instantly

### 🚨 Impact:
- Broken Access Control  
- No data integrity  
- Anyone can manipulate identity  

---

## 4️⃣ Localhost Exposure

Found URLs like:


http://localhost:3003/
...


### 🚨 Conclusion:
- Development environment leaked  
- No proper production deployment  
- Strong indicator of fake / unfinished backend  

---

## 5️⃣ Fake Dashboard Modules

### 📦 Logistics
- Shows "Order Packed"
- No tracking ID or courier integration

👉 Fake delivery simulation

---

### 📧 Webmail
- "Activation in 7–8 days"
- No real inbox

👉 Fake service layer

---

### 👥 Referrals
- Locked system
- Depends on fake webmail

👉 Feature padding for realism

---

## 6️⃣ Domain Switching

- Original domains: `.org / .co`
- Shifted to: `.live`

### 🚨 Conclusion:
- Infrastructure rotation  
- Common phishing/scam technique  

---

## 7️⃣ Psychological Manipulation

The system includes:

- Offer letter (₹45,000 salary)
- Welcome emails
- Manager communication
- Dashboard access
- Fake progress updates

### 🧠 Purpose:
To build trust before triggering payment

---

## 8️⃣ Payment Trap (Core Scam)

Flow:
1. Assign task  
2. Force software purchase  
3. Promise reimbursement  
4. Provide fake portal  
5. No actual payment  

### 🚨 Conclusion:
- Financial exploitation model  

---

# 💻 Technical Summary

| Component | Reality |
|----------|--------|
| Authentication | Weak / bypassable |
| Backend | Not present / simulated |
| Data Handling | Client-side |
| Security | Non-existent |
| Infrastructure | Fake / incomplete |

---

# 🚨 Final Verdict

This is not a legitimate internship system.

This is a:

## ⚠️ FULLY STRUCTURED INTERNSHIP SCAM

Combining:
- Social engineering  
- Fake UI systems  
- Client-side manipulation  
- Payment exploitation  

---

# 🧠 Key Learnings

- Always question reimbursement-based tasks  
- Never trust UI without backend validation  
- URL parameters should NEVER control identity  
- Fake systems can look very realistic  

---

# 🏁 Conclusion

This investigation exposed how attackers can combine **technology + psychology** to create highly convincing scam systems.

As a cybersecurity learner, this experience provided real-world insight into:
- Social engineering attacks  
- Web application flaws  
- Scam infrastructure design  

---

# ⚠️ Disclaimer

This report is created for:
- Educational purposes  
- Awareness  
- Cybersecurity learning  

No harmful actions were performed during this investigation.

---

# 🔥 Final Note

At first, it looked like a dream internship.

But after testing it like a hacker…

It turned out to be a **well-designed trap**.
