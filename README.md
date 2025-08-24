# Smithfield Crime Dashboard

A comprehensive automated crime data tracking and analysis system for Smithfield, Virginia, providing real-time insights and weekly reports on local crime statistics and safety trends.

## Project Overview

The Smithfield Crime Dashboard is designed to collect, process, and analyze crime data from multiple authoritative sources to provide residents, local government, and community organizations with accurate, up-to-date information about public safety in Smithfield, VA. 

### Key Features
- **Automated Daily Data Collection**: Fetches the latest crime statistics from multiple data sources
- **Real-time Processing**: Cleans, validates, and processes raw crime data for analysis
- **Weekly Analytics**: Generates comprehensive reports with trends, insights, and visualizations
- **Notion Integration**: Automatically publishes reports to Notion workspace for easy sharing
- **API Endpoints**: Provides programmatic access to processed crime data
- **Historical Tracking**: Maintains comprehensive crime data history for trend analysis

## Data Sources

### Primary Sources
1. **CrimeGrade.org**
   - Comprehensive crime statistics and safety ratings
   - Real-time incident reporting
   - Neighborhood safety scores
   - API Documentation: [CrimeGrade.org API](https://crimegrade.org/api)

2. **NeighborhoodScout**
   - Detailed neighborhood safety analytics
   - Demographic correlation data
   - Comparative regional statistics
   - Risk assessment metrics

### Data Coverage
- **Geographic Area**: Smithfield, VA and surrounding 10-mile radius
- **Update Frequency**: Daily at 6:00 AM UTC
- **Historical Data**: Up to 365 days of retained data
- **Data Types**: Incident reports, safety ratings, demographic correlations, trend analysis

## Automation Goals

### Daily Operations
- **6:00 AM UTC**: Automated data fetch from all configured sources
- **Data Validation**: Automatic cleaning and validation of incoming data
- **Error Handling**: Comprehensive logging and alert system for data issues
- **Version Control**: Automatic commit of processed data updates

### Weekly Operations
- **Monday 8:00 AM UTC**: Generate comprehensive weekly reports
- **Trend Analysis**: Compare current week with historical data
- **Visualizations**: Create charts and graphs for key metrics
- **Notion Publishing**: Automatically publish reports to configured Notion workspace

### Integration Features
- **GitHub Actions**: Fully automated CI/CD pipeline
- **API Access**: RESTful API for external integrations
- **Multiple Formats**: Export data in JSON, CSV, and HTML formats
- **Backup System**: Automated data backup and retention policies

## Project Structure

```
smithfield-crime-dashboard/
├── README.md                 # Project documentation
├── LICENSE                   # MIT License
├── data/                     # Crime data storage
│   ├── raw/                  # Raw data from external sources
│   └── processed/            # Cleaned and validated data
├── src/                      # Source code modules
│   ├── fetch/                # Data fetching modules
│   ├── parse/                # Data parsing and cleaning
│   ├── api/                  # API server components
│   └── utils/                # Utility functions
├── scripts/                  # Automation scripts
│   ├── update_crime_data.py  # Daily data update script
│   └── generate_reports.py   # Weekly report generation
├── config/                   # Configuration files
│   └── sources.json          # Data source configurations
└── .github/workflows/        # GitHub Actions automation
    └── update.yml            # Daily update and weekly report workflow
```

## Getting Started

### Prerequisites
- Python 3.11 or higher
- Git
- API keys for configured data sources (see Configuration section)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/repo-ranger21/smithfield-crime-dashboard.git
   cd smithfield-crime-dashboard
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt  # TODO: Create requirements.txt
   ```

3. Configure environment variables (see Configuration section)

4. Run initial data fetch:
   ```bash
   python scripts/update_crime_data.py
   ```

### Configuration

Set up the following environment variables or GitHub secrets:
- `CRIMEGRADE_API_KEY`: API key for CrimeGrade.org
- `NEIGHBORHOODSCOUT_API_KEY`: API key for NeighborhoodScout
- `NOTION_API_KEY`: Notion integration API key
- `NOTION_WORKSPACE_ID`: Target Notion workspace ID
- `NOTION_DATABASE_ID`: Target Notion database ID

Configuration settings can be modified in `config/sources.json`.

## Usage

### Manual Data Update
```bash
python scripts/update_crime_data.py
```

### Generate Reports
```bash
python scripts/generate_reports.py
```

### View Processed Data
Processed data is stored in `data/processed/` in JSON and CSV formats.

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature/new-feature`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For questions, issues, or contributions, please:
1. Check existing [Issues](https://github.com/repo-ranger21/smithfield-crime-dashboard/issues)
2. Create a new issue with detailed description
3. Follow the contributing guidelines for pull requests

---

*This project is maintained by the community for the benefit of Smithfield residents and local organizations. Data accuracy depends on source reliability and is provided for informational purposes only.*