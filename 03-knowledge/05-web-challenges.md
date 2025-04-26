<!-- AI.FRAMEWORK.COMPONENT: WEB_CHALLENGES -->
<!-- AI.METADATA
component: web_challenges
version: 1.0
last_updated: 26/04/2025
framework_type: ethical_hacking_mentor
language: en
parent: r3d_hacker_framework
path: knowledge/web-challenges
references: [mode_framework, challenge_library, security_domains]
ai_optimization: [knowledge_graph, parameter_network, computational_index]
complexity_level: 4
context_sensitivity: high
-->

<!-- AI.OPTIMIZATION.START -->

## Knowledge Graph Access

- Challenge Components:
  - frameworks: {nodes: ["structure", "difficulty", "progression"]}
  - categories: {nodes: ["sql_injection", "xss", "auth_bypass", "api_security"]}
  - adaptations: {nodes: ["mode_specific", "skill_level", "complexity"]}

## Parameter Network

- Challenge Dependencies:
  - skill_level -> challenge_selection
  - mode_context -> guidance_level
  - topic_area -> challenge_type
  - learner_progress -> difficulty_adjustment

## Computational Indices

- Challenge Paths:
  - sql_injection: basic -> extraction -> blind -> waf_bypass
  - xss: alert -> filter_bypass -> stored -> dom_based
  - auth: cookie -> jwt -> oauth -> sso
  - api: discovery -> fuzzing -> graphql -> microservices

## Context Sensitivity

- Adaptation Points:
  - Challenge Selection:
    - User Skill Level
    - Previous Completion
    - Learning Style
    - Mode Context
  - Content Adaptation: - Guidance Detail - Hint Availability - Technical Depth - Tool Requirements
  <!-- AI.OPTIMIZATION.END -->

# R3D.HACKER WEB APPLICATION SECURITY CHALLENGES

<!-- AI.SECTION.START: CHALLENGE_FRAMEWORKS -->

## CHALLENGE FRAMEWORKS

<!-- AI.CONTEXT: CHALLENGE_TYPES -->

### Web Challenge Structure Templates

#### n00b_mode Challenge Template

```
BEGINNER CHALLENGE: [Simple Title]

CONCEPT: [Web security concept being taught]

SCENARIO:
[Brief, simple scenario with clear context]

OBJECTIVE:
[Single, straightforward goal]

GUIDANCE:
- [Step-by-step instructions]
- [Specific hints for each step]
- [Clear success indicators]

TOOLS NEEDED:
- [Basic tools with installation guidance]

LEARNING OUTCOME:
[Specific skill or knowledge gained]
```

#### script_kiddie_mode Challenge Template

```
TOOL PRACTICE CHALLENGE: [Descriptive Title]

SCENARIO:
[Practical scenario requiring specific tool usage]

OBJECTIVE:
[Clear goal with defined success criteria]

APPROACH:
- [General methodology steps]
- [Tool usage guidance]
- [Key parameters to consider]

HINTS:
- Hint 1: [General direction]
- Hint 2: [More specific guidance]
- Hint 3: [Near-solution hint]

TOOLS NEEDED:
- [Specific tools with configuration notes]

LEARNING OUTCOME:
[Tool proficiency and technique understanding]
```

#### hack3r_mode Challenge Template

```
SECURITY CHALLENGE: [Professional Title]

SCENARIO:
[Realistic security testing scenario]

TARGET DETAILS:
- [Environment specifications]
- [Available entry points]
- [Scope limitations]

OBJECTIVE:
[Professional testing goal]

CONSTRAINTS:
- [Ethical boundaries]
- [Testing limitations]
- [Documentation requirements]

HINTS AVAILABLE: [Number of hints] (request if needed)

LEARNING OUTCOME:
[Methodology application and security skills]
```

#### elit3_mode Challenge Template

```
ADV4NCED H4CKING CH4LLENGE: [Technical Title]

SC3NARIO:
[Complex security scenario with minimal details]

T4RGET:
[Technical environment with sophisticated protection]

OBJ3CTIVE:
[Advanced security goal requiring multiple steps]

C0NSTRAINTS:
[Professional and ethical boundaries]

H1NTS: Limited hints available only for critical roadblocks

L3ARNING OUTCOME:
[Advanced security techniques and creative problem-solving]
```

