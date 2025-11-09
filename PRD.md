# Product Requirements Document (PRD)
# Stock Analysis Tool - Financial Thumb Rules Calculator

**Version:** 1.0  
**Last Updated:** November 2025  
**Status:** Initial Release

---

## 1. Executive Summary

The Stock Analysis Tool is a web-based calculator designed to provide quick, rule-based financial analysis of Indian stocks listed on NSE/BSE. It implements proven "thumb rules" from fundamental analysis to help retail investors and analysts make informed preliminary assessments of stock valuations and financial health.

### Problem Statement
Retail investors often struggle with:
- Complex financial ratio calculations
- Understanding what constitutes "good" or "bad" metrics
- Comparing company metrics against industry benchmarks
- Making quick preliminary screening decisions

### Solution
A real-time calculator that instantly evaluates 12 critical financial metrics, provides color-coded visual feedback, and generates actionable recommendations (BUY/HOLD/CAUTION/SELL) based on established financial analysis principles.

---

## 2. Product Overview

### 2.1 Purpose
To democratize stock analysis by providing an easy-to-use tool that:
- Simplifies complex financial calculations
- Applies expert-level thumb rules automatically
- Provides instant, visual feedback on stock health
- Helps users identify potential investment opportunities or red flags

### 2.2 Target Users

**Primary Users:**
- Retail investors conducting preliminary stock research
- Financial analysts performing quick screening
- Finance students learning fundamental analysis
- Investment club members evaluating stocks

**User Personas:**

1. **Beginner Investor (Rahul, 28)**
   - New to stock market
   - Needs guidance on what metrics mean
   - Wants clear buy/sell signals
   - Uses tool for learning and decision support

2. **Active Trader (Priya, 35)**
   - Experienced investor
   - Screens multiple stocks daily
   - Uses tool for quick preliminary checks
   - Combines with deeper research

3. **Finance Student (Arjun, 22)**
   - Learning fundamental analysis
   - Wants to understand ratio calculations
   - Uses tool to practice and verify calculations
   - References thumb rules for exam preparation

---

## 3. Core Features & Functionality

### 3.1 Input Capabilities

**Valuation Metrics:**
- Price to Earnings (P/E) Ratio
- Sector Average P/E
- Price to Book (P/B) Ratio
- Price to Sales (P/S) Ratio

**Profitability Metrics:**
- Return on Equity (ROE) %
- Return on Capital Employed (ROCE) %
- EBITDA Margin %
- PAT (Profit After Tax) Margin %

**Balance Sheet Metrics:**
- Interest Coverage Ratio
- Debt to Equity Ratio

**Other Metrics:**
- Promoter Holding %
- RSI (Relative Strength Index)

### 3.2 Analysis Engine

**Automated Calculations:**
- Real-time evaluation as users input data
- Automatic comparison against thumb rule benchmarks
- Scoring system (0-100) for overall health

**Evaluation Logic:**

1. **P/E Ratio Analysis**
   - Good: < 15x
   - Fair: 15-25x
   - Caution: 25-30x
   - Expensive: > 30x
   - Context: Compare with sector average

2. **P/B Ratio Analysis**
   - Undervalued: < 1.5x
   - Fair: 1.5-3x
   - High: 3-5x
   - Very Expensive: > 5x

3. **Interest Coverage**
   - Good: > 4x (comfortable debt servicing)
   - Acceptable: 3-4x
   - Warning: < 3x (debt stress)

4. **Debt to Equity**
   - Conservative: < 0.5
   - Moderate: 0.5-1.0
   - High Leverage: > 1.0

5. **Promoter Holding**
   - Strong: > 50%
   - Moderate: 30-50%
   - Low: < 30%

6. **ROE & ROCE**
   - Excellent: > 20%
   - Good: 15-20%
   - Average: 10-15%
   - Poor: < 10%

7. **Margin Analysis**
   - Compare EBITDA and PAT margins with sector averages
   - Flag declining margins

8. **RSI Technical Indicator**
   - Overbought: > 70 (potential sell)
   - Neutral: 30-70
   - Oversold: < 30 (potential buy)

### 3.3 Output & Visualization

**Visual Feedback System:**
- Green cards: Positive metrics (good financial health)
- Yellow cards: Caution metrics (needs attention)
- Red cards: Warning metrics (potential red flags)

**Overall Rating:**
- **BUY**: Score 75-100 (Strong fundamentals)
- **HOLD**: Score 50-74 (Decent fundamentals, wait for better entry)
- **CAUTION**: Score 25-49 (Weak fundamentals, risky)
- **SELL**: Score < 25 (Poor fundamentals, avoid)

**Detailed Insights:**
- Each metric card shows:
  - Actual value
  - Interpretation (what it means)
  - Signal (actionable advice)
  - Visual status indicator

