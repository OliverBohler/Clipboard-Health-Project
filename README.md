# Clipboard-Health-Project
## By Oliver Bohler
## Project Overview:

This project was developed as part of a data exercise for Clipboard Health, a nationwide staffing platform that connects healthcare professionals with facilities in need of support. With the U.S. healthcare system facing increasing pressure from staff shortages—especially among registered nurses (RNs)—Clipboard Health’s Sales team must take a strategic and data-driven approach to identify facilities and regions most likely to need contracted nurses.

To support this, I conducted a detailed analysis using the CMS Payroll Based Journal (PBJ) staffing data and additional CMS datasets, focusing on the most recent quarter available (2024 Q2). I explored staffing indicators such as nursing staff turnover, occupancy rates, deficiency scores, and score gaps across various states, ownership types, and facility categories. The objective was to identify trends, uncover areas with potentially high demand for staffing support, and deliver clear, actionable recommendations to Clipboard Health’s leadership team that could improve sales targeting, decision-making, and operational success.

# Recommendation 1: Targeting States Based on High Contract Work Potential

Given the vast amount of data in my original dataframe, additional research was conducted to find out which states will experience the highest staffing shortages for nurses by 2035. According to a Health Workforce Analysis published by the Health Resources and Services Administration (HRSA), these states are as follows: 

- Washington (26%), Georgia (21%), California (18%), Oregon (16%), Michigan (15%)
- Idaho (15%), Louisiana (13%), North Carolina (13%), New Jersey (12%), and South Carolina (11%)

Source: American Association of Colleges of Nursing

This is visualized using a histogram:

<img width="869" alt="Histogram_Facilities " src="https://github.com/user-attachments/assets/2b5de213-ea09-41a7-9f51-28740daa052a" />

The histogram illustrates the distribution of unique healthcare facilities across the 10 target states identified as having the highest projected nurse shortages. To deepen the analysis and better understand each state's reliance on contracted nurses, a pie chart was created to compare the total working hours fulfilled by employed staff versus contracted nurses. This comparison helps highlight which states present the strongest opportunities for Clipboard Health to expand contract-based staffing solutions.

<img width="864" alt="Employed vs Contracted nurses pie chart" src="https://github.com/user-attachments/assets/f3ae5c5e-c8fc-486f-bc3e-c07d385c08f6" />

The data shows that California remains the largest market in terms of total healthcare facilities. However, states like Oregon, North Carolina, New Jersey, and Washington stand out for having the highest percentage of working hours fulfilled by contracted nurses—highlighting key opportunities for Clipboard to expand its footprint.

I recommend that Clipboard’s sales efforts focus strategically on these 10 states due to their current reliance on contract staff and future staffing risks, with priority attention given to:
- California
- Oregon
- North Carolina
- New Jersey
- Washington State

To optimize outreach and effectiveness:

Create state-specific sales task groups to build relationships and tailor messaging based on local trends.

# Reccomendation 2: Focus on CNA, LPN and RN jobs Based on Day of the Week
Certified Nursing Assistants (CNA), Licensed Practical Nurses (LPN), and Registered Nurses (RN) consistently log the most hours. The highest demand occurs Monday through Friday, with Wednesday and Thursday standing out as peak days across both states. These are the days when facilities need the most staffing support, making them key targets for sales and recruiting teams. This seems to be a trend accross al 10 target states.
On the weekends (Saturday and Sunday), there is a noticeable drop in overall hours, especially for administrative roles such as RN and LPN administrators. However, core clinical roles—CNA, LPN, and RN—continue to show strong weekend activity, particularly in California, where weekend shifts remain substantial despite the decline.

Since facility needs and state regulations vary, employers often prioritize different types of nurses depending on local requirements. To begin uncovering potential indicators of demand, I analyzed the most commonly employed nurse types across states. A pie chart was created to visualize the distribution of nursing roles, offering an initial snapshot of which nurse types are most in demand and where targeted staffing efforts could be most impactful.

