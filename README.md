# 💅🏽 Color Psychic

<div align="center">✦ Turn “I don't know what colour I want” into a confident choice. ✦

A personalised nail-polish recommendation system powered by collaborative filtering.

<br>"Client History" → "Preference Patterns" → "Similar Clients" → "Recommendations"

</div>---

🌸 The Problem

«“I don't know what colour I want.”»

It sounds simple, but this question can take several minutes to resolve for each client.

At Exquisite Bliss Boutique, the goal is to use data to make that decision faster while still keeping the recommendation personal.

Instead of randomly suggesting colours, Color Psychic learns from previous client choices and identifies patterns in what clients with similar preferences have selected.

---

🔮 What Color Psychic Does

Color Psychic recommends 3 nail-polish colours for a client based on two sources of information:

- 💅🏽 The client's own history — colours they have previously chosen
- 👯 Similar clients — colours chosen by clients with comparable preferences

The system then combines these signals to produce a personalised shortlist of three recommendations.

Example

A client has previously chosen:

"Nude" · "Chrome" · "Burgundy"

Clients with similar preferences frequently choose:

"Rose Gold" · "French White" · "Mocha"

Color Psychic can use these patterns to recommend:

«1. Rose Gold
2. Mocha
3. French White»

The aim is not to tell the client what they must choose.

It gives them a starting point that is relevant to their preferences.

---

🧠 Recommendation Approach

Color Psychic uses Collaborative Filtering.

The system learns from interactions between:

Clients ↔ Nail Colours

Rather than relying only on the properties of a colour, the recommender looks for behavioural patterns.

The basic idea

Client A
   │
   ├── Nude
   ├── Chrome
   └── Burgundy
          │
          ▼
   Find similar clients
          │
          ▼
   Analyse their choices
          │
          ▼
   Rank candidate colours
          │
          ▼
   💅 Top 3 Recommendations

This allows the system to discover relationships that may not be obvious from the colour names alone.

---

📊 Data

The recommendation engine can work with historical booking data containing information such as:

Field| Description
"client_id"| Unique client identifier
"polish_colour"| Colour selected
"booking_date"| Date of appointment
"service_type"| Type of nail service
"purchase_count"| Number of times the colour was selected

Additional features can be introduced as the dataset grows.

---

⚙️ How It Works

1. Collect

Historical client and polish-selection data is collected from previous appointments.

2. Build the Interaction Matrix

Client-colour interactions are transformed into a matrix.

                 Nude   Chrome   Burgundy   Mocha   Rose Gold
Client 001         1       1         1        0         0
Client 002         1       0         1        1         0
Client 003         0       1         0        1         1

3. Find Similar Clients

The system identifies clients whose historical colour choices are similar.

4. Generate Candidates

Colours selected by similar clients become potential recommendations.

5. Rank

Candidate colours are scored according to the recommendation model.

6. Recommend

The system returns the Top 3 colours that the client has not recently selected.

---

🛠️ Technology Stack

Technology| Purpose
🐍 Python| Core development
🐼 Pandas| Data preparation
🔢 NumPy| Numerical operations
🤖 Scikit-learn| Similarity & recommendation modelling
📊 Matplotlib| Data visualisation
🎨 Streamlit| Interactive recommendation interface

---

📈 Evaluation

The recommender can be evaluated using recommendation-system metrics such as:

- Precision@K
- Recall@K
- Hit Rate@K
- Recommendation Coverage

For this project, K = 3, because the system is designed to provide three practical colour options.

---

💻 Example Interface

The final application can allow a user to select a client and receive:

╭──────────────────────────────────────╮
│          🔮 COLOR PSYCHIC            │
│                                      │
│  Client: Client 001                  │
│                                      │
│  Based on your colour history...     │
│                                      │
│  💅 Rose Gold                        │
│  💅 Mocha                            │
│  💅 French White                     │
│                                      │
│  ✦ Your next colour might be here.  │
╰──────────────────────────────────────╯

---

🎯 Business Value

Color Psychic is designed to help Exquisite Bliss Boutique:

⏱ Reduce decision time
Give clients relevant options without starting from zero.

💅 Personalise the experience
Recommendations are influenced by the client's own history.

📊 Use customer data intelligently
Turn appointment history into actionable insights.

✨ Discover client preferences
Identify colour patterns that may otherwise be difficult to see.

📈 Support future business decisions
Recommendation data can eventually help inform polish inventory and promotional decisions.

---

🚀 Future Improvements

Color Psychic can evolve beyond basic collaborative filtering.

Possible future additions include:

- 🎨 Colour-family similarity
- 📅 Seasonal recommendations
- 🔥 Trending-colour detection
- 💰 Revenue-weighted recommendations
- 📱 Instagram engagement signals
- 🧠 Hybrid recommendation models
- 👤 New-client recommendations using onboarding preferences
- 📊 Recommendation analytics dashboard

A future hybrid recommender could combine:

Collaborative Filtering
          +
Colour Characteristics
          +
Client Preferences
          +
Seasonal Trends
          ↓
   Personalised Recommendation

---

🌱 Project Philosophy

Color Psychic demonstrates how data science can solve a small, everyday business problem.

The objective isn't simply to build a recommendation algorithm.

It is to take a familiar customer interaction —

«“I don't know what colour I want.”»

—and transform it into a data-driven experience that helps the client make a decision more easily.

---

<div align="center">💅🏽 Data → Patterns → Personalisation → Better Decisions

Color Psychic

An Exquisite Bliss Boutique Data Science Project

</div>