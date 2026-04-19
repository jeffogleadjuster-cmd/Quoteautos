# QuoteAutos deployable package

This package gives you:
- a public QuoteAutos website
- a 5-step quote flow
- primary / fallback / manual-review quote logic demo
- a hidden staff CRM page
- simple trickle marketing campaign view
- a built-in quote-completion assistant chatbot

## The hidden CRM page
Your private CRM page is:
`/staff-portal`

Use your staff code to open it.
Default code:
`quoteautoscrm`

Change it in your environment variables after deployment.

## Super easy publish steps

### 1) Make a free Vercel account
Go to Vercel and sign in with Google.

### 2) Create a free Supabase account
Go to Supabase and create a project.

### 3) In Supabase, create a table named `quotes`
Use these columns:
- id → uuid, primary key, default generated
- created_at → timestamp with time zone, default now()
- applicant → text
- email → text
- phone → text
- zip → text
- vehicle → text
- path → text
- status → text
- assigned_to → text
- notes → text
- homeowner → text
- insured → text
- drip → text
- form_snapshot → jsonb
- result_snapshot → jsonb

### 4) In Supabase, get these two values
- Project URL
- Service Role Key

### 5) In Vercel, upload this folder as a new project
After upload, open your project settings and add environment variables:
- SUPABASE_URL
- SUPABASE_SERVICE_ROLE_KEY
- CRM_ACCESS_CODE

### 6) Deploy
Vercel will give you a live URL.

### 7) Connect your domain from Network Solutions
In Vercel, add your domain.
Then copy the DNS records Vercel shows you into Network Solutions.

## If you do nothing with Supabase yet
The public website still runs.
The CRM shows demo records only.
New quote submissions will not save permanently until Supabase is connected.

## Local testing if you ever want it
1. install Node.js
2. open this folder in a terminal
3. run `npm install`
4. run `npm run dev`
5. open `http://localhost:3000`

## What the chatbot does
This is a built-in helper, not a paid AI chatbot.
It helps users finish their quote by showing short prompts at the right moments.
