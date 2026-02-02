# StyleNest - HTML/CSS/JavaScript Version

This is the vanilla HTML, CSS, and JavaScript conversion of the StyleNest e-commerce website.

## 📁 File Structure

```
html-version/
├── index.html          # Home page
├── mens.html           # Men's collection page
├── womens.html         # Women's collection page
├── about.html          # About us page
├── contact.html        # Contact page
├── checkout.html       # Checkout page
├── order-success.html  # Order success page
├── terms-conditions.html    # Terms & Conditions policy
├── privacy-policy.html      # Privacy Policy
├── return-refund-policy.html # Return & Refund Policy
├── styles.css          # All CSS styles
├── main.js             # Main JavaScript (cart management, forms, etc.)
├── products.js         # Product data
└── README.md           # This file
```

## 🚀 Features

### Core Features
- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Dark theme (#121212 background, gold #FFD700 accents)
- ✅ Sticky navigation header
- ✅ Mobile menu with hamburger toggle
- ✅ Complete cart functionality with side drawer
- ✅ Real-time cart counter
- ✅ LocalStorage cart persistence
- ✅ Form validation (checkout & contact)
- ✅ Phone number validation for COD orders
- ✅ Product hover effects
- ✅ Smooth transitions and animations

### Pages Included
1. **Home Page** - Hero section, trending products, men's & women's collections, why choose us, promo banner, blog section
2. **Men's Collection** - Full catalog of men's products
3. **Women's Collection** - Full catalog of women's products
4. **About Us** - Company information
5. **Contact Us** - Contact form with business hours
6. **Checkout** - Shipping details form with COD payment
7. **Order Success** - Confirmation page after successful order
8. **Terms & Conditions** - Legal terms and conditions
9. **Privacy Policy** - Data privacy and protection
10. **Return & Refund Policy** - Return and refund procedures

## 🎨 Design Specifications

### Colors
- Primary Background: `#121212`
- Secondary Background: `#1a1a1a`
- Black: `#000000`
- Text Primary: `#ffffff`
- Text Secondary: `#9ca3af`
- Accent: `#FFD700` (Gold)
- Accent Hover: `#FFC700`
- Border: `#374151`

### Typography
- System fonts for fast loading
- Bold headings with proper hierarchy
- Responsive font sizes

## 💻 How to Use

### Option 1: Open Directly in Browser
1. Navigate to the `html-version` folder
2. Double-click `index.html` to open in your default browser
3. All pages and functionality will work immediately

### Option 2: Use a Local Server (Recommended)
For the best experience, use a local development server:

#### Using Python:
```bash
cd html-version
python -m http.server 8000
```
Then open: `http://localhost:8000`

#### Using Node.js (with http-server):
```bash
npm install -g http-server
cd html-version
http-server -p 8000
```
Then open: `http://localhost:8000`

#### Using VS Code Live Server:
1. Install "Live Server" extension
2. Right-click on `index.html`
3. Select "Open with Live Server"

## 🛒 Cart Functionality

### Features
- Add products to cart
- Update product quantities
- Remove products from cart
- Cart drawer slides in from the right
- Real-time cart total calculation
- Cart counter badge in header
- Persistent cart (saved in LocalStorage)
- Empty cart handling

### Usage
```javascript
// Add product to cart
cartManager.addToCart(product);

// Remove from cart
cartManager.removeFromCart(productId);

// Update quantity
cartManager.updateQuantity(productId, newQuantity);

// Clear cart
cartManager.clearCart();

// Open/close cart drawer
cartManager.openCartDrawer();
cartManager.closeCartDrawer();
```

## 📝 Forms

### Contact Form
- Name, email, phone, message fields
- Submits with alert confirmation
- Form resets after submission

### Checkout Form
- Comprehensive validation
- Required fields: name, email, phone, address, city, state, zip code
- Phone validation with international format support
- COD (Cash on Delivery) payment method
- Order summary with cart items
- Redirects to success page after submission

## 🎯 Navigation

### Desktop
- Horizontal navigation menu
- Sticky header
- Cart icon with counter badge

### Mobile
- Hamburger menu icon
- Slide-down mobile menu
- Touch-friendly buttons (48px minimum)

## 📦 Product Data

All product data is stored in `products.js`:
- `mensProducts` - Array of 6 men's products
- `womensProducts` - Array of 6 women's products
- `trendingProducts` - Featured products
- `blogPosts` - Blog articles

### Product Structure
```javascript
{
  id: "unique-id",
  name: "Product Name",
  price: 99.99,
  image: "https://...",
  category: "men" | "women"
}
```

## 🔧 Customization

### Adding New Products
Edit `products.js`:
```javascript
const newProduct = {
  id: "p7",
  name: "New Product",
  price: 149.99,
  image: "https://your-image-url.com",
  category: "men"
};
mensProducts.push(newProduct);
```

### Changing Colors
Edit CSS variables in `styles.css`:
```css
:root {
  --color-accent: #FFD700; /* Change to your color */
}
```

### Modifying Contact Information
Update in each HTML file's footer:
- Address: 40 E 7th St, New York, NY 10003, USA
- Phone: +1-728-009-8383
- Email: care@stylenest.in

## 🌐 Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📱 Responsive Breakpoints

- Mobile: < 640px
- Tablet: 640px - 1024px
- Desktop: > 1024px

## 🔒 Security Notes

- Form submissions are client-side only (mock functionality)
- No actual payment processing
- LocalStorage used for cart (client-side only)
- For production, integrate with a backend API

## 🚀 Production Deployment

### To deploy this site:

1. **Static Hosting** (Recommended):
   - Netlify: Drag & drop the `html-version` folder
   - Vercel: Import the folder as a static site
   - GitHub Pages: Push to repository and enable Pages
   - AWS S3 + CloudFront
   - Firebase Hosting

2. **Traditional Hosting**:
   - Upload all files via FTP/SFTP
   - Ensure proper file permissions
   - Configure web server (Apache/Nginx)

### Performance Optimization:
- Images are already optimized (loaded from Unsplash CDN)
- CSS is in a single file for faster loading
- Minimal JavaScript with no external dependencies
- Consider adding:
  - Image lazy loading
  - CSS/JS minification
  - Gzip compression
  - CDN for static assets

## 📞 Support

For questions or issues with this HTML version:
- Check browser console for JavaScript errors
- Ensure all files are in the same directory
- Verify file names match exactly (case-sensitive)
- Test in multiple browsers

## ✨ Future Enhancements

Possible additions:
- Product search functionality
- Product filtering by category/price
- User authentication
- Wishlist feature
- Product reviews
- Backend integration
- Real payment gateway
- Email notifications
- Order tracking

## 📄 License

This is a demonstration project for StyleNest e-commerce platform.

---

**StyleNest** - Your destination for premium fashion © 2026