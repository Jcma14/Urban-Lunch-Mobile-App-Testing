<!-- ===== HEADER BANNER ===== -->
<p align="center">
  <img src="assets/Urban-lunch-banner.png" alt="Urban.Lunch Banner" style="max-width:100%; height:auto; border-radius:6px;">
</p>

# <p align="center">Urban.Lunch <sub> Mobile App</sub></p>

<p align="center">
  <!-- Badges -->
  <img alt="Platform" src="https://img.shields.io/badge/Platform-Android-blue?style=for-the-badge&logo=android">
  <img alt="Testing" src="https://img.shields.io/badge/Testing-Manual%20%26%20Emulator-yellow?style=for-the-badge">
  <img alt="Status" src="https://img.shields.io/badge/Version-1.0-lightgrey?style=for-the-badge">
</p>


## Overview
**Urban.Lunch** is an Android mobile app that lets users order food from multiple restaurants and pick a single pickup location where all orders are collected.  
This repo documents my QA testing for **Urban.Lunch v1.0**, including test approach, results, defects, and evidence.


## Project Goal
Validate core user flows so that a user can:
- Choose a pick-up point,
- Select dishes from multiple restaurants,
- Confirm an order (with correct totals),
- Track the order status,
- And verify correct handling of geolocation permissions and error messages.


## Approach
- **Emulator:** Android Studio — used Samsung Galaxy S25+ profile (Android 16.0)  
- **Type of testing:** Manual testing (exploratory + scripted) on emulator; log inspection via Logcat.  
- **Test coverage:** Positive, negative and boundary scenarios (e.g., multiple restaurants, max items).  


## Key Results
- **Defects found:** 3 functional defects affecting order confirmation and tracking.  
- **Permissions issue:** Unexpected app behavior when geolocation permissions are denied (app may close or block flow).  
- **Other notes:** Total amount calculation does not include delivery fee correctly.


## Recommendations
1. Fix total cost calculation so `delivery cost` is included in `order total`.  
2. Add estimated delivery time and a preparation timer in the UI.  
3. Define expected behavior when geolocation permission is denied (do not close app; allow retry or redirect to settings).  
4. Re-execute the test suite after fixes and update the test evidence.


## Tools & Skills
<span>
<img src="https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white">
<img src="https://img.shields.io/badge/Mobile%20Testing-1AB26B?style=for-the-badge">
<img src="https://img.shields.io/badge/Test%20Planning-1E90FF?style=for-the-badge">
<img src="https://img.shields.io/badge/Manual%20Testing-E0711B?style=for-the-badge">
<img src="https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white">


## Test Evidence
### Bugs Reported (JIRA) 
![JIRA Bug Report](assets/Jira.png)

### Android Studio - Logcat 
![Android Studio](assets/Android-studio.png)

### Urban.Lunch Mobile App
<p align="center">
  <img src="assets/Urban-lunch-screenshot-1.png" alt="Evidence 1" width="45%" style="margin: 5px; border-radius: 6px;">
  <img src="assets/Urban-lunch-screenshot-2.png" alt="Evidence 2" width="45%" style="margin: 5px; border-radius: 6px;">
</p>


