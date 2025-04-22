# Idaho Pro Services Directory Website

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Idaho's premier directory website for connecting residents with trusted home and business service providers.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Directory Structure](#directory-structure)
- [Customization Guide](#customization-guide)
- [Deployment](#deployment)
- [Custom Domain Setup](#custom-domain-setup)
- [Troubleshooting](#troubleshooting)
- [Resources & Support](#resources--support)

## Overview

Idaho Pro Services is a comprehensive directory website featuring a responsive 3-column grid layout, designed to showcase professional service providers across Idaho. The platform offers easy navigation, search functionality, and categorized listings.

## Features

- Responsive 3-column grid layout
- Advanced search functionality
- Category filtering system
- Service provider profiles
- Contact forms
- Rating and review system
- Mobile-friendly design
- SEO optimization
- Fast loading times

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/idaho-pro-services.git

# Navigate to project directory
cd idaho-pro-services

# Install dependencies
npm install

# Start development server
npm run dev
```

## Directory Structure

```
idaho-pro-services/
├── src/
│   ├── components/
│   ├── pages/
│   ├── styles/
│   └── utils/
├── public/
│   ├── images/
│   └── icons/
├── config/
└── package.json
```

## Customization Guide

### Adding Directory Items

1. Navigate to `src/data/directory.js`
2. Add new items using the following format:

```javascript
{
  id: "unique-id",
  name: "Business Name",
  category: "Category",
  description: "Business description",
  contact: {
    phone: "208-555-0123",
    email: "contact@business.com",
    website: "https://www.business.com"
  }
}
```

### Modifying Category Labels

1. Open `src/config/categories.js`
2. Edit the category array:

```javascript
export const categories = [
  "Home Services",
  "Business Services",
  "Professional Services",
  // Add more categories
];
```

### Updating Hero Section

1. Locate `src/components/Hero.js`
2. Modify the content:

```javascript
<HeroSection>
  <h1>Your New Title</h1>
  <p>Your new description</p>
  <Button>Custom CTA</Button>
</HeroSection>
```

### Customizing Colors

1. Edit `src/styles/variables.scss`:

```scss
$primary-color: #004d99;
$secondary-color: #ff6b6b;
$background-color: #f5f5f5;
```

## Deployment

### Building for Production

```bash
# Create production build
npm run build

# Test production build locally
npm run serve
```

### Deployment Options

- Vercel (Recommended)
- Netlify
- GitHub Pages
- Custom Server

## Custom Domain Setup

1. Purchase domain from preferred registrar
2. Add DNS records:
```
A     @     76.76.21.21
CNAME www   yourdomain.com
```
3. Configure domain in deployment platform
4. Wait for DNS propagation (24-48 hours)

## Troubleshooting

### Common Issues

1. **Build Failures**
   - Clear cache: `npm clean cache --force`
   - Delete node_modules: `rm -rf node_modules`
   - Reinstall dependencies: `npm install`

2. **Styling Issues**
   - Clear browser cache
   - Check CSS specificity
   - Verify media queries

3. **Search Not Working**
   - Check API endpoints
   - Verify search index
   - Console for errors

## Resources & Support

- [Documentation Wiki](https://github.com/yourusername/idaho-pro-services/wiki)
- [Issue Tracker](https://github.com/yourusername/idaho-pro-services/issues)
- [Contributing Guidelines](CONTRIBUTING.md)

### Support Channels

- Email: support@idahoproservices.com
- Discord: [Join Server](https://discord.gg/idahoproservices)
- Twitter: [@IdahoProServ](https://twitter.com/IdahoProServ)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

© 2023 Idaho Pro Services. All rights reserved.