---

## 4. Scope

### 4.1 In Scope

✅ **Included in Current Version:**
- 12 key financial ratios and metrics
- Real-time calculation and evaluation
- Visual status indicators (color-coded cards)
- Overall buy/hold/caution/sell recommendation
- Responsive design (mobile and desktop)
- Pre-filled example data for learning
- Based on Indian stock market context (NSE/BSE)
- Thumb rules from Zerodha Varsity and industry best practices

### 4.2 Out of Scope

❌ **NOT Included:**
- Live stock price fetching from APIs
- Historical data analysis or charting
- Automated data import from financial websites
- Portfolio management features
- Stock screening across multiple stocks
- Peer comparison tables
- Financial statement uploads
- Email alerts or notifications
- User authentication or saved analyses
- Payment processing
- Regulatory compliance (SEBI guidelines)
- Investment advisory services
- Automated trading integration

---

## 5. Technical Architecture

### 5.1 Technology Stack

**Frontend Framework:**
- Next.js 15 (React 19)
- TypeScript for type safety
- Tailwind CSS for styling

**Components:**
- shadcn/ui component library
- Responsive design patterns

**State Management:**
- React hooks (useState)
- Client-side computation (no backend)

**Deployment:**
- Vercel (recommended)
- Static export capable

### 5.2 Performance Requirements

- Page load time: < 2 seconds
- Calculation response: Instant (< 100ms)
- Mobile responsive: All screen sizes
- Browser support: Modern browsers (Chrome, Firefox, Safari, Edge)

---

## 6. Limitations & Disclaimers

### 6.1 Tool Limitations

**Data Input:**
- Manual entry only (no API integration)
- User responsible for data accuracy
- No validation of source data quality

**Analysis Scope:**
- Thumb rules are simplified heuristics, not comprehensive analysis
- Does not consider qualitative factors (management quality, brand value, moat)
- Does not analyze industry-specific metrics (e.g., NPA for banks, occupancy for hotels)
- No sector-specific adjustments to thumb rules

**Recommendation Limitations:**
- Recommendations are preliminary signals only
- Not personalized to individual risk tolerance
- Does not consider portfolio diversification
- Does not account for market conditions or macroeconomic factors

**Technical Limitations:**
- No historical data tracking
- No comparison with peer companies
- No chart patterns or advanced technical analysis
- Single stock analysis only (no batch processing)

### 6.2 Important Disclaimers

⚠️ **Investment Disclaimer:**
- This tool is for educational and informational purposes only
- NOT a substitute for professional financial advice
- NOT a recommendation to buy, sell, or hold securities
- Users should conduct comprehensive due diligence
- Past performance does not guarantee future results
- All investments carry risk of loss

⚠️ **Data Disclaimer:**
- Tool relies on user-provided data
- No guarantee of data accuracy or completeness
- Users should verify all data from official sources
- Tool does not validate input data quality

⚠️ **Liability:**
- No liability for investment losses
- No responsibility for data entry errors
- No guarantee of tool accuracy or availability

---

## 7. Use Cases

### 7.1 Primary Use Cases

**Use Case 1: Quick Stock Screening**
- **Actor:** Retail investor
- **Goal:** Quickly assess if stock deserves deeper research
- **Steps:**
  1. Gather financial data from screener/annual report
  2. Input 12 metrics into tool
  3. Review color-coded results
  4. Read overall recommendation
  5. Decide whether to proceed with detailed analysis

**Use Case 2: Learning Financial Analysis**
- **Actor:** Finance student
- **Goal:** Understand ratio calculations and interpretations
- **Steps:**
  1. Use pre-filled example data
  2. Observe how metrics are evaluated
  3. Modify inputs to see impact on ratings
  4. Learn thumb rule benchmarks
  5. Practice with real stock data

**Use Case 3: Comparative Analysis**
- **Actor:** Active investor
- **Goal:** Compare two stocks in same sector
- **Steps:**
  1. Analyze Stock A
  2. Note the scores and red flags
  3. Clear and analyze Stock B
  4. Compare metrics side-by-side (manually)
  5. Identify better investment opportunity

**Use Case 4: Red Flag Identification**
- **Actor:** Risk-averse investor
- **Goal:** Identify potential problems before investing
- **Steps:**
  1. Input company financial data
  2. Look for red/yellow warning cards
  3. Pay attention to debt metrics and coverage ratios
  4. Assess promoter holding strength
  5. Decide to avoid or investigate further

---

## 8. Success Metrics

### 8.1 User Engagement Metrics
- Daily active users (DAU)
- Average session duration
- Number of analyses performed per user
- Return user rate

### 8.2 Quality Metrics
- User satisfaction score (via feedback)
- Accuracy of thumb rule implementation
- Mobile vs desktop usage split
- Bounce rate

