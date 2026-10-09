# Sahay: Offline Clinic Triage

Sahay helps health workers in low connectivity clinics decide who needs care first, and shows why.

## What it does
- Takes 8 inputs: age, temperature, heart rate, breathing rate, oxygen saturation, systolic BP, alertness, chest pain.
- A **decision tree (CART, Gini impurity) written from scratch in JavaScript** is trained in the browser on page load.
- Outputs a triage level (Low, Medium, High), class probabilities, and a **plain language decision path** that lists every rule that fired.
- Shows feature importance and a held out test report (accuracy, high risk recall, confusion matrix).

## Run it
Open `index.html` in any browser. No install, no internet, no server.

## Data and honesty note
The training cases are synthetic. They are generated with realistic vital sign distributions and labelled with a NEWS2 inspired early warning score plus 5% label noise. The tree has to rediscover those rules from examples. To use real data, replace `makeDataset()` with rows from a real clinical dataset in the same 8 column format.

## Limits
This is a hackathon prototype and not a medical device. It should never replace clinical judgment.

## Tech
Plain HTML, CSS, JavaScript. About 400 lines, zero dependencies.
