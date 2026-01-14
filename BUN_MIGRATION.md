# Bun Migration Guide

This project has been migrated from Node.js/npm to Bun for improved performance and developer experience.

## What Changed

### Package Management
- Replaced `npm` with `bun` for package management
- Replaced `package-lock.json` with `bun.lock`
- Added `bun-types` for TypeScript support

### Scripts
All npm scripts have been updated to use Bun:
- `bun install` - Install dependencies
- `bun run build` - Build the project
- `bun run start` - Start the compiled application
- `bun run dev` - Run TypeScript directly without compilation (new!)
- `bun run auth` - Run authentication setup

### TypeScript Configuration
- Updated target to `ES2022` for better modern JavaScript support
- Changed module resolution to `bundler` for optimal Bun compatibility
- Added `bun-types` for Bun-specific TypeScript definitions

### Performance Benefits
- Faster installation times (2-3x faster than npm)
- Direct TypeScript execution without compilation for development
- Improved startup times
- Native support for ES modules

## Installation

1. Install Bun (if not already installed):
```bash
curl -fsSL https://bun.sh/install | bash
```

2. Install dependencies:
```bash
bun install
```

3. Build the project:
```bash
bun run build
```

4. Run the application:
```bash
bun run start
# or for development (runs TypeScript directly)
bun run dev
```

## Compatibility

This project maintains backward compatibility with Node.js (>=14.0.0) while adding full Bun support (>=1.0.0). You can still use npm/node if needed, though Bun is recommended for better performance.

## Migration Steps Performed

1. Updated `package.json` scripts to use `bun` commands
2. Added Bun engine requirement to `package.json`
3. Updated TypeScript configuration for Bun compatibility
4. Added `bun-types` as a dev dependency
5. Generated `bun.lock` file
6. Removed `package-lock.json`