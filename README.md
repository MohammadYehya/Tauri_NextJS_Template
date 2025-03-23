# Tauri_NextJS_Template
A simple and reusable template for setting up a Tauri project with NextJS+Tailwind for the frontend. This repository provides a structured starting point to avoid repetitive setup tasks.

## Prerequisites
Make sure you have the following installed:
- Node.js (LTS)
- Rust & Cargo (For Tauri)
- Tauri CLI

## Directory Structure
```
📦 tauri-next-tailwind-template
├── 📂 public                 # Next.js public folder
├── 📂 src                    # Next.js source code
│   ├── 📂 app                # Next.js App Router directory
│   ├── 📂 lib                # Utility functions
│   └── 📂 components         # Shadcn components
├── 📂 src-tauri              # Tauri configuration & Rust backend
│   ├── 📜 tauri.conf.json    # Tauri settings
│   └── 📜 Cargo.toml         # Rust dependencies
├── 📜 components.json        # Shadcn configs
├── 📜 package.json           # Dependencies & scripts
└── 📜 README.md              # This file
  ⋮
```

## Installation
1. **Clone the repository**
```bash
git clone https://github.com/MohammadYehya/Tauri_Next_Template.git
cd Tauri-Next-Template
```
2. **Install dependencies**
```bash
npm i
```
3. **Run the Tauri App**
```bash
npx tauri dev
```
4. **Build the Tauri App for Production**
```bash
npx tauri build
```

## Manual Installation
1. Create the frontend of the project
```bash
npx create-next-app
```
2. Update next.config.ts
```ts
const nextConfig: NextConfig = {
  output: "export",
};
```
3. Update tsconfig.json
```json
"exclude": ["node_modules", "src-tauri"]
```
4. Initialize the Tauri App
```bash
npx tauri init    
# If not already installed Tauri-Cli: npm install -D @tauri-apps/cli@latest
```
5. Update src-tauri/tauri.conf.json
```json
{
  "build": {
    "beforeDevCommand": "npm run dev",
    "beforeBuildCommand": "npm run build",
    "devUrl": "http://localhost:3000",
    "frontendDist": "../out"
  }
}
```
6. **Run the Tauri App**
```bash
npx tauri dev
```
7. **Build the Tauri App for Production**
```bash
npx tauri build
```

## Customization
Modify `src/app` to change the UI. Extend the structure as needed for more complex projects.

## Contributing
Feel free to submit issues and pull requests to improve this template.