<!-- AI.SECTION.END: CHALLENGE_FRAMEWORKS -->

<!-- AI.SECTION.START: SQL_INJECTION_CHALLENGES -->

## SQL INJECTION CHALLENGES

<!-- AI.CONTEXT: SQL_INJECTION -->

### SQL Injection Challenges

#### n00b_mode: "First Injection"

```
BEGINNER CHALLENGE: First SQL Injection

CONCEPT: SQL Injection Basics

SCENARIO:
You're testing a simple login page for a security flaw called SQL injection.

OBJECTIVE:
Bypass the login without knowing the correct password.

GUIDANCE:
1. Go to the login page at http://practice-lab.local/login
2. In the username field, try entering: admin' --
3. Leave the password field blank
4. Click the login button
5. Observe what happens

EXPLANATION:
The input admin' -- changes the SQL query structure:
- The single quote (') closes the username string
- The double dash (--) comments out the rest of the query
- This makes the database ignore the password check

TOOLS NEEDED:
- Web browser

LEARNING OUTCOME:
Understanding basic SQL injection and how improper input handling can bypass authentication.
```

#### script_kiddie_mode: "Data Extraction"

```
TOOL PRACTICE CHALLENGE: SQL Injection Data Extraction

SCENARIO:
A product search feature on an e-commerce site appears vulnerable to SQL injection.

OBJECTIVE:
Extract the database version and list of database tables.

APPROACH:
1. Identify the vulnerable parameter in the product search
2. Confirm the vulnerability with a simple test
3. Determine the number of columns using ORDER BY
4. Use UNION SELECT to extract database information
5. Document your findings

HINTS:
- Hint 1: Try searching for a product and adding a single quote
- Hint 2: The UNION SELECT technique requires matching column counts
- Hint 3: Information_schema contains database metadata

TOOLS NEEDED:
- Web browser
- Burp Suite (for request interception)
- SQL injection cheat sheet

LEARNING OUTCOME:
Practical SQL injection exploitation skills and structured data extraction technique.
```

#### hack3r_mode: "Blind SQL Injection"

```
SECURITY CHALLENGE: Blind SQL Injection Exploitation

SCENARIO:
A financial application's account lookup feature may be vulnerable to SQL injection, but it returns no data directly - only "Account found" or "Account not found" messages.

TARGET DETAILS:
- Web application at http://financial-app.laboratory/account
- Parameter: account_number
- No error messages or direct query results displayed

OBJECTIVE:
Confirm vulnerability and extract the administrator's password hash.

CONSTRAINTS:
- Use only boolean-based blind SQL injection techniques
- Document each step of your methodology
- Create a proof of concept that could be reproduced

HINTS AVAILABLE: 3 (request if needed)

LEARNING OUTCOME:
Advanced SQL injection methodology, boolean-based blind exploitation, and systematic data extraction.
```

#### elit3_mode: "WAF Bypass"

```
ADV4NCED H4CKING CH4LLENGE: SQL 1njection WAF Byp4ss

SC3NARIO:
A b4nking application employs a sophisticated WAF that blocks common SQL injection patterns. The application uses parameterized queries except in one legacy function.

T4RGET:
- Internal banking portal with account search functionality
- ModSecurity WAF with OWASP core ruleset
- Oracle database backend
- Custom error handling (no error messages)

OBJ3CTIVE:
Bypass WAF protection, identify and exploit the vulnerable function, and extract admin credentials.

C0NSTRAINTS:
- No automated tools (manual exploitation only)
- Maintain detailed exploitation notes
- Develop at least two different bypass techniques

H1NTS: Limited hints available only for critical roadblocks

L3ARNING OUTCOME:
Advanced WAF bypass techniques, Oracle-specific SQL injection, and sophisticated exploitation methodology.
```

<!-- AI.SECTION.END: SQL_INJECTION_CHALLENGES -->

<!-- AI.SECTION.START: XSS_CHALLENGES -->

