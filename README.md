🏏 IPL Match Winner Predictor – Full-Stack ML Web App
A full-stack web application that predicts the winner of an IPL cricket match based on user inputs using a trained machine learning model (Random Forest Classifier).

📂 Project Structure
bash
Copy
Edit
ipl-predictor/
├── backend/
│   ├── app.py                  # Flask backend with ML prediction route
│   └── model.pkl               # Trained Random Forest Classifier model
├── frontend/
│   └── src/
│       ├── App.js              # Main React component
│       └── components/
│           └── MatchForm.js    # React form for input fields
├── dataset/
│   └── IPL_matches_data.csv    # Processed dataset used for training
├── notebooks/
│   └── model_dev.ipynb         # EDA + Model training Jupyter Notebook
└── README.md
📊 Dataset
Dataset is based on past IPL matches with features like:

Teams playing (Team1, Team2)

Venue

Toss winner & decision

Match winner

You can customize or expand the dataset by downloading IPL match records and converting them into the same format used in IPL_matches_data.csv.

⚙️ Step-by-Step Implementation
✅ 1. Train the ML Model
Open the notebook:

bash
Copy
Edit
notebooks/model_dev.ipynb
Perform:

Exploratory Data Analysis (EDA)

Label Encoding of categorical variables

Model training (Random Forest Classifier)

Save the trained model using:

python
Copy
Edit
import joblib
joblib.dump(rf_model, '../backend/model.pkl')
✅ 2. Backend – Flask API
Navigate to the backend directory:

bash
Copy
Edit
cd backend
Install required dependencies:

bash
Copy
Edit
pip install flask pandas scikit-learn joblib
Run the Flask server:

bash
Copy
Edit
python app.py
API will be available at:

bash
Copy
Edit
http://localhost:5000/predict
✅ 3. Frontend – React UI
Navigate to the frontend directory:

bash
Copy
Edit
cd ../frontend
Create the React app (if not done already):

bash
Copy
Edit
npx create-react-app .
Replace default files with your components:

Update src/App.js

Add MatchForm.js inside src/components/

Install dependencies and run:

bash
Copy
Edit
npm install
npm run dev
Visit your app at:

arduino
Copy
Edit
http://localhost:3000
📥 Features Used for Prediction
team1: First team

team2: Second team

venue: Stadium/location of the match

toss_winner: Toss winning team

toss_decision: Bat or Bowl

🧠 Output
Predicts the winning team based on user-selected match conditions.

🚀 Tech Stack
Frontend: React.js

Backend: Flask

ML Model: Random Forest Classifier (scikit-learn)

Language: Python, JavaScript

Data Handling: Pandas, Numpy

📬 Contributions Welcome!
Suggestions and contributions are encouraged, including:

Improving model accuracy

Adding real-time match data fetching

Deploying the app on platforms like Heroku or Vercel

Enhancing the frontend UI/UX
