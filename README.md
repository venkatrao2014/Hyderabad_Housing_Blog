# Hyderabad_Housing_Blog
# 🏙️ Analyzing Rental Housing Trends in Hyderabad with Gen AI

*By Venkat & Deepika | April 2025*

---

## 👋 Introduction

As part of the 5-day Gen AI Intensive Course with Google, we explored a real-world use case: analyzing rental housing data in Hyderabad.

Our goal was simple — can we use data to understand housing trends and affordability? Can we combine traditional data science with generative AI to make it even better?

This blog walks you through how we approached the problem, what we discovered, and how Gen AI helped us break down the data in smarter ways.

---

## 🧠 The Idea Behind the Project

Hyderabad has seen rapid urban growth, and housing has become both a necessity and a challenge. We wanted to answer questions like:

- Are rents in Hyderabad affordable for an average income earner?
- How have occupancy rates changed over time?
- Can we create a smart summary of listings using Gen AI?

We used a JSON dataset of rental listings and used Python (Pandas, Matplotlib, Seaborn) for analysis. We also integrated mock examples of Gen AI capabilities like structured summarization, prompt-based classification, and affordability analysis.

---

## 📊 What We Did

### 🧹 1. Cleaned the Data

We began by loading the JSON file into a pandas DataFrame. Some of the columns were messy — missing values, wrong formats — so we:

- Converted numeric columns like `avg_rent`, `occupied_units` to floats
- Dropped rows with critical missing values
- Renamed confusing column names for clarity

### 📈 2. Explored Trends Visually

We plotted key trends:

- A **scatter plot** of average rent vs occupied units showed us where affordability may be affecting occupancy
- A **bar chart** comparing total vs occupied units by year helped us track housing trends over time
- A **heatmap** of correlations showed strong links between low-income units and rent levels

### 💸 3. Checked Rent Affordability

We assumed an average monthly income of ₹50,000. Using this, we computed:

- **Rent-to-income ratio** for each listing
- Marked listings as "affordable" if rent was below 30% of income
- Visualized the rent burden with a histogram

We found that quite a few listings were above the affordability threshold — a concerning insight for lower-income groups.

---

## 🧪 How Gen AI Was (or Could Be) Used

We integrated and mocked Gen AI capabilities in the following ways:

- **Structured Output**: Summarized rental listings into clean, readable formats (e.g., "Area, Rent, AC, Pets Allowed, Near Metro")
- **Prompt-based Affordability Classifier**: Used a language model to label whether a listing was affordable or not, based on custom criteria
- **Few-shot Prompting**: Simulated how the model could classify listings with a few examples

Although some of this was mocked (due to the static dataset), the structure shows how we could plug in a real LLM API or tool.

---

## 💡 Key Takeaways

- **Data speaks** — rents and affordability vary across the city and over time
- **Visualization makes it easier** to spot patterns and insights
- **AI enhances analysis** — Gen AI can help simplify complex data for users in real-time

---

## 🎯 Final Thoughts

This project gave us a deeper understanding of how Gen AI and data science can work together. Whether it’s a chatbot for real estate advice, or an assistant summarizing rental listings, the potential is huge.

And it all starts with clean data and curious questions.

Thanks for reading! 😊

---

*Project by Venkat & Deepika, BTech students exploring the intersection of data and Gen AI.*
