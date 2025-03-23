# Tauri_NextJS_Template

npx create-next-app

npm install -D @tauri-apps/cli@latest
npx tauri init

Make sure that src-tauri/tauri.conf.json looks like this

{
  "build": {
    "beforeDevCommand": "npm run dev",
    "beforeBuildCommand": "npm run build",
    "devUrl": "http://localhost:3000",
    "frontendDist": "../out"
  }
}

Update next.config.ts to

const nextConfig: NextConfig = {
  output: "export",
};

npx tauri dev -> development
npx tauri build -> production build