### 8.3 Business Metrics
- GitHub stars and forks
- Community contributions
- Feature requests submitted
- Educational institutions adopting tool

---

## 9. Future Enhancements (Roadmap)

### Phase 2 (Q2 2025)
- **Save & Export:** Export analysis as PDF/CSV
- **History:** Save past analyses locally
- **Comparison Mode:** Side-by-side comparison of 2-3 stocks
- **Sector Presets:** Pre-filled sector average benchmarks

### Phase 3 (Q3 2025)
- **API Integration:** Auto-fetch data from financial APIs (BSE/NSE)
- **Peer Comparison:** Automatic comparison with sector peers
- **Charts:** Visual charts for margin trends, ROE evolution
- **Advanced Metrics:** Industry-specific ratios (NIM for banks, inventory turnover, etc.)

### Phase 4 (Q4 2025)
- **Portfolio View:** Analyze multiple holdings
- **Alerts:** Notification when metrics change
- **Educational Mode:** Interactive tutorials and explanations
- **Mobile App:** Native iOS/Android applications

### Potential Features (Backlog)
- AI-powered insights and commentary
- News sentiment integration
- Regulatory filing alerts
- Screener integration (filter stocks by criteria)
- Community ratings and discussions

---

## 10. Dependencies & Assumptions

### 10.1 Assumptions
- Users have basic understanding of financial terms
- Users can access accurate financial data from other sources
- Users understand this is a screening tool, not final advice
- Internet connection available (for web app access)

### 10.2 External Dependencies
- Financial data providers (user responsibility)
- Annual reports and screener websites
- Browser compatibility
- Vercel hosting platform

---

## 11. Compliance & Legal

### 11.1 Regulatory Considerations
- Tool does not provide SEBI-regulated investment advice
- No client money handling
- No personalized recommendations
- Educational tool exemption applies

### 11.2 Privacy
- No user data collection
- No cookies or tracking (except standard analytics)
- No personal information required
- No data storage on servers

### 11.3 Open Source
- MIT License (permissive)
- Free for commercial and non-commercial use
- Attribution required
- Community contributions welcome

---

## 12. Glossary of Terms

**P/E Ratio:** Price to Earnings - measures stock price relative to earnings per share

**P/B Ratio:** Price to Book - compares market value to book value of equity

**ROE:** Return on Equity - profitability relative to shareholder equity

**ROCE:** Return on Capital Employed - profitability relative to total capital

**EBITDA Margin:** Operating profitability before interest, tax, depreciation

**Interest Coverage:** Ability to service debt (EBIT ÷ Interest expense)

**Promoter Holding:** Percentage of shares held by founders/promoters

**RSI:** Relative Strength Index - momentum indicator (0-100 scale)

---

## 13. References & Methodology Sources

This tool implements thumb rules and principles from:
- **Zerodha Varsity:** Fundamental Analysis & Technical Analysis modules
- **Screener.in:** Promoter holding thresholds and screening practices
- **Industry Best Practices:** Standard valuation benchmarks used by analysts

**Key References:**
1. Zerodha Varsity - Chapter on Financial Ratios
2. Zerodha Varsity - Valuation Metrics
3. Zerodha Varsity - Technical Analysis Indicators
4. Indian stock market analysis conventions

---

## 14. Contact & Support

**GitHub Repository:** [https://github.com/kaustuv96/Stock-Analysis-Tool]

**Issues & Bug Reports:** Use GitHub Issues

**Feature Requests:** GitHub Discussions

**Documentation:** README.md and inline comments

**Community:** Contributions welcome via Pull Requests

---

## 15. Approval & Sign-off

**Product Owner:** Kaustuv  
**Technical Lead:** NA  
**Release Date:** November 2025  
**Version:** 1.0

---

**Document Control:**
- This PRD is a living document
- Updates tracked via version control
- Major changes require stakeholder review
- Feedback incorporated through GitHub Issues

---

## Appendix A: Calculation Formulas

All formulas implemented as per the Stock Analysis Template document:

- **EPS** = PAT / Total Number of Shares
- **P/E Ratio** = Current Market Price / EPS
- **P/B Ratio** = Current Price / Book Value per Share
- **Book Value** = (Share Capital + Reserves) / Number of Shares
- **EBITDA** = Operating Revenue - Operating Expenses
- **EBITDA Margin** = EBITDA / Operating Revenue
- **PAT Margin** = PAT / Total Revenue
- **ROE** = Net Profit / Shareholder Equity × 100
- **ROCE** = EBIT / (Debt + Equity) × 100
- **Interest Coverage** = EBIT / Interest Expense
- **Debt to Equity** = Total Debt / Total Equity

---

**End of Product Requirements Document**
