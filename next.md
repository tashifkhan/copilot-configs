You are an expert in TypeScript, React, Node.js, Next.js App Router, Shadcn UI, Radix UI and Tailwind.

Code Style and Structure

- Write concise, technical TypeScript code following Standard.js rules.
- Use functional and declarative programming patterns; avoid classes.
- Prefer iteration and modularization over code duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoading, hasError).
- Structure files: exported component, subcomponents, helpers, static content.

Standard.js Rules

- Use 3 space indentation.
- Use double quotes for strings except to avoid escaping.
- No semicolons (unless required to disambiguate statements).
- No unused variables.
- Add a space after keywords.
- Add a space before a function declaration's parentheses.
- Always use === instead of ==.
- Infix operators must be spaced.
- Commas should have a space after them.
- Keep else statements on the same line as their curly braces.
- For multi-line if statements, use curly braces.
- Always handle the err function parameter.
- Use camelcase for variables and functions.
- Use PascalCase for constructors and React components.

Naming Conventions

- Use camelcase for directories.
- Favor named exports for components.

React Best Practices

- Use functional components with prop-types for type checking.
- Use the "function" keyword for component definitions.
- Implement hooks correctly (useState, useEffect, useContext, useReducer, useMemo, useCallback).
- Follow the Rules of Hooks (only call hooks at the top level, only call hooks from React functions).
- Create custom hooks to extract reusable component logic.
- Use React.memo() for component memoization when appropriate.
- Implement useCallback for memoizing functions passed as props.
- Use useMemo for expensive computations.
- Avoid inline function definitions in render to prevent unnecessary re-renders.
- Prefer composition over inheritance.
- Use children prop and render props pattern for flexible, reusable components.
- Implement React.lazy() and Suspense for code splitting.
- Use refs sparingly and mainly for DOM access.
- Prefer controlled components over uncontrolled components.
- Implement error boundaries to catch and handle errors gracefully.
- Use cleanup functions in useEffect to prevent memory leaks.
- Use short-circuit evaluation and ternary operators for conditional rendering.

State Management

- Lift state up when needed to share state between components.
- Use redux-toolkit for intermediate state sharing when prop drilling becomes cumbersome.

UI and Styling

- Use Shadcn UI and Radix UI for component foundations.
- Implement responsive design with Tailwind CSS; use a mobile-first approach.
- Implement a consistent naming convention for CSS classes (e.g., BEM) within Stylus modules.
- Use Tailwind for utility classes and rapid prototyping.
  - Use Tailwind for common utilities and layout.
  - Never use the @apply directive

File Structure for Styling

- Example structure:
  components/
  Button/
  Button.ts
  Card/
  Card.ts

Performance Optimization

- Minimize 'use client', 'useEffect', and 'useState'; favor React Server Components (RSC).
- Use
- Use dynamic loading for non-critical components.
- Optimize images: use WebP format, include size data, implement lazy loading.
- Implement route-based code splitting in Next.js.
- Minimize the use of global styles; prefer modular, scoped styles.
- Use PurgeCSS with Tailwind to remove unused styles in production.

Forms and Validation

- Use controlled components for form inputs.
- Implement form validation (client-side and server-side).
- Consider using libraries like react-hook-form for complex forms.
- Use Zod or Joi for schema validation.

Error Handling and Validation

- Prioritize error handling and edge cases.
- Handle errors and edge cases at the beginning of functions.
- Use early returns for error conditions to avoid deeply nested if statements.
- Place the happy path last in the function for improved readability.
- Avoid unnecessary else statements; use if-return pattern instead.
- Use guard clauses to handle preconditions and invalid states early.
- Implement proper error logging and user-friendly error messages.
- Model expected errors as return values in Server Actions.

Accessibility (a11y)

- Use semantic HTML elements.
- Implement proper ARIA attributes.
- Ensure keyboard navigation support.

Key Conventions

- Use <Link /> from next/link instead of <a> always
- Use App router using next/navigation
- Limit 'use client':
  - Favor server components and Next.js SSR.
  - Use only for Web API access in small components.
  - Avoid for data fetching or state management.

Follow Next.js docs for Data Fetching, Rendering, and Routing.
