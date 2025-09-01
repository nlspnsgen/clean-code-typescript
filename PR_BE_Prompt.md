Please perform a comprehensive code review of the branch SOURCE_BRANCH as there is a PR to move this into the staging branch.

I want you to be extremely thorough and flag every issue, potential problem, or improvement opportunity you can find in this Hono/Supabase backend codebase.

## Analysis Areas

### Security & Safety
- SQL injection vulnerabilities and parameterized query usage
- Authentication and authorization implementation
- Input validation and sanitization
- Rate limiting and DoS protection
- Secrets management and environment variable security
- CORS configuration and origin validation
- Data encryption at rest and in transit
- API endpoint exposure and access controls
- Error message information leakage
- Dependency vulnerabilities

### API Design & Standards
- RESTful API design principles
- Consistent HTTP status code usage
- Request/response schema validation
- API versioning strategy
- Content-Type and Accept header handling
- Pagination implementation
- Error response standardization
- OpenAPI/Swagger documentation accuracy

### Hono Framework Best Practices
- Middleware composition and ordering
- Context usage and type safety
- Route organization and grouping
- Error boundary implementation
- Request lifecycle management
- Async/await patterns in handlers
- Proper use of Hono's built-in features
- Performance optimization with Hono

### Database & Supabase Integration
- Query optimization and N+1 problem prevention
- Transaction handling and rollback strategies
- Row Level Security (RLS) policy implementation
- Database connection pooling and management
- Migration scripts and schema changes
- Real-time subscription handling
- Proper indexing strategies
- Data validation at database level

### Performance & Scalability
- Database query efficiency
- Caching strategies and implementation
- Memory usage and leak prevention
- Connection pooling optimization
- Background job processing
- API response time optimization
- Resource cleanup and disposal
- Concurrent request handling

### Error Handling & Monitoring
- Consistent error handling patterns
- Proper error logging and monitoring
- Graceful degradation strategies
- Health check endpoint implementation
- Metrics collection and observability
- Alert thresholds and escalation
- Error recovery mechanisms
- Circuit breaker patterns

### Code Quality & Architecture
- Function and module length and complexity
- Separation of concerns and layered architecture
- Dependency injection and inversion of control
- Business logic separation from HTTP handlers
- Data access layer abstraction
- Service layer organization
- Configuration management
- Code duplication and reusability

### Testing & Reliability
- Unit test coverage and quality
- Integration test implementation
- API contract testing
- Mock and stub usage
- Test data management
- Test environment isolation
- Performance testing considerations
- Error scenario testing

### DevOps & Deployment
- Environment configuration management
- Docker/containerization best practices
- CI/CD pipeline integration
- Database migration handling
- Environment variable validation
- Logging configuration
- Health monitoring setup
- Rollback strategies

### Documentation & Maintainability
- API documentation completeness
- Code comments and inline documentation
- README and setup instructions
- Architecture decision records
- Database schema documentation
- Deployment procedures
- Troubleshooting guides

## Deliverables

**TASK 1: Primary Code Review Analysis**
Create a file named `backend-code-review.md` with your comprehensive findings from the above criteria. For each issue, provide:
1. Severity rating (Critical/High/Medium/Low)
2. Specific file path and line numbers
3. Concrete suggestions for fixes
4. Explanation of why each flagged item is problematic
5. Code examples of better alternatives where applicable
6. Security implications if applicable
7. Performance impact assessment

Be thorough and flag potential issues even if they seem minor. Backend code quality directly impacts system reliability and security.

**TASK 2: Style Guide Compliance Review**
After completing Task 1, perform a separate analysis focused exclusively on TypeScript clean code principles. Reference this style guide: https://github.com/nlspnsgen/clean-code-typescript

Create a file named `backend-style-compliance.md` that identifies:
- All code that violates clean code principles
- Specific style guide rules being broken
- File paths and line numbers for each violation
- Recommended refactoring to align with clean code practices
- Examples of improved code structure and naming
- Function/class design improvements
- Comment and documentation style issues

Focus specifically on:
- Meaningful variable and function names
- Function size and single responsibility
- Class design and composition
- Error handling patterns
- Code organization and structure
- Comment quality and necessity
- TypeScript type usage and safety

## Output Format
Generate exactly two markdown files:
- `backend-code-review.md` - Technical and architectural review findings
- `backend-style-compliance.md` - Clean code style guide violation findings

Both files should be well-structured with clear headings, code examples, and actionable recommendations. Prioritize issues that could impact production stability, security, or maintainability.
