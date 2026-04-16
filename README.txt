=========================================================
  YOUR WEBSITE — HOW EVERYTHING WORKS
  (Read this once. Then you'll never need anyone's help.)
=========================================================

YOUR FOLDER STRUCTURE
─────────────────────
wedding-site-v2/
│
├── index.html         ← The website. Don't touch this.
│
├── data.json          ← YOU EDIT THIS for prices, names, phone number
│
└── images/
    ├── varmala/       ← Put varmala photos here
    ├── sangeet/       ← Put sangeet/mehndi photos here
    ├── stage/         ← Put stage decoration photos here
    ├── car/           ← Put car decoration photos here
    ├── jewellery/     ← Put flower jewellery photos here
    └── gajre/         ← Put gajre photos here


════════════════════════════════════════
HOW TO ADD A NEW PHOTO
════════════════════════════════════════

STEP 1: Put your photo into the right folder
  Example: A varmala photo → drop it into  images/varmala/
  Name it simply, no spaces:  varmala-15.jpg  or  lotus-pink.jpg

STEP 2: Open data.json and find the matching service
  Example: find the "varmala" section, look for "photos": [...]

STEP 3: Add your filename inside the quotes list
  Before:
    "photos": ["varmala-01.jpg", "varmala-02.jpg"]

  After:
    "photos": ["varmala-01.jpg", "varmala-02.jpg", "varmala-15.jpg"]

  (Just add a comma and the filename in quotes)

STEP 4: Save data.json

STEP 5: Push to GitHub (see PUSH COMMANDS below)
  Done! Photo appears on the website automatically.


════════════════════════════════════════
HOW TO CHANGE A PRICE
════════════════════════════════════════

Open data.json → find the service → change "price_range"

Example — to change varmala price:
  Before:  "price_range": "₹2,500 – ₹8,000"
  After:   "price_range": "₹3,000 – ₹10,000"

Save → push to GitHub → done!


════════════════════════════════════════
HOW TO CHANGE YOUR PHONE / WHATSAPP
════════════════════════════════════════

Open data.json → at the top, find "business" section:
  "phone": "919999999999"
  "whatsapp": "919999999999"

Replace with your real number (keep 91 at start, no + or spaces).
Example: +91 98765 43210 → write as → 919876543210

Save → push → all WhatsApp buttons update automatically!


════════════════════════════════════════
PUSH COMMANDS (copy-paste every time you update)
════════════════════════════════════════

cd wedding-site-v2
git add .
git commit -m "Updated photos and prices"
git push

That's it. 4 lines. Site updates in 1 minute.


════════════════════════════════════════
FIRST TIME SETUP (do only once)
════════════════════════════════════════

# 1. Go to your site folder
cd wedding-site-v2

# 2. Initialize git
git init

# 3. Connect to your GitHub repo
git remote add origin https://github.com/Monikarana27/wedding-services-site.git

# 4. Push everything
git add .
git commit -m "First upload"
git branch -M main
git push -u origin main

# 5. Connect GitHub to Netlify:
#    - Go to netlify.com → Log in → Add new site → Import from GitHub
#    - Choose your repo → Deploy
#    - Done! Every time you push to GitHub, Netlify auto-updates your website.


════════════════════════════════════════
PHOTO NAMING RULES (important!)
════════════════════════════════════════

✓ Good names:  varmala-15.jpg   lotus-pink.jpg   rose-varmala.jpg
✗ Bad names:   My Photo (1).jpg   varmala FINAL!.JPG   नई फोटो.jpg

Rules:
- English letters only
- No spaces (use - instead)
- No brackets, exclamation marks, or Hindi text in filename
- .jpg or .jpeg extension

=========================================================
