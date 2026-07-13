### This is the **_BRD_** for **_Alltinium_** project delivery which is discussed between me and Visivo at **_Venture X_** on 08-07-2026.

> Inside this project we have to develop a company **_product showcase portfolio website_** using below stack.

```text
Frontend :
    1. Next.Js
    2. TypeScript
    3. Tailwind CSS
    4. Shad CN Components
    5. Resend Email System
    6. Cookies for Email verification
```

#

## What pages should contain

### Home Page

### About Page

### Service Page

### Material Page

### Contact Page

### Quote Form Fields

## Verification Setup

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
