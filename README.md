# Chillarpay-AI-support-zero-to-few-shot-
Lab 2: From Zero-shot to Few-shot
The ChillarPay Case
Name: [Bharti Williams]        Course: BBA (FinTech), Chitkara Business School        Tool used: Claude
This document has the content of all the files for my GitHub repository (01 to 06 and the README), in order.
File 1: 01_case_study.md
ChillarPay is a fictional UPI payments app in Jaipur, used mainly by college students and small shopkeepers. It has 8 lakh users and receives about 2,000 support messages a day in English and Hinglish. Its 6-person support team cannot keep up, and urgent fraud cases get lost among simple questions.
The Head of Customer Experience asks me, as a Business Analyst: "Can AI sort our messages, set priority and draft replies? When is a simple prompt enough, and when does the AI need examples?"
ChillarPay's support rules (used in every step):
Item	Rule
Categories	Failed Payment, Refund, Fraud Alert, Account & KYC
High priority	Money lost without the customer's consent, or account blocked
Medium priority	Money stuck or delayed, refund pending
Low priority	Information request or profile update
Reply tone	Polite and short; use the customer's first name if given; never promise a refund date; reply in Hinglish if the customer writes in Hinglish

 File 2: 02_dataset.md
Part A: Synthetic customer messages (Step 2)
I used the data prompt from the lab sheet. All names and details are fictional. The set has 8 English and 4 Hinglish messages. The tricky ones are M05 (angry customer), M06 (very short and unclear) and M08 (could fit two categories).
ID	Customer message	Channel
M01	Hi, I paid ₹1,200 to my landlord last evening. The app showed payment failed but the money is deducted from my bank. Please check. - Riya	App chat
M02	Hello, I returned a pair of shoes 6 days ago and the store says my refund of ₹899 has been sent to ChillarPay. I still can't see it. What is the status? Regards, Aman	Email
M03	Maine dukaan par ₹350 pay kiye, paise kat gaye par payment pending dikha raha hai. Dukandaar bol raha hai paise nahi mile. - Sandeep	App chat
M04	Hi team, I changed my SIM and want to update the mobile number linked to my ChillarPay account. What do I need to do? Thanks, Karan	Email
M05	@ChillarPay worst app ever!! Account blocked since morning and I can't take payments in my shop. FIX THIS NOW or I'm uninstalling. #ChillarPayFail	Twitter
M06	money not received	App chat
M07	Hello, naya user hoon. KYC verify karne ka process kya hai? Kaun se documents chahiye?	App chat
M08	My ₹2,000 mobile recharge failed but the amount was deducted. I was told it would be refunded, but 4 days have passed. Is this a failed payment or a refund issue? Please help. Neha	Email
M09	Bhaiya maine apna UPI PIN kisi ko nahi bataya phir bhi ₹7,800 kisi unknown number ko chale gaye. Please jaldi help karo. - Imran	App chat
M10	₹2,499 was debited from my account to a merchant I have never heard of. I did not authorise this. Please help me get it back. - Rohan	App chat
M11	Mera ₹1,500 ka refund abhi tak nahi aaya, order cancel kiye 5 din ho gaye. Please batao kab tak aa jayega? Simran	Email
M12	Quick question @ChillarPay, how long does a refund usually take to reach the account after cancelling an order? Just want to know. Divya	Twitter

Part B: My answer key (Step 3)
I wrote this using the rules table before running any prompt, and I did not change it afterwards.
ID	Correct category	Correct priority
M01	Failed Payment	Medium
M02	Refund	Medium
M03	Failed Payment	Medium
M04	Account & KYC	Low
M05	Account & KYC	High
M06	Failed Payment	Medium
M07	Account & KYC	Low
M08	Refund	Medium
M09	Fraud Alert	High
M10	Fraud Alert	High
M11	Refund	Medium
M12	Refund	Low

 
