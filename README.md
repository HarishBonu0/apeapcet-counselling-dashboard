# APEAPCET Engineering Counselling Dashboard

An interactive Power BI dashboard designed to analyze and visualize APEAPCET (Andhra Pradesh Engineering, Agriculture and Pharmacy Common Entrance Test) engineering college admission data. This project provides comprehensive insights into student admissions across various engineering colleges in Andhra Pradesh.

## Live Dashboard

**View Dashboard:** [Power BI Dashboard Link](https://app.powerbi.com/view?r=eyJrIjoiMzcyMzkzMWUtMjdkNS00NmRhLTllYjYtOWQzZjhhOGI3OWY2IiwidCI6IjFjZGYzNGYzLTA4ZjktNDNlYi05ZDRmLTJiYTRhMWQyMGE2ZiJ9&embedImagePlaceholder=true)

## Project Overview

This dashboard serves as a decision-making tool for students, parents, and education counselors by providing data-driven insights into engineering college admissions. It analyzes historical admission data to help prospective students make informed choices about college and branch selection based on their APEAPCET rank.

### Key Features

**Interactive Filters**
- Rank-based filtering (160 - 179,813)
- College selection (ANIL, AU, GMRI, GVPE, JNTK, MVRG, RVCJ, and more)
- Category filtering (OC, BC_A, BC_B, BC_C, BC_D, BC_E, SC_I, SC_II, SC_III)
- Branch selection (CSE, ECE, EEE, MECH, CIV, and 20+ branches)
- Region-based filtering

**Key Metrics**
- Total available seats: 9,368
- Rank range analysis: 160 to 180,000+
- Gender distribution insights
- Phase-wise admission tracking

### Visualizations

1. **Students by College** - Bar chart showing admission distribution across engineering colleges
2. **Caste Category Distribution** - Donut chart displaying category-wise seat allocation
3. **Counselling Phase Analysis** - Pie chart comparing Phase 1 and Phase 2 admissions  
4. **Gender Distribution** - Treemap visualization of male vs female admissions
5. **Branch Popularity** - Column chart showing student preferences across engineering branches
6. **Detailed Data Table** - Comprehensive table with College, Branch, Category, Min Rank, Max Rank, and Average Rank

## Data Insights

**Top Engineering Colleges by Admissions:**
- KGRL, RVC, ANIL, HITAM, MVGR

**Category Distribution:**
- OC: 25.71%
- BC_D: 23.33%
- BC_A: 15.16%
- BC_B: 10.86%
- Other categories: 25%

**Counselling Phases:**
- Phase 1: 66% (6,310 students)
- Phase 2: 34% (3,120 students)

**Popular Engineering Branches:**
- Computer Science Engineering (CSE)
- Electronics & Communication (ECE)
- Electrical & Electronics (EEE)
- Mechanical Engineering (MECH)

## Use Cases

**For Students:**
- Determine college accessibility based on rank
- Compare branch cutoff ranks across colleges
- Analyze admission trends by category
- Plan college preferences for counselling

**For Education Counselors:**
- Provide data-backed counselling
- Track historical admission patterns
- Assist students in realistic goal setting

**For Researchers:**
- Analyze admission trends over counselling phases
- Study gender distribution in engineering
- Research category-wise representation

## Technical Details

**Technology Stack:**
- Microsoft Power BI Desktop
- DAX (Data Analysis Expressions) for measures
- Power Query (M Language) for data transformation

**Data Model:**

The dashboard utilizes a star schema with the following structure:
- **Fact Table:** Student admissions (StudentID, Rank, College, Branch, Category, Gender, Phase)
- **Dimension Tables:** Colleges, Branches, Categories, Regions

**Key DAX Measures:**
```dax
Total Seats = COUNT(Students[StudentID])
Lowest Rank = MIN(Students[Rank])
Highest Rank = MAX(Students[Rank])
Average Rank = AVERAGE(Students[Rank])
```

## Data Dictionary

| Field | Type | Description |
|-------|------|-------------|
| College | Text | Engineering college code (ANIL, AU, GMRI, etc.) |
| Branch | Text | Engineering specialization (CSE, ECE, MECH, etc.) |
| Caste | Text | Category (OC, BC, SC, ST) |
| Rank | Integer | APEAPCET examination rank (160-179,813) |
| Gender | Text | Student gender (M/F) |
| Phase | Integer | Counselling phase (1 or 2) |
| Region | Text | Geographical region |

## Engineering Branches

- **BIO** - Bio-Technology
- **CAD** - Computer Aided Design  
- **CSE** - Computer Science & Engineering
- **CSE(DA)** - CSE - Data Analytics
- **CSM** - Computer Science (AI & ML)
- **ECE** - Electronics & Communication
- **EEE** - Electrical & Electronics
- **MECH** - Mechanical Engineering
- **CIV** - Civil Engineering
- **CHE** - Chemical Engineering
- And 15+ more branches

## Project Structure

```
apeapcet-counselling-dashboard/
├── README.md
├── LICENSE
├── docs/
│   ├── USER_GUIDE.md
│   ├── DATA_DICTIONARY.md
│   └── TECHNICAL_DOCUMENTATION.md
├── data/
│   ├── sample_data.xlsx
│   └── data_sources.md
├── images/
│   ├── dashboard_overview.png
│   ├── filters_demo.png
│   └── visualizations.png
└── powerbi/
    ├── APEAPCET_Dashboard.pbix
    └── dax_measures.txt
```

## Getting Started

**Prerequisites:**
- Microsoft Power BI Desktop (latest version)
- Basic understanding of Power BI dashboards

**Viewing the Dashboard:**
1. Click on the live dashboard link provided above
2. Use interactive filters to explore data
3. Hover over visualizations for detailed insights
4. Click on charts to cross-filter the entire dashboard

**For Development:**
1. Clone this repository
2. Open the .pbix file in Power BI Desktop  
3. Connect to your data source
4. Refresh data to update visualizations

## Example Queries

**Query 1: Can I get CSE at ANIL with rank 5000?**
- Set Rank filter: 4500-5500
- Select College: ANIL
- Select Branch: CSE
- Check Min/Max rank in the data table

**Query 2: Which colleges offer CSE in OC category?**
- Select Branch: CSE
- Select Category: OC
- Review the "Students by College" chart
- Check detailed rank ranges in the table

**Query 3: Compare Phase 1 vs Phase 2 admissions**
- Click on Phase 1 segment in the pie chart
- Note the filtered metrics
- Click on Phase 2 to compare

## Future Enhancements

- Historical trend analysis across multiple years
- Predictive analytics for cutoff rank estimation  
- Mobile-responsive dashboard version
- Integration with real-time counselling data
- Advanced filtering by college location and facilities

## Contributing

Contributions are welcome. Please follow these steps:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Harish Bonu**
- GitHub: [@HarishBonu0](https://github.com/HarishBonu0)
- LinkedIn: [Connect with me](https://linkedin.com/in/harishbonu)

## Acknowledgments

- APEAPCET officials for providing admission data
- Engineering colleges across Andhra Pradesh
- Microsoft Power BI community

## Disclaimer

This dashboard is created for educational and analytical purposes. All data is based on publicly available APEAPCET counselling information. Please verify critical decisions with official APEAPCET counselling authorities.

---

**Note:** For detailed usage instructions, refer to the [User Guide](docs/USER_GUIDE.md).
