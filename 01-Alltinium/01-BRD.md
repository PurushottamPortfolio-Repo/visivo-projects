### This is the **_BRD_** for **_Alltinium_** project delivery which is discussed between me and Visivo at **_Venture X_** on 08-07-2026.

> Inside this project we have to develop a company **_product showcase portfolio website_** using below stack.

```text
Teck Stack :
    1. Next.Js
    2. TypeScript
    3. Tailwind CSS
    4. Shad CN Components
    5. Resend Email System
    6. Cookies for sessions
    7. DataBase for otp storage and user verification
```

# What pages and sections should contain

## 1. Home Page [Landing Page]

### HeroSection
- Background Image
- Content displayed(title and text)
- Buttons(color, style)
- Below stripe display

### Displaying marquee section
- Content

### ServicesSection
- Background 
- Content
- Cards 

### Material Section
- Background
- content
- material card

### Why choose us
- Background
- content
- material card

### Network Section
- Background
- content
- network map

### Industries Section
- Background
- Content 
- Cards

### CTA Section
- Background colour gradient
- Content
- Buttons
- Cards

### Blog Section
- Background
- content
- Blogs card

---

## 2. About Page

### HeroSection
- Background Image
- Content displayed(title and text)
- Buttons(color, style)
- Below stripe display

### Content about the compnay
- Image 
- Company detail

### What drives us
- Content
- Cards

### Founder Images
- Iamges
- Social Icons
- Content about the founders

### Timeline
- Content 
- logo
- Style

### Below stripe

- Content
- Button

---

## 3. Materials Page

### Page Layout

### HeroSection
- Image and content

### Material Cards
- Material Image
- Material Title
- Grade
- Specifications
- Applications
- Buttons (RFQ & Datesheet)

---

## 4. Services Page

### HeroSection
- Image
- content & buttons

### Services Display
- Cards

### Service Card
- Content

---

## 5. Contact Page

### HeroSection
- Image
- Content & Buttons

### Form 
- Content

### Form Inputs
- Name*
- Email*
- Company(optional)
- Phone(optional)
- Topic dropdown*
  - Sales/RFQ (default)
  - Partner Onboarding
  - Lab Test Booking
  - Press
  - Others
- Message*

### Form Validation
- Set max and min input length
- Email verification via otp

### Company details
- Email
- Phone
- HeadQuarter Address
- Branches(if available)

---

## RFQ Form

- All Fields as per lovable


## Email Verification Setup

```text
OTP valid: 5 minutes
Resend cooldown: 60 seconds
Max resends: 3
Verification cookie: 30 minutes
Rate limit: 5 OTP requests/hour/email
```

```text
             User opens Contact/Quote Form
                       │
                       ▼
             Enter Email Address
                       │
                       ▼
       Check "email_verified" Cookie
                       │
          ┌────────────┴────────────┐
          │                         │
        Exists                   Doesn't Exist
          │                         │
          ▼                         ▼
   Skip OTP Screen           Generate OTP
          │                         │
          │                  Save OTP in DB
          │                         │
          │                  Send Email (Resend)
          │                         │
          │                         ▼
          │                  User enters OTP
          │                         │
          │                         ▼
          │                 Verify OTP
          │                         │
          │                         ▼
          │         Create HttpOnly Cookie (30 min)
          │                         │
          └──────────────► User Verified
                                   │
                                   ▼
                     Contact & Quote Forms Submit
```

### Search bar logic

```text
┌──────────────────────────────────────────────────────────────┐
│ 🔍 Search materials...                                      │
└──────────────────────────────────────────────────────────────┘

Material Categories

[ All 52 ] [ Aluminium 18 ] [ Titanium 12 ]
[ Nickel 10 ] [ Special Steels 12 ]

Material Forms

[ All 52 ] [ Bar 18 ] [ Plate 8 ]
[ Sheet 9 ] [ Pipe 5 ] [ Tube 12 ]

───────────────────────────────────────────────────────────────

Available Materials                      Clear Filters

Showing 18 materials

┌──────────────┐ ┌──────────────┐ ┌──────────────┐
│              │ │              │ │              │
│ MaterialCard │ │ MaterialCard │ │ MaterialCard │
│              │ │              │ │              │
└──────────────┘ └──────────────┘ └──────────────┘

```

---