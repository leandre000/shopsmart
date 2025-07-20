# ShopMart Frontend

A modern, responsive inventory management system built with React, TypeScript, and Tailwind CSS. ShopMart provides comprehensive tools for managing inventory, sales, suppliers, and business analytics.

## 🚀 Features

### Core Functionality
- **Inventory Management**: Add, edit, delete, and track product inventory with real-time stock levels
- **Sales Management**: Process sales transactions and maintain sales history
- **Supplier Management**: Manage supplier information and relationships
- **Debt Tracking**: Monitor customer debts and payment status
- **Reports & Analytics**: Generate detailed business reports and visual analytics
- **User Management**: Role-based access control with admin and user roles

### Technical Features
- **Modern UI/UX**: Built with shadcn/ui components and Tailwind CSS
- **Responsive Design**: Mobile-first approach with responsive layouts
- **Real-time Data**: Live updates and real-time notifications
- **Image Upload**: Product image management with preview functionality
- **Search & Filtering**: Advanced search and filtering capabilities
- **Pagination**: Efficient data pagination for large datasets
- **Form Validation**: Comprehensive form validation with error handling
- **Internationalization**: Multi-language support (English, Spanish, French, Kinyarwanda)

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn** or **bun**
- **Git**

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd shopmart-frontend
   ```

2. **Install dependencies**
   ```bash
   # Using npm
   npm install

   # Using yarn
   yarn install

   # Using bun
   bun install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   VITE_API_BASE_URL=http://localhost:8080
   VITE_APP_NAME=ShopMart
   ```

4. **Start the development server**
   ```bash
   # Using npm
   npm run dev

   # Using yarn
   yarn dev

   # Using bun
   bun dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5173` to view the application.

## 🏗️ Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ui/             # shadcn/ui components
│   ├── Charts.tsx      # Chart components
│   ├── DataTable.tsx   # Data table component
│   ├── LanguageSwitcher.tsx
│   └── Logo.tsx
├── context/            # React context providers
│   └── AuthContext.tsx # Authentication context
├── hooks/              # Custom React hooks
├── layouts/            # Layout components
│   ├── AuthLayout.tsx
│   └── DashboardLayout.tsx
├── lib/                # Utility functions
├── locales/            # Internationalization files
├── pages/              # Page components
│   ├── AboutUs.tsx
│   ├── Admin.tsx
│   ├── ContactUs.tsx
│   ├── Dashboard.tsx
│   ├── Debts.tsx
│   ├── Inventory.tsx
│   ├── LandingPage.tsx
│   ├── Login.tsx
│   ├── Profile.tsx
│   ├── Reports.tsx
│   ├── Sales.tsx
│   ├── SignUp.tsx
│   └── Suppliers.tsx
├── services/           # API services
│   ├── api.ts          # Main API functions
│   ├── auth.ts         # Authentication services
│   └── dashboardService.ts
├── App.tsx             # Main App component
├── main.tsx           # Application entry point
└── index.css          # Global styles
```

## 🔧 Available Scripts

```bash
# Development
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run lint:fix     # Fix ESLint errors

# Type checking
npm run type-check   # Run TypeScript type checking
```

## 🎨 UI Components

