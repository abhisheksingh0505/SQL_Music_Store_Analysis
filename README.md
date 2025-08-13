# 🎵 Music Store Data Analysis with SQL

A comprehensive SQL project designed to analyze online music store data and extract valuable business insights. Perfect for beginners looking to master SQL queries and database analysis techniques.

[![GitHub Repository](https://img.shields.io/badge/GitHub-Repository-blue?style=flat-square&logo=github)](https://github.com/abhisheksingh0505/SQL_Music_Store_Analysis)
[![SQL](https://img.shields.io/badge/SQL-PostgreSQL-blue?style=flat-square&logo=postgresql)](https://www.postgresql.org/)


## 📋 Table of Contents
- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Database Schema](#database-schema)
- [Analysis Questions](#analysis-questions)
- [Key Features](#key-features)
- [Learning Outcomes](#learning-outcomes)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [Resources](#resources)

## 🎯 Overview

This project demonstrates how to leverage SQL to analyze a music store's database and answer critical business questions. Through hands-on analysis, you'll learn to extract meaningful insights that can drive business decisions and understand customer behavior patterns.

**🎥 Complete Tutorial**: [Watch on YouTube](https://www.youtube.com/watch?v=VFIuIjswMKM) by Rishabh Mishra

## 📊 Dataset Description

The music store database contains comprehensive information about:
- **Customers**: Personal details, location, and purchasing history
- **Employees**: Staff information and organizational hierarchy
- **Artists & Albums**: Music catalog with artist details
- **Tracks**: Individual songs with genre, duration, and pricing
- **Invoices**: Transaction records and sales data
- **Playlists**: Curated music collections

## 🛠️ Prerequisites

Before starting this project, ensure you have:
- Basic understanding of SQL syntax
- Familiarity with database concepts
- PostgreSQL installed on your system
- pgAdmin4 for database management

## ⚙️ Installation & Setup

### 1. Install Required Tools
```bash
# Install PostgreSQL (varies by OS)
# Windows: Download from postgresql.org
# macOS: brew install postgresql
# Ubuntu: sudo apt-get install postgresql postgresql-contrib
```

### 2. Setup Database
1. **Clone the repository**:
   ```bash
   git clone https://github.com/abhisheksingh0505/SQL_Music_Store_Analysis.git
   cd SQL_Music_Store_Analysis
   ```

2. **Setup PostgreSQL Database**:
   - Open pgAdmin4 and create a new database named `music_store`
   - Import the `Music_Store_database.sql` file to create schema and load data
   - Alternatively, extract and use data from `music store data.zip`
   - Verify all tables are created successfully by checking the schema diagram

3. **Verify Installation**:
   ```sql
   -- Check if all tables exist and have data
   SELECT table_name, 
          (SELECT COUNT(*) FROM information_schema.columns WHERE table_name = t.table_name) as column_count
   FROM information_schema.tables t
   WHERE table_schema = 'public';
   ```

### 3. Verify Installation
```sql
-- Check if all tables exist
SELECT table_name 
FROM information_schema.tables 
WHERE table_schema = 'public';
```

## 🗄️ Database Schema

![Music Store Database Schema](https://raw.githubusercontent.com/abhisheksingh0505/SQL_Music_Store_Analysis/main/MusicDatabaseSchema.png)

*The complete database schema showing relationships between all tables in the music store database.*

### Core Tables:
- `customer` - Customer information and demographics
- `employee` - Staff details and hierarchy
- `invoice` - Purchase transactions
- `invoice_line` - Individual items per transaction
- `track` - Song details and metadata
- `album` - Album information
- `artist` - Artist profiles
- `genre` - Music categories
- `playlist` - Curated song collections
- `playlist_track` - Songs within playlists

## 🔍 Analysis Questions

This project is structured around three progressive question sets designed to build your SQL skills:

### 🟢 Question Set 1 - Easy
1. **Senior Employee Analysis**: Who is the senior most employee based on job title?
2. **Invoice by Country**: Which countries have the most Invoices?
3. **Top Invoice Values**: What are top 3 values of total invoice?
4. **Best Customer City**: Which city has the best customers? We would like to throw a promotional Music Festival in the city we made the most money. Write a query that returns one city that has the highest sum of invoice totals. Return both the city name & sum of all invoice totals.
5. **Best Customer**: Who is the best customer? The customer who has spent the most money will be declared the best customer. Write a query that returns the person who has spent the most money.

### 🟡 Question Set 2 - Moderate
1. **Rock Music Listeners**: Write query to return the email, first name, last name, & Genre of all Rock Music listeners. Return your list ordered alphabetically by email starting with A.
2. **Top Rock Artists**: Let's invite the artists who have written the most rock music in our dataset. Write a query that returns the Artist name and total track count of the top 10 rock bands.
3. **Long Tracks Analysis**: Return all the track names that have a song length longer than the average song length. Return the Name and Milliseconds for each track. Order by the song length with the longest songs listed first.

### 🔴 Question Set 3 - Advanced
1. **Customer Spending on Artists**: Find how much amount spent by each customer on artists? Write a query to return customer name, artist name and total spent.
2. **Most Popular Genre by Country**: We want to find out the most popular music Genre for each country. We determine the most popular genre as the genre with the highest amount of purchases. Write a query that returns each country along with the top Genre. For countries where the maximum number of purchases is shared return all Genres.
3. **Top Customer by Country**: Write a query that determines the customer that has spent the most on music for each country. Write a query that returns the country along with the top customer and how much they spent. For countries where the top amount spent is shared, provide all customers who spent this amount.

## ✨ Key Features

- **Comprehensive Analysis**: From basic queries to complex business intelligence
- **Real-world Scenarios**: Practical questions faced by music retailers
- **Progressive Difficulty**: Structured learning path from beginner to advanced
- **Best Practices**: Clean, optimized SQL code with proper formatting
- **Business Insights**: Actionable recommendations based on data analysis

## 🎓 Learning Outcomes

After completing this project, you'll master:
- **SQL Fundamentals**: SELECT, WHERE, ORDER BY, GROUP BY
- **Advanced Queries**: JOINs, Subqueries, Window Functions
- **Data Analysis**: Aggregations, Statistical Functions
- **Business Intelligence**: Translating data into insights
- **Database Design**: Understanding relational database structure

## 📁 Project Structure

```
SQL_Music_Store_Analysis/
│
├── 📄 README.md                                    # Project documentation (you're here!)
├── 📋 Music Store Analysis-Questions.docx         # Complete question sets with requirements
├── 🖼️ MusicDatabaseSchema.png                     # Visual database schema diagram
├── 💾 Music_Store_Query.sql                       # Your SQL solutions file
├── 🗄️ Music_Store_database.sql                    # Database schema & sample data
├── 📦 Raw-Music Store Analysis-SQL Project.zip    # Original project files backup
├── 📊 album2.csv                                  # Sample album data file
└── 📁 music store data.zip                        # Complete dataset archive
```

**Quick Start Files:**
- **Questions**: Open `Music Store Analysis-Questions.docx` for all problem statements
- **Schema**: View `MusicDatabaseSchema.png` to understand table relationships  
- **Database**: Use `Music_Store_database.sql` to set up your PostgreSQL database
- **Solutions**: Write your queries in `Music_Store_Query.sql`

## 🚀 Usage

### Getting Started
1. **Setup**: Follow the installation steps above to set up your database
2. **Question Reference**: Open `Music Store Analysis-Questions.docx` for detailed question requirements
3. **Schema Study**: Review `MusicDatabaseSchema.png` to understand table relationships
4. **Solution Development**: Write your queries in `Music_Store_Query.sql`

### Working with the Project
1. Open pgAdmin4 and connect to your `music_store` database
2. Start with Question Set 1 (Easy) and progress through the levels
3. Test each query thoroughly before moving to the next question
4. Document your approach and findings for each solution
5. Compare your solutions with peers for learning enhancement

### Example Query
```sql
-- Find the best customer by total spending
SELECT 
    c.customer_id,
    c.first_name,
    c.last_name,
    SUM(i.total) as total_spent
FROM customer c
JOIN invoice i ON c.customer_id = i.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY total_spent DESC
LIMIT 1;
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-analysis`)
3. Add your queries and documentation
4. Commit changes (`git commit -am 'Add new customer analysis'`)
5. Push to branch (`git push origin feature/new-analysis`)
6. Create a Pull Request

## 📚 Resources

### Learning Materials
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [SQL Tutorial - W3Schools](https://www.w3schools.com/sql/)
- [Database Design Fundamentals](https://www.lucidchart.com/pages/database-diagram/database-design)

### Tools & Extensions
- [pgAdmin4](https://www.pgadmin.org/)
- [DBeaver](https://dbeaver.io/) - Alternative database tool
- [DB Diagram](https://dbdiagram.io/) - Schema visualization

### Additional Practice
- [SQLBolt](https://sqlbolt.com/) - Interactive SQL lessons
- [HackerRank SQL](https://www.hackerrank.com/domains/sql) - Practice problems
- [LeetCode Database](https://leetcode.com/problemset/database/) - Advanced challenges

---

## 👨‍💻 About This Project

**Project Creator**: [Abhishek Singh](https://github.com/abhisheksingh0505)  
**Tutorial Credit**: Based on the excellent guidance by **Rishabh Mishra**  
**Video Tutorial**: [Complete SQL Project Walkthrough](https://www.youtube.com/watch?v=VFIuIjswMKM)

## 🤝 Connect & Contribute

- 🌟 **Star this repository** if you found it helpful!
- 🔀 **Fork** the project to create your own version
- 📢 **Share** with others learning SQL
- 🐛 **Report issues** or suggest improvements
- 💡 **Contribute** additional analysis questions

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/abhisheksingh0505/SQL_Music_Store_Analysis?style=social)
![GitHub forks](https://img.shields.io/github/forks/abhisheksingh0505/SQL_Music_Store_Analysis?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/abhisheksingh0505/SQL_Music_Store_Analysis?style=social)

---



---

### 🎵 Ready to dive into SQL? Clone the repo and start your data analysis journey!

```bash
git clone https://github.com/abhisheksingh0505/SQL_Music_Store_Analysis.git
```

**Happy Querying! 🎵📊**
