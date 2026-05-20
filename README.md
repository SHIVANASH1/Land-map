# Land Feature Detection Map - Boundary Analysis 🗺️

यह एक **interactive web-based map** है जो आपकी boundary के अंदर सभी land features को automatically detect करता है।

## Features 🎯

✅ **Water Bodies** - Rivers, ponds, streams, water bodies  
✅ **Urban Areas** - Buildings, residential zones, populated areas  
✅ **Roads & Infrastructure** - Highways, streets, transportation  
✅ **Agricultural Land** - Farmland, orchards, cropland  
✅ **Trees & Vegetation** - Forests, trees, vegetation areas  
✅ **Drains & Waterways** - Drainage channels, canals, ditches  

## कैसे Use करें?

### 1. **Locally Test करें** (अपने computer पर)
```bash
# बस index.html को अपने browser में खोलें
# या अगर Python है तो:
python -m http.server 8000

# फिर जाएं: http://localhost:8000
```

### 2. **GitHub Pages पर Live करें** 🚀

#### Step 1: GitHub Repository बनाएं
```bash
# अपना repository create करें (example: land-feature-map)
# या अपने existing repository में files add करें
```

#### Step 2: Files Add करें
- `index.html` - main map file

#### Step 3: GitHub Pages Enable करें
1. अपने repository settings जाएं
2. "Pages" section में जाएं (बाईं तरफ)
3. "Source" को **"main branch"** select करें
4. Save करें

#### Step 4: Live URL पाएं
- कुछ minutes में आपका map live होगा:
- `https://yourusername.github.io/repository-name/`

## कैसे काम करता है? ⚙️

1. **Boundary Loading** - आपकी KML file से boundary polygon loaded होती है
2. **Feature Detection** - OpenStreetMap (OSM) और Overpass API से data fetch होता है
3. **Live Visualization** - सभी features map पर display होते हैं colored overlays के साथ
4. **Interactive Filters** - हर feature type को on/off कर सकते हो
5. **Statistics** - Total count दिखाता है हर feature type का

## Data Sources 📊

- **OpenStreetMap (OSM)** - Open, free, community-maintained mapping data
- **Overpass API** - Real-time access to OSM data
- **Leaflet.js** - Interactive map library
- **Font Awesome** - Icons

## Browser Support ✔️

✅ Chrome/Edge (recommended)  
✅ Firefox  
✅ Safari  
✅ Mobile browsers  

## अगर Data नहीं आ रहा?

1. **Overpass API Temporarily Down है** - कुछ देर में try करें
2. **Area में data नहीं है** - OpenStreetMap में contribute करें: https://www.openstreetmap.org
3. **Browser Console** देखें errors के लिए

## कैसे Improve करें?

### Data को Update करें
1. OpenStreetMap (https://www.openstreetmap.org) पर जाएं
2. अपने area में buildings, roads, water bodies add करें
3. Data automatically update होगा next time

### अपने Custom Data Add करें
अगर GeoJSON format में data है तो:

```javascript
// index.html में यह code add करें:
const customGeoJSON = {
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "geometry": {
                "type": "Point",
                "coordinates": [87.5515, 25.5362]
            },
            "properties": {
                "name": "My Feature"
            }
        }
    ]
};

L.geoJSON(customGeoJSON).addTo(map);
```

## Feature Colors 🎨

| Feature | Color | Description |
|---------|-------|-------------|
| Water Bodies | 🔵 Blue | Rivers, ponds, streams |
| Urban Areas | 🔴 Red | Buildings, houses |
| Roads | 🟠 Orange | Highways, streets |
| Agriculture | 🟢 Green | Farms, cropland |
| Vegetation | 💚 Light Green | Trees, forests |
| Drains | 🔷 Light Blue | Drainage channels |

## License 📄

- **Map**: OpenStreetMap contributors (ODbL)
- **Code**: Open source
- **Data**: Creative Commons

## कोई सवाल है?

- OpenStreetMap help: https://wiki.openstreetmap.org
- Leaflet docs: https://leafletjs.com
- Overpass API: https://wiki.openstreetmap.org/wiki/Overpass_API

---

**Made with ❤️ for land feature detection and analysis**
