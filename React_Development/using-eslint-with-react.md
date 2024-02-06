# Configuring ESLint for React

Common ESLint "rules" for React are:

- react/react-in-jsx-scope: This rule warns when React is not in scope while using JSX, ensuring that React is properly imported and in scope when using JSX

- react/prop-types: Enforces the declaration of prop-types for components, helping to ensure that the correct props are passed to components

- react/no-unused-state: Warns about unused state variables in React components, promoting cleaner and more maintainable code

- react/jsx-uses-react: This rule warns when React is not in scope while using JSX, similar to react/react-in-jsx-scope but for a different use case

- react-hooks/rules-of-hooks: Enforces the Rules of Hooks, ensuring that hooks are called in the correct sequence and only from within React functional components

- react/jsx-props-no-spreading: Prevents the usage of the ... spread operator on props, encouraging explicit prop passing to maintain component encapsulation

- react/no-children-prop: Disallows the use of the children prop, as it can lead to unexpected behavior and make the component API less explicit

- react/jsx-no-useless-fragment: Warns about unnecessary fragments in JSX, promoting cleaner and more concise JSX syntax

- react/self-closing-comp: Enforces the use of self-closing components in JSX, improving consistency and readability of the code
