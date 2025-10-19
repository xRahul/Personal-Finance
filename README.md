# Personal Finance Dashboard

A comprehensive, production-ready finance management application for managing Kotak Mahindra Bank statements and Zerodha holdings.

## 🚀 Quick Start

```bash
# 1. Extract
unzip finance-dashboard-complete.zip
cd finance-dashboard

# 2. Configure (optional - defaults work)
cp .env.example .env

# 3. Run with Docker
docker-compose up --build

# 4. Access
# Frontend: http://localhost:3000
# API Docs: http://localhost:8000/docs

# 5. Login
# Username: admin
# Password: admin123
```

## ✨ Features

- **PDF Parser**: Extracts transactions from Kotak Mahindra Bank statements
- **CSV Parser**: Imports Zerodha holdings data
- **SQLite Database**: Local data storage
- **React Dashboard**: Interactive UI with charts
- **REST API**: FastAPI backend with Swagger docs
- **Authentication**: Secure basic auth
- **Docker Ready**: One-command deployment
- **Unit Tests**: Comprehensive test coverage
- **Modular**: Easy to extend with new data sources

## 📁 Project Structure

```
finance-dashboard/
├── backend/          # Python/FastAPI backend
│   ├── app/
│   │   ├── models/   # Database models
│   │   ├── parsers/  # PDF/CSV parsers
│   │   └── routers/  # API endpoints
│   └── tests/        # Unit tests
├── frontend/         # React frontend
│   └── src/
│       └── components/
└── docker-compose.yml
```

## 🔧 Local Development

### Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

### Tests
```bash
cd backend
pytest tests/ -v --cov=app
```

## 📊 Usage

1. **Upload Bank Statement**: Upload Kotak PDF in Upload section
2. **Import Holdings**: Upload Zerodha CSV file
3. **View Dashboard**: Analyze transactions and portfolio

## 🔐 Security

- Basic authentication on all API endpoints
- CORS configuration
- Environment-based secrets
- Input validation

## 🎯 Adding New Banks/Brokers

1. Create parser in `backend/app/parsers/`
2. Inherit from `BaseParser`
3. Implement `parse()` and `validate()`
4. Add router endpoint
5. Update frontend

## 📄 License

MIT License

## 🙏 Acknowledgments

Built with FastAPI, React, SQLite, Docker, and modern best practices.
