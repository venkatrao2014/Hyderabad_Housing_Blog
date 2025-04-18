🧠 Finding the Perfect Rental in Hyderabad — with a Little Help from GenAI 🏠💬
“I need a 2 BHK under ₹15,000, with AC, near the metro... and I want to bring my dog.”
Sounds familiar?

If you've ever tried finding a rental online, you know the pain: endless scrolling, clunky filters, listings that feel like they were written by bots, and no way to ask what you really want.

So I decided to change that—with a dash of GenAI, some NLP magic, and good ol' data science.

This blog takes you through how I built a semantic search engine for Hyderabad rentals, powered by transformer models and human-centered data design. Let’s dive in!

🎯 Why This Project?
Real estate platforms usually offer filters like:

Number of BHKs

Price range

Location

But renters often think in natural language:

“I need something spacious for my pets, maybe near Jubilee Hills, and within ₹12k. AC would be great.”

I wanted to make a system that understands these kinds of queries and returns listings that make sense, not just listings that match checkboxes.

🗂️ Step 1: Understanding the Raw Data
I used a dataset scraped from housing platforms in Hyderabad. Here’s a glimpse of what we started with:

📍 Location info

🛏️ Property type (1 BHK, 2 BHK, etc.)

🧾 Rent details

📦 Furnishing, amenities (AC, gym, pool, pets allowed, etc.)

🏢 Floor and size

📝 Property title (a short, often messy description)

The data was rich, but noisy. So I rolled up my sleeves and got to work.

🛠️ Step 2: Cleaning, Enriching, and Engineering Features
Before we could search semantically, we had to teach the machine what it’s looking at. Here's what I did:

🔍 Data Cleaning
Removed missing values and irrelevant fields

Standardized column names and fixed typos

Converted rent and deposit columns to numeric values

🧠 Feature Engineering
Parsed rent from messy titles like "2 BHK for ₹13000 near metro"

Created new columns:

pets_allowed

has_ac

near_metro

Calculated rent-to-income ratio based on an assumed average salary (₹50,000/month)

Created description columns that summarize the listing like:

“2 BHK in Madhapur, ₹13,000/month, semi-furnished, AC, pets allowed, floor 2 of 5”

This served as a foundation for semantic understanding.

📊 Step 3: Visualizing the Market
To understand the dynamics of the rental market, I created a few visualizations:

Histogram of rental prices: showed that most listings cluster around ₹10,000–₹20,000

Scatter plot of rent vs. property size: helped spot overpriced listings

Correlation heatmap: revealed that floor number and amenities had little impact on price compared to size and location

Affordability analysis: tagged listings as “affordable” based on income thresholds

These helped validate assumptions and informed the design of search filters later.

🤖 Step 4: Bringing in GenAI — Semantic Search
Now for the fun part.

Using sentence-transformers, I encoded each listing into a vector using the "paraphrase-MiniLM-L6-v2" model—a lightweight, high-performance transformer perfect for this kind of task.

How it works:
Each listing is transformed into a 384-dimensional vector (its "semantic fingerprint").

The user query is also transformed into a vector.

We compute cosine similarity between the query and every listing.

Return the top matches, sorted by how well they mean the same thing—even if the wording differs.

Example:
User query:

“I want a cheap place under ₹10,000 with AC, near a metro, pet-friendly.”

Even if listings don’t say “cheap” or “pet-friendly” explicitly, the model can infer meaning from phrases like:

“budget-friendly”

“pets allowed”

“close to metro station”

No exact matches? No problem. GenAI’s got your back.

🧾 Step 5: Building a Human-Readable Summary
To make results more user-friendly, I generated structured outputs:

markdown
Copy
Edit
🏡 **Area**: Kukatpally  
💰 **Rent**: ₹9,500/month  
🐶 **Pets Allowed**: Yes  
❄️ **AC**: Yes  
🚇 **Near Metro**: Yes  
📝 **Description**: 1 BHK in Kukatpally, ₹9500/month, unfurnished, AC, pets allowed, floor 1 of 3.
This can easily plug into:

A chatbot

A search assistant

A recommendation engine

It’s how you bridge data and conversation.

🧪 GenAI Capabilities Demonstrated
✅ Natural Language Processing
Turned messy listing text into structured, searchable data

✅ Semantic Embeddings
Understood "meaning" behind free-text queries using sentence transformers

✅ Vector Search
Ranked listings based on similarity to user intent, not keywords

✅ Explainability
Results came with structured descriptions so users know why something was shown

✅ Personalization Ready
With small tweaks, it can support user profiles and dynamic re-ranking

🔮 Where This Can Go
This is just the beginning. Here are ideas to take it further:

🧭 Geospatial search: sort by proximity to schools, hospitals, offices

🧑‍💻 ChatGPT plugin or LangChain agent to have real conversations

🎯 User profiles: show better results over time using interaction data

🧼 Data pipeline: auto-clean and update listings from real-time APIs

🎛️ Streamlit dashboard: create a GUI where users can test natural queries live

🧩 Tech Stack

Tool	Purpose
Python	Core language
Pandas	Data wrangling
Matplotlib / Seaborn	Visualizations
SentenceTransformers	Embeddings
Scikit-learn	Similarity scoring
Jupyter	Notebook development
📌 Final Thoughts
This project was a blast to work on—and it's a great demonstration of how GenAI can make traditional workflows 10x more intuitive.

We went from:

Static filters + messy listings
To:
Meaningful, conversational, semantically smart housing discovery

If you're a student, data scientist, or product builder curious about applying LLMs to real-world use cases, start here. It's a perfect blend of NLP, product thinking, and user empathy.

🙌 Let’s Connect
If you found this helpful or want to collaborate on building this into a live app, I’d love to hear from you! Fork the repo, open an issue, or shoot me a message.