<img width="847" alt="Nursing_Types per state" src="https://github.com/user-attachments/assets/90fccb96-76af-4b2b-8bed-2f9cdab74982" />

The three dominant job types in the healthcare sector are:

### Certified Nursing Assistants (CNAs) 
- Over 50% of employed healthcare professionals fall into this category, making it the most in-demand role.
- CNAs are essential for day-to-day patient care, which could explain their high employment rate in facilities.

### Licensed Practical Nurses (LPNs) 
- LPN employment rates range from 15% to 26.8% depending on the state.
- These roles provide a bridge between CNAs and RNs, playing a crucial role in patient supervision and medication administration.

### Registered Nurses (RNs) 
- The RN employment share varies between 8% and 14%, with one exception: Louisiana (LA), where only 3.4% of employed nurses are RNs.
- The lower RN employment rate in LA is likely due to the higher share of CNAs and LPNs, possibly influenced by state-level policies or cost-saving employment structures.

After identifying which nursing roles make up the majority of the workforce, the next logical step was to assess the potential for contracted work within each job category. Understanding which roles rely more heavily on contracted staff allows the sales team to focus their outreach more strategically. To visualize this, I created a stacked bar chart comparing employed versus contracted hours across nursing job types.

<img width="851" alt="Hours worked CPN LPN CNA" src="https://github.com/user-attachments/assets/5242b60d-d76e-4765-9452-ad5917af1ba7" />

To further highlight the dependency on specific nurse types and uncover potential scheduling patterns, I generated heatmaps illustrating the total working hours by nurse type across each day of the week for all target states. This approach helps identify trends in staffing needs and may reveal which nurse types are more likely to be needed on certain days—providing another layer of insight for optimizing contract placements.

<img width="860" alt="Hours worked per day by nurse type" src="https://github.com/user-attachments/assets/3e2806d6-f444-4e2d-aca7-277785702294" />

To gain a deeper understanding of working hour distributions and nurse demand patterns, the state of California—representing the largest market—was examined in greater detail.

<img width="846" alt="Hours worked by Nurse CA" src="https://github.com/user-attachments/assets/2febb725-e98f-4c8c-892f-768701169610" />

These patterns suggest that while weekday staffing should be a primary focus, weekend coverage remains critical for clinical roles. The sales team can use this insight to prioritize outreach based on both role type and day of the week, helping facilities stay fully staffed and responsive to patient care demands.

- Prioritize outreach to facilities on Tuesdays through Thursdays, aligning with peak workload periods.

- Focus heavily on CNA, LPN, and RN roles, which consistently show the highest demand.

- Tailor weekend staffing strategies to clinical roles only, as administrative needs sharply decline during that time.

# Recomendation 3: Targeting High-Occupancy Facilities

To better identify potential staffing needs, I created a new column called Occupancy Rate, which measures how fully a facility's available capacity is being utilized. This was calculated by dividing the average number of residents per day by the number of certified beds for each facility.

The rationale behind this metric is simple: If a facility consistently operates at or above 80% occupancy, it likely indicates a higher workload for staff, potential signs of stress or overextension, and ultimately a greater need for staffing support. For this analysis, I defined a “high occupancy” facility as one where the occupancy rate is ≥ 80%. These facilities were then flagged as higher-priority opportunities for staffing intervention.

<img width="848" alt="Occupancy Rate Scatter plot" src="https://github.com/user-attachments/assets/d5742a0c-cc88-4338-bf15-7614c8ffba09" />

The findings of the scatter plot are then visualized based on the percentage per state of facilities with high and normal occupancy rates. A review of facilities across multiple states reveals several consistent trends that highlight where staffing efforts should be prioritized. High demand is evident, with a significant number of facilities—particularly in states like California, South Carolina, North Carolina, and New Jersey—operating at or above 80% occupancy. This indicates ongoing or imminent strain on staffing resources.

