# ICMD Global — deploy checklist

## 1. Fill the 3 placeholders in index.html
- **Phone**: find-and-replace `4070000000` (6 hits, tel: links) and `(407) 000-0000` (displayed).
- **Formspree**: sign up free at formspree.io → new form → replace `YOUR_FORM_ID` in the form action.
- **Demo URL**: replace `https://CLEARWAVE_URL.vercel.app` with the deployed Clearwave spec-site URL. (Deploy it first if you haven't: `cd spec-site-pool && vercel --prod`.)

## 2. GitHub + Vercel
```
cd icmd-global-site
git init && git add . && git commit -m "ICMD Global site"
# create repo on github.com, then:
git remote add origin https://github.com/<you>/icmd-global-site.git
git push -u origin main
```
Vercel → New Project → import the repo → deploy (no build settings needed, it's static).

## 3. Domain
Vercel project → Settings → Domains → add your ICMD Global domain → follow the DNS instructions at your registrar. SSL is automatic.

## 4. After launch
- Test the form (Formspree's first submission needs email confirmation).
- Test tap-to-call on your phone.
- Optional: add the site to Google Search Console — same as you'll do for clients.
