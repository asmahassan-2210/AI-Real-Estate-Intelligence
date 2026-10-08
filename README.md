# 1. Clone the repository
git clone https://github.com/<your-username>/ai-real-estate-platform.git
cd ai-real-estate-platform

# 2. Set up virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install required dependencies
pip install -r requirements.txt

# 4. Set up environment variables
cp .env.example .env
# Open .env and add your OPENAI_API_KEY

# 5. Train the Machine Learning model
python -m src.model_trainer

# 6. Start the FastAPI server
uvicorn app.main:app --reload