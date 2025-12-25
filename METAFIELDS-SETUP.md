# Quick Setup Guide: Product Metafields

## ⚠️ Important: You need PRODUCT METAFIELDS, not Metaobjects

You're currently on the Metaobjects page. We need to create **Product Metafields** instead.

## Steps to Create Product Metafields

### Step 1: Navigate to Product Metafields

1. In your Shopify Admin, go to: **Settings** → **Custom data**
2. Click on **Products** (not "Metaobjects")
3. You should see a page titled "Product metafields" with an "Add definition" button

### Step 2: Create the "Entries" Metafield

1. Click **Add definition**
2. Fill in:
   - **Name**: `Entries`
   - **Namespace and key**: 
     - Namespace: Type `custom` (or select from dropdown if available)
     - Key: Type `entries`
   - **Description**: `Number of entries for this product (e.g., 8,880)`
   - **Type**: Select **Single line text** (or **Integer** if you want numbers only)
   - **Validation**: Leave empty or add pattern if needed
3. Click **Save**

### Step 3: Create the "Badge Multiplier" Metafield

1. Still on the **Products** metafields page, click **Add definition** again
2. Fill in:
   - **Name**: `Badge Multiplier`
   - **Namespace and key**: 
     - Namespace: Type `custom` (same as before)
     - Key: Type `badge_multiplier`
   - **Description**: `Multiplier value for the badge (e.g., 120)`
   - **Type**: Select **Single line text** (or **Integer**)
   - **Validation**: Leave empty
3. Click **Save**

### Step 4: Add Values to Your Products

1. Go to **Products** in your Shopify admin
2. Click on any product
3. Scroll down to find the **Metafields** section
4. You should see:
   - **Entries**: Enter a value like `8,880` or `8880`
   - **Badge Multiplier**: Enter a value like `120`
5. Click **Save product**

### Step 5: Verify in Theme Editor

1. Go to **Online Store** → **Themes**
2. Click **Customize** on your active theme
3. Navigate to a product page
4. Make sure the **Product entries & badge** block is added after the Price block
5. The metafields should display automatically!

## Quick Links

- **Product Metafields**: `https://pfp-sam.myshopify.com/admin/settings/metafields/products`
- **Products**: `https://pfp-sam.myshopify.com/admin/products`
- **Theme Editor**: `https://pfp-sam.myshopify.com/admin/themes/current/editor`

## What the Code Expects

Our code looks for:
- `product.metafields.custom.entries` - The entries count
- `product.metafields.custom.badge_multiplier` - The badge multiplier

Make sure the namespace is `custom` and the keys are exactly `entries` and `badge_multiplier`.