## CROSS-SITE SCRIPTING CHALLENGES

<!-- AI.CONTEXT: XSS -->

### Cross-Site Scripting Challenges

#### n00b_mode: "Hello Alert"

```
BEGINNER CHALLENGE: Hello Alert XSS

CONCEPT: Cross-Site Scripting Basics

SCENARIO:
You're testing a comment section on a blog for a security vulnerability called Cross-Site Scripting (XSS).

OBJECTIVE:
Make a JavaScript alert box appear when someone views your comment.

GUIDANCE:
1. Go to the blog comment section at http://practice-lab.local/blog
2. In the comment field, enter: <script>alert('XSS')</script>
3. Submit the comment
4. Refresh the page to view your comment
5. Observe the alert box that appears

EXPLANATION:
- The <script> tags tell the browser to run JavaScript code
- The alert() function creates a pop-up message box
- When your comment is displayed to any viewer, the code runs in their browser

TOOLS NEEDED:
- Web browser

LEARNING OUTCOME:
Understanding basic Cross-Site Scripting and how it allows injecting code into web pages.
```

#### script_kiddie_mode: "Filtered XSS"

```
TOOL PRACTICE CHALLENGE: Bypassing Basic XSS Filters

SCENARIO:
A contact form on a website filters out obvious <script> tags but may still be vulnerable to XSS.

OBJECTIVE:
Bypass the filter and make an alert box appear when the form is viewed by an administrator.

APPROACH:
1. Test basic XSS payloads to identify filtering behavior
2. Try alternative XSS vectors that might bypass filters
3. Use browser development tools to understand the filtering mechanism
4. Document successful bypass techniques

HINTS:
- Hint 1: Try using event handlers like onload or onerror
- Hint 2: HTML tags like <img> and <body> can execute JavaScript
- Hint 3: Try this payload: <img src="x" onerror="alert('XSS')">

TOOLS NEEDED:
- Web browser with developer tools
- XSS cheat sheet

LEARNING OUTCOME:
XSS filter bypass techniques and alternative JavaScript execution vectors.
```

#### hack3r_mode: "Stored XSS Attack Chain"

```
SECURITY CHALLENGE: Stored XSS Attack Chain

SCENARIO:
An e-commerce platform allows users to create product reviews with formatting options. The site may be vulnerable to a stored XSS attack that could target administrators.

TARGET DETAILS:
- Product review system at http://ecommerce.laboratory/products
- Rich text editor for reviews with HTML support
- Admin panel at /admin requiring authentication
- Reviews are moderated before appearing publicly

OBJECTIVE:
Develop a stored XSS payload that captures admin cookies when a review is viewed in the moderation panel.

CONSTRAINTS:
- Set up a controlled environment to receive stolen cookies
- Craft a payload that avoids detection during moderation
- Document the full attack chain and potential impact

HINTS AVAILABLE: 3 (request if needed)

LEARNING OUTCOME:
Advanced XSS payload development, understanding security implications of stored XSS, and cookie theft techniques.
```

#### elit3_mode: "DOM-Based XSS"

```
ADV4NCED H4CKING CH4LLENGE: D0M-Based XSS in SPA

SC3NARIO:
A modern single-page application (SPA) built with React uses client-side routing and renders user-generated content. The application implements CSP with nonce-based script protection.

T4RGET:
- SPA with React frontend and GraphQL API
- Content-Security-Policy: script-src 'self' 'nonce-[random]'
- Client-side routing using fragment identifiers
- User profile customization features

OBJ3CTIVE:
Identify DOM-based XSS vulnerabilities in the client-side code and develop a sophisticated exploitation chain that bypasses CSP.

C0NSTRAINTS:
- No server-side injection vectors
- Must work in modern browsers with standard security features enabled
- Full technical documentation of vulnerability and exploitation

H1NTS: Limited hints available only for critical roadblocks

L3ARNING OUTCOME:
Advanced DOM-based XSS, CSP bypass techniques, and security vulnerabilities in modern JavaScript frameworks.
```

<!-- AI.SECTION.END: XSS_CHALLENGES -->

<!-- AI.SECTION.START: AUTH_CHALLENGES -->

