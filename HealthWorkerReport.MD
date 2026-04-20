# 📱 Digital Health Reporting App for Community Health Workers in Nigeria  
**Built with Power Apps, Dataverse & Power BI**  
*A step‑by‑step walkthrough of my Microsoft Elevate AI Developers Program Capstone Project*
![My image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/health%20worker_Thumbnail.png?raw=true)

---

## 🚨 Problem Statement  
Community Health Workers (CHWs) in rural Nigeria rely on paper forms to record patient visits. These forms are later re‑entered manually at Local Government Area (LGA) offices, often days later, leading to delays, errors, and data loss. Supervisors cannot act on health trends quickly enough, leaving communities underserved.  

---

## 🎯 Project Goal  
The goal of this app is to eliminate paper‑based reporting by enabling CHWs to record patient visits digitally on their phones. Data is stored directly in **Dataverse** and visualized in **Power BI**, giving supervisors real‑time insights into visit volumes, health trends, and community outreach coverage.  

---

## 🛠 Tools & Technologies  
- **Microsoft Power Apps** – Mobile data entry app  
- **Microsoft Dataverse** – Cloud data storage  
- **Microsoft Power BI Desktop** – Supervisor dashboard  
- **DAX & Power Query** – Data modelling and measures  
- **Microsoft 365 Developer Account** – Free Developer environment  

---

## 📝 Step‑by‑Step Build Process  

### Step 1: Designing the Data Model in Dataverse  
- Referenced **NPHCDA HMIS standard fields** to ensure real‑world relevance.  
- Created a `Patient_Information` table with required fields:  
  - Patient Full Name  
  - Visit ID  
  - Diagnosis  
  - Chief Complaint  
  - Patient Age  
  - Gender (Choice field)  
  - Community  
  - Local Government Area (LGA)  
  - Referral Needed (Yes/No)  
  - Visit Date  
- **Design decision:** Referral Needed and Gender as choice fields for cleaner Power BI filtering.  

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/power%20App%20Project%202.png?raw=true)

---

### Step 2: Building the Power App  
- Built a **Canvas App** with two screens:  
  - **Screen 1:** Patient Visit Form with required fields and validation.  
  - **Screen 2:** Gallery of recent submissions with search and edit functionality.  
- Required fields marked with an asterisk (*) to guide CHWs.  

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Power%20App%20Gallery%20Without%20Image.jpg?raw=true)
  

---

### Step 3: Entering Test Records  
- Entered 7 test records through the app to validate the end‑to‑end pipeline.  
- Records represented different communities, LGAs, diagnoses, and referral outcomes.  

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Power%20App%20Gallery%203.png?raw=true)

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Power%20App%20Gallery%203.png?raw=true)

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Dataverse2.png?raw=true)



---

### Step 4: Connecting Dataverse to Power BI  
- Imported the Dataverse table into Power BI Desktop:  
  - Get Data → Dataverse → Environment URL → Sign in → Select table → Import mode.  
- Ensured stable connections and verified data integrity.  

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/PowerApp_Dataverse_PowerBI.jpg?raw=true)

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/powerBI_DirtyData.jpg?raw=true)

![My Image](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Power_BI_Cleaned_Data.png?raw=true)


---

### Step 5: Data Modelling with a Calendar Table  
- Created a Calendar dimension table using:  

```DAX
Calendar = CALENDARAUTO()
```
![My Image](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/power_App_Datamodelling.png?raw=true)

### Step 6: Creating DAX Measures
Built some simple measures to power KPI cards:

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/power%20App__DAX.png?raw=true)

## Step 7: Designing the Dashboard
Final dashboard included:

* KPI Cards: Total Visits, Communities Reached, Referrals Made, Average Age, Referral Rate %
* Bar Chart: Visits by Day of Week
* Donut Charts: Gender Distribution, Chief Complaints Breakdown
* Community Reach Summary Table
* Dynamic "Last Refreshed" timestamp

![My Image Description](https://github.com/R887645/Field-Reporting-App-Analytics-Dashboard-for-Community-Health-Workers/blob/main/Power%20Apps_Power%20BI.png?raw=true)

## 📊 Results
Even with 7 test records, the dashboard demonstrated:

* Communities reached by CHWs
* Common diagnoses (Malaria, Fever, Diarrhoea)
* Referral rate (28.57%)
* Gender distribution of patients
* Visit patterns by day of week

## ⚠️ Limitations

1. Built in a developer tenant (not production‑ready), so the App Link can't be tested for external use.
2. Limited test data (7 records).
3. Requires internet connectivity (no offline support yet).

## 🔮 Future Improvements

* Offline capability for low‑network areas.
* Automated alerts via Power Automate.
* User authentication for CHWs (Community Health Workers).
* Trend analysis and drill‑through dashboards.
* Integration with real NPHCDA datasets.

## 💡 Key Takeaways

* Low‑code tools can solve real health challenges.
* Proper data modelling is critical for clean analytics.
* Building for real‑world problems makes projects impactful.

## 🏁 Conclusion

This project demonstrates that low-code tools like Microsoft Power Apps and Power BI 
are not just for corporate enterprises, they can be powerful enablers for 
community health organizations, NGOs, and public health agencies seeking to digitize 
their field operations and make data-driven decisions.

For organizations like the NPHCDA and community health programs across Africa, 
solutions like this can:

* Reduce reliance on paper-based reporting
* Improve visibility into CHW activities at the grassroots level
* Enable faster, evidence-based response to health trends
* Bridge the gap between field workers and decision-makers

---

👋 **About the Author**

Hi, I'm **Rofiah**: an E-commerce Data Analyst currently expanding into Microsoft 
Power Platform, building low & no-code automation solutions with Power Automate, 
Power Apps and Power Pages.

I believe data is most powerful when it solves real problems for real people.

**[Read My Article on Medium](https://medium.com/@kehindeazeez49/how-i-built-a-digital-health-reporting-app-for-community-health-workers-in-nigeria-using-power-599bb54df5b5?postPublishedType=initial)**


📌 PLEASE NOTE:
- The Power App link is not accessible to external users as this was built on a 
  Microsoft 365 Developer sandbox account — access is restricted to within that tenant only.

- The Power BI dashboard link is equally unavailable for external access 
  for the same reason. In a real organisational deployment, access would be 
  granted and managed within the organisation's Microsoft 365 tenant.

- The dashboard was built with only 7 test records, this is intentional. 
  The goal was to demonstrate the end-to-end connection between Power Apps 
  and Power BI, not to present real patient data. In a live deployment, 
  the dashboard would reflect hundreds of real field visits over time.

