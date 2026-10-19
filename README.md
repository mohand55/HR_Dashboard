# 📊 HR Analytics Dashboard (Power BI)

An interactive **Power BI** dashboard that gives HR a clear view of **hiring**, **sick leaves**, and **employee satisfaction** across the company. It has a home page with navigation buttons and three analysis pages, all filterable with slicers.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `HR_Dashboard.pbix` | The Power BI Desktop report (data model, measures, visuals) |
| `HR_Dashboard.pdf` | A static export of all pages for quick preview |
| `README.md` | Project documentation |

> To open the `.pbix` file you need **Power BI Desktop** (free, Windows): https://powerbi.microsoft.com/desktop

---

## 🗂️ Dashboard Pages

### 1. Home Page
Landing page titled **HR Analytics** with navigation buttons to:
- Hiring Information
- Sick Leaves Information
- Satisfaction Information

### 2. Hiring Information
Answers: *Where and how are we hiring, and in which departments/roles?*

| Visual | What it shows |
|--------|---------------|
| Card – **Total Employees** | Headcount (**1,000** employees) |
| Bar chart – **Hiring by Hiring Source** | LinkedIn (209), Walk-in (207), Agency (204), Website (204), Referral (176) |
| Column chart – **Hiring by Department** | New hires per department |
| Column chart – **Hiring by Job Title** | Employees per job title (Manager, Engineer, Coordinator, Executive, Developer, Analyst, …) |
| Line chart – **Hiring Over Months** | New hires per month (peak in June, lowest in November) |
| Slicers | Month, Department, Hiring Source, Job Title |

### 3. Sick Leaves Information
Answers: *How much sick leave is taken, why, and by whom?*

| Visual | What it shows |
|--------|---------------|
| Card – **Number of Sick Leave Cases** | **2,500** cases |
| Card – **Avg Sick Leave Days per Case** | **3.05** days |
| Card – **Avg Annual Leave Balance** | **15.03** days |
| Card – **Avg Sick Leave Balance** | **7.32** days |
| Clustered bar – **Cases & Total Days by Department** | Engineering (452) · Marketing (436) · Finance (432) · Sales (412) · IT Support (405) · HR (363) |
| Column – **Total Sick Leave Days by Reason** | Back Pain, Headache, COVID, Stress, Flu |
| Column – **Cases by Reason** | Back Pain (532), COVID (520), Headache (506), Flu (474), Stress (468) |
| Line/column – **Cases by Month** | Monthly trend (peak in August, lowest in February) |
| Slicers | Month, Department, Reason |

### 4. Satisfaction Information
Answers: *How satisfied are employees, and does it relate to sick leave?*

| Visual | What it shows |
|--------|---------------|
| Card – **Avg Satisfaction Score** | **5.50** overall |
| Column – **Avg Satisfaction by Department** | HR 5.8 · Marketing 5.6 · IT Support 5.6 · Sales 5.6 · Finance 5.4 · Engineering 5.1 |
| Scatter – **Satisfaction vs. Sick Leave Cases** | One point per department, to explore the relationship between the two |

---

## 🔍 Key Insights

- **Hiring sources are well balanced** – LinkedIn leads slightly; Referral is the lowest-performing channel.
- **Engineering** has the most sick-leave cases **and** the lowest satisfaction score (5.1) – worth investigating.
- **HR** has the fewest sick-leave cases and the highest satisfaction (5.8).
- **Back Pain** is the top sick-leave reason by both cases and total days.
- Average sick leave duration is about **3 days per case**.

---

## 🧮 Data Model

| Table | Purpose |
|-------|---------|
| `Employees` | Employee details (Department, JobTitle, satisfaction, leave balances) |
| `Hiring` | Hiring records (Hiring Source) |
| `SickLeaves` | Sick leave records (Reason, days) |
| `Date` | Calendar table (Month, Short Month) |
| `_Measure` | Dedicated table holding all DAX measures |

### DAX Measures
`Total Employees` · `New Hires` · `Number Of Sick Leave Cases` · `Total Sick Leave Days` · `Average Sick Leave Days Per Days` · `Average Annual Leave Balance` · `Average Sick Leave Balance` · `Average Satisfaction Score`

---

## 🛠️ Tools & Skills Demonstrated

- Power BI Desktop
- Data modeling (star schema, date table)
- DAX measures
- Interactive slicers & page navigation
- Dashboard design (black & grey theme, custom icons)
