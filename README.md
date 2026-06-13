EDA & Feature Engineering – Google Play Store Dataset

## Short Description
Exploratory Data Analysis and Feature Engineering on the Google Play Store dataset (10,841 apps, 14 features) to uncover insights about app categories, installs, ratings, pricing, and more.

## Dataset
- Rows: 10,841
- Columns: 14 (App, Category, Rating, Reviews, Size, Installs, Type, Price, Content Rating, Genres, Last Updated, Current Ver, Android Ver, Unnamed: 0)

## Workflow

### 1. Data Cleaning
- Removed invalid rows (e.g., row with shifted/corrupted data)
- Converted `Reviews` to integer type
- Cleaned and converted `Size` (M → KB, removed "Varies with device")
- Cleaned `Installs` and `Price` columns (removed `+`, `,`, `$`) and converted to numeric
- Parsed `Last Updated` into `Day`, `Month`, `Year` features
- Removed duplicate app entries (1,181 duplicates dropped)

### 2. Exploratory Data Analysis
- Univariate analysis of numerical features (Rating, Reviews, Size, Installs, Price, etc.)
- Univariate analysis of categorical features (Type, Content Rating, Category, Genres)
- Distribution analysis showing skewness in Reviews, Size, Installs, and Price

### 3. Feature Engineering
- Extracted date-based features (Day, Month, Year) from `Last Updated`
- Created cleaned numeric columns for Size, Installs, and Price

## Key Insights

1. Most popular categories: FAMILY (19%), GAME (10%), and TOOLS (8.6%) dominate the Play Store.
2. Least popular categories: Beauty, Comics, Art & Design, and Weather make up less than 1% each.
3. Most installed category: GAME, with nearly **35 billion installs**, followed by COMMUNICATION and TOOLS.
4. Top apps per category:
   - Game: Subway Surfers
   - Communication: Hangouts
   - Productivity: Google Drive
   - Social: Instagram
5. Ratings: 271 apps on the Play Store have a perfect 5.0 rating, with "DN Employee" (FAMILY category) topping the list.
6. Distribution:Rating and Year are left-skewed; Reviews, Size, Installs, and Price are right-skewed.
7. Most apps are Free (92.6%) with a content rating of Everyone (80%).

## Tools & Libraries
- Python (Pandas, NumPy)
- Matplotlib & Seaborn for visualization
- Jupyter Notebook

## Future Work
- Build predictive models for app ratings/installs
- Sentiment analysis on app reviews
- Deeper genre-level breakdowns
