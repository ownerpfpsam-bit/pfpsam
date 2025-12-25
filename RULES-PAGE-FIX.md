# Fix: Rules Page Template Not Showing

## Problem
The `page.giveaway-rules.json` template exists but isn't showing on your site.

## Solution: Assign Template to Page in Shopify Admin

### Step 1: Find Your Rules Page
1. Go to **Online Store** → **Pages** in your Shopify admin
2. Find the page that should display the giveaway rules (or create it if it doesn't exist)
3. Click on the page to edit it

### Step 2: Assign the Template
1. In the page editor, scroll down to the **Search engine listing** section (or look for **Template** section)
2. Find the **Template** dropdown/selector
3. Select **`giveaway-rules`** from the template options
   - If you don't see it, make sure the template file `page.giveaway-rules.json` is saved in your theme
4. Click **Save**

### Step 3: Verify the Page Handle
1. In the same page editor, check the **Page handle** field
2. It should be something like `giveaway-rules` or `official-rules` 
3. The URL will be: `yourstore.com/pages/[handle]`
4. Make sure it matches what you're linking to

### Step 4: Upload Template File to Shopify (REQUIRED)
**This is the most important step!** The template file needs to be uploaded to Shopify:

1. Go to **Online Store** → **Themes**
2. Click **Actions** → **Edit code** on your current theme (pfpsam/main)
3. In the left sidebar, click on **Templates**
4. Look for `page.giveaway-rules.json` in the list
   - **If it's NOT there:** Click **Add a new template** → Select **Page** → Name it `giveaway-rules` → Click **Create template**
   - **If it IS there:** Click on it to open it
5. Copy the entire contents of the template file from your local `templates/page.giveaway-rules.json` file
6. Paste it into the Shopify code editor (replace any existing content)
7. Click **Save** in the top right
8. Go back to your page editor and refresh - the template should now appear in the dropdown!

### Step 5: Clear Cache
1. After saving, try accessing the page in an incognito/private browser window
2. Or clear your browser cache

## Quick Links
- **Pages**: `https://pfp-sam.myshopify.com/admin/pages`
- **Theme Editor**: `https://pfp-sam.myshopify.com/admin/themes/current/editor`
- **Theme Code Editor**: `https://pfp-sam.myshopify.com/admin/themes/current/editor?template=page.giveaway-rules`

## Common Issues

**Template not in dropdown:**
- Make sure the file is named exactly `page.giveaway-rules.json` (not `.liquid`)
- The file must be in the `templates/` folder
- Try refreshing the admin page

**Page shows default template:**
- Double-check the template is selected in page settings
- Make sure you're viewing the correct page (check the URL/handle)

**Template shows but content is wrong:**
- The template file might need to be synced from your local files
- Check if changes were made in the theme editor that overwrote the template

