# 🚀 Vercel Environment Variables - COPY & PASTE

## Step 1: Go to Vercel Dashboard
1. Visit https://vercel.com/dashboard
2. Select your project: **new-marian-dental-clinic**
3. Click **Settings** → **Environment Variables**

## Step 2: Add These 4 Variables

Copy and paste each one exactly as shown:

---

### Variable 1
**Name:** `SUPABASE_URL`  
**Value:**
```
https://agnfndxmlmwrhhnjsdzb.supabase.co
```
**Environments:** ✅ Production ✅ Preview ✅ Development

---

### Variable 2
**Name:** `SUPABASE_ANON_KEY`  
**Value:**
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImFnbmZuZHhtbG13cmhobmpzZHpiIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzA4MzY4MjksImV4cCI6MjA4NjQxMjgyOX0.c9rEEtqpraTXFZeIJCEKhY947NjRyFxk5tyOwlqwNOE
```
**Environments:** ✅ Production ✅ Preview ✅ Development

---

### Variable 3
**Name:** `RESEND_API_KEY`  
**Value:**
```
re_iRui48k8_NJGNhAYd5aMq3G6Zqpuq9hmC
```
**Environments:** ✅ Production ✅ Preview ✅ Development

---

### Variable 4
**Name:** `CLINIC_EMAIL`  
**Value:**
```
doctor@mariandental.com
```
**Environments:** ✅ Production ✅ Preview ✅ Development

---

## Step 3: Redeploy
1. Go to **Deployments** tab
2. Click the **"..."** menu on the latest deployment
3. Click **"Redeploy"**
4. Wait ~2 minutes for completion

## ✅ Done!
Your backend API will now work on Vercel.

---

## 🧪 Quick Test (After Redeploy)

Visit your live site and open browser console (F12), then paste:

```javascript
fetch('https://your-site.vercel.app/api/appointments', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    name: 'Test Patient',
    phone: '9876543210',
    service: 'General Checkup',
    date: '2024-02-15',
    time: '10:00 AM'
  })
})
.then(r => r.json())
.then(data => console.log('✅ Success:', data))
.catch(err => console.error('❌ Error:', err));
```

If you see "✅ Success", your backend is working!
