# Digital Clock - Multiple Time Zones

A beautiful, responsive digital clock application that displays the current time in different time zones around the world.

## Features

✨ **Key Features:**
- 📍 8 Pre-configured Major Cities (New York, London, Paris, Dubai, Singapore, Tokyo, Sydney, Los Angeles)
- 🌍 Add Custom Time Zones on the fly
- 🎨 Modern glassmorphism UI design
- 📱 Fully responsive (works on desktop, tablet, mobile)
- ⏰ Real-time updates (every second)
- 🌐 UTC offset display
- 📅 Date display for each timezone
- 🎯 Easy-to-use custom timezone input
- 🖥️ Local time display

## File Structure

```
digital-clock/
├── index.html      # Main HTML structure
├── style.css       # Styling and animations
├── script.js       # JavaScript functionality
└── README.md       # Documentation
```

## How to Use

### Basic Usage
1. Open `index.html` in your web browser
2. View the current time in 8 major cities worldwide
3. Scroll down to see your local time

### Adding Custom Time Zones

1. Scroll to "Add Custom Time Zone" section
2. Enter a city name (e.g., "Mumbai", "Bangkok")
3. Enter the UTC offset (e.g., 5.5 for IST, -7 for MST)
4. Click "Add Clock"
5. The new clock will appear and update in real-time
6. Click the "×" button on any custom clock to remove it

### UTC Offset Examples
- UTC-12: Baker Island
- UTC-8: Los Angeles, Vancouver
- UTC-5: New York, Toronto
- UTC+0: London, Dublin
- UTC+1: Paris, Berlin
- UTC+5.5: India Standard Time (IST)
- UTC+8: Singapore, Hong Kong
- UTC+9: Tokyo, Seoul
- UTC+12: New Zealand

## Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with gradients, animations, and glassmorphism
- **JavaScript (ES6+)** - Time calculations and DOM manipulation

## Browser Compatibility

- Chrome/Edge (Latest)
- Firefox (Latest)
- Safari (Latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Key JavaScript Functions

### `getTimeForTimezone(offset)`
Calculates the current time for a given UTC offset.

```javascript
const timeInZone = getTimeForTimezone(5.5); // IST
```

### `updateAllClocks()`
Updates all clocks (predefined and custom) every second.

### `addCustomTimezone()`
Adds a new custom timezone clock based on user input.

```javascript
addCustomTimezone(); // Triggered by button click
```

### `removeCustomTimezone(id)`
Removes a custom timezone clock.

## Styling Features

- **Glassmorphism Effect**: Semi-transparent backgrounds with backdrop blur
- **Gradient Backgrounds**: Linear gradients for visual appeal
- **Responsive Grid**: Auto-fitting columns based on screen size
- **Hover Effects**: Cards lift up on hover
- **Green Digital Display**: Classic digital clock green text with glow effect
- **Smooth Animations**: Pulsing text animation for visual feedback

## Customization

### Change Pre-configured Cities
Edit the `timeZones` array in `script.js`:

```javascript
const timeZones = [
    { id: 'ny', city: 'New York', offset: -5, name: 'America/New_York' },
    // Add or modify cities here
];
```

### Modify Colors
Edit the gradients in `style.css`:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Update Interval
Modify the interval in `script.js`:

```javascript
setInterval(updateAllClocks, 1000); // Change 1000 to desired milliseconds
```

## Live Demo

Open `index.html` directly in your browser - no server required!

## Notes

- All times are calculated based on the system's local time and the provided UTC offset
- Daylight Saving Time (DST) is not automatically calculated
- For accurate DST-aware times, consider integrating with a timezone library like `moment-timezone`

## Future Enhancements

- [ ] Add DST support using timezone libraries
- [ ] Save custom timezones to localStorage
- [ ] Add alarm functionality
- [ ] Weather information for each timezone
- [ ] Sunrise/Sunset times
- [ ] 24-hour format toggle
- [ ] Sound notifications

## License

Free to use and modify for personal or commercial projects.

---

**Created with ❤️ using HTML, CSS, and JavaScript**
