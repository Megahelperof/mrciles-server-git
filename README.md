
# 🤖 Mrciles Backend Discord Bot System

Welcome to your custom backend system! This Discord bot provides two specialized services for managing your e-commerce operations through Discord commands.

## 🌟 Bot Capabilities

### 1. **Firebase Bot**
- **Product Catalog Management** - Add/remove products via Discord commands
- **Image Processing** - Handles product image uploads and storage
- **Category Organization** - Organizes products into categories/subcategories
- **Bulk Operations** - Add/remove multiple products at once
- **Firebase Integration** - Direct connection to your Firebase database

### 2. **Scraper Bot**
- **Price Monitoring** - Tracks prices across multiple websites
- **Stock Availability** - Checks real-time product availability
- **Price Comparison** - Finds products closest to target prices
- **Bulk Operations** - Add/remove multiple products at once
- **Error Reporting** - Identifies products with monitoring issues

## 📋 Deployment Instructions

### Step 1: Prepare Your Environment
1. Create a new repository for your backend code
2. Add these files to your repository:
   - `index.js` (the main bot file)
   - `package.json` (with required dependencies)
   - `render.yaml` (deployment configuration)


### Step 2: Required Environment Variables

#### For Firebase Bot:
```env
BOT_TYPE=FIREBASE_BOT
DISCORD_BOT_TOKEN=your_bot_token
FIREBASE_SERVICE_ACCOUNT=base64_encoded_service_account
ADMIN_ROLE_ID=your_admin_role_id
```

#### For Scraper Bot:
```env
BOT_TYPE=SCRAPER_BOT
DISCORD_BOT_TOKEN=your_bot_token
DISCORD_CLIENT_ID=your_client_id
DISCORD_GUILD_ID=your_server_id
```

### Step 3: Generate Firebase Credentials
1. Generate your Firebase service account JSON file
2. Encode it in Base64:
   ```bash
   base64 -i serviceAccount.json > encoded.txt
   ```
3. Use the content of `encoded.txt` as `FIREBASE_SERVICE_ACCOUNT` value

### Step 4: Deploy to Render
1. Connect your GitHub repository to Render
2. Select the repository containing your bot code
3. Render will automatically detect `render.yaml`
4. Confirm deployment

## 🎯 Bot Command Reference

### Firebase Bot Commands:
```
/add - Add new product with image
/remove [id] - Remove product by ID
/bulk-add - Add multiple products via ZIP
/help - Show available commands
```

### Scraper Bot Commands:
```
/products - Check product status
/invalid - Show products with errors
/prices [target] - Find products near target price
/addlink [name] [url] - Add new product to monitor
/removelink [id] - Remove product by ID
/bulklink - Bulk import from JSON
/bulkremovelink - Remove multiple products
```

## 🔧 Technical Requirements
- Node.js v18+
- Render Web Service
- Firebase Project (for Firebase Bot)
- Discord Developer Application

## ⚠️ Important Notes
1. Keep all environment variables SECURE
2. The Firebase Bot requires admin privileges
3. Use different bots for different environments
4. Contact cbam on Discord for Firebase setup assistance
5. The system automatically cleans up old data every 5 minutes

## 📞 Support & Maintenance
For assistance with:
- Firebase configuration
- Discord bot permissions
- Deployment issues
- Custom feature requests

Contact: **cbam on Discord**

---

*This backend system has been custom-built for Mrciles with specialized e-commerce functionality. Thank you for choosing our services!*
```
