# DGA-Algorithm-Detection

## Problem Statement

The goal of this project is to detect tricky domain names—domains that are not random but disguise themselves using confusing characters. The classification task involves categorizing domains into four categories: **Benign**, **Phishing**, **Defacement**, and **Malware**.

## Program Flow Overview

### 1. Load and Process Data
- Load the domain data from CSV or Excel files.
- Extract features from each domain name, including:
  - Length
  - Digit count
  - Vowel to consonant ratio
  - Entropy

### 2. Model Training
- Preprocess the extracted features by normalizing and reducing dimensionality.
- Train a **Random Forest** classifier on the preprocessed data.
- Save the trained model, scaler, and PCA objects for future use.

### 3. Classification
- Load new domain data for prediction.
- Preprocess the new data using the saved scaler and PCA objects.
- Classify the new data using the trained model.
- Save and report the classification results.

### 4. Interactive Elements
- Use widgets for user inputs to specify the training and prediction files.
- Execute the training and classification processes based on user interaction.

## Machine Learning Model: Random Forest Classifier

The **Random Forest** classifier was chosen for its robustness and ability to handle complex data structures. It operates by constructing multiple decision trees and outputting the mode of the classes or the mean prediction of the individual trees. This model is suitable for this problem due to its high performance in classification tasks.

## Categories Explained

### 1. Benign Domains
- **Definition:** Legitimate domains with no malicious intent. These domains belong to safe websites used for normal purposes, such as businesses, organizations, or personal sites.
- **Characteristics:** Often straightforward names that directly relate to the entity they represent, without unusual patterns or characteristics suggesting malicious intent.
- **Examples:**
  - `google.com`: The domain of the Google search engine.
  - `wikipedia.org`: The domain for Wikipedia, a popular online encyclopedia.

### 2. Phishing Domains
- **Definition:** Domains created to deceive users into divulging sensitive information such as usernames, passwords, or credit card details by mimicking legitimate websites.
- **Characteristics:** Often use misspelled common domain names, similar-looking characters (homoglyphs), or add prefixes/suffixes to genuine domains.
- **Examples:**
  - `app1e.com`: Using a homoglyph (replacing 'l' with '1') to resemble apple.com.
  - `micr0s0ft.com`: Using a homoglyph (replacing 'o' with '0').

### 3. Defacement Domains
- **Definition:** Domains associated with cyber attacks where the appearance of a website is altered without authorization, often to display political messages, vandalize, or demonstrate security vulnerabilities.
- **Characteristics:** May include additional words in the domain name, often redirecting visitors to pages showcasing altered content or messages.
- **Examples:**
  - `google.ro`: A domain indicating that google.com has been hacked and its content altered.
  - `paypal.ro`: A domain highlighting that the associated website has been defaced.

### 4. Malware Domains
- **Definition:** Domains used to propagate malicious software (malware) to unsuspecting users' devices. These may host or redirect to malicious content that installs malware on the victim's system.
- **Characteristics:** Often have random or nonsensical names to evade detection, may use domains that are temporarily registered or employ domain generation algorithms (DGAs) to dynamically generate new domain names.
- **Examples:**
  - `xyz-download.com`: A domain enticing users to download a file that contains malware.
  - `malware-botnet.net`: A domain associated with a botnet spreading malware across multiple devices.

![Sample output image failed to load]("C:\Users\Sneha Anne George\Downloads\sample_run_1.png")

