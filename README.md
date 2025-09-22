# 🎴 Credit Card Generator

> Interactive Vue.js credit card component with real-time validation, animations, and downloadable card images

[![Vue.js](https://img.shields.io/badge/Vue.js-2.6.10-4FC08D?style=flat&logo=vue.js)](https://vuejs.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/Yashkadekar/credit-card-generator)](https://github.com/Yashkadekar/credit-card-generator/issues)

A beautiful and interactive credit card form component built with Vue.js. Features smooth animations, real-time validation, automatic card type detection, and the ability to download your card as a high-resolution image.

![Demo](demo.gif)

## ✨ Features

- 🎨 **Interactive Design** - Smooth animations and beautiful UI
- 💳 **Card Type Detection** - Automatically detects Visa, MasterCard, Amex, etc.
- ✅ **Real-time Validation** - Instant form validation with Luhn algorithm
- 📱 **Responsive** - Works perfectly on all devices
- 🎯 **Card Masking** - Secure card number display with toggle option
- 📥 **Download Feature** - Export your card as PNG image
- 🌈 **Dynamic Backgrounds** - Random beautiful card backgrounds
- 🎪 **Micro-interactions** - Delightful hover and focus effects
- 🔄 **Form Persistence** - Maintains state during interactions

## 🚀 Quick Start

### Installation

```bash
npm install
```

### Development

```bash
npm run serve
```

Open [http://localhost:8080](http://localhost:8080) to view it in the browser.

### Build for Production

```bash
npm run build
```

## 📖 Usage

### Basic Implementation

```vue
<template>
  <div>
    <CardForm
      :form-data="formData"
      @input-card-number="updateCardNumber"
      @input-card-name="updateCardName"
      @input-card-month="updateCardMonth"
      @input-card-year="updateCardYear"
      @input-card-cvv="updateCardCvv"
      :download-card="downloadCard"
    />
  </div>
</template>

<script>
import CardForm from '@/components/CardForm'

export default {
  components: {
    CardForm
  },
  data() {
    return {
      formData: {
        cardNumber: '',
        cardName: '',
        cardMonth: '',
        cardYear: '',
        cardCvv: ''
      }
    }
  },
  methods: {
    updateCardNumber(val) {
      this.formData.cardNumber = val
    },
    updateCardName(val) {
      this.formData.cardName = val
    },
    updateCardMonth(val) {
      this.formData.cardMonth = val
    },
    updateCardYear(val) {
      this.formData.cardYear = val
    },
    updateCardCvv(val) {
      this.formData.cardCvv = val
    },
    downloadCard() {
      // Download functionality will be triggered automatically
      // when form is valid and submitted
    }
  }
}
</script>
```

## 🎨 Customization

### Card Size
The component features an optimized larger card size:
- **Desktop:** 600px × 380px
- **Mobile:** 450px × 280px
- **Small Mobile:** 240px height

### Background Images
Customize card backgrounds by providing your own images or using the built-in random background system.

## 📋 Requirements

- Vue.js 2.6+
- Modern browser with ES6 support
- npm or yarn

## 🛠️ Available Scripts

- `npm run serve` - Start development server
- `npm run build` - Build for production
- `npm run test:unit` - Run unit tests
- `npm run lint` - Lint and fix files

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Original design inspiration
- Vue.js community
- All contributors

---

**Made with ❤️ by [Yash Kadekar](https://github.com/Yashkadekar)**

⭐ Star this repo if you found it useful!
