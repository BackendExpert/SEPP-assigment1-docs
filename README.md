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

### AI Equipment Search

 "I need a powerful drill for concrete."

- AI work

```text

Customer request
      ↓
Fine-tuned model
      ↓
Understand intent
      ↓
Equipment search API
      ↓
MongoDB
      ↓
Suitable equipment
      ↓
AI response


```

### AI Rental Cost Assistant

```text

"How much is this generator from September 8 at 9 AM until September 10 at 3 PM?"

```


```text

Customer
   ↓
AI
   ↓
Extract:
equipment
start
end
branch
   ↓
NestJS quotation API
   ↓
Rental Engine
   ↓
Holiday calculation
   ↓
Pricing
   ↓
VAT
   ↓
Quotation
   ↓
AI explains result


```

### AI Equipment Information Assistant - Rag vectorDB 

```text

"What is this machine used for?"

```

- rag vector workflow

```text

Equipment manuals
Equipment descriptions
Specifications
Safety documentation
FAQs
        ↓
Embedding
        ↓
Vector database
        ↓
RAG
        ↓
Fine-tuned AI

```

### AI FAQ / Policy Assistant

- chatbot

- create pdf upload 


## for AI

### Fine-tuning

- Teach your model:

- - Customer-service behaviour
- - Domain terminology
- - Response style
- - Intent recognition
- - Equipment-related conversational patterns
- - Sinhala/Tamil/English patterns

- AI access to DB and filtering data


# Tool Rental Product List

## Construction

- Rotary Hammer
- SDS Hammer Drill
- Demolition Hammer
- Concrete Mixer
- Plate Compactor
- Concrete Vibrator
- Cut-Off Saw
- Angle Grinder
- Core Drill
- Diamond Cutter
- Tile Cutter
- Rebar Cutter
- Rebar Bender
- Laser Level
- Rotary Laser
- Jackhammer
- Scaffold Tower
- Material Hoist
- Floor Grinder
- Concrete Planer

## Cleaning

- Pressure Washer
- Wet/Dry Vacuum
- Carpet Cleaner
- Floor Scrubber
- Floor Polisher
- Steam Cleaner
- High-Pressure Cleaner
- Drain Cleaner
- Industrial Vacuum
- Upholstery Cleaner
- Sweeper
- Air Mover

## Landscaping

- Brush Cutter
- Hedge Trimmer
- Chainsaw
- Lawn Mower
- Sod Cutter
- Stump Grinder
- Wood Chipper
- Leaf Blower
- Earth Auger
- Tiller
- Scarifier
- Pole Saw

## Power

- Petrol Generator
- Diesel Generator
- Inverter Generator
- Portable Power Station
- Battery Power Station
- Generator Transfer Switch
- Extension Distribution Board
- Site Transformer
- Portable Lighting Tower
- Work Light

## Pumps

- Submersible Drainage Pump
- Dirty-Water Pump
- Clean-Water Pump
- Sewage Pump
- Petrol Water Pump
- Diesel Water Pump
- High-Pressure Pump
- Trash Pump
- Dewatering Pump
- Sludge Pump

