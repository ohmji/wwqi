# Update Pages Index Command

Updates wwqi/analysis/index.md and quant/wwqi/index.md when new analysis files are found in wwqi/analysis directory.

## Command Usage

```bash
# Run the update pages command
update_pages
```

## What This Command Does

1. **Scans wwqi/analysis directory** for all analysis files (*.md, *.html)
2. **Extracts key information** from each analysis file:
   - Ticker symbol
   - Company name  
   - Business sector/category
   - Investment recommendation
   - Analysis date
   - Key insights/summary
3. **Updates wwqi/analysis/index.md** with new analysis cards in the appropriate sector sections
4. **Updates quant/wwqi/index.md** portfolio holdings section with latest positions
5. **Maintains proper formatting** and styling for both pages

## File Pattern Recognition

The command recognizes these analysis file patterns:
- `TICKER_analysis_YYYYMMDD.md` - Full investment analysis
- `TICKER_business_explanation_YYYYMMDD.md` - Business model analysis  
- `TICKER_management_governance_analysis_YYYYMMDD.md` - Management analysis

## Auto-Detection Features

### Ticker Extraction
- Extracts ticker from filename (e.g., COST from `COST_analysis_20250921.md`)
- Handles special cases like multi-word tickers

### Sector Classification
- **Technology & Software**: Software, SaaS, Tech platforms
- **Consumer & Retail**: E-commerce, Retail, Consumer discretionary
- **Consumer Staples & Transportation**: Food/Beverage, Transportation, Utilities
- **Healthcare & Pharmaceuticals**: Healthcare, Biotech, Medical devices
- **Financial Services**: Banks, Insurance, Fintech
- **Energy & Materials**: Energy, Mining, Commodities

### Recommendation Mapping
- Extracts investment recommendations from analysis content
- Maps to visual classes: `buy`, `hold`, `sell`, `cautious`
- Default fallback: `hold` if recommendation not clearly identified

## Implementation Steps

### 1. Analysis File Discovery
```bash
# Find all analysis files
find wwqi/analysis -name "*_analysis_*.md" -o -name "*_business_explanation_*.md" -o -name "*_management_*.md"
```

### 2. Content Extraction
For each file, extract:
- **Ticker**: From filename pattern
- **Company Name**: From title/header in content
- **Recommendation**: From analysis conclusions
- **Key Insight**: Summary sentence from executive summary
- **Date**: From filename or content date

### 3. Index Page Updates

#### wwqi/analysis/index.md Updates
- Add new analysis cards to appropriate sector sections
- Update analysis statistics (counts by recommendation, sector)
- Maintain chronological ordering (newest first)
- Update meta statistics at bottom

#### quant/wwqi/index.md Updates  
- Update portfolio holdings section with latest positions
- Sync stock prices (if available)
- Update recommendation badges
- Maintain consistent styling

### 4. Template for New Analysis Cards

```html
<a href="TICKER_analysis_YYYYMMDD.html" class="analysis-card">
  <div class="analysis-header">
    <span class="analysis-ticker">TICKER</span>
    <span class="analysis-recommendation [buy|hold|sell|cautious]">RECOMMENDATION</span>
  </div>
  <h3>Company Name - Business Description</h3>
  <p class="analysis-insight">Key insight or summary</p>
  <div class="analysis-meta">
    <span class="analysis-date">Month DD, YYYY</span>
    <span class="analysis-status">=� View Analysis</span>
  </div>
</a>
```

### 5. Smart Deduplication
- Check existing entries before adding new ones
- Update existing entries if newer analysis available
- Remove outdated analysis references

## Error Handling

- **Missing files**: Skip gracefully with warning
- **Parse errors**: Use fallback values (default to HOLD recommendation)
- **Invalid dates**: Use file modification time as fallback
- **Missing company names**: Use ticker as fallback

## Example Workflow

```bash
# 1. User creates new analysis file
touch wwqi/analysis/NVDA_analysis_20250921.md

# 2. Run update command  
update_pages

# 3. Command automatically:
#    - Detects new NVDA analysis
#    - Extracts NVIDIA as company name
#    - Classifies as Technology & Software
#    - Adds card to analysis/index.md Technology section
#    - Updates portfolio on main index.md
#    - Updates statistics counters
```

## Future Enhancements

- **Auto-categorization** using AI analysis of business description
- **Price integration** with real-time stock data APIs
- **Performance tracking** by comparing recommendations to actual returns
- **Alert system** for significant changes in analysis recommendations
- **Backup/versioning** of index pages before updates

---

This command ensures both index pages stay automatically synchronized with the latest analysis files, maintaining consistency and reducing manual maintenance work.