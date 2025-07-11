# XAMPP Quick Setup Guide

## 🚀 Quick Fix for Backend Connection

### Step 1: Start XAMPP
1. Open **XAMPP Control Panel** (Run as Administrator if needed)
2. Click **Start** next to **Apache**
3. Wait until status shows **Running** (green background)

### Step 2: Copy Backend Files
Copy the entire `backend` folder to XAMPP:

```
Source: [Your Project]/backend/
Target: C:\xampp\htdocs\project\backend\
```

**Required files:**
- `C:\xampp\htdocs\project\backend\process.php`
- `C:\xampp\htdocs\project\backend\puppeteer_cart_search.js`
- `C:\xampp\htdocs\project\backend\README.md`

### Step 3: Test Connection
Open browser and go to: `http://localhost/project/backend/process.php`

**Expected result:** PHP error message saying "No URL provided" (this is normal!)

**If you see:**
- ❌ "404 Not Found" → Files are in wrong location
- ❌ "This site can't be reached" → Apache is not running
- ✅ PHP error message → Everything is working!

### Step 4: Run Analysis
Go back to your application and try running an analysis.

## 🔧 Common Issues

### Port 80 Already in Use
If Apache won't start:
1. Open XAMPP Control Panel
2. Click **Config** next to Apache
3. Select **httpd.conf**
4. Change `Listen 80` to `Listen 8080`
5. Change `ServerName localhost:80` to `ServerName localhost:8080`
6. Save and restart Apache
7. Test with: `http://localhost:8080/project/backend/process.php`

### Permission Issues
If you get permission errors:
1. Run XAMPP Control Panel as Administrator
2. Make sure Windows Firewall allows Apache
3. Check folder permissions for `C:\xampp\htdocs\`

### Alternative Locations
If the standard path doesn't work, try copying files to:
- `C:\xampp\htdocs\backend\` (without project folder)
- Test with: `http://localhost/backend/process.php`

## 📞 Need Help?
Check these files for detailed troubleshooting:
- `XAMPP_TROUBLESHOOTING.md`
- `STEP_BY_STEP_FIX.md`
- `DIAGNOSTIC_CHECKLIST.md`