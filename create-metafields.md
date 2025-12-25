# Creating Product Metafields for Entries & Badge

This guide will help you create the required metafields in your Shopify store.

## Required Metafields

1. **Entries Count** (`custom.entries`)
   - Namespace: `custom`
   - Key: `entries`
   - Type: Single line text or Integer
   - Description: Number of entries for the product (e.g., "8,880" or "8880")

2. **Badge Multiplier** (`custom.badge_multiplier`)
   - Namespace: `custom`
   - Key: `badge_multiplier`
   - Type: Single line text or Integer
   - Description: Multiplier value for the badge (e.g., "120" or "120x")

## Method 1: Shopify Admin (Recommended)

### Step 1: Create the Entries Metafield

1. Go to your Shopify Admin: `https://pfp-sam.myshopify.com/admin`
2. Navigate to **Settings** → **Custom data** → **Products**
3. Click **Add definition**
4. Fill in the form:
   - **Name**: `Entries`
   - **Namespace and key**: `custom.entries` (type "custom" in namespace, "entries" in key)
   - **Description**: `Number of entries for this product`
   - **Type**: Select **Single line text** (or **Integer** if you prefer numbers)
   - **Validation**: Optional - you can add a pattern if needed
5. Click **Save**

### Step 2: Create the Badge Multiplier Metafield

1. Still in **Settings** → **Custom data** → **Products**
2. Click **Add definition** again
3. Fill in the form:
   - **Name**: `Badge Multiplier`
   - **Namespace and key**: `custom.badge_multiplier` (type "custom" in namespace, "badge_multiplier" in key)
   - **Description**: `Multiplier value displayed in the badge`
   - **Type**: Select **Single line text** (or **Integer** if you prefer numbers)
   - **Validation**: Optional
4. Click **Save**

### Step 3: Add Values to Products

1. Go to **Products** in your Shopify admin
2. Select a product you want to add metafield values to
3. Scroll down to find the **Metafields** section
4. You should see:
   - **Entries**: Enter the number (e.g., "8,880" or "8880")
   - **Badge Multiplier**: Enter the multiplier (e.g., "120")
5. Click **Save**

Repeat for each product.

## Method 2: Using Shopify GraphQL Admin API

If you prefer to use the API, you can use the Shopify GraphQL Admin API to create metafield definitions programmatically.

## Verification

After creating the metafields and adding values to products:

1. Visit a product page on your store
2. The entries count and badge should display automatically if:
   - The metafields are created correctly
   - Values are added to the product
   - The "Product entries & badge" block is added to your product template

## Troubleshooting

- **Metafields not showing**: Make sure you're using the correct namespace (`custom`) and keys (`entries`, `badge_multiplier`)
- **Values not displaying**: Check that you've added values to the product in the Metafields section
- **Block not appearing**: Make sure you've added the "Product entries & badge" block in the theme editor

