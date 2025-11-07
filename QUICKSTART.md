# Quick Start Guide

Get the AI Wiki Quiz Generator up and running in 5 minutes!

## Prerequisites Check

- [ ] Python 3.10+ installed (`python --version`)
- [ ] Node.js 18+ installed (`node --version`)
- [ ] Gemini API Key (get from https://makersuite.google.com/app/apikey)

## Step 1: Backend Setup (2 minutes)

```bash
# Navigate to backend
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
# Copy the content below and paste into a new file named .env
```

Create `backend/.env` file:
```env
GEMINI_API_KEY=your_api_key_here
DATABASE_URL=sqlite:///./quiz_history.db
```

```bash
# Start backend server
uvicorn main:app --reload
```

Backend should now be running at `http://localhost:8000`

## Step 2: Frontend Setup (2 minutes)

Open a **new terminal**:

```bash
# Navigate to frontend
cd frontend

# Install dependencies
npm install

# Start frontend server
npm run dev
```

Frontend should now be running at `http://localhost:5173`

## Step 3: Test It! (1 minute)

1. Open browser to `http://localhost:5173`
2. Enter a Wikipedia URL: `https://en.wikipedia.org/wiki/Alan_Turing`
3. Click "Generate Quiz"
4. Wait for the magic! ✨

## Troubleshooting

### Backend won't start
- Check if port 8000 is available
- Verify `.env` file exists with `GEMINI_API_KEY`
- Ensure virtual environment is activated

### Frontend won't start
- Check if port 5173 is available
- Run `npm install` again
- Check Node.js version: `node --version`

### API errors
- Verify backend is running on port 8000
- Check browser console for CORS errors
- Verify API key is valid

### Database errors
- SQLite is used by default (no setup needed)
- For PostgreSQL/MySQL, update `DATABASE_URL` in `.env`

## Next Steps

- Try different Wikipedia articles
- Check the History tab to see all generated quizzes
- View API documentation at `http://localhost:8000/docs`

Enjoy generating quizzes! 🎓

