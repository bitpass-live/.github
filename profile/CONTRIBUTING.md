# Contributing to BitPass

First off, thank you for considering contributing to BitPass! It's people like you that make BitPass a great tool for event organizers and attendees around the world. This document provides guidelines and instructions for contributing to our open source project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Documentation](#documentation)
- [Non-Code Contributions](#non-code-contributions)
- [Communication](#communication)

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

## Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn
- Git
- Basic knowledge of TypeScript, React, and Next.js
- Familiarity with Bitcoin, Lightning Network, and Nostr (helpful but not required)

### Setting Up Your Development Environment

1. Fork the repository you want to contribute to:
   - [BitPass App](https://github.com/bitpass-live/bitpass-app)
   - [BitPass API](https://github.com/bitpass-live/bitpass-api)

2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
   cd REPOSITORY-NAME
   ```

3. Add the original repository as a remote:
   ```bash
   git remote add upstream https://github.com/bitpass-live/REPOSITORY-NAME.git
   ```

4. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

5. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Development Workflow

### Branch Organization

- `main` - Production-ready code. All PRs eventually target this branch.
- `dev` - Development branch where features are integrated before release.
- `feature/*` - Feature branches for new functionality.
- `bugfix/*` - Branches for bug fixes.
- `hotfix/*` - Emergency fixes for production issues.

### Issues

Before starting work on a new feature or fix:

1. Check existing issues to see if your problem/idea has already been addressed.
2. If not, create a new issue describing what you want to work on.
3. Wait for feedback from maintainers before investing significant time.

### Working on Issues

1. Comment on the issue you want to work on to let others know.
2. Make sure your fork is up to date:
   ```bash
   git fetch upstream
   git checkout dev
   git merge upstream/dev
   ```
3. Create a new branch for your work:
   ```bash
   git checkout -b feature/issue-number-short-description
   ```

## Pull Request Process

1. Ensure your code follows our [coding standards](#coding-standards).
2. Update documentation if necessary.
3. Add tests for new functionality.
4. Make sure all tests pass:
   ```bash
   npm test
   # or
   yarn test
   ```
5. Push your changes to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
6. Create a pull request to the `dev` branch of the original repository.
7. Fill out the PR template with all required information.
8. Wait for code review and address any feedback.

### PR Requirements

- Clear, descriptive title
- Reference to related issue(s)
- Description of changes made
- Screenshots/GIFs for UI changes
- All status checks passing

## Coding Standards

### General Guidelines

- Write clean, readable, and maintainable code
- Follow the principle of "Do One Thing Well"
- Keep functions small and focused
- Use meaningful variable and function names
- Comment complex logic, but prefer self-documenting code

### TypeScript/JavaScript

- Follow the [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- Use TypeScript for type safety
- Use ES6+ features when appropriate
- Avoid any and explicit type assertions when possible

### React

- Use functional components with hooks
- Keep components small and focused
- Use proper component composition
- Follow React best practices for performance

### CSS/Styling

- Use Tailwind CSS for styling
- Follow the BitPass design system
- Ensure responsive design for all components
- Use semantic class names

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

Types include:
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code changes that neither fix bugs nor add features
- `test`: Adding or modifying tests
- `chore`: Changes to the build process or auxiliary tools

Example:
```
feat(auth): add Nostr key authentication

Implements Nostr key-based authentication using NIP-07.
Closes #123
```

## Testing

- Write tests for all new functionality
- Ensure existing tests pass before submitting a PR
- Follow test-driven development when appropriate
- Test across different browsers and devices

### Types of Tests

- **Unit Tests**: Test individual functions and components
- **Integration Tests**: Test interactions between components
- **End-to-End Tests**: Test complete user flows

## Documentation

Good documentation is crucial for any open source project:

- Update README.md with new features or changes
- Document APIs using JSDoc comments
- Update user documentation for UI changes
- Add inline comments for complex logic

## Non-Code Contributions

We value all types of contributions, not just code:

- **Design**: UI/UX improvements, mockups, design assets
- **Documentation**: Improving or translating documentation
- **Testing**: Manual testing, bug reports, usability feedback
- **Community**: Answering questions, helping new contributors
- **Promotion**: Writing blog posts, tutorials, or social media content

## Communication

- **GitHub Issues**: For bug reports, feature requests, and discussions
- **Pull Requests**: For code contributions and reviews
- **Discord**: For real-time communication and community discussions
- **Twitter**: For announcements and public discussions

## Bitcoin and Nostr Specific Guidelines

### Lightning Network Integration

- Follow best practices for Lightning Network payment handling
- Ensure proper error handling for payment failures
- Test with testnet before mainnet

### Nostr Integration

- Follow relevant NIPs (Nostr Implementation Possibilities)
- Ensure compatibility with popular Nostr clients
- Prioritize user privacy and security

## Questions?

If you have any questions or need help, please:

1. Check the documentation
2. Search existing issues
3. Ask in our Discord community
4. Open a new issue with the "question" label

Thank you for contributing to BitPass! Together, we're building the future of Bitcoin-native ticketing.
