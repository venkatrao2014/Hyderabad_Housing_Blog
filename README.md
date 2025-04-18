Navigating the Rental Housing Market in Hyderabad: My Data Journey
Hey there! 👋
Have you ever wondered what’s really going on with rental prices in a city like Hyderabad? How affordable are those cozy apartments we dream of? 🤔 Well, I decided to dive into this very topic for my capstone project in the Google Gen AI Intensive Course 2025. In this post, I’ll take you through my journey of exploring Hyderabad's rental housing market through data. Grab a cup of coffee ☕ and let’s get started!

The Problem: Affordable Housing is a Puzzle 🧩
With Hyderabad rapidly growing, rental prices are becoming a big topic of discussion. It's not just about how much rent you pay but also about how much of your paycheck gets spent on housing. Are rentals in Hyderabad affordable, or is everyone just scraping by? 🤷‍♂️

That’s the question I set out to answer by analyzing rental prices, occupancy rates, and affordability—using data to uncover the truth. And I have to say, it’s been quite a ride! 🎢

Getting the Data: All About That Info 📊
The first step was grabbing the data. I got my hands on some housing listings for Hyderabad, and it had everything you’d need to understand the rental market: the number of units, occupied units, rental prices, and more. But here’s the thing—this data came in JSON format. Not a big deal, though; I was ready to dive in and clean it up.

Here’s what I did:

Loaded the Data: I imported everything into a pandas DataFrame (basically a spreadsheet for Python!).

Cleaned it Up: A lot of the columns had missing or non-numeric values, so I had to clean them up to ensure the analysis would work properly.

Filtered Out the Noise: I focused on the columns that were most useful for the analysis like total units, occupied units, low-income units, and of course, average rent.

Exploratory Data Analysis (EDA): Let’s Dive In! 🔍
With the data now ready, it was time to play detective. 🕵️‍♂️ I wanted to see how all these variables were related. How does rent compare to the number of occupied units? Is there a pattern?

Scatter Plot: Rent vs. Occupied Units
I started by plotting average rent against occupied units. This gave me an idea of how rent impacts whether or not a unit is occupied. The results were pretty telling: higher rent often means lower occupancy. So if you're charging a premium, you might find fewer people willing to rent.

Bar Plot: Yearly Trends in Units
Next up, I grouped the data by year to see how the rental market has changed over time. The bar plot showed the trends in total and occupied units. Some years saw a huge increase in the number of rental units available, while others saw a dip. It was interesting to track how the market had evolved.

Rent-to-Income Ratio: Is Housing Affordable? 💸
Now, let’s get to the heart of the matter—affordability. We all know how difficult it can be to afford rent. So, I calculated the rent-to-income ratio assuming an average monthly income of ₹50,000. Why? Because if your rent is more than 30% of your income, it’s usually considered unaffordable.

Histogram: Rent-to-Income Ratio Distribution
I created a histogram to show how many rental units fall within the affordable range. I also drew a red line at the 30% threshold—anything beyond that is unaffordable for most people. And guess what? Most of the listings I looked at were beyond that threshold. Yikes, right?

It’s clear that rental prices in Hyderabad are leaving many tenants in a tight spot. 🚨

Key Insights: What the Data Tells Us 📌
After digging through the data, here are a few things I learned:

Affordability Is a Big Issue: A large portion of the rental units are not affordable based on an average income of ₹50,000/month.

Rent vs. Occupancy: There’s a negative correlation between rent and occupancy—higher rents tend to have fewer people occupying those units.

What Can Be Done?: This analysis highlights areas where changes can be made. We need more affordable housing, and there’s definitely room for policy improvement to help people who are being priced out of the market.

What’s Next? 🤔
While this analysis is a great starting point, there’s a lot more that could be done. Here are some ideas for further research:

Predicting Rent Prices: Using machine learning to predict future rental prices based on trends.

Geospatial Analysis: Examining rental trends across different neighborhoods in Hyderabad to understand where the demand is highest.

Wrapping Up 🎁
So there you have it! Through data science, we’ve peeled back the layers of Hyderabad’s rental housing market. While this is just the beginning, the insights gathered here can help urban planners, real estate developers, and policymakers make more informed decisions about housing affordability.

I hope this post gave you some valuable insights and sparked your curiosity about the power of data analysis in solving real-world problems. If you have any questions or thoughts about this project, I’d love to hear them. Drop a comment below!
