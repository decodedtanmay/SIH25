# 🌍 SIH25 - Smart India Hackathon 2025

An innovative solution developed for Smart India Hackathon 2025. This project addresses critical challenges through a modern, scalable web application combining emergency response systems with real-time data processing.

## 📋 Problem Statement

This project was developed as part of Smart India Hackathon 2025 to solve critical challenges in emergency management and disaster response systems through intelligent automation and real-time monitoring.

## ✨ Features

### 🎯 Core Functionality
- Intelligent emergency detection and analysis
- Real-time data processing and visualization
- User-friendly dashboard for monitoring
- Automated reporting system
- Scalable architecture for large-scale deployment

### 📊 Dashboard & Analytics
- Real-time data visualization
- Key performance indicators (KPIs)
- Historical data analysis
- Predictive insights
- Custom report generation

### 👥 User Management
- Role-based access control
- Multi-level user hierarchy
- User activity tracking
- Permission management
- Team collaboration features

### 🔐 Security & Compliance
- End-to-end data encryption
- Secure authentication
- Audit trails
- GDPR compliance
- Data backup and recovery

## 🛠️ Tech Stack

- **Frontend**: React 18 + TypeScript / Next.js
- **Backend**: Node.js with Next.js API Routes
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: JWT + OAuth
- **Styling**: TailwindCSS
- **Deployment**: Vercel
- **Real-time**: WebSocket/Socket.io

## 🚀 Quick Start

### Prerequisites
- Node.js (v18+)
- PostgreSQL database
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/decodedtanmay/SIH25.git
cd SIH25

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env.local

# Setup database
npm run db:setup

# Run migrations
npm run db:migrate
```

### Development

```bash
# Start development server
npm run dev

# Application will be available at http://localhost:3000
```

### Build

```bash
# Build for production
npm run build

# Start production server
npm start
```

## 📁 Project Structure

```
SIH25/
├── emergent/                   # Emergency management module
│   ├── frontend/              # React frontend
│   │   ├── public/
│   │   ├── src/
│   │   ├── package.json
│   │   └── README.md
│   └── backend/               # Node.js backend
├── src/
│   ├── app/                   # Next.js app directory
│   │   ├── api/              # API routes
│   │   ├── components/       # React components
│   │   ├── pages/            # Page components
│   │   └── layout.tsx
│   ├── lib/                  # Utility functions
│   ├── hooks/                # Custom hooks
│   ├── types/                # TypeScript types
│   └── styles/               # Global styles
├── prisma/
│   ├── schema.prisma        # Database schema
│   └── migrations/          # Database migrations
├── public/                   # Static assets
├── docs/                     # Documentation
│   ├── DATABASE_SETUP.md
│   ├── API.md
│   └── ARCHITECTURE.md
├── .env.example              # Environment template
├── package.json
├── tsconfig.json
├── next.config.ts
└── README.md
```

## 🔑 Environment Variables

Create `.env.local`:

```env
# Database
DATABASE_URL=postgresql://user:password@localhost:5432/sih25

# Authentication
JWT_SECRET=your_jwt_secret_here
NEXTAUTH_SECRET=your_nextauth_secret

# API Configuration
API_URL=http://localhost:3000
NEXT_PUBLIC_API_URL=http://localhost:3000

# OAuth (if applicable)
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

## 💾 Database Setup

### Initialize Database

```bash
# Create database
npm run db:create

# Run migrations
npm run db:migrate

# Seed initial data (if available)
npm run db:seed
```

### Database Schema

Key tables and relationships are defined in `prisma/schema.prisma`.

View [DATABASE_SETUP.md](./DATABASE_SETUP.md) for detailed schema documentation.

## 📊 API Documentation

Comprehensive API documentation available in [API.md](./docs/API.md)

### Example API Endpoints

```
GET    /api/emergencies       # Fetch emergencies
POST   /api/emergencies       # Create new emergency
PUT    /api/emergencies/:id   # Update emergency
DELETE /api/emergencies/:id   # Delete emergency
GET    /api/analytics         # Get analytics
```

## 🎯 Key Features In Detail

### Real-Time Processing
- Stream processing for live data
- Instant notifications
- Live dashboard updates
- Queue-based task processing

### Scalability
- Horizontal scaling support
- Database connection pooling
- Caching strategies
- Load balancing ready

### Performance
- Code splitting
- Image optimization
- Database query optimization
- API response caching

### User Experience
- Intuitive interface
- Responsive design
- Accessibility compliance
- Multi-language support

## 🔐 Security Features

- Password hashing with bcrypt
- SQL injection prevention
- CORS configuration
- Rate limiting
- Input validation and sanitization
- XSS protection

## 🧪 Testing

```bash
# Run unit tests
npm run test

# Run integration tests
npm run test:integration

# Run e2e tests
npm run test:e2e

# Generate coverage report
npm run test:coverage
```

## 📈 Performance Monitoring

- Application Performance Monitoring (APM)
- Error tracking
- Database query profiling
- API response time monitoring
- User analytics

## 🚀 Deployment

### Deploy to Vercel

```bash
# Connect GitHub repository to Vercel dashboard
# Or use Vercel CLI
vercel deploy --prod
```

### Manual Deployment

```bash
# Build application
npm run build

# Deploy to your server
# Copy build files to your hosting provider
```

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Follow code style guidelines
4. Write tests for new features
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## 📚 Documentation

- [Database Setup Guide](./DATABASE_SETUP.md)
- [API Documentation](./docs/API.md)
- [Architecture Overview](./docs/ARCHITECTURE.md)
- [Contributing Guide](./CONTRIBUTING.md)

## 🏆 Smart India Hackathon 2025

This project was developed as part of **Smart India Hackathon 2025** - a national hackathon promoting innovation in governance and public services.

- **Hackathon Website**: [SIH 2025](https://www.sih.gov.in)
- **Team**: Collaborative effort by innovative developers

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Authors

**Team Members**:
- Tanmay - [GitHub Profile](https://github.com/decodedtanmay)
- Arnav - [GitHub Profile](https://github.com/Arnavcloud0412)

## 🙏 Acknowledgments

- Smart India Hackathon organizing committee
- Problem statement providers
- React and Next.js communities
- Prisma for excellent ORM
- PostgreSQL community

## 📞 Support & Feedback

Have questions or suggestions?
- Open an [Issue](https://github.com/decodedtanmay/SIH25/issues)
- Check [Documentation](./docs)
- Contact via GitHub

## 🔗 Links

- **GitHub Repository**: https://github.com/decodedtanmay/SIH25
- **Parent Repository**: https://github.com/Arnavcloud0412/SIH25

---

**⭐ If you find this project useful, please give it a star!**

Developed with innovation and excellence for Smart India Hackathon 2025
