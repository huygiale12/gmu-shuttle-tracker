# GMU Shuttle Tracker

A real-time shuttle tracking system for George Mason University, built with React and implementing SysML/MBSE requirements.

![GMU Shuttle](https://img.shields.io/badge/GMU-Shuttle%20Tracker-0066FF)
![React](https://img.shields.io/badge/React-18.2-61DAFB)
![License](https://img.shields.io/badge/license-MIT-green)

## 📋 Overview

This application is a live shuttle tracking system designed for GMU's campus transportation network, featuring real-time vehicle monitoring, route management, and on-demand booking capabilities.

### ✨ Key Features

- **Live Tracking**: Real-time GPS updates every 3 seconds (REQ-P-01)
- **5 Transit Routes**: Blue, Green, Orange, Purple, and Red lines
- **Delay Notifications**: Automatic alerts when shuttles exceed 5-minute delays (REQ-F-03)
- **On-Demand Booking**: Request rides with pickup/drop-off locations (REQ-F-04)
- **Route Filtering**: Filter map view by specific corridors (REQ-U-01)
- **Live Occupancy**: Real-time passenger capacity monitoring
- **Responsive Design**: Works on desktop and mobile devices

## 🚀 Live Demo

Simply open `gmu-shuttle-app.html` in any modern web browser - no build process required!

## 📦 Installation

### Option 1: Direct Use
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/gmu-shuttle-tracker.git

# Open the file
cd gmu-shuttle-tracker
open gmu-shuttle-app.html  # macOS
# or
start gmu-shuttle-app.html  # Windows
# or
xdg-open gmu-shuttle-app.html  # Linux
```

### Option 2: Local Server
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve

# Then visit http://localhost:8000
```

## 🎯 Requirements Implemented

This project implements requirements from SYST 205: Systems Engineering Principles

### Functional Requirements
- **REQ-F-01**: Route timetable access for all 5 corridors
- **REQ-F-02**: Real-time vehicle position tracking
- **REQ-F-03**: Delay notifications (>5 minutes)
- **REQ-F-04**: On-demand ride booking

### Performance Requirements
- **REQ-P-01**: GPS coordinate updates every 3 seconds
- **REQ-P-02**: ETA calculations within 2-second response time
- **REQ-P-03**: 10-meter positioning accuracy

### Usability Requirements
- **REQ-U-01**: Route-specific filtering
- **REQ-U-02**: Accessibility features

### Security Requirements
- **REQ-S-01**: NetID authentication (framework ready)
- **REQ-S-02**: TLS 1.3 encryption (deployment ready)
- **REQ-S-03**: Role-based access control

## 🏗️ Architecture

### Technology Stack
- **Frontend**: React 18.2
- **Styling**: Custom CSS with CSS Variables
- **Fonts**: Archivo (UI) + JetBrains Mono (monospace)
- **Icons**: Unicode emoji markers

### Component Structure
```
App
├── Header (Logo, Mode Toggle, Status)
├── Sidebar
│   ├── Route Filters
│   └── Shuttle List
└── Map Container
    ├── Route Lines
    ├── Shuttle Markers
    ├── Stop Markers
    └── Booking Panel (on-demand mode)
```

## 🎨 Design System

### Color Palette
- **Routes**: Blue (#0066FF), Green (#00CC66), Orange (#FF6B35), Purple (#9D4EDD), Red (#EE4266)
- **Background**: Dark theme (#0A0E17, #151922, #1E242E)
- **Text**: Primary (#F8F9FA), Secondary (#ADB5BD)

### Typography
- **Display**: Archivo (900 weight for headers)
- **Body**: Archivo (400-700 weights)
- **Code**: JetBrains Mono (shuttle IDs, technical data)

## 📱 Usage

### Scheduled Service Mode
1. View all active shuttles on the map
2. Filter by route using the sidebar
3. Click on shuttles for details
4. Monitor real-time positions and ETAs

### On-Demand Mode
1. Click "On-Demand" toggle
2. Enter pickup location
3. Enter drop-off destination
4. Request shuttle

## 🔧 Customization

### Adding New Routes
```javascript
const ROUTES = [
    {
        id: 'NEW_ROUTE',
        name: 'New Line',
        color: '#YOUR_COLOR',
        path: 'Stop A → Stop B → Stop C'
    },
    // ... existing routes
];
```

### Adjusting Update Frequency
```javascript
// Change GPS update interval (default: 3000ms)
setInterval(() => {
    // Update logic
}, 3000); // Modify this value
```

## 📊 SysML Models

This implementation is based on comprehensive SysML models including:
- Requirements Diagram (req)
- Block Definition Diagram (bdd)
- Activity Diagram (act)
- Sequence Diagram (sd)
- State Machine Diagram (stm)

See `Final_Assignment_Raymond_Le_G01503237.pdf` for complete model documentation.

## 🚧 Future Enhancements

- [ ] Real GPS integration via browser Geolocation API
- [ ] Backend API integration for live data
- [ ] User authentication with NetID
- [ ] Push notifications for delays
- [ ] Offline mode with cached schedules (REQ-R-01)
- [ ] Accessibility screen reader support (REQ-U-02)
- [ ] Route optimization algorithms
- [ ] Historical data analytics

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Raymond Le**
- Student ID: G01503237
- Course: SYST 205 - Systems Engineering Principles
- Semester: Fall 2025

## 🙏 Acknowledgments

- George Mason University Transportation Services
- SysML and MBSE methodologies
- PlantUML for diagram generation
- React community for excellent documentation

## 📞 Support

For questions or issues, please open an issue on GitHub or contact through GMU email.

---

**Note**: This is a demonstration project for educational purposes. For actual GMU shuttle tracking, visit [GMU Transportation Services](https://transportation.gmu.edu/shuttles/).