<img width="846" alt="Occupancy Rates pie chart" src="https://github.com/user-attachments/assets/7b978b92-ccb3-4ee6-b562-b1c3932f2cc9" />

Next these high occupancy facilities are grouped for each state by facility type and ownership type, enabling the sales team to target their efforts more percise on industry needs.
Dominance of Skilled Nursing Facilities
Across nearly all states, Skilled Nursing Facilities (brown slice) consistently make up the largest share of high-occupancy institutions:

<img width="843" alt="Facilities with high occupancy" src="https://github.com/user-attachments/assets/432b9336-4dd9-4159-8bab-121d21762309" />

## Dominance of Skilled Nursing Facilities
- NC (43.4%), LA (43.2%), CA (24.0%), WA (30.0%), and MI (25.1%) show a strong presence of this facility type.
This suggests that Skilled Nursing Facilities are regularly operating near or at capacity, pointing to higher demand and potential staffing shortages — especially in states like NC and LA.

## Nursing Homes Are a Close Second
- States like GA (30.2%), NJ (38.0%), and ID (28.1%) show a notable presence of Nursing Homes in the high occupancy group. This aligns with the aging population and highlights long-term care facilities as consistent pressure points.

## Post-Acute and General Healthcare Stand Out in CA and SC
- Post-Acute Care (purple) is significant in CA (21.2%) and SC (15.3%). General Healthcare facilities are notably present in CA (16.0%), SC (19.7%), and OR (9.5%). These indicate that in certain states, even general medical and transitional care settings are nearing full occupancy, which is less common nationally.

## The “Unknown” Category
- The “Unknown” category still has room for potential and key insights but the approach worked very well for the state of California, enabling me to see the spread of healthcare facilities. As mentioned earlier, this is due to facilities where no clear categorization could be assigned through name parsing. This limits the full interpretability of the data — but can be improved with further manual verification or by scraping data from CMS/NPI databases using the facility ID or name.
---
The landscape is largely dominated by for-profit ownership, especially facilities owned by individuals and corporations. These types of facilities tend to operate on tighter budgets, making them more susceptible to the impact of staff shortages, while also being more flexible and responsive when it comes to implementing staffing solutions. Additionally, high-occupancy facilities are frequently concentrated in a few core categories such as Skilled Nursing, Assisted Living, and Memory Care. These settings are labor-intensive and require specialized staff, and in many states, just two to three of these facility types account for as much as 60–80% of the total.

<img width="864" alt="High Occupancy by Ownership" src="https://github.com/user-attachments/assets/444a5162-7c1a-4f09-aebd-2421ef4307f2" />

## Top 3 States to Target (Based on High Occupancy):
## 1. California (CA)
- Occupancy: 84.3% of facilities are ≥80% full (Extremely high demand due to high occupancy).

- Ownership Type: Dominated by For-profit Individual (53%) and Corporation (31%). Privately owned facilities suggest more flexible staffing decisions.

- Facility Type: Spread out but largest share in Residential care (24%), Skilled Nursing (21%), and Assisted Living (16%).

## 2. South Carolina (SC)
- Occupancy: 74.5% ≥80% occupancy — among the highest.

- Ownership Type: Mostly For-profit Individual (47%) and Corporation (31%). High occupancy and privately owned structure create pressure to retain staff.

- Facility Type: Fairly concentrated across Skilled Nursing, Assisted Living, and Memory Care.

## 3. New Jersey (NJ)
- Occupancy: 61.9% of facilities are ≥80% full.

- Ownership Type: Strong presence of For-profit Individual (42%) and Corporation (28%). Clear concentration in two key facility types makes targeted staffing more efficient.

- Facility Type: Dominated by Skilled Nursing (40.8%) and Assisted Living (38%). High private ownership simplifies implementation.


