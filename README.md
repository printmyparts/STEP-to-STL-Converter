# STEP to STL Converter - Vercel Deployment

Free online STEP to STL converter that runs entirely in the browser using OpenCascade.js.

## 🚀 Deploy to Vercel

### Method 1: GitHub (Recommended)
1. Create a new GitHub repository
2. Upload these files to the repository
3. Go to [vercel.com](https://vercel.com)
4. Click "New Project"
5. Import your GitHub repository
6. Click "Deploy"
7. Done! Your converter will be live at `your-project.vercel.app`

### Method 2: Vercel CLI
```bash
npm i -g vercel
cd vercel-converter
vercel
```

### Method 3: Drag & Drop
1. Go to [vercel.com](https://vercel.com)
2. Drag the `vercel-converter` folder onto the Vercel dashboard
3. Done!

## 📋 Files Included

- `index.html` - Main converter application
- `vercel.json` - Vercel configuration for proper headers
- `README.md` - This file

## 🔧 Custom Domain (Optional)

1. Go to your Vercel project settings
2. Click "Domains"
3. Add your custom domain (e.g., `converter.yoursite.com`)
4. Update your DNS records as instructed
5. Done! SSL certificate is automatic

## 🌐 Embed in WordPress

Once deployed, add this to your WordPress page using an HTML widget:

```html
<iframe 
  src="https://your-project.vercel.app" 
  width="100%" 
  height="900px" 
  frameborder="0"
  style="border: none; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</iframe>
```

Replace `your-project.vercel.app` with your actual Vercel URL.

## ✨ Features

- ✅ 100% client-side conversion (files never uploaded)
- ✅ Supports .step and .stp files
- ✅ Three quality presets with file size limits
- ✅ Drag & drop interface
- ✅ Mobile responsive
- ✅ No backend required
- ✅ Free hosting on Vercel

## 🔒 Privacy

All file processing happens locally in the user's browser. No files are ever uploaded to any server.

## 📊 Technical Details

- **Frontend**: Vanilla JavaScript
- **CAD Engine**: OpenCascade.js v1.1.1 (from UNPKG CDN)
- **WASM Size**: ~66MB (cached after first load)
- **Hosting**: Vercel (free tier)

## 🛠️ Customization

### Change File Size Limits
Edit the `data-max-size` attributes in `index.html`:
```html
<input ... data-max-size="50">  <!-- Low: 50 MB -->
<input ... data-max-size="20">  <!-- Medium: 20 MB -->
<input ... data-max-size="10">  <!-- High: 10 MB -->
```

### Change Colors
Find and replace these hex codes in the CSS:
- `#667eea` - Primary purple
- `#764ba2` - Secondary purple

### Change Quality Values
Edit the `value` attributes:
```html
<input ... value="0.5">   <!-- Low: 0.5 -->
<input ... value="0.1">   <!-- Medium: 0.1 -->
<input ... value="0.01">  <!-- High: 0.01 -->
```
Lower values = higher quality (more triangles in mesh)

## 📞 Support

For issues or questions, check the [OpenCascade.js documentation](https://ocjs.org/).
