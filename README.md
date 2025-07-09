# LawAI-SIH 🏛️⚖️

**Smart India Hackathon 2024 - Legal AI Solution**

A comprehensive AI-powered legal assistance platform that leverages Natural Language Processing (NLP) and Machine Learning to help law enforcement personnel identify applicable laws and regulations for FIR cases. The system provides intelligent case analysis, legal database integration, and real-time case monitoring capabilities.

## 🌟 Overview

LawAI-SIH is an innovative web application designed to bridge the gap between incident reporting and legal framework application. It utilizes Google's Gemini AI model to analyze FIR details and automatically identify relevant legal provisions, making the legal process more efficient and accessible for law enforcement agencies.

## 🏗️ Architecture

### Frontend Architecture
```
Frontend/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── Footer.js
│   │   ├── KeyFeatures.js
│   │   ├── MenuBar.js
│   │   └── Sidebar.js
│   ├── pages/              # Application pages
│   │   ├── Landing.js      # Landing page
│   │   ├── Query.js        # AI Query interface
│   │   ├── Database.js     # Case database
│   │   ├── BareActs.js     # Legal acts repository
│   │   ├── Download.js     # Document downloads
│   │   └── ...
│   ├── styles/             # CSS modules
│   ├── images/             # Static assets
│   └── contexts/           # React Context providers
```

### Backend Architecture
```
Backend/
├── index.js               # Main server entry point
├── gemini.js             # Google Gemini AI integration
├── server.js             # MongoDB operations
├── laws.js               # Legal database routes
├── laws.json             # Legal acts data
└── vercel.json           # Deployment configuration
```

## 🚀 Key Features

### 🤖 AI-Powered Legal Analysis
- **Gemini AI Integration**: Utilizes Google's Gemini 1.5 Flash model for intelligent FIR analysis
- **Natural Language Processing**: Interprets incident details and maps them to relevant legal provisions
- **Contextual Understanding**: Provides detailed explanations of applicable laws and sections

### 📊 Comprehensive Database Management
- **MongoDB Integration**: Robust NoSQL database for case management
- **Real-time Data**: Live updates and case tracking capabilities
- **Search Functionality**: Advanced search by act, section, keyword, or case details

### 🎨 Modern User Interface
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Dark/Light Mode**: Customizable theme support
- **Accessibility**: WCAG compliant design with screen reader support
- **Progressive Web App**: PWA capabilities for mobile installation

### 🔊 Voice Integration
- **Speech Recognition**: Voice-to-text input for FIR details
- **Multilingual Support**: Support for multiple Indian languages
- **Hands-free Operation**: Voice commands for better accessibility

### 📄 Document Management
- **PDF Generation**: Automated FIR and case report generation using jsPDF
- **Download Center**: Centralized document download hub
- **Template System**: Standardized legal document templates

## 🛠️ Technology Stack

### Frontend Technologies
| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18.3.1 | Frontend framework |
| **React Router DOM** | 6.26.1 | Client-side routing |
| **Tailwind CSS** | 3.4.10 | Utility-first CSS framework |
| **Framer Motion** | 11.5.6 | Animation library |
| **Axios** | 1.7.7 | HTTP client |
| **React Icons** | 5.3.0 | Icon library |
| **jsPDF** | 2.5.2 | PDF generation |
| **Recharts** | 2.12.7 | Data visualization |
| **PowerBI Client** | 2.23.1 | Business intelligence integration |

### Backend Technologies
| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | Latest | Runtime environment |
| **Express.js** | 4.21.0 | Web framework |
| **MongoDB** | 6.9.0 | NoSQL database |
| **Google Generative AI** | 0.20.0 | AI/ML integration |
| **CORS** | 2.8.5 | Cross-origin resource sharing |
| **dotenv** | 16.4.5 | Environment variable management |

### DevOps & Deployment
- **Vercel**: Frontend deployment platform
- **MongoDB Atlas**: Cloud database hosting
- **Environment Variables**: Secure configuration management
- **Git**: Version control system

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- **Node.js** (v16.0.0 or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local installation or MongoDB Atlas account)
- **Google Gemini API Key**
- **Git** for version control

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/LawAI-SIH.git
cd LawAI-SIH
```

### 2. Backend Setup
```bash
cd Backend
npm install
```

Create a `.env` file in the Backend directory:
```env
api_key=your_google_gemini_api_key
mongouri=your_mongodb_connection_string
PORT=5000
```

### 3. Frontend Setup
```bash
cd ../Frontend
npm install
```

### 4. Start the Development Servers

**Backend Server:**
```bash
cd Backend
npm start
# Server runs on http://localhost:5000
```

**Frontend Server:**
```bash
cd Frontend
npm start
# Application runs on http://localhost:3000
```

## 🔧 Configuration

### Environment Variables

#### Backend (.env)
```env
# Google Gemini AI Configuration
api_key=your_google_gemini_api_key

# MongoDB Configuration
mongouri=mongodb+srv://username:password@cluster.mongodb.net/FIR

# Server Configuration
PORT=5000
NODE_ENV=development
```

#### Frontend Environment Variables (Optional)
Create `.env` in Frontend directory for any client-side configurations:
```env
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_ENV=development
```

## 📱 Usage Guide

### 1. Landing Page
- Navigate to the application homepage
- Explore key features and system overview
- Access navigation menu for different modules

### 2. Query Module
- Enter FIR details in natural language
- Use voice input for hands-free operation
- Receive AI-generated legal analysis
- View applicable laws and sections

### 3. Database Module
- Browse existing cases and FIRs
- Search by various criteria
- Monitor case status and updates
- Generate reports and analytics

### 4. Legal Acts Repository
- Access comprehensive legal database
- Search by act name, section, or keywords
- Download legal documents
- View categorized legal provisions

## 🔌 API Endpoints

### Gemini AI Routes
```
POST /api/gemini/generate
- Body: { "query": "FIR details or legal question" }
- Response: AI-generated legal analysis
```

### MongoDB Routes
```
GET /api/server/cases
- Response: List of all cases from database