## Recommendation 4: Focus on States with Score Gaps of 7 or more Points and Low Ratings
In this section, I analyze the gap between Adjusted Scores and Expected Scores for nursing facilities. A significant gap may indicate a discrepancy between how a facility is expected to perform and how it actually performs based on claims data. By creating a has_big_gap flag for facilities with a gap ≥7 points, I am able to visualize where these discrepancies are concentrated across states. This allows for the identification of states with the highest number of facilities exhibiting unexpectedly poor performance or underreporting issues. These insights can help prioritize auditing efforts, uncover systemic problems, or highlight areas where facilities might require additional support or oversight.

<img width="854" alt="Scoregaps stacked chart" src="https://github.com/user-attachments/assets/ff6807be-ea1e-4123-9fd0-a3d6862b52e6" />

To gain a deeper understanding of working hour distributions and nurse demand patterns, each state was examined in greater detail. This close-up view allowed for a more focused analysis of staffing dynamics and facility behaviors. To dig deeper into potential causes behind observed discrepancies, I cross-analyzed score gaps with ownership type, centering the analysis on the three most prevalent structures: For-profit Corporations, For-profit Limited Liability Companies, and Non-profit Corporations. This comparison enabled me to explore whether structural differences in governance and financial incentives may correlate with performance misalignment, such as lower expected scores or higher turnover rates. By doing so, I aimed to uncover patterns that could inform more targeted outreach strategies depending on the ownership model.

<img width="850" alt="scoregaps by owner type" src="https://github.com/user-attachments/assets/a47d1b8e-45d6-420c-bbf5-362c0ed1e4bd" />

Furthermore, because ownership type alone does not fully capture the operational dynamics of healthcare facilities, I expanded the analysis to include facility type as a key variable. Specifically, I focused on the three most common categories in the dataset: Rehabilitation Centers, General Healthcare Facilities, and Care Centers. These facility types are not only widely represented, but also functionally distinct in terms of the services they provide, the complexity of care, and how staffing resources are allocated. By layering facility type onto the ownership analysis, I was able to better assess how structural and operational characteristics together may influence the likelihood of large score gaps—ultimately helping to pinpoint where inefficiencies or misalignments in care delivery may be occurring.

<img width="866" alt="scoregaps by facility" src="https://github.com/user-attachments/assets/619442a4-f063-489d-bb30-93c4b7011b44" />

Analyzing the relationship between overall facility ratings and nursing staff turnover rates provides a high-level view of organizational health and workforce stability. Facilities with lower ratings often face systemic challenges that can contribute to higher turnover, such as understaffing, low morale, or poor management practices. By examining turnover across different rating levels, we can begin to identify trends and patterns that suggest whether staffing instability is a potential driver of poor performance or vice versa. This insight is especially valuable for stakeholders aiming to improve care quality, as reducing turnover is both a symptom and a solution to deeper operational issues.

<img width="854" alt="Nursing Staff Turnover by Rating" src="https://github.com/user-attachments/assets/0b6b6750-d6fe-490c-a802-b69f0f1a54f5" />

Facilities with a discrepancy of 7 or more points between their expected and adjusted scores may be signaling deeper quality or reporting issues—especially when these facilities also hold low overall ratings (1–3 stars). By analyzing these overlaps, I identified specific states—such as California, Michigan, and North Carolina—where the problem is most concentrated. These states also exhibit higher levels of nursing staff turnover, particularly in lower-rated institutions, reinforcing concerns around staffing stability and patient care.

In addition, ownership analysis shows that “For-profit – Limited Liability Companies” are often the most associated with score gaps. When layered with facility type, Rehabilitation Centers emerge as the most frequent among high-gap facilities, indicating a potential link between care complexity and quality consistency.

To improve national standards, Clipboard Health's sales team should focus on these high-risk intersections of geography, ownership, and facility type.

- California, Michigan, New Jersey and North Carolina have the highest number of facilities with ≥7 point score gaps, many of which are also low-rated and high in staff turnover.

- For-profit – Limited Liability Companies dominate the ownership of facilities with the most significant discrepancies.

- Rehabilitation Centers are the most common facility type among high-gap institutions, suggesting targeted complexity challenges.
