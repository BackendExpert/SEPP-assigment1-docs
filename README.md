# Lanka Tool Hire (Pvt) Ltd

## Fuctions

## Customer Web Application

-	Registration/login 
-	Equipment catalogue 
-	Categories 
-	Search 
-	Basic filters 
-	Equipment details 
-	Branch information 
-	Rental pricing 
-	Rental calculator 
-	Quotation 
-	Reviews 
-	Comments 
-	Company responses 
-	AI assistant

## Rental & Quotation Engine
-	Hourly price 
-	Daily price 
-	Weekly price 
-	Rental duration calculation 
-	Start/end date & time 
-	Poya/public holiday handling 
-	Branch closure validation 
-	VAT calculation 
-	Quotation breakdown 
-	Quotation number 
-	Price snapshot

## Review System

### Ratings

- Use only 5 categories:


1.	Equipment Performance 
2.	Customer Service 
3.	Technical Support 
4.	After-Sales Support 
5.	Overall Experience 

### Customers can:
-	Write review 
-	Give ratings 
-	Comment 
-	Reply to comments 
-	Report review 

### Company can:

-	Respond 

### Moderator:

-	Approve 
-	Reject


## Multilingual Support

- For the prototype:
- -  UI can support the three languages 
- -  Reviews support all three 
- -  Comments support all three 
- -  AI supports all three


## Admin Portal

### Equipment

- Add 
- Edit 
- Delete/archive 
- Images 
- Description 
- Specifications 
- Category 

### Pricing

- Hourly 
- Daily 
- Weekly 
- Monthly/long-term 

### Branches

- Add/edit 
- Opening hours 
- Closure status 

### Holidays

- Poya days 
- Public holidays 

### Reviews

- Pending 
- Approve 
- Reject 
- Hide 

### Users

- Customer 
- Admin 
- Moderator



## React Native Mobile App

```text

Login
 ↓
Home
 ↓
Catalogue
 ↓
Search
 ↓
Equipment Details
 ↓
Rental Calculator
 ↓
Quotation
 ↓
Reviews
 ↓
AI Assistant

```

## Final architecture

```text

                 ┌──────────────────┐
                 │ Customer Website │
                 │ React + Vite     │
                 └────────┬─────────┘
                          │
                 ┌────────▼─────────┐
                 │ Customer Mobile  │
                 │ React Native     │
                 └────────┬─────────┘
                          │
                 ┌────────▼─────────┐
                 │    NestJS API    │
                 └────────┬─────────┘
                          │
       ┌──────────────────┼──────────────────┐
       │                  │                  │
       ▼                  ▼                  ▼
  Catalogue         Rental Engine       Review System
       │                  │                  │
       │             VAT/Holidays       Moderation
       │                  │                  │
       └──────────────────┼──────────────────┘
                          │
                    ┌─────▼─────┐
                    │   MongoDB │
                    └───────────┘
                          │
                    ┌─────▼─────┐
                    │ AI Service│
                    └─────┬─────┘
                          │
                 Fine-tuned Model
                          +
                         RAG
                          +
                    Tool Calling

```


## MVP should actually be this

### Backend

- NestJS
- MongoDB

- Auth
- Equipment
- Categories
- Branches
- Pricing
- Holidays
- Quotation
- Reviews
- Moderation
- AI

### Catalogue

- Search
- Equipment Details
- Rental Calculator
- Quotation
- Reviews
- AI
- Admin


### Mobile

- Catalogue
- Search
- Equipment
- Quotation
- Reviews
- AI

### AI

```text

Fine-tuned model
+
RAG
+
Tool calling
+
English/Sinhala/Tamil

```


## AI features

### AI Customer Service Assistant

This should be the main AI feature.

Customer can ask naturally:

```text


"I need a machine for removing water from a construction site."

"What equipment can I rent for painting a house?"

"Can I get a generator from Kandy?"

"How much would a pressure washer cost for three days?"


```

The AI understands the request and helps the customer.