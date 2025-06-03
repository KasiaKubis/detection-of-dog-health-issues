# PetGuard — AI-based Early Detection of Dogs' Health Issues

Final project for the Building AI course

## Summary

PetGuard is an AI-powered mobile app that monitors dogs’ activity and vital signs to detect early signs of health problems like arthritis or obesity. It alerts owners and vets for timely intervention.  
Building AI course project

## Background

Many dogs suffer from chronic health issues that often go unnoticed until advanced stages. Early detection is difficult but crucial for better care.  
My motivation comes from owning a dog diagnosed late with arthritis, which caused avoidable suffering. This project aims to improve animal health and owner peace of mind by leveraging wearable sensor data and AI.  

Problems addressed include:  
* Late detection of chronic diseases in pets  
* Lack of continuous health monitoring outside vet visits  
* Difficulty for owners to spot subtle early symptoms  

## How is it used?

Dog owners use the PetGuard app paired with a wearable collar sensor to continuously monitor their pets’ activity, heart rate, and behavior. When abnormalities are detected, the app notifies the owner and can share reports with veterinarians.  
This is useful in everyday home environments and for dogs with known risk factors or older age.  
Users include dog owners looking for preventive care and vets who want remote monitoring capabilities.  

## Data sources and AI methods

PetGuard depends heavily on **wearable sensor data** collected from dogs’ collars, including:

* **Activity levels** (accelerometer data) to detect changes in movement patterns  
* **Heart rate** and **body temperature** for physiological monitoring  
* **Owner-reported symptoms and behavior logs** entered through the app, like appetite or coughing  
* **Veterinary health records** (historical diagnoses and treatment outcomes) used for supervised training  

The quality and availability of these data sources are critical — especially labeled veterinary data to train accurate predictive models. Initially, publicly available datasets on pet activity can be combined with synthetic data to bootstrap model development.

### AI techniques useful for this project:

* **Time-series anomaly detection** algorithms (e.g., LSTM autoencoders) to spot deviations from normal activity or vitals  
* **Classification models** such as Random Forests or Neural Networks to predict specific conditions (arthritis, obesity risk) based on sensor and owner input data  
* **Natural Language Processing (NLP)** for analyzing free-text symptom descriptions by owners to enrich data features  
* **Data preprocessing** techniques to handle missing data, normalize sensor streams, and personalize models per breed or age  

---

## Challenges

While PetGuard aims to provide early warnings about pet health, it does **not replace veterinary diagnosis**. Some limitations include:

* **Data scarcity and quality:** High-quality, labeled veterinary datasets are rare, limiting model accuracy and generalization  
* **Variability:** Differences between dog breeds, ages, and environments make creating universally accurate models difficult  
* **Owner input variability:** Subjective or inconsistent symptom reports may reduce prediction reliability  
* **Ethical and privacy concerns:** Handling sensitive pet and owner data responsibly is essential, especially if sharing with veterinarians  
* **False positives/negatives:** Over-alerting owners or missing subtle signs can reduce trust and usefulness  

---

## What next?

PetGuard can grow into a more comprehensive pet health platform by:

* Integrating **additional sensors** such as GPS or respiratory rate monitors for richer data  
* Developing **personalized AI models** that adapt to individual pets over time for higher accuracy  
* Employing **federated learning** to train models across users without sharing raw data, enhancing privacy  
* Expanding to cover other common pets like cats or horses  
* Adding **telemedicine features** enabling direct video or chat consultations with vets through the app  
* Collaborating with veterinary clinics to validate and improve model predictions in real-world settings  
