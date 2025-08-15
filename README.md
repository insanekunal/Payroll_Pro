# PayrollPro India - Employee Payroll Management System

A modern, full-stack employee payroll management system built with React, TypeScript, and Express. Designed specifically for Indian companies with INR currency support, Indian address formats, and compliance-ready features. Includes comprehensive employee management, automated payroll calculations, detailed analytics, and a beautiful dark/light theme interface.

![PayrollPro Dashboard](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-5.5.3-blue)
![React](https://img.shields.io/badge/React-18.3.1-blue)
![Vite](https://img.shields.io/badge/Vite-6.3.5-purple)

## ✨ Features

### 🏢 **Employee Management**
- **Complete CRUD Operations**: Add, edit, delete, and view employees
- **Comprehensive Employee Profiles**: Personal info, employment details, contact information
- **Advanced Search & Filtering**: Filter by department, status, and search by name/email
- **Responsive Data Tables**: Professional table layouts with sorting and pagination
- **Status Management**: Track active, inactive, and terminated employees

### 💰 **Payroll Processing**
- **Interactive Payroll Calculator**: Select employees, set pay periods, add overtime and bonuses
- **Automated Calculations**: Real-time salary calculations with tax deductions
- **Payment Management**: Process payments and track payment history
- **Flexible Pay Periods**: Support for weekly, bi-weekly, monthly, and custom periods
- **Overtime & Bonus Handling**: Easy overtime rate calculations and bonus additions

### 📊 **Reports & Analytics**
- **Visual Dashboard**: Interactive charts and graphs using Recharts
- **Department Analytics**: Employee distribution and salary analysis by department
- **Salary Range Reports**: Visual breakdown of salary ranges across the organization
- **Monthly Trends**: Track payroll trends over time
- **Export Capabilities**: Download reports in various formats
- **Top Performers**: Identify highest earners and department summaries

### ⚙️ **System Settings**
- **Company Configuration**: Manage business details, contact information, and tax settings
- **Payroll Settings**: Configure pay periods, deduction rates, and overtime multipliers
- **System Preferences**: Timezone, date formats, and notification settings
- **Security Controls**: Two-factor authentication, session management, and access controls
- **Data Management**: Backup, import, and synchronization tools

### 🎨 **Modern UI/UX**
- **Dark/Light Theme**: Seamless theme switching with system preference detection
- **Smooth Animations**: Professional fade-in, slide, and scale effects
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Interactive Elements**: Hover effects, loading states, and micro-interactions
- **Accessibility**: Screen reader support and keyboard navigation

## 🚀 Tech Stack

### Frontend
- **React 18** - Modern React with hooks and concurrent features
- **TypeScript** - Type-safe development with excellent IntelliSense
- **Vite** - Lightning-fast build tool and dev server
- **TailwindCSS** - Utility-first CSS framework for rapid styling
- **Radix UI** - Accessible, unstyled UI primitives
- **React Router 6** - Client-side routing with SPA mode
- **Recharts** - Responsive chart library built on D3
- **Lucide React** - Beautiful, customizable icons

### Backend
- **Express.js** - Fast, minimalist web framework
- **TypeScript** - Full-stack type safety
- **Zod** - Schema validation with TypeScript integration
- **CORS** - Cross-origin resource sharing support

### Development Tools
- **Vitest** - Fast unit testing framework
- **ESLint** - Code linting and quality assurance
- **Prettier** - Code formatting and style consistency
- **Hot Reload** - Real-time development updates

## 📁 Project Structure

```
PayrollPro/
├── client/                     # Frontend React application
│   ├── components/            # Reusable UI components
│   │   ├── ui/               # Base UI components (buttons, cards, etc.)
│   │   ├── Dashboard.tsx     # Main dashboard component
│   │   ├── EmployeeForm.tsx  # Employee creation/editing form
│   │   ├── EmployeeTable.tsx # Employee data table
│   │   ├── PayrollCalculator.tsx # Payroll calculation interface
│   │   ├── PayrollTable.tsx  # Payroll history table
│   │   ├── Header.tsx        # Navigation header
│   │   └── ThemeToggle.tsx   # Dark/light mode toggle
│   ├── pages/                # Route components
│   │   ├── Index.tsx         # Dashboard page
│   │   ├── Employees.tsx     # Employee management
│   │   ├── Payroll.tsx       # Payroll processing
│   │   ├── Reports.tsx       # Analytics and reports
│   │   └── Settings.tsx      # System configuration
│   ├── hooks/                # Custom React hooks
│   │   ├── use-theme.ts      # Theme management
│   │   └── use-toast.ts      # Toast notifications
│   ├── lib/                  # Utility functions
│   └── global.css           # Global styles and animations
├── server/                   # Backend Express application
│   ├��─ routes/              # API route handlers
│   │   ├── employees.ts     # Employee CRUD operations
│   │   └── demo.ts         # Demo endpoints
│   └── index.ts            # Server configuration
├── shared/                  # Shared TypeScript types
│   ├── api.ts              # API interfaces
│   └── employee.ts         # Employee data models
└── package.json            # Dependencies and scripts
```

## 🛠️ Installation & Setup

### Prerequisites
- **Node.js** (v18 or higher)
- **npm** or **yarn**

### Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd payrollpro
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:8080`

### Development Commands

```bash
# Start development server (frontend + backend)
npm run dev

# Build for production
npm run build

# Start production server
npm run start

# Run TypeScript type checking
npm run typecheck

# Run tests
npm test

# Format code
npm run format.fix
```

## 🔌 API Endpoints

### Employee Management
- `GET /api/employees` - Get all employees
- `GET /api/employees/:id` - Get employee by ID
- `POST /api/employees` - Create new employee
- `PUT /api/employees/:id` - Update employee
- `DELETE /api/employees/:id` - Delete employee

### Dashboard & Analytics
- `GET /api/dashboard/stats` - Get dashboard statistics

### Payroll Management
- `GET /api/payroll` - Get payroll entries (with optional filters)
- `POST /api/payroll/calculate` - Calculate payroll for an employee
- `PATCH /api/payroll/:id/pay` - Process payment for payroll entry

### System
- `GET /api/ping` - Health check endpoint

## 🎯 Usage Guide

### Managing Employees

1. **Adding Employees**
   - Navigate to the Employees page
   - Click "Add Employee" button
   - Fill in personal and employment details
   - Set salary and employment information
   - Save to create the employee record

2. **Editing Employees**
   - Find the employee in the table
   - Click the edit button (three dots menu)
   - Update any necessary information
   - Save changes

### Processing Payroll

1. **Calculate Payroll**
   - Go to the Payroll page
   - Click "New Payroll" button
   - Select employee and pay period
   - Add any overtime or bonuses
   - Review calculations and save

2. **Process Payments**
   - View pending payrolls in the table
   - Click "Process" for any pending payment
   - Confirm payment processing

### Viewing Reports

1. **Dashboard Analytics**
   - View key metrics on the main dashboard
   - See employee distribution and payroll summaries
   - Monitor pending payments and recent activity

2. **Detailed Reports**
   - Visit the Reports page for comprehensive analytics
   - View charts for department distribution
   - Analyze salary ranges and trends
   - Export data for external analysis

## 🎨 Customization

### Theme Configuration
The system supports full dark/light theme customization. Themes are configured in:
- `client/global.css` - CSS custom properties for colors
- `tailwind.config.ts` - Tailwind theme configuration
- Theme toggle available in header and settings

### Adding New Features
1. Create components in `client/components/`
2. Add routes in `client/App.tsx`
3. Create API endpoints in `server/routes/`
4. Define TypeScript types in `shared/`

## 🚀 Deployment

### Standard Deployment
```bash
# Build the application
npm run build

# Start production server
npm start
```

### Cloud Deployment
The application is ready for deployment on:
- **Netlify** - Static site hosting with serverless functions
- **Vercel** - Full-stack application deployment
- **Railway** - Container-based deployment
- **Heroku** - Platform-as-a-service deployment

### Environment Variables
Configure these environment variables for production:
```bash
NODE_ENV=production
PORT=8080
# Add any additional configuration as needed
```

## 📊 Sample Data

The system comes with pre-loaded sample data including:
- 10 sample Indian employees (Arjun Sharma, Priya Patel, Rahul Kumar, etc.)
- Sample payroll entries with INR calculations
- Indian address formats and phone numbers
- Department and role configurations suitable for Indian companies
- PAN format tax IDs and Indian bank account details

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use meaningful component and function names
- Write tests for new features
- Maintain responsive design principles
- Follow the existing code style and patterns

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the documentation in the `docs/` folder
- Review the codebase for implementation examples


**PayrollPro** - Modern payroll management made simple. Built with ❤️ using React and TypeScript.
