---
layout: default
title: Home
---

# Charlie Munger Investment Analysis Framework

> *"It is remarkable how much long-term advantage people like us have gotten by trying to be consistently not stupid, instead of trying to be very intelligent."*
> 
> — Charlie Munger

## About This Portfolio

This site showcases systematic investment analysis following Charlie Munger's time-tested principles:

- **Circle of Competence:** Only analyze businesses we truly understand
- **Mental Models:** Apply multidisciplinary thinking from psychology, economics, math, and science
- **Margin of Safety:** Buy quality businesses at significant discounts to intrinsic value
- **Long-term Thinking:** Hold great businesses for decades, not quarters
- **Quality over Quantity:** Concentrate on excellent opportunities

## Navigation

### 📊 [Analysis Portfolio](/analysis/)
Individual company analyses following the complete Munger framework

### 💼 [Portfolio Management](/portfolio/)
Current positions, watchlists, and portfolio construction guidelines

### 🧠 [Framework Documentation](/framework/)
Complete methodology, mental models, and analysis checklists

---

## Latest Analyses

{% for analysis in site.analyses limit:5 %}
- [{{ analysis.title }}]({{ analysis.url }}) - {{ analysis.date | date: "%B %d, %Y" }}
{% endfor %}

## Current Holdings Summary

| Company | Ticker | Position | Thesis | Status |
|---------|---------|----------|---------|---------|
| Costco | COST | Hold | Quality business, overvalued | Monitor for entry |
| Coca-Cola | KO | Qualified Buy | Defensive dividend aristocrat | Fair value |
| Lululemon | LULU | Hold/Weak Buy | Turnaround opportunity | Undervalued |

## Key Metrics Dashboard

### Portfolio Performance
- **Total Return (YTD):** To be updated
- **Sharpe Ratio:** To be updated  
- **Maximum Drawdown:** To be updated
- **Alpha vs S&P 500:** To be updated

### Analysis Statistics
- **Companies Analyzed:** 5+
- **Industries Covered:** Technology, Consumer, Aerospace, Retail
- **Average Analysis Time:** 12-18 hours per company
- **Recommendation Accuracy:** Track record building

---

## Recent Updates

**September 2025:**
- ✅ Completed Rocket Lab (RKLB) analysis
- ✅ Updated Costco (COST) valuation assessment  
- ✅ Added business explanation command framework
- 🔄 Monitoring Figma post-IPO performance

**Investment Philosophy Reminders:**
- Patience over activity
- Understanding over speculation  
- Quality over price alone
- Long-term compounding focus

---

*This site documents a systematic approach to value investing. All analysis is for educational purposes. Please consult qualified financial advisors for investment decisions.*