The project uses [shadcn/ui](https://ui.shadcn.com/) components built on top of Tailwind CSS. Key components include:

- **Button**: Various button styles and variants
- **Card**: Content containers with headers and descriptions
- **Dialog**: Modal dialogs for forms and confirmations
- **Table**: Data tables with sorting and pagination
- **Form**: Form components with validation
- **Input**: Text inputs with various types
- **Badge**: Status indicators and labels
- **Tabs**: Tabbed navigation
- **Alert**: Notification components
- **Avatar**: User profile images
- **Progress**: Progress indicators
- **Toast**: Notification toasts

## 🔐 Authentication

The application implements JWT-based authentication with the following features:

- **Login/Logout**: Secure authentication flow
- **Sign Up**: User registration with validation
- **Password Reset**: Forgot password functionality
- **Role-based Access**: Admin and user roles
- **Protected Routes**: Route protection based on authentication status
- **Profile Management**: User profile updates

### Authentication Flow

1. **Login**: Users authenticate with email and password
2. **Token Storage**: JWT tokens are stored securely
3. **Route Protection**: Protected routes check authentication status
4. **Role Verification**: Admin routes require admin privileges
5. **Auto-logout**: Automatic logout on token expiration

## 📊 API Integration

The application integrates with a RESTful API backend. Key API endpoints include:

### Authentication
- `POST /auth/login` - User login
- `POST /auth/signup` - User registration
- `POST /auth/forgot-password` - Password reset request
- `POST /auth/reset-password` - Password reset

### Inventory Management
- `GET /inventory` - Get all inventory items
- `POST /inventory` - Add new inventory item
- `PUT /inventory/{id}` - Update inventory item
- `DELETE /inventory/{id}` - Delete inventory item
- `GET /inventory/{id}` - Get inventory item by ID

### Sales Management
- `GET /sales` - Get all sales
- `POST /sales` - Create new sale
- `DELETE /sales/{id}` - Delete sale
- `GET /sales/summary` - Get sales summary

### Supplier Management
- `GET /suppliers` - Get all suppliers
- `POST /suppliers` - Add new supplier
- `PUT /suppliers/{id}` - Update supplier
- `DELETE /suppliers/{id}` - Delete supplier

### Debt Management
- `GET /debts` - Get all debts
- `POST /debts` - Add new debt
- `PUT /debts/{id}` - Update debt
- `DELETE /debts/{id}` - Delete debt

## 📈 Reports & Analytics

The Reports page provides comprehensive business analytics:

### Sales Analytics
- **Daily/Weekly/Monthly Sales**: Time-based sales tracking
- **Sales vs Profit**: Comparative analysis
- **Category Performance**: Sales breakdown by category
- **Top Selling Products**: Product performance ranking

### Visual Charts
- **Bar Charts**: Sales and profit visualization
- **Pie Charts**: Category distribution
- **Line Charts**: Trend analysis
- **Responsive Design**: Charts adapt to screen size

### Export Features
- **Report Generation**: Custom date range reports
- **Data Export**: Export reports in various formats
- **Print Support**: Print-friendly report layouts

## 🌐 Internationalization

The application supports multiple languages:

- **English** (en)
- **Spanish** (es)
- **French** (fr)
- **Kinyarwanda** (rw)

Language switching is available throughout the application via the LanguageSwitcher component.

## 📱 Responsive Design

The application is built with a mobile-first approach:

- **Mobile**: Optimized for smartphones and tablets
- **Tablet**: Responsive layouts for medium screens
- **Desktop**: Full-featured desktop experience
- **Touch-friendly**: Optimized for touch interactions

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Input Validation**: Comprehensive form validation
- **XSS Protection**: Built-in XSS protection
- **CSRF Protection**: CSRF token implementation
- **Secure Headers**: Security headers configuration
- **Error Handling**: Secure error handling without information leakage

## 🧪 Testing

```bash
# Run tests
npm run test

# Run tests with coverage
npm run test:coverage

# Run tests in watch mode
npm run test:watch
```

## 📦 Build & Deployment

### Production Build
```bash
npm run build
```

### Environment Variables
```env
# Production
VITE_API_BASE_URL=https://your-api-domain.com
VITE_APP_NAME=ShopMart
NODE_ENV=production
```

### Deployment Options
- **Vercel**: Zero-config deployment
- **Netlify**: Static site hosting
- **AWS S3**: Static website hosting
- **Docker**: Containerized deployment

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use ESLint and Prettier for code formatting
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:

- **Documentation**: Check the inline code comments
- **Issues**: Create an issue on GitHub
- **Email**: Contact the development team
- **Discord**: Join our community server

## 🔄 Changelog

### Version 1.0.0
- Initial release
- Core inventory management features
- Sales tracking and reporting
- Supplier management
- User authentication and authorization
- Multi-language support
- Responsive design

## 🙏 Acknowledgments

- [shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [React](https://reactjs.org/) for the JavaScript library
- [TypeScript](https://www.typescriptlang.org/) for type safety
- [Vite](https://vitejs.dev/) for the build tool
- [Recharts](https://recharts.org/) for the chart components
- [Lucide React](https://lucide.dev/) for the icons

---

**ShopMart Frontend** - Modern inventory management made simple. 