## AUTHENTICATION BYPASS CHALLENGES

<!-- AI.CONTEXT: AUTH_BYPASS -->

### Authentication Bypass Challenges

#### n00b_mode: "Remember Me"

```
BEGINNER CHALLENGE: Remember Me Bypass

CONCEPT: Cookie Manipulation

SCENARIO:
A website uses a "Remember Me" cookie to keep users logged in.

OBJECTIVE:
Modify a cookie to gain access to another user's account.

GUIDANCE:
1. Log in to the practice site with the provided credentials
2. Use browser developer tools to examine cookies (F12 > Application > Cookies)
3. Find the "remember_user" cookie
4. Note that it contains a value like "user_123"
5. Try changing "123" to another number, like "456"
6. Refresh the page and observe what happens

EXPLANATION:
- Cookies store user data in your browser
- The "remember_user" cookie identifies which account you're using
- Changing this value tricks the site into showing you another account
- Proper security would encrypt or sign this value to prevent tampering

TOOLS NEEDED:
- Web browser with developer tools

LEARNING OUTCOME:
Understanding cookie-based authentication and the risks of insecure cookie implementation.
```

#### script_kiddie_mode: "JWT Token Tampering"

```
TOOL PRACTICE CHALLENGE: JWT Token Manipulation

SCENARIO:
A web application uses JSON Web Tokens (JWT) for authentication, but the tokens may be improperly secured.

OBJECTIVE:
Analyze and modify a JWT token to elevate privileges from user to administrator.

APPROACH:
1. Log in with provided user credentials
2. Capture and decode the JWT authentication token
3. Analyze the token structure and claims
4. Attempt to modify the "role" claim
5. Test the modified token to verify privilege escalation

HINTS:
- Hint 1: Use jwt.io to decode and examine the token structure
- Hint 2: Check if the token is using the "none" algorithm
- Hint 3: The "role" claim might be set to "user" and could be changed to "admin"

TOOLS NEEDED:
- Web browser with developer tools
- JWT decoder (jwt.io or similar)
- Burp Suite (optional)

LEARNING OUTCOME:
Understanding JWT structure, common JWT security flaws, and token tampering techniques.
```

#### hack3r_mode: "OAuth Flow Exploitation"

```
SECURITY CHALLENGE: OAuth Authentication Bypass

SCENARIO:
A SaaS platform implements OAuth 2.0 for third-party authentication but may have flaws in its implementation.

TARGET DETAILS:
- OAuth 2.0 authentication flow with multiple providers
- Authorization code flow implementation
- Redirect URI validation
- State parameter implementation

OBJECTIVE:
Identify and exploit vulnerabilities in the OAuth implementation to gain unauthorized access.

CONSTRAINTS:
- Test only against the lab environment
- Document all identified vulnerabilities
- Explain the potential impact of each vulnerability
- Provide remediation recommendations

HINTS AVAILABLE: 3 (request if needed)

LEARNING OUTCOME:
OAuth 2.0 security vulnerabilities, authentication flow analysis, and secure implementation best practices.
```

#### elit3_mode: "SSO Security Assessment"

```
ADV4NCED H4CKING CH4LLENGE: Ent3rprise SSO Byp4ss

SC3NARIO:
A multinational corporation uses a complex Single Sign-On (SSO) implementation across multiple applications and services, including legacy systems.

T4RGET:
- SAML 2.0 based SSO with multiple service providers
- IdP-initiated and SP-initiated flows
- X.509 certificate-based validation
- Mixed application environment (modern and legacy)

OBJ3CTIVE:
Perform a comprehensive security assessment of the SSO implementation and develop exploitation techniques for identified vulnerabilities.

C0NSTRAINTS:
- Test only in designated lab environment
- No disruption to production systems
- Technical documentation suitable for security engineers
- Root cause analysis for all vulnerabilities

H1NTS: Limited hints available only for critical roadblocks

L3ARNING OUTCOME:
Advanced SSO security assessment methodology, SAML 2.0 exploitation techniques, and enterprise authentication security.
```

<!-- AI.SECTION.END: AUTH_CHALLENGES -->

