# Guide360 — AI-Powered Travel Assistant

A modern, responsive travel planning web application that helps users discover destinations, book accommodations, find dining options, and create AI-generated itineraries with multi-modal routing.

---

## 🎯 Features

### Core Functionality
- **AI Trip Generator** — Create personalized itineraries based on destination, dates, travel style, and party size
- **Discover Section** — Browse destinations by interest, experience curated collections, and explore iconic places worldwide
- **Hotels** — Search and filter accommodations by price, popularity, and location
- **Restaurants** — Browse dining options from street food to fine dining
- **Things to Do** — Discover activities and attractions (adventure, culture, relaxation)
- **Instant Map Routes (IMR)** — Multi-modal routing with auto-selected transport modes (air, train, bus, car, bike, cycle, walk)
- **Trip Management** — Save, view, and manage saved trips

### Technical Highlights
- **Responsive Design** — Mobile-first approach with Bootstrap 5.3.1
- **Sidebar Navigation** — Fixed navigation with smooth transitions
- **Dark Mode Support** — Built-in theme switching
- **LocalStorage Persistence** — Client-side data storage for users, trips, and messages
- **Interactive Map** — Leaflet.js integration with dynamic route planning
- **Smooth Animations** — AOS (Animate On Scroll) library for engaging UX

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Frontend Framework** | Bootstrap 5.3.1 |
| **Mapping** | Leaflet 1.9.4 |
| **Icons** | Font Awesome 6.4.0 |
| **Animations** | AOS 2.3.4 |
| **Storage** | Browser LocalStorage |
| **Routing** | OpenStreetMap Nominatim |

---

## 📂 Project Structure

```
guide-360/
├── README.md          # This file
├── source code        # Single-file HTML/CSS/JavaScript application
└── (Future expansion)
    ├── /public        # Static assets
    ├── /src           # Component structure
    └── /api           # Backend endpoints
```

---

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools or dependencies required (standalone HTML)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/myakalavignesh01/guide-360.git
   cd guide-360
   ```

2. **Open in browser**
   - Double-click `source code` or
   - Use a local server:
     ```bash
     python -m http.server 8000
     # Then visit http://localhost:8000
     ```

3. **Start exploring**
   - Navigate using the sidebar menu
   - Create a trip from the hero section or dedicated Trip Builder
   - Add map points to visualize multi-modal routes

---

## 🎮 Usage Guide

### Creating a Trip
1. Click **"Home"** or scroll to the hero section
2. Enter destination (e.g., "Goa", "Paris")
3. Select travel dates and party type
4. Click **"Create Trip"** to generate AI suggestions
5. View budget estimates and itinerary details

### Multi-Modal Routing (IMR)
1. Go to **"IMR"** section
2. Search for locations or click on the map to add points
3. Auto-selected transport modes appear in the table
4. Click on a route segment to override the travel mode
5. View total distance and estimated travel time

### Managing Trips
- **Save trips** from the AI generator
- **View saved trips** in the Trip Management section
- **Delete trips** with the delete button

### User Authentication
- Access **Login/Register** from the sidebar
- Demo credentials are stored in browser LocalStorage

---

## 📊 Data & API Integration

### LocalStorage Keys
| Key | Purpose |
|-----|---------|
| `g360_listings` | Hotels, restaurants, activities |
| `g360_aiTrips` | Saved user trips |
| `g360_users` | User accounts (demo) |
| `g360_messages` | Contact form submissions |
| `g360_tempTrip` | Temporary trip data |

### External APIs
- **OpenStreetMap Nominatim** — Location search
- **Leaflet Tile Layer** — Map rendering
- `/api/guide360-ai` — AI trip generation (optional backend endpoint)

### Fallback Behavior
If the AI endpoint is unavailable, the app uses a **local AI generator** that:
- Filters destinations from sample data
- Calculates budget based on travel mood
- Generates basic itineraries

---

## 🎨 Design System

### Color Palette
| Element | Light Mode | Dark Mode |
|---------|-----------|-----------|
| Background | `#f6f8fb` | `#071227` |
| Card | `#ffffff` | `#0b1220` |
| Accent | `#0ea5a4` | `#2dd4bf` |
| Text (Muted) | `#6b7280` | `#9aa4b2` |

### Responsive Breakpoints
- **Desktop**: ≥ 1200px — Full grid (4 columns)
- **Tablet**: 600–1200px — 2–3 columns
- **Mobile**: < 600px — Single column, collapsed sidebar

---

## 🔧 Configuration & Customization

### Adjust Transport Speeds
Edit the `transportModes` object in the script:
```javascript
const transportModes = {
  air:   { label: "✈ Air",   speed: 800 },
  train: { label: "🚆 Train", speed: 90  },
  // ... adjust speeds (km/h)
};
```

### Add More Sample Data
Modify `seedListings()` to add hotels, restaurants, and activities:
```javascript
{id:'l9', type:'hotel', title:'New Hotel', city:'Jaipur', price:3500, img:'...', desc:'...'}
```

### Connect Real Backend
Replace `callGuideAI()` endpoint with your actual API:
```javascript
const endpoint = 'https://your-api.com/api/generate-trip';
```

---

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome | ✅ 90+ |
| Firefox | ✅ 88+ |
| Safari | ✅ 14+ |
| Edge | ✅ 90+ |
| IE11 | ❌ Not supported |

---

## 🚧 Future Enhancements

- [ ] Backend API integration for AI trip generation
- [ ] User authentication with persistent database
- [ ] Real-time booking integration (hotels, flights)
- [ ] Social sharing and trip collaboration
- [ ] Push notifications for travel updates
- [ ] Offline mode with service workers
- [ ] Mobile app (React Native/Flutter)
- [ ] Payment gateway integration
- [ ] Real-time weather & recommendations
- [ ] Accessibility improvements (WCAG 2.1 AA compliance)

---

## 🐛 Known Issues & Limitations

| Issue | Workaround |
|-------|-----------|
| No persistent backend | Data clears on browser refresh |
| Limited sample data | Expand `seedListings()` with more entries |
| AI endpoint optional | Uses local generator as fallback |
| Mobile sidebar overlap | Dismiss menu after selection |

---

## 📝 Contributing

Contributions are welcome! To contribute:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/my-feature`)
3. **Commit** changes (`git commit -m 'Add feature'`)
4. **Push** to branch (`git push origin feature/my-feature`)
5. **Open** a Pull Request

---

## 📄 License

This project is open source and available under the **MIT License**. See LICENSE file for details.

---

## 👤 Author

**Akalavignesh** — [@myakalavignesh01](https://github.com/myakalavignesh01)

---

## 📞 Support & Feedback

- **Issues**: [GitHub Issues](https://github.com/myakalavignesh01/guide-360/issues)
- **Contact**: Use the Contact form in the app
- **Email**: Check repository for contact info

---

## 🙏 Acknowledgments

- **Bootstrap** — UI framework
- **Leaflet** — Interactive maps
- **Font Awesome** — Icons
- **OpenStreetMap** — Map tiles & geocoding
- **Pexels** — Stock photography

---

**Guide360** — Plan, Save & Share Trips Worldwide 🌍✈️

