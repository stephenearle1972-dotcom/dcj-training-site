# DCJ Training Website - Publishing Guide for 1Grid

## 📋 What You Need

1. **Your website files** (included in this package)
2. **1Grid hosting account** (you already have this)
3. **Domain**: www.dcjtraining.co.za (already owned)
4. **Your photos** (renamed as shown below)
5. **FTP client** (FileZilla - free download)

---

## 📁 File Structure Setup

Create this folder structure on your computer first:

```
dcjtraining-website/
├── index.html (the main website file)
├── images/
│   ├── logo.jpg (your DCJ logo)
│   ├── students-competition.jpg (photo 1)
│   ├── team-celebration.jpg (photo 2)
│   └── student-building.jpg (photo 3)
```

---

## 🖼️ Preparing Your Images

1. **Rename your uploaded photos**:
   - `dcj_logo.jpg` → `logo.jpg`
   - `WhatsApp_Image_2026-01-29_at_17_22_48.jpeg` → `students-competition.jpg`
   - `WhatsApp_Image_2026-01-29_at_17_23_06.jpeg` → `team-celebration.jpg`
   - `WhatsApp_Image_2026-01-29_at_17_23_23.jpeg` → `student-building.jpg`

2. **Optimize images** (recommended):
   - Use a free tool like TinyPNG (tinypng.com)
   - Resize large images to max 1920px width
   - This makes your site load faster

---

## 🚀 Publishing to 1Grid - Step by Step

### Option 1: Using 1Grid File Manager (Easiest)

1. **Log into your 1Grid account**:
   - Go to https://www.1grid.com/
   - Click "Login" (top right)
   - Enter your credentials

2. **Access cPanel**:
   - Once logged in, look for "cPanel" or "Control Panel"
   - Click to open your hosting control panel

3. **Open File Manager**:
   - In cPanel, find "File Manager" (usually under "Files" section)
   - Click to open

4. **Navigate to public_html**:
   - Click on the `public_html` folder
   - This is where your website files go

5. **Upload index.html**:
   - Click "Upload" button at the top
   - Select your `index.html` file
   - Wait for upload to complete

6. **Create images folder**:
   - Click "New Folder" button
   - Name it: `images` (lowercase, no spaces)
   - Press Enter/Create

7. **Upload images**:
   - Click on the `images` folder to open it
   - Click "Upload" button
   - Select all 4 image files (logo and 3 photos)
   - Wait for upload to complete

8. **Verify**:
   - Go to www.dcjtraining.co.za in your browser
   - Your site should be live!

---

### Option 2: Using FTP (FileZilla) - More Control

