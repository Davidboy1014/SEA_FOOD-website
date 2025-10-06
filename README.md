# SEA Food Restaurant Website

A full-stack web application for a Southeast Asian restaurant featuring an online ordering system with cart functionality, payment processing, and menu management.

## 🌟 Features

### Frontend (React + Vite)
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Interactive Menu**: Browse entrees, drinks, desserts, and alcoholic beverages
- **Shopping Cart**: Add/remove items, adjust quantities, and view cart summary
- **Order Processing**: Complete order flow with payment information
- **Contact System**: Contact form for customer inquiries
- **About Page**: Restaurant information and mission statement

### Backend (Node.js + Express + MongoDB)
- **RESTful API**: Complete CRUD operations for menu items
- **Cart Management**: Session-based cart with MongoDB storage
- **Order Processing**: Save orders and clear cart upon completion
- **Contact Inquiries**: Store customer messages and feedback
- **Database Integration**: MongoDB with collections for products, cart, orders, and inquiries

## 🏗️ Project Structure

```
SEA_FOOD-website/
├── backend/                         # Node.js backend server
│   ├── server.js                    # Express server and API routes
│   ├── assets/
│   │   └── data.json               # Sample menu data
│   ├── insert*.js                  # Data seeding scripts
│   ├── env.example                 # Environment variables template
│   ├── .gitignore                  # Backend gitignore
│   └── package.json                # Backend dependencies
├── frontend/                        # React frontend application
│   ├── src/
│   │   ├── components/             # React components
│   │   │   ├── App.jsx             # Main application component
│   │   │   ├── EntreeMenu.jsx      # Entrees menu component
│   │   │   ├── DrinksMenu.jsx      # Drinks menu component
│   │   │   ├── DessertsMenu.jsx    # Desserts menu component
│   │   │   ├── ViewCart.jsx        # Shopping cart component
│   │   │   ├── PaymentInfo.jsx     # Payment form component
│   │   │   ├── OrderSummary.jsx    # Order confirmation component
│   │   │   ├── Contact.jsx         # Contact form component
│   │   │   └── About_Us.jsx        # About page component
│   │   ├── assets/                 # SVG icons and images
│   │   ├── images/                 # Team photos and images
│   │   └── styles/                 # CSS files
│   ├── public/                     # Static assets
│   ├── package.json                # Frontend dependencies
│   ├── vite.config.js              # Vite configuration
│   ├── tailwind.config.js          # Tailwind CSS configuration
│   ├── eslint.config.js            # ESLint configuration
│   └── .gitignore                  # Frontend gitignore
├── Documents/                       # Project documentation
│   ├── Final project proposal.pdf  # Project proposal document
│   └── IP14_MT_Proposal (4).pdf    # Additional proposal
├── package.json                     # Root package.json with scripts
├── .gitignore                       # Root gitignore
└── README.md                        # Project documentation
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local instance or MongoDB Atlas)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd SEA_FOOD-website
   ```

2. **Install all dependencies (recommended)**
   ```bash
   npm run install:all
   ```
   
   **OR install manually:**
   ```bash
   # Install root dependencies
   npm install
   
   # Install backend dependencies
   cd backend
   npm install
   
   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

3. **Environment Setup**
   - Copy the environment template:
     ```bash
     cp backend/env.example backend/.env
     ```
   - Edit `backend/.env` with your MongoDB connection string:
     ```env
     MONGODB_URI=your_mongodb_connection_string
     PORT=3000
     NODE_ENV=development
     ```

### Running the Application

**Option 1: Run both frontend and backend together**
```bash
npm start
```

**Option 2: Run separately**
```bash
# Terminal 1 - Start the backend server
npm run start:backend
# API available at http://localhost:3000

# Terminal 2 - Start the frontend development server  
npm run start:frontend
# Application available at http://localhost:5173
```

**Option 3: Manual startup**
```bash
# Backend
cd backend
npm start

# Frontend (in new terminal)
cd frontend
npm run dev
```

## 📡 API Endpoints

### Menu Items
- `GET /products` - Get all entrees
- `GET /drinks` - Get all drinks
- `GET /desserts` - Get all desserts
- `GET /alcohol` - Get all alcoholic beverages

### Cart Management
- `GET /cart` - Get current cart items
- `POST /cart` - Add items to cart
- `PUT /cart/:product_id` - Update item quantity
- `DELETE /cart/:product_id` - Remove item from cart
- `DELETE /cart` - Clear entire cart

### Orders & Inquiries
- `POST /orders` - Submit new order
- `POST /inquiries` - Submit contact form

## 🎨 Technologies Used

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **ESLint** - Code linting

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **CORS** - Cross-origin resource sharing
- **Body Parser** - Request body parsing

## 🍽️ Menu Categories

### Entrees
Traditional Southeast Asian main dishes including:
- Pho (Vietnamese noodle soup)
- Pad Thai (Thai stir-fried noodles)
- Nasi Goreng (Indonesian fried rice)
- And more authentic dishes

### Drinks
- Traditional beverages like Thai Iced Tea
- Fresh fruit smoothies
- Vietnamese coffee
- Refreshing tropical drinks

### Desserts
- Traditional Southeast Asian sweets
- Tropical fruit desserts
- Coconut-based treats
- Rice-based desserts

### Alcoholic Beverages
- Southeast Asian beers
- Traditional rice wines
- Tropical cocktails

## 🔧 Development

### Available Scripts

**Frontend:**
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

**Backend:**
- `npm start` - Start production server
- `npm run dev` - Start development server

### Database Setup

The application uses MongoDB with the following collections:
- `products` - Menu entrees
- `drinks` - Beverage items
- `desserts` - Dessert items
- `alcohol` - Alcoholic beverages
- `cart` - Shopping cart items
- `orders` - Completed orders
- `inquiries` - Contact form submissions

## 👥 Authors

- **Trung Ly** - Full-stack development
- **David Cavan** - Full-stack development

## 📄 License

This project is licensed under the ISC License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

For support or questions, please contact us through the contact form on the website or create an issue in the repository.

---

*Experience the vibrant flavors of Southeast Asia with SEA Food - where authentic cuisine meets modern technology.*