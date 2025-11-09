# Contributing to Stock Analysis Tool

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## How to Contribute

### Reporting Bugs

If you find a bug, please open an issue with:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable
- Your environment (browser, OS)

### Suggesting Features

Feature suggestions are welcome! Please open an issue with:
- Clear description of the feature
- Use case and benefits
- Any relevant examples or mockups

### Code Contributions

1. **Fork the repository**
2. **Create a feature branch**
   \`\`\`bash
   git checkout -b feature/your-feature-name
   \`\`\`

3. **Make your changes**
   - Follow existing code style
   - Add comments for complex logic
   - Update documentation if needed

4. **Test your changes**
   - Ensure the app runs without errors
   - Test all affected functionality

5. **Commit your changes**
   \`\`\`bash
   git commit -m "Add: description of your changes"
   \`\`\`

6. **Push to your fork**
   \`\`\`bash
   git push origin feature/your-feature-name
   \`\`\`

7. **Open a Pull Request**
   - Provide clear description of changes
   - Reference any related issues

## Development Guidelines

### Code Style
- Use TypeScript for type safety
- Follow existing naming conventions
- Use meaningful variable and function names
- Keep functions small and focused

### Component Structure
- One component per file
- Use functional components with hooks
- Implement proper prop typing
- Extract reusable logic into custom hooks

### Analysis Logic
- Document all formulas with sources
- Add unit tests for calculation functions
- Validate input ranges and edge cases
- Provide clear error messages

### UI/UX
- Maintain consistent design patterns
- Ensure responsive layouts
- Use semantic HTML
- Follow accessibility best practices

## Adding New Metrics

To add a new financial metric:

1. **Update the analysis logic** (`lib/stock-analysis.ts`)
   - Add the calculation function
   - Define evaluation criteria
   - Add to the analysis results

2. **Update the UI** (`components/stock-analyzer.tsx`)
   - Add input field with validation
   - Add result card with interpretation

3. **Update documentation**
   - Add formula and source
   - Explain interpretation guidelines

## Questions?

Feel free to open an issue for any questions about contributing!
