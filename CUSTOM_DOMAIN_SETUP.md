# Custom Domain Setup for GitHub Pages

## Understanding the Current URL

Your site is currently at: `https://boyeshi.github.io/eademola.github.io/`

This is because:
- Repository owner: `Boyeshi`
- Repository name: `eademola.github.io`
- GitHub treats this as a **project page**, not a user page

## Why Not `https://eademola.github.io`?

For a site to be at `https://eademola.github.io`, you would need:
- A GitHub account named `eademola`
- A repository named `eademola.github.io` under that account
- This is called a "User Pages" site in GitHub terminology

## Best Solution: Use a Custom Domain (Recommended)

A custom domain is more professional and gives you full control. Here's how:

---

### Step 1: Purchase a Domain

**Recommended Registrars:**
- [Namecheap](https://www.namecheap.com) - ~$12/year
- [Google Domains](https://domains.google) - ~$12/year  
- [Cloudflare](https://www.cloudflare.com/products/registrar/) - At-cost pricing

**Domain Suggestions:**
- `eniolaademola.com`
- `eademola.com`
- `eademola.ca` (for Canada)
- `eniolaademola.me`

---

### Step 2: Configure DNS Records

After purchasing, add these DNS records in your domain registrar:

#### For Apex Domain (e.g., `eademola.com`):

Add **4 A records** pointing to GitHub Pages IPs:
```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

#### For www Subdomain:

Add a **CNAME record**:
```
Type: CNAME
Name: www
Value: boyeshi.github.io
```

---

### Step 3: Configure GitHub Pages

1. Go to your repository: `https://github.com/Boyeshi/eademola.github.io`
2. Click **Settings** → **Pages**
3. Under **Custom domain**, enter your domain: `eademola.com`
4. Click **Save**
5. Check **Enforce HTTPS** (after DNS propagates, ~24 hours)

---

### Step 4: Wait for DNS Propagation

- DNS changes take 15 minutes to 48 hours to propagate
- Check status: https://dnschecker.org
- Once propagated, your site will be live at your custom domain

---

## Alternative: Transfer Repository to New Account

If you create a GitHub account named `eademola`:

1. **Create account**: https://github.com/signup
   - Username: `eademola`

2. **Transfer repository**:
   - Go to repository **Settings** → **General**
   - Scroll to **Danger Zone**
   - Click **Transfer ownership**
   - Transfer to `eademola` account
   - Repository becomes: `eademola/eademola.github.io`

3. **GitHub Pages will automatically deploy to**: `https://eademola.github.io`

**Note:** You'll need access to both accounts to transfer.

---

## Comparison

| Option | URL | Cost | Setup Time | Professional? |
|--------|-----|------|------------|---------------|
| Current | `boyeshi.github.io/eademola.github.io` | Free | Done | ⭐⭐ |
| Custom Domain | `eademola.com` | $12/year | 30 min + DNS wait | ⭐⭐⭐⭐⭐ |
| Transfer Account | `eademola.github.io` | Free | 15 min | ⭐⭐⭐ |

---

## Recommendation for CPA Portfolio

For a **professional CPA portfolio**, I strongly recommend **Option 2: Custom Domain**

**Why?**
- ✅ Looks more professional on resume/business cards
- ✅ Easier to remember and share
- ✅ Shows you're serious about your career
- ✅ Can use professional email (with domain email service)
- ✅ Full control - domain is yours forever
- ✅ Can move hosting later if needed

**Examples:**
- `www.eademola.com` - Your portfolio
- `contact@eademola.com` - Professional email (optional)

---

## Custom Domain Setup Guide (Detailed)

### Using Namecheap (Example)

1. **Buy domain** at namecheap.com
2. **Login** → Dashboard → Manage domain
3. **Advanced DNS** tab
4. **Add New Record** (repeat for each):
   - A Record: `@` → `185.199.108.153`
   - A Record: `@` → `185.199.109.153`
   - A Record: `@` → `185.199.110.153`
   - A Record: `@` → `185.199.111.153`
   - CNAME Record: `www` → `boyeshi.github.io`
5. **Save all changes**
6. **GitHub**: Settings → Pages → Custom domain → Enter domain → Save
7. **Wait 24-48 hours** for DNS propagation
8. **Enable HTTPS** in GitHub Pages settings

---

## Troubleshooting

### Site shows 404 after adding custom domain
- Wait for DNS propagation (up to 48 hours)
- Check DNS with: https://dnschecker.org
- Verify A records point to correct IPs

### "DNS check unsuccessful" in GitHub Pages
- DNS hasn't propagated yet
- Wait a few more hours
- Verify CNAME record points to `boyeshi.github.io`

### HTTPS not available
- Must wait for DNS propagation first
- GitHub automatically provisions SSL certificate
- Can take 24-48 hours after DNS propagates

---

## Current Site Status

✅ **Your site is live and working at**:  
`https://boyeshi.github.io/eademola.github.io/`

All pages are functional:
- Home: `/index.html`
- Experience: `/experience.html`
- Case Highlights: `/case-highlights.html`
- CPA Path: `/cpa-path.html`
- Contact: `/contact.html`

You can use this URL immediately while setting up a custom domain.

---

## Quick Start: Custom Domain in 5 Minutes

1. Buy domain at Namecheap: ~5 minutes
2. Add DNS records (above): ~2 minutes
3. Configure GitHub Pages: ~1 minute
4. Wait for DNS (automated): 24-48 hours
5. Enable HTTPS: ~1 minute

**Total active time: ~10 minutes**  
**Total wait time: 24-48 hours**

---

## Need Help?

- GitHub Pages Docs: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- DNS Checker: https://dnschecker.org
- Namecheap Support: https://www.namecheap.com/support/

---

**Your portfolio is professional and ready. A custom domain is the final touch for maximum impact!** 🚀
