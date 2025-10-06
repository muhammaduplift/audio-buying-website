# Custom Domain Setup Guide

## Step 1: Purchase a Domain
1. Buy a domain from registrars like:
   - Namecheap
   - GoDaddy
   - Google Domains
   - Cloudflare

## Step 2: Configure DNS Records

### Option A: Using Apex Domain (example.com)
Add these **A records** to your DNS settings:
```
Type: A
Name: @ (or leave blank)
Value: 185.199.108.153

Type: A
Name: @ (or leave blank)
Value: 185.199.109.153

Type: A
Name: @ (or leave blank)
Value: 185.199.110.153

Type: A
Name: @ (or leave blank)
Value: 185.199.111.153
```

### Option B: Using Subdomain (www.example.com)
Add this **CNAME record**:
```
Type: CNAME
Name: www
Value: muhammaduplift.github.io
```

### Recommended: Use Both
- Add all 4 A records for apex domain
- Add 1 CNAME record for www subdomain

## Step 3: Add CNAME File to Repository

In your repository, create a file named `CNAME` (no extension) with your domain:

```bash
cd "C:\Alt Agents\audio-buying-website"
echo yourdomain.com > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

Replace `yourdomain.com` with your actual domain.

## Step 4: Configure GitHub Pages

1. Go to: https://github.com/muhammaduplift/audio-buying-website/settings/pages
2. Under "Custom domain", enter your domain (e.g., `yourdomain.com`)
3. Click **Save**
4. Wait for DNS check to complete (usually 10-30 minutes)
5. Once verified, check **Enforce HTTPS**

## Step 5: Wait for DNS Propagation

DNS changes can take:
- **Minimum:** 10-30 minutes
- **Maximum:** 24-48 hours

Check propagation status at: https://dnschecker.org

## Verification

Once complete, your site will be accessible at:
- `https://yourdomain.com`
- `https://www.yourdomain.com` (if you added CNAME record)

## Troubleshooting

### DNS Check Failing
- Wait longer (up to 24 hours)
- Verify DNS records are correct
- Clear browser cache

### Certificate Issues
- Make sure "Enforce HTTPS" is checked
- Wait 24 hours for certificate provisioning
- Try unchecking and re-checking "Enforce HTTPS"

### Domain Not Working
- Verify CNAME file exists in repository
- Check DNS records at your registrar
- Use `dig yourdomain.com` to verify DNS resolution

## Example: Namecheap Configuration

1. Login to Namecheap
2. Go to Domain List → Manage
3. Click "Advanced DNS"
4. Add records:
   - 4 A Records pointing to GitHub IPs
   - 1 CNAME Record: `www` → `muhammaduplift.github.io`
5. Save changes

## Current GitHub Pages URL
https://muhammaduplift.github.io/audio-buying-website/
