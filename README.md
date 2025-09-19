# Jowhara Collection E-commerce Website

A modern, full-stack e-commerce application for beauty and fragrance products built with React, TypeScript, and Supabase.

## 🚀 Features

### Frontend
- **Modern React 18** with TypeScript for type safety
- **Tailwind CSS** for responsive, mobile-first design
- **Vite** for fast development and optimized builds
- **Real-time updates** via Supabase subscriptions
- **Admin dashboard** for complete store management
- **WhatsApp integration** for seamless customer communication
- **SEO optimized** with meta tags and structured data

### Backend (Supabase)
- **PostgreSQL database** with Row Level Security (RLS)
- **Real-time subscriptions** for live data updates
- **Authentication** with role-based access control
- **File storage** for product images
- **Edge functions** for serverless API endpoints
- **Comprehensive audit logging** for admin actions

### Admin Features
- Product catalog management (CRUD operations)
- Category and brand management
- Banner/promotion management
- Order tracking and status updates
- Customer management
- Inventory tracking with low-stock alerts
- Analytics dashboard with sales insights
- Activity logging for audit trails

## 🛠️ Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Vite
- **Backend**: Supabase (PostgreSQL, Auth, Storage, Edge Functions)
- **Icons**: Lucide React
- **Deployment**: Bolt Hosting

## 📦 Database Schema

### Core Tables
- `categories` - Product categories with SEO fields
- `brands` - Brand information and metadata
- `products` - Complete product catalog with variants
- `customers` - Customer profiles and preferences
- `orders` - Order management with status tracking
- `banners` - Homepage banners and promotions

### Admin Tables
- `inventory_logs` - Stock movement tracking
- `admin_activity_logs` - Audit trail for admin actions

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Supabase account

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd jowhara-collection
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   VITE_SUPABASE_URL=https://tgquiihnjasgxenltzcd.supabase.co
   VITE_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InRncXVpaWhuamFzZ3hlbmx0emNkIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTgyODI4OTUsImV4cCI6MjA3Mzg1ODg5NX0.Tg-LU5GCufExbXEgRr9JIWNDDnGdRytPGuI0VPDizaY
   ```

4. **Set up the database**
   Run the migration file in your Supabase SQL editor:
   ```bash
   # Copy and execute the contents of supabase/migrations/create_complete_schema.sql
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Access the application**
   - Frontend: http://localhost:5000
   - Admin Panel: http://localhost:5000 (click the shield icon in header)

## 🔐 Admin Setup

To create an admin user:

1. **Sign up** through Supabase Auth (or create via Supabase dashboard)
2. **Set admin role** in Supabase dashboard:
   - Go to Authentication > Users
   - Find your user and edit
   - In "User Metadata" add: `{"role": "admin"}`
3. **Access admin panel** via the shield icon in the header

## 📱 Features Overview

### Customer Features
- Browse products by category and brand
- Advanced search and filtering
- Product details with images and specifications
- WhatsApp ordering integration
- Responsive design for all devices

### Admin Features
- **Dashboard**: Overview of sales, orders, and inventory
- **Products**: Full CRUD operations with image management
- **Categories**: Organize products with SEO optimization
- **Brands**: Manage brand information and logos
- **Orders**: Track and update order status
- **Banners**: Homepage promotion management
- **Analytics**: Sales insights and performance metrics

## 🔒 Security

- **Row Level Security (RLS)** enabled on all tables
- **Role-based access control** for admin functions
- **Input validation** and sanitization
- **Secure authentication** via Supabase Auth
- **Audit logging** for all admin actions

## 📊 Database Relationships

```
categories (1) ←→ (many) products
brands (1) ←→ (many) products
customers (1) ←→ (many) orders
products (many) ←→ (many) order_items
categories (1) ←→ (many) banners
```

## 🚀 Deployment

The application is configured for deployment on Bolt Hosting with automatic builds and deployments.

### Build Command
```bash
npm run build
```

### Environment Variables (Production)
Ensure all environment variables are set in your deployment platform.

## 📞 Support

For support and inquiries:
- **Phone**: +254 722 240558
- **Email**: info@jowhara.co.ke
- **WhatsApp**: Available 24/7

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is proprietary software owned by Jowhara Collection.

---

**Built with ❤️ for Jowhara Collection**