#  Personalized Mentor Recommendation System for CLAT Aspirants

Hi I am yash! In this project, I built a smart AI/ML system that recommends top mentors (CLAT toppers) to law aspirants based on their preparation profiles. My aim was to make mentorship more personalized and helpful for CLAT students.

---

##  Objective

I wanted to match aspirants with mentors who understand their learning needs. So, I designed a recommendation engine that uses both traditional feature-based similarity and deep semantic understanding with SBERT (Sentence-BERT).

---

##  What I Did

###  Data Generation
I generated:
- 500 mock aspirants
- 100 mentors
- 2,000 ratings (to simulate feedback)

I used realistic CLAT score distributions and added useful features like preferred subjects, prep level, and learning style.

###  Feature Engineering
For both aspirants and mentors, I processed:
- Subject preferences (multi-label)
- Prep level & learning/teaching style (one-hot)
- Rank, score, coaching access, weekly study hours, and more

###  Matching Approaches

####  KNN-Based Matching
I encoded features into vectors and used cosine similarity with KNN to find top 3 mentors per aspirant.

####  SBERT Semantic Matching
I also created natural language profiles for every aspirant and mentor and used `sentence-transformers` to compute semantic embeddings. Then I compared profiles using cosine similarity and returned the best matches.

---

##  Example Output

```json
{
  "aspirant_id": 0,
  "recommended_mentors": [86, 9, 98]
}
