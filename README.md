# Expenses Chart Component

A responsive and interactive expenses chart component built with HTML, CSS, and JavaScript. This component displays weekly spending data in an elegant bar chart format with hover interactions and responsive design for both desktop and mobile devices.

![Preview](./preview.jpg)

## Features

- 📊 **Dynamic Bar Chart** - Visualizes weekly spending data with proportional bar heights
- 🎯 **Interactive Hover States** - Displays exact amounts when hovering over chart bars
- 📱 **Fully Responsive** - Optimized layouts for mobile (375px) and desktop (1440px) screens
- 🎨 **Modern Design** - Beautiful gradient balance card and clean chart interface
- 🔄 **Dynamic Data Loading** - Loads chart data from JSON file and renders bars automatically
- 🌟 **Current Day Highlighting** - Today's bar is highlighted in a different color (cyan)
- ✨ **Smooth Animations** - Smooth transitions and hover effects for better user experience

## Technologies Used

- **HTML5** - Semantic markup structure
- **CSS3** - Custom properties, Flexbox, responsive design, animations
- **JavaScript (Vanilla)** - Dynamic chart rendering, data fetching, interactivity
- **Google Fonts** - DM Sans font family

## Getting Started

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser
3. The chart will automatically load data from `data.json` and render

### Usage

- **Hover over bars** to see the exact spending amount for each day
- The chart automatically highlights today's bar in cyan
- The component is fully responsive and adapts to different screen sizes

## Design Specifications

### Colors

- **Primary**
  - Red 500: `hsl(10, 79%, 65%)`
  - Blue 300: `hsl(186, 34%, 65%)`

- **Neutral**
  - Brown 950: `hsl(25, 47%, 15%)`
  - Brown 400: `hsl(28, 10%, 53%)`
  - Red 100: `hsl(26, 66%, 93%)`
  - Cream: `hsl(33, 100%, 98%)`

### Typography

- **Font Family**: DM Sans (Google Fonts)
- **Font Weights**: 400 (Regular), 700 (Bold)
- **Body Font Size**: 18px

### Layout

- **Mobile**: 375px
- **Desktop**: 1440px
- **Content Max Width**: 540px

## Key Features Implementation

### Dynamic Chart Rendering

The chart bars are dynamically generated from the `data.json` file:

```javascript
// Bars are created proportionally based on the maximum amount
const maxAmount = Math.max(...data.map(item => item.amount));
const height = (item.amount / maxAmount) * 200;
```

### Current Day Detection

The component automatically detects and highlights the current day:

```javascript
function getCurrentDay() {
  const days = ['sun', 'mon', 'tue', 'wed', 'thu', 'fri', 'sat'];
  const today = new Date().getDay();
  return days[today];
}
```

### Interactive Tooltips

Hover tooltips show exact spending amounts with smooth animations and proper positioning above each bar.

## Responsive Breakpoints

- **Mobile**: Default styles (320px - 767px)
- **Tablet/Desktop**: `@media (min-width: 768px)`
- **Small Mobile**: `@media (max-width: 374px)` - Adjusted spacing

## Future Enhancements

- [ ] Add animation on initial load
- [ ] Support for different time periods (monthly, yearly)
- [ ] Data editing capabilities
- [ ] Export chart as image
- [ ] Multiple currency support
- [ ] Dark mode theme

## Credits

- Challenge by [Frontend Mentor](https://www.frontendmentor.io)
- Design inspiration from Frontend Mentor challenges
- Icons and assets from the challenge repository

## License

This project is open source and available for learning purposes.

## Author

Estif

---

⭐ If you find this project helpful, please give it a star!