1. **Download FileZilla** (if you don't have it):
   - Go to: https://filezilla-project.org/
   - Download FileZilla Client (it's free)
   - Install it

2. **Get your FTP credentials from 1Grid**:
   - Log into 1Grid account
   - Go to cPanel
   - Look for "FTP Accounts" section
   - Note down:
     - Host: usually `ftp.dcjtraining.co.za` or your server IP
     - Username: (provided by 1Grid)
     - Password: (provided by 1Grid)
     - Port: 21

3. **Connect with FileZilla**:
   - Open FileZilla
   - Enter your details at the top:
     - Host: `ftp.dcjtraining.co.za`
     - Username: (your FTP username)
     - Password: (your FTP password)
     - Port: 21
   - Click "Quickconnect"

4. **Upload files**:
   - On the right side (Remote site), navigate to `/public_html`
   - On the left side (Local site), navigate to your website folder
   - Drag and drop:
     - `index.html` to the right side
     - The entire `images` folder to the right side
   - Wait for upload to complete

5. **Check permissions** (if images don't show):
   - Right-click on `images` folder
   - Select "File Permissions"
   - Set to: 755
   - Check "Recurse into subdirectories"
   - Click OK

---

## 🔧 Configuring Your Domain

If www.dcjtraining.co.za doesn't point to your 1Grid hosting yet:

1. **Log into your domain registrar** (where you bought the domain)
2. **Find DNS settings** or "Nameservers"
3. **Update nameservers** to 1Grid's nameservers:
   - 1Grid will have provided these (usually in your welcome email)
   - They look like: `ns1.1grid.com` and `ns2.1grid.com`
4. **Wait 24-48 hours** for DNS propagation

**OR**

If you want faster setup:
1. In cPanel, go to "Domains" or "Addon Domains"
2. Add: `dcjtraining.co.za`
3. Point document root to: `/public_html`

---

## ✅ After Publishing Checklist

- [ ] Website loads at www.dcjtraining.co.za
- [ ] Logo shows in header
- [ ] All 3 photos show in hero section
- [ ] Registration form opens when clicking buttons
- [ ] All navigation links work
- [ ] Site works on mobile (test on your phone)
- [ ] Contact information is correct

---

## 🔄 Making Updates Later

To update your website:

1. **Edit the index.html file** on your computer
2. **Re-upload** to 1Grid using File Manager or FileZilla
3. **Replace the old file** when prompted
4. **Clear your browser cache** (Ctrl+F5) to see changes

---

## 📧 Setting Up Email Form Backend

The registration form currently shows a success message but doesn't send emails. To make it actually send:

### Option 1: Use Formspree (Easiest - Free)

1. Go to https://formspree.io/
2. Sign up for free account
3. Create a new form
4. Copy the form endpoint URL they give you
5. Contact me to update the form with this URL

### Option 2: Use EmailJS (Free)

1. Go to https://www.emailjs.com/
2. Sign up for free account
3. Set up email service
4. Get your service ID, template ID, and public key
5. Contact me to integrate this

### Option 3: Custom PHP Script (Requires PHP on server)

1. 1Grid supports PHP
2. I can create a simple PHP email handler
3. Just provide the email address to receive registrations

---

## 💳 Adding Online Payment (Next Steps)

To accept online payments for registrations:

### Recommended for South Africa:

**1. PayFast** (Most popular in SA)
- Website: https://www.payfast.co.za/
- Monthly fee: R0 (free for under 50 transactions)
- Transaction fee: 2.9% + R2
- Easy integration
- Accepts credit cards, EFT, instant EFT

**2. Yoco** (Great for small businesses)
- Website: https://www.yoco.com/
- Transaction fee: 2.95%
- No monthly fees
- Simple setup

**3. PayGate** (Enterprise option)
- More features
- Higher fees
- Better for larger operations

### Integration Steps:
1. Sign up with chosen payment provider
2. Get API credentials
3. I can integrate payment buttons into the registration form
4. Test payments
5. Go live!

---

## 📱 Important Contact Info to Update

Currently the website has placeholder information. Update these:

**In the HTML file, find and replace:**

1. **Phone number**: `+27 12 345 6789` → Your real number
2. **Email**: `info@dcjtraining.co.za` → Your real email
3. **Facebook link**: Already correct in the code

**To edit:**
1. Open `index.html` in Notepad or any text editor
2. Press Ctrl+F to find text
3. Replace with your real information
4. Save file
5. Re-upload to 1Grid

---

## 🆘 Troubleshooting

### Images not showing?
- Check file names match exactly (case-sensitive)
- Verify images are in the `images` folder
- Check file permissions (should be 644 for files, 755 for folders)
- Clear browser cache (Ctrl+F5)

### Website not loading?
- Check domain is pointing to 1Grid nameservers
- Wait 24-48 hours for DNS propagation
- Verify index.html is in `/public_html` folder
- Contact 1Grid support if needed

### Mobile site looks wrong?
- This shouldn't happen - the site is fully responsive
- Try clearing browser cache
- Test in different browsers

### Form not submitting?
- The form shows a success message but needs backend setup
- Follow "Setting Up Email Form Backend" section above

---

## 📞 1Grid Support Contact

If you need help with hosting:
- **Website**: https://www.1grid.com/
- **Support**: Look for "Support" or "Contact" in your account
- **Phone**: Check your 1Grid welcome email for support number

---

## 🎯 Next Steps After Launch

1. **Test everything** thoroughly
2. **Set up email backend** for registrations
3. **Add online payment** integration
4. **Promote your website**:
   - Update Facebook page with website link
   - Share on social media
   - Print on flyers/business cards
5. **Monitor registrations** and respond quickly

---

## 📊 Recommended Additional Features

Once your site is live, consider:

1. **Google Analytics** - Track visitor numbers (free)
2. **Facebook Pixel** - Track conversions from ads
3. **WhatsApp Chat Widget** - Quick parent contact
4. **Testimonial Section** - Add parent reviews
5. **Photo Gallery Page** - More competition photos
6. **Blog Section** - Share robotics news

I can help add any of these features!

---

## ✨ Your Website Features

Your new website includes:

✅ Full registration form with validation
✅ 3-tier pricing structure with detailed features
✅ Monthly and term payment options
✅ Responsive design (works on all devices)
✅ LEGO-themed animations and design
✅ Contact information section
✅ Social media integration
✅ Professional layout
✅ Fast loading
✅ SEO-friendly structure

---

## 💡 Tips for Success

1. **Update content regularly** - Keep pricing and schedules current
2. **Respond quickly** to registrations (within 24 hours)
3. **Take more photos** - Add to the gallery as you grow
4. **Collect testimonials** - Ask happy parents for reviews
5. **Track registrations** - Use a spreadsheet to manage students
6. **Promote on Facebook** - Share posts linking to your website

---

## 🤝 Need More Help?

If you need assistance with:
- Uploading files
- Setting up email backend
- Integrating payments
- Making design changes
- Adding new features
- Technical issues

Just ask! I'm here to help make your website successful.

---

**Good luck with DCJ Training! 🚀🤖**

Your website is ready to bring in students and grow your robotics program!