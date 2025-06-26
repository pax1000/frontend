# Egyptian Tech Price Finder

A modern web application that helps users find the best tech product prices across Egypt's top electronics stores. The application provides real-time price comparison from multiple retailers with an elegant, user-friendly interface.

## 🌟 Features

### Core Functionality
- **Multi-Store Search**: Searches across major Egyptian tech retailers:
  - Sigma Computer
  - ElNekhely
  - ElBadr Group
  - Compumarts

- **Real-Time Results**: Live scraping of product data with loading indicators
- **Trending Products**: Displays popular search terms based on user activity
- **Advanced Filtering**: Filter results by store, price range, and sorting options

### User Interface
- **Modern Design**: Dark theme with glassmorphism effects and smooth animations
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Interactive Elements**: Hover effects, smooth transitions, and intuitive controls
- **Real-Time Status**: Live scraping status indicators for each store

## 🚀 Getting Started

### Prerequisites
- A backend API server running on `http://127.0.0.1:8000`
- Modern web browser with JavaScript enabled

### Installation

1. **Clone or download the project files**:
   ```
   index.html
   style.css
   script.js
   ```

2. **Set up the backend API** (not included in this frontend):
   - The application expects endpoints at `http://127.0.0.1:8000`
   - Required endpoints:
     - `GET /search/{query}` - Search for products
     - `GET /trending` - Get trending searches

3. **Open the application**:
   ```bash
   # Simply open index.html in your web browser
   # Or serve it using a local server
   python -m http.server 8080
   # Then visit http://localhost:8080
   ```

## 🔧 API Requirements

The frontend expects a backend API with the following endpoints:

### Search Endpoint
```
GET /search/{query}
```
**Response Format**:
```json
[
  {
    "id": "unique-product-id",
    "title": "Product Name",
    "price": 15000,
    "store": "sigma",
    "link": "https://store-url.com/product"
  }
]
```

### Trending Endpoint
```
GET /trending
```
**Response Format**:
```json
[
  {
    "product_name": "RTX 4080",
    "search_count": 150
  }
]
```

## 🎨 Design Features

### Visual Elements
- **Dark Theme**: Professional dark color scheme with blue accents
- **Glassmorphism**: Semi-transparent elements with backdrop blur effects
- **Gradient Backgrounds**: Smooth color transitions throughout the interface
- **Micro-Animations**: Subtle hover effects and loading animations

### Color Palette
- **Primary**: Blue gradient (#4c6ef5 to #7c3aed)
- **Background**: Dark blue gradient (#1a1a2e to #0f3460)
- **Surface**: Semi-transparent dark panels (rgba(30, 30, 46, 0.95))
- **Text**: Light gray (#e0e0e0) with various opacity levels
- **Accent**: Green for prices (#4ade80), Cyan for interactive elements (#7dd3fc)

## 🛠️ Technical Details

### File Structure
```
egyptian-tech-finder/
├── index.html          # Main HTML structure
├── style.css           # Styling and animations
└── script.js           # JavaScript functionality
```

### Key Components

#### Search Functionality
- Real-time search with Enter key support
- Loading states with store-specific status indicators
- Error handling for failed requests

#### Filtering & Sorting
- **Sort Options**: Name (A-Z), Price (Low to High), Price (High to Low)
- **Store Filter**: Filter by specific retailer
- **Price Range**: Set minimum and maximum price filters
- **Reset Filters**: One-click filter reset

#### Product Display
- Grid layout with responsive cards
- Product information: title, price, store badge
- Direct links to store product pages
- Copy link functionality

### Browser Compatibility
- Modern browsers (Chrome 60+, Firefox 55+, Safari 12+, Edge 79+)
- ES6+ JavaScript features used
- CSS Grid and Flexbox for layouts
- CSS Custom Properties for theming

## 📱 Responsive Design

The application is fully responsive with breakpoints for:
- **Desktop**: Full-width layout with multi-column grid
- **Tablet**: Adapted spacing and column layout
- **Mobile**: Single-column layout with stacked elements

## 🎯 Usage

1. **Search**: Enter a product name in the search bar (e.g., "RTX 4080", "iPhone 15")
2. **Browse Trending**: Click on trending tags for popular searches
3. **Filter Results**: Use the filtering options to narrow down results
4. **Compare Prices**: View prices across different stores
5. **Visit Store**: Click "View Product" to go to the retailer's website

## 🔧 Customization

### Adding New Stores
To add support for additional stores:

1. Update the store filter options in `index.html`:
```html
<option value="new-store">New Store Name</option>
```

2. Add store status indicator in the loading section:
```html
<div class="status-item" id="status-new-store">
    <i class="fas fa-clock"></i>
    <span>New Store Name</span>
</div>
```

3. Update the backend API to include the new store in search results

### Styling Modifications
- Colors can be customized in the CSS custom properties
- Animations can be adjusted by modifying transition durations
- Layout can be modified using CSS Grid and Flexbox properties

## 🚀 Performance Optimizations

- **CSS**: Optimized animations using `transform` and `opacity`
- **JavaScript**: Event delegation and debounced input handling
- **Images**: Font icons used instead of image files
- **Loading**: Progressive loading states for better UX

## 🐛 Known Issues

- Backend API must be running on localhost:8000
- CORS may need to be configured for cross-origin requests
- Search requires exact product name matching (depends on backend implementation)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## 📞 Support

For support or questions about this application, please open an issue in the repository or contact the development team.

---

*Built for the Egyptian tech community to find the best deals across local retailers* 🇪🇬