GET /api/server/
- Response: API welcome message
```

### Legal Database Routes
```
GET /api/laws/
- Response: Available legal acts and sections

POST /api/laws/search
- Body: Search parameters
- Response: Filtered legal provisions
```

## 🏗️ Project Structure

```
LawAI-SIH/
│
├── README.md                 # Project documentation
│
├── Frontend/                 # React frontend application
│   ├── public/              # Static assets
│   │   ├── index.html       # HTML template
│   │   ├── favicon.ico      # Application favicon
│   │   └── manifest.json    # PWA manifest
│   │
│   ├── src/                 # Source code
│   │   ├── components/      # Reusable components
│   │   │   ├── Footer.js
│   │   │   ├── KeyFeatures.js
│   │   │   ├── MenuBar.js
│   │   │   └── Sidebar.js
│   │   │
│   │   ├── pages/           # Application pages
│   │   │   ├── Landing.js   # Home page
│   │   │   ├── Query.js     # AI query interface
│   │   │   ├── Database.js  # Case database
│   │   │   ├── BareActs.js  # Legal repository
│   │   │   └── ...
│   │   │
│   │   ├── styles/          # CSS modules
│   │   ├── images/          # Image assets
│   │   ├── App.js           # Main application component
│   │   └── index.js         # Application entry point
│   │
│   ├── package.json         # Dependencies and scripts
│   └── tailwind.config.js   # Tailwind configuration
│
├── Backend/                 # Node.js backend server
│   ├── index.js            # Server entry point
│   ├── gemini.js           # Gemini AI integration
│   ├── server.js           # MongoDB operations
│   ├── laws.js             # Legal database routes
│   ├── laws.json           # Legal acts data
│   ├── package.json        # Backend dependencies
│   └── vercel.json         # Deployment configuration
│
└── .gitignore              # Git ignore rules
```

## 🚀 Deployment

### Frontend Deployment (Vercel/Netlify)
```bash
cd Frontend
npm run build
# Deploy the 'build' folder to your hosting platform
```

### Backend Deployment (Vercel)
```bash
cd Backend
# Configure vercel.json (already included)
vercel --prod
```

### Environment Setup for Production
- Set up MongoDB Atlas cluster
- Configure Google Cloud Console for Gemini API
- Set environment variables in hosting platform
- Update CORS settings for production domains

## 🔒 Security Features

- **API Key Protection**: Environment variables for sensitive data
- **CORS Configuration**: Controlled cross-origin access
- **Input Validation**: Sanitized user inputs
- **Secure Headers**: HTTP security headers implementation
- **Rate Limiting**: API request throttling (recommended for production)

## 🧪 Testing

### Frontend Testing
```bash
cd Frontend
npm test                    # Run unit tests
npm run test:coverage      # Generate coverage report
```

### Backend Testing
```bash
cd Backend
npm test                   # Run API tests
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow React best practices and hooks patterns
- Use Tailwind CSS for styling consistency
- Implement proper error handling
- Add comprehensive comments for complex logic
- Ensure mobile responsiveness
- Test across different browsers

## 🐛 Troubleshooting

### Common Issues

**1. MongoDB Connection Error**
```bash
Error: MongoDB URI is not defined
Solution: Check your .env file and MongoDB connection string
```

**2. Gemini API Error**
```bash
Error: Failed to generate response
Solution: Verify your Google Gemini API key and quota
```

**3. CORS Error**
```bash
Solution: Ensure backend CORS is configured for your frontend domain
```

**4. Build Errors**
```bash
Solution: Delete node_modules and package-lock.json, then run npm install
```

## 📊 Performance Optimization

- **Code Splitting**: Lazy loading for route components
- **Image Optimization**: Compressed and responsive images
- **Caching Strategy**: Browser and server-side caching
- **Bundle Analysis**: Webpack bundle analyzer integration
- **CDN Integration**: Static asset delivery optimization

## 🔮 Future Roadmap

- [ ] Multi-language support for regional languages
- [ ] Machine learning model training for case predictions
- [ ] Integration with government legal databases
- [ ] Real-time collaboration features
- [ ] Advanced analytics and reporting
- [ ] Mobile application development
- [ ] Blockchain integration for case integrity
- [ ] AI-powered legal document drafting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

**Smart India Hackathon 2024 Team**
- **Team Lead**: [Your Name]
- **Frontend Developer**: [Team Member]
- **Backend Developer**: [Team Member]
- **AI/ML Engineer**: [Team Member]
- **UI/UX Designer**: [Team Member]

## 🙏 Acknowledgments

- **Google Gemini AI** for providing advanced AI capabilities
- **MongoDB** for robust database solutions
- **Smart India Hackathon** for the platform and opportunity
- **Government of India** for supporting innovation in legal technology
- **Open Source Community** for the amazing tools and libraries

## 📞 Support

For support, email your-email@domain.com or create an issue in the repository.

## 🔗 Links

- **Live Demo**: [https://your-app-url.vercel.app](https://your-app-url.vercel.app)
- **API Documentation**: [API Docs](https://your-api-docs-url.com)
- **Design System**: [Figma Design](https://figma.com/your-design)
- **Project Repository**: [GitHub](https://github.com/yourusername/LawAI-SIH)

---

**Made with ❤️ for Smart India Hackathon 2024**

*Empowering Legal Professionals with AI Technology*