<!-- AI.SECTION.START: API_CHALLENGES -->

## API SECURITY CHALLENGES

<!-- AI.CONTEXT: API_SECURITY -->

### API Security Challenges

#### n00b_mode: "API Discovery"

```
BEGINNER CHALLENGE: API Endpoint Discovery

CONCEPT: API Reconnaissance

SCENARIO:
You're testing a web application and need to discover hidden API endpoints.

OBJECTIVE:
Identify undocumented API endpoints that the application uses.

GUIDANCE:
1. Open the target web application in your browser
2. Open browser developer tools (F12)
3. Go to the Network tab
4. Use the application normally while watching network requests
5. Look for requests to URLs containing "api", "service", or "v1/v2/v3"
6. Make a list of all API endpoints you discover

EXPLANATION:
- Modern web applications use APIs to communicate with servers
- Many API endpoints may not be documented publicly
- The browser's developer tools show all requests the application makes
- These hidden endpoints might have security vulnerabilities

TOOLS NEEDED:
- Web browser with developer tools

LEARNING OUTCOME:
Basic API endpoint discovery and understanding how modern web applications communicate.
```

#### script_kiddie_mode: "API Parameter Fuzzing"

```
TOOL PRACTICE CHALLENGE: API Parameter Fuzzing

SCENARIO:
You've discovered an API endpoint that accepts various parameters, and you need to test it for security issues.

OBJECTIVE:
Use parameter fuzzing to identify vulnerabilities in an API endpoint.

APPROACH:
1. Document the API endpoint structure and identified parameters
2. Set up Burp Suite to intercept API requests
3. Use Intruder to fuzz different parameter values
4. Analyze responses for errors, unexpected behavior, or data leakage
5. Document all findings and potential vulnerabilities

HINTS:
- Hint 1: Try common parameter names like "id", "user", "file", etc.
- Hint 2: Test different data types (strings, numbers, special characters)
- Hint 3: Look for differences in response times, status codes, and content

TOOLS NEEDED:
- Burp Suite Community/Professional
- API parameter wordlists
- Postman (optional)

LEARNING OUTCOME:
API fuzzing methodology, parameter manipulation techniques, and identifying common API vulnerabilities.
```

#### hack3r_mode: "GraphQL Security Assessment"

```
SECURITY CHALLENGE: GraphQL API Security Assessment

SCENARIO:
A modern web application uses GraphQL for its data layer. You need to assess the GraphQL implementation for security vulnerabilities.

TARGET DETAILS:
- GraphQL endpoint at /graphql
- Authentication via Bearer token
- Multiple object types and relationships
- Introspection enabled

OBJECTIVE:
Perform a comprehensive security assessment of the GraphQL API, identifying and exploiting vulnerabilities.

CONSTRAINTS:
- Document all queries and methodology
- Identify authorization flaws and data exposure risks
- Develop proof-of-concept exploits for key vulnerabilities
- Provide clear remediation guidance

HINTS AVAILABLE: 3 (request if needed)

LEARNING OUTCOME:
GraphQL security assessment methodology, common GraphQL vulnerabilities, and secure implementation practices.
```

#### elit3_mode: "Chained API Exploitation"

```
ADV4NCED H4CKING CH4LLENGE: API S3curity Ch4in Exploitati0n

SC3NARIO:
A financial services platform exposes multiple microservices through a complex API gateway with sophisticated security controls.

T4RGET:
- Microservice architecture with 20+ services
- OAuth 2.0 authentication with JWT
- Rate limiting and anomaly detection
- API gateway with request validation
- Role-based access controls

OBJ3CTIVE:
Identify and chain multiple API vulnerabilities to achieve unauthorized data access across service boundaries.

C0NSTRAINTS:
- No automated scanning tools
- Develop a sophisticated exploitation chain
- Document complete attack methodology
- Demonstrate impact across service boundaries

H1NTS: Limited hints available only for critical roadblocks

L3ARNING OUTCOME:
Advanced API security assessment, vulnerability chaining techniques, microservice security architecture, and sophisticated exploitation methodology.
```

<!-- AI.SECTION.END: API_CHALLENGES -->
