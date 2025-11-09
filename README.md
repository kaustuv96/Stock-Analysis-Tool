# Stock Analysis Tool

A comprehensive web application for analyzing Indian stocks (NSE/BSE) using fundamental and technical analysis thumb rules. This tool implements key financial metrics and ratios to help investors make informed decisions based on established valuation principles.

## Features

### Real-Time Analysis
- Instant calculation and evaluation of 12+ critical financial metrics
- Color-coded visual indicators (Good/Warning/Caution)
- Automated rating system (BUY/HOLD/CAUTION/SELL)
- Live updates as you modify input values

### Key Metrics Analyzed

#### Valuation Metrics
- **P/E Ratio**: Flags stocks trading above 25-30x earnings
- **P/E vs Sector Average**: Compares company valuation to industry peers
- **P/B Ratio**: Evaluates if stock is trading above/below book value
- **P/S Ratio**: Assesses revenue-based valuation

#### Profitability Indicators
- **EBITDA Margin**: Operating efficiency measurement
- **PAT Margin**: Overall profitability after all expenses
- **ROE (Return on Equity)**: Shareholder return efficiency
- **ROCE (Return on Capital Employed)**: Overall capital efficiency

#### Balance Sheet Strength
- **Interest Coverage Ratio**: Ability to service debt (>3-4x ideal)
- **Debt to Equity Ratio**: Leverage assessment (<1 safer)

#### Market & Technical
- **Promoter Holding**: Insider confidence indicator (>50% ideal)
- **RSI (Relative Strength Index)**: Momentum indicator (30-70 range)

## Getting Started

### Prerequisites
- Node.js 18+ or higher
- npm, yarn, or pnpm package manager

### Installation

1. Clone the repository:
\`\`\`bash
git clone https://github.com/yourusername/stock-analysis-tool.git
cd stock-analysis-tool
\`\`\`

2. Install dependencies:
\`\`\`bash
npm install
# or
yarn install
# or
pnpm install
\`\`\`

3. Run the development server:
\`\`\`bash
npm run dev
# or
yarn dev
# or
pnpm dev
\`\`\`

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

1. **Enter Stock Data**: Fill in the financial metrics for the stock you want to analyze
2. **Review Analysis**: Results update automatically showing:
   - Overall recommendation rating
   - Individual metric evaluations
   - Visual status indicators
   - Actionable insights for each metric

### Example Data

The tool comes pre-loaded with example data from Aarti Industries Ltd (ARBL) for demonstration purposes. Simply modify the values to analyze any other stock.

## Project Structure

\`\`\`
├── app/
│   ├── page.tsx           # Main application page
│   ├── layout.tsx         # Root layout
│   └── globals.css        # Global styles
├── components/
│   ├── stock-analyzer.tsx # Main analysis component
│   └── ui/                # Reusable UI components
├── lib/
│   ├── stock-analysis.ts  # Analysis logic & algorithms
│   └── utils.ts           # Utility functions
└── public/                # Static assets
\`\`\`

## Technology Stack

- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn/ui (Radix UI)
- **Icons**: Lucide React
- **Deployment**: Vercel

## Analysis Methodology

This tool implements thumb rules from established financial analysis frameworks:

### Valuation Rules
- P/E Ratio should not exceed 25-30x for most stocks
- Compare P/E with sector average to assess relative valuation
- P/B < 1.5x generally indicates undervaluation
- P/S ratio should be compared with competitors

### Profitability Benchmarks
- EBITDA Margin: Higher indicates better operational efficiency
- PAT Margin: Should show consistent or improving trend
- ROE > 15%: Generally considered good
- ROCE > 15%: Indicates efficient capital deployment

### Financial Health
- Interest Coverage > 3-4x: Comfortable debt servicing
- Debt to Equity < 1: Lower financial leverage risk
- Promoter Holding > 50%: Strong insider confidence

### Technical Indicators
- RSI > 70: Overbought (sell signal)
- RSI < 30: Oversold (buy signal)
- RSI 30-70: Neutral range

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This tool is for educational and informational purposes only. It should not be considered as financial advice. Always conduct your own research and consult with a qualified financial advisor before making investment decisions.

## Acknowledgments

- Analysis methodology based on Zerodha Varsity modules
- Financial formulas and thumb rules from industry best practices
- Designed for NSE/BSE listed companies

## Support

For issues, questions, or suggestions, please open an issue on GitHub.

---

Built with ❤️ for Indian stock market investors
