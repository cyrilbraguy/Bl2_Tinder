# Bl2_Tinder
This project belongs to CDSD certification Block 2 
Tinder project
  
<img src="https://full-stack-assets.s3.eu-west-3.amazonaws.com/M03-EDA/Tinder-Symbole.png" alt="Tinder" width="30%" />
  

# Speed Dating with Tinder

## Company's description 📇

<a href="https://tinder.com/" target="_blank">Tinder</a> is an online dating and geosocial networking application. In Tinder, users "swipe right" to like or "swipe left" to dislike other users' profiles, which include their photos, a short bio, and a list of their interests.

## PITCH

Tinder, the famous online dating and geosocial networking application launched in 2012. After a meteoric rise at 65 milions matches in 2021, Tinder is facing declining matches and wants to understand **what makes people interested in each other.** Its marketing team relies on a 2002-2004 speed dating experiment of several waves: four-minute dates, followed by decisions on second dates and ratings on six attributes, plus questionnaire data on demographics, habits, and lifestyle of people and speeddating partner.

## GOALS
- Use the dataset, through descriptive statistics and visualizations, to identify what drives people to accept a second date.  
- Explore questions such as attractiveness versus its real impact, shared interests versus shared background, self-perception accuracy, and date order. 
- Deliver a notebook with statistics, charts, and interpretations.


# Project implementation

# load dataset : 
8378 lines 195 columns, 21 waves,

**missing values:**  percentage: 26.4% 
see plot 
13 -> 17 colonnes full
72 -> 69 colonnes avec moins de 5% de valeurs manquantes : imputation possible AVG/median or mode
total after treatment : 96 

20 colonnes avec 5 a 15% de valeurs manquantes : a examiner pour imputation 
19 : missing 15 to 40% : imputation possible si pattern ou 
71 : plis de 40% missing : rien à faire, inutilisables 
  
-  after treatment missing values : 13+72 columns
-  treatment per waves
-  - correct : id, pid, age, age_o
  
  **clean data**
  - data types : int, bool, float, categorial 

  - columns rename for better intelligibility
  - Replace columns dictionnaries for categorical variables
  - ratings update on same scale sum_100 even when missing descriptor
  - Aggregate data of persons in a DataFrame : **perso_df**
    - calculation of additional indicators : 
      - success_rate, 
      - decision_rate, 
      - decision_partner_rate, 
      - match_rate...
  - compute stats per wave : **synth1**

# 2 EDA od speed daters