Here's a better phrased version of your frontend prompt with clearer instructions for the dual analysis:
Please perform a comprehensive code review of the branch SOURCE_BRANCH as there is a PR to move this into the staging branch.

I want you to be extremely thorough and flag every issue, potential problem, or improvement opportunity you can find.

## Analysis Areas

### Security & Safety
- Check for XSS vulnerabilities, unsafe dangerouslySetInnerHTML usage
- Look for hardcoded secrets, API keys, or sensitive data
- Validate input sanitization and data validation
- Check for unsafe external library usage
- Review any authentication/authorization changes

### React Best Practices
- Component structure and composition patterns
- Proper use of hooks (useEffect dependencies, cleanup, custom hooks)
- State management patterns and unnecessary re-renders
- Prop drilling vs context usage
- Key props in lists and their stability
- Ref usage and forwarding
- Conditional rendering patterns
- Event handler patterns and binding

### Performance
- Unnecessary re-renders (missing React.memo, useMemo, useCallback)
- Large bundle imports that could be tree-shaken
- Inefficient data structures or algorithms
- Heavy computations that should be memoized
- Large objects/arrays being recreated on each render
- Unused code or imports

### Code Quality & Maintainability
- Function and component length and complexity
- Variable and function naming conventions
- Code duplication and opportunities for abstraction
- Magic numbers and hardcoded values
- Error handling and edge cases
- Loading and error states
- Accessibility issues (a11y)
- TypeScript usage if applicable (proper typing, any usage)

### Architecture & Design
- Separation of concerns
- Single responsibility principle violations
- Coupling between components
- Business logic mixed with UI logic
- Data flow patterns
- File organization and structure

### Testing & Debugging
- Missing or insufficient test coverage for new functionality
- Debugger statements or console.logs left in code
- Development-only code in production builds

### Documentation & Comments
- Missing or outdated comments
- Complex logic that needs explanation
- Public API documentation
- README updates if needed

## Deliverables

**TASK 1: Primary Code Review Analysis**
Create a file named `code-review-analysis.md` with your comprehensive findings from the above criteria. For each issue, provide:
1. Severity rating (Critical/High/Medium/Low)
2. Specific file path and line numbers
3. Concrete suggestions for fixes
4. Explanation of why each flagged item is problematic
5. Code examples of better alternatives where applicable

Be nitpicky and don't hesitate to flag even minor issues. I'd rather have false positives than miss real problems.

**TASK 2: Style Guide Compliance Review**
After completing Task 1, perform a separate analysis focused exclusively on style guide adherence. Reference this TypeScript clean code style guide: https://github.com/nlspnsgen/clean-code-typescript

Create a file named `style-guide-compliance.md` that identifies:
- All code that violates the style guide principles
- Specific style guide rules being broken
- File paths and line numbers for each violation
- Recommended fixes to align with the style guide
- Examples of how the code should be refactored

Treat this as a completely separate analysis from Task 1 - focus only on style, naming conventions, code organization, and clean code principles as outlined in the referenced guide.

## Output Format
Generate exactly two markdown files:
- `code-review-analysis.md` - Technical review findings
- `style-guide-compliance.md` - Style guide violation findings

Both files should be well-structured with clear headings, bullet points, and code examples where helpful.
The key improvements:
1. Clear separation of the two tasks with distinct purposes
2. Better file names that clearly indicate their content:
    * code-review-analysis.md for technical issues
    * style-guide-compliance.md for style violations
3. Explicit instructions for what each analysis should focus on
4. Structured deliverables section that makes it crystal clear what's expected
5. Emphasis on separation - making it clear these are two different types of analysis
This should give you much clearer, more organized results with the two distinct perspectives you're looking for.
