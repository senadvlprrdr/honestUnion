# honestUnion

![CI](https://img.shields.io/github/actions/workflow/status/senadvlprrdr/honestUnion/ci.yml?branch=main&label=CI) ![React](https://img.shields.io/badge/react-18+-61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6) ![License](https://img.shields.io/github/license/senadvlprrdr/honestUnion?color=blue)

honestUnion is a tree-shakeable React component library with headless hooks and accessible UI components. It includes Button (with primary/secondary/ghost variants and sm/md/lg sizes), Card, and a useToggle hook -- all fully typed with TypeScript, forwardRef-enabled, and built with WAI-ARIA keyboard navigation support. Zero runtime dependencies.

## Features

- Tree-shakeable ES modules -- import only Button, Card, or useToggle
- Button component with primary/secondary/ghost variants and sm/md/lg sizes
- Tested with @testing-library/react and Vitest
- Full TypeScript types with generic component props
- Zero runtime dependencies -- only React as peer dependency

## Prerequisites

- React 18 or higher (peer dependency)
- Node.js 16 or higher for development

## Installation

```bash
npm install honestUnion
# or
yarn add honestUnion
# or
pnpm add honestUnion
```

## Usage

```tsx
import { Button, Card } from 'honestUnion';
import { useToggle } from 'honestUnion';

function App() {
  const [open, toggle] = useToggle(false);

  return (
    <Card title="Demo Component">
      <Button variant="primary" size="md" onClick={toggle}>
        {open ? 'Close' : 'Open'}
      </Button>
      {open && <p>Content is now visible!</p>}
    </Card>
  );
}
```

## Project Structure

```
honestUnion/
├── src/
│   ├── Button.tsx
│   ├── Card.tsx
│   ├── useToggle.ts
│   └── index.ts
├── tests/
│   └── Button.test.tsx
├── package.json  tsconfig.json  tsup.config.ts
├── README.md  LICENSE  CHANGELOG.md  CONTRIBUTING.md  CODE_OF_CONDUCT.md
├── .github/
│   ├── workflows/ci.yml
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   └── PULL_REQUEST_TEMPLATE.md
└── .gitignore
```

## Running Tests

```bash
npm test
# watch mode
npm test -- --watch
```

## FAQ

**Is this production-ready?**
Yes, honestUnion includes tests, CI/CD, and documentation. However, you should review the code and adapt it to your specific needs before deploying.

**Can I use this in my project?**
Yes, honestUnion is licensed under the MIT. See the [LICENSE](LICENSE) file for details.

**How do I report a bug?**
Please [open an issue](https://github.com/senadvlprrdr/honestUnion/issues/new?template=bug_report.md) using the bug report template.

**How do I request a feature?**
Please [open an issue](https://github.com/senadvlprrdr/honestUnion/issues/new?template=feature_request.md) using the feature request template.

**How can I contribute?**
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

Quick start:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Make your changes and run tests (see [Running Tests](#running-tests) above)
4. Commit with a clear message: `git commit -am 'Add: my feature'`
5. Push to your fork: `git push origin feature/my-feature`
6. Open a Pull Request

Please ensure all tests pass before submitting a pull request.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes and version history.

## License

This project is licensed under the MIT -- see the [LICENSE](LICENSE) file for details.

Copyright (c) 2026 nina smith.
