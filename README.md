# Airline Customer Segmentation: Loyalty Program Analytics ✈️📊

## 📌 Project Overview
This project applies Unsupervised Machine Learning (Clustering) to the EastWest Airlines frequent flyer database. The objective is to identify distinct passenger segments based on their mileage accumulation, credit card spending habits, and flight frequency. By moving away from "one-size-fits-all" marketing, the airline can deploy hyper-personalized strategies to maximize customer retention and credit card loyalty.

## 📊 Dataset Description
The dataset contains information on 3,999 customers enrolled in the frequent flyer program.
* **Dataset Size:** 3,999 records, 12 variables.
* **Key Features:**
  * `Balance`: Miles eligible for award travel.
  * `cc1_miles`, `cc2_miles`, `cc3_miles`: Miles earned through different credit card tiers.
  * `Bonus_miles` & `Bonus_trans`: Number of non-flight miles and transactions in the past 12 months.
  * `Flight_miles_12mo`: Total miles flown in the last year.
  * `Award?`: Whether the customer has redeemed miles for a flight.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (K-Means Clustering)
* **Data Visualization:** `matplotlib`, `seaborn`

## 🧠 Methodology
1. **Exploratory Data Analysis (EDA):** Visualized mileage distributions and discovered extreme outliers in `Balance` (ranging from 0 to 1.7M miles).
2. **Data Preprocessing:** Standardized features using **StandardScaler** to ensure that features with high magnitudes (like Balance) did not bias the distance calculations. **80/20 train-test split applied** for validation.
3. **Model Selection:** Utilized the **Elbow Method** to identify K=5 as the optimal number of clusters for meaningful segment separation.
4. **Validation:** Confirmed segment distinctness using a **Cluster Scatter Plot** and verified consistent behavior within each group.

## 📈 Key Results & Analytics Inference
The model successfully categorized the 4,000-strong database into four strategic pillars:
* **Cluster 1 (The Bulk):** The largest group with the lowest value. *Inference:* These are entry-level flyers with low program engagement.
* **Cluster 2 (The VIP Flyers):** High balances and the highest flight activity. *Inference:* These represent the most profitable "power users."
* **Cluster 0 & 3 (The Card Loyalists):** Earn miles primarily through transactional volume (CC1 and CC3). *Inference:* These are high-spend retail users.
* **Cluster 4 (The Rewards Users):** High usage specifically in CC2 rewards. *Inference:* Niche group focusing on peripheral card perks.

## 💼 Business Impact & Strategic Action Plan
* **Targeting The Bulk:** Action: Deploy "First Flight" deep discounts to establish habitual booking and drive the first mileage redemption.
* **Retaining VIPs:** Action: Provide priority service, exclusive lounge access, and frictionless "Elite Status" renewals to prevent churn to competitors.
* **Engaging Card Loyalists:** Action: Partner with major retail brands to offer "Double-Point Weekends," capturing more of their daily transactional spend.
* **Niche Rewards:** Action: Offer specialized card-holder events or specific travel insurance perks to Cluster 4 to maintain their unique loyalty path.

