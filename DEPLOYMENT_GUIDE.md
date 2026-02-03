# Deploying Your Site to Netlify with Password Protection

## Why Netlify?
- **Free** for personal sites
- **Easy** drag-and-drop deployment
- **Built-in password protection** (more secure than JavaScript)
- **Custom domain** support (lucyrowland.ca)
- **Automatic HTTPS**

---

## OPTION 1: Netlify's Built-in Password (RECOMMENDED)

This is the most secure and professional option.

### Steps:

1. **Sign up for Netlify**
   - Go to https://www.netlify.com
   - Click "Sign up" (use GitHub, GitLab, or email)

2. **Deploy Your Site**
   - Click "Add new site" → "Deploy manually"
   - Drag and drop ALL your HTML files:
     - index.html
     - blog.html
     - blog-post-1.html
     - blog-post-2.html
   - Netlify will give you a URL like `random-name-123.netlify.app`

3. **Add Password Protection**
   - Go to your site settings
   - Click "Site details" → "Site protection"
   - Choose "Password protection"
   - Set your password
   - **Done!** Your entire site is now password-protected

4. **Connect Your Custom Domain**
   - In site settings, go to "Domain management"
   - Click "Add custom domain"
   - Enter: `lucyrowland.ca`
   - Netlify will give you DNS settings
   - Update your domain registrar's DNS to point to Netlify
   - Wait 24-48 hours for DNS to propagate

### To Update Your Site Later:
- Just drag and drop new files to Netlify's "Deploys" tab
- Your password protection stays active

---

## OPTION 2: JavaScript Password Page (Backup Option)

If you want to use the custom password page I created:

1. **Rename files:**
   - Rename `index.html` to `main.html`
   - Rename `password.html` to `index.html`

2. **Edit the password:**
   - Open the NEW `index.html` (the password page)
   - Find this line: `const CORRECT_PASSWORD = "YOUR_PASSWORD_HERE";`
   - Change `YOUR_PASSWORD_HERE` to your actual password
   - Save the file

3. **Deploy to Netlify:**
   - Upload all files to Netlify
   - Visitors will see the password page first
   - After entering the password, they'll go to main.html

**Note:** This is less secure than Netlify's built-in protection, but works anywhere.

---

## Connecting lucyrowland.ca to Netlify

Once your site is deployed on Netlify:

1. **Get Netlify's DNS info:**
   - In Netlify: Domain settings → DNS records
   - You'll see something like: `apex-loadbalancer.netlify.com`

2. **Update your domain registrar:**
   - Log into wherever you bought lucyrowland.ca
   - Find DNS settings
   - Add an A record or ALIAS record pointing to Netlify's address
   - Netlify will verify and enable HTTPS automatically

---

## Cost Breakdown

**Netlify Free Plan:**
- ✅ Unlimited sites
- ✅ Password protection
- ✅ Custom domains
- ✅ HTTPS certificates
- ✅ 100GB bandwidth/month (plenty for a portfolio)

**Your Domain (lucyrowland.ca):**
- ~$15-20/year (you already have this)

**Total ongoing cost: $0** (just your annual domain renewal)

---

## When You're Ready to Go Public

To remove password protection later:

**If using Netlify's built-in password:**
- Just go to Site protection settings
- Click "Remove password protection"
- Done!

**If using JavaScript password page:**
- Delete password.html
- Rename main.html back to index.html
- Re-deploy

---

## Need Help?

If you run into any issues:
1. Netlify has excellent docs: https://docs.netlify.com
2. Their support is very responsive (even on free plan)
3. The community forum is helpful: https://answers.netlify.com

Let me know if you hit any snags!
