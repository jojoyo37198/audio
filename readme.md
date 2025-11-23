

================================================================
File Path: .env
================================================================

VITE_SUPABASE_URL=https://olttfhcpbzutpfahidva.supabase.co
VITE_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im9sdHRmaGNwYnp1dHBmYWhpZHZhIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NjI2NTU4NTIsImV4cCI6MjA3ODIzMTg1Mn0.ZjbcroOkQQXGTlRKu29tO-2pa9jEDOAb10DZbn6viKE


================================================================
File Path: .env.example
================================================================

VITE_SUPABASE_URL=your_supabase_url_here
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key_here


================================================================
File Path: .gitignore
================================================================

.env
.env.local
.env*.local


================================================================
File Path: .npmrc
================================================================

loglevel=error
legacy-peer-deps=true


================================================================
File Path: eslint.config.js
================================================================

import js from '@eslint/js'
import globals from 'globals'
import reactHooks from 'eslint-plugin-react-hooks'
import reactRefresh from 'eslint-plugin-react-refresh'
import tseslint from 'typescript-eslint'

export default tseslint.config(
  { ignores: ['dist'] },
  {
    extends: [js.configs.recommended, ...tseslint.configs.recommended],
    files: ['**/*.{ts,tsx}'],
    languageOptions: {
      ecmaVersion: 2020,
      globals: globals.browser,
    },
    plugins: {
      'react-hooks': reactHooks,
      'react-refresh': reactRefresh,
    },
    rules: {
      ...reactHooks.configs.recommended.rules,
      'react-refresh/only-export-components': [
        'warn',
        { allowConstantExport: true },
      ],
    },
  },
)
 



================================================================
File Path: index.html
================================================================

<!doctype html>
<html lang="zh-TW">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>專業庭園設計與景觀維護｜打造永續綠色空間 - 悅境園藝</title>
   <meta name="description" content="悅境園藝｜專業庭園設計、景觀施工與永續植栽養護服務。為您打造獨特美麗的綠色空間,讓環境充滿自然生機。立即諮詢,專案規劃您的理想庭園。">
   <meta name="keywords" content="庭園設計,植栽養護,景觀施工,綠化工程,景觀維護">
    <script src="https://www.youtube.com/iframe_api"></script>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html> 



================================================================
File Path: knowledge.log
================================================================

 
[啟動] 已清空 knowledge.log 



================================================================
File Path: package-lock.json
================================================================

{
  "name": "vite-react-ts-template",
  "version": "0.0.0",
  "lockfileVersion": 3,
  "requires": true,
  "packages": {
    "": {
      "name": "vite-react-ts-template",
      "version": "0.0.0",
      "dependencies": {
        "@lumi.new/sdk": "0.2.1",
        "@supabase/supabase-js": "^2.80.0",
        "bcryptjs": "^3.0.3",
        "cors": "^2.8.5",
        "dotenv": "^17.2.3",
        "exceljs": "^4.4.0",
        "express": "^5.1.0",
        "framer-motion": "12.23.11",
        "lucide-react": "0.540.0",
        "multer": "^2.0.2",
        "papaparse": "^5.5.3",
        "react": "18.3.1",
        "react-dom": "18.3.1",
        "react-hot-toast": "2.5.2",
        "react-router-dom": "6.26.0"
      },
      "devDependencies": {
        "@eslint/js": "9.9.1",
        "@types/cors": "^2.8.19",
        "@types/express": "^5.0.5",
        "@types/multer": "^2.0.0",
        "@types/node": "^24.10.0",
        "@types/papaparse": "^5.3.14",
        "@types/react": "18.3.5",
        "@types/react-dom": "18.3.0",
        "@vitejs/plugin-react-swc": "3.11.0",
        "autoprefixer": "10.4.21",
        "eslint": "9.9.1",
        "eslint-plugin-react-hooks": "5.1.0-rc.0",
        "eslint-plugin-react-refresh": "0.4.11",
        "globals": "15.9.0",
        "postcss": "8.5.6",
        "tailwindcss": "3.4.17",
        "tsx": "^4.20.6",
        "typescript": "5.5.3",
        "typescript-eslint": "8.3.0",
        "vite": "^7.1.12",
        "vite-plugin-javascript-obfuscator": "^3.1.0",
        "vite-plugin-obfuscator": "^1.0.5"
      }
    },
    "node_modules/@alloc/quick-lru": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/@alloc/quick-lru/-/quick-lru-5.2.0.tgz",
      "integrity": "sha512-UrcABB+4bUrFABwbluTIBErXwvbsU/V7TZWfmbgJfbkwiBuziS9gxdODUyuiecfdGQ85jglMW6juS3+z5TsKLw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/@esbuild/aix-ppc64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/aix-ppc64/-/aix-ppc64-0.25.12.tgz",
      "integrity": "sha512-Hhmwd6CInZ3dwpuGTF8fJG6yoWmsToE+vYgD4nytZVxcu1ulHpUQRAB1UJ8+N1Am3Mz4+xOByoQoSZf4D+CpkA==",
      "cpu": [
        "ppc64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "aix"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/android-arm": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/android-arm/-/android-arm-0.25.12.tgz",
      "integrity": "sha512-VJ+sKvNA/GE7Ccacc9Cha7bpS8nyzVv0jdVgwNDaR4gDMC/2TTRc33Ip8qrNYUcpkOHUT5OZ0bUcNNVZQ9RLlg==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/android-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/android-arm64/-/android-arm64-0.25.12.tgz",
      "integrity": "sha512-6AAmLG7zwD1Z159jCKPvAxZd4y/VTO0VkprYy+3N2FtJ8+BQWFXU+OxARIwA46c5tdD9SsKGZ/1ocqBS/gAKHg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/android-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/android-x64/-/android-x64-0.25.12.tgz",
      "integrity": "sha512-5jbb+2hhDHx5phYR2By8GTWEzn6I9UqR11Kwf22iKbNpYrsmRB18aX/9ivc5cabcUiAT/wM+YIZ6SG9QO6a8kg==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/darwin-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/darwin-arm64/-/darwin-arm64-0.25.12.tgz",
      "integrity": "sha512-N3zl+lxHCifgIlcMUP5016ESkeQjLj/959RxxNYIthIg+CQHInujFuXeWbWMgnTo4cp5XVHqFPmpyu9J65C1Yg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/darwin-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/darwin-x64/-/darwin-x64-0.25.12.tgz",
      "integrity": "sha512-HQ9ka4Kx21qHXwtlTUVbKJOAnmG1ipXhdWTmNXiPzPfWKpXqASVcWdnf2bnL73wgjNrFXAa3yYvBSd9pzfEIpA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/freebsd-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/freebsd-arm64/-/freebsd-arm64-0.25.12.tgz",
      "integrity": "sha512-gA0Bx759+7Jve03K1S0vkOu5Lg/85dou3EseOGUes8flVOGxbhDDh/iZaoek11Y8mtyKPGF3vP8XhnkDEAmzeg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "freebsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/freebsd-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/freebsd-x64/-/freebsd-x64-0.25.12.tgz",
      "integrity": "sha512-TGbO26Yw2xsHzxtbVFGEXBFH0FRAP7gtcPE7P5yP7wGy7cXK2oO7RyOhL5NLiqTlBh47XhmIUXuGciXEqYFfBQ==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "freebsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-arm": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-arm/-/linux-arm-0.25.12.tgz",
      "integrity": "sha512-lPDGyC1JPDou8kGcywY0YILzWlhhnRjdof3UlcoqYmS9El818LLfJJc3PXXgZHrHCAKs/Z2SeZtDJr5MrkxtOw==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-arm64/-/linux-arm64-0.25.12.tgz",
      "integrity": "sha512-8bwX7a8FghIgrupcxb4aUmYDLp8pX06rGh5HqDT7bB+8Rdells6mHvrFHHW2JAOPZUbnjUpKTLg6ECyzvas2AQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-ia32": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-ia32/-/linux-ia32-0.25.12.tgz",
      "integrity": "sha512-0y9KrdVnbMM2/vG8KfU0byhUN+EFCny9+8g202gYqSSVMonbsCfLjUO+rCci7pM0WBEtz+oK/PIwHkzxkyharA==",
      "cpu": [
        "ia32"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-loong64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-loong64/-/linux-loong64-0.25.12.tgz",
      "integrity": "sha512-h///Lr5a9rib/v1GGqXVGzjL4TMvVTv+s1DPoxQdz7l/AYv6LDSxdIwzxkrPW438oUXiDtwM10o9PmwS/6Z0Ng==",
      "cpu": [
        "loong64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-mips64el": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-mips64el/-/linux-mips64el-0.25.12.tgz",
      "integrity": "sha512-iyRrM1Pzy9GFMDLsXn1iHUm18nhKnNMWscjmp4+hpafcZjrr2WbT//d20xaGljXDBYHqRcl8HnxbX6uaA/eGVw==",
      "cpu": [
        "mips64el"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-ppc64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-ppc64/-/linux-ppc64-0.25.12.tgz",
      "integrity": "sha512-9meM/lRXxMi5PSUqEXRCtVjEZBGwB7P/D4yT8UG/mwIdze2aV4Vo6U5gD3+RsoHXKkHCfSxZKzmDssVlRj1QQA==",
      "cpu": [
        "ppc64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-riscv64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-riscv64/-/linux-riscv64-0.25.12.tgz",
      "integrity": "sha512-Zr7KR4hgKUpWAwb1f3o5ygT04MzqVrGEGXGLnj15YQDJErYu/BGg+wmFlIDOdJp0PmB0lLvxFIOXZgFRrdjR0w==",
      "cpu": [
        "riscv64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-s390x": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-s390x/-/linux-s390x-0.25.12.tgz",
      "integrity": "sha512-MsKncOcgTNvdtiISc/jZs/Zf8d0cl/t3gYWX8J9ubBnVOwlk65UIEEvgBORTiljloIWnBzLs4qhzPkJcitIzIg==",
      "cpu": [
        "s390x"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/linux-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/linux-x64/-/linux-x64-0.25.12.tgz",
      "integrity": "sha512-uqZMTLr/zR/ed4jIGnwSLkaHmPjOjJvnm6TVVitAa08SLS9Z0VM8wIRx7gWbJB5/J54YuIMInDquWyYvQLZkgw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/netbsd-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/netbsd-arm64/-/netbsd-arm64-0.25.12.tgz",
      "integrity": "sha512-xXwcTq4GhRM7J9A8Gv5boanHhRa/Q9KLVmcyXHCTaM4wKfIpWkdXiMog/KsnxzJ0A1+nD+zoecuzqPmCRyBGjg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "netbsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/netbsd-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/netbsd-x64/-/netbsd-x64-0.25.12.tgz",
      "integrity": "sha512-Ld5pTlzPy3YwGec4OuHh1aCVCRvOXdH8DgRjfDy/oumVovmuSzWfnSJg+VtakB9Cm0gxNO9BzWkj6mtO1FMXkQ==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "netbsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/openbsd-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/openbsd-arm64/-/openbsd-arm64-0.25.12.tgz",
      "integrity": "sha512-fF96T6KsBo/pkQI950FARU9apGNTSlZGsv1jZBAlcLL1MLjLNIWPBkj5NlSz8aAzYKg+eNqknrUJ24QBybeR5A==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "openbsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/openbsd-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/openbsd-x64/-/openbsd-x64-0.25.12.tgz",
      "integrity": "sha512-MZyXUkZHjQxUvzK7rN8DJ3SRmrVrke8ZyRusHlP+kuwqTcfWLyqMOE3sScPPyeIXN/mDJIfGXvcMqCgYKekoQw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "openbsd"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/openharmony-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/openharmony-arm64/-/openharmony-arm64-0.25.12.tgz",
      "integrity": "sha512-rm0YWsqUSRrjncSXGA7Zv78Nbnw4XL6/dzr20cyrQf7ZmRcsovpcRBdhD43Nuk3y7XIoW2OxMVvwuRvk9XdASg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "openharmony"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/sunos-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/sunos-x64/-/sunos-x64-0.25.12.tgz",
      "integrity": "sha512-3wGSCDyuTHQUzt0nV7bocDy72r2lI33QL3gkDNGkod22EsYl04sMf0qLb8luNKTOmgF/eDEDP5BFNwoBKH441w==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "sunos"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/win32-arm64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/win32-arm64/-/win32-arm64-0.25.12.tgz",
      "integrity": "sha512-rMmLrur64A7+DKlnSuwqUdRKyd3UE7oPJZmnljqEptesKM8wx9J8gx5u0+9Pq0fQQW8vqeKebwNXdfOyP+8Bsg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/win32-ia32": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/win32-ia32/-/win32-ia32-0.25.12.tgz",
      "integrity": "sha512-HkqnmmBoCbCwxUKKNPBixiWDGCpQGVsrQfJoVGYLPT41XWF8lHuE5N6WhVia2n4o5QK5M4tYr21827fNhi4byQ==",
      "cpu": [
        "ia32"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@esbuild/win32-x64": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/@esbuild/win32-x64/-/win32-x64-0.25.12.tgz",
      "integrity": "sha512-alJC0uCZpTFrSL0CCDjcgleBXPnCrEAhTBILpeAp7M/OFgoqtAetfBzX0xM00MUsVVPpVjlPuMbREqnZCXaTnA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/@eslint-community/eslint-utils": {
      "version": "4.9.0",
      "resolved": "https://registry.npmjs.org/@eslint-community/eslint-utils/-/eslint-utils-4.9.0.tgz",
      "integrity": "sha512-ayVFHdtZ+hsq1t2Dy24wCmGXGe4q9Gu3smhLYALJrr473ZH27MsnSL+LKUlimp4BWJqMDMLmPpx/Q9R3OAlL4g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "eslint-visitor-keys": "^3.4.3"
      },
      "engines": {
        "node": "^12.22.0 || ^14.17.0 || >=16.0.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      },
      "peerDependencies": {
        "eslint": "^6.0.0 || ^7.0.0 || >=8.0.0"
      }
    },
    "node_modules/@eslint-community/eslint-utils/node_modules/eslint-visitor-keys": {
      "version": "3.4.3",
      "resolved": "https://registry.npmjs.org/eslint-visitor-keys/-/eslint-visitor-keys-3.4.3.tgz",
      "integrity": "sha512-wpc+LXeiyiisxPlEkUzU6svyS1frIO3Mgxj1fdy7Pm8Ygzguax2N3Fa/D/ag1WqbOprdI+uY6wMUl8/a2G+iag==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": "^12.22.0 || ^14.17.0 || >=16.0.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/@eslint-community/regexpp": {
      "version": "4.12.2",
      "resolved": "https://registry.npmjs.org/@eslint-community/regexpp/-/regexpp-4.12.2.tgz",
      "integrity": "sha512-EriSTlt5OC9/7SXkRSCAhfSxxoSUgBm33OH+IkwbdpgoqsSsUg7y3uh+IICI/Qg4BBWr3U2i39RpmycbxMq4ew==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": "^12.0.0 || ^14.0.0 || >=16.0.0"
      }
    },
    "node_modules/@eslint/config-array": {
      "version": "0.18.0",
      "resolved": "https://registry.npmjs.org/@eslint/config-array/-/config-array-0.18.0.tgz",
      "integrity": "sha512-fTxvnS1sRMu3+JjXwJG0j/i4RT9u4qJ+lqS/yCGap4lH4zZGzQ7tu+xZqQmcMZq5OBZDL4QRxQzRjkWcGt8IVw==",
      "dev": true,
      "license": "Apache-2.0",
      "dependencies": {
        "@eslint/object-schema": "^2.1.4",
        "debug": "^4.3.1",
        "minimatch": "^3.1.2"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      }
    },
    "node_modules/@eslint/eslintrc": {
      "version": "3.3.1",
      "resolved": "https://registry.npmjs.org/@eslint/eslintrc/-/eslintrc-3.3.1.tgz",
      "integrity": "sha512-gtF186CXhIl1p4pJNGZw8Yc6RlshoePRvE0X91oPGb3vZ8pM3qOS9W9NGPat9LziaBV7XrJWGylNQXkGcnM3IQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ajv": "^6.12.4",
        "debug": "^4.3.2",
        "espree": "^10.0.1",
        "globals": "^14.0.0",
        "ignore": "^5.2.0",
        "import-fresh": "^3.2.1",
        "js-yaml": "^4.1.0",
        "minimatch": "^3.1.2",
        "strip-json-comments": "^3.1.1"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/@eslint/eslintrc/node_modules/globals": {
      "version": "14.0.0",
      "resolved": "https://registry.npmjs.org/globals/-/globals-14.0.0.tgz",
      "integrity": "sha512-oahGvuMGQlPw/ivIYBjVSrWAfWLBeku5tpPE2fOPLi+WHffIWbuh2tCjhyQhTBPMf5E9jDEH4FOmTYgYwbKwtQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=18"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/@eslint/js": {
      "version": "9.9.1",
      "resolved": "https://registry.npmjs.org/@eslint/js/-/js-9.9.1.tgz",
      "integrity": "sha512-xIDQRsfg5hNBqHz04H1R3scSVwmI+KUbqjsQKHKQ1DAUSaUjYPReZZmS/5PNiKu1fUvzDd6H7DEDKACSEhu+TQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      }
    },
    "node_modules/@eslint/object-schema": {
      "version": "2.1.7",
      "resolved": "https://registry.npmjs.org/@eslint/object-schema/-/object-schema-2.1.7.tgz",
      "integrity": "sha512-VtAOaymWVfZcmZbp6E2mympDIHvyjXs/12LqWYjVw6qjrfF+VK+fyG33kChz3nnK+SU5/NeHOqrTEHS8sXO3OA==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      }
    },
    "node_modules/@fast-csv/format": {
      "version": "4.3.5",
      "resolved": "https://registry.npmjs.org/@fast-csv/format/-/format-4.3.5.tgz",
      "integrity": "sha512-8iRn6QF3I8Ak78lNAa+Gdl5MJJBM5vRHivFtMRUWINdevNo00K7OXxS2PshawLKTejVwieIlPmK5YlLu6w4u8A==",
      "license": "MIT",
      "dependencies": {
        "@types/node": "^14.0.1",
        "lodash.escaperegexp": "^4.1.2",
        "lodash.isboolean": "^3.0.3",
        "lodash.isequal": "^4.5.0",
        "lodash.isfunction": "^3.0.9",
        "lodash.isnil": "^4.0.0"
      }
    },
    "node_modules/@fast-csv/format/node_modules/@types/node": {
      "version": "14.18.63",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-14.18.63.tgz",
      "integrity": "sha512-fAtCfv4jJg+ExtXhvCkCqUKZ+4ok/JQk01qDKhL5BDDoS3AxKXhV5/MAVUZyQnSEd2GT92fkgZl0pz0Q0AzcIQ==",
      "license": "MIT"
    },
    "node_modules/@fast-csv/parse": {
      "version": "4.3.6",
      "resolved": "https://registry.npmjs.org/@fast-csv/parse/-/parse-4.3.6.tgz",
      "integrity": "sha512-uRsLYksqpbDmWaSmzvJcuApSEe38+6NQZBUsuAyMZKqHxH0g1wcJgsKUvN3WC8tewaqFjBMMGrkHmC+T7k8LvA==",
      "license": "MIT",
      "dependencies": {
        "@types/node": "^14.0.1",
        "lodash.escaperegexp": "^4.1.2",
        "lodash.groupby": "^4.6.0",
        "lodash.isfunction": "^3.0.9",
        "lodash.isnil": "^4.0.0",
        "lodash.isundefined": "^3.0.1",
        "lodash.uniq": "^4.5.0"
      }
    },
    "node_modules/@fast-csv/parse/node_modules/@types/node": {
      "version": "14.18.63",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-14.18.63.tgz",
      "integrity": "sha512-fAtCfv4jJg+ExtXhvCkCqUKZ+4ok/JQk01qDKhL5BDDoS3AxKXhV5/MAVUZyQnSEd2GT92fkgZl0pz0Q0AzcIQ==",
      "license": "MIT"
    },
    "node_modules/@humanwhocodes/module-importer": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/@humanwhocodes/module-importer/-/module-importer-1.0.1.tgz",
      "integrity": "sha512-bxveV4V8v5Yb4ncFTT3rPSgZBOpCkjfK0y4oVVVJwIuDVBRMDXrPyXRL988i5ap9m9bnyEEjWfm5WkBmtffLfA==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": ">=12.22"
      },
      "funding": {
        "type": "github",
        "url": "https://github.com/sponsors/nzakas"
      }
    },
    "node_modules/@humanwhocodes/retry": {
      "version": "0.3.1",
      "resolved": "https://registry.npmjs.org/@humanwhocodes/retry/-/retry-0.3.1.tgz",
      "integrity": "sha512-JBxkERygn7Bv/GbN5Rv8Ul6LVknS+5Bp6RgDC/O8gEBU/yeH5Ui5C/OlWrTb6qct7LjjfT6Re2NxB0ln0yYybA==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": ">=18.18"
      },
      "funding": {
        "type": "github",
        "url": "https://github.com/sponsors/nzakas"
      }
    },
    "node_modules/@isaacs/cliui": {
      "version": "8.0.2",
      "resolved": "https://registry.npmjs.org/@isaacs/cliui/-/cliui-8.0.2.tgz",
      "integrity": "sha512-O8jcjabXaleOG9DQ0+ARXWZBTfnP4WNAqzuiJK7ll44AmxGKv/J2M4TPjxjY3znBCfvBXFzucm1twdyFybFqEA==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "string-width": "^5.1.2",
        "string-width-cjs": "npm:string-width@^4.2.0",
        "strip-ansi": "^7.0.1",
        "strip-ansi-cjs": "npm:strip-ansi@^6.0.1",
        "wrap-ansi": "^8.1.0",
        "wrap-ansi-cjs": "npm:wrap-ansi@^7.0.0"
      },
      "engines": {
        "node": ">=12"
      }
    },
    "node_modules/@isaacs/cliui/node_modules/ansi-regex": {
      "version": "6.2.2",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-6.2.2.tgz",
      "integrity": "sha512-Bq3SmSpyFHaWjPk8If9yc6svM8c56dB5BAtW4Qbw5jHTwwXXcTLoRMkpDJp6VL0XzlWaCHTXrkFURMYmD0sLqg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-regex?sponsor=1"
      }
    },
    "node_modules/@isaacs/cliui/node_modules/strip-ansi": {
      "version": "7.1.2",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-7.1.2.tgz",
      "integrity": "sha512-gmBGslpoQJtgnMAvOVqGZpEz9dyoKTCzy2nfz/n8aIFhN/jCE/rCmcxabB6jOOHV+0WNnylOxaxBQPSvcWklhA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^6.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/strip-ansi?sponsor=1"
      }
    },
    "node_modules/@javascript-obfuscator/escodegen": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/@javascript-obfuscator/escodegen/-/escodegen-2.3.0.tgz",
      "integrity": "sha512-QVXwMIKqYMl3KwtTirYIA6gOCiJ0ZDtptXqAv/8KWLG9uQU2fZqTVy7a/A5RvcoZhbDoFfveTxuGxJ5ibzQtkw==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "@javascript-obfuscator/estraverse": "^5.3.0",
        "esprima": "^4.0.1",
        "esutils": "^2.0.2",
        "optionator": "^0.8.1"
      },
      "engines": {
        "node": ">=6.0"
      },
      "optionalDependencies": {
        "source-map": "~0.6.1"
      }
    },
    "node_modules/@javascript-obfuscator/escodegen/node_modules/levn": {
      "version": "0.3.0",
      "resolved": "https://registry.npmjs.org/levn/-/levn-0.3.0.tgz",
      "integrity": "sha512-0OO4y2iOHix2W6ujICbKIaEQXvFQHue65vUG3pb5EUomzPI90z9hsA1VsO/dbIIpC53J8gxM9Q4Oho0jrCM/yA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "prelude-ls": "~1.1.2",
        "type-check": "~0.3.2"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/@javascript-obfuscator/escodegen/node_modules/optionator": {
      "version": "0.8.3",
      "resolved": "https://registry.npmjs.org/optionator/-/optionator-0.8.3.tgz",
      "integrity": "sha512-+IW9pACdk3XWmmTXG8m3upGUJst5XRGzxMRjXzAuJ1XnIFNvfhjjIuYkDvysnPQ7qzqVzLt78BCruntqRhWQbA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "deep-is": "~0.1.3",
        "fast-levenshtein": "~2.0.6",
        "levn": "~0.3.0",
        "prelude-ls": "~1.1.2",
        "type-check": "~0.3.2",
        "word-wrap": "~1.2.3"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/@javascript-obfuscator/escodegen/node_modules/prelude-ls": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/prelude-ls/-/prelude-ls-1.1.2.tgz",
      "integrity": "sha512-ESF23V4SKG6lVSGZgYNpbsiaAkdab6ZgOxe52p7+Kid3W3u3bxR4Vfd/o21dmN7jSt0IwgZ4v5MUd26FEtXE9w==",
      "dev": true,
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/@javascript-obfuscator/escodegen/node_modules/type-check": {
      "version": "0.3.2",
      "resolved": "https://registry.npmjs.org/type-check/-/type-check-0.3.2.tgz",
      "integrity": "sha512-ZCmOJdvOWDBYJlzAoFkC+Q0+bUyEOS1ltgp1MGU03fqHG+dbi9tBFU2Rd9QKiDZFAYrhPh2JUf7rZRIuHRKtOg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "prelude-ls": "~1.1.2"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/@javascript-obfuscator/estraverse": {
      "version": "5.4.0",
      "resolved": "https://registry.npmjs.org/@javascript-obfuscator/estraverse/-/estraverse-5.4.0.tgz",
      "integrity": "sha512-CZFX7UZVN9VopGbjTx4UXaXsi9ewoM1buL0kY7j1ftYdSs7p2spv9opxFjHlQ/QGTgh4UqufYqJJ0WKLml7b6w==",
      "dev": true,
      "license": "BSD-2-Clause",
      "engines": {
        "node": ">=4.0"
      }
    },
    "node_modules/@jridgewell/gen-mapping": {
      "version": "0.3.13",
      "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.3.13.tgz",
      "integrity": "sha512-2kkt/7niJ6MgEPxF0bYdQ6etZaA+fQvDcLKckhy1yIQOzaoKjBBjSj63/aLVjYE3qhRt5dvM+uUyfCg6UKCBbA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/sourcemap-codec": "^1.5.0",
        "@jridgewell/trace-mapping": "^0.3.24"
      }
    },
    "node_modules/@jridgewell/resolve-uri": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/resolve-uri/-/resolve-uri-3.1.2.tgz",
      "integrity": "sha512-bRISgCIjP20/tbWSPWMEi54QVPRZExkuD9lJL+UIxUKtwVJA8wW1Trb1jMs1RFXo1CBTNZ/5hpC9QvmKWdopKw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@jridgewell/sourcemap-codec": {
      "version": "1.5.5",
      "resolved": "https://registry.npmjs.org/@jridgewell/sourcemap-codec/-/sourcemap-codec-1.5.5.tgz",
      "integrity": "sha512-cYQ9310grqxueWbl+WuIUIaiUaDcj7WOq5fVhEljNVgRfOUhY9fy2zTvfoqWsnebh8Sl70VScFbICvJnLKB0Og==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@jridgewell/trace-mapping": {
      "version": "0.3.31",
      "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.31.tgz",
      "integrity": "sha512-zzNR+SdQSDJzc8joaeP8QQoCQr8NuYx2dIIytl1QeBEZHJ9uW6hebsrYgbz8hJwUQao3TWCMtmfV8Nu1twOLAw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/resolve-uri": "^3.1.0",
        "@jridgewell/sourcemap-codec": "^1.4.14"
      }
    },
    "node_modules/@lumi.new/sdk": {
      "version": "0.2.1",
      "resolved": "https://registry.npmjs.org/@lumi.new/sdk/-/sdk-0.2.1.tgz",
      "integrity": "sha512-FSqGe/3fudj989JQRBaIix8e7IA0UW1r8saZD2Nvy7nfhuHsGnDDhB33xTzmmpTSc0w06+GnFVK0cMvxXCqqGA==",
      "dependencies": {
        "crypto-js": "^4.2.0",
        "object-hash": "^3.0.0",
        "ofetch": "^1.4.1",
        "uuid": "^11.1.0"
      }
    },
    "node_modules/@nodelib/fs.scandir": {
      "version": "2.1.5",
      "resolved": "https://registry.npmjs.org/@nodelib/fs.scandir/-/fs.scandir-2.1.5.tgz",
      "integrity": "sha512-vq24Bq3ym5HEQm2NKCr3yXDwjc7vTsEThRDnkp2DK9p1uqLR+DHurm/NOTo0KG7HYHU7eppKZj3MyqYuMBf62g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@nodelib/fs.stat": "2.0.5",
        "run-parallel": "^1.1.9"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/@nodelib/fs.stat": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/@nodelib/fs.stat/-/fs.stat-2.0.5.tgz",
      "integrity": "sha512-RkhPPp2zrqDAQA/2jNhnztcPAlv64XdhIp7a7454A5ovI7Bukxgt7MX7udwAu3zg1DcpPU0rz3VV1SeaqvY4+A==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/@nodelib/fs.walk": {
      "version": "1.2.8",
      "resolved": "https://registry.npmjs.org/@nodelib/fs.walk/-/fs.walk-1.2.8.tgz",
      "integrity": "sha512-oGB+UxlgWcgQkgwo8GcEGwemoTFt3FIO9ababBmaGwXIoBKZ+GTy0pP185beGg7Llih/NSHSV2XAs1lnznocSg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@nodelib/fs.scandir": "2.1.5",
        "fastq": "^1.6.0"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/@pkgjs/parseargs": {
      "version": "0.11.0",
      "resolved": "https://registry.npmjs.org/@pkgjs/parseargs/-/parseargs-0.11.0.tgz",
      "integrity": "sha512-+1VkjdD0QBLPodGrJUeqarH8VAIvQODIbwh9XpP5Syisf7YoQgsJKPNFoqqLQlu+VQ/tVSshMR6loPMn8U+dPg==",
      "dev": true,
      "license": "MIT",
      "optional": true,
      "engines": {
        "node": ">=14"
      }
    },
    "node_modules/@remix-run/router": {
      "version": "1.19.0",
      "resolved": "https://registry.npmjs.org/@remix-run/router/-/router-1.19.0.tgz",
      "integrity": "sha512-zDICCLKEwbVYTS6TjYaWtHXxkdoUvD/QXvyVZjGCsWz5vyH7aFeONlPffPdW+Y/t6KT0MgXb2Mfjun9YpWN1dA==",
      "license": "MIT",
      "engines": {
        "node": ">=14.0.0"
      }
    },
    "node_modules/@rolldown/pluginutils": {
      "version": "1.0.0-beta.27",
      "resolved": "https://registry.npmjs.org/@rolldown/pluginutils/-/pluginutils-1.0.0-beta.27.tgz",
      "integrity": "sha512-+d0F4MKMCbeVUJwG96uQ4SgAznZNSq93I3V+9NHA4OpvqG8mRCpGdKmK8l/dl02h2CCDHwW2FqilnTyDcAnqjA==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@rollup/rollup-android-arm-eabi": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-android-arm-eabi/-/rollup-android-arm-eabi-4.53.2.tgz",
      "integrity": "sha512-yDPzwsgiFO26RJA4nZo8I+xqzh7sJTZIWQOxn+/XOdPE31lAvLIYCKqjV+lNH/vxE2L2iH3plKxDCRK6i+CwhA==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ]
    },
    "node_modules/@rollup/rollup-android-arm64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-android-arm64/-/rollup-android-arm64-4.53.2.tgz",
      "integrity": "sha512-k8FontTxIE7b0/OGKeSN5B6j25EuppBcWM33Z19JoVT7UTXFSo3D9CdU39wGTeb29NO3XxpMNauh09B+Ibw+9g==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "android"
      ]
    },
    "node_modules/@rollup/rollup-darwin-arm64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-darwin-arm64/-/rollup-darwin-arm64-4.53.2.tgz",
      "integrity": "sha512-A6s4gJpomNBtJ2yioj8bflM2oogDwzUiMl2yNJ2v9E7++sHrSrsQ29fOfn5DM/iCzpWcebNYEdXpaK4tr2RhfQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ]
    },
    "node_modules/@rollup/rollup-darwin-x64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-darwin-x64/-/rollup-darwin-x64-4.53.2.tgz",
      "integrity": "sha512-e6XqVmXlHrBlG56obu9gDRPW3O3hLxpwHpLsBJvuI8qqnsrtSZ9ERoWUXtPOkY8c78WghyPHZdmPhHLWNdAGEw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ]
    },
    "node_modules/@rollup/rollup-freebsd-arm64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-freebsd-arm64/-/rollup-freebsd-arm64-4.53.2.tgz",
      "integrity": "sha512-v0E9lJW8VsrwPux5Qe5CwmH/CF/2mQs6xU1MF3nmUxmZUCHazCjLgYvToOk+YuuUqLQBio1qkkREhxhc656ViA==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "freebsd"
      ]
    },
    "node_modules/@rollup/rollup-freebsd-x64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-freebsd-x64/-/rollup-freebsd-x64-4.53.2.tgz",
      "integrity": "sha512-ClAmAPx3ZCHtp6ysl4XEhWU69GUB1D+s7G9YjHGhIGCSrsg00nEGRRZHmINYxkdoJehde8VIsDC5t9C0gb6yqA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "freebsd"
      ]
    },
    "node_modules/@rollup/rollup-linux-arm-gnueabihf": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-arm-gnueabihf/-/rollup-linux-arm-gnueabihf-4.53.2.tgz",
      "integrity": "sha512-EPlb95nUsz6Dd9Qy13fI5kUPXNSljaG9FiJ4YUGU1O/Q77i5DYFW5KR8g1OzTcdZUqQQ1KdDqsTohdFVwCwjqg==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-arm-musleabihf": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-arm-musleabihf/-/rollup-linux-arm-musleabihf-4.53.2.tgz",
      "integrity": "sha512-BOmnVW+khAUX+YZvNfa0tGTEMVVEerOxN0pDk2E6N6DsEIa2Ctj48FOMfNDdrwinocKaC7YXUZ1pHlKpnkja/Q==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-arm64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-arm64-gnu/-/rollup-linux-arm64-gnu-4.53.2.tgz",
      "integrity": "sha512-Xt2byDZ+6OVNuREgBXr4+CZDJtrVso5woFtpKdGPhpTPHcNG7D8YXeQzpNbFRxzTVqJf7kvPMCub/pcGUWgBjA==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-arm64-musl": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-arm64-musl/-/rollup-linux-arm64-musl-4.53.2.tgz",
      "integrity": "sha512-+LdZSldy/I9N8+klim/Y1HsKbJ3BbInHav5qE9Iy77dtHC/pibw1SR/fXlWyAk0ThnpRKoODwnAuSjqxFRDHUQ==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-loong64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-loong64-gnu/-/rollup-linux-loong64-gnu-4.53.2.tgz",
      "integrity": "sha512-8ms8sjmyc1jWJS6WdNSA23rEfdjWB30LH8Wqj0Cqvv7qSHnvw6kgMMXRdop6hkmGPlyYBdRPkjJnj3KCUHV/uQ==",
      "cpu": [
        "loong64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-ppc64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-ppc64-gnu/-/rollup-linux-ppc64-gnu-4.53.2.tgz",
      "integrity": "sha512-3HRQLUQbpBDMmzoxPJYd3W6vrVHOo2cVW8RUo87Xz0JPJcBLBr5kZ1pGcQAhdZgX9VV7NbGNipah1omKKe23/g==",
      "cpu": [
        "ppc64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-riscv64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-riscv64-gnu/-/rollup-linux-riscv64-gnu-4.53.2.tgz",
      "integrity": "sha512-fMjKi+ojnmIvhk34gZP94vjogXNNUKMEYs+EDaB/5TG/wUkoeua7p7VCHnE6T2Tx+iaghAqQX8teQzcvrYpaQA==",
      "cpu": [
        "riscv64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-riscv64-musl": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-riscv64-musl/-/rollup-linux-riscv64-musl-4.53.2.tgz",
      "integrity": "sha512-XuGFGU+VwUUV5kLvoAdi0Wz5Xbh2SrjIxCtZj6Wq8MDp4bflb/+ThZsVxokM7n0pcbkEr2h5/pzqzDYI7cCgLQ==",
      "cpu": [
        "riscv64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-s390x-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-s390x-gnu/-/rollup-linux-s390x-gnu-4.53.2.tgz",
      "integrity": "sha512-w6yjZF0P+NGzWR3AXWX9zc0DNEGdtvykB03uhonSHMRa+oWA6novflo2WaJr6JZakG2ucsyb+rvhrKac6NIy+w==",
      "cpu": [
        "s390x"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-x64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-x64-gnu/-/rollup-linux-x64-gnu-4.53.2.tgz",
      "integrity": "sha512-yo8d6tdfdeBArzC7T/PnHd7OypfI9cbuZzPnzLJIyKYFhAQ8SvlkKtKBMbXDxe1h03Rcr7u++nFS7tqXz87Gtw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-linux-x64-musl": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-linux-x64-musl/-/rollup-linux-x64-musl-4.53.2.tgz",
      "integrity": "sha512-ah59c1YkCxKExPP8O9PwOvs+XRLKwh/mV+3YdKqQ5AMQ0r4M4ZDuOrpWkUaqO7fzAHdINzV9tEVu8vNw48z0lA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "linux"
      ]
    },
    "node_modules/@rollup/rollup-openharmony-arm64": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-openharmony-arm64/-/rollup-openharmony-arm64-4.53.2.tgz",
      "integrity": "sha512-4VEd19Wmhr+Zy7hbUsFZ6YXEiP48hE//KPLCSVNY5RMGX2/7HZ+QkN55a3atM1C/BZCGIgqN+xrVgtdak2S9+A==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "openharmony"
      ]
    },
    "node_modules/@rollup/rollup-win32-arm64-msvc": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-win32-arm64-msvc/-/rollup-win32-arm64-msvc-4.53.2.tgz",
      "integrity": "sha512-IlbHFYc/pQCgew/d5fslcy1KEaYVCJ44G8pajugd8VoOEI8ODhtb/j8XMhLpwHCMB3yk2J07ctup10gpw2nyMA==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ]
    },
    "node_modules/@rollup/rollup-win32-ia32-msvc": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-win32-ia32-msvc/-/rollup-win32-ia32-msvc-4.53.2.tgz",
      "integrity": "sha512-lNlPEGgdUfSzdCWU176ku/dQRnA7W+Gp8d+cWv73jYrb8uT7HTVVxq62DUYxjbaByuf1Yk0RIIAbDzp+CnOTFg==",
      "cpu": [
        "ia32"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ]
    },
    "node_modules/@rollup/rollup-win32-x64-gnu": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-win32-x64-gnu/-/rollup-win32-x64-gnu-4.53.2.tgz",
      "integrity": "sha512-S6YojNVrHybQis2lYov1sd+uj7K0Q05NxHcGktuMMdIQ2VixGwAfbJ23NnlvvVV1bdpR2m5MsNBViHJKcA4ADw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ]
    },
    "node_modules/@rollup/rollup-win32-x64-msvc": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/@rollup/rollup-win32-x64-msvc/-/rollup-win32-x64-msvc-4.53.2.tgz",
      "integrity": "sha512-k+/Rkcyx//P6fetPoLMb8pBeqJBNGx81uuf7iljX9++yNBVRDQgD04L+SVXmXmh5ZP4/WOp4mWF0kmi06PW2tA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "win32"
      ]
    },
    "node_modules/@supabase/auth-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/auth-js/-/auth-js-2.81.1.tgz",
      "integrity": "sha512-K20GgiSm9XeRLypxYHa5UCnybWc2K0ok0HLbqCej/wRxDpJxToXNOwKt0l7nO8xI1CyQ+GrNfU6bcRzvdbeopQ==",
      "license": "MIT",
      "dependencies": {
        "tslib": "2.8.1"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@supabase/functions-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/functions-js/-/functions-js-2.81.1.tgz",
      "integrity": "sha512-sYgSO3mlgL0NvBFS3oRfCK4OgKGQwuOWJLzfPyWg0k8MSxSFSDeN/JtrDJD5GQrxskP6c58+vUzruBJQY78AqQ==",
      "license": "MIT",
      "dependencies": {
        "tslib": "2.8.1"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@supabase/postgrest-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/postgrest-js/-/postgrest-js-2.81.1.tgz",
      "integrity": "sha512-DePpUTAPXJyBurQ4IH2e42DWoA+/Qmr5mbgY4B6ZcxVc/ZUKfTVK31BYIFBATMApWraFc8Q/Sg+yxtfJ3E0wSg==",
      "license": "MIT",
      "dependencies": {
        "tslib": "2.8.1"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@supabase/realtime-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/realtime-js/-/realtime-js-2.81.1.tgz",
      "integrity": "sha512-ViQ+Kxm8BuUP/TcYmH9tViqYKGSD1LBjdqx2p5J+47RES6c+0QHedM0PPAjthMdAHWyb2LGATE9PD2++2rO/tw==",
      "license": "MIT",
      "dependencies": {
        "@types/phoenix": "^1.6.6",
        "@types/ws": "^8.18.1",
        "tslib": "2.8.1",
        "ws": "^8.18.2"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@supabase/storage-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/storage-js/-/storage-js-2.81.1.tgz",
      "integrity": "sha512-UNmYtjnZnhouqnbEMC1D5YJot7y0rIaZx7FG2Fv8S3hhNjcGVvO+h9We/tggi273BFkiahQPS/uRsapo1cSapw==",
      "license": "MIT",
      "dependencies": {
        "tslib": "2.8.1"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@supabase/supabase-js": {
      "version": "2.81.1",
      "resolved": "https://registry.npmjs.org/@supabase/supabase-js/-/supabase-js-2.81.1.tgz",
      "integrity": "sha512-KSdY7xb2L0DlLmlYzIOghdw/na4gsMcqJ8u4sD6tOQJr+x3hLujU9s4R8N3ob84/1bkvpvlU5PYKa1ae+OICnw==",
      "license": "MIT",
      "dependencies": {
        "@supabase/auth-js": "2.81.1",
        "@supabase/functions-js": "2.81.1",
        "@supabase/postgrest-js": "2.81.1",
        "@supabase/realtime-js": "2.81.1",
        "@supabase/storage-js": "2.81.1"
      },
      "engines": {
        "node": ">=20.0.0"
      }
    },
    "node_modules/@swc/core": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core/-/core-1.15.2.tgz",
      "integrity": "sha512-OQm+yJdXxvSjqGeaWhP6Ia264ogifwAO7Q12uTDVYj/Ks4jBTI4JknlcjDRAXtRhqbWsfbZyK/5RtuIPyptk3w==",
      "dev": true,
      "hasInstallScript": true,
      "license": "Apache-2.0",
      "dependencies": {
        "@swc/counter": "^0.1.3",
        "@swc/types": "^0.1.25"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/swc"
      },
      "optionalDependencies": {
        "@swc/core-darwin-arm64": "1.15.2",
        "@swc/core-darwin-x64": "1.15.2",
        "@swc/core-linux-arm-gnueabihf": "1.15.2",
        "@swc/core-linux-arm64-gnu": "1.15.2",
        "@swc/core-linux-arm64-musl": "1.15.2",
        "@swc/core-linux-x64-gnu": "1.15.2",
        "@swc/core-linux-x64-musl": "1.15.2",
        "@swc/core-win32-arm64-msvc": "1.15.2",
        "@swc/core-win32-ia32-msvc": "1.15.2",
        "@swc/core-win32-x64-msvc": "1.15.2"
      },
      "peerDependencies": {
        "@swc/helpers": ">=0.5.17"
      },
      "peerDependenciesMeta": {
        "@swc/helpers": {
          "optional": true
        }
      }
    },
    "node_modules/@swc/core-darwin-arm64": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-darwin-arm64/-/core-darwin-arm64-1.15.2.tgz",
      "integrity": "sha512-Ghyz4RJv4zyXzrUC1B2MLQBbppIB5c4jMZJybX2ebdEQAvryEKp3gq1kBksCNsatKGmEgXul88SETU19sMWcrw==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-darwin-x64": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-darwin-x64/-/core-darwin-x64-1.15.2.tgz",
      "integrity": "sha512-7n/PGJOcL2QoptzL42L5xFFfXY5rFxLHnuz1foU+4ruUTG8x2IebGhtwVTpaDN8ShEv2UZObBlT1rrXTba15Zw==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-linux-arm-gnueabihf": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-linux-arm-gnueabihf/-/core-linux-arm-gnueabihf-1.15.2.tgz",
      "integrity": "sha512-ZUQVCfRJ9wimuxkStRSlLwqX4TEDmv6/J+E6FicGkQ6ssLMWoKDy0cAo93HiWt/TWEee5vFhFaSQYzCuBEGO6A==",
      "cpu": [
        "arm"
      ],
      "dev": true,
      "license": "Apache-2.0",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-linux-arm64-gnu": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-linux-arm64-gnu/-/core-linux-arm64-gnu-1.15.2.tgz",
      "integrity": "sha512-GZh3pYBmfnpQ+JIg+TqLuz+pM+Mjsk5VOzi8nwKn/m+GvQBsxD5ectRtxuWUxMGNG8h0lMy4SnHRqdK3/iJl7A==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-linux-arm64-musl": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-linux-arm64-musl/-/core-linux-arm64-musl-1.15.2.tgz",
      "integrity": "sha512-5av6VYZZeneiYIodwzGMlnyVakpuYZryGzFIbgu1XP8wVylZxduEzup4eP8atiMDFmIm+s4wn8GySJmYqeJC0A==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-linux-x64-gnu": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-linux-x64-gnu/-/core-linux-x64-gnu-1.15.2.tgz",
      "integrity": "sha512-1nO/UfdCLuT/uE/7oB3EZgTeZDCIa6nL72cFEpdegnqpJVNDI6Qb8U4g/4lfVPkmHq2lvxQ0L+n+JdgaZLhrRA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-linux-x64-musl": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-linux-x64-musl/-/core-linux-x64-musl-1.15.2.tgz",
      "integrity": "sha512-Ksfrb0Tx310kr+TLiUOvB/I80lyZ3lSOp6cM18zmNRT/92NB4mW8oX2Jo7K4eVEI2JWyaQUAFubDSha2Q+439A==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "linux"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-win32-arm64-msvc": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-win32-arm64-msvc/-/core-win32-arm64-msvc-1.15.2.tgz",
      "integrity": "sha512-IzUb5RlMUY0r1A9IuJrQ7Tbts1wWb73/zXVXT8VhewbHGoNlBKE0qUhKMED6Tv4wDF+pmbtUJmKXDthytAvLmg==",
      "cpu": [
        "arm64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-win32-ia32-msvc": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-win32-ia32-msvc/-/core-win32-ia32-msvc-1.15.2.tgz",
      "integrity": "sha512-kCATEzuY2LP9AlbU2uScjcVhgnCAkRdu62vbce17Ro5kxEHxYWcugkveyBRS3AqZGtwAKYbMAuNloer9LS/hpw==",
      "cpu": [
        "ia32"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/core-win32-x64-msvc": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/@swc/core-win32-x64-msvc/-/core-win32-x64-msvc-1.15.2.tgz",
      "integrity": "sha512-iJaHeYCF4jTn7OEKSa3KRiuVFIVYts8jYjNmCdyz1u5g8HRyTDISD76r8+ljEOgm36oviRQvcXaw6LFp1m0yyA==",
      "cpu": [
        "x64"
      ],
      "dev": true,
      "license": "Apache-2.0 AND MIT",
      "optional": true,
      "os": [
        "win32"
      ],
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/@swc/counter": {
      "version": "0.1.3",
      "resolved": "https://registry.npmjs.org/@swc/counter/-/counter-0.1.3.tgz",
      "integrity": "sha512-e2BR4lsJkkRlKZ/qCHPw9ZaSxc0MVUd7gtbtaB7aMvHeJVYe8sOB8DBZkP2DtISHGSku9sCK6T6cnY0CtXrOCQ==",
      "dev": true,
      "license": "Apache-2.0"
    },
    "node_modules/@swc/types": {
      "version": "0.1.25",
      "resolved": "https://registry.npmjs.org/@swc/types/-/types-0.1.25.tgz",
      "integrity": "sha512-iAoY/qRhNH8a/hBvm3zKj9qQ4oc2+3w1unPJa2XvTK3XjeLXtzcCingVPw/9e5mn1+0yPqxcBGp9Jf0pkfMb1g==",
      "dev": true,
      "license": "Apache-2.0",
      "dependencies": {
        "@swc/counter": "^0.1.3"
      }
    },
    "node_modules/@types/body-parser": {
      "version": "1.19.6",
      "resolved": "https://registry.npmjs.org/@types/body-parser/-/body-parser-1.19.6.tgz",
      "integrity": "sha512-HLFeCYgz89uk22N5Qg3dvGvsv46B8GLvKKo1zKG4NybA8U2DiEO3w9lqGg29t/tfLRJpJ6iQxnVw4OnB7MoM9g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/connect": "*",
        "@types/node": "*"
      }
    },
    "node_modules/@types/connect": {
      "version": "3.4.38",
      "resolved": "https://registry.npmjs.org/@types/connect/-/connect-3.4.38.tgz",
      "integrity": "sha512-K6uROf1LD88uDQqJCktA4yzL1YYAK6NgfsI0v/mTgyPKWsX1CnJ0XPSDhViejru1GcRkLWb8RlzFYJRqGUbaug==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/cors": {
      "version": "2.8.19",
      "resolved": "https://registry.npmjs.org/@types/cors/-/cors-2.8.19.tgz",
      "integrity": "sha512-mFNylyeyqN93lfe/9CSxOGREz8cpzAhH+E93xJ4xWQf62V8sQ/24reV2nyzUWM6H6Xji+GGHpkbLe7pVoUEskg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/estree": {
      "version": "1.0.8",
      "resolved": "https://registry.npmjs.org/@types/estree/-/estree-1.0.8.tgz",
      "integrity": "sha512-dWHzHa2WqEXI/O1E9OjrocMTKJl2mSrEolh1Iomrv6U+JuNwaHXsXx9bLu5gG7BUWFIN0skIQJQ/L1rIex4X6w==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/express": {
      "version": "5.0.5",
      "resolved": "https://registry.npmjs.org/@types/express/-/express-5.0.5.tgz",
      "integrity": "sha512-LuIQOcb6UmnF7C1PCFmEU1u2hmiHL43fgFQX67sN3H4Z+0Yk0Neo++mFsBjhOAuLzvlQeqAAkeDOZrJs9rzumQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/body-parser": "*",
        "@types/express-serve-static-core": "^5.0.0",
        "@types/serve-static": "^1"
      }
    },
    "node_modules/@types/express-serve-static-core": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/@types/express-serve-static-core/-/express-serve-static-core-5.1.0.tgz",
      "integrity": "sha512-jnHMsrd0Mwa9Cf4IdOzbz543y4XJepXrbia2T4b6+spXC2We3t1y6K44D3mR8XMFSXMCf3/l7rCgddfx7UNVBA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*",
        "@types/qs": "*",
        "@types/range-parser": "*",
        "@types/send": "*"
      }
    },
    "node_modules/@types/http-errors": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/@types/http-errors/-/http-errors-2.0.5.tgz",
      "integrity": "sha512-r8Tayk8HJnX0FztbZN7oVqGccWgw98T/0neJphO91KkmOzug1KkofZURD4UaD5uH8AqcFLfdPErnBod0u71/qg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/mime": {
      "version": "1.3.5",
      "resolved": "https://registry.npmjs.org/@types/mime/-/mime-1.3.5.tgz",
      "integrity": "sha512-/pyBZWSLD2n0dcHE3hq8s8ZvcETHtEuF+3E7XVt0Ig2nvsVQXdghHVcEkIWjy9A0wKfTn97a/PSDYohKIlnP/w==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/minimatch": {
      "version": "3.0.5",
      "resolved": "https://registry.npmjs.org/@types/minimatch/-/minimatch-3.0.5.tgz",
      "integrity": "sha512-Klz949h02Gz2uZCMGwDUSDS1YBlTdDDgbWHi+81l29tQALUtvz4rAYi5uoVhE5Lagoq6DeqAUlbrHvW/mXDgdQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/multer": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/@types/multer/-/multer-2.0.0.tgz",
      "integrity": "sha512-C3Z9v9Evij2yST3RSBktxP9STm6OdMc5uR1xF1SGr98uv8dUlAL2hqwrZ3GVB3uyMyiegnscEK6PGtYvNrjTjw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/express": "*"
      }
    },
    "node_modules/@types/node": {
      "version": "24.10.1",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-24.10.1.tgz",
      "integrity": "sha512-GNWcUTRBgIRJD5zj+Tq0fKOJ5XZajIiBroOF0yvj2bSU1WvNdYS/dn9UxwsujGW4JX06dnHyjV2y9rRaybH0iQ==",
      "license": "MIT",
      "dependencies": {
        "undici-types": "~7.16.0"
      }
    },
    "node_modules/@types/papaparse": {
      "version": "5.5.0",
      "resolved": "https://registry.npmjs.org/@types/papaparse/-/papaparse-5.5.0.tgz",
      "integrity": "sha512-GVs5iMQmUr54BAZYYkByv8zPofFxmyxUpISPb2oh8sayR3+1zbxasrOvoKiHJ/nnoq/uULuPsu1Lze1EkagVFg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/phoenix": {
      "version": "1.6.6",
      "resolved": "https://registry.npmjs.org/@types/phoenix/-/phoenix-1.6.6.tgz",
      "integrity": "sha512-PIzZZlEppgrpoT2QgbnDU+MMzuR6BbCjllj0bM70lWoejMeNJAxCchxnv7J3XFkI8MpygtRpzXrIlmWUBclP5A==",
      "license": "MIT"
    },
    "node_modules/@types/prop-types": {
      "version": "15.7.15",
      "resolved": "https://registry.npmjs.org/@types/prop-types/-/prop-types-15.7.15.tgz",
      "integrity": "sha512-F6bEyamV9jKGAFBEmlQnesRPGOQqS2+Uwi0Em15xenOxHaf2hv6L8YCVn3rPdPJOiJfPiCnLIRyvwVaqMY3MIw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/qs": {
      "version": "6.14.0",
      "resolved": "https://registry.npmjs.org/@types/qs/-/qs-6.14.0.tgz",
      "integrity": "sha512-eOunJqu0K1923aExK6y8p6fsihYEn/BYuQ4g0CxAAgFc4b/ZLN4CrsRZ55srTdqoiLzU2B2evC+apEIxprEzkQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/range-parser": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/@types/range-parser/-/range-parser-1.2.7.tgz",
      "integrity": "sha512-hKormJbkJqzQGhziax5PItDUTMAM9uE2XXQmM37dyd4hVM+5aVl7oVxMVUiVQn2oCQFN/LKCZdvSM0pFRqbSmQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/react": {
      "version": "18.3.5",
      "resolved": "https://registry.npmjs.org/@types/react/-/react-18.3.5.tgz",
      "integrity": "sha512-WeqMfGJLGuLCqHGYRGHxnKrXcTitc6L/nBUWfWPcTarG3t9PsquqUMuVeXZeca+mglY4Vo5GZjCi0A3Or2lnxA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/prop-types": "*",
        "csstype": "^3.0.2"
      }
    },
    "node_modules/@types/react-dom": {
      "version": "18.3.0",
      "resolved": "https://registry.npmjs.org/@types/react-dom/-/react-dom-18.3.0.tgz",
      "integrity": "sha512-EhwApuTmMBmXuFOikhQLIBUn6uFg81SwLMOAUgodJF14SOBOCMdU04gDoYi0WOJJHD144TL32z4yDqCW3dnkQg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/react": "*"
      }
    },
    "node_modules/@types/send": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/@types/send/-/send-1.2.1.tgz",
      "integrity": "sha512-arsCikDvlU99zl1g69TcAB3mzZPpxgw0UQnaHeC1Nwb015xp8bknZv5rIfri9xTOcMuaVgvabfIRA7PSZVuZIQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/serve-static": {
      "version": "1.15.10",
      "resolved": "https://registry.npmjs.org/@types/serve-static/-/serve-static-1.15.10.tgz",
      "integrity": "sha512-tRs1dB+g8Itk72rlSI2ZrW6vZg0YrLI81iQSTkMmOqnqCaNr/8Ek4VwWcN5vZgCYWbg/JJSGBlUaYGAOP73qBw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/http-errors": "*",
        "@types/node": "*",
        "@types/send": "<1"
      }
    },
    "node_modules/@types/serve-static/node_modules/@types/send": {
      "version": "0.17.6",
      "resolved": "https://registry.npmjs.org/@types/send/-/send-0.17.6.tgz",
      "integrity": "sha512-Uqt8rPBE8SY0RK8JB1EzVOIZ32uqy8HwdxCnoCOsYrvnswqmFZ/k+9Ikidlk/ImhsdvBsloHbAlewb2IEBV/Og==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/mime": "^1",
        "@types/node": "*"
      }
    },
    "node_modules/@types/validator": {
      "version": "13.15.9",
      "resolved": "https://registry.npmjs.org/@types/validator/-/validator-13.15.9.tgz",
      "integrity": "sha512-9ENIuq9PUX45M1QRtfJDprgfErED4fBiMPmjlPci4W9WiBelVtHYCjF3xkQNcSnmUeuruLS1kH6hSl5M1vz4Sw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/@types/ws": {
      "version": "8.18.1",
      "resolved": "https://registry.npmjs.org/@types/ws/-/ws-8.18.1.tgz",
      "integrity": "sha512-ThVF6DCVhA8kUGy+aazFQ4kXQ7E1Ty7A3ypFOe0IcJV8O/M511G99AW24irKrW56Wt44yG9+ij8FaqoBGkuBXg==",
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@typescript-eslint/eslint-plugin": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/eslint-plugin/-/eslint-plugin-8.3.0.tgz",
      "integrity": "sha512-FLAIn63G5KH+adZosDYiutqkOkYEx0nvcwNNfJAf+c7Ae/H35qWwTYvPZUKFj5AS+WfHG/WJJfWnDnyNUlp8UA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@eslint-community/regexpp": "^4.10.0",
        "@typescript-eslint/scope-manager": "8.3.0",
        "@typescript-eslint/type-utils": "8.3.0",
        "@typescript-eslint/utils": "8.3.0",
        "@typescript-eslint/visitor-keys": "8.3.0",
        "graphemer": "^1.4.0",
        "ignore": "^5.3.1",
        "natural-compare": "^1.4.0",
        "ts-api-utils": "^1.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependencies": {
        "@typescript-eslint/parser": "^8.0.0 || ^8.0.0-alpha.0",
        "eslint": "^8.57.0 || ^9.0.0"
      },
      "peerDependenciesMeta": {
        "typescript": {
          "optional": true
        }
      }
    },
    "node_modules/@typescript-eslint/parser": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/parser/-/parser-8.3.0.tgz",
      "integrity": "sha512-h53RhVyLu6AtpUzVCYLPhZGL5jzTD9fZL+SYf/+hYOx2bDkyQXztXSc4tbvKYHzfMXExMLiL9CWqJmVz6+78IQ==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "@typescript-eslint/scope-manager": "8.3.0",
        "@typescript-eslint/types": "8.3.0",
        "@typescript-eslint/typescript-estree": "8.3.0",
        "@typescript-eslint/visitor-keys": "8.3.0",
        "debug": "^4.3.4"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependencies": {
        "eslint": "^8.57.0 || ^9.0.0"
      },
      "peerDependenciesMeta": {
        "typescript": {
          "optional": true
        }
      }
    },
    "node_modules/@typescript-eslint/scope-manager": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/scope-manager/-/scope-manager-8.3.0.tgz",
      "integrity": "sha512-mz2X8WcN2nVu5Hodku+IR8GgCOl4C0G/Z1ruaWN4dgec64kDBabuXyPAr+/RgJtumv8EEkqIzf3X2U5DUKB2eg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@typescript-eslint/types": "8.3.0",
        "@typescript-eslint/visitor-keys": "8.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      }
    },
    "node_modules/@typescript-eslint/type-utils": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/type-utils/-/type-utils-8.3.0.tgz",
      "integrity": "sha512-wrV6qh//nLbfXZQoj32EXKmwHf4b7L+xXLrP3FZ0GOUU72gSvLjeWUl5J5Ue5IwRxIV1TfF73j/eaBapxx99Lg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@typescript-eslint/typescript-estree": "8.3.0",
        "@typescript-eslint/utils": "8.3.0",
        "debug": "^4.3.4",
        "ts-api-utils": "^1.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependenciesMeta": {
        "typescript": {
          "optional": true
        }
      }
    },
    "node_modules/@typescript-eslint/types": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/types/-/types-8.3.0.tgz",
      "integrity": "sha512-y6sSEeK+facMaAyixM36dQ5NVXTnKWunfD1Ft4xraYqxP0lC0POJmIaL/mw72CUMqjY9qfyVfXafMeaUj0noWw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      }
    },
    "node_modules/@typescript-eslint/typescript-estree": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/typescript-estree/-/typescript-estree-8.3.0.tgz",
      "integrity": "sha512-Mq7FTHl0R36EmWlCJWojIC1qn/ZWo2YiWYc1XVtasJ7FIgjo0MVv9rZWXEE7IK2CGrtwe1dVOxWwqXUdNgfRCA==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "@typescript-eslint/types": "8.3.0",
        "@typescript-eslint/visitor-keys": "8.3.0",
        "debug": "^4.3.4",
        "fast-glob": "^3.3.2",
        "is-glob": "^4.0.3",
        "minimatch": "^9.0.4",
        "semver": "^7.6.0",
        "ts-api-utils": "^1.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependenciesMeta": {
        "typescript": {
          "optional": true
        }
      }
    },
    "node_modules/@typescript-eslint/typescript-estree/node_modules/brace-expansion": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-2.0.2.tgz",
      "integrity": "sha512-Jt0vHyM+jmUBqojB7E1NIYadt0vI0Qxjxd2TErW94wDz+E2LAm5vKMXXwg6ZZBTHPuUlDgQHKXvjGBdfcF1ZDQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "balanced-match": "^1.0.0"
      }
    },
    "node_modules/@typescript-eslint/typescript-estree/node_modules/minimatch": {
      "version": "9.0.5",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-9.0.5.tgz",
      "integrity": "sha512-G6T0ZX48xgozx7587koeX9Ys2NYy6Gmv//P89sEte9V9whIapMNF4idKxnW2QtCcLiTWlb/wfCabAtAFWhhBow==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "brace-expansion": "^2.0.1"
      },
      "engines": {
        "node": ">=16 || 14 >=14.17"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/@typescript-eslint/utils": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/utils/-/utils-8.3.0.tgz",
      "integrity": "sha512-F77WwqxIi/qGkIGOGXNBLV7nykwfjLsdauRB/DOFPdv6LTF3BHHkBpq81/b5iMPSF055oO2BiivDJV4ChvNtXA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@eslint-community/eslint-utils": "^4.4.0",
        "@typescript-eslint/scope-manager": "8.3.0",
        "@typescript-eslint/types": "8.3.0",
        "@typescript-eslint/typescript-estree": "8.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependencies": {
        "eslint": "^8.57.0 || ^9.0.0"
      }
    },
    "node_modules/@typescript-eslint/visitor-keys": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/@typescript-eslint/visitor-keys/-/visitor-keys-8.3.0.tgz",
      "integrity": "sha512-RmZwrTbQ9QveF15m/Cl28n0LXD6ea2CjkhH5rQ55ewz3H24w+AMCJHPVYaZ8/0HoG8Z3cLLFFycRXxeO2tz9FA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@typescript-eslint/types": "8.3.0",
        "eslint-visitor-keys": "^3.4.3"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      }
    },
    "node_modules/@typescript-eslint/visitor-keys/node_modules/eslint-visitor-keys": {
      "version": "3.4.3",
      "resolved": "https://registry.npmjs.org/eslint-visitor-keys/-/eslint-visitor-keys-3.4.3.tgz",
      "integrity": "sha512-wpc+LXeiyiisxPlEkUzU6svyS1frIO3Mgxj1fdy7Pm8Ygzguax2N3Fa/D/ag1WqbOprdI+uY6wMUl8/a2G+iag==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": "^12.22.0 || ^14.17.0 || >=16.0.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/@vitejs/plugin-react-swc": {
      "version": "3.11.0",
      "resolved": "https://registry.npmjs.org/@vitejs/plugin-react-swc/-/plugin-react-swc-3.11.0.tgz",
      "integrity": "sha512-YTJCGFdNMHCMfjODYtxRNVAYmTWQ1Lb8PulP/2/f/oEEtglw8oKxKIZmmRkyXrVrHfsKOaVkAc3NT9/dMutO5w==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@rolldown/pluginutils": "1.0.0-beta.27",
        "@swc/core": "^1.12.11"
      },
      "peerDependencies": {
        "vite": "^4 || ^5 || ^6 || ^7"
      }
    },
    "node_modules/accepts": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/accepts/-/accepts-2.0.0.tgz",
      "integrity": "sha512-5cvg6CtKwfgdmVqY1WIiXKc3Q1bkRqGLi+2W/6ao+6Y7gu/RCwRuAhGEzh5B4KlszSuTLgZYuqFqo5bImjNKng==",
      "license": "MIT",
      "dependencies": {
        "mime-types": "^3.0.0",
        "negotiator": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/acorn": {
      "version": "8.15.0",
      "resolved": "https://registry.npmjs.org/acorn/-/acorn-8.15.0.tgz",
      "integrity": "sha512-NZyJarBfL7nWwIq+FDL6Zp/yHEhePMNnnJ0y3qfieCrmNvYct8uvtiV41UvlSe6apAfk0fY1FbWx+NwfmpvtTg==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "acorn": "bin/acorn"
      },
      "engines": {
        "node": ">=0.4.0"
      }
    },
    "node_modules/acorn-jsx": {
      "version": "5.3.2",
      "resolved": "https://registry.npmjs.org/acorn-jsx/-/acorn-jsx-5.3.2.tgz",
      "integrity": "sha512-rq9s+JNhf0IChjtDXxllJ7g41oZk5SlXtp0LHwyA5cejwn7vKmKp4pPri6YEePv2PU65sAsegbXtIinmDFDXgQ==",
      "dev": true,
      "license": "MIT",
      "peerDependencies": {
        "acorn": "^6.0.0 || ^7.0.0 || ^8.0.0"
      }
    },
    "node_modules/ajv": {
      "version": "6.12.6",
      "resolved": "https://registry.npmjs.org/ajv/-/ajv-6.12.6.tgz",
      "integrity": "sha512-j3fVLgvTo527anyYyJOGTYJbG+vnnQYvE0m5mmkc1TK+nxAppkCLMIL0aZ4dblVCNoGShhm+kzE4ZUykBoMg4g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "fast-deep-equal": "^3.1.1",
        "fast-json-stable-stringify": "^2.0.0",
        "json-schema-traverse": "^0.4.1",
        "uri-js": "^4.2.2"
      },
      "funding": {
        "type": "github",
        "url": "https://github.com/sponsors/epoberezkin"
      }
    },
    "node_modules/ansi-regex": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-5.0.1.tgz",
      "integrity": "sha512-quJQXlTSUGL2LH9SUXo8VwsY4soanhgo6LNSm84E1LBcE8s3O0wpdiRzyR9z/ZZJMlMWv37qOOb9pdJlMUEKFQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/ansi-styles": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-4.3.0.tgz",
      "integrity": "sha512-zbB9rCJAT1rbjiVDb2hqKFHNYLxgtk8NURxZ3IZwD3F6NtxbXZQCnnSi1Lkx+IDohdPlFp222wVALIheZJQSEg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "color-convert": "^2.0.1"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-styles?sponsor=1"
      }
    },
    "node_modules/any-promise": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/any-promise/-/any-promise-1.3.0.tgz",
      "integrity": "sha512-7UvmKalWRt1wgjL1RrGxoSJW/0QZFIegpeGvZG9kjp8vrRu55XTHbwnqq2GpXm9uLbcuhxm3IqX9OB4MZR1b2A==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/anymatch": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/anymatch/-/anymatch-3.1.3.tgz",
      "integrity": "sha512-KMReFUr0B4t+D+OBkjR3KYqvocp2XaSzO55UcB6mgQMd3KbcE+mWTyvVV7D/zsdEbNnV6acZUutkiHQXvTr1Rw==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "normalize-path": "^3.0.0",
        "picomatch": "^2.0.4"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/append-field": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/append-field/-/append-field-1.0.0.tgz",
      "integrity": "sha512-klpgFSWLW1ZEs8svjfb7g4qWY0YS5imI82dTg+QahUvJ8YqAY0P10Uk8tTyh9ZGuYEZEMaeJYCF5BFuX552hsw==",
      "license": "MIT"
    },
    "node_modules/archiver": {
      "version": "5.3.2",
      "resolved": "https://registry.npmjs.org/archiver/-/archiver-5.3.2.tgz",
      "integrity": "sha512-+25nxyyznAXF7Nef3y0EbBeqmGZgeN/BxHX29Rs39djAfaFalmQ89SE6CWyDCHzGL0yt/ycBtNOmGTW0FyGWNw==",
      "license": "MIT",
      "dependencies": {
        "archiver-utils": "^2.1.0",
        "async": "^3.2.4",
        "buffer-crc32": "^0.2.1",
        "readable-stream": "^3.6.0",
        "readdir-glob": "^1.1.2",
        "tar-stream": "^2.2.0",
        "zip-stream": "^4.1.0"
      },
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/archiver-utils": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/archiver-utils/-/archiver-utils-2.1.0.tgz",
      "integrity": "sha512-bEL/yUb/fNNiNTuUz979Z0Yg5L+LzLxGJz8x79lYmR54fmTIb6ob/hNQgkQnIUDWIFjZVQwl9Xs356I6BAMHfw==",
      "license": "MIT",
      "dependencies": {
        "glob": "^7.1.4",
        "graceful-fs": "^4.2.0",
        "lazystream": "^1.0.0",
        "lodash.defaults": "^4.2.0",
        "lodash.difference": "^4.5.0",
        "lodash.flatten": "^4.4.0",
        "lodash.isplainobject": "^4.0.6",
        "lodash.union": "^4.6.0",
        "normalize-path": "^3.0.0",
        "readable-stream": "^2.0.0"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/archiver-utils/node_modules/readable-stream": {
      "version": "2.3.8",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.3.8.tgz",
      "integrity": "sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==",
      "license": "MIT",
      "dependencies": {
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.3",
        "isarray": "~1.0.0",
        "process-nextick-args": "~2.0.0",
        "safe-buffer": "~5.1.1",
        "string_decoder": "~1.1.1",
        "util-deprecate": "~1.0.1"
      }
    },
    "node_modules/archiver-utils/node_modules/safe-buffer": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.1.2.tgz",
      "integrity": "sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==",
      "license": "MIT"
    },
    "node_modules/archiver-utils/node_modules/string_decoder": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.1.1.tgz",
      "integrity": "sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.1.0"
      }
    },
    "node_modules/arg": {
      "version": "5.0.2",
      "resolved": "https://registry.npmjs.org/arg/-/arg-5.0.2.tgz",
      "integrity": "sha512-PYjyFOLKQ9y57JvQ6QLo8dAgNqswh8M1RMJYdQduT6xbWSgK36P/Z/v+p888pM69jMMfS8Xd8F6I1kQ/I9HUGg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/argparse": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/argparse/-/argparse-2.0.1.tgz",
      "integrity": "sha512-8+9WqebbFzpX9OR+Wa6O29asIogeRMzcGtAINdpMHHyAg10f05aSFVBbcEqGf/PXw1EjAZ+q2/bEBg3DvurK3Q==",
      "dev": true,
      "license": "Python-2.0"
    },
    "node_modules/array-differ": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/array-differ/-/array-differ-3.0.0.tgz",
      "integrity": "sha512-THtfYS6KtME/yIAhKjZ2ul7XI96lQGHRputJQHO80LAWQnuGP4iCIN8vdMRboGbIEYBwU33q8Tch1os2+X0kMg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/array-union": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/array-union/-/array-union-2.1.0.tgz",
      "integrity": "sha512-HGyxoOTYUyCM6stUe6EJgnd4EoewAI7zMdfqO+kGjnlZmBDz/cR5pf8r/cR4Wq60sL/p0IkcjUEEPwS3GFrIyw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/arrify": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/arrify/-/arrify-2.0.1.tgz",
      "integrity": "sha512-3duEwti880xqi4eAMN8AyR4a0ByT90zoYdLlevfrvU43vb0YZwZVfxOgxWrLXXXpyugL0hNZc9G6BiB5B3nUug==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/assert": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/assert/-/assert-2.0.0.tgz",
      "integrity": "sha512-se5Cd+js9dXJnu6Ag2JFc00t+HmHOen+8Q+L7O9zI0PqQXr20uk2J0XQqMxZEeo5U50o8Nvmmx7dZrl+Ufr35A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "es6-object-assign": "^1.1.0",
        "is-nan": "^1.2.1",
        "object-is": "^1.0.1",
        "util": "^0.12.0"
      }
    },
    "node_modules/async": {
      "version": "3.2.6",
      "resolved": "https://registry.npmjs.org/async/-/async-3.2.6.tgz",
      "integrity": "sha512-htCUDlxyyCLMgaM3xXg0C0LW2xqfuQ6p05pCEIsXuyQ+a1koYKTuBMzRNwmybfLgvJDMd0r1LTn4+E0Ti6C2AA==",
      "license": "MIT"
    },
    "node_modules/autoprefixer": {
      "version": "10.4.21",
      "resolved": "https://registry.npmjs.org/autoprefixer/-/autoprefixer-10.4.21.tgz",
      "integrity": "sha512-O+A6LWV5LDHSJD3LjHYoNi4VLsj/Whi7k6zG12xTYaU4cQ8oxQGckXNX8cRHK5yOZ/ppVHe0ZBXGzSV9jXdVbQ==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/autoprefixer"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "browserslist": "^4.24.4",
        "caniuse-lite": "^1.0.30001702",
        "fraction.js": "^4.3.7",
        "normalize-range": "^0.1.2",
        "picocolors": "^1.1.1",
        "postcss-value-parser": "^4.2.0"
      },
      "bin": {
        "autoprefixer": "bin/autoprefixer"
      },
      "engines": {
        "node": "^10 || ^12 || >=14"
      },
      "peerDependencies": {
        "postcss": "^8.1.0"
      }
    },
    "node_modules/available-typed-arrays": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/available-typed-arrays/-/available-typed-arrays-1.0.7.tgz",
      "integrity": "sha512-wvUjBtSGN7+7SjNpq/9M2Tg350UZD3q62IFZLbRAR1bSMlCo1ZaeW+BJ+D090e4hIIZLBcTDWe4Mh4jvUDajzQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "possible-typed-array-names": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/balanced-match": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/balanced-match/-/balanced-match-1.0.2.tgz",
      "integrity": "sha512-3oSeUO0TMV67hN1AmbXsK4yaqU7tjiHlbxRDZOpH0KW9+CeX4bRAaX0Anxt0tx2MrpRpWwQaPwIlISEJhYU5Pw==",
      "license": "MIT"
    },
    "node_modules/base64-js": {
      "version": "1.5.1",
      "resolved": "https://registry.npmjs.org/base64-js/-/base64-js-1.5.1.tgz",
      "integrity": "sha512-AKpaYlHn8t4SVbOHCy+b5+KKgvR4vrsD8vbvrbiQJps7fKDTkjkDry6ji0rUJjC0kzbNePLwzxq8iypo41qeWA==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT"
    },
    "node_modules/baseline-browser-mapping": {
      "version": "2.8.28",
      "resolved": "https://registry.npmjs.org/baseline-browser-mapping/-/baseline-browser-mapping-2.8.28.tgz",
      "integrity": "sha512-gYjt7OIqdM0PcttNYP2aVrr2G0bMALkBaoehD4BuRGjAOtipg0b6wHg1yNL+s5zSnLZZrGHOw4IrND8CD+3oIQ==",
      "dev": true,
      "license": "Apache-2.0",
      "bin": {
        "baseline-browser-mapping": "dist/cli.js"
      }
    },
    "node_modules/bcryptjs": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/bcryptjs/-/bcryptjs-3.0.3.tgz",
      "integrity": "sha512-GlF5wPWnSa/X5LKM1o0wz0suXIINz1iHRLvTS+sLyi7XPbe5ycmYI3DlZqVGZZtDgl4DmasFg7gOB3JYbphV5g==",
      "license": "BSD-3-Clause",
      "bin": {
        "bcrypt": "bin/bcrypt"
      }
    },
    "node_modules/big-integer": {
      "version": "1.6.52",
      "resolved": "https://registry.npmjs.org/big-integer/-/big-integer-1.6.52.tgz",
      "integrity": "sha512-QxD8cf2eVqJOOz63z6JIN9BzvVs/dlySa5HGSBH5xtR8dPteIRQnBxxKqkNTiT6jbDTF6jAfrd4oMcND9RGbQg==",
      "license": "Unlicense",
      "engines": {
        "node": ">=0.6"
      }
    },
    "node_modules/binary": {
      "version": "0.3.0",
      "resolved": "https://registry.npmjs.org/binary/-/binary-0.3.0.tgz",
      "integrity": "sha512-D4H1y5KYwpJgK8wk1Cue5LLPgmwHKYSChkbspQg5JtVuR5ulGckxfR62H3AE9UDkdMC8yyXlqYihuz3Aqg2XZg==",
      "license": "MIT",
      "dependencies": {
        "buffers": "~0.1.1",
        "chainsaw": "~0.1.0"
      },
      "engines": {
        "node": "*"
      }
    },
    "node_modules/binary-extensions": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/binary-extensions/-/binary-extensions-2.3.0.tgz",
      "integrity": "sha512-Ceh+7ox5qe7LJuLHoY0feh3pHuUDHAcRUeyL2VYghZwfpkNIy/+8Ocg0a3UuSoYzavmylwuLWQOf3hl0jjMMIw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/bl": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/bl/-/bl-4.1.0.tgz",
      "integrity": "sha512-1W07cM9gS6DcLperZfFSj+bWLtaPGSOHWhPiGzXmvVJbRLdG82sH/Kn8EtW1VqWVA54AKf2h5k5BbnIbwF3h6w==",
      "license": "MIT",
      "dependencies": {
        "buffer": "^5.5.0",
        "inherits": "^2.0.4",
        "readable-stream": "^3.4.0"
      }
    },
    "node_modules/bluebird": {
      "version": "3.4.7",
      "resolved": "https://registry.npmjs.org/bluebird/-/bluebird-3.4.7.tgz",
      "integrity": "sha512-iD3898SR7sWVRHbiQv+sHUtHnMvC1o3nW5rAcqnq3uOn07DSAppZYUkIGslDz6gXC7HfunPe7YVBgoEJASPcHA==",
      "license": "MIT"
    },
    "node_modules/body-parser": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/body-parser/-/body-parser-2.2.0.tgz",
      "integrity": "sha512-02qvAaxv8tp7fBa/mw1ga98OGm+eCbqzJOKoRt70sLmfEEi+jyBYVTDGfCL/k06/4EMk/z01gCe7HoCH/f2LTg==",
      "license": "MIT",
      "dependencies": {
        "bytes": "^3.1.2",
        "content-type": "^1.0.5",
        "debug": "^4.4.0",
        "http-errors": "^2.0.0",
        "iconv-lite": "^0.6.3",
        "on-finished": "^2.4.1",
        "qs": "^6.14.0",
        "raw-body": "^3.0.0",
        "type-is": "^2.0.0"
      },
      "engines": {
        "node": ">=18"
      }
    },
    "node_modules/brace-expansion": {
      "version": "1.1.12",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-1.1.12.tgz",
      "integrity": "sha512-9T9UjW3r0UW5c1Q7GTwllptXwhvYmEzFhzMfZ9H7FQWt+uZePjZPjBP/W1ZEyZ1twGWom5/56TF4lPcqjnDHcg==",
      "license": "MIT",
      "dependencies": {
        "balanced-match": "^1.0.0",
        "concat-map": "0.0.1"
      }
    },
    "node_modules/braces": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/braces/-/braces-3.0.3.tgz",
      "integrity": "sha512-yQbXgO/OSZVD2IsiLlro+7Hf6Q18EJrKSEsdoMzKePKXct3gvD8oLcOQdIzGupr5Fj+EDe8gO/lxc1BzfMpxvA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "fill-range": "^7.1.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/browserslist": {
      "version": "4.28.0",
      "resolved": "https://registry.npmjs.org/browserslist/-/browserslist-4.28.0.tgz",
      "integrity": "sha512-tbydkR/CxfMwelN0vwdP/pLkDwyAASZ+VfWm4EOwlB6SWhx1sYnWLqo8N5j0rAzPfzfRaxt0mM/4wPU/Su84RQ==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/browserslist"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "baseline-browser-mapping": "^2.8.25",
        "caniuse-lite": "^1.0.30001754",
        "electron-to-chromium": "^1.5.249",
        "node-releases": "^2.0.27",
        "update-browserslist-db": "^1.1.4"
      },
      "bin": {
        "browserslist": "cli.js"
      },
      "engines": {
        "node": "^6 || ^7 || ^8 || ^9 || ^10 || ^11 || ^12 || >=13.7"
      }
    },
    "node_modules/buffer": {
      "version": "5.7.1",
      "resolved": "https://registry.npmjs.org/buffer/-/buffer-5.7.1.tgz",
      "integrity": "sha512-EHcyIPBQ4BSGlvjB16k5KgAJ27CIsHY/2JBmCRReo48y9rQ3MaUzWX3KVlBa4U7MyX02HdVj0K7C3WaB3ju7FQ==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "base64-js": "^1.3.1",
        "ieee754": "^1.1.13"
      }
    },
    "node_modules/buffer-crc32": {
      "version": "0.2.13",
      "resolved": "https://registry.npmjs.org/buffer-crc32/-/buffer-crc32-0.2.13.tgz",
      "integrity": "sha512-VO9Ht/+p3SN7SKWqcrgEzjGbRSJYTx+Q1pTQC0wrWqHx0vpJraQ6GtHx8tvcg1rlK1byhU5gccxgOgj7B0TDkQ==",
      "license": "MIT",
      "engines": {
        "node": "*"
      }
    },
    "node_modules/buffer-from": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/buffer-from/-/buffer-from-1.1.2.tgz",
      "integrity": "sha512-E+XQCRwSbaaiChtv6k6Dwgc+bx+Bs6vuKJHHl5kox/BaKbhiXzqQOwK4cO22yElGp2OCmjwVhT3HmxgyPGnJfQ==",
      "license": "MIT"
    },
    "node_modules/buffer-indexof-polyfill": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/buffer-indexof-polyfill/-/buffer-indexof-polyfill-1.0.2.tgz",
      "integrity": "sha512-I7wzHwA3t1/lwXQh+A5PbNvJxgfo5r3xulgpYDB5zckTu/Z9oUK9biouBKQUjEqzaz3HnAT6TYoovmE+GqSf7A==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10"
      }
    },
    "node_modules/buffers": {
      "version": "0.1.1",
      "resolved": "https://registry.npmjs.org/buffers/-/buffers-0.1.1.tgz",
      "integrity": "sha512-9q/rDEGSb/Qsvv2qvzIzdluL5k7AaJOTrw23z9reQthrbF7is4CtlT0DXyO1oei2DCp4uojjzQ7igaSHp1kAEQ==",
      "engines": {
        "node": ">=0.2.0"
      }
    },
    "node_modules/busboy": {
      "version": "1.6.0",
      "resolved": "https://registry.npmjs.org/busboy/-/busboy-1.6.0.tgz",
      "integrity": "sha512-8SFQbg/0hQ9xy3UNTB0YEnsNBbWfhf7RtnzpL7TkBiTBRfrQ9Fxcnz7VJsleJpyp6rVLvXiuORqjlHi5q+PYuA==",
      "dependencies": {
        "streamsearch": "^1.1.0"
      },
      "engines": {
        "node": ">=10.16.0"
      }
    },
    "node_modules/bytes": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/bytes/-/bytes-3.1.2.tgz",
      "integrity": "sha512-/Nf7TyzTx6S3yRJObOAV7956r8cr2+Oj8AC5dt8wSP3BQAoeX58NoHyCU8P8zGkNXStjTSi6fzO6F0pBdcYbEg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/call-bind": {
      "version": "1.0.8",
      "resolved": "https://registry.npmjs.org/call-bind/-/call-bind-1.0.8.tgz",
      "integrity": "sha512-oKlSFMcMwpUg2ednkhQ454wfWiU/ul3CkJe/PEHcTKuiX6RpbehUiFMXu13HalGZxfUwCQzZG747YXBn1im9ww==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bind-apply-helpers": "^1.0.0",
        "es-define-property": "^1.0.0",
        "get-intrinsic": "^1.2.4",
        "set-function-length": "^1.2.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/call-bind-apply-helpers": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/call-bind-apply-helpers/-/call-bind-apply-helpers-1.0.2.tgz",
      "integrity": "sha512-Sp1ablJ0ivDkSzjcaJdxEunN5/XvksFJ2sMBFfq6x0ryhQV/2b/KwFe21cMpmHtPOSij8K99/wSfoEuTObmuMQ==",
      "license": "MIT",
      "dependencies": {
        "es-errors": "^1.3.0",
        "function-bind": "^1.1.2"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/call-bound": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/call-bound/-/call-bound-1.0.4.tgz",
      "integrity": "sha512-+ys997U96po4Kx/ABpBCqhA9EuxJaQWDQg7295H4hBphv3IZg0boBKuwYpt4YXp6MZ5AmZQnU/tyMTlRpaSejg==",
      "license": "MIT",
      "dependencies": {
        "call-bind-apply-helpers": "^1.0.2",
        "get-intrinsic": "^1.3.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/callsites": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/callsites/-/callsites-3.1.0.tgz",
      "integrity": "sha512-P8BjAsXvZS+VIDUI11hHCQEv74YT67YUi5JJFNWIqL235sBmjX4+qx9Muvls5ivyNENctx46xQLQ3aTuE7ssaQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/camelcase-css": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/camelcase-css/-/camelcase-css-2.0.1.tgz",
      "integrity": "sha512-QOSvevhslijgYwRx6Rv7zKdMF8lbRmx+uQGx2+vDc+KI/eBnsy9kit5aj23AgGu3pa4t9AgwbnXWqS+iOY+2aA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/caniuse-lite": {
      "version": "1.0.30001755",
      "resolved": "https://registry.npmjs.org/caniuse-lite/-/caniuse-lite-1.0.30001755.tgz",
      "integrity": "sha512-44V+Jm6ctPj7R52Na4TLi3Zri4dWUljJd+RDm+j8LtNCc/ihLCT+X1TzoOAkRETEWqjuLnh9581Tl80FvK7jVA==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/caniuse-lite"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "CC-BY-4.0"
    },
    "node_modules/chainsaw": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/chainsaw/-/chainsaw-0.1.0.tgz",
      "integrity": "sha512-75kWfWt6MEKNC8xYXIdRpDehRYY/tNSgwKaJq+dbbDcxORuVrrQ+SEHoWsniVn9XPYfP4gmdWIeDk/4YNp1rNQ==",
      "license": "MIT/X11",
      "dependencies": {
        "traverse": ">=0.3.0 <0.4"
      },
      "engines": {
        "node": "*"
      }
    },
    "node_modules/chalk": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-4.1.2.tgz",
      "integrity": "sha512-oKnbhFyRIXpUuez8iBMmyEa4nbj4IOQyuhc/wy9kY7/WVPcwIO9VA668Pu8RkO7+0G76SLROeyw9CpQ061i4mA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^4.1.0",
        "supports-color": "^7.1.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/chalk?sponsor=1"
      }
    },
    "node_modules/chance": {
      "version": "1.1.9",
      "resolved": "https://registry.npmjs.org/chance/-/chance-1.1.9.tgz",
      "integrity": "sha512-TfxnA/DcZXRTA4OekA2zL9GH8qscbbl6X0ZqU4tXhGveVY/mXWvEQLt5GwZcYXTEyEFflVtj+pG8nc8EwSm1RQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/char-regex": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/char-regex/-/char-regex-1.0.2.tgz",
      "integrity": "sha512-kWWXztvZ5SBQV+eRgKFeh8q5sLuZY2+8WUIzlxWVTg+oGwY14qylx1KbKzHd8P6ZYkAg0xyIDU9JMHhyJMZ1jw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/charenc": {
      "version": "0.0.2",
      "resolved": "https://registry.npmjs.org/charenc/-/charenc-0.0.2.tgz",
      "integrity": "sha512-yrLQ/yVUFXkzg7EDQsPieE/53+0RlaWTs+wBrvW36cyilJ2SaDWfl4Yj7MtLTXleV9uEKefbAGUPv2/iWSooRA==",
      "dev": true,
      "license": "BSD-3-Clause",
      "engines": {
        "node": "*"
      }
    },
    "node_modules/chokidar": {
      "version": "3.6.0",
      "resolved": "https://registry.npmjs.org/chokidar/-/chokidar-3.6.0.tgz",
      "integrity": "sha512-7VT13fmjotKpGipCW9JEQAusEPE+Ei8nl6/g4FBAmIm0GOOLMua9NDDo/DWp0ZAxCr3cPq5ZpBqmPAQgDda2Pw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "anymatch": "~3.1.2",
        "braces": "~3.0.2",
        "glob-parent": "~5.1.2",
        "is-binary-path": "~2.1.0",
        "is-glob": "~4.0.1",
        "normalize-path": "~3.0.0",
        "readdirp": "~3.6.0"
      },
      "engines": {
        "node": ">= 8.10.0"
      },
      "funding": {
        "url": "https://paulmillr.com/funding/"
      },
      "optionalDependencies": {
        "fsevents": "~2.3.2"
      }
    },
    "node_modules/chokidar/node_modules/glob-parent": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/glob-parent/-/glob-parent-5.1.2.tgz",
      "integrity": "sha512-AOIgSQCepiJYwP3ARnGx+5VnTu2HBYdzbGP45eLw1vr3zB3vZLeyed1sC9hnbcOc9/SrMyM5RPQrkGz4aS9Zow==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "is-glob": "^4.0.1"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/class-validator": {
      "version": "0.14.1",
      "resolved": "https://registry.npmjs.org/class-validator/-/class-validator-0.14.1.tgz",
      "integrity": "sha512-2VEG9JICxIqTpoK1eMzZqaV+u/EiwEJkMGzTrZf6sU/fwsnOITVgYJ8yojSy6CaXtO9V0Cc6ZQZ8h8m4UBuLwQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/validator": "^13.11.8",
        "libphonenumber-js": "^1.10.53",
        "validator": "^13.9.0"
      }
    },
    "node_modules/color-convert": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-2.0.1.tgz",
      "integrity": "sha512-RRECPsj7iu/xb5oKYcsFHSppFNnsj/52OVTRKb4zP5onXwVF3zVmmToNcOfGC+CRDpfK/U584fMg38ZHCaElKQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "color-name": "~1.1.4"
      },
      "engines": {
        "node": ">=7.0.0"
      }
    },
    "node_modules/color-name": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.4.tgz",
      "integrity": "sha512-dOy+3AuW3a2wNbZHIuMZpTcgjGuLU/uBL/ubcZF9OXbDo8ff4O8yVp5Bf0efS8uEoYo5q4Fx7dY9OgQGXgAsQA==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/commander": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/commander/-/commander-4.1.1.tgz",
      "integrity": "sha512-NOKm8xhkzAjzFx8B2v5OAHT+u5pRQc2UCa2Vq9jYL/31o2wi9mxBA7LIFs3sV5VSC49z6pEhfbMULvShKj26WA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/compress-commons": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/compress-commons/-/compress-commons-4.1.2.tgz",
      "integrity": "sha512-D3uMHtGc/fcO1Gt1/L7i1e33VOvD4A9hfQLP+6ewd+BvG/gQ84Yh4oftEhAdjSMgBgwGL+jsppT7JYNpo6MHHg==",
      "license": "MIT",
      "dependencies": {
        "buffer-crc32": "^0.2.13",
        "crc32-stream": "^4.0.2",
        "normalize-path": "^3.0.0",
        "readable-stream": "^3.6.0"
      },
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/concat-map": {
      "version": "0.0.1",
      "resolved": "https://registry.npmjs.org/concat-map/-/concat-map-0.0.1.tgz",
      "integrity": "sha512-/Srv4dswyQNBfohGpz9o6Yb3Gz3SrUDqBH5rTuhGR7ahtlbYKnVxw2bCFMRljaA7EXHaXZ8wsHdodFvbkhKmqg==",
      "license": "MIT"
    },
    "node_modules/concat-stream": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/concat-stream/-/concat-stream-2.0.0.tgz",
      "integrity": "sha512-MWufYdFw53ccGjCA+Ol7XJYpAlW6/prSMzuPOTRnJGcGzuhLn4Scrz7qf6o8bROZ514ltazcIFJZevcfbo0x7A==",
      "engines": [
        "node >= 6.0"
      ],
      "license": "MIT",
      "dependencies": {
        "buffer-from": "^1.0.0",
        "inherits": "^2.0.3",
        "readable-stream": "^3.0.2",
        "typedarray": "^0.0.6"
      }
    },
    "node_modules/content-disposition": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/content-disposition/-/content-disposition-1.0.1.tgz",
      "integrity": "sha512-oIXISMynqSqm241k6kcQ5UwttDILMK4BiurCfGEREw6+X9jkkpEe5T9FZaApyLGGOnFuyMWZpdolTXMtvEJ08Q==",
      "license": "MIT",
      "engines": {
        "node": ">=18"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/express"
      }
    },
    "node_modules/content-type": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/content-type/-/content-type-1.0.5.tgz",
      "integrity": "sha512-nTjqfcBFEipKdXCv4YDQWCfmcLZKm81ldF0pAopTvyrFGVbcR6P/VAAd5G7N+0tTr8QqiU0tFadD6FK4NtJwOA==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/cookie": {
      "version": "0.7.2",
      "resolved": "https://registry.npmjs.org/cookie/-/cookie-0.7.2.tgz",
      "integrity": "sha512-yki5XnKuf750l50uGTllt6kKILY4nQ1eNIQatoXEByZ5dWgnKqbnqmTrBE5B4N7lrMJKQ2ytWMiTO2o0v6Ew/w==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/cookie-signature": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/cookie-signature/-/cookie-signature-1.2.2.tgz",
      "integrity": "sha512-D76uU73ulSXrD1UXF4KE2TMxVVwhsnCgfAyTg9k8P6KGZjlXKrOLe4dJQKI3Bxi5wjesZoFXJWElNWBjPZMbhg==",
      "license": "MIT",
      "engines": {
        "node": ">=6.6.0"
      }
    },
    "node_modules/core-util-is": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/core-util-is/-/core-util-is-1.0.3.tgz",
      "integrity": "sha512-ZQBvi1DcpJ4GDqanjucZ2Hj3wEO5pZDS89BWbkcrvdxksJorwUDDZamX9ldFkp9aw2lmBDLgkObEA4DWNJ9FYQ==",
      "license": "MIT"
    },
    "node_modules/cors": {
      "version": "2.8.5",
      "resolved": "https://registry.npmjs.org/cors/-/cors-2.8.5.tgz",
      "integrity": "sha512-KIHbLJqu73RGr/hnbrO9uBeixNGuvSQjul/jdFvS/KFSIH1hWVd1ng7zOHx+YrEfInLG7q4n6GHQ9cDtxv/P6g==",
      "license": "MIT",
      "dependencies": {
        "object-assign": "^4",
        "vary": "^1"
      },
      "engines": {
        "node": ">= 0.10"
      }
    },
    "node_modules/crc-32": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/crc-32/-/crc-32-1.2.2.tgz",
      "integrity": "sha512-ROmzCKrTnOwybPcJApAA6WBWij23HVfGVNKqqrZpuyZOHqK2CwHSvpGuyt/UNNvaIjEd8X5IFGp4Mh+Ie1IHJQ==",
      "license": "Apache-2.0",
      "bin": {
        "crc32": "bin/crc32.njs"
      },
      "engines": {
        "node": ">=0.8"
      }
    },
    "node_modules/crc32-stream": {
      "version": "4.0.3",
      "resolved": "https://registry.npmjs.org/crc32-stream/-/crc32-stream-4.0.3.tgz",
      "integrity": "sha512-NT7w2JVU7DFroFdYkeq8cywxrgjPHWkdX1wjpRQXPX5Asews3tA+Ght6lddQO5Mkumffp3X7GEqku3epj2toIw==",
      "license": "MIT",
      "dependencies": {
        "crc-32": "^1.2.0",
        "readable-stream": "^3.4.0"
      },
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/cross-spawn": {
      "version": "7.0.6",
      "resolved": "https://registry.npmjs.org/cross-spawn/-/cross-spawn-7.0.6.tgz",
      "integrity": "sha512-uV2QOWP2nWzsy2aMp8aRibhi9dlzF5Hgh5SHaB9OiTGEyDTiJJyx0uy51QXdyWbtAHNua4XJzUKca3OzKUd3vA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "path-key": "^3.1.0",
        "shebang-command": "^2.0.0",
        "which": "^2.0.1"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/crypt": {
      "version": "0.0.2",
      "resolved": "https://registry.npmjs.org/crypt/-/crypt-0.0.2.tgz",
      "integrity": "sha512-mCxBlsHFYh9C+HVpiEacem8FEBnMXgU9gy4zmNC+SXAZNB/1idgp/aulFJ4FgCi7GPEVbfyng092GqL2k2rmow==",
      "dev": true,
      "license": "BSD-3-Clause",
      "engines": {
        "node": "*"
      }
    },
    "node_modules/crypto-js": {
      "version": "4.2.0",
      "resolved": "https://registry.npmjs.org/crypto-js/-/crypto-js-4.2.0.tgz",
      "integrity": "sha512-KALDyEYgpY+Rlob/iriUtjV6d5Eq+Y191A5g4UqLAi8CyGP9N1+FdVbkc1SxKc2r4YAYqG8JzO2KGL+AizD70Q==",
      "license": "MIT"
    },
    "node_modules/cssesc": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/cssesc/-/cssesc-3.0.0.tgz",
      "integrity": "sha512-/Tb/JcjK111nNScGob5MNtsntNM1aCNUDipB/TkwZFhyDrrE47SOx/18wF2bbjgc3ZzCSKW1T5nt5EbFoAz/Vg==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "cssesc": "bin/cssesc"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/csstype": {
      "version": "3.2.1",
      "resolved": "https://registry.npmjs.org/csstype/-/csstype-3.2.1.tgz",
      "integrity": "sha512-98XGutrXoh75MlgLihlNxAGbUuFQc7l1cqcnEZlLNKc0UrVdPndgmaDmYTDDh929VS/eqTZV0rozmhu2qqT1/g==",
      "license": "MIT"
    },
    "node_modules/dayjs": {
      "version": "1.11.19",
      "resolved": "https://registry.npmjs.org/dayjs/-/dayjs-1.11.19.tgz",
      "integrity": "sha512-t5EcLVS6QPBNqM2z8fakk/NKel+Xzshgt8FFKAn+qwlD1pzZWxh0nVCrvFK7ZDb6XucZeF9z8C7CBWTRIVApAw==",
      "license": "MIT"
    },
    "node_modules/debug": {
      "version": "4.4.3",
      "resolved": "https://registry.npmjs.org/debug/-/debug-4.4.3.tgz",
      "integrity": "sha512-RGwwWnwQvkVfavKVt22FGLw+xYSdzARwm0ru6DhTVA3umU5hZc28V3kO4stgYryrTlLpuvgI9GiijltAjNbcqA==",
      "license": "MIT",
      "dependencies": {
        "ms": "^2.1.3"
      },
      "engines": {
        "node": ">=6.0"
      },
      "peerDependenciesMeta": {
        "supports-color": {
          "optional": true
        }
      }
    },
    "node_modules/deep-is": {
      "version": "0.1.4",
      "resolved": "https://registry.npmjs.org/deep-is/-/deep-is-0.1.4.tgz",
      "integrity": "sha512-oIPzksmTg4/MriiaYGO+okXDT7ztn/w3Eptv/+gSIdMdKsJo0u4CfYNFJPy+4SKMuCqGw2wxnA+URMg3t8a/bQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/define-data-property": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/define-data-property/-/define-data-property-1.1.4.tgz",
      "integrity": "sha512-rBMvIzlpA8v6E+SJZoo++HAYqsLrkg7MSfIinMPFhmkorw7X+dOXVJQs+QT69zGkzMyfDnIMN2Wid1+NbL3T+A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "es-define-property": "^1.0.0",
        "es-errors": "^1.3.0",
        "gopd": "^1.0.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/define-properties": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/define-properties/-/define-properties-1.2.1.tgz",
      "integrity": "sha512-8QmQKqEASLd5nx0U1B1okLElbUuuttJ/AnYmRXbbbGDWh6uS208EjD4Xqq/I9wK7u0v6O08XhTWnt5XtEbR6Dg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "define-data-property": "^1.0.1",
        "has-property-descriptors": "^1.0.0",
        "object-keys": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/depd": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/depd/-/depd-2.0.0.tgz",
      "integrity": "sha512-g7nH6P6dyDioJogAAGprGpCtVImJhpPk/roCzdb3fIh61/s/nPsfR6onyMwkCAR/OlC3yBC0lESvUoQEAssIrw==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/destr": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/destr/-/destr-2.0.5.tgz",
      "integrity": "sha512-ugFTXCtDZunbzasqBxrK93Ik/DRYsO6S/fedkWEMKqt04xZ4csmnmwGDBAb07QWNaGMAmnTIemsYZCksjATwsA==",
      "license": "MIT"
    },
    "node_modules/didyoumean": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/didyoumean/-/didyoumean-1.2.2.tgz",
      "integrity": "sha512-gxtyfqMg7GKyhQmb056K7M3xszy/myH8w+B4RT+QXBQsvAOdc3XymqDDPHx1BgPgsdAA5SIifona89YtRATDzw==",
      "dev": true,
      "license": "Apache-2.0"
    },
    "node_modules/dlv": {
      "version": "1.1.3",
      "resolved": "https://registry.npmjs.org/dlv/-/dlv-1.1.3.tgz",
      "integrity": "sha512-+HlytyjlPKnIG8XuRG8WvmBP8xs8P71y+SKKS6ZXWoEgLuePxtDoUEiH7WkdePWrQ5JBpE6aoVqfZfJUQkjXwA==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/dotenv": {
      "version": "17.2.3",
      "resolved": "https://registry.npmjs.org/dotenv/-/dotenv-17.2.3.tgz",
      "integrity": "sha512-JVUnt+DUIzu87TABbhPmNfVdBDt18BLOWjMUFJMSi/Qqg7NTYtabbvSNJGOJ7afbRuv9D/lngizHtP7QyLQ+9w==",
      "license": "BSD-2-Clause",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://dotenvx.com"
      }
    },
    "node_modules/dunder-proto": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/dunder-proto/-/dunder-proto-1.0.1.tgz",
      "integrity": "sha512-KIN/nDJBQRcXw0MLVhZE9iQHmG68qAVIBg9CqmUYjmQIhgij9U5MFvrqkUL5FbtyyzZuOeOt0zdeRe4UY7ct+A==",
      "license": "MIT",
      "dependencies": {
        "call-bind-apply-helpers": "^1.0.1",
        "es-errors": "^1.3.0",
        "gopd": "^1.2.0"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/duplexer2": {
      "version": "0.1.4",
      "resolved": "https://registry.npmjs.org/duplexer2/-/duplexer2-0.1.4.tgz",
      "integrity": "sha512-asLFVfWWtJ90ZyOUHMqk7/S2w2guQKxUI2itj3d92ADHhxUSbCMGi1f1cBcJ7xM1To+pE/Khbwo1yuNbMEPKeA==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "readable-stream": "^2.0.2"
      }
    },
    "node_modules/duplexer2/node_modules/readable-stream": {
      "version": "2.3.8",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.3.8.tgz",
      "integrity": "sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==",
      "license": "MIT",
      "dependencies": {
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.3",
        "isarray": "~1.0.0",
        "process-nextick-args": "~2.0.0",
        "safe-buffer": "~5.1.1",
        "string_decoder": "~1.1.1",
        "util-deprecate": "~1.0.1"
      }
    },
    "node_modules/duplexer2/node_modules/safe-buffer": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.1.2.tgz",
      "integrity": "sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==",
      "license": "MIT"
    },
    "node_modules/duplexer2/node_modules/string_decoder": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.1.1.tgz",
      "integrity": "sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.1.0"
      }
    },
    "node_modules/eastasianwidth": {
      "version": "0.2.0",
      "resolved": "https://registry.npmjs.org/eastasianwidth/-/eastasianwidth-0.2.0.tgz",
      "integrity": "sha512-I88TYZWc9XiYHRQ4/3c5rjjfgkjhLyW2luGIheGERbNQ6OY7yTybanSpDXZa8y7VUP9YmDcYa+eyq4ca7iLqWA==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/ee-first": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/ee-first/-/ee-first-1.1.1.tgz",
      "integrity": "sha512-WMwm9LhRUo+WUaRN+vRuETqG89IgZphVSNkdFgeb6sS/E4OrDIN7t48CAewSHXc6C8lefD8KKfr5vY61brQlow==",
      "license": "MIT"
    },
    "node_modules/electron-to-chromium": {
      "version": "1.5.254",
      "resolved": "https://registry.npmjs.org/electron-to-chromium/-/electron-to-chromium-1.5.254.tgz",
      "integrity": "sha512-DcUsWpVhv9svsKRxnSCZ86SjD+sp32SGidNB37KpqXJncp1mfUgKbHvBomE89WJDbfVKw1mdv5+ikrvd43r+Bg==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/emoji-regex": {
      "version": "9.2.2",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-9.2.2.tgz",
      "integrity": "sha512-L18DaJsXSUk2+42pv8mLs5jJT2hqFkFE4j21wOmgbUqsZ2hL72NsUU785g9RXgo3s0ZNgVl42TiHp3ZtOv/Vyg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/encodeurl": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/encodeurl/-/encodeurl-2.0.0.tgz",
      "integrity": "sha512-Q0n9HRi4m6JuGIV1eFlmvJB7ZEVxu93IrMyiMsGC0lrMJMWzRgx6WGquyfQgZVb31vhGgXnfmPNNXmxnOkRBrg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/end-of-stream": {
      "version": "1.4.5",
      "resolved": "https://registry.npmjs.org/end-of-stream/-/end-of-stream-1.4.5.tgz",
      "integrity": "sha512-ooEGc6HP26xXq/N+GCGOT0JKCLDGrq2bQUZrQ7gyrJiZANJ/8YDTxTpQBXGMn+WbIQXNVpyWymm7KYVICQnyOg==",
      "license": "MIT",
      "dependencies": {
        "once": "^1.4.0"
      }
    },
    "node_modules/es-define-property": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/es-define-property/-/es-define-property-1.0.1.tgz",
      "integrity": "sha512-e3nRfgfUZ4rNGL232gUgX06QNyyez04KdjFrF+LTRoOXmrOgFKDg4BCdsjW8EnT69eqdYGmRpJwiPVYNrCaW3g==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/es-errors": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/es-errors/-/es-errors-1.3.0.tgz",
      "integrity": "sha512-Zf5H2Kxt2xjTvbJvP2ZWLEICxA6j+hAmMzIlypy4xcBg1vKVnx89Wy0GbS+kf5cwCVFFzdCFh2XSCFNULS6csw==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/es-object-atoms": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/es-object-atoms/-/es-object-atoms-1.1.1.tgz",
      "integrity": "sha512-FGgH2h8zKNim9ljj7dankFPcICIK9Cp5bm+c2gQSYePhpaG5+esrLODihIorn+Pe6FGJzWhXQotPv73jTaldXA==",
      "license": "MIT",
      "dependencies": {
        "es-errors": "^1.3.0"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/es6-object-assign": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/es6-object-assign/-/es6-object-assign-1.1.0.tgz",
      "integrity": "sha512-MEl9uirslVwqQU369iHNWZXsI8yaZYGg/D65aOgZkeyFJwHYSxilf7rQzXKI7DdDuBPrBXbfk3sl9hJhmd5AUw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/esbuild": {
      "version": "0.25.12",
      "resolved": "https://registry.npmjs.org/esbuild/-/esbuild-0.25.12.tgz",
      "integrity": "sha512-bbPBYYrtZbkt6Os6FiTLCTFxvq4tt3JKall1vRwshA3fdVztsLAatFaZobhkBC8/BrPetoa0oksYoKXoG4ryJg==",
      "dev": true,
      "hasInstallScript": true,
      "license": "MIT",
      "bin": {
        "esbuild": "bin/esbuild"
      },
      "engines": {
        "node": ">=18"
      },
      "optionalDependencies": {
        "@esbuild/aix-ppc64": "0.25.12",
        "@esbuild/android-arm": "0.25.12",
        "@esbuild/android-arm64": "0.25.12",
        "@esbuild/android-x64": "0.25.12",
        "@esbuild/darwin-arm64": "0.25.12",
        "@esbuild/darwin-x64": "0.25.12",
        "@esbuild/freebsd-arm64": "0.25.12",
        "@esbuild/freebsd-x64": "0.25.12",
        "@esbuild/linux-arm": "0.25.12",
        "@esbuild/linux-arm64": "0.25.12",
        "@esbuild/linux-ia32": "0.25.12",
        "@esbuild/linux-loong64": "0.25.12",
        "@esbuild/linux-mips64el": "0.25.12",
        "@esbuild/linux-ppc64": "0.25.12",
        "@esbuild/linux-riscv64": "0.25.12",
        "@esbuild/linux-s390x": "0.25.12",
        "@esbuild/linux-x64": "0.25.12",
        "@esbuild/netbsd-arm64": "0.25.12",
        "@esbuild/netbsd-x64": "0.25.12",
        "@esbuild/openbsd-arm64": "0.25.12",
        "@esbuild/openbsd-x64": "0.25.12",
        "@esbuild/openharmony-arm64": "0.25.12",
        "@esbuild/sunos-x64": "0.25.12",
        "@esbuild/win32-arm64": "0.25.12",
        "@esbuild/win32-ia32": "0.25.12",
        "@esbuild/win32-x64": "0.25.12"
      }
    },
    "node_modules/escalade": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/escalade/-/escalade-3.2.0.tgz",
      "integrity": "sha512-WUj2qlxaQtO4g6Pq5c29GTcWGDyd8itL8zTlipgECz3JesAiiOKotd8JU6otB3PACgG6xkJUyVhboMS+bje/jA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/escape-html": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/escape-html/-/escape-html-1.0.3.tgz",
      "integrity": "sha512-NiSupZ4OeuGwr68lGIeym/ksIZMJodUGOSCZ/FSnTxcrekbvqrgdUxlJOMpijaKZVjAJrWrGs/6Jy8OMuyj9ow==",
      "license": "MIT"
    },
    "node_modules/escape-string-regexp": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/escape-string-regexp/-/escape-string-regexp-4.0.0.tgz",
      "integrity": "sha512-TtpcNJ3XAzx3Gq8sWRzJaVajRs0uVxA2YAkdb1jm2YkPz4G6egUFAyA3n5vtEIZefPk5Wa4UXbKuS5fKkJWdgA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/eslint": {
      "version": "9.9.1",
      "resolved": "https://registry.npmjs.org/eslint/-/eslint-9.9.1.tgz",
      "integrity": "sha512-dHvhrbfr4xFQ9/dq+jcVneZMyRYLjggWjk6RVsIiHsP8Rz6yZ8LvZ//iU4TrZF+SXWG+JkNF2OyiZRvzgRDqMg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@eslint-community/eslint-utils": "^4.2.0",
        "@eslint-community/regexpp": "^4.11.0",
        "@eslint/config-array": "^0.18.0",
        "@eslint/eslintrc": "^3.1.0",
        "@eslint/js": "9.9.1",
        "@humanwhocodes/module-importer": "^1.0.1",
        "@humanwhocodes/retry": "^0.3.0",
        "@nodelib/fs.walk": "^1.2.8",
        "ajv": "^6.12.4",
        "chalk": "^4.0.0",
        "cross-spawn": "^7.0.2",
        "debug": "^4.3.2",
        "escape-string-regexp": "^4.0.0",
        "eslint-scope": "^8.0.2",
        "eslint-visitor-keys": "^4.0.0",
        "espree": "^10.1.0",
        "esquery": "^1.5.0",
        "esutils": "^2.0.2",
        "fast-deep-equal": "^3.1.3",
        "file-entry-cache": "^8.0.0",
        "find-up": "^5.0.0",
        "glob-parent": "^6.0.2",
        "ignore": "^5.2.0",
        "imurmurhash": "^0.1.4",
        "is-glob": "^4.0.0",
        "is-path-inside": "^3.0.3",
        "json-stable-stringify-without-jsonify": "^1.0.1",
        "levn": "^0.4.1",
        "lodash.merge": "^4.6.2",
        "minimatch": "^3.1.2",
        "natural-compare": "^1.4.0",
        "optionator": "^0.9.3",
        "strip-ansi": "^6.0.1",
        "text-table": "^0.2.0"
      },
      "bin": {
        "eslint": "bin/eslint.js"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "url": "https://eslint.org/donate"
      },
      "peerDependencies": {
        "jiti": "*"
      },
      "peerDependenciesMeta": {
        "jiti": {
          "optional": true
        }
      }
    },
    "node_modules/eslint-plugin-react-hooks": {
      "version": "5.1.0-rc.0",
      "resolved": "https://registry.npmjs.org/eslint-plugin-react-hooks/-/eslint-plugin-react-hooks-5.1.0-rc.0.tgz",
      "integrity": "sha512-xBc+mRT2KSyzKm78GyaOFPyF4EnSRfTSmre88Ak8jG1HnpNGEiHETbCuXih8Xl796DryrJej/8IdW4oQ+m5kPg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "peerDependencies": {
        "eslint": "^3.0.0 || ^4.0.0 || ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0-0 || ^9.0.0"
      }
    },
    "node_modules/eslint-plugin-react-refresh": {
      "version": "0.4.11",
      "resolved": "https://registry.npmjs.org/eslint-plugin-react-refresh/-/eslint-plugin-react-refresh-0.4.11.tgz",
      "integrity": "sha512-wrAKxMbVr8qhXTtIKfXqAn5SAtRZt0aXxe5P23Fh4pUAdC6XEsybGLB8P0PI4j1yYqOgUEUlzKAGDfo7rJOjcw==",
      "dev": true,
      "license": "MIT",
      "peerDependencies": {
        "eslint": ">=7"
      }
    },
    "node_modules/eslint-scope": {
      "version": "8.4.0",
      "resolved": "https://registry.npmjs.org/eslint-scope/-/eslint-scope-8.4.0.tgz",
      "integrity": "sha512-sNXOfKCn74rt8RICKMvJS7XKV/Xk9kA7DyJr8mJik3S7Cwgy3qlkkmyS2uQB3jiJg6VNdZd/pDBJu0nvG2NlTg==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "esrecurse": "^4.3.0",
        "estraverse": "^5.2.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/eslint-visitor-keys": {
      "version": "4.2.1",
      "resolved": "https://registry.npmjs.org/eslint-visitor-keys/-/eslint-visitor-keys-4.2.1.tgz",
      "integrity": "sha512-Uhdk5sfqcee/9H/rCOJikYz67o0a2Tw2hGRPOG2Y1R2dg7brRe1uG0yaNQDHu+TO/uQPF/5eCapvYSmHUjt7JQ==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/espree": {
      "version": "10.4.0",
      "resolved": "https://registry.npmjs.org/espree/-/espree-10.4.0.tgz",
      "integrity": "sha512-j6PAQ2uUr79PZhBjP5C5fhl8e39FmRnOjsD5lGnWrFU8i2G776tBK7+nP8KuQUTTyAZUwfQqXAgrVH5MbH9CYQ==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "acorn": "^8.15.0",
        "acorn-jsx": "^5.3.2",
        "eslint-visitor-keys": "^4.2.1"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "url": "https://opencollective.com/eslint"
      }
    },
    "node_modules/esprima": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/esprima/-/esprima-4.0.1.tgz",
      "integrity": "sha512-eGuFFw7Upda+g4p+QHvnW0RyTX/SVeJBDM/gCtMARO0cLuT2HcEKnTPvhjV6aGeqrCB/sbNop0Kszm0jsaWU4A==",
      "dev": true,
      "license": "BSD-2-Clause",
      "bin": {
        "esparse": "bin/esparse.js",
        "esvalidate": "bin/esvalidate.js"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/esquery": {
      "version": "1.6.0",
      "resolved": "https://registry.npmjs.org/esquery/-/esquery-1.6.0.tgz",
      "integrity": "sha512-ca9pw9fomFcKPvFLXhBKUK90ZvGibiGOvRJNbjljY7s7uq/5YO4BOzcYtJqExdx99rF6aAcnRxHmcUHcz6sQsg==",
      "dev": true,
      "license": "BSD-3-Clause",
      "dependencies": {
        "estraverse": "^5.1.0"
      },
      "engines": {
        "node": ">=0.10"
      }
    },
    "node_modules/esrecurse": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/esrecurse/-/esrecurse-4.3.0.tgz",
      "integrity": "sha512-KmfKL3b6G+RXvP8N1vr3Tq1kL/oCFgn2NYXEtqP8/L3pKapUA4G8cFVaoF3SU323CD4XypR/ffioHmkti6/Tag==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "estraverse": "^5.2.0"
      },
      "engines": {
        "node": ">=4.0"
      }
    },
    "node_modules/estraverse": {
      "version": "5.3.0",
      "resolved": "https://registry.npmjs.org/estraverse/-/estraverse-5.3.0.tgz",
      "integrity": "sha512-MMdARuVEQziNTeJD8DgMqmhwR11BRQ/cBP+pLtYdSTnf3MIO8fFeiINEbX36ZdNlfU/7A9f3gUw49B3oQsvwBA==",
      "dev": true,
      "license": "BSD-2-Clause",
      "engines": {
        "node": ">=4.0"
      }
    },
    "node_modules/esutils": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/esutils/-/esutils-2.0.3.tgz",
      "integrity": "sha512-kVscqXk4OCp68SZ0dkgEKVi6/8ij300KBWTJq32P/dYeWTSwK41WyTxalN1eRmA5Z9UU/LX9D7FWSmV9SAYx6g==",
      "dev": true,
      "license": "BSD-2-Clause",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/etag": {
      "version": "1.8.1",
      "resolved": "https://registry.npmjs.org/etag/-/etag-1.8.1.tgz",
      "integrity": "sha512-aIL5Fx7mawVa300al2BnEE4iNvo1qETxLrPI/o05L7z6go7fCw1J6EQmbK4FmJ2AS7kgVF/KEZWufBfdClMcPg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/exceljs": {
      "version": "4.4.0",
      "resolved": "https://registry.npmjs.org/exceljs/-/exceljs-4.4.0.tgz",
      "integrity": "sha512-XctvKaEMaj1Ii9oDOqbW/6e1gXknSY4g/aLCDicOXqBE4M0nRWkUu0PTp++UPNzoFY12BNHMfs/VadKIS6llvg==",
      "license": "MIT",
      "dependencies": {
        "archiver": "^5.0.0",
        "dayjs": "^1.8.34",
        "fast-csv": "^4.3.1",
        "jszip": "^3.10.1",
        "readable-stream": "^3.6.0",
        "saxes": "^5.0.1",
        "tmp": "^0.2.0",
        "unzipper": "^0.10.11",
        "uuid": "^8.3.0"
      },
      "engines": {
        "node": ">=8.3.0"
      }
    },
    "node_modules/exceljs/node_modules/uuid": {
      "version": "8.3.2",
      "resolved": "https://registry.npmjs.org/uuid/-/uuid-8.3.2.tgz",
      "integrity": "sha512-+NYs2QeMWy+GWFOEm9xnn6HCDp0l7QBD7ml8zLUmJ+93Q5NF0NocErnwkTkXVFNiX3/fpC6afS8Dhb/gz7R7eg==",
      "license": "MIT",
      "bin": {
        "uuid": "dist/bin/uuid"
      }
    },
    "node_modules/express": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/express/-/express-5.1.0.tgz",
      "integrity": "sha512-DT9ck5YIRU+8GYzzU5kT3eHGA5iL+1Zd0EutOmTE9Dtk+Tvuzd23VBU+ec7HPNSTxXYO55gPV/hq4pSBJDjFpA==",
      "license": "MIT",
      "dependencies": {
        "accepts": "^2.0.0",
        "body-parser": "^2.2.0",
        "content-disposition": "^1.0.0",
        "content-type": "^1.0.5",
        "cookie": "^0.7.1",
        "cookie-signature": "^1.2.1",
        "debug": "^4.4.0",
        "encodeurl": "^2.0.0",
        "escape-html": "^1.0.3",
        "etag": "^1.8.1",
        "finalhandler": "^2.1.0",
        "fresh": "^2.0.0",
        "http-errors": "^2.0.0",
        "merge-descriptors": "^2.0.0",
        "mime-types": "^3.0.0",
        "on-finished": "^2.4.1",
        "once": "^1.4.0",
        "parseurl": "^1.3.3",
        "proxy-addr": "^2.0.7",
        "qs": "^6.14.0",
        "range-parser": "^1.2.1",
        "router": "^2.2.0",
        "send": "^1.1.0",
        "serve-static": "^2.2.0",
        "statuses": "^2.0.1",
        "type-is": "^2.0.1",
        "vary": "^1.1.2"
      },
      "engines": {
        "node": ">= 18"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/express"
      }
    },
    "node_modules/fast-csv": {
      "version": "4.3.6",
      "resolved": "https://registry.npmjs.org/fast-csv/-/fast-csv-4.3.6.tgz",
      "integrity": "sha512-2RNSpuwwsJGP0frGsOmTb9oUF+VkFSM4SyLTDgwf2ciHWTarN0lQTC+F2f/t5J9QjW+c65VFIAAu85GsvMIusw==",
      "license": "MIT",
      "dependencies": {
        "@fast-csv/format": "4.3.5",
        "@fast-csv/parse": "4.3.6"
      },
      "engines": {
        "node": ">=10.0.0"
      }
    },
    "node_modules/fast-deep-equal": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/fast-deep-equal/-/fast-deep-equal-3.1.3.tgz",
      "integrity": "sha512-f3qQ9oQy9j2AhBe/H9VC91wLmKBCCU/gDOnKNAYG5hswO7BLKj09Hc5HYNz9cGI++xlpDCIgDaitVs03ATR84Q==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/fast-glob": {
      "version": "3.3.3",
      "resolved": "https://registry.npmjs.org/fast-glob/-/fast-glob-3.3.3.tgz",
      "integrity": "sha512-7MptL8U0cqcFdzIzwOTHoilX9x5BrNqye7Z/LuC7kCMRio1EMSyqRK3BEAUD7sXRq4iT4AzTVuZdhgQ2TCvYLg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@nodelib/fs.stat": "^2.0.2",
        "@nodelib/fs.walk": "^1.2.3",
        "glob-parent": "^5.1.2",
        "merge2": "^1.3.0",
        "micromatch": "^4.0.8"
      },
      "engines": {
        "node": ">=8.6.0"
      }
    },
    "node_modules/fast-glob/node_modules/glob-parent": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/glob-parent/-/glob-parent-5.1.2.tgz",
      "integrity": "sha512-AOIgSQCepiJYwP3ARnGx+5VnTu2HBYdzbGP45eLw1vr3zB3vZLeyed1sC9hnbcOc9/SrMyM5RPQrkGz4aS9Zow==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "is-glob": "^4.0.1"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/fast-json-stable-stringify": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/fast-json-stable-stringify/-/fast-json-stable-stringify-2.1.0.tgz",
      "integrity": "sha512-lhd/wF+Lk98HZoTCtlVraHtfh5XYijIjalXck7saUtuanSDyLMxnHhSXEDJqHxD7msR8D0uCmqlkwjCV8xvwHw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/fast-levenshtein": {
      "version": "2.0.6",
      "resolved": "https://registry.npmjs.org/fast-levenshtein/-/fast-levenshtein-2.0.6.tgz",
      "integrity": "sha512-DCXu6Ifhqcks7TZKY3Hxp3y6qphY5SJZmrWMDrKcERSOXWQdMhU9Ig/PYrzyw/ul9jOIyh0N4M0tbC5hodg8dw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/fastq": {
      "version": "1.19.1",
      "resolved": "https://registry.npmjs.org/fastq/-/fastq-1.19.1.tgz",
      "integrity": "sha512-GwLTyxkCXjXbxqIhTsMI2Nui8huMPtnxg7krajPJAjnEG/iiOS7i+zCtWGZR9G0NBKbXKh6X9m9UIsYX/N6vvQ==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "reusify": "^1.0.4"
      }
    },
    "node_modules/file-entry-cache": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/file-entry-cache/-/file-entry-cache-8.0.0.tgz",
      "integrity": "sha512-XXTUwCvisa5oacNGRP9SfNtYBNAMi+RPwBFmblZEF7N7swHYQS6/Zfk7SRwx4D5j3CH211YNRco1DEMNVfZCnQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "flat-cache": "^4.0.0"
      },
      "engines": {
        "node": ">=16.0.0"
      }
    },
    "node_modules/fill-range": {
      "version": "7.1.1",
      "resolved": "https://registry.npmjs.org/fill-range/-/fill-range-7.1.1.tgz",
      "integrity": "sha512-YsGpe3WHLK8ZYi4tWDg2Jy3ebRz2rXowDxnld4bkQB00cc/1Zw9AWnC0i9ztDJitivtQvaI9KaLyKrc+hBW0yg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "to-regex-range": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/finalhandler": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/finalhandler/-/finalhandler-2.1.0.tgz",
      "integrity": "sha512-/t88Ty3d5JWQbWYgaOGCCYfXRwV1+be02WqYYlL6h0lEiUAMPM8o8qKGO01YIkOHzka2up08wvgYD0mDiI+q3Q==",
      "license": "MIT",
      "dependencies": {
        "debug": "^4.4.0",
        "encodeurl": "^2.0.0",
        "escape-html": "^1.0.3",
        "on-finished": "^2.4.1",
        "parseurl": "^1.3.3",
        "statuses": "^2.0.1"
      },
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/find-up": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/find-up/-/find-up-5.0.0.tgz",
      "integrity": "sha512-78/PXT1wlLLDgTzDs7sjq9hzz0vXD+zn+7wypEe4fXQxCmdmqfGsEPQxmiCSQI3ajFV91bVSsvNtrJRiW6nGng==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "locate-path": "^6.0.0",
        "path-exists": "^4.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/flat-cache": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/flat-cache/-/flat-cache-4.0.1.tgz",
      "integrity": "sha512-f7ccFPK3SXFHpx15UIGyRJ/FJQctuKZ0zVuN3frBo4HnK3cay9VEW0R6yPYFHC0AgqhukPzKjq22t5DmAyqGyw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "flatted": "^3.2.9",
        "keyv": "^4.5.4"
      },
      "engines": {
        "node": ">=16"
      }
    },
    "node_modules/flatted": {
      "version": "3.3.3",
      "resolved": "https://registry.npmjs.org/flatted/-/flatted-3.3.3.tgz",
      "integrity": "sha512-GX+ysw4PBCz0PzosHDepZGANEuFCMLrnRTiEy9McGjmkCQYwRq4A/X786G/fjM/+OjsWSU1ZrY5qyARZmO/uwg==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/for-each": {
      "version": "0.3.5",
      "resolved": "https://registry.npmjs.org/for-each/-/for-each-0.3.5.tgz",
      "integrity": "sha512-dKx12eRCVIzqCxFGplyFKJMPvLEWgmNtUrpTiJIR5u97zEhRG8ySrtboPHZXx7daLxQVrl643cTzbab2tkQjxg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "is-callable": "^1.2.7"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/foreground-child": {
      "version": "3.3.1",
      "resolved": "https://registry.npmjs.org/foreground-child/-/foreground-child-3.3.1.tgz",
      "integrity": "sha512-gIXjKqtFuWEgzFRJA9WCQeSJLZDjgJUOMCMzxtvFq/37KojM1BFGufqsCy0r4qSQmYLsZYMeyRqzIWOMup03sw==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "cross-spawn": "^7.0.6",
        "signal-exit": "^4.0.1"
      },
      "engines": {
        "node": ">=14"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/forwarded": {
      "version": "0.2.0",
      "resolved": "https://registry.npmjs.org/forwarded/-/forwarded-0.2.0.tgz",
      "integrity": "sha512-buRG0fpBtRHSTCOASe6hD258tEubFoRLb4ZNA6NxMVHNw2gOcwHo9wyablzMzOA5z9xA9L1KNjk/Nt6MT9aYow==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/fraction.js": {
      "version": "4.3.7",
      "resolved": "https://registry.npmjs.org/fraction.js/-/fraction.js-4.3.7.tgz",
      "integrity": "sha512-ZsDfxO51wGAXREY55a7la9LScWpwv9RxIrYABrlvOFBlH/ShPnrtsXeuUIfXKKOVicNxQ+o8JTbJvjS4M89yew==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": "*"
      },
      "funding": {
        "type": "patreon",
        "url": "https://github.com/sponsors/rawify"
      }
    },
    "node_modules/framer-motion": {
      "version": "12.23.11",
      "resolved": "https://registry.npmjs.org/framer-motion/-/framer-motion-12.23.11.tgz",
      "integrity": "sha512-VzNi+exyI3bn7Pzvz1Fjap1VO9gQu8mxrsSsNamMidsZ8AA8W2kQsR+YQOciEUbMtkKAWIbPHPttfn5e9jqqJQ==",
      "license": "MIT",
      "dependencies": {
        "motion-dom": "^12.23.9",
        "motion-utils": "^12.23.6",
        "tslib": "^2.4.0"
      },
      "peerDependencies": {
        "@emotion/is-prop-valid": "*",
        "react": "^18.0.0 || ^19.0.0",
        "react-dom": "^18.0.0 || ^19.0.0"
      },
      "peerDependenciesMeta": {
        "@emotion/is-prop-valid": {
          "optional": true
        },
        "react": {
          "optional": true
        },
        "react-dom": {
          "optional": true
        }
      }
    },
    "node_modules/fresh": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/fresh/-/fresh-2.0.0.tgz",
      "integrity": "sha512-Rx/WycZ60HOaqLKAi6cHRKKI7zxWbJ31MhntmtwMoaTeF7XFH9hhBp8vITaMidfljRQ6eYWCKkaTK+ykVJHP2A==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/fs-constants": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/fs-constants/-/fs-constants-1.0.0.tgz",
      "integrity": "sha512-y6OAwoSIf7FyjMIv94u+b5rdheZEjzR63GTyZJm5qh4Bi+2YgwLCcI/fPFZkL5PSixOt6ZNKm+w+Hfp/Bciwow==",
      "license": "MIT"
    },
    "node_modules/fs.realpath": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/fs.realpath/-/fs.realpath-1.0.0.tgz",
      "integrity": "sha512-OO0pH2lK6a0hZnAdau5ItzHPI6pUlvI7jMVnxUQRtw4owF2wk8lOSabtGDCTP4Ggrg2MbGnWO9X8K1t4+fGMDw==",
      "license": "ISC"
    },
    "node_modules/fsevents": {
      "version": "2.3.3",
      "resolved": "https://registry.npmjs.org/fsevents/-/fsevents-2.3.3.tgz",
      "integrity": "sha512-5xoDfX+fL7faATnagmWPpbFtwh/R77WmMMqqHGS65C3vvB0YHrgF+B1YmZ3441tMj5n63k0212XNoJwzlhffQw==",
      "dev": true,
      "hasInstallScript": true,
      "license": "MIT",
      "optional": true,
      "os": [
        "darwin"
      ],
      "engines": {
        "node": "^8.16.0 || ^10.6.0 || >=11.0.0"
      }
    },
    "node_modules/fstream": {
      "version": "1.0.12",
      "resolved": "https://registry.npmjs.org/fstream/-/fstream-1.0.12.tgz",
      "integrity": "sha512-WvJ193OHa0GHPEL+AycEJgxvBEwyfRkN1vhjca23OaPVMCaLCXTd5qAu82AjTcgP1UJmytkOKb63Ypde7raDIg==",
      "deprecated": "This package is no longer supported.",
      "license": "ISC",
      "dependencies": {
        "graceful-fs": "^4.1.2",
        "inherits": "~2.0.0",
        "mkdirp": ">=0.5 0",
        "rimraf": "2"
      },
      "engines": {
        "node": ">=0.6"
      }
    },
    "node_modules/function-bind": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/function-bind/-/function-bind-1.1.2.tgz",
      "integrity": "sha512-7XHNxH7qX9xG5mIwxkhumTox/MIRNcOgDrxWsMt2pAr23WHp6MrRlN7FBSFpCpr+oVO0F744iUgR82nJMfG2SA==",
      "license": "MIT",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/generator-function": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/generator-function/-/generator-function-2.0.1.tgz",
      "integrity": "sha512-SFdFmIJi+ybC0vjlHN0ZGVGHc3lgE0DxPAT0djjVg+kjOnSqclqmj0KQ7ykTOLP6YxoqOvuAODGdcHJn+43q3g==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/get-intrinsic": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/get-intrinsic/-/get-intrinsic-1.3.0.tgz",
      "integrity": "sha512-9fSjSaos/fRIVIp+xSJlE6lfwhES7LNtKaCBIamHsjr2na1BiABJPo0mOjjz8GJDURarmCPGqaiVg5mfjb98CQ==",
      "license": "MIT",
      "dependencies": {
        "call-bind-apply-helpers": "^1.0.2",
        "es-define-property": "^1.0.1",
        "es-errors": "^1.3.0",
        "es-object-atoms": "^1.1.1",
        "function-bind": "^1.1.2",
        "get-proto": "^1.0.1",
        "gopd": "^1.2.0",
        "has-symbols": "^1.1.0",
        "hasown": "^2.0.2",
        "math-intrinsics": "^1.1.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/get-proto": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/get-proto/-/get-proto-1.0.1.tgz",
      "integrity": "sha512-sTSfBjoXBp89JvIKIefqw7U2CCebsc74kiY6awiGogKtoSGbgjYE/G/+l9sF3MWFPNc9IcoOC4ODfKHfxFmp0g==",
      "license": "MIT",
      "dependencies": {
        "dunder-proto": "^1.0.1",
        "es-object-atoms": "^1.0.0"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/get-tsconfig": {
      "version": "4.13.0",
      "resolved": "https://registry.npmjs.org/get-tsconfig/-/get-tsconfig-4.13.0.tgz",
      "integrity": "sha512-1VKTZJCwBrvbd+Wn3AOgQP/2Av+TfTCOlE4AcRJE72W1ksZXbAx8PPBR9RzgTeSPzlPMHrbANMH3LbltH73wxQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "resolve-pkg-maps": "^1.0.0"
      },
      "funding": {
        "url": "https://github.com/privatenumber/get-tsconfig?sponsor=1"
      }
    },
    "node_modules/glob": {
      "version": "7.2.3",
      "resolved": "https://registry.npmjs.org/glob/-/glob-7.2.3.tgz",
      "integrity": "sha512-nFR0zLpU2YCaRxwoCJvL6UvCH2JFyFVIvwTLsIf21AuHlMskA1hhTdk+LlYJtOlYt9v6dvszD2BGRqBL+iQK9Q==",
      "deprecated": "Glob versions prior to v9 are no longer supported",
      "license": "ISC",
      "dependencies": {
        "fs.realpath": "^1.0.0",
        "inflight": "^1.0.4",
        "inherits": "2",
        "minimatch": "^3.1.1",
        "once": "^1.3.0",
        "path-is-absolute": "^1.0.0"
      },
      "engines": {
        "node": "*"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/glob-parent": {
      "version": "6.0.2",
      "resolved": "https://registry.npmjs.org/glob-parent/-/glob-parent-6.0.2.tgz",
      "integrity": "sha512-XxwI8EOhVQgWp6iDL+3b0r86f4d6AX6zSU55HfB4ydCEuXLXc5FcYeOu+nnGftS4TEju/11rt4KJPTMgbfmv4A==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "is-glob": "^4.0.3"
      },
      "engines": {
        "node": ">=10.13.0"
      }
    },
    "node_modules/globals": {
      "version": "15.9.0",
      "resolved": "https://registry.npmjs.org/globals/-/globals-15.9.0.tgz",
      "integrity": "sha512-SmSKyLLKFbSr6rptvP8izbyxJL4ILwqO9Jg23UA0sDlGlu58V59D1//I3vlc0KJphVdUR7vMjHIplYnzBxorQA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=18"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/goober": {
      "version": "2.1.18",
      "resolved": "https://registry.npmjs.org/goober/-/goober-2.1.18.tgz",
      "integrity": "sha512-2vFqsaDVIT9Gz7N6kAL++pLpp41l3PfDuusHcjnGLfR6+huZkl6ziX+zgVC3ZxpqWhzH6pyDdGrCeDhMIvwaxw==",
      "license": "MIT",
      "peerDependencies": {
        "csstype": "^3.0.10"
      }
    },
    "node_modules/gopd": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/gopd/-/gopd-1.2.0.tgz",
      "integrity": "sha512-ZUKRh6/kUFoAiTAtTYPZJ3hw9wNxx+BIBOijnlG9PnrJsCcSjs1wyyD6vJpaYtgnzDrKYRSqf3OO6Rfa93xsRg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/graceful-fs": {
      "version": "4.2.11",
      "resolved": "https://registry.npmjs.org/graceful-fs/-/graceful-fs-4.2.11.tgz",
      "integrity": "sha512-RbJ5/jmFcNNCcDV5o9eTnBLJ/HszWV0P73bc+Ff4nS/rJj+YaS6IGyiOL0VoBYX+l1Wrl3k63h/KrH+nhJ0XvQ==",
      "license": "ISC"
    },
    "node_modules/graphemer": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/graphemer/-/graphemer-1.4.0.tgz",
      "integrity": "sha512-EtKwoO6kxCL9WO5xipiHTZlSzBm7WLT627TqC/uVRd0HKmq8NXyebnNYxDoBi7wt8eTWrUrKXCOVaFq9x1kgag==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/has-flag": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/has-flag/-/has-flag-4.0.0.tgz",
      "integrity": "sha512-EykJT/Q1KjTWctppgIAgfSO0tKVuZUjhgMr17kqTumMl6Afv3EISleU7qZUzoXDFTAHTDC4NOoG/ZxU3EvlMPQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/has-property-descriptors": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/has-property-descriptors/-/has-property-descriptors-1.0.2.tgz",
      "integrity": "sha512-55JNKuIW+vq4Ke1BjOTjM2YctQIvCT7GFzHwmfZPGo5wnrgkid0YQtnAleFSqumZm4az3n2BS+erby5ipJdgrg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "es-define-property": "^1.0.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-symbols": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/has-symbols/-/has-symbols-1.1.0.tgz",
      "integrity": "sha512-1cDNdwJ2Jaohmb3sg4OmKaMBwuC48sYni5HUw2DvsC8LjGTLK9h+eb1X6RyuOHe4hT0ULCW68iomhjUoKUqlPQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/has-tostringtag": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/has-tostringtag/-/has-tostringtag-1.0.2.tgz",
      "integrity": "sha512-NqADB8VjPFLM2V0VvHUewwwsw0ZWBaIdgo+ieHtK3hasLz4qeCRjYcqfB6AQrBggRKppKF8L52/VqdVsO47Dlw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "has-symbols": "^1.0.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/hasown": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/hasown/-/hasown-2.0.2.tgz",
      "integrity": "sha512-0hJU9SCPvmMzIBdZFqNPXWa6dqh7WdH0cII9y+CyS8rG3nL48Bclra9HmKhVVUHyPWNH5Y7xDwAB7bfgSjkUMQ==",
      "license": "MIT",
      "dependencies": {
        "function-bind": "^1.1.2"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/http-errors": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/http-errors/-/http-errors-2.0.0.tgz",
      "integrity": "sha512-FtwrG/euBzaEjYeRqOgly7G0qviiXoJWnvEH2Z1plBdXgbyjv34pHTSb9zoeHMyDy33+DWy5Wt9Wo+TURtOYSQ==",
      "license": "MIT",
      "dependencies": {
        "depd": "2.0.0",
        "inherits": "2.0.4",
        "setprototypeof": "1.2.0",
        "statuses": "2.0.1",
        "toidentifier": "1.0.1"
      },
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/http-errors/node_modules/statuses": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/statuses/-/statuses-2.0.1.tgz",
      "integrity": "sha512-RwNA9Z/7PrK06rYLIzFMlaF+l73iwpzsqRIFgbMLbTcLD6cOao82TaWefPXQvB2fOC4AjuYSEndS7N/mTCbkdQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/iconv-lite": {
      "version": "0.6.3",
      "resolved": "https://registry.npmjs.org/iconv-lite/-/iconv-lite-0.6.3.tgz",
      "integrity": "sha512-4fCk79wshMdzMp2rH06qWrJE4iolqLhCUH+OiuIgU++RB0+94NlDL81atO7GX55uUKueo0txHNtvEyI6D7WdMw==",
      "license": "MIT",
      "dependencies": {
        "safer-buffer": ">= 2.1.2 < 3.0.0"
      },
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/ieee754": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/ieee754/-/ieee754-1.2.1.tgz",
      "integrity": "sha512-dcyqhDvX1C46lXZcVqCpK+FtMRQVdIMN6/Df5js2zouUsqG7I6sFxitIC+7KYK29KdXOLHdu9zL4sFnoVQnqaA==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "BSD-3-Clause"
    },
    "node_modules/ignore": {
      "version": "5.3.2",
      "resolved": "https://registry.npmjs.org/ignore/-/ignore-5.3.2.tgz",
      "integrity": "sha512-hsBTNUqQTDwkWtcdYI2i06Y/nUBEsNEDJKjWdigLvegy8kDuJAS8uRlpkkcQpyEXL0Z/pjDy5HBmMjRCJ2gq+g==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 4"
      }
    },
    "node_modules/immediate": {
      "version": "3.0.6",
      "resolved": "https://registry.npmjs.org/immediate/-/immediate-3.0.6.tgz",
      "integrity": "sha512-XXOFtyqDjNDAQxVfYxuF7g9Il/IbWmmlQg2MYKOH8ExIT1qg6xc4zyS3HaEEATgs1btfzxq15ciUiY7gjSXRGQ==",
      "license": "MIT"
    },
    "node_modules/import-fresh": {
      "version": "3.3.1",
      "resolved": "https://registry.npmjs.org/import-fresh/-/import-fresh-3.3.1.tgz",
      "integrity": "sha512-TR3KfrTZTYLPB6jUjfx6MF9WcWrHL9su5TObK4ZkYgBdWKPOFoSoQIdEuTuR82pmtxH2spWG9h6etwfr1pLBqQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "parent-module": "^1.0.0",
        "resolve-from": "^4.0.0"
      },
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/imurmurhash": {
      "version": "0.1.4",
      "resolved": "https://registry.npmjs.org/imurmurhash/-/imurmurhash-0.1.4.tgz",
      "integrity": "sha512-JmXMZ6wuvDmLiHEml9ykzqO6lwFbof0GG4IkcGaENdCRDDmMVnny7s5HsIgHCbaq0w2MyPhDqkhTUgS2LU2PHA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.8.19"
      }
    },
    "node_modules/inflight": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/inflight/-/inflight-1.0.6.tgz",
      "integrity": "sha512-k92I/b08q4wvFscXCLvqfsHCrjrF7yiXsQuIVvVE7N82W3+aqpzuUdBbfhWcy/FZR3/4IgflMgKLOsvPDrGCJA==",
      "deprecated": "This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.",
      "license": "ISC",
      "dependencies": {
        "once": "^1.3.0",
        "wrappy": "1"
      }
    },
    "node_modules/inherits": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/inherits/-/inherits-2.0.4.tgz",
      "integrity": "sha512-k/vGaX4/Yla3WzyMCvTQOXYeIHvqOKtnqBduzTHpzpQZzAskKMhZ2K+EnBiSM9zGSoIFeMpXKxa4dYeZIQqewQ==",
      "license": "ISC"
    },
    "node_modules/inversify": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/inversify/-/inversify-6.0.1.tgz",
      "integrity": "sha512-B3ex30927698TJENHR++8FfEaJGqoWOgI6ZY5Ht/nLUsFCwHn6akbwtnUAPCgUepAnTpe2qHxhDNjoKLyz6rgQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/ipaddr.js": {
      "version": "1.9.1",
      "resolved": "https://registry.npmjs.org/ipaddr.js/-/ipaddr.js-1.9.1.tgz",
      "integrity": "sha512-0KI/607xoxSToH7GjN1FfSbLoU0+btTicjsQSWQlh/hZykN8KpmMf7uYwPW3R+akZ6R/w18ZlXSHBYXiYUPO3g==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.10"
      }
    },
    "node_modules/is-arguments": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/is-arguments/-/is-arguments-1.2.0.tgz",
      "integrity": "sha512-7bVbi0huj/wrIAOzb8U1aszg9kdi3KN/CyU19CTI7tAoZYEZoL9yCDXpbXN+uPsuWnP02cyug1gleqq+TU+YCA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.2",
        "has-tostringtag": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-binary-path": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/is-binary-path/-/is-binary-path-2.1.0.tgz",
      "integrity": "sha512-ZMERYes6pDydyuGidse7OsHxtbI7WVeUEozgR/g7rd0xUimYNlvZRE/K2MgZTjWy725IfelLeVcEM97mmtRGXw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "binary-extensions": "^2.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/is-buffer": {
      "version": "1.1.6",
      "resolved": "https://registry.npmjs.org/is-buffer/-/is-buffer-1.1.6.tgz",
      "integrity": "sha512-NcdALwpXkTm5Zvvbk7owOUSvVvBKDgKP5/ewfXEznmQFfs4ZRmanOeKBTjRVjka3QFoN6XJ+9F3USqfHqTaU5w==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/is-callable": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/is-callable/-/is-callable-1.2.7.tgz",
      "integrity": "sha512-1BC0BVFhS/p0qtw6enp8e+8OD0UrK0oFLztSjNzhcKA3WDuJxxAPXzPuPtKkjEY9UUoEWlX/8fgKeu2S8i9JTA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-core-module": {
      "version": "2.16.1",
      "resolved": "https://registry.npmjs.org/is-core-module/-/is-core-module-2.16.1.tgz",
      "integrity": "sha512-UfoeMA6fIJ8wTYFEUjelnaGI67v6+N7qXJEvQuIGa99l4xsCruSYOVSQ0uPANn4dAzm8lkYPaKLrrijLq7x23w==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "hasown": "^2.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-extglob": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/is-extglob/-/is-extglob-2.1.1.tgz",
      "integrity": "sha512-SbKbANkN603Vi4jEZv49LeVJMn4yGwsbzZworEoyEiutsN3nJYdbO36zfhGJ6QEDpOZIFkDtnq5JRxmvl3jsoQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/is-fullwidth-code-point": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/is-fullwidth-code-point/-/is-fullwidth-code-point-3.0.0.tgz",
      "integrity": "sha512-zymm5+u+sCsSWyD9qNaejV3DFvhCKclKdizYaJUuHA83RLjb7nSuGnddCHGv0hk+KY7BMAlsWeK4Ueg6EV6XQg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/is-generator-function": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/is-generator-function/-/is-generator-function-1.1.2.tgz",
      "integrity": "sha512-upqt1SkGkODW9tsGNG5mtXTXtECizwtS2kA161M+gJPc1xdb/Ax629af6YrTwcOeQHbewrPNlE5Dx7kzvXTizA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.4",
        "generator-function": "^2.0.0",
        "get-proto": "^1.0.1",
        "has-tostringtag": "^1.0.2",
        "safe-regex-test": "^1.1.0"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-glob": {
      "version": "4.0.3",
      "resolved": "https://registry.npmjs.org/is-glob/-/is-glob-4.0.3.tgz",
      "integrity": "sha512-xelSayHH36ZgE7ZWhli7pW34hNbNl8Ojv5KVmkJD4hBdD3th8Tfk9vYasLM+mXWOZhFkgZfxhLSnrwRr4elSSg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "is-extglob": "^2.1.1"
      },
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/is-nan": {
      "version": "1.3.2",
      "resolved": "https://registry.npmjs.org/is-nan/-/is-nan-1.3.2.tgz",
      "integrity": "sha512-E+zBKpQ2t6MEo1VsonYmluk9NxGrbzpeeLC2xIViuO2EjU2xsXsBPwTr3Ykv9l08UYEVEdWeRZNouaZqF6RN0w==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bind": "^1.0.0",
        "define-properties": "^1.1.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-number": {
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/is-number/-/is-number-7.0.0.tgz",
      "integrity": "sha512-41Cifkg6e8TylSpdtTpeLVMqvSBEVzTttHvERD741+pnZ8ANv0004MRL43QKPDlK9cGvNp6NZWZUBlbGXYxxng==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.12.0"
      }
    },
    "node_modules/is-path-inside": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/is-path-inside/-/is-path-inside-3.0.3.tgz",
      "integrity": "sha512-Fd4gABb+ycGAmKou8eMftCupSir5lRxqf4aD/vd0cD2qc4HL07OjCeuHMr8Ro4CoMaeCKDB0/ECBOVWjTwUvPQ==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/is-promise": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/is-promise/-/is-promise-4.0.0.tgz",
      "integrity": "sha512-hvpoI6korhJMnej285dSg6nu1+e6uxs7zG3BYAm5byqDsgJNWwxzM6z6iZiAgQR4TJ30JmBTOwqZUw3WlyH3AQ==",
      "license": "MIT"
    },
    "node_modules/is-regex": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/is-regex/-/is-regex-1.2.1.tgz",
      "integrity": "sha512-MjYsKHO5O7mCsmRGxWcLWheFqN9DJ/2TmngvjKXihe6efViPqc274+Fx/4fYj/r03+ESvBdTXK0V6tA3rgez1g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.2",
        "gopd": "^1.2.0",
        "has-tostringtag": "^1.0.2",
        "hasown": "^2.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-typed-array": {
      "version": "1.1.15",
      "resolved": "https://registry.npmjs.org/is-typed-array/-/is-typed-array-1.1.15.tgz",
      "integrity": "sha512-p3EcsicXjit7SaskXHs1hA91QxgTw46Fv6EFKKGS5DRFLD8yKnohjF3hxoju94b/OcMZoQukzpPpBE9uLVKzgQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "which-typed-array": "^1.1.16"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/isarray": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/isarray/-/isarray-1.0.0.tgz",
      "integrity": "sha512-VLghIWNM6ELQzo7zwmcg0NmTVyWKYjvIeM83yjp0wRDTmUnrM678fQbcKBo6n2CJEF0szoG//ytg+TKla89ALQ==",
      "license": "MIT"
    },
    "node_modules/isexe": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/isexe/-/isexe-2.0.0.tgz",
      "integrity": "sha512-RHxMLp9lnKHGHRng9QFhRCMbYAcVpn69smSGcq3f36xjgVVWThj4qqLbTLlq7Ssj8B+fIQ1EuCEGI2lKsyQeIw==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/jackspeak": {
      "version": "3.4.3",
      "resolved": "https://registry.npmjs.org/jackspeak/-/jackspeak-3.4.3.tgz",
      "integrity": "sha512-OGlZQpz2yfahA/Rd1Y8Cd9SIEsqvXkLVoSw/cgwhnhFMDbsQFeZYoJJ7bIZBS9BcamUW96asq/npPWugM+RQBw==",
      "dev": true,
      "license": "BlueOak-1.0.0",
      "dependencies": {
        "@isaacs/cliui": "^8.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      },
      "optionalDependencies": {
        "@pkgjs/parseargs": "^0.11.0"
      }
    },
    "node_modules/javascript-obfuscator": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/javascript-obfuscator/-/javascript-obfuscator-4.1.1.tgz",
      "integrity": "sha512-gt+KZpIIrrxXHEQGD8xZrL8mTRwRY0U76/xz/YX0gZdPrSqQhT/c7dYLASlLlecT3r+FxE7je/+C0oLnTDCx4A==",
      "dev": true,
      "hasInstallScript": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "@javascript-obfuscator/escodegen": "2.3.0",
        "@javascript-obfuscator/estraverse": "5.4.0",
        "acorn": "8.8.2",
        "assert": "2.0.0",
        "chalk": "4.1.2",
        "chance": "1.1.9",
        "class-validator": "0.14.1",
        "commander": "10.0.0",
        "eslint-scope": "7.1.1",
        "eslint-visitor-keys": "3.3.0",
        "fast-deep-equal": "3.1.3",
        "inversify": "6.0.1",
        "js-string-escape": "1.0.1",
        "md5": "2.3.0",
        "mkdirp": "2.1.3",
        "multimatch": "5.0.0",
        "opencollective-postinstall": "2.0.3",
        "process": "0.11.10",
        "reflect-metadata": "0.1.13",
        "source-map-support": "0.5.21",
        "string-template": "1.0.0",
        "stringz": "2.1.0",
        "tslib": "2.5.0"
      },
      "bin": {
        "javascript-obfuscator": "bin/javascript-obfuscator"
      },
      "engines": {
        "node": ">=12.22.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/javascript-obfuscator"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/acorn": {
      "version": "8.8.2",
      "resolved": "https://registry.npmjs.org/acorn/-/acorn-8.8.2.tgz",
      "integrity": "sha512-xjIYgE8HBrkpd/sJqOGNspf8uHG+NOHGOw6a/Urj8taM2EXfdNAH2oFcPeIFfsv3+kz/mJrS5VuMqbNLjCa2vw==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "acorn": "bin/acorn"
      },
      "engines": {
        "node": ">=0.4.0"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/commander": {
      "version": "10.0.0",
      "resolved": "https://registry.npmjs.org/commander/-/commander-10.0.0.tgz",
      "integrity": "sha512-zS5PnTI22FIRM6ylNW8G4Ap0IEOyk62fhLSD0+uHRT9McRCLGpkVNvao4bjimpK/GShynyQkFFxHhwMcETmduA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=14"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/eslint-scope": {
      "version": "7.1.1",
      "resolved": "https://registry.npmjs.org/eslint-scope/-/eslint-scope-7.1.1.tgz",
      "integrity": "sha512-QKQM/UXpIiHcLqJ5AOyIW7XZmzjkzQXYE54n1++wb0u9V/abW3l9uQnxX8Z5Xd18xyKIMTUAyQ0k1e8pz6LUrw==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "esrecurse": "^4.3.0",
        "estraverse": "^5.2.0"
      },
      "engines": {
        "node": "^12.22.0 || ^14.17.0 || >=16.0.0"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/eslint-visitor-keys": {
      "version": "3.3.0",
      "resolved": "https://registry.npmjs.org/eslint-visitor-keys/-/eslint-visitor-keys-3.3.0.tgz",
      "integrity": "sha512-mQ+suqKJVyeuwGYHAdjMFqjCyfl8+Ldnxuyp3ldiMBFKkvytrXUZWaiPCEav8qDHKty44bD+qV1IP4T+w+xXRA==",
      "dev": true,
      "license": "Apache-2.0",
      "engines": {
        "node": "^12.22.0 || ^14.17.0 || >=16.0.0"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/mkdirp": {
      "version": "2.1.3",
      "resolved": "https://registry.npmjs.org/mkdirp/-/mkdirp-2.1.3.tgz",
      "integrity": "sha512-sjAkg21peAG9HS+Dkx7hlG9Ztx7HLeKnvB3NQRcu/mltCVmvkF0pisbiTSfDVYTT86XEfZrTUosLdZLStquZUw==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "mkdirp": "dist/cjs/src/bin.js"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/javascript-obfuscator/node_modules/tslib": {
      "version": "2.5.0",
      "resolved": "https://registry.npmjs.org/tslib/-/tslib-2.5.0.tgz",
      "integrity": "sha512-336iVw3rtn2BUK7ORdIAHTyxHGRIHVReokCR3XjbckJMK7ms8FysBfhLR8IXnAgy7T0PTPNBWKiH514FOW/WSg==",
      "dev": true,
      "license": "0BSD"
    },
    "node_modules/jiti": {
      "version": "1.21.7",
      "resolved": "https://registry.npmjs.org/jiti/-/jiti-1.21.7.tgz",
      "integrity": "sha512-/imKNG4EbWNrVjoNC/1H5/9GFy+tqjGBHCaSsN+P2RnPqjsLmv6UD3Ej+Kj8nBWaRAwyk7kK5ZUc+OEatnTR3A==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "jiti": "bin/jiti.js"
      }
    },
    "node_modules/js-string-escape": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/js-string-escape/-/js-string-escape-1.0.1.tgz",
      "integrity": "sha512-Smw4xcfIQ5LVjAOuJCvN/zIodzA/BBSsluuoSykP+lUvScIi4U6RJLfwHet5cxFnCswUjISV8oAXaqaJDY3chg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/js-tokens": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/js-tokens/-/js-tokens-4.0.0.tgz",
      "integrity": "sha512-RdJUflcE3cUzKiMqQgsCu06FPu9UdIJO0beYbPhHN4k6apgJtifcoCtT9bcxOpYBtpD2kCM6Sbzg4CausW/PKQ==",
      "license": "MIT"
    },
    "node_modules/js-yaml": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/js-yaml/-/js-yaml-4.1.1.tgz",
      "integrity": "sha512-qQKT4zQxXl8lLwBtHMWwaTcGfFOZviOJet3Oy/xmGk2gZH677CJM9EvtfdSkgWcATZhj/55JZ0rmy3myCT5lsA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "argparse": "^2.0.1"
      },
      "bin": {
        "js-yaml": "bin/js-yaml.js"
      }
    },
    "node_modules/json-buffer": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/json-buffer/-/json-buffer-3.0.1.tgz",
      "integrity": "sha512-4bV5BfR2mqfQTJm+V5tPPdf+ZpuhiIvTuAB5g8kcrXOZpTT/QwwVRWBywX1ozr6lEuPdbHxwaJlm9G6mI2sfSQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/json-schema-traverse": {
      "version": "0.4.1",
      "resolved": "https://registry.npmjs.org/json-schema-traverse/-/json-schema-traverse-0.4.1.tgz",
      "integrity": "sha512-xbbCH5dCYU5T8LcEhhuh7HJ88HXuW3qsI3Y0zOZFKfZEHcpWiHU/Jxzk629Brsab/mMiHQti9wMP+845RPe3Vg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/json-stable-stringify-without-jsonify": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/json-stable-stringify-without-jsonify/-/json-stable-stringify-without-jsonify-1.0.1.tgz",
      "integrity": "sha512-Bdboy+l7tA3OGW6FjyFHWkP5LuByj1Tk33Ljyq0axyzdk9//JSi2u3fP1QSmd1KNwq6VOKYGlAu87CisVir6Pw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/jszip": {
      "version": "3.10.1",
      "resolved": "https://registry.npmjs.org/jszip/-/jszip-3.10.1.tgz",
      "integrity": "sha512-xXDvecyTpGLrqFrvkrUSoxxfJI5AH7U8zxxtVclpsUtMCq4JQ290LY8AW5c7Ggnr/Y/oK+bQMbqK2qmtk3pN4g==",
      "license": "(MIT OR GPL-3.0-or-later)",
      "dependencies": {
        "lie": "~3.3.0",
        "pako": "~1.0.2",
        "readable-stream": "~2.3.6",
        "setimmediate": "^1.0.5"
      }
    },
    "node_modules/jszip/node_modules/readable-stream": {
      "version": "2.3.8",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.3.8.tgz",
      "integrity": "sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==",
      "license": "MIT",
      "dependencies": {
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.3",
        "isarray": "~1.0.0",
        "process-nextick-args": "~2.0.0",
        "safe-buffer": "~5.1.1",
        "string_decoder": "~1.1.1",
        "util-deprecate": "~1.0.1"
      }
    },
    "node_modules/jszip/node_modules/safe-buffer": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.1.2.tgz",
      "integrity": "sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==",
      "license": "MIT"
    },
    "node_modules/jszip/node_modules/string_decoder": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.1.1.tgz",
      "integrity": "sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.1.0"
      }
    },
    "node_modules/keyv": {
      "version": "4.5.4",
      "resolved": "https://registry.npmjs.org/keyv/-/keyv-4.5.4.tgz",
      "integrity": "sha512-oxVHkHR/EJf2CNXnWxRLW6mg7JyCCUcG0DtEGmL2ctUo1PNTin1PUil+r/+4r5MpVgC/fn1kjsx7mjSujKqIpw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "json-buffer": "3.0.1"
      }
    },
    "node_modules/lazystream": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/lazystream/-/lazystream-1.0.1.tgz",
      "integrity": "sha512-b94GiNHQNy6JNTrt5w6zNyffMrNkXZb3KTkCZJb2V1xaEGCk093vkZ2jk3tpaeP33/OiXC+WvK9AxUebnf5nbw==",
      "license": "MIT",
      "dependencies": {
        "readable-stream": "^2.0.5"
      },
      "engines": {
        "node": ">= 0.6.3"
      }
    },
    "node_modules/lazystream/node_modules/readable-stream": {
      "version": "2.3.8",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.3.8.tgz",
      "integrity": "sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==",
      "license": "MIT",
      "dependencies": {
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.3",
        "isarray": "~1.0.0",
        "process-nextick-args": "~2.0.0",
        "safe-buffer": "~5.1.1",
        "string_decoder": "~1.1.1",
        "util-deprecate": "~1.0.1"
      }
    },
    "node_modules/lazystream/node_modules/safe-buffer": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.1.2.tgz",
      "integrity": "sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==",
      "license": "MIT"
    },
    "node_modules/lazystream/node_modules/string_decoder": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.1.1.tgz",
      "integrity": "sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.1.0"
      }
    },
    "node_modules/levn": {
      "version": "0.4.1",
      "resolved": "https://registry.npmjs.org/levn/-/levn-0.4.1.tgz",
      "integrity": "sha512-+bT2uH4E5LGE7h/n3evcS/sQlJXCpIp6ym8OWJ5eV6+67Dsql/LaaT7qJBAt2rzfoa/5QBGBhxDix1dMt2kQKQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "prelude-ls": "^1.2.1",
        "type-check": "~0.4.0"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/libphonenumber-js": {
      "version": "1.12.26",
      "resolved": "https://registry.npmjs.org/libphonenumber-js/-/libphonenumber-js-1.12.26.tgz",
      "integrity": "sha512-MagMOuqEXB2Pa90cWE+BoCmcKJx+de5uBIicaUkQ+uiEslZ0OBMNOkSZT/36syXNHu68UeayTxPm3DYM2IHoLQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/lie": {
      "version": "3.3.0",
      "resolved": "https://registry.npmjs.org/lie/-/lie-3.3.0.tgz",
      "integrity": "sha512-UaiMJzeWRlEujzAuw5LokY1L5ecNQYZKfmyZ9L7wDHb/p5etKaxXhohBcrw0EYby+G/NA52vRSN4N39dxHAIwQ==",
      "license": "MIT",
      "dependencies": {
        "immediate": "~3.0.5"
      }
    },
    "node_modules/lilconfig": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/lilconfig/-/lilconfig-3.1.3.tgz",
      "integrity": "sha512-/vlFKAoH5Cgt3Ie+JLhRbwOsCQePABiU3tJ1egGvyQ+33R/vcwM2Zl2QR/LzjsBeItPt3oSVXapn+m4nQDvpzw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=14"
      },
      "funding": {
        "url": "https://github.com/sponsors/antonk52"
      }
    },
    "node_modules/lines-and-columns": {
      "version": "1.2.4",
      "resolved": "https://registry.npmjs.org/lines-and-columns/-/lines-and-columns-1.2.4.tgz",
      "integrity": "sha512-7ylylesZQ/PV29jhEDl3Ufjo6ZX7gCqJr5F7PKrqc93v7fzSymt1BpwEU8nAUXs8qzzvqhbjhK5QZg6Mt/HkBg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/listenercount": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/listenercount/-/listenercount-1.0.1.tgz",
      "integrity": "sha512-3mk/Zag0+IJxeDrxSgaDPy4zZ3w05PRZeJNnlWhzFz5OkX49J4krc+A8X2d2M69vGMBEX0uyl8M+W+8gH+kBqQ==",
      "license": "ISC"
    },
    "node_modules/locate-path": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/locate-path/-/locate-path-6.0.0.tgz",
      "integrity": "sha512-iPZK6eYjbxRu3uB4/WZ3EsEIMJFMqAoopl3R+zuq0UjcAm/MO6KCweDgPfP3elTztoKP3KtnVHxTn2NHBSDVUw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "p-locate": "^5.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/lodash.defaults": {
      "version": "4.2.0",
      "resolved": "https://registry.npmjs.org/lodash.defaults/-/lodash.defaults-4.2.0.tgz",
      "integrity": "sha512-qjxPLHd3r5DnsdGacqOMU6pb/avJzdh9tFX2ymgoZE27BmjXrNy/y4LoaiTeAb+O3gL8AfpJGtqfX/ae2leYYQ==",
      "license": "MIT"
    },
    "node_modules/lodash.difference": {
      "version": "4.5.0",
      "resolved": "https://registry.npmjs.org/lodash.difference/-/lodash.difference-4.5.0.tgz",
      "integrity": "sha512-dS2j+W26TQ7taQBGN8Lbbq04ssV3emRw4NY58WErlTO29pIqS0HmoT5aJ9+TUQ1N3G+JOZSji4eugsWwGp9yPA==",
      "license": "MIT"
    },
    "node_modules/lodash.escaperegexp": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/lodash.escaperegexp/-/lodash.escaperegexp-4.1.2.tgz",
      "integrity": "sha512-TM9YBvyC84ZxE3rgfefxUWiQKLilstD6k7PTGt6wfbtXF8ixIJLOL3VYyV/z+ZiPLsVxAsKAFVwWlWeb2Y8Yyw==",
      "license": "MIT"
    },
    "node_modules/lodash.flatten": {
      "version": "4.4.0",
      "resolved": "https://registry.npmjs.org/lodash.flatten/-/lodash.flatten-4.4.0.tgz",
      "integrity": "sha512-C5N2Z3DgnnKr0LOpv/hKCgKdb7ZZwafIrsesve6lmzvZIRZRGaZ/l6Q8+2W7NaT+ZwO3fFlSCzCzrDCFdJfZ4g==",
      "license": "MIT"
    },
    "node_modules/lodash.groupby": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/lodash.groupby/-/lodash.groupby-4.6.0.tgz",
      "integrity": "sha512-5dcWxm23+VAoz+awKmBaiBvzox8+RqMgFhi7UvX9DHZr2HdxHXM/Wrf8cfKpsW37RNrvtPn6hSwNqurSILbmJw==",
      "license": "MIT"
    },
    "node_modules/lodash.isboolean": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/lodash.isboolean/-/lodash.isboolean-3.0.3.tgz",
      "integrity": "sha512-Bz5mupy2SVbPHURB98VAcw+aHh4vRV5IPNhILUCsOzRmsTmSQ17jIuqopAentWoehktxGd9e/hbIXq980/1QJg==",
      "license": "MIT"
    },
    "node_modules/lodash.isequal": {
      "version": "4.5.0",
      "resolved": "https://registry.npmjs.org/lodash.isequal/-/lodash.isequal-4.5.0.tgz",
      "integrity": "sha512-pDo3lu8Jhfjqls6GkMgpahsF9kCyayhgykjyLMNFTKWrpVdAQtYyB4muAMWozBB4ig/dtWAmsMxLEI8wuz+DYQ==",
      "deprecated": "This package is deprecated. Use require('node:util').isDeepStrictEqual instead.",
      "license": "MIT"
    },
    "node_modules/lodash.isfunction": {
      "version": "3.0.9",
      "resolved": "https://registry.npmjs.org/lodash.isfunction/-/lodash.isfunction-3.0.9.tgz",
      "integrity": "sha512-AirXNj15uRIMMPihnkInB4i3NHeb4iBtNg9WRWuK2o31S+ePwwNmDPaTL3o7dTJ+VXNZim7rFs4rxN4YU1oUJw==",
      "license": "MIT"
    },
    "node_modules/lodash.isnil": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/lodash.isnil/-/lodash.isnil-4.0.0.tgz",
      "integrity": "sha512-up2Mzq3545mwVnMhTDMdfoG1OurpA/s5t88JmQX809eH3C8491iu2sfKhTfhQtKY78oPNhiaHJUpT/dUDAAtng==",
      "license": "MIT"
    },
    "node_modules/lodash.isplainobject": {
      "version": "4.0.6",
      "resolved": "https://registry.npmjs.org/lodash.isplainobject/-/lodash.isplainobject-4.0.6.tgz",
      "integrity": "sha512-oSXzaWypCMHkPC3NvBEaPHf0KsA5mvPrOPgQWDsbg8n7orZ290M0BmC/jgRZ4vcJ6DTAhjrsSYgdsW/F+MFOBA==",
      "license": "MIT"
    },
    "node_modules/lodash.isundefined": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/lodash.isundefined/-/lodash.isundefined-3.0.1.tgz",
      "integrity": "sha512-MXB1is3s899/cD8jheYYE2V9qTHwKvt+npCwpD+1Sxm3Q3cECXCiYHjeHWXNwr6Q0SOBPrYUDxendrO6goVTEA==",
      "license": "MIT"
    },
    "node_modules/lodash.merge": {
      "version": "4.6.2",
      "resolved": "https://registry.npmjs.org/lodash.merge/-/lodash.merge-4.6.2.tgz",
      "integrity": "sha512-0KpjqXRVvrYyCsX1swR/XTK0va6VQkQM6MNo7PqW77ByjAhoARA8EfrP1N4+KlKj8YS0ZUCtRT/YUuhyYDujIQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/lodash.union": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/lodash.union/-/lodash.union-4.6.0.tgz",
      "integrity": "sha512-c4pB2CdGrGdjMKYLA+XiRDO7Y0PRQbm/Gzg8qMj+QH+pFVAoTp5sBpO0odL3FjoPCGjK96p6qsP+yQoiLoOBcw==",
      "license": "MIT"
    },
    "node_modules/lodash.uniq": {
      "version": "4.5.0",
      "resolved": "https://registry.npmjs.org/lodash.uniq/-/lodash.uniq-4.5.0.tgz",
      "integrity": "sha512-xfBaXQd9ryd9dlSDvnvI0lvxfLJlYAZzXomUYzLKtUeOQvOP5piqAWuGtrhWeqaXK9hhoM/iyJc5AV+XfsX3HQ==",
      "license": "MIT"
    },
    "node_modules/loose-envify": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/loose-envify/-/loose-envify-1.4.0.tgz",
      "integrity": "sha512-lyuxPGr/Wfhrlem2CL/UcnUc1zcqKAImBDzukY7Y5F/yQiNdko6+fRLevlw1HgMySw7f611UIY408EtxRSoK3Q==",
      "license": "MIT",
      "dependencies": {
        "js-tokens": "^3.0.0 || ^4.0.0"
      },
      "bin": {
        "loose-envify": "cli.js"
      }
    },
    "node_modules/lru-cache": {
      "version": "10.4.3",
      "resolved": "https://registry.npmjs.org/lru-cache/-/lru-cache-10.4.3.tgz",
      "integrity": "sha512-JNAzZcXrCt42VGLuYz0zfAzDfAvJWW6AfYlDBQyDV5DClI2m5sAmK+OIO7s59XfsRsWHp02jAJrRadPRGTt6SQ==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/lucide-react": {
      "version": "0.540.0",
      "resolved": "https://registry.npmjs.org/lucide-react/-/lucide-react-0.540.0.tgz",
      "integrity": "sha512-armkCAqQvO62EIX4Hq7hqX/q11WSZu0Jd23cnnqx0/49yIxGXyL/zyZfBxNN9YDx0ensPTb4L+DjTh3yQXUxtQ==",
      "license": "ISC",
      "peerDependencies": {
        "react": "^16.5.1 || ^17.0.0 || ^18.0.0 || ^19.0.0"
      }
    },
    "node_modules/math-intrinsics": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/math-intrinsics/-/math-intrinsics-1.1.0.tgz",
      "integrity": "sha512-/IXtbwEk5HTPyEwyKX6hGkYXxM9nbj64B+ilVJnC/R6B0pH5G4V3b0pVbL7DBj4tkhBAppbQUlf6F6Xl9LHu1g==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/md5": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/md5/-/md5-2.3.0.tgz",
      "integrity": "sha512-T1GITYmFaKuO91vxyoQMFETst+O71VUPEU3ze5GNzDm0OWdP8v1ziTaAEPUr/3kLsY3Sftgz242A1SetQiDL7g==",
      "dev": true,
      "license": "BSD-3-Clause",
      "dependencies": {
        "charenc": "0.0.2",
        "crypt": "0.0.2",
        "is-buffer": "~1.1.6"
      }
    },
    "node_modules/media-typer": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/media-typer/-/media-typer-1.1.0.tgz",
      "integrity": "sha512-aisnrDP4GNe06UcKFnV5bfMNPBUw4jsLGaWwWfnH3v02GnBuXX2MCVn5RbrWo0j3pczUilYblq7fQ7Nw2t5XKw==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/merge-descriptors": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/merge-descriptors/-/merge-descriptors-2.0.0.tgz",
      "integrity": "sha512-Snk314V5ayFLhp3fkUREub6WtjBfPdCPY1Ln8/8munuLuiYhsABgBVWsozAG+MWMbVEvcdcpbi9R7ww22l9Q3g==",
      "license": "MIT",
      "engines": {
        "node": ">=18"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/merge2": {
      "version": "1.4.1",
      "resolved": "https://registry.npmjs.org/merge2/-/merge2-1.4.1.tgz",
      "integrity": "sha512-8q7VEgMJW4J8tcfVPy8g09NcQwZdbwFEqhe/WZkoIzjn/3TGDwtOCYtXGxA3O8tPzpczCCDgv+P2P5y00ZJOOg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/micromatch": {
      "version": "4.0.8",
      "resolved": "https://registry.npmjs.org/micromatch/-/micromatch-4.0.8.tgz",
      "integrity": "sha512-PXwfBhYu0hBCPw8Dn0E+WDYb7af3dSLVWKi3HGv84IdF4TyFoC0ysxFd0Goxw7nSv4T/PzEJQxsYsEiFCKo2BA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "braces": "^3.0.3",
        "picomatch": "^2.3.1"
      },
      "engines": {
        "node": ">=8.6"
      }
    },
    "node_modules/mime-db": {
      "version": "1.54.0",
      "resolved": "https://registry.npmjs.org/mime-db/-/mime-db-1.54.0.tgz",
      "integrity": "sha512-aU5EJuIN2WDemCcAp2vFBfp/m4EAhWJnUNSSw0ixs7/kXbd6Pg64EmwJkNdFhB8aWt1sH2CTXrLxo/iAGV3oPQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/mime-types": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/mime-types/-/mime-types-3.0.1.tgz",
      "integrity": "sha512-xRc4oEhT6eaBpU1XF7AjpOFD+xQmXNB5OVKwp4tqCuBpHLS/ZbBDrc07mYTDqVMg6PfxUjjNp85O6Cd2Z/5HWA==",
      "license": "MIT",
      "dependencies": {
        "mime-db": "^1.54.0"
      },
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/minimatch": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-3.1.2.tgz",
      "integrity": "sha512-J7p63hRiAjw1NDEww1W7i37+ByIrOWO5XQQAzZ3VOcL0PNybwpfmV/N05zFAzwQ9USyEcX6t3UO+K5aqBQOIHw==",
      "license": "ISC",
      "dependencies": {
        "brace-expansion": "^1.1.7"
      },
      "engines": {
        "node": "*"
      }
    },
    "node_modules/minimist": {
      "version": "1.2.8",
      "resolved": "https://registry.npmjs.org/minimist/-/minimist-1.2.8.tgz",
      "integrity": "sha512-2yyAR8qBkN3YuheJanUpWC5U3bb5osDywNB8RzDVlDwDHbocAJveqqj1u8+SVD7jkWT4yvsHCpWqqWqAxb0zCA==",
      "license": "MIT",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/minipass": {
      "version": "7.1.2",
      "resolved": "https://registry.npmjs.org/minipass/-/minipass-7.1.2.tgz",
      "integrity": "sha512-qOOzS1cBTWYF4BH8fVePDBOO9iptMnGUEZwNc/cMWnTV2nVLZ7VoNWEPHkYczZA0pdoA7dl6e7FL659nX9S2aw==",
      "dev": true,
      "license": "ISC",
      "engines": {
        "node": ">=16 || 14 >=14.17"
      }
    },
    "node_modules/mkdirp": {
      "version": "0.5.6",
      "resolved": "https://registry.npmjs.org/mkdirp/-/mkdirp-0.5.6.tgz",
      "integrity": "sha512-FP+p8RB8OWpF3YZBCrP5gtADmtXApB5AMLn+vdyA+PyxCjrCs00mjyUozssO33cwDeT3wNGdLxJ5M//YqtHAJw==",
      "license": "MIT",
      "dependencies": {
        "minimist": "^1.2.6"
      },
      "bin": {
        "mkdirp": "bin/cmd.js"
      }
    },
    "node_modules/motion-dom": {
      "version": "12.23.23",
      "resolved": "https://registry.npmjs.org/motion-dom/-/motion-dom-12.23.23.tgz",
      "integrity": "sha512-n5yolOs0TQQBRUFImrRfs/+6X4p3Q4n1dUEqt/H58Vx7OW6RF+foWEgmTVDhIWJIMXOuNNL0apKH2S16en9eiA==",
      "license": "MIT",
      "dependencies": {
        "motion-utils": "^12.23.6"
      }
    },
    "node_modules/motion-utils": {
      "version": "12.23.6",
      "resolved": "https://registry.npmjs.org/motion-utils/-/motion-utils-12.23.6.tgz",
      "integrity": "sha512-eAWoPgr4eFEOFfg2WjIsMoqJTW6Z8MTUCgn/GZ3VRpClWBdnbjryiA3ZSNLyxCTmCQx4RmYX6jX1iWHbenUPNQ==",
      "license": "MIT"
    },
    "node_modules/ms": {
      "version": "2.1.3",
      "resolved": "https://registry.npmjs.org/ms/-/ms-2.1.3.tgz",
      "integrity": "sha512-6FlzubTLZG3J2a/NVCAleEhjzq5oxgHyaCU9yYXvcLsvoVaHJq/s5xXI6/XXP6tz7R9xAOtHnSO/tXtF3WRTlA==",
      "license": "MIT"
    },
    "node_modules/multer": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/multer/-/multer-2.0.2.tgz",
      "integrity": "sha512-u7f2xaZ/UG8oLXHvtF/oWTRvT44p9ecwBBqTwgJVq0+4BW1g8OW01TyMEGWBHbyMOYVHXslaut7qEQ1meATXgw==",
      "license": "MIT",
      "dependencies": {
        "append-field": "^1.0.0",
        "busboy": "^1.6.0",
        "concat-stream": "^2.0.0",
        "mkdirp": "^0.5.6",
        "object-assign": "^4.1.1",
        "type-is": "^1.6.18",
        "xtend": "^4.0.2"
      },
      "engines": {
        "node": ">= 10.16.0"
      }
    },
    "node_modules/multer/node_modules/media-typer": {
      "version": "0.3.0",
      "resolved": "https://registry.npmjs.org/media-typer/-/media-typer-0.3.0.tgz",
      "integrity": "sha512-dq+qelQ9akHpcOl/gUVRTxVIOkAJ1wR3QAvb4RsVjS8oVoFjDGTc679wJYmUmknUF5HwMLOgb5O+a3KxfWapPQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/multer/node_modules/mime-db": {
      "version": "1.52.0",
      "resolved": "https://registry.npmjs.org/mime-db/-/mime-db-1.52.0.tgz",
      "integrity": "sha512-sPU4uV7dYlvtWJxwwxHD0PuihVNiE7TyAbQ5SWxDCB9mUYvOgroQOwYQQOKPJ8CIbE+1ETVlOoK1UC2nU3gYvg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/multer/node_modules/mime-types": {
      "version": "2.1.35",
      "resolved": "https://registry.npmjs.org/mime-types/-/mime-types-2.1.35.tgz",
      "integrity": "sha512-ZDY+bPm5zTTF+YpCrAU9nK0UgICYPT0QtT1NZWFv4s++TNkcgVaT0g6+4R2uI4MjQjzysHB1zxuWL50hzaeXiw==",
      "license": "MIT",
      "dependencies": {
        "mime-db": "1.52.0"
      },
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/multer/node_modules/type-is": {
      "version": "1.6.18",
      "resolved": "https://registry.npmjs.org/type-is/-/type-is-1.6.18.tgz",
      "integrity": "sha512-TkRKr9sUTxEH8MdfuCSP7VizJyzRNMjj2J2do2Jr3Kym598JVdEksuzPQCnlFPW4ky9Q+iA+ma9BGm06XQBy8g==",
      "license": "MIT",
      "dependencies": {
        "media-typer": "0.3.0",
        "mime-types": "~2.1.24"
      },
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/multimatch": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/multimatch/-/multimatch-5.0.0.tgz",
      "integrity": "sha512-ypMKuglUrZUD99Tk2bUQ+xNQj43lPEfAeX2o9cTteAmShXy2VHDJpuwu1o0xqoKCt9jLVAvwyFKdLTPXKAfJyA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/minimatch": "^3.0.3",
        "array-differ": "^3.0.0",
        "array-union": "^2.1.0",
        "arrify": "^2.0.1",
        "minimatch": "^3.0.4"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/mz": {
      "version": "2.7.0",
      "resolved": "https://registry.npmjs.org/mz/-/mz-2.7.0.tgz",
      "integrity": "sha512-z81GNO7nnYMEhrGh9LeymoE4+Yr0Wn5McHIZMK5cfQCl+NDX08sCZgUc9/6MHni9IWuFLm1Z3HTCXu2z9fN62Q==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "any-promise": "^1.0.0",
        "object-assign": "^4.0.1",
        "thenify-all": "^1.0.0"
      }
    },
    "node_modules/nanoid": {
      "version": "3.3.11",
      "resolved": "https://registry.npmjs.org/nanoid/-/nanoid-3.3.11.tgz",
      "integrity": "sha512-N8SpfPUnUp1bK+PMYW8qSWdl9U+wwNWI4QKxOYDy9JAro3WMX7p2OeVRF9v+347pnakNevPmiHhNmZ2HbFA76w==",
      "dev": true,
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "bin": {
        "nanoid": "bin/nanoid.cjs"
      },
      "engines": {
        "node": "^10 || ^12 || ^13.7 || ^14 || >=15.0.1"
      }
    },
    "node_modules/natural-compare": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/natural-compare/-/natural-compare-1.4.0.tgz",
      "integrity": "sha512-OWND8ei3VtNC9h7V60qff3SVobHr996CTwgxubgyQYEpg290h9J0buyECNNJexkFm5sOajh5G116RYA1c8ZMSw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/negotiator": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/negotiator/-/negotiator-1.0.0.tgz",
      "integrity": "sha512-8Ofs/AUQh8MaEcrlq5xOX0CQ9ypTF5dl78mjlMNfOK08fzpgTHQRQPBxcPlEtIw0yRpws+Zo/3r+5WRby7u3Gg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/node-fetch-native": {
      "version": "1.6.7",
      "resolved": "https://registry.npmjs.org/node-fetch-native/-/node-fetch-native-1.6.7.tgz",
      "integrity": "sha512-g9yhqoedzIUm0nTnTqAQvueMPVOuIY16bqgAJJC8XOOubYFNwz6IER9qs0Gq2Xd0+CecCKFjtdDTMA4u4xG06Q==",
      "license": "MIT"
    },
    "node_modules/node-releases": {
      "version": "2.0.27",
      "resolved": "https://registry.npmjs.org/node-releases/-/node-releases-2.0.27.tgz",
      "integrity": "sha512-nmh3lCkYZ3grZvqcCH+fjmQ7X+H0OeZgP40OierEaAptX4XofMh5kwNbWh7lBduUzCcV/8kZ+NDLCwm2iorIlA==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/normalize-path": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/normalize-path/-/normalize-path-3.0.0.tgz",
      "integrity": "sha512-6eZs5Ls3WtCisHWp9S2GUy8dqkpGi4BVSz3GaqiE6ezub0512ESztXUwUB6C6IKbQkY2Pnb/mD4WYojCRwcwLA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/normalize-range": {
      "version": "0.1.2",
      "resolved": "https://registry.npmjs.org/normalize-range/-/normalize-range-0.1.2.tgz",
      "integrity": "sha512-bdok/XvKII3nUpklnV6P2hxtMNrCboOjAcyBuQnWEhO665FwrSNRxU+AqpsyvO6LgGYPspN+lu5CLtw4jPRKNA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/object-assign": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/object-assign/-/object-assign-4.1.1.tgz",
      "integrity": "sha512-rJgTQnkUnH1sFw8yT6VSU3zD3sWmu6sZhIseY8VX+GRu3P6F7Fu+JNDoXfklElbLJSnc3FUQHVe4cU5hj+BcUg==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/object-hash": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/object-hash/-/object-hash-3.0.0.tgz",
      "integrity": "sha512-RSn9F68PjH9HqtltsSnqYC1XXoWe9Bju5+213R98cNGttag9q9yAOTzdbsqvIa7aNm5WffBZFpWYr2aWrklWAw==",
      "license": "MIT",
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/object-inspect": {
      "version": "1.13.4",
      "resolved": "https://registry.npmjs.org/object-inspect/-/object-inspect-1.13.4.tgz",
      "integrity": "sha512-W67iLl4J2EXEGTbfeHCffrjDfitvLANg0UlX3wFUUSTx92KXRFegMHUVgSqE+wvhAbi4WqjGg9czysTV2Epbew==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/object-is": {
      "version": "1.1.6",
      "resolved": "https://registry.npmjs.org/object-is/-/object-is-1.1.6.tgz",
      "integrity": "sha512-F8cZ+KfGlSGi09lJT7/Nd6KJZ9ygtvYC0/UYYLI9nmQKLMnydpB9yvbv9K1uSkEu7FU9vYPmVwLg328tX+ot3Q==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bind": "^1.0.7",
        "define-properties": "^1.2.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/object-keys": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/object-keys/-/object-keys-1.1.1.tgz",
      "integrity": "sha512-NuAESUOUMrlIXOfHKzD6bpPu3tYt3xvjNdRIQ+FeT0lNb4K8WR70CaDxhuNguS2XG+GjkyMwOzsN5ZktImfhLA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/ofetch": {
      "version": "1.5.1",
      "resolved": "https://registry.npmjs.org/ofetch/-/ofetch-1.5.1.tgz",
      "integrity": "sha512-2W4oUZlVaqAPAil6FUg/difl6YhqhUR7x2eZY4bQCko22UXg3hptq9KLQdqFClV+Wu85UX7hNtdGTngi/1BxcA==",
      "license": "MIT",
      "dependencies": {
        "destr": "^2.0.5",
        "node-fetch-native": "^1.6.7",
        "ufo": "^1.6.1"
      }
    },
    "node_modules/on-finished": {
      "version": "2.4.1",
      "resolved": "https://registry.npmjs.org/on-finished/-/on-finished-2.4.1.tgz",
      "integrity": "sha512-oVlzkg3ENAhCk2zdv7IJwd/QUD4z2RxRwpkcGY8psCVcCYZNq4wYnVWALHM+brtuJjePWiYF/ClmuDr8Ch5+kg==",
      "license": "MIT",
      "dependencies": {
        "ee-first": "1.1.1"
      },
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/once": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/once/-/once-1.4.0.tgz",
      "integrity": "sha512-lNaJgI+2Q5URQBkccEKHTQOPaXdUxnZZElQTZY0MFUAuaEqe1E+Nyvgdz/aIyNi6Z9MzO5dv1H8n58/GELp3+w==",
      "license": "ISC",
      "dependencies": {
        "wrappy": "1"
      }
    },
    "node_modules/opencollective-postinstall": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/opencollective-postinstall/-/opencollective-postinstall-2.0.3.tgz",
      "integrity": "sha512-8AV/sCtuzUeTo8gQK5qDZzARrulB3egtLzFgteqB2tcT4Mw7B8Kt7JcDHmltjz6FOAHsvTevk70gZEbhM4ZS9Q==",
      "dev": true,
      "license": "MIT",
      "bin": {
        "opencollective-postinstall": "index.js"
      }
    },
    "node_modules/optionator": {
      "version": "0.9.4",
      "resolved": "https://registry.npmjs.org/optionator/-/optionator-0.9.4.tgz",
      "integrity": "sha512-6IpQ7mKUxRcZNLIObR0hz7lxsapSSIYNZJwXPGeF0mTVqGKFIXj1DQcMoT22S3ROcLyY/rz0PWaWZ9ayWmad9g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "deep-is": "^0.1.3",
        "fast-levenshtein": "^2.0.6",
        "levn": "^0.4.1",
        "prelude-ls": "^1.2.1",
        "type-check": "^0.4.0",
        "word-wrap": "^1.2.5"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/p-limit": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-3.1.0.tgz",
      "integrity": "sha512-TYOanM3wGwNGsZN2cVTYPArw454xnXj5qmWF1bEoAc4+cU/ol7GVh7odevjp1FNHduHc3KZMcFduxU5Xc6uJRQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "yocto-queue": "^0.1.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/p-locate": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/p-locate/-/p-locate-5.0.0.tgz",
      "integrity": "sha512-LaNjtRWUBY++zB5nE/NwcaoMylSPk+S+ZHNB1TzdbMJMny6dynpAGt7X/tl/QYq3TIeE6nxHppbo2LGymrG5Pw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "p-limit": "^3.0.2"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/package-json-from-dist": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/package-json-from-dist/-/package-json-from-dist-1.0.1.tgz",
      "integrity": "sha512-UEZIS3/by4OC8vL3P2dTXRETpebLI2NiI5vIrjaD/5UtrkFX/tNbwjTSRAGC/+7CAo2pIcBaRgWmcBBHcsaCIw==",
      "dev": true,
      "license": "BlueOak-1.0.0"
    },
    "node_modules/pako": {
      "version": "1.0.11",
      "resolved": "https://registry.npmjs.org/pako/-/pako-1.0.11.tgz",
      "integrity": "sha512-4hLB8Py4zZce5s4yd9XzopqwVv/yGNhV1Bl8NTmCq1763HeK2+EwVTv+leGeL13Dnh2wfbqowVPXCIO0z4taYw==",
      "license": "(MIT AND Zlib)"
    },
    "node_modules/papaparse": {
      "version": "5.5.3",
      "resolved": "https://registry.npmjs.org/papaparse/-/papaparse-5.5.3.tgz",
      "integrity": "sha512-5QvjGxYVjxO59MGU2lHVYpRWBBtKHnlIAcSe1uNFCkkptUh63NFRj0FJQm7nR67puEruUci/ZkjmEFrjCAyP4A==",
      "license": "MIT"
    },
    "node_modules/parent-module": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/parent-module/-/parent-module-1.0.1.tgz",
      "integrity": "sha512-GQ2EWRpQV8/o+Aw8YqtfZZPfNRWZYkbidE9k5rpl/hC3vtHHBfGm2Ifi6qWV+coDGkrUKZAxE3Lot5kcsRlh+g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "callsites": "^3.0.0"
      },
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/parseurl": {
      "version": "1.3.3",
      "resolved": "https://registry.npmjs.org/parseurl/-/parseurl-1.3.3.tgz",
      "integrity": "sha512-CiyeOxFT/JZyN5m0z9PfXw4SCBJ6Sygz1Dpl0wqjlhDEGGBP1GnsUVEL0p63hoG1fcj3fHynXi9NYO4nWOL+qQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/path-exists": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/path-exists/-/path-exists-4.0.0.tgz",
      "integrity": "sha512-ak9Qy5Q7jYb2Wwcey5Fpvg2KoAc/ZIhLSLOSBmRmygPsGwkVVt0fZa0qrtMz+m6tJTAHfZQ8FnmB4MG4LWy7/w==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/path-is-absolute": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/path-is-absolute/-/path-is-absolute-1.0.1.tgz",
      "integrity": "sha512-AVbw3UJ2e9bq64vSaS9Am0fje1Pa8pbGqTTsmXfaIiMpnr5DlDhfJOuLj9Sf95ZPVDAUerDfEk88MPmPe7UCQg==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/path-key": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/path-key/-/path-key-3.1.1.tgz",
      "integrity": "sha512-ojmeN0qd+y0jszEtoY48r0Peq5dwMEkIlCOu6Q5f41lfkswXuKtYrhgoTpLnyIcHm24Uhqx+5Tqm2InSwLhE6Q==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/path-parse": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/path-parse/-/path-parse-1.0.7.tgz",
      "integrity": "sha512-LDJzPVEEEPR+y48z93A0Ed0yXb8pAByGWo/k5YYdYgpY2/2EsOsksJrq7lOHxryrVOn1ejG6oAp8ahvOIQD8sw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/path-scurry": {
      "version": "1.11.1",
      "resolved": "https://registry.npmjs.org/path-scurry/-/path-scurry-1.11.1.tgz",
      "integrity": "sha512-Xa4Nw17FS9ApQFJ9umLiJS4orGjm7ZzwUrwamcGQuHSzDyth9boKDaycYdDcZDuqYATXw4HFXgaqWTctW/v1HA==",
      "dev": true,
      "license": "BlueOak-1.0.0",
      "dependencies": {
        "lru-cache": "^10.2.0",
        "minipass": "^5.0.0 || ^6.0.2 || ^7.0.0"
      },
      "engines": {
        "node": ">=16 || 14 >=14.18"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/path-to-regexp": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/path-to-regexp/-/path-to-regexp-8.3.0.tgz",
      "integrity": "sha512-7jdwVIRtsP8MYpdXSwOS0YdD0Du+qOoF/AEPIt88PcCFrZCzx41oxku1jD88hZBwbNUIEfpqvuhjFaMAqMTWnA==",
      "license": "MIT",
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/express"
      }
    },
    "node_modules/picocolors": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/picocolors/-/picocolors-1.1.1.tgz",
      "integrity": "sha512-xceH2snhtb5M9liqDsmEw56le376mTZkEX/jEb/RxNFyegNul7eNslCXP9FDj/Lcu0X8KEyMceP2ntpaHrDEVA==",
      "dev": true,
      "license": "ISC"
    },
    "node_modules/picomatch": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/picomatch/-/picomatch-2.3.1.tgz",
      "integrity": "sha512-JU3teHTNjmE2VCGFzuY8EXzCDVwEqB2a8fsIvwaStHhAWJEeVd1o1QD80CU6+ZdEXXSLbSsuLwJjkCBWqRQUVA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8.6"
      },
      "funding": {
        "url": "https://github.com/sponsors/jonschlinkert"
      }
    },
    "node_modules/pify": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/pify/-/pify-2.3.0.tgz",
      "integrity": "sha512-udgsAY+fTnvv7kI7aaxbqwWNb0AHiB0qBO89PZKPkoTmGOgdbrHDKD+0B2X4uTfJ/FT1R09r9gTsjUjNJotuog==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/pirates": {
      "version": "4.0.7",
      "resolved": "https://registry.npmjs.org/pirates/-/pirates-4.0.7.tgz",
      "integrity": "sha512-TfySrs/5nm8fQJDcBDuUng3VOUKsd7S+zqvbOTiGXHfxX4wK31ard+hoNuvkicM/2YFzlpDgABOevKSsB4G/FA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/possible-typed-array-names": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/possible-typed-array-names/-/possible-typed-array-names-1.1.0.tgz",
      "integrity": "sha512-/+5VFTchJDoVj3bhoqi6UeymcD00DAwb1nJwamzPvHEszJ4FpF6SNNbUbOS8yI56qHzdV8eK0qEfOSiodkTdxg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/postcss": {
      "version": "8.5.6",
      "resolved": "https://registry.npmjs.org/postcss/-/postcss-8.5.6.tgz",
      "integrity": "sha512-3Ybi1tAuwAP9s0r1UQ2J4n5Y0G05bJkpUIO0/bI9MhwmD70S5aTWbXGBwxHrelT+XM1k6dM0pk+SwNkpTRN7Pg==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/postcss"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "nanoid": "^3.3.11",
        "picocolors": "^1.1.1",
        "source-map-js": "^1.2.1"
      },
      "engines": {
        "node": "^10 || ^12 || >=14"
      }
    },
    "node_modules/postcss-import": {
      "version": "15.1.0",
      "resolved": "https://registry.npmjs.org/postcss-import/-/postcss-import-15.1.0.tgz",
      "integrity": "sha512-hpr+J05B2FVYUAXHeK1YyI267J/dDDhMU6B6civm8hSY1jYJnBXxzKDKDswzJmtLHryrjhnDjqqp/49t8FALew==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "postcss-value-parser": "^4.0.0",
        "read-cache": "^1.0.0",
        "resolve": "^1.1.7"
      },
      "engines": {
        "node": ">=14.0.0"
      },
      "peerDependencies": {
        "postcss": "^8.0.0"
      }
    },
    "node_modules/postcss-js": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/postcss-js/-/postcss-js-4.1.0.tgz",
      "integrity": "sha512-oIAOTqgIo7q2EOwbhb8UalYePMvYoIeRY2YKntdpFQXNosSu3vLrniGgmH9OKs/qAkfoj5oB3le/7mINW1LCfw==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "camelcase-css": "^2.0.1"
      },
      "engines": {
        "node": "^12 || ^14 || >= 16"
      },
      "peerDependencies": {
        "postcss": "^8.4.21"
      }
    },
    "node_modules/postcss-load-config": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/postcss-load-config/-/postcss-load-config-4.0.2.tgz",
      "integrity": "sha512-bSVhyJGL00wMVoPUzAVAnbEoWyqRxkjv64tUl427SKnPrENtq6hJwUojroMz2VB+Q1edmi4IfrAPpami5VVgMQ==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "lilconfig": "^3.0.0",
        "yaml": "^2.3.4"
      },
      "engines": {
        "node": ">= 14"
      },
      "peerDependencies": {
        "postcss": ">=8.0.9",
        "ts-node": ">=9.0.0"
      },
      "peerDependenciesMeta": {
        "postcss": {
          "optional": true
        },
        "ts-node": {
          "optional": true
        }
      }
    },
    "node_modules/postcss-nested": {
      "version": "6.2.0",
      "resolved": "https://registry.npmjs.org/postcss-nested/-/postcss-nested-6.2.0.tgz",
      "integrity": "sha512-HQbt28KulC5AJzG+cZtj9kvKB93CFCdLvog1WFLf1D+xmMvPGlBstkpTEZfK5+AN9hfJocyBFCNiqyS48bpgzQ==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/postcss/"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "postcss-selector-parser": "^6.1.1"
      },
      "engines": {
        "node": ">=12.0"
      },
      "peerDependencies": {
        "postcss": "^8.2.14"
      }
    },
    "node_modules/postcss-selector-parser": {
      "version": "6.1.2",
      "resolved": "https://registry.npmjs.org/postcss-selector-parser/-/postcss-selector-parser-6.1.2.tgz",
      "integrity": "sha512-Q8qQfPiZ+THO/3ZrOrO0cJJKfpYCagtMUkXbnEfmgUjwXg6z/WBeOyS9APBBPCTSiDV+s4SwQGu8yFsiMRIudg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "cssesc": "^3.0.0",
        "util-deprecate": "^1.0.2"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/postcss-value-parser": {
      "version": "4.2.0",
      "resolved": "https://registry.npmjs.org/postcss-value-parser/-/postcss-value-parser-4.2.0.tgz",
      "integrity": "sha512-1NNCs6uurfkVbeXG4S8JFT9t19m45ICnif8zWLd5oPSZ50QnwMfK+H3jv408d4jw/7Bttv5axS5IiHoLaVNHeQ==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/prelude-ls": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/prelude-ls/-/prelude-ls-1.2.1.tgz",
      "integrity": "sha512-vkcDPrRZo1QZLbn5RLGPpg/WmIQ65qoWWhcGKf/b5eplkkarX0m9z8ppCat4mlOqUsWpyNuYgO3VRyrYHSzX5g==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/process": {
      "version": "0.11.10",
      "resolved": "https://registry.npmjs.org/process/-/process-0.11.10.tgz",
      "integrity": "sha512-cdGef/drWFoydD1JsMzuFf8100nZl+GT+yacc2bEced5f9Rjk4z+WtFUTBu9PhOi9j/jfmBPu0mMEY4wIdAF8A==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.6.0"
      }
    },
    "node_modules/process-nextick-args": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/process-nextick-args/-/process-nextick-args-2.0.1.tgz",
      "integrity": "sha512-3ouUOpQhtgrbOa17J7+uxOTpITYWaGP7/AhoR3+A+/1e9skrzelGi/dXzEYyvbxubEF6Wn2ypscTKiKJFFn1ag==",
      "license": "MIT"
    },
    "node_modules/proxy-addr": {
      "version": "2.0.7",
      "resolved": "https://registry.npmjs.org/proxy-addr/-/proxy-addr-2.0.7.tgz",
      "integrity": "sha512-llQsMLSUDUPT44jdrU/O37qlnifitDP+ZwrmmZcoSKyLKvtZxpyV0n2/bD/N4tBAAZ/gJEdZU7KMraoK1+XYAg==",
      "license": "MIT",
      "dependencies": {
        "forwarded": "0.2.0",
        "ipaddr.js": "1.9.1"
      },
      "engines": {
        "node": ">= 0.10"
      }
    },
    "node_modules/punycode": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/punycode/-/punycode-2.3.1.tgz",
      "integrity": "sha512-vYt7UD1U9Wg6138shLtLOvdAu+8DsC/ilFtEVHcH+wydcSpNE20AfSOduf6MkRFahL5FY7X1oU7nKVZFtfq8Fg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/qs": {
      "version": "6.14.0",
      "resolved": "https://registry.npmjs.org/qs/-/qs-6.14.0.tgz",
      "integrity": "sha512-YWWTjgABSKcvs/nWBi9PycY/JiPJqOD4JA6o9Sej2AtvSGarXxKC3OQSk4pAarbdQlKAh5D4FCQkJNkW+GAn3w==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "side-channel": "^1.1.0"
      },
      "engines": {
        "node": ">=0.6"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/queue-microtask": {
      "version": "1.2.3",
      "resolved": "https://registry.npmjs.org/queue-microtask/-/queue-microtask-1.2.3.tgz",
      "integrity": "sha512-NuaNSa6flKT5JaSYQzJok04JzTL1CA6aGhv5rfLW3PgqA+M2ChpZQnAC8h8i4ZFkBS8X5RqkDBHA7r4hej3K9A==",
      "dev": true,
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT"
    },
    "node_modules/range-parser": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/range-parser/-/range-parser-1.2.1.tgz",
      "integrity": "sha512-Hrgsx+orqoygnmhFbKaHE6c296J+HTAQXoxEF6gNupROmmGJRoyzfG3ccAveqCBrwr/2yxQ5BVd/GTl5agOwSg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/raw-body": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/raw-body/-/raw-body-3.0.1.tgz",
      "integrity": "sha512-9G8cA+tuMS75+6G/TzW8OtLzmBDMo8p1JRxN5AZ+LAp8uxGA8V8GZm4GQ4/N5QNQEnLmg6SS7wyuSmbKepiKqA==",
      "license": "MIT",
      "dependencies": {
        "bytes": "3.1.2",
        "http-errors": "2.0.0",
        "iconv-lite": "0.7.0",
        "unpipe": "1.0.0"
      },
      "engines": {
        "node": ">= 0.10"
      }
    },
    "node_modules/raw-body/node_modules/iconv-lite": {
      "version": "0.7.0",
      "resolved": "https://registry.npmjs.org/iconv-lite/-/iconv-lite-0.7.0.tgz",
      "integrity": "sha512-cf6L2Ds3h57VVmkZe+Pn+5APsT7FpqJtEhhieDCvrE2MK5Qk9MyffgQyuxQTm6BChfeZNtcOLHp9IcWRVcIcBQ==",
      "license": "MIT",
      "dependencies": {
        "safer-buffer": ">= 2.1.2 < 3.0.0"
      },
      "engines": {
        "node": ">=0.10.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/express"
      }
    },
    "node_modules/react": {
      "version": "18.3.1",
      "resolved": "https://registry.npmjs.org/react/-/react-18.3.1.tgz",
      "integrity": "sha512-wS+hAgJShR0KhEvPJArfuPVN1+Hz1t0Y6n5jLrGQbkb4urgPE/0Rve+1kMB1v/oWgHgm4WIcV+i7F2pTVj+2iQ==",
      "license": "MIT",
      "dependencies": {
        "loose-envify": "^1.1.0"
      },
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/react-dom": {
      "version": "18.3.1",
      "resolved": "https://registry.npmjs.org/react-dom/-/react-dom-18.3.1.tgz",
      "integrity": "sha512-5m4nQKp+rZRb09LNH59GM4BxTh9251/ylbKIbpe7TpGxfJ+9kv6BLkLBXIjjspbgbnIBNqlI23tRnTWT0snUIw==",
      "license": "MIT",
      "dependencies": {
        "loose-envify": "^1.1.0",
        "scheduler": "^0.23.2"
      },
      "peerDependencies": {
        "react": "^18.3.1"
      }
    },
    "node_modules/react-hot-toast": {
      "version": "2.5.2",
      "resolved": "https://registry.npmjs.org/react-hot-toast/-/react-hot-toast-2.5.2.tgz",
      "integrity": "sha512-Tun3BbCxzmXXM7C+NI4qiv6lT0uwGh4oAfeJyNOjYUejTsm35mK9iCaYLGv8cBz9L5YxZLx/2ii7zsIwPtPUdw==",
      "license": "MIT",
      "dependencies": {
        "csstype": "^3.1.3",
        "goober": "^2.1.16"
      },
      "engines": {
        "node": ">=10"
      },
      "peerDependencies": {
        "react": ">=16",
        "react-dom": ">=16"
      }
    },
    "node_modules/react-router": {
      "version": "6.26.0",
      "resolved": "https://registry.npmjs.org/react-router/-/react-router-6.26.0.tgz",
      "integrity": "sha512-wVQq0/iFYd3iZ9H2l3N3k4PL8EEHcb0XlU2Na8nEwmiXgIUElEH6gaJDtUQxJ+JFzmIXaQjfdpcGWaM6IoQGxg==",
      "license": "MIT",
      "dependencies": {
        "@remix-run/router": "1.19.0"
      },
      "engines": {
        "node": ">=14.0.0"
      },
      "peerDependencies": {
        "react": ">=16.8"
      }
    },
    "node_modules/react-router-dom": {
      "version": "6.26.0",
      "resolved": "https://registry.npmjs.org/react-router-dom/-/react-router-dom-6.26.0.tgz",
      "integrity": "sha512-RRGUIiDtLrkX3uYcFiCIxKFWMcWQGMojpYZfcstc63A1+sSnVgILGIm9gNUA6na3Fm1QuPGSBQH2EMbAZOnMsQ==",
      "license": "MIT",
      "dependencies": {
        "@remix-run/router": "1.19.0",
        "react-router": "6.26.0"
      },
      "engines": {
        "node": ">=14.0.0"
      },
      "peerDependencies": {
        "react": ">=16.8",
        "react-dom": ">=16.8"
      }
    },
    "node_modules/read-cache": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/read-cache/-/read-cache-1.0.0.tgz",
      "integrity": "sha512-Owdv/Ft7IjOgm/i0xvNDZ1LrRANRfew4b2prF3OWMQLxLfu3bS8FVhCsrSCMK4lR56Y9ya+AThoTpDCTxCmpRA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "pify": "^2.3.0"
      }
    },
    "node_modules/readable-stream": {
      "version": "3.6.2",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-3.6.2.tgz",
      "integrity": "sha512-9u/sniCrY3D5WdsERHzHE4G2YCXqoG5FTHUiCC4SIbr6XcLZBY05ya9EKjYek9O5xOAwjGq+1JdGBAS7Q9ScoA==",
      "license": "MIT",
      "dependencies": {
        "inherits": "^2.0.3",
        "string_decoder": "^1.1.1",
        "util-deprecate": "^1.0.1"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/readdir-glob": {
      "version": "1.1.3",
      "resolved": "https://registry.npmjs.org/readdir-glob/-/readdir-glob-1.1.3.tgz",
      "integrity": "sha512-v05I2k7xN8zXvPD9N+z/uhXPaj0sUFCe2rcWZIpBsqxfP7xXFQ0tipAd/wjj1YxWyWtUS5IDJpOG82JKt2EAVA==",
      "license": "Apache-2.0",
      "dependencies": {
        "minimatch": "^5.1.0"
      }
    },
    "node_modules/readdir-glob/node_modules/brace-expansion": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-2.0.2.tgz",
      "integrity": "sha512-Jt0vHyM+jmUBqojB7E1NIYadt0vI0Qxjxd2TErW94wDz+E2LAm5vKMXXwg6ZZBTHPuUlDgQHKXvjGBdfcF1ZDQ==",
      "license": "MIT",
      "dependencies": {
        "balanced-match": "^1.0.0"
      }
    },
    "node_modules/readdir-glob/node_modules/minimatch": {
      "version": "5.1.6",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-5.1.6.tgz",
      "integrity": "sha512-lKwV/1brpG6mBUFHtb7NUmtABCb2WZZmm2wNiOA5hAb8VdCS4B3dtMWyvcoViccwAW/COERjXLt0zP1zXUN26g==",
      "license": "ISC",
      "dependencies": {
        "brace-expansion": "^2.0.1"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/readdirp": {
      "version": "3.6.0",
      "resolved": "https://registry.npmjs.org/readdirp/-/readdirp-3.6.0.tgz",
      "integrity": "sha512-hOS089on8RduqdbhvQ5Z37A0ESjsqz6qnRcffsMU3495FuTdqSm+7bhJ29JvIOsBDEEnan5DPu9t3To9VRlMzA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "picomatch": "^2.2.1"
      },
      "engines": {
        "node": ">=8.10.0"
      }
    },
    "node_modules/reflect-metadata": {
      "version": "0.1.13",
      "resolved": "https://registry.npmjs.org/reflect-metadata/-/reflect-metadata-0.1.13.tgz",
      "integrity": "sha512-Ts1Y/anZELhSsjMcU605fU9RE4Oi3p5ORujwbIKXfWa+0Zxs510Qrmrce5/Jowq3cHSZSJqBjypxmHarc+vEWg==",
      "dev": true,
      "license": "Apache-2.0"
    },
    "node_modules/resolve": {
      "version": "1.22.11",
      "resolved": "https://registry.npmjs.org/resolve/-/resolve-1.22.11.tgz",
      "integrity": "sha512-RfqAvLnMl313r7c9oclB1HhUEAezcpLjz95wFH4LVuhk9JF/r22qmVP9AMmOU4vMX7Q8pN8jwNg/CSpdFnMjTQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "is-core-module": "^2.16.1",
        "path-parse": "^1.0.7",
        "supports-preserve-symlinks-flag": "^1.0.0"
      },
      "bin": {
        "resolve": "bin/resolve"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/resolve-from": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/resolve-from/-/resolve-from-4.0.0.tgz",
      "integrity": "sha512-pb/MYmXstAkysRFx8piNI1tGFNQIFA3vkE3Gq4EuA1dF6gHp/+vgZqsCGJapvy8N3Q+4o7FwvquPJcnZ7RYy4g==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/resolve-pkg-maps": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/resolve-pkg-maps/-/resolve-pkg-maps-1.0.0.tgz",
      "integrity": "sha512-seS2Tj26TBVOC2NIc2rOe2y2ZO7efxITtLZcGSOnHHNOQ7CkiUBfw0Iw2ck6xkIhPwLhKNLS8BO+hEpngQlqzw==",
      "dev": true,
      "license": "MIT",
      "funding": {
        "url": "https://github.com/privatenumber/resolve-pkg-maps?sponsor=1"
      }
    },
    "node_modules/reusify": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/reusify/-/reusify-1.1.0.tgz",
      "integrity": "sha512-g6QUff04oZpHs0eG5p83rFLhHeV00ug/Yf9nZM6fLeUrPguBTkTQOdpAWWspMh55TZfVQDPaN3NQJfbVRAxdIw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "iojs": ">=1.0.0",
        "node": ">=0.10.0"
      }
    },
    "node_modules/rimraf": {
      "version": "2.7.1",
      "resolved": "https://registry.npmjs.org/rimraf/-/rimraf-2.7.1.tgz",
      "integrity": "sha512-uWjbaKIK3T1OSVptzX7Nl6PvQ3qAGtKEtVRjRuazjfL3Bx5eI409VZSqgND+4UNnmzLVdPj9FqFJNPqBZFve4w==",
      "deprecated": "Rimraf versions prior to v4 are no longer supported",
      "license": "ISC",
      "dependencies": {
        "glob": "^7.1.3"
      },
      "bin": {
        "rimraf": "bin.js"
      }
    },
    "node_modules/rollup": {
      "version": "4.53.2",
      "resolved": "https://registry.npmjs.org/rollup/-/rollup-4.53.2.tgz",
      "integrity": "sha512-MHngMYwGJVi6Fmnk6ISmnk7JAHRNF0UkuucA0CUW3N3a4KnONPEZz+vUanQP/ZC/iY1Qkf3bwPWzyY84wEks1g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@types/estree": "1.0.8"
      },
      "bin": {
        "rollup": "dist/bin/rollup"
      },
      "engines": {
        "node": ">=18.0.0",
        "npm": ">=8.0.0"
      },
      "optionalDependencies": {
        "@rollup/rollup-android-arm-eabi": "4.53.2",
        "@rollup/rollup-android-arm64": "4.53.2",
        "@rollup/rollup-darwin-arm64": "4.53.2",
        "@rollup/rollup-darwin-x64": "4.53.2",
        "@rollup/rollup-freebsd-arm64": "4.53.2",
        "@rollup/rollup-freebsd-x64": "4.53.2",
        "@rollup/rollup-linux-arm-gnueabihf": "4.53.2",
        "@rollup/rollup-linux-arm-musleabihf": "4.53.2",
        "@rollup/rollup-linux-arm64-gnu": "4.53.2",
        "@rollup/rollup-linux-arm64-musl": "4.53.2",
        "@rollup/rollup-linux-loong64-gnu": "4.53.2",
        "@rollup/rollup-linux-ppc64-gnu": "4.53.2",
        "@rollup/rollup-linux-riscv64-gnu": "4.53.2",
        "@rollup/rollup-linux-riscv64-musl": "4.53.2",
        "@rollup/rollup-linux-s390x-gnu": "4.53.2",
        "@rollup/rollup-linux-x64-gnu": "4.53.2",
        "@rollup/rollup-linux-x64-musl": "4.53.2",
        "@rollup/rollup-openharmony-arm64": "4.53.2",
        "@rollup/rollup-win32-arm64-msvc": "4.53.2",
        "@rollup/rollup-win32-ia32-msvc": "4.53.2",
        "@rollup/rollup-win32-x64-gnu": "4.53.2",
        "@rollup/rollup-win32-x64-msvc": "4.53.2",
        "fsevents": "~2.3.2"
      }
    },
    "node_modules/router": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/router/-/router-2.2.0.tgz",
      "integrity": "sha512-nLTrUKm2UyiL7rlhapu/Zl45FwNgkZGaCpZbIHajDYgwlJCOzLSk+cIPAnsEqV955GjILJnKbdQC1nVPz+gAYQ==",
      "license": "MIT",
      "dependencies": {
        "debug": "^4.4.0",
        "depd": "^2.0.0",
        "is-promise": "^4.0.0",
        "parseurl": "^1.3.3",
        "path-to-regexp": "^8.0.0"
      },
      "engines": {
        "node": ">= 18"
      }
    },
    "node_modules/run-parallel": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/run-parallel/-/run-parallel-1.2.0.tgz",
      "integrity": "sha512-5l4VyZR86LZ/lDxZTR6jqL8AFE2S0IFLMP26AbjsLVADxHdhB/c0GUsH+y39UfCi3dzz8OlQuPmnaJOMoDHQBA==",
      "dev": true,
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "queue-microtask": "^1.2.2"
      }
    },
    "node_modules/safe-buffer": {
      "version": "5.2.1",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.2.1.tgz",
      "integrity": "sha512-rp3So07KcdmmKbGvgaNxQSJr7bGVSVk5S9Eq1F+ppbRo70+YeaDxkw5Dd8NPN+GD6bjnYm2VuPuCXmpuYvmCXQ==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT"
    },
    "node_modules/safe-regex-test": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/safe-regex-test/-/safe-regex-test-1.1.0.tgz",
      "integrity": "sha512-x/+Cz4YrimQxQccJf5mKEbIa1NzeCRNI5Ecl/ekmlYaampdNLPalVyIcCZNNH3MvmqBugV5TMYZXv0ljslUlaw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.2",
        "es-errors": "^1.3.0",
        "is-regex": "^1.2.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/safer-buffer": {
      "version": "2.1.2",
      "resolved": "https://registry.npmjs.org/safer-buffer/-/safer-buffer-2.1.2.tgz",
      "integrity": "sha512-YZo3K82SD7Riyi0E1EQPojLz7kpepnSQI9IyPbHHg1XXXevb5dJI7tpyN2ADxGcQbHG7vcyRHk0cbwqcQriUtg==",
      "license": "MIT"
    },
    "node_modules/saxes": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/saxes/-/saxes-5.0.1.tgz",
      "integrity": "sha512-5LBh1Tls8c9xgGjw3QrMwETmTMVk0oFgvrFSvWx62llR2hcEInrKNZ2GZCCuuy2lvWrdl5jhbpeqc5hRYKFOcw==",
      "license": "ISC",
      "dependencies": {
        "xmlchars": "^2.2.0"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/scheduler": {
      "version": "0.23.2",
      "resolved": "https://registry.npmjs.org/scheduler/-/scheduler-0.23.2.tgz",
      "integrity": "sha512-UOShsPwz7NrMUqhR6t0hWjFduvOzbtv7toDH1/hIrfRNIDBnnBWd0CwJTGvTpngVlmwGCdP9/Zl/tVrDqcuYzQ==",
      "license": "MIT",
      "dependencies": {
        "loose-envify": "^1.1.0"
      }
    },
    "node_modules/semver": {
      "version": "7.7.3",
      "resolved": "https://registry.npmjs.org/semver/-/semver-7.7.3.tgz",
      "integrity": "sha512-SdsKMrI9TdgjdweUSR9MweHA4EJ8YxHn8DFaDisvhVlUOe4BF1tLD7GAj0lIqWVl+dPb/rExr0Btby5loQm20Q==",
      "dev": true,
      "license": "ISC",
      "bin": {
        "semver": "bin/semver.js"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/send": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/send/-/send-1.2.0.tgz",
      "integrity": "sha512-uaW0WwXKpL9blXE2o0bRhoL2EGXIrZxQ2ZQ4mgcfoBxdFmQold+qWsD2jLrfZ0trjKL6vOw0j//eAwcALFjKSw==",
      "license": "MIT",
      "dependencies": {
        "debug": "^4.3.5",
        "encodeurl": "^2.0.0",
        "escape-html": "^1.0.3",
        "etag": "^1.8.1",
        "fresh": "^2.0.0",
        "http-errors": "^2.0.0",
        "mime-types": "^3.0.1",
        "ms": "^2.1.3",
        "on-finished": "^2.4.1",
        "range-parser": "^1.2.1",
        "statuses": "^2.0.1"
      },
      "engines": {
        "node": ">= 18"
      }
    },
    "node_modules/serve-static": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/serve-static/-/serve-static-2.2.0.tgz",
      "integrity": "sha512-61g9pCh0Vnh7IutZjtLGGpTA355+OPn2TyDv/6ivP2h/AdAVX9azsoxmg2/M6nZeQZNYBEwIcsne1mJd9oQItQ==",
      "license": "MIT",
      "dependencies": {
        "encodeurl": "^2.0.0",
        "escape-html": "^1.0.3",
        "parseurl": "^1.3.3",
        "send": "^1.2.0"
      },
      "engines": {
        "node": ">= 18"
      }
    },
    "node_modules/set-function-length": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/set-function-length/-/set-function-length-1.2.2.tgz",
      "integrity": "sha512-pgRc4hJ4/sNjWCSS9AmnS40x3bNMDTknHgL5UaMBTMyJnU90EgWh1Rz+MC9eFu4BuN/UwZjKQuY/1v3rM7HMfg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "define-data-property": "^1.1.4",
        "es-errors": "^1.3.0",
        "function-bind": "^1.1.2",
        "get-intrinsic": "^1.2.4",
        "gopd": "^1.0.1",
        "has-property-descriptors": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      }
    },
    "node_modules/setimmediate": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/setimmediate/-/setimmediate-1.0.5.tgz",
      "integrity": "sha512-MATJdZp8sLqDl/68LfQmbP8zKPLQNV6BIZoIgrscFDQ+RsvK/BxeDQOgyxKKoh0y/8h3BqVFnCqQ/gd+reiIXA==",
      "license": "MIT"
    },
    "node_modules/setprototypeof": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/setprototypeof/-/setprototypeof-1.2.0.tgz",
      "integrity": "sha512-E5LDX7Wrp85Kil5bhZv46j8jOeboKq5JMmYM3gVGdGH8xFpPWXUMsNrlODCrkoxMEeNi/XZIwuRvY4XNwYMJpw==",
      "license": "ISC"
    },
    "node_modules/shebang-command": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/shebang-command/-/shebang-command-2.0.0.tgz",
      "integrity": "sha512-kHxr2zZpYtdmrN1qDjrrX/Z1rR1kG8Dx+gkpK1G4eXmvXswmcE1hTWBWYUzlraYw1/yZp6YuDY77YtvbN0dmDA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "shebang-regex": "^3.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/shebang-regex": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/shebang-regex/-/shebang-regex-3.0.0.tgz",
      "integrity": "sha512-7++dFhtcx3353uBaq8DDR4NuxBetBzC7ZQOhmTQInHEd6bSrXdiEyzCvG07Z44UYdLShWUyXt5M/yhz8ekcb1A==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/side-channel": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/side-channel/-/side-channel-1.1.0.tgz",
      "integrity": "sha512-ZX99e6tRweoUXqR+VBrslhda51Nh5MTQwou5tnUDgbtyM0dBgmhEDtWGP/xbKn6hqfPRHujUNwz5fy/wbbhnpw==",
      "license": "MIT",
      "dependencies": {
        "es-errors": "^1.3.0",
        "object-inspect": "^1.13.3",
        "side-channel-list": "^1.0.0",
        "side-channel-map": "^1.0.1",
        "side-channel-weakmap": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/side-channel-list": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/side-channel-list/-/side-channel-list-1.0.0.tgz",
      "integrity": "sha512-FCLHtRD/gnpCiCHEiJLOwdmFP+wzCmDEkc9y7NsYxeF4u7Btsn1ZuwgwJGxImImHicJArLP4R0yX4c2KCrMrTA==",
      "license": "MIT",
      "dependencies": {
        "es-errors": "^1.3.0",
        "object-inspect": "^1.13.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/side-channel-map": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/side-channel-map/-/side-channel-map-1.0.1.tgz",
      "integrity": "sha512-VCjCNfgMsby3tTdo02nbjtM/ewra6jPHmpThenkTYh8pG9ucZ/1P8So4u4FGBek/BjpOVsDCMoLA/iuBKIFXRA==",
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.2",
        "es-errors": "^1.3.0",
        "get-intrinsic": "^1.2.5",
        "object-inspect": "^1.13.3"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/side-channel-weakmap": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/side-channel-weakmap/-/side-channel-weakmap-1.0.2.tgz",
      "integrity": "sha512-WPS/HvHQTYnHisLo9McqBHOJk2FkHO/tlpvldyrnem4aeQp4hai3gythswg6p01oSoTl58rcpiFAjF2br2Ak2A==",
      "license": "MIT",
      "dependencies": {
        "call-bound": "^1.0.2",
        "es-errors": "^1.3.0",
        "get-intrinsic": "^1.2.5",
        "object-inspect": "^1.13.3",
        "side-channel-map": "^1.0.1"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/signal-exit": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/signal-exit/-/signal-exit-4.1.0.tgz",
      "integrity": "sha512-bzyZ1e88w9O1iNJbKnOlvYTrWPDl46O1bG0D3XInv+9tkPrxrN8jUUTiFlDkkmKWgn1M6CfIA13SuGqOa9Korw==",
      "dev": true,
      "license": "ISC",
      "engines": {
        "node": ">=14"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/source-map": {
      "version": "0.6.1",
      "resolved": "https://registry.npmjs.org/source-map/-/source-map-0.6.1.tgz",
      "integrity": "sha512-UjgapumWlbMhkBgzT7Ykc5YXUT46F0iKu8SGXq0bcwP5dz/h0Plj6enJqjz1Zbq2l5WaqYnrVbwWOWMyF3F47g==",
      "dev": true,
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/source-map-js": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/source-map-js/-/source-map-js-1.2.1.tgz",
      "integrity": "sha512-UXWMKhLOwVKb728IUtQPXxfYU+usdybtUrK/8uGE8CQMvrhOpwvzDBwj0QhSL7MQc7vIsISBG8VQ8+IDQxpfQA==",
      "dev": true,
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/source-map-support": {
      "version": "0.5.21",
      "resolved": "https://registry.npmjs.org/source-map-support/-/source-map-support-0.5.21.tgz",
      "integrity": "sha512-uBHU3L3czsIyYXKX88fdrGovxdSCoTGDRZ6SYXtSRxLZUzHg5P/66Ht6uoUlHu9EZod+inXhKo3qQgwXUT/y1w==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "buffer-from": "^1.0.0",
        "source-map": "^0.6.0"
      }
    },
    "node_modules/statuses": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/statuses/-/statuses-2.0.2.tgz",
      "integrity": "sha512-DvEy55V3DB7uknRo+4iOGT5fP1slR8wQohVdknigZPMpMstaKJQWhwiYBACJE3Ul2pTnATihhBYnRhZQHGBiRw==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/streamsearch": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/streamsearch/-/streamsearch-1.1.0.tgz",
      "integrity": "sha512-Mcc5wHehp9aXz1ax6bZUyY5afg9u2rv5cqQI3mRrYkGC8rW2hM02jWuwjtL++LS5qinSyhj2QfLyNsuc+VsExg==",
      "engines": {
        "node": ">=10.0.0"
      }
    },
    "node_modules/string_decoder": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.3.0.tgz",
      "integrity": "sha512-hkRX8U1WjJFd8LsDJ2yQ/wWWxaopEsABU1XfkM8A+j0+85JAGppt16cr1Whg6KIbb4okU6Mql6BOj+uup/wKeA==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.2.0"
      }
    },
    "node_modules/string-template": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/string-template/-/string-template-1.0.0.tgz",
      "integrity": "sha512-SLqR3GBUXuoPP5MmYtD7ompvXiG87QjT6lzOszyXjTM86Uu7At7vNnt2xgyTLq5o9T4IxTYFyGxcULqpsmsfdg==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/string-width": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-5.1.2.tgz",
      "integrity": "sha512-HnLOCR3vjcY8beoNLtcjZ5/nxn2afmME6lhrDrebokqMap+XbeW8n9TXpPDOqdGK5qcI3oT0GKTW6wC7EMiVqA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "eastasianwidth": "^0.2.0",
        "emoji-regex": "^9.2.2",
        "strip-ansi": "^7.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/string-width-cjs": {
      "name": "string-width",
      "version": "4.2.3",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-4.2.3.tgz",
      "integrity": "sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "emoji-regex": "^8.0.0",
        "is-fullwidth-code-point": "^3.0.0",
        "strip-ansi": "^6.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/string-width-cjs/node_modules/emoji-regex": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-8.0.0.tgz",
      "integrity": "sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/string-width/node_modules/ansi-regex": {
      "version": "6.2.2",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-6.2.2.tgz",
      "integrity": "sha512-Bq3SmSpyFHaWjPk8If9yc6svM8c56dB5BAtW4Qbw5jHTwwXXcTLoRMkpDJp6VL0XzlWaCHTXrkFURMYmD0sLqg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-regex?sponsor=1"
      }
    },
    "node_modules/string-width/node_modules/strip-ansi": {
      "version": "7.1.2",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-7.1.2.tgz",
      "integrity": "sha512-gmBGslpoQJtgnMAvOVqGZpEz9dyoKTCzy2nfz/n8aIFhN/jCE/rCmcxabB6jOOHV+0WNnylOxaxBQPSvcWklhA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^6.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/strip-ansi?sponsor=1"
      }
    },
    "node_modules/stringz": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/stringz/-/stringz-2.1.0.tgz",
      "integrity": "sha512-KlywLT+MZ+v0IRepfMxRtnSvDCMc3nR1qqCs3m/qIbSOWkNZYT8XHQA31rS3TnKp0c5xjZu3M4GY/2aRKSi/6A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "char-regex": "^1.0.2"
      }
    },
    "node_modules/strip-ansi": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-6.0.1.tgz",
      "integrity": "sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-ansi-cjs": {
      "name": "strip-ansi",
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-6.0.1.tgz",
      "integrity": "sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-json-comments": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/strip-json-comments/-/strip-json-comments-3.1.1.tgz",
      "integrity": "sha512-6fPc+R4ihwqP6N/aIv2f1gMH8lOVtWQHoqC4yK6oSDVVocumAsfCqjkXnqiYMhmMwS/mEHLp7Vehlt3ql6lEig==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/sucrase": {
      "version": "3.35.0",
      "resolved": "https://registry.npmjs.org/sucrase/-/sucrase-3.35.0.tgz",
      "integrity": "sha512-8EbVDiu9iN/nESwxeSxDKe0dunta1GOlHufmSSXxMD2z2/tMZpDMpvXQGsc+ajGo8y2uYUmixaSRUc/QPoQ0GA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@jridgewell/gen-mapping": "^0.3.2",
        "commander": "^4.0.0",
        "glob": "^10.3.10",
        "lines-and-columns": "^1.1.6",
        "mz": "^2.7.0",
        "pirates": "^4.0.1",
        "ts-interface-checker": "^0.1.9"
      },
      "bin": {
        "sucrase": "bin/sucrase",
        "sucrase-node": "bin/sucrase-node"
      },
      "engines": {
        "node": ">=16 || 14 >=14.17"
      }
    },
    "node_modules/sucrase/node_modules/brace-expansion": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-2.0.2.tgz",
      "integrity": "sha512-Jt0vHyM+jmUBqojB7E1NIYadt0vI0Qxjxd2TErW94wDz+E2LAm5vKMXXwg6ZZBTHPuUlDgQHKXvjGBdfcF1ZDQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "balanced-match": "^1.0.0"
      }
    },
    "node_modules/sucrase/node_modules/glob": {
      "version": "10.4.5",
      "resolved": "https://registry.npmjs.org/glob/-/glob-10.4.5.tgz",
      "integrity": "sha512-7Bv8RF0k6xjo7d4A/PxYLbUCfb6c+Vpd2/mB2yRDlew7Jb5hEXiCD9ibfO7wpk8i4sevK6DFny9h7EYbM3/sHg==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "foreground-child": "^3.1.0",
        "jackspeak": "^3.1.2",
        "minimatch": "^9.0.4",
        "minipass": "^7.1.2",
        "package-json-from-dist": "^1.0.0",
        "path-scurry": "^1.11.1"
      },
      "bin": {
        "glob": "dist/esm/bin.mjs"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/sucrase/node_modules/minimatch": {
      "version": "9.0.5",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-9.0.5.tgz",
      "integrity": "sha512-G6T0ZX48xgozx7587koeX9Ys2NYy6Gmv//P89sEte9V9whIapMNF4idKxnW2QtCcLiTWlb/wfCabAtAFWhhBow==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "brace-expansion": "^2.0.1"
      },
      "engines": {
        "node": ">=16 || 14 >=14.17"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/supports-color": {
      "version": "7.2.0",
      "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-7.2.0.tgz",
      "integrity": "sha512-qpCAvRl9stuOHveKsn7HncJRvv501qIacKzQlO/+Lwxc9+0q2wLyv4Dfvt80/DPn2pqOBsJdDiogXGR9+OvwRw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "has-flag": "^4.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/supports-preserve-symlinks-flag": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/supports-preserve-symlinks-flag/-/supports-preserve-symlinks-flag-1.0.0.tgz",
      "integrity": "sha512-ot0WnXS9fgdkgIcePe6RHNk1WA8+muPa6cSjeR3V8K27q9BB1rTE3R1p7Hv0z1ZyAc8s6Vvv8DIyWf681MAt0w==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/tailwindcss": {
      "version": "3.4.17",
      "resolved": "https://registry.npmjs.org/tailwindcss/-/tailwindcss-3.4.17.tgz",
      "integrity": "sha512-w33E2aCvSDP0tW9RZuNXadXlkHXqFzSkQew/aIa2i/Sj8fThxwovwlXHSPXTbAHwEIhBFXAedUhP2tueAKP8Og==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@alloc/quick-lru": "^5.2.0",
        "arg": "^5.0.2",
        "chokidar": "^3.6.0",
        "didyoumean": "^1.2.2",
        "dlv": "^1.1.3",
        "fast-glob": "^3.3.2",
        "glob-parent": "^6.0.2",
        "is-glob": "^4.0.3",
        "jiti": "^1.21.6",
        "lilconfig": "^3.1.3",
        "micromatch": "^4.0.8",
        "normalize-path": "^3.0.0",
        "object-hash": "^3.0.0",
        "picocolors": "^1.1.1",
        "postcss": "^8.4.47",
        "postcss-import": "^15.1.0",
        "postcss-js": "^4.0.1",
        "postcss-load-config": "^4.0.2",
        "postcss-nested": "^6.2.0",
        "postcss-selector-parser": "^6.1.2",
        "resolve": "^1.22.8",
        "sucrase": "^3.35.0"
      },
      "bin": {
        "tailwind": "lib/cli.js",
        "tailwindcss": "lib/cli.js"
      },
      "engines": {
        "node": ">=14.0.0"
      }
    },
    "node_modules/tar-stream": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/tar-stream/-/tar-stream-2.2.0.tgz",
      "integrity": "sha512-ujeqbceABgwMZxEJnk2HDY2DlnUZ+9oEcb1KzTVfYHio0UE6dG71n60d8D2I4qNvleWrrXpmjpt7vZeF1LnMZQ==",
      "license": "MIT",
      "dependencies": {
        "bl": "^4.0.3",
        "end-of-stream": "^1.4.1",
        "fs-constants": "^1.0.0",
        "inherits": "^2.0.3",
        "readable-stream": "^3.1.1"
      },
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/text-table": {
      "version": "0.2.0",
      "resolved": "https://registry.npmjs.org/text-table/-/text-table-0.2.0.tgz",
      "integrity": "sha512-N+8UisAXDGk8PFXP4HAzVR9nbfmVJ3zYLAWiTIoqC5v5isinhr+r5uaO8+7r3BMfuNIufIsA7RdpVgacC2cSpw==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/thenify": {
      "version": "3.3.1",
      "resolved": "https://registry.npmjs.org/thenify/-/thenify-3.3.1.tgz",
      "integrity": "sha512-RVZSIV5IG10Hk3enotrhvz0T9em6cyHBLkH/YAZuKqd8hRkKhSfCGIcP2KUY0EPxndzANBmNllzWPwak+bheSw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "any-promise": "^1.0.0"
      }
    },
    "node_modules/thenify-all": {
      "version": "1.6.0",
      "resolved": "https://registry.npmjs.org/thenify-all/-/thenify-all-1.6.0.tgz",
      "integrity": "sha512-RNxQH/qI8/t3thXJDwcstUO4zeqo64+Uy/+sNVRBx4Xn2OX+OZ9oP+iJnNFqplFra2ZUVeKCSa2oVWi3T4uVmA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "thenify": ">= 3.1.0 < 4"
      },
      "engines": {
        "node": ">=0.8"
      }
    },
    "node_modules/tinyglobby": {
      "version": "0.2.15",
      "resolved": "https://registry.npmjs.org/tinyglobby/-/tinyglobby-0.2.15.tgz",
      "integrity": "sha512-j2Zq4NyQYG5XMST4cbs02Ak8iJUdxRM0XI5QyxXuZOzKOINmWurp3smXu3y5wDcJrptwpSjgXHzIQxR0omXljQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "fdir": "^6.5.0",
        "picomatch": "^4.0.3"
      },
      "engines": {
        "node": ">=12.0.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/SuperchupuDev"
      }
    },
    "node_modules/tinyglobby/node_modules/fdir": {
      "version": "6.5.0",
      "resolved": "https://registry.npmjs.org/fdir/-/fdir-6.5.0.tgz",
      "integrity": "sha512-tIbYtZbucOs0BRGqPJkshJUYdL+SDH7dVM8gjy+ERp3WAUjLEFJE+02kanyHtwjWOnwrKYBiwAmM0p4kLJAnXg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12.0.0"
      },
      "peerDependencies": {
        "picomatch": "^3 || ^4"
      },
      "peerDependenciesMeta": {
        "picomatch": {
          "optional": true
        }
      }
    },
    "node_modules/tinyglobby/node_modules/picomatch": {
      "version": "4.0.3",
      "resolved": "https://registry.npmjs.org/picomatch/-/picomatch-4.0.3.tgz",
      "integrity": "sha512-5gTmgEY/sqK6gFXLIsQNH19lWb4ebPDLA4SdLP7dsWkIXHWlG66oPuVvXSGFPppYZz8ZDZq0dYYrbHfBCVUb1Q==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/jonschlinkert"
      }
    },
    "node_modules/tmp": {
      "version": "0.2.5",
      "resolved": "https://registry.npmjs.org/tmp/-/tmp-0.2.5.tgz",
      "integrity": "sha512-voyz6MApa1rQGUxT3E+BK7/ROe8itEx7vD8/HEvt4xwXucvQ5G5oeEiHkmHZJuBO21RpOf+YYm9MOivj709jow==",
      "license": "MIT",
      "engines": {
        "node": ">=14.14"
      }
    },
    "node_modules/to-regex-range": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/to-regex-range/-/to-regex-range-5.0.1.tgz",
      "integrity": "sha512-65P7iz6X5yEr1cwcgvQxbbIw7Uk3gOy5dIdtZ4rDveLqhrdJP+Li/Hx6tyK0NEb+2GCyneCMJiGqrADCSNk8sQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "is-number": "^7.0.0"
      },
      "engines": {
        "node": ">=8.0"
      }
    },
    "node_modules/toidentifier": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/toidentifier/-/toidentifier-1.0.1.tgz",
      "integrity": "sha512-o5sSPKEkg/DIQNmH43V0/uerLrpzVedkUh8tGNvaeXpfpuwjKenlSox/2O/BTlZUtEe+JG7s5YhEz608PlAHRA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.6"
      }
    },
    "node_modules/traverse": {
      "version": "0.3.9",
      "resolved": "https://registry.npmjs.org/traverse/-/traverse-0.3.9.tgz",
      "integrity": "sha512-iawgk0hLP3SxGKDfnDJf8wTz4p2qImnyihM5Hh/sGvQ3K37dPi/w8sRhdNIxYA1TwFwc5mDhIJq+O0RsvXBKdQ==",
      "license": "MIT/X11",
      "engines": {
        "node": "*"
      }
    },
    "node_modules/ts-api-utils": {
      "version": "1.4.3",
      "resolved": "https://registry.npmjs.org/ts-api-utils/-/ts-api-utils-1.4.3.tgz",
      "integrity": "sha512-i3eMG77UTMD0hZhgRS562pv83RC6ukSAC2GMNWc+9dieh/+jDM5u5YG+NHX6VNDRHQcHwmsTHctP9LhbC3WxVw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=16"
      },
      "peerDependencies": {
        "typescript": ">=4.2.0"
      }
    },
    "node_modules/ts-interface-checker": {
      "version": "0.1.13",
      "resolved": "https://registry.npmjs.org/ts-interface-checker/-/ts-interface-checker-0.1.13.tgz",
      "integrity": "sha512-Y/arvbn+rrz3JCKl9C4kVNfTfSm2/mEp5FSz5EsZSANGPSlQrpRI5M4PKF+mJnE52jOO90PnPSc3Ur3bTQw0gA==",
      "dev": true,
      "license": "Apache-2.0"
    },
    "node_modules/tslib": {
      "version": "2.8.1",
      "resolved": "https://registry.npmjs.org/tslib/-/tslib-2.8.1.tgz",
      "integrity": "sha512-oJFu94HQb+KVduSUQL7wnpmqnfmLsOA/nAh6b6EH0wCEoK0/mPeXU6c3wKDV83MkOuHPRHtSXKKU99IBazS/2w==",
      "license": "0BSD"
    },
    "node_modules/tsx": {
      "version": "4.20.6",
      "resolved": "https://registry.npmjs.org/tsx/-/tsx-4.20.6.tgz",
      "integrity": "sha512-ytQKuwgmrrkDTFP4LjR0ToE2nqgy886GpvRSpU0JAnrdBYppuY5rLkRUYPU1yCryb24SsKBTL/hlDQAEFVwtZg==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "esbuild": "~0.25.0",
        "get-tsconfig": "^4.7.5"
      },
      "bin": {
        "tsx": "dist/cli.mjs"
      },
      "engines": {
        "node": ">=18.0.0"
      },
      "optionalDependencies": {
        "fsevents": "~2.3.3"
      }
    },
    "node_modules/type-check": {
      "version": "0.4.0",
      "resolved": "https://registry.npmjs.org/type-check/-/type-check-0.4.0.tgz",
      "integrity": "sha512-XleUoc9uwGXqjWwXaUTZAmzMcFZ5858QA2vvx1Ur5xIcixXIP+8LnFDgRplU30us6teqdlskFfu+ae4K79Ooew==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "prelude-ls": "^1.2.1"
      },
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/type-is": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/type-is/-/type-is-2.0.1.tgz",
      "integrity": "sha512-OZs6gsjF4vMp32qrCbiVSkrFmXtG/AZhY3t0iAMrMBiAZyV9oALtXO8hsrHbMXF9x6L3grlFuwW2oAz7cav+Gw==",
      "license": "MIT",
      "dependencies": {
        "content-type": "^1.0.5",
        "media-typer": "^1.1.0",
        "mime-types": "^3.0.0"
      },
      "engines": {
        "node": ">= 0.6"
      }
    },
    "node_modules/typedarray": {
      "version": "0.0.6",
      "resolved": "https://registry.npmjs.org/typedarray/-/typedarray-0.0.6.tgz",
      "integrity": "sha512-/aCDEGatGvZ2BIk+HmLf4ifCJFwvKFNb9/JeZPMulfgFracn9QFcAf5GO8B/mweUjSoblS5In0cWhqpfs/5PQA==",
      "license": "MIT"
    },
    "node_modules/typescript": {
      "version": "5.5.3",
      "resolved": "https://registry.npmjs.org/typescript/-/typescript-5.5.3.tgz",
      "integrity": "sha512-/hreyEujaB0w76zKo6717l3L0o/qEUtRgdvUBvlkhoWeOVMjMuHNHk0BRBzikzuGDqNmPQbg5ifMEqsHLiIUcQ==",
      "dev": true,
      "license": "Apache-2.0",
      "bin": {
        "tsc": "bin/tsc",
        "tsserver": "bin/tsserver"
      },
      "engines": {
        "node": ">=14.17"
      }
    },
    "node_modules/typescript-eslint": {
      "version": "8.3.0",
      "resolved": "https://registry.npmjs.org/typescript-eslint/-/typescript-eslint-8.3.0.tgz",
      "integrity": "sha512-EvWjwWLwwKDIJuBjk2I6UkV8KEQcwZ0VM10nR1rIunRDIP67QJTZAHBXTX0HW/oI1H10YESF8yWie8fRQxjvFA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@typescript-eslint/eslint-plugin": "8.3.0",
        "@typescript-eslint/parser": "8.3.0",
        "@typescript-eslint/utils": "8.3.0"
      },
      "engines": {
        "node": "^18.18.0 || ^20.9.0 || >=21.1.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/typescript-eslint"
      },
      "peerDependenciesMeta": {
        "typescript": {
          "optional": true
        }
      }
    },
    "node_modules/ufo": {
      "version": "1.6.1",
      "resolved": "https://registry.npmjs.org/ufo/-/ufo-1.6.1.tgz",
      "integrity": "sha512-9a4/uxlTWJ4+a5i0ooc1rU7C7YOw3wT+UGqdeNNHWnOF9qcMBgLRS+4IYUqbczewFx4mLEig6gawh7X6mFlEkA==",
      "license": "MIT"
    },
    "node_modules/undici-types": {
      "version": "7.16.0",
      "resolved": "https://registry.npmjs.org/undici-types/-/undici-types-7.16.0.tgz",
      "integrity": "sha512-Zz+aZWSj8LE6zoxD+xrjh4VfkIG8Ya6LvYkZqtUQGJPZjYl53ypCaUwWqo7eI0x66KBGeRo+mlBEkMSeSZ38Nw==",
      "license": "MIT"
    },
    "node_modules/unpipe": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/unpipe/-/unpipe-1.0.0.tgz",
      "integrity": "sha512-pjy2bYhSsufwWlKwPc+l3cN7+wuJlK6uz0YdJEOlQDbl6jo/YlPi4mb8agUkVC8BF7V8NuzeyPNqRksA3hztKQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/unzipper": {
      "version": "0.10.14",
      "resolved": "https://registry.npmjs.org/unzipper/-/unzipper-0.10.14.tgz",
      "integrity": "sha512-ti4wZj+0bQTiX2KmKWuwj7lhV+2n//uXEotUmGuQqrbVZSEGFMbI68+c6JCQ8aAmUWYvtHEz2A8K6wXvueR/6g==",
      "license": "MIT",
      "dependencies": {
        "big-integer": "^1.6.17",
        "binary": "~0.3.0",
        "bluebird": "~3.4.1",
        "buffer-indexof-polyfill": "~1.0.0",
        "duplexer2": "~0.1.4",
        "fstream": "^1.0.12",
        "graceful-fs": "^4.2.2",
        "listenercount": "~1.0.1",
        "readable-stream": "~2.3.6",
        "setimmediate": "~1.0.4"
      }
    },
    "node_modules/unzipper/node_modules/readable-stream": {
      "version": "2.3.8",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.3.8.tgz",
      "integrity": "sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==",
      "license": "MIT",
      "dependencies": {
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.3",
        "isarray": "~1.0.0",
        "process-nextick-args": "~2.0.0",
        "safe-buffer": "~5.1.1",
        "string_decoder": "~1.1.1",
        "util-deprecate": "~1.0.1"
      }
    },
    "node_modules/unzipper/node_modules/safe-buffer": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.1.2.tgz",
      "integrity": "sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==",
      "license": "MIT"
    },
    "node_modules/unzipper/node_modules/string_decoder": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.1.1.tgz",
      "integrity": "sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.1.0"
      }
    },
    "node_modules/update-browserslist-db": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/update-browserslist-db/-/update-browserslist-db-1.1.4.tgz",
      "integrity": "sha512-q0SPT4xyU84saUX+tomz1WLkxUbuaJnR1xWt17M7fJtEJigJeWUNGUqrauFXsHnqev9y9JTRGwk13tFBuKby4A==",
      "dev": true,
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/browserslist"
        },
        {
          "type": "github",
          "url": "https://github.com/sponsors/ai"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "escalade": "^3.2.0",
        "picocolors": "^1.1.1"
      },
      "bin": {
        "update-browserslist-db": "cli.js"
      },
      "peerDependencies": {
        "browserslist": ">= 4.21.0"
      }
    },
    "node_modules/uri-js": {
      "version": "4.4.1",
      "resolved": "https://registry.npmjs.org/uri-js/-/uri-js-4.4.1.tgz",
      "integrity": "sha512-7rKUyy33Q1yc98pQ1DAmLtwX109F7TIfWlW1Ydo8Wl1ii1SeHieeh0HHfPeL2fMXK6z0s8ecKs9frCuLJvndBg==",
      "dev": true,
      "license": "BSD-2-Clause",
      "dependencies": {
        "punycode": "^2.1.0"
      }
    },
    "node_modules/util": {
      "version": "0.12.5",
      "resolved": "https://registry.npmjs.org/util/-/util-0.12.5.tgz",
      "integrity": "sha512-kZf/K6hEIrWHI6XqOFUiiMa+79wE/D8Q+NCNAWclkyg3b4d2k7s0QGepNjiABc+aR3N1PAyHL7p6UcLY6LmrnA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "inherits": "^2.0.3",
        "is-arguments": "^1.0.4",
        "is-generator-function": "^1.0.7",
        "is-typed-array": "^1.1.3",
        "which-typed-array": "^1.1.2"
      }
    },
    "node_modules/util-deprecate": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/util-deprecate/-/util-deprecate-1.0.2.tgz",
      "integrity": "sha512-EPD5q1uXyFxJpCrLnCc1nHnq3gOa6DZBocAIiI2TaSCA7VCJ1UJDMagCzIkXNsUYfD1daK//LTEQ8xiIbrHtcw==",
      "license": "MIT"
    },
    "node_modules/uuid": {
      "version": "11.1.0",
      "resolved": "https://registry.npmjs.org/uuid/-/uuid-11.1.0.tgz",
      "integrity": "sha512-0/A9rDy9P7cJ+8w1c9WD9V//9Wj15Ce2MPz8Ri6032usz+NfePxx5AcN3bN+r6ZL6jEo066/yNYB3tn4pQEx+A==",
      "funding": [
        "https://github.com/sponsors/broofa",
        "https://github.com/sponsors/ctavan"
      ],
      "license": "MIT",
      "bin": {
        "uuid": "dist/esm/bin/uuid"
      }
    },
    "node_modules/validator": {
      "version": "13.15.23",
      "resolved": "https://registry.npmjs.org/validator/-/validator-13.15.23.tgz",
      "integrity": "sha512-4yoz1kEWqUjzi5zsPbAS/903QXSYp0UOtHsPpp7p9rHAw/W+dkInskAE386Fat3oKRROwO98d9ZB0G4cObgUyw==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">= 0.10"
      }
    },
    "node_modules/vary": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/vary/-/vary-1.1.2.tgz",
      "integrity": "sha512-BNGbWLfd0eUPabhkXUVm0j8uuvREyTh5ovRa/dyow/BqAbZJyC+5fU+IzQOzmAKzYqYRAISoRhdQr3eIZ/PXqg==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.8"
      }
    },
    "node_modules/vite": {
      "version": "7.2.2",
      "resolved": "https://registry.npmjs.org/vite/-/vite-7.2.2.tgz",
      "integrity": "sha512-BxAKBWmIbrDgrokdGZH1IgkIk/5mMHDreLDmCJ0qpyJaAteP8NvMhkwr/ZCQNqNH97bw/dANTE9PDzqwJghfMQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "esbuild": "^0.25.0",
        "fdir": "^6.5.0",
        "picomatch": "^4.0.3",
        "postcss": "^8.5.6",
        "rollup": "^4.43.0",
        "tinyglobby": "^0.2.15"
      },
      "bin": {
        "vite": "bin/vite.js"
      },
      "engines": {
        "node": "^20.19.0 || >=22.12.0"
      },
      "funding": {
        "url": "https://github.com/vitejs/vite?sponsor=1"
      },
      "optionalDependencies": {
        "fsevents": "~2.3.3"
      },
      "peerDependencies": {
        "@types/node": "^20.19.0 || >=22.12.0",
        "jiti": ">=1.21.0",
        "less": "^4.0.0",
        "lightningcss": "^1.21.0",
        "sass": "^1.70.0",
        "sass-embedded": "^1.70.0",
        "stylus": ">=0.54.8",
        "sugarss": "^5.0.0",
        "terser": "^5.16.0",
        "tsx": "^4.8.1",
        "yaml": "^2.4.2"
      },
      "peerDependenciesMeta": {
        "@types/node": {
          "optional": true
        },
        "jiti": {
          "optional": true
        },
        "less": {
          "optional": true
        },
        "lightningcss": {
          "optional": true
        },
        "sass": {
          "optional": true
        },
        "sass-embedded": {
          "optional": true
        },
        "stylus": {
          "optional": true
        },
        "sugarss": {
          "optional": true
        },
        "terser": {
          "optional": true
        },
        "tsx": {
          "optional": true
        },
        "yaml": {
          "optional": true
        }
      }
    },
    "node_modules/vite-plugin-javascript-obfuscator": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/vite-plugin-javascript-obfuscator/-/vite-plugin-javascript-obfuscator-3.1.0.tgz",
      "integrity": "sha512-sf4JFlG1iUPl7bLXHGOy+bKWOQUFyXzJFWa+n2S2xMMvyfM+V9R40HhpZoIF1eAjifArM1SF7fbSFIaTuUIbPA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "anymatch": "~3.1.3",
        "javascript-obfuscator": "^4.1.0"
      }
    },
    "node_modules/vite-plugin-obfuscator": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/vite-plugin-obfuscator/-/vite-plugin-obfuscator-1.0.5.tgz",
      "integrity": "sha512-5kflM0I3dIpFYIRmPHtdr5Y54Zrtzrhzm6eQMdIh8kcq3Mde/Fr8E3wR4Z2kdtZYSP3DjqeR4LfXRAIsNBGoFg==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "javascript-obfuscator": "^4.0.0"
      }
    },
    "node_modules/vite/node_modules/fdir": {
      "version": "6.5.0",
      "resolved": "https://registry.npmjs.org/fdir/-/fdir-6.5.0.tgz",
      "integrity": "sha512-tIbYtZbucOs0BRGqPJkshJUYdL+SDH7dVM8gjy+ERp3WAUjLEFJE+02kanyHtwjWOnwrKYBiwAmM0p4kLJAnXg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12.0.0"
      },
      "peerDependencies": {
        "picomatch": "^3 || ^4"
      },
      "peerDependenciesMeta": {
        "picomatch": {
          "optional": true
        }
      }
    },
    "node_modules/vite/node_modules/picomatch": {
      "version": "4.0.3",
      "resolved": "https://registry.npmjs.org/picomatch/-/picomatch-4.0.3.tgz",
      "integrity": "sha512-5gTmgEY/sqK6gFXLIsQNH19lWb4ebPDLA4SdLP7dsWkIXHWlG66oPuVvXSGFPppYZz8ZDZq0dYYrbHfBCVUb1Q==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/jonschlinkert"
      }
    },
    "node_modules/which": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/which/-/which-2.0.2.tgz",
      "integrity": "sha512-BLI3Tl1TW3Pvl70l3yq3Y64i+awpwXqsGBYWkkqMtnbXgrMD+yj7rhW0kuEDxzJaYXGjEW5ogapKNMEKNMjibA==",
      "dev": true,
      "license": "ISC",
      "dependencies": {
        "isexe": "^2.0.0"
      },
      "bin": {
        "node-which": "bin/node-which"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/which-typed-array": {
      "version": "1.1.19",
      "resolved": "https://registry.npmjs.org/which-typed-array/-/which-typed-array-1.1.19.tgz",
      "integrity": "sha512-rEvr90Bck4WZt9HHFC4DJMsjvu7x+r6bImz0/BrbWb7A2djJ8hnZMrWnHo9F8ssv0OMErasDhftrfROTyqSDrw==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "available-typed-arrays": "^1.0.7",
        "call-bind": "^1.0.8",
        "call-bound": "^1.0.4",
        "for-each": "^0.3.5",
        "get-proto": "^1.0.1",
        "gopd": "^1.2.0",
        "has-tostringtag": "^1.0.2"
      },
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/word-wrap": {
      "version": "1.2.5",
      "resolved": "https://registry.npmjs.org/word-wrap/-/word-wrap-1.2.5.tgz",
      "integrity": "sha512-BN22B5eaMMI9UMtjrGd5g5eCYPpCPDUy0FJXbYsaT5zYxjFOckS53SQDE3pWkVoWpHXVb3BrYcEN4Twa55B5cA==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/wrap-ansi": {
      "version": "8.1.0",
      "resolved": "https://registry.npmjs.org/wrap-ansi/-/wrap-ansi-8.1.0.tgz",
      "integrity": "sha512-si7QWI6zUMq56bESFvagtmzMdGOtoxfR+Sez11Mobfc7tm+VkUckk9bW2UeffTGVUbOksxmSw0AA2gs8g71NCQ==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^6.1.0",
        "string-width": "^5.0.1",
        "strip-ansi": "^7.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/wrap-ansi?sponsor=1"
      }
    },
    "node_modules/wrap-ansi-cjs": {
      "name": "wrap-ansi",
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/wrap-ansi/-/wrap-ansi-7.0.0.tgz",
      "integrity": "sha512-YVGIj2kamLSTxw6NsZjoBxfSwsn0ycdesmc4p+Q21c5zPuZ1pl+NfxVdxPtdHvmNVOQ6XSYG4AUtyt/Fi7D16Q==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^4.0.0",
        "string-width": "^4.1.0",
        "strip-ansi": "^6.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/wrap-ansi?sponsor=1"
      }
    },
    "node_modules/wrap-ansi-cjs/node_modules/emoji-regex": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-8.0.0.tgz",
      "integrity": "sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A==",
      "dev": true,
      "license": "MIT"
    },
    "node_modules/wrap-ansi-cjs/node_modules/string-width": {
      "version": "4.2.3",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-4.2.3.tgz",
      "integrity": "sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "emoji-regex": "^8.0.0",
        "is-fullwidth-code-point": "^3.0.0",
        "strip-ansi": "^6.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/wrap-ansi/node_modules/ansi-regex": {
      "version": "6.2.2",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-6.2.2.tgz",
      "integrity": "sha512-Bq3SmSpyFHaWjPk8If9yc6svM8c56dB5BAtW4Qbw5jHTwwXXcTLoRMkpDJp6VL0XzlWaCHTXrkFURMYmD0sLqg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-regex?sponsor=1"
      }
    },
    "node_modules/wrap-ansi/node_modules/ansi-styles": {
      "version": "6.2.3",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-6.2.3.tgz",
      "integrity": "sha512-4Dj6M28JB+oAH8kFkTLUo+a2jwOFkuqb3yucU0CANcRRUbxS0cP0nZYCGjcc3BNXwRIsUVmDGgzawme7zvJHvg==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-styles?sponsor=1"
      }
    },
    "node_modules/wrap-ansi/node_modules/strip-ansi": {
      "version": "7.1.2",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-7.1.2.tgz",
      "integrity": "sha512-gmBGslpoQJtgnMAvOVqGZpEz9dyoKTCzy2nfz/n8aIFhN/jCE/rCmcxabB6jOOHV+0WNnylOxaxBQPSvcWklhA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^6.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/strip-ansi?sponsor=1"
      }
    },
    "node_modules/wrappy": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/wrappy/-/wrappy-1.0.2.tgz",
      "integrity": "sha512-l4Sp/DRseor9wL6EvV2+TuQn63dMkPjZ/sp9XkghTEbV9KlPS1xUsZ3u7/IQO4wxtcFB4bgpQPRcR3QCvezPcQ==",
      "license": "ISC"
    },
    "node_modules/ws": {
      "version": "8.18.3",
      "resolved": "https://registry.npmjs.org/ws/-/ws-8.18.3.tgz",
      "integrity": "sha512-PEIGCY5tSlUt50cqyMXfCzX+oOPqN0vuGqWzbcJ2xvnkzkq46oOpz7dQaTDBdfICb4N14+GARUDw2XV2N4tvzg==",
      "license": "MIT",
      "engines": {
        "node": ">=10.0.0"
      },
      "peerDependencies": {
        "bufferutil": "^4.0.1",
        "utf-8-validate": ">=5.0.2"
      },
      "peerDependenciesMeta": {
        "bufferutil": {
          "optional": true
        },
        "utf-8-validate": {
          "optional": true
        }
      }
    },
    "node_modules/xmlchars": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/xmlchars/-/xmlchars-2.2.0.tgz",
      "integrity": "sha512-JZnDKK8B0RCDw84FNdDAIpZK+JuJw+s7Lz8nksI7SIuU3UXJJslUthsi+uWBUYOwPFwW7W7PRLRfUKpxjtjFCw==",
      "license": "MIT"
    },
    "node_modules/xtend": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/xtend/-/xtend-4.0.2.tgz",
      "integrity": "sha512-LKYU1iAXJXUgAXn9URjiu+MWhyUXHsvfp7mcuYm9dSUKK0/CjtrUwFAxD82/mCWbtLsGjFIad0wIsod4zrTAEQ==",
      "license": "MIT",
      "engines": {
        "node": ">=0.4"
      }
    },
    "node_modules/yaml": {
      "version": "2.8.1",
      "resolved": "https://registry.npmjs.org/yaml/-/yaml-2.8.1.tgz",
      "integrity": "sha512-lcYcMxX2PO9XMGvAJkJ3OsNMw+/7FKes7/hgerGUYWIoWu5j/+YQqcZr5JnPZWzOsEBgMbSbiSTn/dv/69Mkpw==",
      "dev": true,
      "license": "ISC",
      "bin": {
        "yaml": "bin.mjs"
      },
      "engines": {
        "node": ">= 14.6"
      }
    },
    "node_modules/yocto-queue": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/yocto-queue/-/yocto-queue-0.1.0.tgz",
      "integrity": "sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q==",
      "dev": true,
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/zip-stream": {
      "version": "4.1.1",
      "resolved": "https://registry.npmjs.org/zip-stream/-/zip-stream-4.1.1.tgz",
      "integrity": "sha512-9qv4rlDiopXg4E69k+vMHjNN63YFMe9sZMrdlvKnCjlCRWeCBswPPMPUfx+ipsAWq1LXHe70RcbaHdJJpS6hyQ==",
      "license": "MIT",
      "dependencies": {
        "archiver-utils": "^3.0.4",
        "compress-commons": "^4.1.2",
        "readable-stream": "^3.6.0"
      },
      "engines": {
        "node": ">= 10"
      }
    },
    "node_modules/zip-stream/node_modules/archiver-utils": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/archiver-utils/-/archiver-utils-3.0.4.tgz",
      "integrity": "sha512-KVgf4XQVrTjhyWmx6cte4RxonPLR9onExufI1jhvw/MQ4BB6IsZD5gT8Lq+u/+pRkWna/6JoHpiQioaqFP5Rzw==",
      "license": "MIT",
      "dependencies": {
        "glob": "^7.2.3",
        "graceful-fs": "^4.2.0",
        "lazystream": "^1.0.0",
        "lodash.defaults": "^4.2.0",
        "lodash.difference": "^4.5.0",
        "lodash.flatten": "^4.4.0",
        "lodash.isplainobject": "^4.0.6",
        "lodash.union": "^4.6.0",
        "normalize-path": "^3.0.0",
        "readable-stream": "^3.6.0"
      },
      "engines": {
        "node": ">= 10"
      }
    }
  }
}



================================================================
File Path: package.json
================================================================

{
  "name": "vite-react-ts-template",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "build:dev": "vite build --mode development",
    "lint": "eslint .",
    "preview": "vite preview",
    "upload-server": "node scripts/uploadServer.cjs"
  },
  "dependencies": {
    "@lumi.new/sdk": "0.2.1",
    "@supabase/supabase-js": "^2.80.0",
    "bcryptjs": "^3.0.3",
    "cors": "^2.8.5",
    "dotenv": "^17.2.3",
    "exceljs": "^4.4.0",
    "express": "^5.1.0",
    "framer-motion": "12.23.11",
    "lucide-react": "0.540.0",
    "multer": "^2.0.2",
    "papaparse": "^5.5.3",
    "react": "18.3.1",
    "react-dom": "18.3.1",
    "react-hot-toast": "2.5.2",
    "react-router-dom": "6.26.0"
  },
  "devDependencies": {
    "@eslint/js": "9.9.1",
    "@types/cors": "^2.8.19",
    "@types/express": "^5.0.5",
    "@types/multer": "^2.0.0",
    "@types/node": "^24.10.0",
    "@types/papaparse": "^5.3.14",
    "@types/react": "18.3.5",
    "@types/react-dom": "18.3.0",
    "@vitejs/plugin-react-swc": "3.11.0",
    "autoprefixer": "10.4.21",
    "eslint": "9.9.1",
    "eslint-plugin-react-hooks": "5.1.0-rc.0",
    "eslint-plugin-react-refresh": "0.4.11",
    "globals": "15.9.0",
    "postcss": "8.5.6",
    "tailwindcss": "3.4.17",
    "tsx": "^4.20.6",
    "typescript": "5.5.3",
    "typescript-eslint": "8.3.0",
    "vite": "^7.1.12",
    "vite-plugin-javascript-obfuscator": "^3.1.0",
    "vite-plugin-obfuscator": "^1.0.5"
  },
  "pnpm": {
    "overrides": {
      "@swc/core": "1.13.3"
    }
  }
}



================================================================
File Path: pnpm-lock.yaml
================================================================

lockfileVersion: '9.0'

settings:
  autoInstallPeers: true
  excludeLinksFromLockfile: false

overrides:
  '@swc/core': 1.13.3

importers:

  .:
    dependencies:
      '@lumi.new/sdk':
        specifier: 0.2.1
        version: 0.2.1
      '@supabase/supabase-js':
        specifier: ^2.80.0
        version: 2.81.1
      bcryptjs:
        specifier: ^3.0.3
        version: 3.0.3
      cors:
        specifier: ^2.8.5
        version: 2.8.5
      exceljs:
        specifier: ^4.4.0
        version: 4.4.0
      express:
        specifier: ^5.1.0
        version: 5.1.0
      framer-motion:
        specifier: 12.23.11
        version: 12.23.11(react-dom@18.3.1(react@18.3.1))(react@18.3.1)
      lucide-react:
        specifier: 0.540.0
        version: 0.540.0(react@18.3.1)
      multer:
        specifier: ^2.0.2
        version: 2.0.2
      papaparse:
        specifier: ^5.5.3
        version: 5.5.3
      react:
        specifier: 18.3.1
        version: 18.3.1
      react-dom:
        specifier: 18.3.1
        version: 18.3.1(react@18.3.1)
      react-hot-toast:
        specifier: 2.5.2
        version: 2.5.2(react-dom@18.3.1(react@18.3.1))(react@18.3.1)
      react-router-dom:
        specifier: 6.26.0
        version: 6.26.0(react-dom@18.3.1(react@18.3.1))(react@18.3.1)
    devDependencies:
      '@eslint/js':
        specifier: 9.9.1
        version: 9.9.1
      '@types/cors':
        specifier: ^2.8.19
        version: 2.8.19
      '@types/express':
        specifier: ^5.0.5
        version: 5.0.5
      '@types/multer':
        specifier: ^2.0.0
        version: 2.0.0
      '@types/node':
        specifier: ^24.10.0
        version: 24.10.1
      '@types/papaparse':
        specifier: ^5.3.14
        version: 5.5.0
      '@types/react':
        specifier: 18.3.5
        version: 18.3.5
      '@types/react-dom':
        specifier: 18.3.0
        version: 18.3.0
      '@vitejs/plugin-react-swc':
        specifier: 3.11.0
        version: 3.11.0(vite@7.2.2(@types/node@24.10.1)(jiti@1.21.7)(tsx@4.20.6)(yaml@2.8.1))
      autoprefixer:
        specifier: 10.4.21
        version: 10.4.21(postcss@8.5.6)
      eslint:
        specifier: 9.9.1
        version: 9.9.1(jiti@1.21.7)
      eslint-plugin-react-hooks:
        specifier: 5.1.0-rc.0
        version: 5.1.0-rc.0(eslint@9.9.1(jiti@1.21.7))
      eslint-plugin-react-refresh:
        specifier: 0.4.11
        version: 0.4.11(eslint@9.9.1(jiti@1.21.7))
      globals:
        specifier: 15.9.0
        version: 15.9.0
      postcss:
        specifier: 8.5.6
        version: 8.5.6
      tailwindcss:
        specifier: 3.4.17
        version: 3.4.17
      tsx:
        specifier: ^4.20.6
        version: 4.20.6
      typescript:
        specifier: 5.5.3
        version: 5.5.3
      typescript-eslint:
        specifier: 8.3.0
        version: 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      vite:
        specifier: ^7.1.12
        version: 7.2.2(@types/node@24.10.1)(jiti@1.21.7)(tsx@4.20.6)(yaml@2.8.1)
      vite-plugin-javascript-obfuscator:
        specifier: ^3.1.0
        version: 3.1.0
      vite-plugin-obfuscator:
        specifier: ^1.0.5
        version: 1.0.5

packages:

  '@alloc/quick-lru@5.2.0':
    resolution: {integrity: sha512-UrcABB+4bUrFABwbluTIBErXwvbsU/V7TZWfmbgJfbkwiBuziS9gxdODUyuiecfdGQ85jglMW6juS3+z5TsKLw==}
    engines: {node: '>=10'}

  '@esbuild/aix-ppc64@0.25.12':
    resolution: {integrity: sha512-Hhmwd6CInZ3dwpuGTF8fJG6yoWmsToE+vYgD4nytZVxcu1ulHpUQRAB1UJ8+N1Am3Mz4+xOByoQoSZf4D+CpkA==}
    engines: {node: '>=18'}
    cpu: [ppc64]
    os: [aix]

  '@esbuild/android-arm64@0.25.12':
    resolution: {integrity: sha512-6AAmLG7zwD1Z159jCKPvAxZd4y/VTO0VkprYy+3N2FtJ8+BQWFXU+OxARIwA46c5tdD9SsKGZ/1ocqBS/gAKHg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [android]

  '@esbuild/android-arm@0.25.12':
    resolution: {integrity: sha512-VJ+sKvNA/GE7Ccacc9Cha7bpS8nyzVv0jdVgwNDaR4gDMC/2TTRc33Ip8qrNYUcpkOHUT5OZ0bUcNNVZQ9RLlg==}
    engines: {node: '>=18'}
    cpu: [arm]
    os: [android]

  '@esbuild/android-x64@0.25.12':
    resolution: {integrity: sha512-5jbb+2hhDHx5phYR2By8GTWEzn6I9UqR11Kwf22iKbNpYrsmRB18aX/9ivc5cabcUiAT/wM+YIZ6SG9QO6a8kg==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [android]

  '@esbuild/darwin-arm64@0.25.12':
    resolution: {integrity: sha512-N3zl+lxHCifgIlcMUP5016ESkeQjLj/959RxxNYIthIg+CQHInujFuXeWbWMgnTo4cp5XVHqFPmpyu9J65C1Yg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [darwin]

  '@esbuild/darwin-x64@0.25.12':
    resolution: {integrity: sha512-HQ9ka4Kx21qHXwtlTUVbKJOAnmG1ipXhdWTmNXiPzPfWKpXqASVcWdnf2bnL73wgjNrFXAa3yYvBSd9pzfEIpA==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [darwin]

  '@esbuild/freebsd-arm64@0.25.12':
    resolution: {integrity: sha512-gA0Bx759+7Jve03K1S0vkOu5Lg/85dou3EseOGUes8flVOGxbhDDh/iZaoek11Y8mtyKPGF3vP8XhnkDEAmzeg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [freebsd]

  '@esbuild/freebsd-x64@0.25.12':
    resolution: {integrity: sha512-TGbO26Yw2xsHzxtbVFGEXBFH0FRAP7gtcPE7P5yP7wGy7cXK2oO7RyOhL5NLiqTlBh47XhmIUXuGciXEqYFfBQ==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [freebsd]

  '@esbuild/linux-arm64@0.25.12':
    resolution: {integrity: sha512-8bwX7a8FghIgrupcxb4aUmYDLp8pX06rGh5HqDT7bB+8Rdells6mHvrFHHW2JAOPZUbnjUpKTLg6ECyzvas2AQ==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [linux]

  '@esbuild/linux-arm@0.25.12':
    resolution: {integrity: sha512-lPDGyC1JPDou8kGcywY0YILzWlhhnRjdof3UlcoqYmS9El818LLfJJc3PXXgZHrHCAKs/Z2SeZtDJr5MrkxtOw==}
    engines: {node: '>=18'}
    cpu: [arm]
    os: [linux]

  '@esbuild/linux-ia32@0.25.12':
    resolution: {integrity: sha512-0y9KrdVnbMM2/vG8KfU0byhUN+EFCny9+8g202gYqSSVMonbsCfLjUO+rCci7pM0WBEtz+oK/PIwHkzxkyharA==}
    engines: {node: '>=18'}
    cpu: [ia32]
    os: [linux]

  '@esbuild/linux-loong64@0.25.12':
    resolution: {integrity: sha512-h///Lr5a9rib/v1GGqXVGzjL4TMvVTv+s1DPoxQdz7l/AYv6LDSxdIwzxkrPW438oUXiDtwM10o9PmwS/6Z0Ng==}
    engines: {node: '>=18'}
    cpu: [loong64]
    os: [linux]

  '@esbuild/linux-mips64el@0.25.12':
    resolution: {integrity: sha512-iyRrM1Pzy9GFMDLsXn1iHUm18nhKnNMWscjmp4+hpafcZjrr2WbT//d20xaGljXDBYHqRcl8HnxbX6uaA/eGVw==}
    engines: {node: '>=18'}
    cpu: [mips64el]
    os: [linux]

  '@esbuild/linux-ppc64@0.25.12':
    resolution: {integrity: sha512-9meM/lRXxMi5PSUqEXRCtVjEZBGwB7P/D4yT8UG/mwIdze2aV4Vo6U5gD3+RsoHXKkHCfSxZKzmDssVlRj1QQA==}
    engines: {node: '>=18'}
    cpu: [ppc64]
    os: [linux]

  '@esbuild/linux-riscv64@0.25.12':
    resolution: {integrity: sha512-Zr7KR4hgKUpWAwb1f3o5ygT04MzqVrGEGXGLnj15YQDJErYu/BGg+wmFlIDOdJp0PmB0lLvxFIOXZgFRrdjR0w==}
    engines: {node: '>=18'}
    cpu: [riscv64]
    os: [linux]

  '@esbuild/linux-s390x@0.25.12':
    resolution: {integrity: sha512-MsKncOcgTNvdtiISc/jZs/Zf8d0cl/t3gYWX8J9ubBnVOwlk65UIEEvgBORTiljloIWnBzLs4qhzPkJcitIzIg==}
    engines: {node: '>=18'}
    cpu: [s390x]
    os: [linux]

  '@esbuild/linux-x64@0.25.12':
    resolution: {integrity: sha512-uqZMTLr/zR/ed4jIGnwSLkaHmPjOjJvnm6TVVitAa08SLS9Z0VM8wIRx7gWbJB5/J54YuIMInDquWyYvQLZkgw==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [linux]

  '@esbuild/netbsd-arm64@0.25.12':
    resolution: {integrity: sha512-xXwcTq4GhRM7J9A8Gv5boanHhRa/Q9KLVmcyXHCTaM4wKfIpWkdXiMog/KsnxzJ0A1+nD+zoecuzqPmCRyBGjg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [netbsd]

  '@esbuild/netbsd-x64@0.25.12':
    resolution: {integrity: sha512-Ld5pTlzPy3YwGec4OuHh1aCVCRvOXdH8DgRjfDy/oumVovmuSzWfnSJg+VtakB9Cm0gxNO9BzWkj6mtO1FMXkQ==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [netbsd]

  '@esbuild/openbsd-arm64@0.25.12':
    resolution: {integrity: sha512-fF96T6KsBo/pkQI950FARU9apGNTSlZGsv1jZBAlcLL1MLjLNIWPBkj5NlSz8aAzYKg+eNqknrUJ24QBybeR5A==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [openbsd]

  '@esbuild/openbsd-x64@0.25.12':
    resolution: {integrity: sha512-MZyXUkZHjQxUvzK7rN8DJ3SRmrVrke8ZyRusHlP+kuwqTcfWLyqMOE3sScPPyeIXN/mDJIfGXvcMqCgYKekoQw==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [openbsd]

  '@esbuild/openharmony-arm64@0.25.12':
    resolution: {integrity: sha512-rm0YWsqUSRrjncSXGA7Zv78Nbnw4XL6/dzr20cyrQf7ZmRcsovpcRBdhD43Nuk3y7XIoW2OxMVvwuRvk9XdASg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [openharmony]

  '@esbuild/sunos-x64@0.25.12':
    resolution: {integrity: sha512-3wGSCDyuTHQUzt0nV7bocDy72r2lI33QL3gkDNGkod22EsYl04sMf0qLb8luNKTOmgF/eDEDP5BFNwoBKH441w==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [sunos]

  '@esbuild/win32-arm64@0.25.12':
    resolution: {integrity: sha512-rMmLrur64A7+DKlnSuwqUdRKyd3UE7oPJZmnljqEptesKM8wx9J8gx5u0+9Pq0fQQW8vqeKebwNXdfOyP+8Bsg==}
    engines: {node: '>=18'}
    cpu: [arm64]
    os: [win32]

  '@esbuild/win32-ia32@0.25.12':
    resolution: {integrity: sha512-HkqnmmBoCbCwxUKKNPBixiWDGCpQGVsrQfJoVGYLPT41XWF8lHuE5N6WhVia2n4o5QK5M4tYr21827fNhi4byQ==}
    engines: {node: '>=18'}
    cpu: [ia32]
    os: [win32]

  '@esbuild/win32-x64@0.25.12':
    resolution: {integrity: sha512-alJC0uCZpTFrSL0CCDjcgleBXPnCrEAhTBILpeAp7M/OFgoqtAetfBzX0xM00MUsVVPpVjlPuMbREqnZCXaTnA==}
    engines: {node: '>=18'}
    cpu: [x64]
    os: [win32]

  '@eslint-community/eslint-utils@4.9.0':
    resolution: {integrity: sha512-ayVFHdtZ+hsq1t2Dy24wCmGXGe4q9Gu3smhLYALJrr473ZH27MsnSL+LKUlimp4BWJqMDMLmPpx/Q9R3OAlL4g==}
    engines: {node: ^12.22.0 || ^14.17.0 || >=16.0.0}
    peerDependencies:
      eslint: ^6.0.0 || ^7.0.0 || >=8.0.0

  '@eslint-community/regexpp@4.12.2':
    resolution: {integrity: sha512-EriSTlt5OC9/7SXkRSCAhfSxxoSUgBm33OH+IkwbdpgoqsSsUg7y3uh+IICI/Qg4BBWr3U2i39RpmycbxMq4ew==}
    engines: {node: ^12.0.0 || ^14.0.0 || >=16.0.0}

  '@eslint/config-array@0.18.0':
    resolution: {integrity: sha512-fTxvnS1sRMu3+JjXwJG0j/i4RT9u4qJ+lqS/yCGap4lH4zZGzQ7tu+xZqQmcMZq5OBZDL4QRxQzRjkWcGt8IVw==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@eslint/eslintrc@3.3.1':
    resolution: {integrity: sha512-gtF186CXhIl1p4pJNGZw8Yc6RlshoePRvE0X91oPGb3vZ8pM3qOS9W9NGPat9LziaBV7XrJWGylNQXkGcnM3IQ==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@eslint/js@9.9.1':
    resolution: {integrity: sha512-xIDQRsfg5hNBqHz04H1R3scSVwmI+KUbqjsQKHKQ1DAUSaUjYPReZZmS/5PNiKu1fUvzDd6H7DEDKACSEhu+TQ==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@eslint/object-schema@2.1.7':
    resolution: {integrity: sha512-VtAOaymWVfZcmZbp6E2mympDIHvyjXs/12LqWYjVw6qjrfF+VK+fyG33kChz3nnK+SU5/NeHOqrTEHS8sXO3OA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@fast-csv/format@4.3.5':
    resolution: {integrity: sha512-8iRn6QF3I8Ak78lNAa+Gdl5MJJBM5vRHivFtMRUWINdevNo00K7OXxS2PshawLKTejVwieIlPmK5YlLu6w4u8A==}

  '@fast-csv/parse@4.3.6':
    resolution: {integrity: sha512-uRsLYksqpbDmWaSmzvJcuApSEe38+6NQZBUsuAyMZKqHxH0g1wcJgsKUvN3WC8tewaqFjBMMGrkHmC+T7k8LvA==}

  '@humanwhocodes/module-importer@1.0.1':
    resolution: {integrity: sha512-bxveV4V8v5Yb4ncFTT3rPSgZBOpCkjfK0y4oVVVJwIuDVBRMDXrPyXRL988i5ap9m9bnyEEjWfm5WkBmtffLfA==}
    engines: {node: '>=12.22'}

  '@humanwhocodes/retry@0.3.1':
    resolution: {integrity: sha512-JBxkERygn7Bv/GbN5Rv8Ul6LVknS+5Bp6RgDC/O8gEBU/yeH5Ui5C/OlWrTb6qct7LjjfT6Re2NxB0ln0yYybA==}
    engines: {node: '>=18.18'}

  '@isaacs/cliui@8.0.2':
    resolution: {integrity: sha512-O8jcjabXaleOG9DQ0+ARXWZBTfnP4WNAqzuiJK7ll44AmxGKv/J2M4TPjxjY3znBCfvBXFzucm1twdyFybFqEA==}
    engines: {node: '>=12'}

  '@javascript-obfuscator/escodegen@2.3.0':
    resolution: {integrity: sha512-QVXwMIKqYMl3KwtTirYIA6gOCiJ0ZDtptXqAv/8KWLG9uQU2fZqTVy7a/A5RvcoZhbDoFfveTxuGxJ5ibzQtkw==}
    engines: {node: '>=6.0'}

  '@javascript-obfuscator/estraverse@5.4.0':
    resolution: {integrity: sha512-CZFX7UZVN9VopGbjTx4UXaXsi9ewoM1buL0kY7j1ftYdSs7p2spv9opxFjHlQ/QGTgh4UqufYqJJ0WKLml7b6w==}
    engines: {node: '>=4.0'}

  '@jridgewell/gen-mapping@0.3.13':
    resolution: {integrity: sha512-2kkt/7niJ6MgEPxF0bYdQ6etZaA+fQvDcLKckhy1yIQOzaoKjBBjSj63/aLVjYE3qhRt5dvM+uUyfCg6UKCBbA==}

  '@jridgewell/resolve-uri@3.1.2':
    resolution: {integrity: sha512-bRISgCIjP20/tbWSPWMEi54QVPRZExkuD9lJL+UIxUKtwVJA8wW1Trb1jMs1RFXo1CBTNZ/5hpC9QvmKWdopKw==}
    engines: {node: '>=6.0.0'}

  '@jridgewell/sourcemap-codec@1.5.5':
    resolution: {integrity: sha512-cYQ9310grqxueWbl+WuIUIaiUaDcj7WOq5fVhEljNVgRfOUhY9fy2zTvfoqWsnebh8Sl70VScFbICvJnLKB0Og==}

  '@jridgewell/trace-mapping@0.3.31':
    resolution: {integrity: sha512-zzNR+SdQSDJzc8joaeP8QQoCQr8NuYx2dIIytl1QeBEZHJ9uW6hebsrYgbz8hJwUQao3TWCMtmfV8Nu1twOLAw==}

  '@lumi.new/sdk@0.2.1':
    resolution: {integrity: sha512-FSqGe/3fudj989JQRBaIix8e7IA0UW1r8saZD2Nvy7nfhuHsGnDDhB33xTzmmpTSc0w06+GnFVK0cMvxXCqqGA==}

  '@nodelib/fs.scandir@2.1.5':
    resolution: {integrity: sha512-vq24Bq3ym5HEQm2NKCr3yXDwjc7vTsEThRDnkp2DK9p1uqLR+DHurm/NOTo0KG7HYHU7eppKZj3MyqYuMBf62g==}
    engines: {node: '>= 8'}

  '@nodelib/fs.stat@2.0.5':
    resolution: {integrity: sha512-RkhPPp2zrqDAQA/2jNhnztcPAlv64XdhIp7a7454A5ovI7Bukxgt7MX7udwAu3zg1DcpPU0rz3VV1SeaqvY4+A==}
    engines: {node: '>= 8'}

  '@nodelib/fs.walk@1.2.8':
    resolution: {integrity: sha512-oGB+UxlgWcgQkgwo8GcEGwemoTFt3FIO9ababBmaGwXIoBKZ+GTy0pP185beGg7Llih/NSHSV2XAs1lnznocSg==}
    engines: {node: '>= 8'}

  '@pkgjs/parseargs@0.11.0':
    resolution: {integrity: sha512-+1VkjdD0QBLPodGrJUeqarH8VAIvQODIbwh9XpP5Syisf7YoQgsJKPNFoqqLQlu+VQ/tVSshMR6loPMn8U+dPg==}
    engines: {node: '>=14'}

  '@remix-run/router@1.19.0':
    resolution: {integrity: sha512-zDICCLKEwbVYTS6TjYaWtHXxkdoUvD/QXvyVZjGCsWz5vyH7aFeONlPffPdW+Y/t6KT0MgXb2Mfjun9YpWN1dA==}
    engines: {node: '>=14.0.0'}

  '@rolldown/pluginutils@1.0.0-beta.27':
    resolution: {integrity: sha512-+d0F4MKMCbeVUJwG96uQ4SgAznZNSq93I3V+9NHA4OpvqG8mRCpGdKmK8l/dl02h2CCDHwW2FqilnTyDcAnqjA==}

  '@rollup/rollup-android-arm-eabi@4.53.2':
    resolution: {integrity: sha512-yDPzwsgiFO26RJA4nZo8I+xqzh7sJTZIWQOxn+/XOdPE31lAvLIYCKqjV+lNH/vxE2L2iH3plKxDCRK6i+CwhA==}
    cpu: [arm]
    os: [android]

  '@rollup/rollup-android-arm64@4.53.2':
    resolution: {integrity: sha512-k8FontTxIE7b0/OGKeSN5B6j25EuppBcWM33Z19JoVT7UTXFSo3D9CdU39wGTeb29NO3XxpMNauh09B+Ibw+9g==}
    cpu: [arm64]
    os: [android]

  '@rollup/rollup-darwin-arm64@4.53.2':
    resolution: {integrity: sha512-A6s4gJpomNBtJ2yioj8bflM2oogDwzUiMl2yNJ2v9E7++sHrSrsQ29fOfn5DM/iCzpWcebNYEdXpaK4tr2RhfQ==}
    cpu: [arm64]
    os: [darwin]

  '@rollup/rollup-darwin-x64@4.53.2':
    resolution: {integrity: sha512-e6XqVmXlHrBlG56obu9gDRPW3O3hLxpwHpLsBJvuI8qqnsrtSZ9ERoWUXtPOkY8c78WghyPHZdmPhHLWNdAGEw==}
    cpu: [x64]
    os: [darwin]

  '@rollup/rollup-freebsd-arm64@4.53.2':
    resolution: {integrity: sha512-v0E9lJW8VsrwPux5Qe5CwmH/CF/2mQs6xU1MF3nmUxmZUCHazCjLgYvToOk+YuuUqLQBio1qkkREhxhc656ViA==}
    cpu: [arm64]
    os: [freebsd]

  '@rollup/rollup-freebsd-x64@4.53.2':
    resolution: {integrity: sha512-ClAmAPx3ZCHtp6ysl4XEhWU69GUB1D+s7G9YjHGhIGCSrsg00nEGRRZHmINYxkdoJehde8VIsDC5t9C0gb6yqA==}
    cpu: [x64]
    os: [freebsd]

  '@rollup/rollup-linux-arm-gnueabihf@4.53.2':
    resolution: {integrity: sha512-EPlb95nUsz6Dd9Qy13fI5kUPXNSljaG9FiJ4YUGU1O/Q77i5DYFW5KR8g1OzTcdZUqQQ1KdDqsTohdFVwCwjqg==}
    cpu: [arm]
    os: [linux]

  '@rollup/rollup-linux-arm-musleabihf@4.53.2':
    resolution: {integrity: sha512-BOmnVW+khAUX+YZvNfa0tGTEMVVEerOxN0pDk2E6N6DsEIa2Ctj48FOMfNDdrwinocKaC7YXUZ1pHlKpnkja/Q==}
    cpu: [arm]
    os: [linux]

  '@rollup/rollup-linux-arm64-gnu@4.53.2':
    resolution: {integrity: sha512-Xt2byDZ+6OVNuREgBXr4+CZDJtrVso5woFtpKdGPhpTPHcNG7D8YXeQzpNbFRxzTVqJf7kvPMCub/pcGUWgBjA==}
    cpu: [arm64]
    os: [linux]

  '@rollup/rollup-linux-arm64-musl@4.53.2':
    resolution: {integrity: sha512-+LdZSldy/I9N8+klim/Y1HsKbJ3BbInHav5qE9Iy77dtHC/pibw1SR/fXlWyAk0ThnpRKoODwnAuSjqxFRDHUQ==}
    cpu: [arm64]
    os: [linux]

  '@rollup/rollup-linux-loong64-gnu@4.53.2':
    resolution: {integrity: sha512-8ms8sjmyc1jWJS6WdNSA23rEfdjWB30LH8Wqj0Cqvv7qSHnvw6kgMMXRdop6hkmGPlyYBdRPkjJnj3KCUHV/uQ==}
    cpu: [loong64]
    os: [linux]

  '@rollup/rollup-linux-ppc64-gnu@4.53.2':
    resolution: {integrity: sha512-3HRQLUQbpBDMmzoxPJYd3W6vrVHOo2cVW8RUo87Xz0JPJcBLBr5kZ1pGcQAhdZgX9VV7NbGNipah1omKKe23/g==}
    cpu: [ppc64]
    os: [linux]

  '@rollup/rollup-linux-riscv64-gnu@4.53.2':
    resolution: {integrity: sha512-fMjKi+ojnmIvhk34gZP94vjogXNNUKMEYs+EDaB/5TG/wUkoeua7p7VCHnE6T2Tx+iaghAqQX8teQzcvrYpaQA==}
    cpu: [riscv64]
    os: [linux]

  '@rollup/rollup-linux-riscv64-musl@4.53.2':
    resolution: {integrity: sha512-XuGFGU+VwUUV5kLvoAdi0Wz5Xbh2SrjIxCtZj6Wq8MDp4bflb/+ThZsVxokM7n0pcbkEr2h5/pzqzDYI7cCgLQ==}
    cpu: [riscv64]
    os: [linux]

  '@rollup/rollup-linux-s390x-gnu@4.53.2':
    resolution: {integrity: sha512-w6yjZF0P+NGzWR3AXWX9zc0DNEGdtvykB03uhonSHMRa+oWA6novflo2WaJr6JZakG2ucsyb+rvhrKac6NIy+w==}
    cpu: [s390x]
    os: [linux]

  '@rollup/rollup-linux-x64-gnu@4.53.2':
    resolution: {integrity: sha512-yo8d6tdfdeBArzC7T/PnHd7OypfI9cbuZzPnzLJIyKYFhAQ8SvlkKtKBMbXDxe1h03Rcr7u++nFS7tqXz87Gtw==}
    cpu: [x64]
    os: [linux]

  '@rollup/rollup-linux-x64-musl@4.53.2':
    resolution: {integrity: sha512-ah59c1YkCxKExPP8O9PwOvs+XRLKwh/mV+3YdKqQ5AMQ0r4M4ZDuOrpWkUaqO7fzAHdINzV9tEVu8vNw48z0lA==}
    cpu: [x64]
    os: [linux]

  '@rollup/rollup-openharmony-arm64@4.53.2':
    resolution: {integrity: sha512-4VEd19Wmhr+Zy7hbUsFZ6YXEiP48hE//KPLCSVNY5RMGX2/7HZ+QkN55a3atM1C/BZCGIgqN+xrVgtdak2S9+A==}
    cpu: [arm64]
    os: [openharmony]

  '@rollup/rollup-win32-arm64-msvc@4.53.2':
    resolution: {integrity: sha512-IlbHFYc/pQCgew/d5fslcy1KEaYVCJ44G8pajugd8VoOEI8ODhtb/j8XMhLpwHCMB3yk2J07ctup10gpw2nyMA==}
    cpu: [arm64]
    os: [win32]

  '@rollup/rollup-win32-ia32-msvc@4.53.2':
    resolution: {integrity: sha512-lNlPEGgdUfSzdCWU176ku/dQRnA7W+Gp8d+cWv73jYrb8uT7HTVVxq62DUYxjbaByuf1Yk0RIIAbDzp+CnOTFg==}
    cpu: [ia32]
    os: [win32]

  '@rollup/rollup-win32-x64-gnu@4.53.2':
    resolution: {integrity: sha512-S6YojNVrHybQis2lYov1sd+uj7K0Q05NxHcGktuMMdIQ2VixGwAfbJ23NnlvvVV1bdpR2m5MsNBViHJKcA4ADw==}
    cpu: [x64]
    os: [win32]

  '@rollup/rollup-win32-x64-msvc@4.53.2':
    resolution: {integrity: sha512-k+/Rkcyx//P6fetPoLMb8pBeqJBNGx81uuf7iljX9++yNBVRDQgD04L+SVXmXmh5ZP4/WOp4mWF0kmi06PW2tA==}
    cpu: [x64]
    os: [win32]

  '@supabase/auth-js@2.81.1':
    resolution: {integrity: sha512-K20GgiSm9XeRLypxYHa5UCnybWc2K0ok0HLbqCej/wRxDpJxToXNOwKt0l7nO8xI1CyQ+GrNfU6bcRzvdbeopQ==}
    engines: {node: '>=20.0.0'}

  '@supabase/functions-js@2.81.1':
    resolution: {integrity: sha512-sYgSO3mlgL0NvBFS3oRfCK4OgKGQwuOWJLzfPyWg0k8MSxSFSDeN/JtrDJD5GQrxskP6c58+vUzruBJQY78AqQ==}
    engines: {node: '>=20.0.0'}

  '@supabase/postgrest-js@2.81.1':
    resolution: {integrity: sha512-DePpUTAPXJyBurQ4IH2e42DWoA+/Qmr5mbgY4B6ZcxVc/ZUKfTVK31BYIFBATMApWraFc8Q/Sg+yxtfJ3E0wSg==}
    engines: {node: '>=20.0.0'}

  '@supabase/realtime-js@2.81.1':
    resolution: {integrity: sha512-ViQ+Kxm8BuUP/TcYmH9tViqYKGSD1LBjdqx2p5J+47RES6c+0QHedM0PPAjthMdAHWyb2LGATE9PD2++2rO/tw==}
    engines: {node: '>=20.0.0'}

  '@supabase/storage-js@2.81.1':
    resolution: {integrity: sha512-UNmYtjnZnhouqnbEMC1D5YJot7y0rIaZx7FG2Fv8S3hhNjcGVvO+h9We/tggi273BFkiahQPS/uRsapo1cSapw==}
    engines: {node: '>=20.0.0'}

  '@supabase/supabase-js@2.81.1':
    resolution: {integrity: sha512-KSdY7xb2L0DlLmlYzIOghdw/na4gsMcqJ8u4sD6tOQJr+x3hLujU9s4R8N3ob84/1bkvpvlU5PYKa1ae+OICnw==}
    engines: {node: '>=20.0.0'}

  '@swc/core-darwin-arm64@1.13.3':
    resolution: {integrity: sha512-ux0Ws4pSpBTqbDS9GlVP354MekB1DwYlbxXU3VhnDr4GBcCOimpocx62x7cFJkSpEBF8bmX8+/TTCGKh4PbyXw==}
    engines: {node: '>=10'}
    cpu: [arm64]
    os: [darwin]

  '@swc/core-darwin-x64@1.13.3':
    resolution: {integrity: sha512-p0X6yhxmNUOMZrbeZ3ZNsPige8lSlSe1llllXvpCLkKKxN/k5vZt1sULoq6Nj4eQ7KeHQVm81/+AwKZyf/e0TA==}
    engines: {node: '>=10'}
    cpu: [x64]
    os: [darwin]

  '@swc/core-linux-arm-gnueabihf@1.13.3':
    resolution: {integrity: sha512-OmDoiexL2fVWvQTCtoh0xHMyEkZweQAlh4dRyvl8ugqIPEVARSYtaj55TBMUJIP44mSUOJ5tytjzhn2KFxFcBA==}
    engines: {node: '>=10'}
    cpu: [arm]
    os: [linux]

  '@swc/core-linux-arm64-gnu@1.13.3':
    resolution: {integrity: sha512-STfKku3QfnuUj6k3g9ld4vwhtgCGYIFQmsGPPgT9MK/dI3Lwnpe5Gs5t1inoUIoGNP8sIOLlBB4HV4MmBjQuhw==}
    engines: {node: '>=10'}
    cpu: [arm64]
    os: [linux]

  '@swc/core-linux-arm64-musl@1.13.3':
    resolution: {integrity: sha512-bc+CXYlFc1t8pv9yZJGus372ldzOVscBl7encUBlU1m/Sig0+NDJLz6cXXRcFyl6ABNOApWeR4Yl7iUWx6C8og==}
    engines: {node: '>=10'}
    cpu: [arm64]
    os: [linux]

  '@swc/core-linux-x64-gnu@1.13.3':
    resolution: {integrity: sha512-dFXoa0TEhohrKcxn/54YKs1iwNeW6tUkHJgXW33H381SvjKFUV53WR231jh1sWVJETjA3vsAwxKwR23s7UCmUA==}
    engines: {node: '>=10'}
    cpu: [x64]
    os: [linux]

  '@swc/core-linux-x64-musl@1.13.3':
    resolution: {integrity: sha512-ieyjisLB+ldexiE/yD8uomaZuZIbTc8tjquYln9Quh5ykOBY7LpJJYBWvWtm1g3pHv6AXlBI8Jay7Fffb6aLfA==}
    engines: {node: '>=10'}
    cpu: [x64]
    os: [linux]

  '@swc/core-win32-arm64-msvc@1.13.3':
    resolution: {integrity: sha512-elTQpnaX5vESSbhCEgcwXjpMsnUbqqHfEpB7ewpkAsLzKEXZaK67ihSRYAuAx6ewRQTo7DS5iTT6X5aQD3MzMw==}
    engines: {node: '>=10'}
    cpu: [arm64]
    os: [win32]

  '@swc/core-win32-ia32-msvc@1.13.3':
    resolution: {integrity: sha512-nvehQVEOdI1BleJpuUgPLrclJ0TzbEMc+MarXDmmiRFwEUGqj+pnfkTSb7RZyS1puU74IXdK/YhTirHurtbI9w==}
    engines: {node: '>=10'}
    cpu: [ia32]
    os: [win32]

  '@swc/core-win32-x64-msvc@1.13.3':
    resolution: {integrity: sha512-A+JSKGkRbPLVV2Kwx8TaDAV0yXIXm/gc8m98hSkVDGlPBBmydgzNdWy3X7HTUBM7IDk7YlWE7w2+RUGjdgpTmg==}
    engines: {node: '>=10'}
    cpu: [x64]
    os: [win32]

  '@swc/core@1.13.3':
    resolution: {integrity: sha512-ZaDETVWnm6FE0fc+c2UE8MHYVS3Fe91o5vkmGfgwGXFbxYvAjKSqxM/j4cRc9T7VZNSJjriXq58XkfCp3Y6f+w==}
    engines: {node: '>=10'}
    peerDependencies:
      '@swc/helpers': '>=0.5.17'
    peerDependenciesMeta:
      '@swc/helpers':
        optional: true

  '@swc/counter@0.1.3':
    resolution: {integrity: sha512-e2BR4lsJkkRlKZ/qCHPw9ZaSxc0MVUd7gtbtaB7aMvHeJVYe8sOB8DBZkP2DtISHGSku9sCK6T6cnY0CtXrOCQ==}

  '@swc/types@0.1.25':
    resolution: {integrity: sha512-iAoY/qRhNH8a/hBvm3zKj9qQ4oc2+3w1unPJa2XvTK3XjeLXtzcCingVPw/9e5mn1+0yPqxcBGp9Jf0pkfMb1g==}

  '@types/body-parser@1.19.6':
    resolution: {integrity: sha512-HLFeCYgz89uk22N5Qg3dvGvsv46B8GLvKKo1zKG4NybA8U2DiEO3w9lqGg29t/tfLRJpJ6iQxnVw4OnB7MoM9g==}

  '@types/connect@3.4.38':
    resolution: {integrity: sha512-K6uROf1LD88uDQqJCktA4yzL1YYAK6NgfsI0v/mTgyPKWsX1CnJ0XPSDhViejru1GcRkLWb8RlzFYJRqGUbaug==}

  '@types/cors@2.8.19':
    resolution: {integrity: sha512-mFNylyeyqN93lfe/9CSxOGREz8cpzAhH+E93xJ4xWQf62V8sQ/24reV2nyzUWM6H6Xji+GGHpkbLe7pVoUEskg==}

  '@types/estree@1.0.8':
    resolution: {integrity: sha512-dWHzHa2WqEXI/O1E9OjrocMTKJl2mSrEolh1Iomrv6U+JuNwaHXsXx9bLu5gG7BUWFIN0skIQJQ/L1rIex4X6w==}

  '@types/express-serve-static-core@5.1.0':
    resolution: {integrity: sha512-jnHMsrd0Mwa9Cf4IdOzbz543y4XJepXrbia2T4b6+spXC2We3t1y6K44D3mR8XMFSXMCf3/l7rCgddfx7UNVBA==}

  '@types/express@5.0.5':
    resolution: {integrity: sha512-LuIQOcb6UmnF7C1PCFmEU1u2hmiHL43fgFQX67sN3H4Z+0Yk0Neo++mFsBjhOAuLzvlQeqAAkeDOZrJs9rzumQ==}

  '@types/http-errors@2.0.5':
    resolution: {integrity: sha512-r8Tayk8HJnX0FztbZN7oVqGccWgw98T/0neJphO91KkmOzug1KkofZURD4UaD5uH8AqcFLfdPErnBod0u71/qg==}

  '@types/mime@1.3.5':
    resolution: {integrity: sha512-/pyBZWSLD2n0dcHE3hq8s8ZvcETHtEuF+3E7XVt0Ig2nvsVQXdghHVcEkIWjy9A0wKfTn97a/PSDYohKIlnP/w==}

  '@types/minimatch@3.0.5':
    resolution: {integrity: sha512-Klz949h02Gz2uZCMGwDUSDS1YBlTdDDgbWHi+81l29tQALUtvz4rAYi5uoVhE5Lagoq6DeqAUlbrHvW/mXDgdQ==}

  '@types/multer@2.0.0':
    resolution: {integrity: sha512-C3Z9v9Evij2yST3RSBktxP9STm6OdMc5uR1xF1SGr98uv8dUlAL2hqwrZ3GVB3uyMyiegnscEK6PGtYvNrjTjw==}

  '@types/node@14.18.63':
    resolution: {integrity: sha512-fAtCfv4jJg+ExtXhvCkCqUKZ+4ok/JQk01qDKhL5BDDoS3AxKXhV5/MAVUZyQnSEd2GT92fkgZl0pz0Q0AzcIQ==}

  '@types/node@24.10.1':
    resolution: {integrity: sha512-GNWcUTRBgIRJD5zj+Tq0fKOJ5XZajIiBroOF0yvj2bSU1WvNdYS/dn9UxwsujGW4JX06dnHyjV2y9rRaybH0iQ==}

  '@types/papaparse@5.5.0':
    resolution: {integrity: sha512-GVs5iMQmUr54BAZYYkByv8zPofFxmyxUpISPb2oh8sayR3+1zbxasrOvoKiHJ/nnoq/uULuPsu1Lze1EkagVFg==}

  '@types/phoenix@1.6.6':
    resolution: {integrity: sha512-PIzZZlEppgrpoT2QgbnDU+MMzuR6BbCjllj0bM70lWoejMeNJAxCchxnv7J3XFkI8MpygtRpzXrIlmWUBclP5A==}

  '@types/prop-types@15.7.15':
    resolution: {integrity: sha512-F6bEyamV9jKGAFBEmlQnesRPGOQqS2+Uwi0Em15xenOxHaf2hv6L8YCVn3rPdPJOiJfPiCnLIRyvwVaqMY3MIw==}

  '@types/qs@6.14.0':
    resolution: {integrity: sha512-eOunJqu0K1923aExK6y8p6fsihYEn/BYuQ4g0CxAAgFc4b/ZLN4CrsRZ55srTdqoiLzU2B2evC+apEIxprEzkQ==}

  '@types/range-parser@1.2.7':
    resolution: {integrity: sha512-hKormJbkJqzQGhziax5PItDUTMAM9uE2XXQmM37dyd4hVM+5aVl7oVxMVUiVQn2oCQFN/LKCZdvSM0pFRqbSmQ==}

  '@types/react-dom@18.3.0':
    resolution: {integrity: sha512-EhwApuTmMBmXuFOikhQLIBUn6uFg81SwLMOAUgodJF14SOBOCMdU04gDoYi0WOJJHD144TL32z4yDqCW3dnkQg==}

  '@types/react@18.3.5':
    resolution: {integrity: sha512-WeqMfGJLGuLCqHGYRGHxnKrXcTitc6L/nBUWfWPcTarG3t9PsquqUMuVeXZeca+mglY4Vo5GZjCi0A3Or2lnxA==}

  '@types/send@0.17.6':
    resolution: {integrity: sha512-Uqt8rPBE8SY0RK8JB1EzVOIZ32uqy8HwdxCnoCOsYrvnswqmFZ/k+9Ikidlk/ImhsdvBsloHbAlewb2IEBV/Og==}

  '@types/send@1.2.1':
    resolution: {integrity: sha512-arsCikDvlU99zl1g69TcAB3mzZPpxgw0UQnaHeC1Nwb015xp8bknZv5rIfri9xTOcMuaVgvabfIRA7PSZVuZIQ==}

  '@types/serve-static@1.15.10':
    resolution: {integrity: sha512-tRs1dB+g8Itk72rlSI2ZrW6vZg0YrLI81iQSTkMmOqnqCaNr/8Ek4VwWcN5vZgCYWbg/JJSGBlUaYGAOP73qBw==}

  '@types/validator@13.15.9':
    resolution: {integrity: sha512-9ENIuq9PUX45M1QRtfJDprgfErED4fBiMPmjlPci4W9WiBelVtHYCjF3xkQNcSnmUeuruLS1kH6hSl5M1vz4Sw==}

  '@types/ws@8.18.1':
    resolution: {integrity: sha512-ThVF6DCVhA8kUGy+aazFQ4kXQ7E1Ty7A3ypFOe0IcJV8O/M511G99AW24irKrW56Wt44yG9+ij8FaqoBGkuBXg==}

  '@typescript-eslint/eslint-plugin@8.3.0':
    resolution: {integrity: sha512-FLAIn63G5KH+adZosDYiutqkOkYEx0nvcwNNfJAf+c7Ae/H35qWwTYvPZUKFj5AS+WfHG/WJJfWnDnyNUlp8UA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      '@typescript-eslint/parser': ^8.0.0 || ^8.0.0-alpha.0
      eslint: ^8.57.0 || ^9.0.0
      typescript: '*'
    peerDependenciesMeta:
      typescript:
        optional: true

  '@typescript-eslint/parser@8.3.0':
    resolution: {integrity: sha512-h53RhVyLu6AtpUzVCYLPhZGL5jzTD9fZL+SYf/+hYOx2bDkyQXztXSc4tbvKYHzfMXExMLiL9CWqJmVz6+78IQ==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      eslint: ^8.57.0 || ^9.0.0
      typescript: '*'
    peerDependenciesMeta:
      typescript:
        optional: true

  '@typescript-eslint/scope-manager@8.3.0':
    resolution: {integrity: sha512-mz2X8WcN2nVu5Hodku+IR8GgCOl4C0G/Z1ruaWN4dgec64kDBabuXyPAr+/RgJtumv8EEkqIzf3X2U5DUKB2eg==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@typescript-eslint/type-utils@8.3.0':
    resolution: {integrity: sha512-wrV6qh//nLbfXZQoj32EXKmwHf4b7L+xXLrP3FZ0GOUU72gSvLjeWUl5J5Ue5IwRxIV1TfF73j/eaBapxx99Lg==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      typescript: '*'
    peerDependenciesMeta:
      typescript:
        optional: true

  '@typescript-eslint/types@8.3.0':
    resolution: {integrity: sha512-y6sSEeK+facMaAyixM36dQ5NVXTnKWunfD1Ft4xraYqxP0lC0POJmIaL/mw72CUMqjY9qfyVfXafMeaUj0noWw==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@typescript-eslint/typescript-estree@8.3.0':
    resolution: {integrity: sha512-Mq7FTHl0R36EmWlCJWojIC1qn/ZWo2YiWYc1XVtasJ7FIgjo0MVv9rZWXEE7IK2CGrtwe1dVOxWwqXUdNgfRCA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      typescript: '*'
    peerDependenciesMeta:
      typescript:
        optional: true

  '@typescript-eslint/utils@8.3.0':
    resolution: {integrity: sha512-F77WwqxIi/qGkIGOGXNBLV7nykwfjLsdauRB/DOFPdv6LTF3BHHkBpq81/b5iMPSF055oO2BiivDJV4ChvNtXA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      eslint: ^8.57.0 || ^9.0.0

  '@typescript-eslint/visitor-keys@8.3.0':
    resolution: {integrity: sha512-RmZwrTbQ9QveF15m/Cl28n0LXD6ea2CjkhH5rQ55ewz3H24w+AMCJHPVYaZ8/0HoG8Z3cLLFFycRXxeO2tz9FA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  '@vitejs/plugin-react-swc@3.11.0':
    resolution: {integrity: sha512-YTJCGFdNMHCMfjODYtxRNVAYmTWQ1Lb8PulP/2/f/oEEtglw8oKxKIZmmRkyXrVrHfsKOaVkAc3NT9/dMutO5w==}
    peerDependencies:
      vite: ^4 || ^5 || ^6 || ^7

  accepts@2.0.0:
    resolution: {integrity: sha512-5cvg6CtKwfgdmVqY1WIiXKc3Q1bkRqGLi+2W/6ao+6Y7gu/RCwRuAhGEzh5B4KlszSuTLgZYuqFqo5bImjNKng==}
    engines: {node: '>= 0.6'}

  acorn-jsx@5.3.2:
    resolution: {integrity: sha512-rq9s+JNhf0IChjtDXxllJ7g41oZk5SlXtp0LHwyA5cejwn7vKmKp4pPri6YEePv2PU65sAsegbXtIinmDFDXgQ==}
    peerDependencies:
      acorn: ^6.0.0 || ^7.0.0 || ^8.0.0

  acorn@8.15.0:
    resolution: {integrity: sha512-NZyJarBfL7nWwIq+FDL6Zp/yHEhePMNnnJ0y3qfieCrmNvYct8uvtiV41UvlSe6apAfk0fY1FbWx+NwfmpvtTg==}
    engines: {node: '>=0.4.0'}
    hasBin: true

  acorn@8.8.2:
    resolution: {integrity: sha512-xjIYgE8HBrkpd/sJqOGNspf8uHG+NOHGOw6a/Urj8taM2EXfdNAH2oFcPeIFfsv3+kz/mJrS5VuMqbNLjCa2vw==}
    engines: {node: '>=0.4.0'}
    hasBin: true

  ajv@6.12.6:
    resolution: {integrity: sha512-j3fVLgvTo527anyYyJOGTYJbG+vnnQYvE0m5mmkc1TK+nxAppkCLMIL0aZ4dblVCNoGShhm+kzE4ZUykBoMg4g==}

  ansi-regex@5.0.1:
    resolution: {integrity: sha512-quJQXlTSUGL2LH9SUXo8VwsY4soanhgo6LNSm84E1LBcE8s3O0wpdiRzyR9z/ZZJMlMWv37qOOb9pdJlMUEKFQ==}
    engines: {node: '>=8'}

  ansi-regex@6.2.2:
    resolution: {integrity: sha512-Bq3SmSpyFHaWjPk8If9yc6svM8c56dB5BAtW4Qbw5jHTwwXXcTLoRMkpDJp6VL0XzlWaCHTXrkFURMYmD0sLqg==}
    engines: {node: '>=12'}

  ansi-styles@4.3.0:
    resolution: {integrity: sha512-zbB9rCJAT1rbjiVDb2hqKFHNYLxgtk8NURxZ3IZwD3F6NtxbXZQCnnSi1Lkx+IDohdPlFp222wVALIheZJQSEg==}
    engines: {node: '>=8'}

  ansi-styles@6.2.3:
    resolution: {integrity: sha512-4Dj6M28JB+oAH8kFkTLUo+a2jwOFkuqb3yucU0CANcRRUbxS0cP0nZYCGjcc3BNXwRIsUVmDGgzawme7zvJHvg==}
    engines: {node: '>=12'}

  any-promise@1.3.0:
    resolution: {integrity: sha512-7UvmKalWRt1wgjL1RrGxoSJW/0QZFIegpeGvZG9kjp8vrRu55XTHbwnqq2GpXm9uLbcuhxm3IqX9OB4MZR1b2A==}

  anymatch@3.1.3:
    resolution: {integrity: sha512-KMReFUr0B4t+D+OBkjR3KYqvocp2XaSzO55UcB6mgQMd3KbcE+mWTyvVV7D/zsdEbNnV6acZUutkiHQXvTr1Rw==}
    engines: {node: '>= 8'}

  append-field@1.0.0:
    resolution: {integrity: sha512-klpgFSWLW1ZEs8svjfb7g4qWY0YS5imI82dTg+QahUvJ8YqAY0P10Uk8tTyh9ZGuYEZEMaeJYCF5BFuX552hsw==}

  archiver-utils@2.1.0:
    resolution: {integrity: sha512-bEL/yUb/fNNiNTuUz979Z0Yg5L+LzLxGJz8x79lYmR54fmTIb6ob/hNQgkQnIUDWIFjZVQwl9Xs356I6BAMHfw==}
    engines: {node: '>= 6'}

  archiver-utils@3.0.4:
    resolution: {integrity: sha512-KVgf4XQVrTjhyWmx6cte4RxonPLR9onExufI1jhvw/MQ4BB6IsZD5gT8Lq+u/+pRkWna/6JoHpiQioaqFP5Rzw==}
    engines: {node: '>= 10'}

  archiver@5.3.2:
    resolution: {integrity: sha512-+25nxyyznAXF7Nef3y0EbBeqmGZgeN/BxHX29Rs39djAfaFalmQ89SE6CWyDCHzGL0yt/ycBtNOmGTW0FyGWNw==}
    engines: {node: '>= 10'}

  arg@5.0.2:
    resolution: {integrity: sha512-PYjyFOLKQ9y57JvQ6QLo8dAgNqswh8M1RMJYdQduT6xbWSgK36P/Z/v+p888pM69jMMfS8Xd8F6I1kQ/I9HUGg==}

  argparse@2.0.1:
    resolution: {integrity: sha512-8+9WqebbFzpX9OR+Wa6O29asIogeRMzcGtAINdpMHHyAg10f05aSFVBbcEqGf/PXw1EjAZ+q2/bEBg3DvurK3Q==}

  array-differ@3.0.0:
    resolution: {integrity: sha512-THtfYS6KtME/yIAhKjZ2ul7XI96lQGHRputJQHO80LAWQnuGP4iCIN8vdMRboGbIEYBwU33q8Tch1os2+X0kMg==}
    engines: {node: '>=8'}

  array-union@2.1.0:
    resolution: {integrity: sha512-HGyxoOTYUyCM6stUe6EJgnd4EoewAI7zMdfqO+kGjnlZmBDz/cR5pf8r/cR4Wq60sL/p0IkcjUEEPwS3GFrIyw==}
    engines: {node: '>=8'}

  arrify@2.0.1:
    resolution: {integrity: sha512-3duEwti880xqi4eAMN8AyR4a0ByT90zoYdLlevfrvU43vb0YZwZVfxOgxWrLXXXpyugL0hNZc9G6BiB5B3nUug==}
    engines: {node: '>=8'}

  assert@2.0.0:
    resolution: {integrity: sha512-se5Cd+js9dXJnu6Ag2JFc00t+HmHOen+8Q+L7O9zI0PqQXr20uk2J0XQqMxZEeo5U50o8Nvmmx7dZrl+Ufr35A==}

  async@3.2.6:
    resolution: {integrity: sha512-htCUDlxyyCLMgaM3xXg0C0LW2xqfuQ6p05pCEIsXuyQ+a1koYKTuBMzRNwmybfLgvJDMd0r1LTn4+E0Ti6C2AA==}

  autoprefixer@10.4.21:
    resolution: {integrity: sha512-O+A6LWV5LDHSJD3LjHYoNi4VLsj/Whi7k6zG12xTYaU4cQ8oxQGckXNX8cRHK5yOZ/ppVHe0ZBXGzSV9jXdVbQ==}
    engines: {node: ^10 || ^12 || >=14}
    hasBin: true
    peerDependencies:
      postcss: ^8.1.0

  available-typed-arrays@1.0.7:
    resolution: {integrity: sha512-wvUjBtSGN7+7SjNpq/9M2Tg350UZD3q62IFZLbRAR1bSMlCo1ZaeW+BJ+D090e4hIIZLBcTDWe4Mh4jvUDajzQ==}
    engines: {node: '>= 0.4'}

  balanced-match@1.0.2:
    resolution: {integrity: sha512-3oSeUO0TMV67hN1AmbXsK4yaqU7tjiHlbxRDZOpH0KW9+CeX4bRAaX0Anxt0tx2MrpRpWwQaPwIlISEJhYU5Pw==}

  base64-js@1.5.1:
    resolution: {integrity: sha512-AKpaYlHn8t4SVbOHCy+b5+KKgvR4vrsD8vbvrbiQJps7fKDTkjkDry6ji0rUJjC0kzbNePLwzxq8iypo41qeWA==}

  baseline-browser-mapping@2.8.28:
    resolution: {integrity: sha512-gYjt7OIqdM0PcttNYP2aVrr2G0bMALkBaoehD4BuRGjAOtipg0b6wHg1yNL+s5zSnLZZrGHOw4IrND8CD+3oIQ==}
    hasBin: true

  bcryptjs@3.0.3:
    resolution: {integrity: sha512-GlF5wPWnSa/X5LKM1o0wz0suXIINz1iHRLvTS+sLyi7XPbe5ycmYI3DlZqVGZZtDgl4DmasFg7gOB3JYbphV5g==}
    hasBin: true

  big-integer@1.6.52:
    resolution: {integrity: sha512-QxD8cf2eVqJOOz63z6JIN9BzvVs/dlySa5HGSBH5xtR8dPteIRQnBxxKqkNTiT6jbDTF6jAfrd4oMcND9RGbQg==}
    engines: {node: '>=0.6'}

  binary-extensions@2.3.0:
    resolution: {integrity: sha512-Ceh+7ox5qe7LJuLHoY0feh3pHuUDHAcRUeyL2VYghZwfpkNIy/+8Ocg0a3UuSoYzavmylwuLWQOf3hl0jjMMIw==}
    engines: {node: '>=8'}

  binary@0.3.0:
    resolution: {integrity: sha512-D4H1y5KYwpJgK8wk1Cue5LLPgmwHKYSChkbspQg5JtVuR5ulGckxfR62H3AE9UDkdMC8yyXlqYihuz3Aqg2XZg==}

  bl@4.1.0:
    resolution: {integrity: sha512-1W07cM9gS6DcLperZfFSj+bWLtaPGSOHWhPiGzXmvVJbRLdG82sH/Kn8EtW1VqWVA54AKf2h5k5BbnIbwF3h6w==}

  bluebird@3.4.7:
    resolution: {integrity: sha512-iD3898SR7sWVRHbiQv+sHUtHnMvC1o3nW5rAcqnq3uOn07DSAppZYUkIGslDz6gXC7HfunPe7YVBgoEJASPcHA==}

  body-parser@2.2.0:
    resolution: {integrity: sha512-02qvAaxv8tp7fBa/mw1ga98OGm+eCbqzJOKoRt70sLmfEEi+jyBYVTDGfCL/k06/4EMk/z01gCe7HoCH/f2LTg==}
    engines: {node: '>=18'}

  brace-expansion@1.1.12:
    resolution: {integrity: sha512-9T9UjW3r0UW5c1Q7GTwllptXwhvYmEzFhzMfZ9H7FQWt+uZePjZPjBP/W1ZEyZ1twGWom5/56TF4lPcqjnDHcg==}

  brace-expansion@2.0.2:
    resolution: {integrity: sha512-Jt0vHyM+jmUBqojB7E1NIYadt0vI0Qxjxd2TErW94wDz+E2LAm5vKMXXwg6ZZBTHPuUlDgQHKXvjGBdfcF1ZDQ==}

  braces@3.0.3:
    resolution: {integrity: sha512-yQbXgO/OSZVD2IsiLlro+7Hf6Q18EJrKSEsdoMzKePKXct3gvD8oLcOQdIzGupr5Fj+EDe8gO/lxc1BzfMpxvA==}
    engines: {node: '>=8'}

  browserslist@4.28.0:
    resolution: {integrity: sha512-tbydkR/CxfMwelN0vwdP/pLkDwyAASZ+VfWm4EOwlB6SWhx1sYnWLqo8N5j0rAzPfzfRaxt0mM/4wPU/Su84RQ==}
    engines: {node: ^6 || ^7 || ^8 || ^9 || ^10 || ^11 || ^12 || >=13.7}
    hasBin: true

  buffer-crc32@0.2.13:
    resolution: {integrity: sha512-VO9Ht/+p3SN7SKWqcrgEzjGbRSJYTx+Q1pTQC0wrWqHx0vpJraQ6GtHx8tvcg1rlK1byhU5gccxgOgj7B0TDkQ==}

  buffer-from@1.1.2:
    resolution: {integrity: sha512-E+XQCRwSbaaiChtv6k6Dwgc+bx+Bs6vuKJHHl5kox/BaKbhiXzqQOwK4cO22yElGp2OCmjwVhT3HmxgyPGnJfQ==}

  buffer-indexof-polyfill@1.0.2:
    resolution: {integrity: sha512-I7wzHwA3t1/lwXQh+A5PbNvJxgfo5r3xulgpYDB5zckTu/Z9oUK9biouBKQUjEqzaz3HnAT6TYoovmE+GqSf7A==}
    engines: {node: '>=0.10'}

  buffer@5.7.1:
    resolution: {integrity: sha512-EHcyIPBQ4BSGlvjB16k5KgAJ27CIsHY/2JBmCRReo48y9rQ3MaUzWX3KVlBa4U7MyX02HdVj0K7C3WaB3ju7FQ==}

  buffers@0.1.1:
    resolution: {integrity: sha512-9q/rDEGSb/Qsvv2qvzIzdluL5k7AaJOTrw23z9reQthrbF7is4CtlT0DXyO1oei2DCp4uojjzQ7igaSHp1kAEQ==}
    engines: {node: '>=0.2.0'}

  busboy@1.6.0:
    resolution: {integrity: sha512-8SFQbg/0hQ9xy3UNTB0YEnsNBbWfhf7RtnzpL7TkBiTBRfrQ9Fxcnz7VJsleJpyp6rVLvXiuORqjlHi5q+PYuA==}
    engines: {node: '>=10.16.0'}

  bytes@3.1.2:
    resolution: {integrity: sha512-/Nf7TyzTx6S3yRJObOAV7956r8cr2+Oj8AC5dt8wSP3BQAoeX58NoHyCU8P8zGkNXStjTSi6fzO6F0pBdcYbEg==}
    engines: {node: '>= 0.8'}

  call-bind-apply-helpers@1.0.2:
    resolution: {integrity: sha512-Sp1ablJ0ivDkSzjcaJdxEunN5/XvksFJ2sMBFfq6x0ryhQV/2b/KwFe21cMpmHtPOSij8K99/wSfoEuTObmuMQ==}
    engines: {node: '>= 0.4'}

  call-bind@1.0.8:
    resolution: {integrity: sha512-oKlSFMcMwpUg2ednkhQ454wfWiU/ul3CkJe/PEHcTKuiX6RpbehUiFMXu13HalGZxfUwCQzZG747YXBn1im9ww==}
    engines: {node: '>= 0.4'}

  call-bound@1.0.4:
    resolution: {integrity: sha512-+ys997U96po4Kx/ABpBCqhA9EuxJaQWDQg7295H4hBphv3IZg0boBKuwYpt4YXp6MZ5AmZQnU/tyMTlRpaSejg==}
    engines: {node: '>= 0.4'}

  callsites@3.1.0:
    resolution: {integrity: sha512-P8BjAsXvZS+VIDUI11hHCQEv74YT67YUi5JJFNWIqL235sBmjX4+qx9Muvls5ivyNENctx46xQLQ3aTuE7ssaQ==}
    engines: {node: '>=6'}

  camelcase-css@2.0.1:
    resolution: {integrity: sha512-QOSvevhslijgYwRx6Rv7zKdMF8lbRmx+uQGx2+vDc+KI/eBnsy9kit5aj23AgGu3pa4t9AgwbnXWqS+iOY+2aA==}
    engines: {node: '>= 6'}

  caniuse-lite@1.0.30001754:
    resolution: {integrity: sha512-x6OeBXueoAceOmotzx3PO4Zpt4rzpeIFsSr6AAePTZxSkXiYDUmpypEl7e2+8NCd9bD7bXjqyef8CJYPC1jfxg==}

  chainsaw@0.1.0:
    resolution: {integrity: sha512-75kWfWt6MEKNC8xYXIdRpDehRYY/tNSgwKaJq+dbbDcxORuVrrQ+SEHoWsniVn9XPYfP4gmdWIeDk/4YNp1rNQ==}

  chalk@4.1.2:
    resolution: {integrity: sha512-oKnbhFyRIXpUuez8iBMmyEa4nbj4IOQyuhc/wy9kY7/WVPcwIO9VA668Pu8RkO7+0G76SLROeyw9CpQ061i4mA==}
    engines: {node: '>=10'}

  chance@1.1.9:
    resolution: {integrity: sha512-TfxnA/DcZXRTA4OekA2zL9GH8qscbbl6X0ZqU4tXhGveVY/mXWvEQLt5GwZcYXTEyEFflVtj+pG8nc8EwSm1RQ==}

  char-regex@1.0.2:
    resolution: {integrity: sha512-kWWXztvZ5SBQV+eRgKFeh8q5sLuZY2+8WUIzlxWVTg+oGwY14qylx1KbKzHd8P6ZYkAg0xyIDU9JMHhyJMZ1jw==}
    engines: {node: '>=10'}

  charenc@0.0.2:
    resolution: {integrity: sha512-yrLQ/yVUFXkzg7EDQsPieE/53+0RlaWTs+wBrvW36cyilJ2SaDWfl4Yj7MtLTXleV9uEKefbAGUPv2/iWSooRA==}

  chokidar@3.6.0:
    resolution: {integrity: sha512-7VT13fmjotKpGipCW9JEQAusEPE+Ei8nl6/g4FBAmIm0GOOLMua9NDDo/DWp0ZAxCr3cPq5ZpBqmPAQgDda2Pw==}
    engines: {node: '>= 8.10.0'}

  class-validator@0.14.1:
    resolution: {integrity: sha512-2VEG9JICxIqTpoK1eMzZqaV+u/EiwEJkMGzTrZf6sU/fwsnOITVgYJ8yojSy6CaXtO9V0Cc6ZQZ8h8m4UBuLwQ==}

  color-convert@2.0.1:
    resolution: {integrity: sha512-RRECPsj7iu/xb5oKYcsFHSppFNnsj/52OVTRKb4zP5onXwVF3zVmmToNcOfGC+CRDpfK/U584fMg38ZHCaElKQ==}
    engines: {node: '>=7.0.0'}

  color-name@1.1.4:
    resolution: {integrity: sha512-dOy+3AuW3a2wNbZHIuMZpTcgjGuLU/uBL/ubcZF9OXbDo8ff4O8yVp5Bf0efS8uEoYo5q4Fx7dY9OgQGXgAsQA==}

  commander@10.0.0:
    resolution: {integrity: sha512-zS5PnTI22FIRM6ylNW8G4Ap0IEOyk62fhLSD0+uHRT9McRCLGpkVNvao4bjimpK/GShynyQkFFxHhwMcETmduA==}
    engines: {node: '>=14'}

  commander@4.1.1:
    resolution: {integrity: sha512-NOKm8xhkzAjzFx8B2v5OAHT+u5pRQc2UCa2Vq9jYL/31o2wi9mxBA7LIFs3sV5VSC49z6pEhfbMULvShKj26WA==}
    engines: {node: '>= 6'}

  compress-commons@4.1.2:
    resolution: {integrity: sha512-D3uMHtGc/fcO1Gt1/L7i1e33VOvD4A9hfQLP+6ewd+BvG/gQ84Yh4oftEhAdjSMgBgwGL+jsppT7JYNpo6MHHg==}
    engines: {node: '>= 10'}

  concat-map@0.0.1:
    resolution: {integrity: sha512-/Srv4dswyQNBfohGpz9o6Yb3Gz3SrUDqBH5rTuhGR7ahtlbYKnVxw2bCFMRljaA7EXHaXZ8wsHdodFvbkhKmqg==}

  concat-stream@2.0.0:
    resolution: {integrity: sha512-MWufYdFw53ccGjCA+Ol7XJYpAlW6/prSMzuPOTRnJGcGzuhLn4Scrz7qf6o8bROZ514ltazcIFJZevcfbo0x7A==}
    engines: {'0': node >= 6.0}

  content-disposition@1.0.1:
    resolution: {integrity: sha512-oIXISMynqSqm241k6kcQ5UwttDILMK4BiurCfGEREw6+X9jkkpEe5T9FZaApyLGGOnFuyMWZpdolTXMtvEJ08Q==}
    engines: {node: '>=18'}

  content-type@1.0.5:
    resolution: {integrity: sha512-nTjqfcBFEipKdXCv4YDQWCfmcLZKm81ldF0pAopTvyrFGVbcR6P/VAAd5G7N+0tTr8QqiU0tFadD6FK4NtJwOA==}
    engines: {node: '>= 0.6'}

  cookie-signature@1.2.2:
    resolution: {integrity: sha512-D76uU73ulSXrD1UXF4KE2TMxVVwhsnCgfAyTg9k8P6KGZjlXKrOLe4dJQKI3Bxi5wjesZoFXJWElNWBjPZMbhg==}
    engines: {node: '>=6.6.0'}

  cookie@0.7.2:
    resolution: {integrity: sha512-yki5XnKuf750l50uGTllt6kKILY4nQ1eNIQatoXEByZ5dWgnKqbnqmTrBE5B4N7lrMJKQ2ytWMiTO2o0v6Ew/w==}
    engines: {node: '>= 0.6'}

  core-util-is@1.0.3:
    resolution: {integrity: sha512-ZQBvi1DcpJ4GDqanjucZ2Hj3wEO5pZDS89BWbkcrvdxksJorwUDDZamX9ldFkp9aw2lmBDLgkObEA4DWNJ9FYQ==}

  cors@2.8.5:
    resolution: {integrity: sha512-KIHbLJqu73RGr/hnbrO9uBeixNGuvSQjul/jdFvS/KFSIH1hWVd1ng7zOHx+YrEfInLG7q4n6GHQ9cDtxv/P6g==}
    engines: {node: '>= 0.10'}

  crc-32@1.2.2:
    resolution: {integrity: sha512-ROmzCKrTnOwybPcJApAA6WBWij23HVfGVNKqqrZpuyZOHqK2CwHSvpGuyt/UNNvaIjEd8X5IFGp4Mh+Ie1IHJQ==}
    engines: {node: '>=0.8'}
    hasBin: true

  crc32-stream@4.0.3:
    resolution: {integrity: sha512-NT7w2JVU7DFroFdYkeq8cywxrgjPHWkdX1wjpRQXPX5Asews3tA+Ght6lddQO5Mkumffp3X7GEqku3epj2toIw==}
    engines: {node: '>= 10'}

  cross-spawn@7.0.6:
    resolution: {integrity: sha512-uV2QOWP2nWzsy2aMp8aRibhi9dlzF5Hgh5SHaB9OiTGEyDTiJJyx0uy51QXdyWbtAHNua4XJzUKca3OzKUd3vA==}
    engines: {node: '>= 8'}

  crypt@0.0.2:
    resolution: {integrity: sha512-mCxBlsHFYh9C+HVpiEacem8FEBnMXgU9gy4zmNC+SXAZNB/1idgp/aulFJ4FgCi7GPEVbfyng092GqL2k2rmow==}

  crypto-js@4.2.0:
    resolution: {integrity: sha512-KALDyEYgpY+Rlob/iriUtjV6d5Eq+Y191A5g4UqLAi8CyGP9N1+FdVbkc1SxKc2r4YAYqG8JzO2KGL+AizD70Q==}

  cssesc@3.0.0:
    resolution: {integrity: sha512-/Tb/JcjK111nNScGob5MNtsntNM1aCNUDipB/TkwZFhyDrrE47SOx/18wF2bbjgc3ZzCSKW1T5nt5EbFoAz/Vg==}
    engines: {node: '>=4'}
    hasBin: true

  csstype@3.2.1:
    resolution: {integrity: sha512-98XGutrXoh75MlgLihlNxAGbUuFQc7l1cqcnEZlLNKc0UrVdPndgmaDmYTDDh929VS/eqTZV0rozmhu2qqT1/g==}

  dayjs@1.11.19:
    resolution: {integrity: sha512-t5EcLVS6QPBNqM2z8fakk/NKel+Xzshgt8FFKAn+qwlD1pzZWxh0nVCrvFK7ZDb6XucZeF9z8C7CBWTRIVApAw==}

  debug@4.4.3:
    resolution: {integrity: sha512-RGwwWnwQvkVfavKVt22FGLw+xYSdzARwm0ru6DhTVA3umU5hZc28V3kO4stgYryrTlLpuvgI9GiijltAjNbcqA==}
    engines: {node: '>=6.0'}
    peerDependencies:
      supports-color: '*'
    peerDependenciesMeta:
      supports-color:
        optional: true

  deep-is@0.1.4:
    resolution: {integrity: sha512-oIPzksmTg4/MriiaYGO+okXDT7ztn/w3Eptv/+gSIdMdKsJo0u4CfYNFJPy+4SKMuCqGw2wxnA+URMg3t8a/bQ==}

  define-data-property@1.1.4:
    resolution: {integrity: sha512-rBMvIzlpA8v6E+SJZoo++HAYqsLrkg7MSfIinMPFhmkorw7X+dOXVJQs+QT69zGkzMyfDnIMN2Wid1+NbL3T+A==}
    engines: {node: '>= 0.4'}

  define-properties@1.2.1:
    resolution: {integrity: sha512-8QmQKqEASLd5nx0U1B1okLElbUuuttJ/AnYmRXbbbGDWh6uS208EjD4Xqq/I9wK7u0v6O08XhTWnt5XtEbR6Dg==}
    engines: {node: '>= 0.4'}

  depd@2.0.0:
    resolution: {integrity: sha512-g7nH6P6dyDioJogAAGprGpCtVImJhpPk/roCzdb3fIh61/s/nPsfR6onyMwkCAR/OlC3yBC0lESvUoQEAssIrw==}
    engines: {node: '>= 0.8'}

  destr@2.0.5:
    resolution: {integrity: sha512-ugFTXCtDZunbzasqBxrK93Ik/DRYsO6S/fedkWEMKqt04xZ4csmnmwGDBAb07QWNaGMAmnTIemsYZCksjATwsA==}

  didyoumean@1.2.2:
    resolution: {integrity: sha512-gxtyfqMg7GKyhQmb056K7M3xszy/myH8w+B4RT+QXBQsvAOdc3XymqDDPHx1BgPgsdAA5SIifona89YtRATDzw==}

  dlv@1.1.3:
    resolution: {integrity: sha512-+HlytyjlPKnIG8XuRG8WvmBP8xs8P71y+SKKS6ZXWoEgLuePxtDoUEiH7WkdePWrQ5JBpE6aoVqfZfJUQkjXwA==}

  dunder-proto@1.0.1:
    resolution: {integrity: sha512-KIN/nDJBQRcXw0MLVhZE9iQHmG68qAVIBg9CqmUYjmQIhgij9U5MFvrqkUL5FbtyyzZuOeOt0zdeRe4UY7ct+A==}
    engines: {node: '>= 0.4'}

  duplexer2@0.1.4:
    resolution: {integrity: sha512-asLFVfWWtJ90ZyOUHMqk7/S2w2guQKxUI2itj3d92ADHhxUSbCMGi1f1cBcJ7xM1To+pE/Khbwo1yuNbMEPKeA==}

  eastasianwidth@0.2.0:
    resolution: {integrity: sha512-I88TYZWc9XiYHRQ4/3c5rjjfgkjhLyW2luGIheGERbNQ6OY7yTybanSpDXZa8y7VUP9YmDcYa+eyq4ca7iLqWA==}

  ee-first@1.1.1:
    resolution: {integrity: sha512-WMwm9LhRUo+WUaRN+vRuETqG89IgZphVSNkdFgeb6sS/E4OrDIN7t48CAewSHXc6C8lefD8KKfr5vY61brQlow==}

  electron-to-chromium@1.5.254:
    resolution: {integrity: sha512-DcUsWpVhv9svsKRxnSCZ86SjD+sp32SGidNB37KpqXJncp1mfUgKbHvBomE89WJDbfVKw1mdv5+ikrvd43r+Bg==}

  emoji-regex@8.0.0:
    resolution: {integrity: sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A==}

  emoji-regex@9.2.2:
    resolution: {integrity: sha512-L18DaJsXSUk2+42pv8mLs5jJT2hqFkFE4j21wOmgbUqsZ2hL72NsUU785g9RXgo3s0ZNgVl42TiHp3ZtOv/Vyg==}

  encodeurl@2.0.0:
    resolution: {integrity: sha512-Q0n9HRi4m6JuGIV1eFlmvJB7ZEVxu93IrMyiMsGC0lrMJMWzRgx6WGquyfQgZVb31vhGgXnfmPNNXmxnOkRBrg==}
    engines: {node: '>= 0.8'}

  end-of-stream@1.4.5:
    resolution: {integrity: sha512-ooEGc6HP26xXq/N+GCGOT0JKCLDGrq2bQUZrQ7gyrJiZANJ/8YDTxTpQBXGMn+WbIQXNVpyWymm7KYVICQnyOg==}

  es-define-property@1.0.1:
    resolution: {integrity: sha512-e3nRfgfUZ4rNGL232gUgX06QNyyez04KdjFrF+LTRoOXmrOgFKDg4BCdsjW8EnT69eqdYGmRpJwiPVYNrCaW3g==}
    engines: {node: '>= 0.4'}

  es-errors@1.3.0:
    resolution: {integrity: sha512-Zf5H2Kxt2xjTvbJvP2ZWLEICxA6j+hAmMzIlypy4xcBg1vKVnx89Wy0GbS+kf5cwCVFFzdCFh2XSCFNULS6csw==}
    engines: {node: '>= 0.4'}

  es-object-atoms@1.1.1:
    resolution: {integrity: sha512-FGgH2h8zKNim9ljj7dankFPcICIK9Cp5bm+c2gQSYePhpaG5+esrLODihIorn+Pe6FGJzWhXQotPv73jTaldXA==}
    engines: {node: '>= 0.4'}

  es6-object-assign@1.1.0:
    resolution: {integrity: sha512-MEl9uirslVwqQU369iHNWZXsI8yaZYGg/D65aOgZkeyFJwHYSxilf7rQzXKI7DdDuBPrBXbfk3sl9hJhmd5AUw==}

  esbuild@0.25.12:
    resolution: {integrity: sha512-bbPBYYrtZbkt6Os6FiTLCTFxvq4tt3JKall1vRwshA3fdVztsLAatFaZobhkBC8/BrPetoa0oksYoKXoG4ryJg==}
    engines: {node: '>=18'}
    hasBin: true

  escalade@3.2.0:
    resolution: {integrity: sha512-WUj2qlxaQtO4g6Pq5c29GTcWGDyd8itL8zTlipgECz3JesAiiOKotd8JU6otB3PACgG6xkJUyVhboMS+bje/jA==}
    engines: {node: '>=6'}

  escape-html@1.0.3:
    resolution: {integrity: sha512-NiSupZ4OeuGwr68lGIeym/ksIZMJodUGOSCZ/FSnTxcrekbvqrgdUxlJOMpijaKZVjAJrWrGs/6Jy8OMuyj9ow==}

  escape-string-regexp@4.0.0:
    resolution: {integrity: sha512-TtpcNJ3XAzx3Gq8sWRzJaVajRs0uVxA2YAkdb1jm2YkPz4G6egUFAyA3n5vtEIZefPk5Wa4UXbKuS5fKkJWdgA==}
    engines: {node: '>=10'}

  eslint-plugin-react-hooks@5.1.0-rc.0:
    resolution: {integrity: sha512-xBc+mRT2KSyzKm78GyaOFPyF4EnSRfTSmre88Ak8jG1HnpNGEiHETbCuXih8Xl796DryrJej/8IdW4oQ+m5kPg==}
    engines: {node: '>=10'}
    peerDependencies:
      eslint: ^3.0.0 || ^4.0.0 || ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0-0 || ^9.0.0

  eslint-plugin-react-refresh@0.4.11:
    resolution: {integrity: sha512-wrAKxMbVr8qhXTtIKfXqAn5SAtRZt0aXxe5P23Fh4pUAdC6XEsybGLB8P0PI4j1yYqOgUEUlzKAGDfo7rJOjcw==}
    peerDependencies:
      eslint: '>=7'

  eslint-scope@7.1.1:
    resolution: {integrity: sha512-QKQM/UXpIiHcLqJ5AOyIW7XZmzjkzQXYE54n1++wb0u9V/abW3l9uQnxX8Z5Xd18xyKIMTUAyQ0k1e8pz6LUrw==}
    engines: {node: ^12.22.0 || ^14.17.0 || >=16.0.0}

  eslint-scope@8.4.0:
    resolution: {integrity: sha512-sNXOfKCn74rt8RICKMvJS7XKV/Xk9kA7DyJr8mJik3S7Cwgy3qlkkmyS2uQB3jiJg6VNdZd/pDBJu0nvG2NlTg==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  eslint-visitor-keys@3.3.0:
    resolution: {integrity: sha512-mQ+suqKJVyeuwGYHAdjMFqjCyfl8+Ldnxuyp3ldiMBFKkvytrXUZWaiPCEav8qDHKty44bD+qV1IP4T+w+xXRA==}
    engines: {node: ^12.22.0 || ^14.17.0 || >=16.0.0}

  eslint-visitor-keys@3.4.3:
    resolution: {integrity: sha512-wpc+LXeiyiisxPlEkUzU6svyS1frIO3Mgxj1fdy7Pm8Ygzguax2N3Fa/D/ag1WqbOprdI+uY6wMUl8/a2G+iag==}
    engines: {node: ^12.22.0 || ^14.17.0 || >=16.0.0}

  eslint-visitor-keys@4.2.1:
    resolution: {integrity: sha512-Uhdk5sfqcee/9H/rCOJikYz67o0a2Tw2hGRPOG2Y1R2dg7brRe1uG0yaNQDHu+TO/uQPF/5eCapvYSmHUjt7JQ==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  eslint@9.9.1:
    resolution: {integrity: sha512-dHvhrbfr4xFQ9/dq+jcVneZMyRYLjggWjk6RVsIiHsP8Rz6yZ8LvZ//iU4TrZF+SXWG+JkNF2OyiZRvzgRDqMg==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    hasBin: true
    peerDependencies:
      jiti: '*'
    peerDependenciesMeta:
      jiti:
        optional: true

  espree@10.4.0:
    resolution: {integrity: sha512-j6PAQ2uUr79PZhBjP5C5fhl8e39FmRnOjsD5lGnWrFU8i2G776tBK7+nP8KuQUTTyAZUwfQqXAgrVH5MbH9CYQ==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}

  esprima@4.0.1:
    resolution: {integrity: sha512-eGuFFw7Upda+g4p+QHvnW0RyTX/SVeJBDM/gCtMARO0cLuT2HcEKnTPvhjV6aGeqrCB/sbNop0Kszm0jsaWU4A==}
    engines: {node: '>=4'}
    hasBin: true

  esquery@1.6.0:
    resolution: {integrity: sha512-ca9pw9fomFcKPvFLXhBKUK90ZvGibiGOvRJNbjljY7s7uq/5YO4BOzcYtJqExdx99rF6aAcnRxHmcUHcz6sQsg==}
    engines: {node: '>=0.10'}

  esrecurse@4.3.0:
    resolution: {integrity: sha512-KmfKL3b6G+RXvP8N1vr3Tq1kL/oCFgn2NYXEtqP8/L3pKapUA4G8cFVaoF3SU323CD4XypR/ffioHmkti6/Tag==}
    engines: {node: '>=4.0'}

  estraverse@5.3.0:
    resolution: {integrity: sha512-MMdARuVEQziNTeJD8DgMqmhwR11BRQ/cBP+pLtYdSTnf3MIO8fFeiINEbX36ZdNlfU/7A9f3gUw49B3oQsvwBA==}
    engines: {node: '>=4.0'}

  esutils@2.0.3:
    resolution: {integrity: sha512-kVscqXk4OCp68SZ0dkgEKVi6/8ij300KBWTJq32P/dYeWTSwK41WyTxalN1eRmA5Z9UU/LX9D7FWSmV9SAYx6g==}
    engines: {node: '>=0.10.0'}

  etag@1.8.1:
    resolution: {integrity: sha512-aIL5Fx7mawVa300al2BnEE4iNvo1qETxLrPI/o05L7z6go7fCw1J6EQmbK4FmJ2AS7kgVF/KEZWufBfdClMcPg==}
    engines: {node: '>= 0.6'}

  exceljs@4.4.0:
    resolution: {integrity: sha512-XctvKaEMaj1Ii9oDOqbW/6e1gXknSY4g/aLCDicOXqBE4M0nRWkUu0PTp++UPNzoFY12BNHMfs/VadKIS6llvg==}
    engines: {node: '>=8.3.0'}

  express@5.1.0:
    resolution: {integrity: sha512-DT9ck5YIRU+8GYzzU5kT3eHGA5iL+1Zd0EutOmTE9Dtk+Tvuzd23VBU+ec7HPNSTxXYO55gPV/hq4pSBJDjFpA==}
    engines: {node: '>= 18'}

  fast-csv@4.3.6:
    resolution: {integrity: sha512-2RNSpuwwsJGP0frGsOmTb9oUF+VkFSM4SyLTDgwf2ciHWTarN0lQTC+F2f/t5J9QjW+c65VFIAAu85GsvMIusw==}
    engines: {node: '>=10.0.0'}

  fast-deep-equal@3.1.3:
    resolution: {integrity: sha512-f3qQ9oQy9j2AhBe/H9VC91wLmKBCCU/gDOnKNAYG5hswO7BLKj09Hc5HYNz9cGI++xlpDCIgDaitVs03ATR84Q==}

  fast-glob@3.3.3:
    resolution: {integrity: sha512-7MptL8U0cqcFdzIzwOTHoilX9x5BrNqye7Z/LuC7kCMRio1EMSyqRK3BEAUD7sXRq4iT4AzTVuZdhgQ2TCvYLg==}
    engines: {node: '>=8.6.0'}

  fast-json-stable-stringify@2.1.0:
    resolution: {integrity: sha512-lhd/wF+Lk98HZoTCtlVraHtfh5XYijIjalXck7saUtuanSDyLMxnHhSXEDJqHxD7msR8D0uCmqlkwjCV8xvwHw==}

  fast-levenshtein@2.0.6:
    resolution: {integrity: sha512-DCXu6Ifhqcks7TZKY3Hxp3y6qphY5SJZmrWMDrKcERSOXWQdMhU9Ig/PYrzyw/ul9jOIyh0N4M0tbC5hodg8dw==}

  fastq@1.19.1:
    resolution: {integrity: sha512-GwLTyxkCXjXbxqIhTsMI2Nui8huMPtnxg7krajPJAjnEG/iiOS7i+zCtWGZR9G0NBKbXKh6X9m9UIsYX/N6vvQ==}

  fdir@6.5.0:
    resolution: {integrity: sha512-tIbYtZbucOs0BRGqPJkshJUYdL+SDH7dVM8gjy+ERp3WAUjLEFJE+02kanyHtwjWOnwrKYBiwAmM0p4kLJAnXg==}
    engines: {node: '>=12.0.0'}
    peerDependencies:
      picomatch: ^3 || ^4
    peerDependenciesMeta:
      picomatch:
        optional: true

  file-entry-cache@8.0.0:
    resolution: {integrity: sha512-XXTUwCvisa5oacNGRP9SfNtYBNAMi+RPwBFmblZEF7N7swHYQS6/Zfk7SRwx4D5j3CH211YNRco1DEMNVfZCnQ==}
    engines: {node: '>=16.0.0'}

  fill-range@7.1.1:
    resolution: {integrity: sha512-YsGpe3WHLK8ZYi4tWDg2Jy3ebRz2rXowDxnld4bkQB00cc/1Zw9AWnC0i9ztDJitivtQvaI9KaLyKrc+hBW0yg==}
    engines: {node: '>=8'}

  finalhandler@2.1.0:
    resolution: {integrity: sha512-/t88Ty3d5JWQbWYgaOGCCYfXRwV1+be02WqYYlL6h0lEiUAMPM8o8qKGO01YIkOHzka2up08wvgYD0mDiI+q3Q==}
    engines: {node: '>= 0.8'}

  find-up@5.0.0:
    resolution: {integrity: sha512-78/PXT1wlLLDgTzDs7sjq9hzz0vXD+zn+7wypEe4fXQxCmdmqfGsEPQxmiCSQI3ajFV91bVSsvNtrJRiW6nGng==}
    engines: {node: '>=10'}

  flat-cache@4.0.1:
    resolution: {integrity: sha512-f7ccFPK3SXFHpx15UIGyRJ/FJQctuKZ0zVuN3frBo4HnK3cay9VEW0R6yPYFHC0AgqhukPzKjq22t5DmAyqGyw==}
    engines: {node: '>=16'}

  flatted@3.3.3:
    resolution: {integrity: sha512-GX+ysw4PBCz0PzosHDepZGANEuFCMLrnRTiEy9McGjmkCQYwRq4A/X786G/fjM/+OjsWSU1ZrY5qyARZmO/uwg==}

  for-each@0.3.5:
    resolution: {integrity: sha512-dKx12eRCVIzqCxFGplyFKJMPvLEWgmNtUrpTiJIR5u97zEhRG8ySrtboPHZXx7daLxQVrl643cTzbab2tkQjxg==}
    engines: {node: '>= 0.4'}

  foreground-child@3.3.1:
    resolution: {integrity: sha512-gIXjKqtFuWEgzFRJA9WCQeSJLZDjgJUOMCMzxtvFq/37KojM1BFGufqsCy0r4qSQmYLsZYMeyRqzIWOMup03sw==}
    engines: {node: '>=14'}

  forwarded@0.2.0:
    resolution: {integrity: sha512-buRG0fpBtRHSTCOASe6hD258tEubFoRLb4ZNA6NxMVHNw2gOcwHo9wyablzMzOA5z9xA9L1KNjk/Nt6MT9aYow==}
    engines: {node: '>= 0.6'}

  fraction.js@4.3.7:
    resolution: {integrity: sha512-ZsDfxO51wGAXREY55a7la9LScWpwv9RxIrYABrlvOFBlH/ShPnrtsXeuUIfXKKOVicNxQ+o8JTbJvjS4M89yew==}

  framer-motion@12.23.11:
    resolution: {integrity: sha512-VzNi+exyI3bn7Pzvz1Fjap1VO9gQu8mxrsSsNamMidsZ8AA8W2kQsR+YQOciEUbMtkKAWIbPHPttfn5e9jqqJQ==}
    peerDependencies:
      '@emotion/is-prop-valid': '*'
      react: ^18.0.0 || ^19.0.0
      react-dom: ^18.0.0 || ^19.0.0
    peerDependenciesMeta:
      '@emotion/is-prop-valid':
        optional: true
      react:
        optional: true
      react-dom:
        optional: true

  fresh@2.0.0:
    resolution: {integrity: sha512-Rx/WycZ60HOaqLKAi6cHRKKI7zxWbJ31MhntmtwMoaTeF7XFH9hhBp8vITaMidfljRQ6eYWCKkaTK+ykVJHP2A==}
    engines: {node: '>= 0.8'}

  fs-constants@1.0.0:
    resolution: {integrity: sha512-y6OAwoSIf7FyjMIv94u+b5rdheZEjzR63GTyZJm5qh4Bi+2YgwLCcI/fPFZkL5PSixOt6ZNKm+w+Hfp/Bciwow==}

  fs.realpath@1.0.0:
    resolution: {integrity: sha512-OO0pH2lK6a0hZnAdau5ItzHPI6pUlvI7jMVnxUQRtw4owF2wk8lOSabtGDCTP4Ggrg2MbGnWO9X8K1t4+fGMDw==}

  fsevents@2.3.3:
    resolution: {integrity: sha512-5xoDfX+fL7faATnagmWPpbFtwh/R77WmMMqqHGS65C3vvB0YHrgF+B1YmZ3441tMj5n63k0212XNoJwzlhffQw==}
    engines: {node: ^8.16.0 || ^10.6.0 || >=11.0.0}
    os: [darwin]

  fstream@1.0.12:
    resolution: {integrity: sha512-WvJ193OHa0GHPEL+AycEJgxvBEwyfRkN1vhjca23OaPVMCaLCXTd5qAu82AjTcgP1UJmytkOKb63Ypde7raDIg==}
    engines: {node: '>=0.6'}
    deprecated: This package is no longer supported.

  function-bind@1.1.2:
    resolution: {integrity: sha512-7XHNxH7qX9xG5mIwxkhumTox/MIRNcOgDrxWsMt2pAr23WHp6MrRlN7FBSFpCpr+oVO0F744iUgR82nJMfG2SA==}

  generator-function@2.0.1:
    resolution: {integrity: sha512-SFdFmIJi+ybC0vjlHN0ZGVGHc3lgE0DxPAT0djjVg+kjOnSqclqmj0KQ7ykTOLP6YxoqOvuAODGdcHJn+43q3g==}
    engines: {node: '>= 0.4'}

  get-intrinsic@1.3.0:
    resolution: {integrity: sha512-9fSjSaos/fRIVIp+xSJlE6lfwhES7LNtKaCBIamHsjr2na1BiABJPo0mOjjz8GJDURarmCPGqaiVg5mfjb98CQ==}
    engines: {node: '>= 0.4'}

  get-proto@1.0.1:
    resolution: {integrity: sha512-sTSfBjoXBp89JvIKIefqw7U2CCebsc74kiY6awiGogKtoSGbgjYE/G/+l9sF3MWFPNc9IcoOC4ODfKHfxFmp0g==}
    engines: {node: '>= 0.4'}

  get-tsconfig@4.13.0:
    resolution: {integrity: sha512-1VKTZJCwBrvbd+Wn3AOgQP/2Av+TfTCOlE4AcRJE72W1ksZXbAx8PPBR9RzgTeSPzlPMHrbANMH3LbltH73wxQ==}

  glob-parent@5.1.2:
    resolution: {integrity: sha512-AOIgSQCepiJYwP3ARnGx+5VnTu2HBYdzbGP45eLw1vr3zB3vZLeyed1sC9hnbcOc9/SrMyM5RPQrkGz4aS9Zow==}
    engines: {node: '>= 6'}

  glob-parent@6.0.2:
    resolution: {integrity: sha512-XxwI8EOhVQgWp6iDL+3b0r86f4d6AX6zSU55HfB4ydCEuXLXc5FcYeOu+nnGftS4TEju/11rt4KJPTMgbfmv4A==}
    engines: {node: '>=10.13.0'}

  glob@10.4.5:
    resolution: {integrity: sha512-7Bv8RF0k6xjo7d4A/PxYLbUCfb6c+Vpd2/mB2yRDlew7Jb5hEXiCD9ibfO7wpk8i4sevK6DFny9h7EYbM3/sHg==}
    hasBin: true

  glob@7.2.3:
    resolution: {integrity: sha512-nFR0zLpU2YCaRxwoCJvL6UvCH2JFyFVIvwTLsIf21AuHlMskA1hhTdk+LlYJtOlYt9v6dvszD2BGRqBL+iQK9Q==}
    deprecated: Glob versions prior to v9 are no longer supported

  globals@14.0.0:
    resolution: {integrity: sha512-oahGvuMGQlPw/ivIYBjVSrWAfWLBeku5tpPE2fOPLi+WHffIWbuh2tCjhyQhTBPMf5E9jDEH4FOmTYgYwbKwtQ==}
    engines: {node: '>=18'}

  globals@15.9.0:
    resolution: {integrity: sha512-SmSKyLLKFbSr6rptvP8izbyxJL4ILwqO9Jg23UA0sDlGlu58V59D1//I3vlc0KJphVdUR7vMjHIplYnzBxorQA==}
    engines: {node: '>=18'}

  goober@2.1.18:
    resolution: {integrity: sha512-2vFqsaDVIT9Gz7N6kAL++pLpp41l3PfDuusHcjnGLfR6+huZkl6ziX+zgVC3ZxpqWhzH6pyDdGrCeDhMIvwaxw==}
    peerDependencies:
      csstype: ^3.0.10

  gopd@1.2.0:
    resolution: {integrity: sha512-ZUKRh6/kUFoAiTAtTYPZJ3hw9wNxx+BIBOijnlG9PnrJsCcSjs1wyyD6vJpaYtgnzDrKYRSqf3OO6Rfa93xsRg==}
    engines: {node: '>= 0.4'}

  graceful-fs@4.2.11:
    resolution: {integrity: sha512-RbJ5/jmFcNNCcDV5o9eTnBLJ/HszWV0P73bc+Ff4nS/rJj+YaS6IGyiOL0VoBYX+l1Wrl3k63h/KrH+nhJ0XvQ==}

  graphemer@1.4.0:
    resolution: {integrity: sha512-EtKwoO6kxCL9WO5xipiHTZlSzBm7WLT627TqC/uVRd0HKmq8NXyebnNYxDoBi7wt8eTWrUrKXCOVaFq9x1kgag==}

  has-flag@4.0.0:
    resolution: {integrity: sha512-EykJT/Q1KjTWctppgIAgfSO0tKVuZUjhgMr17kqTumMl6Afv3EISleU7qZUzoXDFTAHTDC4NOoG/ZxU3EvlMPQ==}
    engines: {node: '>=8'}

  has-property-descriptors@1.0.2:
    resolution: {integrity: sha512-55JNKuIW+vq4Ke1BjOTjM2YctQIvCT7GFzHwmfZPGo5wnrgkid0YQtnAleFSqumZm4az3n2BS+erby5ipJdgrg==}

  has-symbols@1.1.0:
    resolution: {integrity: sha512-1cDNdwJ2Jaohmb3sg4OmKaMBwuC48sYni5HUw2DvsC8LjGTLK9h+eb1X6RyuOHe4hT0ULCW68iomhjUoKUqlPQ==}
    engines: {node: '>= 0.4'}

  has-tostringtag@1.0.2:
    resolution: {integrity: sha512-NqADB8VjPFLM2V0VvHUewwwsw0ZWBaIdgo+ieHtK3hasLz4qeCRjYcqfB6AQrBggRKppKF8L52/VqdVsO47Dlw==}
    engines: {node: '>= 0.4'}

  hasown@2.0.2:
    resolution: {integrity: sha512-0hJU9SCPvmMzIBdZFqNPXWa6dqh7WdH0cII9y+CyS8rG3nL48Bclra9HmKhVVUHyPWNH5Y7xDwAB7bfgSjkUMQ==}
    engines: {node: '>= 0.4'}

  http-errors@2.0.0:
    resolution: {integrity: sha512-FtwrG/euBzaEjYeRqOgly7G0qviiXoJWnvEH2Z1plBdXgbyjv34pHTSb9zoeHMyDy33+DWy5Wt9Wo+TURtOYSQ==}
    engines: {node: '>= 0.8'}

  iconv-lite@0.6.3:
    resolution: {integrity: sha512-4fCk79wshMdzMp2rH06qWrJE4iolqLhCUH+OiuIgU++RB0+94NlDL81atO7GX55uUKueo0txHNtvEyI6D7WdMw==}
    engines: {node: '>=0.10.0'}

  iconv-lite@0.7.0:
    resolution: {integrity: sha512-cf6L2Ds3h57VVmkZe+Pn+5APsT7FpqJtEhhieDCvrE2MK5Qk9MyffgQyuxQTm6BChfeZNtcOLHp9IcWRVcIcBQ==}
    engines: {node: '>=0.10.0'}

  ieee754@1.2.1:
    resolution: {integrity: sha512-dcyqhDvX1C46lXZcVqCpK+FtMRQVdIMN6/Df5js2zouUsqG7I6sFxitIC+7KYK29KdXOLHdu9zL4sFnoVQnqaA==}

  ignore@5.3.2:
    resolution: {integrity: sha512-hsBTNUqQTDwkWtcdYI2i06Y/nUBEsNEDJKjWdigLvegy8kDuJAS8uRlpkkcQpyEXL0Z/pjDy5HBmMjRCJ2gq+g==}
    engines: {node: '>= 4'}

  immediate@3.0.6:
    resolution: {integrity: sha512-XXOFtyqDjNDAQxVfYxuF7g9Il/IbWmmlQg2MYKOH8ExIT1qg6xc4zyS3HaEEATgs1btfzxq15ciUiY7gjSXRGQ==}

  import-fresh@3.3.1:
    resolution: {integrity: sha512-TR3KfrTZTYLPB6jUjfx6MF9WcWrHL9su5TObK4ZkYgBdWKPOFoSoQIdEuTuR82pmtxH2spWG9h6etwfr1pLBqQ==}
    engines: {node: '>=6'}

  imurmurhash@0.1.4:
    resolution: {integrity: sha512-JmXMZ6wuvDmLiHEml9ykzqO6lwFbof0GG4IkcGaENdCRDDmMVnny7s5HsIgHCbaq0w2MyPhDqkhTUgS2LU2PHA==}
    engines: {node: '>=0.8.19'}

  inflight@1.0.6:
    resolution: {integrity: sha512-k92I/b08q4wvFscXCLvqfsHCrjrF7yiXsQuIVvVE7N82W3+aqpzuUdBbfhWcy/FZR3/4IgflMgKLOsvPDrGCJA==}
    deprecated: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.

  inherits@2.0.4:
    resolution: {integrity: sha512-k/vGaX4/Yla3WzyMCvTQOXYeIHvqOKtnqBduzTHpzpQZzAskKMhZ2K+EnBiSM9zGSoIFeMpXKxa4dYeZIQqewQ==}

  inversify@6.0.1:
    resolution: {integrity: sha512-B3ex30927698TJENHR++8FfEaJGqoWOgI6ZY5Ht/nLUsFCwHn6akbwtnUAPCgUepAnTpe2qHxhDNjoKLyz6rgQ==}

  ipaddr.js@1.9.1:
    resolution: {integrity: sha512-0KI/607xoxSToH7GjN1FfSbLoU0+btTicjsQSWQlh/hZykN8KpmMf7uYwPW3R+akZ6R/w18ZlXSHBYXiYUPO3g==}
    engines: {node: '>= 0.10'}

  is-arguments@1.2.0:
    resolution: {integrity: sha512-7bVbi0huj/wrIAOzb8U1aszg9kdi3KN/CyU19CTI7tAoZYEZoL9yCDXpbXN+uPsuWnP02cyug1gleqq+TU+YCA==}
    engines: {node: '>= 0.4'}

  is-binary-path@2.1.0:
    resolution: {integrity: sha512-ZMERYes6pDydyuGidse7OsHxtbI7WVeUEozgR/g7rd0xUimYNlvZRE/K2MgZTjWy725IfelLeVcEM97mmtRGXw==}
    engines: {node: '>=8'}

  is-buffer@1.1.6:
    resolution: {integrity: sha512-NcdALwpXkTm5Zvvbk7owOUSvVvBKDgKP5/ewfXEznmQFfs4ZRmanOeKBTjRVjka3QFoN6XJ+9F3USqfHqTaU5w==}

  is-callable@1.2.7:
    resolution: {integrity: sha512-1BC0BVFhS/p0qtw6enp8e+8OD0UrK0oFLztSjNzhcKA3WDuJxxAPXzPuPtKkjEY9UUoEWlX/8fgKeu2S8i9JTA==}
    engines: {node: '>= 0.4'}

  is-core-module@2.16.1:
    resolution: {integrity: sha512-UfoeMA6fIJ8wTYFEUjelnaGI67v6+N7qXJEvQuIGa99l4xsCruSYOVSQ0uPANn4dAzm8lkYPaKLrrijLq7x23w==}
    engines: {node: '>= 0.4'}

  is-extglob@2.1.1:
    resolution: {integrity: sha512-SbKbANkN603Vi4jEZv49LeVJMn4yGwsbzZworEoyEiutsN3nJYdbO36zfhGJ6QEDpOZIFkDtnq5JRxmvl3jsoQ==}
    engines: {node: '>=0.10.0'}

  is-fullwidth-code-point@3.0.0:
    resolution: {integrity: sha512-zymm5+u+sCsSWyD9qNaejV3DFvhCKclKdizYaJUuHA83RLjb7nSuGnddCHGv0hk+KY7BMAlsWeK4Ueg6EV6XQg==}
    engines: {node: '>=8'}

  is-generator-function@1.1.2:
    resolution: {integrity: sha512-upqt1SkGkODW9tsGNG5mtXTXtECizwtS2kA161M+gJPc1xdb/Ax629af6YrTwcOeQHbewrPNlE5Dx7kzvXTizA==}
    engines: {node: '>= 0.4'}

  is-glob@4.0.3:
    resolution: {integrity: sha512-xelSayHH36ZgE7ZWhli7pW34hNbNl8Ojv5KVmkJD4hBdD3th8Tfk9vYasLM+mXWOZhFkgZfxhLSnrwRr4elSSg==}
    engines: {node: '>=0.10.0'}

  is-nan@1.3.2:
    resolution: {integrity: sha512-E+zBKpQ2t6MEo1VsonYmluk9NxGrbzpeeLC2xIViuO2EjU2xsXsBPwTr3Ykv9l08UYEVEdWeRZNouaZqF6RN0w==}
    engines: {node: '>= 0.4'}

  is-number@7.0.0:
    resolution: {integrity: sha512-41Cifkg6e8TylSpdtTpeLVMqvSBEVzTttHvERD741+pnZ8ANv0004MRL43QKPDlK9cGvNp6NZWZUBlbGXYxxng==}
    engines: {node: '>=0.12.0'}

  is-path-inside@3.0.3:
    resolution: {integrity: sha512-Fd4gABb+ycGAmKou8eMftCupSir5lRxqf4aD/vd0cD2qc4HL07OjCeuHMr8Ro4CoMaeCKDB0/ECBOVWjTwUvPQ==}
    engines: {node: '>=8'}

  is-promise@4.0.0:
    resolution: {integrity: sha512-hvpoI6korhJMnej285dSg6nu1+e6uxs7zG3BYAm5byqDsgJNWwxzM6z6iZiAgQR4TJ30JmBTOwqZUw3WlyH3AQ==}

  is-regex@1.2.1:
    resolution: {integrity: sha512-MjYsKHO5O7mCsmRGxWcLWheFqN9DJ/2TmngvjKXihe6efViPqc274+Fx/4fYj/r03+ESvBdTXK0V6tA3rgez1g==}
    engines: {node: '>= 0.4'}

  is-typed-array@1.1.15:
    resolution: {integrity: sha512-p3EcsicXjit7SaskXHs1hA91QxgTw46Fv6EFKKGS5DRFLD8yKnohjF3hxoju94b/OcMZoQukzpPpBE9uLVKzgQ==}
    engines: {node: '>= 0.4'}

  isarray@1.0.0:
    resolution: {integrity: sha512-VLghIWNM6ELQzo7zwmcg0NmTVyWKYjvIeM83yjp0wRDTmUnrM678fQbcKBo6n2CJEF0szoG//ytg+TKla89ALQ==}

  isexe@2.0.0:
    resolution: {integrity: sha512-RHxMLp9lnKHGHRng9QFhRCMbYAcVpn69smSGcq3f36xjgVVWThj4qqLbTLlq7Ssj8B+fIQ1EuCEGI2lKsyQeIw==}

  jackspeak@3.4.3:
    resolution: {integrity: sha512-OGlZQpz2yfahA/Rd1Y8Cd9SIEsqvXkLVoSw/cgwhnhFMDbsQFeZYoJJ7bIZBS9BcamUW96asq/npPWugM+RQBw==}

  javascript-obfuscator@4.1.1:
    resolution: {integrity: sha512-gt+KZpIIrrxXHEQGD8xZrL8mTRwRY0U76/xz/YX0gZdPrSqQhT/c7dYLASlLlecT3r+FxE7je/+C0oLnTDCx4A==}
    engines: {node: '>=12.22.0'}
    hasBin: true

  jiti@1.21.7:
    resolution: {integrity: sha512-/imKNG4EbWNrVjoNC/1H5/9GFy+tqjGBHCaSsN+P2RnPqjsLmv6UD3Ej+Kj8nBWaRAwyk7kK5ZUc+OEatnTR3A==}
    hasBin: true

  js-string-escape@1.0.1:
    resolution: {integrity: sha512-Smw4xcfIQ5LVjAOuJCvN/zIodzA/BBSsluuoSykP+lUvScIi4U6RJLfwHet5cxFnCswUjISV8oAXaqaJDY3chg==}
    engines: {node: '>= 0.8'}

  js-tokens@4.0.0:
    resolution: {integrity: sha512-RdJUflcE3cUzKiMqQgsCu06FPu9UdIJO0beYbPhHN4k6apgJtifcoCtT9bcxOpYBtpD2kCM6Sbzg4CausW/PKQ==}

  js-yaml@4.1.1:
    resolution: {integrity: sha512-qQKT4zQxXl8lLwBtHMWwaTcGfFOZviOJet3Oy/xmGk2gZH677CJM9EvtfdSkgWcATZhj/55JZ0rmy3myCT5lsA==}
    hasBin: true

  json-buffer@3.0.1:
    resolution: {integrity: sha512-4bV5BfR2mqfQTJm+V5tPPdf+ZpuhiIvTuAB5g8kcrXOZpTT/QwwVRWBywX1ozr6lEuPdbHxwaJlm9G6mI2sfSQ==}

  json-schema-traverse@0.4.1:
    resolution: {integrity: sha512-xbbCH5dCYU5T8LcEhhuh7HJ88HXuW3qsI3Y0zOZFKfZEHcpWiHU/Jxzk629Brsab/mMiHQti9wMP+845RPe3Vg==}

  json-stable-stringify-without-jsonify@1.0.1:
    resolution: {integrity: sha512-Bdboy+l7tA3OGW6FjyFHWkP5LuByj1Tk33Ljyq0axyzdk9//JSi2u3fP1QSmd1KNwq6VOKYGlAu87CisVir6Pw==}

  jszip@3.10.1:
    resolution: {integrity: sha512-xXDvecyTpGLrqFrvkrUSoxxfJI5AH7U8zxxtVclpsUtMCq4JQ290LY8AW5c7Ggnr/Y/oK+bQMbqK2qmtk3pN4g==}

  keyv@4.5.4:
    resolution: {integrity: sha512-oxVHkHR/EJf2CNXnWxRLW6mg7JyCCUcG0DtEGmL2ctUo1PNTin1PUil+r/+4r5MpVgC/fn1kjsx7mjSujKqIpw==}

  lazystream@1.0.1:
    resolution: {integrity: sha512-b94GiNHQNy6JNTrt5w6zNyffMrNkXZb3KTkCZJb2V1xaEGCk093vkZ2jk3tpaeP33/OiXC+WvK9AxUebnf5nbw==}
    engines: {node: '>= 0.6.3'}

  levn@0.3.0:
    resolution: {integrity: sha512-0OO4y2iOHix2W6ujICbKIaEQXvFQHue65vUG3pb5EUomzPI90z9hsA1VsO/dbIIpC53J8gxM9Q4Oho0jrCM/yA==}
    engines: {node: '>= 0.8.0'}

  levn@0.4.1:
    resolution: {integrity: sha512-+bT2uH4E5LGE7h/n3evcS/sQlJXCpIp6ym8OWJ5eV6+67Dsql/LaaT7qJBAt2rzfoa/5QBGBhxDix1dMt2kQKQ==}
    engines: {node: '>= 0.8.0'}

  libphonenumber-js@1.12.26:
    resolution: {integrity: sha512-MagMOuqEXB2Pa90cWE+BoCmcKJx+de5uBIicaUkQ+uiEslZ0OBMNOkSZT/36syXNHu68UeayTxPm3DYM2IHoLQ==}

  lie@3.3.0:
    resolution: {integrity: sha512-UaiMJzeWRlEujzAuw5LokY1L5ecNQYZKfmyZ9L7wDHb/p5etKaxXhohBcrw0EYby+G/NA52vRSN4N39dxHAIwQ==}

  lilconfig@3.1.3:
    resolution: {integrity: sha512-/vlFKAoH5Cgt3Ie+JLhRbwOsCQePABiU3tJ1egGvyQ+33R/vcwM2Zl2QR/LzjsBeItPt3oSVXapn+m4nQDvpzw==}
    engines: {node: '>=14'}

  lines-and-columns@1.2.4:
    resolution: {integrity: sha512-7ylylesZQ/PV29jhEDl3Ufjo6ZX7gCqJr5F7PKrqc93v7fzSymt1BpwEU8nAUXs8qzzvqhbjhK5QZg6Mt/HkBg==}

  listenercount@1.0.1:
    resolution: {integrity: sha512-3mk/Zag0+IJxeDrxSgaDPy4zZ3w05PRZeJNnlWhzFz5OkX49J4krc+A8X2d2M69vGMBEX0uyl8M+W+8gH+kBqQ==}

  locate-path@6.0.0:
    resolution: {integrity: sha512-iPZK6eYjbxRu3uB4/WZ3EsEIMJFMqAoopl3R+zuq0UjcAm/MO6KCweDgPfP3elTztoKP3KtnVHxTn2NHBSDVUw==}
    engines: {node: '>=10'}

  lodash.defaults@4.2.0:
    resolution: {integrity: sha512-qjxPLHd3r5DnsdGacqOMU6pb/avJzdh9tFX2ymgoZE27BmjXrNy/y4LoaiTeAb+O3gL8AfpJGtqfX/ae2leYYQ==}

  lodash.difference@4.5.0:
    resolution: {integrity: sha512-dS2j+W26TQ7taQBGN8Lbbq04ssV3emRw4NY58WErlTO29pIqS0HmoT5aJ9+TUQ1N3G+JOZSji4eugsWwGp9yPA==}

  lodash.escaperegexp@4.1.2:
    resolution: {integrity: sha512-TM9YBvyC84ZxE3rgfefxUWiQKLilstD6k7PTGt6wfbtXF8ixIJLOL3VYyV/z+ZiPLsVxAsKAFVwWlWeb2Y8Yyw==}

  lodash.flatten@4.4.0:
    resolution: {integrity: sha512-C5N2Z3DgnnKr0LOpv/hKCgKdb7ZZwafIrsesve6lmzvZIRZRGaZ/l6Q8+2W7NaT+ZwO3fFlSCzCzrDCFdJfZ4g==}

  lodash.groupby@4.6.0:
    resolution: {integrity: sha512-5dcWxm23+VAoz+awKmBaiBvzox8+RqMgFhi7UvX9DHZr2HdxHXM/Wrf8cfKpsW37RNrvtPn6hSwNqurSILbmJw==}

  lodash.isboolean@3.0.3:
    resolution: {integrity: sha512-Bz5mupy2SVbPHURB98VAcw+aHh4vRV5IPNhILUCsOzRmsTmSQ17jIuqopAentWoehktxGd9e/hbIXq980/1QJg==}

  lodash.isequal@4.5.0:
    resolution: {integrity: sha512-pDo3lu8Jhfjqls6GkMgpahsF9kCyayhgykjyLMNFTKWrpVdAQtYyB4muAMWozBB4ig/dtWAmsMxLEI8wuz+DYQ==}
    deprecated: This package is deprecated. Use require('node:util').isDeepStrictEqual instead.

  lodash.isfunction@3.0.9:
    resolution: {integrity: sha512-AirXNj15uRIMMPihnkInB4i3NHeb4iBtNg9WRWuK2o31S+ePwwNmDPaTL3o7dTJ+VXNZim7rFs4rxN4YU1oUJw==}

  lodash.isnil@4.0.0:
    resolution: {integrity: sha512-up2Mzq3545mwVnMhTDMdfoG1OurpA/s5t88JmQX809eH3C8491iu2sfKhTfhQtKY78oPNhiaHJUpT/dUDAAtng==}

  lodash.isplainobject@4.0.6:
    resolution: {integrity: sha512-oSXzaWypCMHkPC3NvBEaPHf0KsA5mvPrOPgQWDsbg8n7orZ290M0BmC/jgRZ4vcJ6DTAhjrsSYgdsW/F+MFOBA==}

  lodash.isundefined@3.0.1:
    resolution: {integrity: sha512-MXB1is3s899/cD8jheYYE2V9qTHwKvt+npCwpD+1Sxm3Q3cECXCiYHjeHWXNwr6Q0SOBPrYUDxendrO6goVTEA==}

  lodash.merge@4.6.2:
    resolution: {integrity: sha512-0KpjqXRVvrYyCsX1swR/XTK0va6VQkQM6MNo7PqW77ByjAhoARA8EfrP1N4+KlKj8YS0ZUCtRT/YUuhyYDujIQ==}

  lodash.union@4.6.0:
    resolution: {integrity: sha512-c4pB2CdGrGdjMKYLA+XiRDO7Y0PRQbm/Gzg8qMj+QH+pFVAoTp5sBpO0odL3FjoPCGjK96p6qsP+yQoiLoOBcw==}

  lodash.uniq@4.5.0:
    resolution: {integrity: sha512-xfBaXQd9ryd9dlSDvnvI0lvxfLJlYAZzXomUYzLKtUeOQvOP5piqAWuGtrhWeqaXK9hhoM/iyJc5AV+XfsX3HQ==}

  loose-envify@1.4.0:
    resolution: {integrity: sha512-lyuxPGr/Wfhrlem2CL/UcnUc1zcqKAImBDzukY7Y5F/yQiNdko6+fRLevlw1HgMySw7f611UIY408EtxRSoK3Q==}
    hasBin: true

  lru-cache@10.4.3:
    resolution: {integrity: sha512-JNAzZcXrCt42VGLuYz0zfAzDfAvJWW6AfYlDBQyDV5DClI2m5sAmK+OIO7s59XfsRsWHp02jAJrRadPRGTt6SQ==}

  lucide-react@0.540.0:
    resolution: {integrity: sha512-armkCAqQvO62EIX4Hq7hqX/q11WSZu0Jd23cnnqx0/49yIxGXyL/zyZfBxNN9YDx0ensPTb4L+DjTh3yQXUxtQ==}
    peerDependencies:
      react: ^16.5.1 || ^17.0.0 || ^18.0.0 || ^19.0.0

  math-intrinsics@1.1.0:
    resolution: {integrity: sha512-/IXtbwEk5HTPyEwyKX6hGkYXxM9nbj64B+ilVJnC/R6B0pH5G4V3b0pVbL7DBj4tkhBAppbQUlf6F6Xl9LHu1g==}
    engines: {node: '>= 0.4'}

  md5@2.3.0:
    resolution: {integrity: sha512-T1GITYmFaKuO91vxyoQMFETst+O71VUPEU3ze5GNzDm0OWdP8v1ziTaAEPUr/3kLsY3Sftgz242A1SetQiDL7g==}

  media-typer@0.3.0:
    resolution: {integrity: sha512-dq+qelQ9akHpcOl/gUVRTxVIOkAJ1wR3QAvb4RsVjS8oVoFjDGTc679wJYmUmknUF5HwMLOgb5O+a3KxfWapPQ==}
    engines: {node: '>= 0.6'}

  media-typer@1.1.0:
    resolution: {integrity: sha512-aisnrDP4GNe06UcKFnV5bfMNPBUw4jsLGaWwWfnH3v02GnBuXX2MCVn5RbrWo0j3pczUilYblq7fQ7Nw2t5XKw==}
    engines: {node: '>= 0.8'}

  merge-descriptors@2.0.0:
    resolution: {integrity: sha512-Snk314V5ayFLhp3fkUREub6WtjBfPdCPY1Ln8/8munuLuiYhsABgBVWsozAG+MWMbVEvcdcpbi9R7ww22l9Q3g==}
    engines: {node: '>=18'}

  merge2@1.4.1:
    resolution: {integrity: sha512-8q7VEgMJW4J8tcfVPy8g09NcQwZdbwFEqhe/WZkoIzjn/3TGDwtOCYtXGxA3O8tPzpczCCDgv+P2P5y00ZJOOg==}
    engines: {node: '>= 8'}

  micromatch@4.0.8:
    resolution: {integrity: sha512-PXwfBhYu0hBCPw8Dn0E+WDYb7af3dSLVWKi3HGv84IdF4TyFoC0ysxFd0Goxw7nSv4T/PzEJQxsYsEiFCKo2BA==}
    engines: {node: '>=8.6'}

  mime-db@1.52.0:
    resolution: {integrity: sha512-sPU4uV7dYlvtWJxwwxHD0PuihVNiE7TyAbQ5SWxDCB9mUYvOgroQOwYQQOKPJ8CIbE+1ETVlOoK1UC2nU3gYvg==}
    engines: {node: '>= 0.6'}

  mime-db@1.54.0:
    resolution: {integrity: sha512-aU5EJuIN2WDemCcAp2vFBfp/m4EAhWJnUNSSw0ixs7/kXbd6Pg64EmwJkNdFhB8aWt1sH2CTXrLxo/iAGV3oPQ==}
    engines: {node: '>= 0.6'}

  mime-types@2.1.35:
    resolution: {integrity: sha512-ZDY+bPm5zTTF+YpCrAU9nK0UgICYPT0QtT1NZWFv4s++TNkcgVaT0g6+4R2uI4MjQjzysHB1zxuWL50hzaeXiw==}
    engines: {node: '>= 0.6'}

  mime-types@3.0.1:
    resolution: {integrity: sha512-xRc4oEhT6eaBpU1XF7AjpOFD+xQmXNB5OVKwp4tqCuBpHLS/ZbBDrc07mYTDqVMg6PfxUjjNp85O6Cd2Z/5HWA==}
    engines: {node: '>= 0.6'}

  minimatch@3.1.2:
    resolution: {integrity: sha512-J7p63hRiAjw1NDEww1W7i37+ByIrOWO5XQQAzZ3VOcL0PNybwpfmV/N05zFAzwQ9USyEcX6t3UO+K5aqBQOIHw==}

  minimatch@5.1.6:
    resolution: {integrity: sha512-lKwV/1brpG6mBUFHtb7NUmtABCb2WZZmm2wNiOA5hAb8VdCS4B3dtMWyvcoViccwAW/COERjXLt0zP1zXUN26g==}
    engines: {node: '>=10'}

  minimatch@9.0.5:
    resolution: {integrity: sha512-G6T0ZX48xgozx7587koeX9Ys2NYy6Gmv//P89sEte9V9whIapMNF4idKxnW2QtCcLiTWlb/wfCabAtAFWhhBow==}
    engines: {node: '>=16 || 14 >=14.17'}

  minimist@1.2.8:
    resolution: {integrity: sha512-2yyAR8qBkN3YuheJanUpWC5U3bb5osDywNB8RzDVlDwDHbocAJveqqj1u8+SVD7jkWT4yvsHCpWqqWqAxb0zCA==}

  minipass@7.1.2:
    resolution: {integrity: sha512-qOOzS1cBTWYF4BH8fVePDBOO9iptMnGUEZwNc/cMWnTV2nVLZ7VoNWEPHkYczZA0pdoA7dl6e7FL659nX9S2aw==}
    engines: {node: '>=16 || 14 >=14.17'}

  mkdirp@0.5.6:
    resolution: {integrity: sha512-FP+p8RB8OWpF3YZBCrP5gtADmtXApB5AMLn+vdyA+PyxCjrCs00mjyUozssO33cwDeT3wNGdLxJ5M//YqtHAJw==}
    hasBin: true

  mkdirp@2.1.3:
    resolution: {integrity: sha512-sjAkg21peAG9HS+Dkx7hlG9Ztx7HLeKnvB3NQRcu/mltCVmvkF0pisbiTSfDVYTT86XEfZrTUosLdZLStquZUw==}
    engines: {node: '>=10'}
    hasBin: true

  motion-dom@12.23.23:
    resolution: {integrity: sha512-n5yolOs0TQQBRUFImrRfs/+6X4p3Q4n1dUEqt/H58Vx7OW6RF+foWEgmTVDhIWJIMXOuNNL0apKH2S16en9eiA==}

  motion-utils@12.23.6:
    resolution: {integrity: sha512-eAWoPgr4eFEOFfg2WjIsMoqJTW6Z8MTUCgn/GZ3VRpClWBdnbjryiA3ZSNLyxCTmCQx4RmYX6jX1iWHbenUPNQ==}

  ms@2.1.3:
    resolution: {integrity: sha512-6FlzubTLZG3J2a/NVCAleEhjzq5oxgHyaCU9yYXvcLsvoVaHJq/s5xXI6/XXP6tz7R9xAOtHnSO/tXtF3WRTlA==}

  multer@2.0.2:
    resolution: {integrity: sha512-u7f2xaZ/UG8oLXHvtF/oWTRvT44p9ecwBBqTwgJVq0+4BW1g8OW01TyMEGWBHbyMOYVHXslaut7qEQ1meATXgw==}
    engines: {node: '>= 10.16.0'}

  multimatch@5.0.0:
    resolution: {integrity: sha512-ypMKuglUrZUD99Tk2bUQ+xNQj43lPEfAeX2o9cTteAmShXy2VHDJpuwu1o0xqoKCt9jLVAvwyFKdLTPXKAfJyA==}
    engines: {node: '>=10'}

  mz@2.7.0:
    resolution: {integrity: sha512-z81GNO7nnYMEhrGh9LeymoE4+Yr0Wn5McHIZMK5cfQCl+NDX08sCZgUc9/6MHni9IWuFLm1Z3HTCXu2z9fN62Q==}

  nanoid@3.3.11:
    resolution: {integrity: sha512-N8SpfPUnUp1bK+PMYW8qSWdl9U+wwNWI4QKxOYDy9JAro3WMX7p2OeVRF9v+347pnakNevPmiHhNmZ2HbFA76w==}
    engines: {node: ^10 || ^12 || ^13.7 || ^14 || >=15.0.1}
    hasBin: true

  natural-compare@1.4.0:
    resolution: {integrity: sha512-OWND8ei3VtNC9h7V60qff3SVobHr996CTwgxubgyQYEpg290h9J0buyECNNJexkFm5sOajh5G116RYA1c8ZMSw==}

  negotiator@1.0.0:
    resolution: {integrity: sha512-8Ofs/AUQh8MaEcrlq5xOX0CQ9ypTF5dl78mjlMNfOK08fzpgTHQRQPBxcPlEtIw0yRpws+Zo/3r+5WRby7u3Gg==}
    engines: {node: '>= 0.6'}

  node-fetch-native@1.6.7:
    resolution: {integrity: sha512-g9yhqoedzIUm0nTnTqAQvueMPVOuIY16bqgAJJC8XOOubYFNwz6IER9qs0Gq2Xd0+CecCKFjtdDTMA4u4xG06Q==}

  node-releases@2.0.27:
    resolution: {integrity: sha512-nmh3lCkYZ3grZvqcCH+fjmQ7X+H0OeZgP40OierEaAptX4XofMh5kwNbWh7lBduUzCcV/8kZ+NDLCwm2iorIlA==}

  normalize-path@3.0.0:
    resolution: {integrity: sha512-6eZs5Ls3WtCisHWp9S2GUy8dqkpGi4BVSz3GaqiE6ezub0512ESztXUwUB6C6IKbQkY2Pnb/mD4WYojCRwcwLA==}
    engines: {node: '>=0.10.0'}

  normalize-range@0.1.2:
    resolution: {integrity: sha512-bdok/XvKII3nUpklnV6P2hxtMNrCboOjAcyBuQnWEhO665FwrSNRxU+AqpsyvO6LgGYPspN+lu5CLtw4jPRKNA==}
    engines: {node: '>=0.10.0'}

  object-assign@4.1.1:
    resolution: {integrity: sha512-rJgTQnkUnH1sFw8yT6VSU3zD3sWmu6sZhIseY8VX+GRu3P6F7Fu+JNDoXfklElbLJSnc3FUQHVe4cU5hj+BcUg==}
    engines: {node: '>=0.10.0'}

  object-hash@3.0.0:
    resolution: {integrity: sha512-RSn9F68PjH9HqtltsSnqYC1XXoWe9Bju5+213R98cNGttag9q9yAOTzdbsqvIa7aNm5WffBZFpWYr2aWrklWAw==}
    engines: {node: '>= 6'}

  object-inspect@1.13.4:
    resolution: {integrity: sha512-W67iLl4J2EXEGTbfeHCffrjDfitvLANg0UlX3wFUUSTx92KXRFegMHUVgSqE+wvhAbi4WqjGg9czysTV2Epbew==}
    engines: {node: '>= 0.4'}

  object-is@1.1.6:
    resolution: {integrity: sha512-F8cZ+KfGlSGi09lJT7/Nd6KJZ9ygtvYC0/UYYLI9nmQKLMnydpB9yvbv9K1uSkEu7FU9vYPmVwLg328tX+ot3Q==}
    engines: {node: '>= 0.4'}

  object-keys@1.1.1:
    resolution: {integrity: sha512-NuAESUOUMrlIXOfHKzD6bpPu3tYt3xvjNdRIQ+FeT0lNb4K8WR70CaDxhuNguS2XG+GjkyMwOzsN5ZktImfhLA==}
    engines: {node: '>= 0.4'}

  ofetch@1.5.1:
    resolution: {integrity: sha512-2W4oUZlVaqAPAil6FUg/difl6YhqhUR7x2eZY4bQCko22UXg3hptq9KLQdqFClV+Wu85UX7hNtdGTngi/1BxcA==}

  on-finished@2.4.1:
    resolution: {integrity: sha512-oVlzkg3ENAhCk2zdv7IJwd/QUD4z2RxRwpkcGY8psCVcCYZNq4wYnVWALHM+brtuJjePWiYF/ClmuDr8Ch5+kg==}
    engines: {node: '>= 0.8'}

  once@1.4.0:
    resolution: {integrity: sha512-lNaJgI+2Q5URQBkccEKHTQOPaXdUxnZZElQTZY0MFUAuaEqe1E+Nyvgdz/aIyNi6Z9MzO5dv1H8n58/GELp3+w==}

  opencollective-postinstall@2.0.3:
    resolution: {integrity: sha512-8AV/sCtuzUeTo8gQK5qDZzARrulB3egtLzFgteqB2tcT4Mw7B8Kt7JcDHmltjz6FOAHsvTevk70gZEbhM4ZS9Q==}
    hasBin: true

  optionator@0.8.3:
    resolution: {integrity: sha512-+IW9pACdk3XWmmTXG8m3upGUJst5XRGzxMRjXzAuJ1XnIFNvfhjjIuYkDvysnPQ7qzqVzLt78BCruntqRhWQbA==}
    engines: {node: '>= 0.8.0'}

  optionator@0.9.4:
    resolution: {integrity: sha512-6IpQ7mKUxRcZNLIObR0hz7lxsapSSIYNZJwXPGeF0mTVqGKFIXj1DQcMoT22S3ROcLyY/rz0PWaWZ9ayWmad9g==}
    engines: {node: '>= 0.8.0'}

  p-limit@3.1.0:
    resolution: {integrity: sha512-TYOanM3wGwNGsZN2cVTYPArw454xnXj5qmWF1bEoAc4+cU/ol7GVh7odevjp1FNHduHc3KZMcFduxU5Xc6uJRQ==}
    engines: {node: '>=10'}

  p-locate@5.0.0:
    resolution: {integrity: sha512-LaNjtRWUBY++zB5nE/NwcaoMylSPk+S+ZHNB1TzdbMJMny6dynpAGt7X/tl/QYq3TIeE6nxHppbo2LGymrG5Pw==}
    engines: {node: '>=10'}

  package-json-from-dist@1.0.1:
    resolution: {integrity: sha512-UEZIS3/by4OC8vL3P2dTXRETpebLI2NiI5vIrjaD/5UtrkFX/tNbwjTSRAGC/+7CAo2pIcBaRgWmcBBHcsaCIw==}

  pako@1.0.11:
    resolution: {integrity: sha512-4hLB8Py4zZce5s4yd9XzopqwVv/yGNhV1Bl8NTmCq1763HeK2+EwVTv+leGeL13Dnh2wfbqowVPXCIO0z4taYw==}

  papaparse@5.5.3:
    resolution: {integrity: sha512-5QvjGxYVjxO59MGU2lHVYpRWBBtKHnlIAcSe1uNFCkkptUh63NFRj0FJQm7nR67puEruUci/ZkjmEFrjCAyP4A==}

  parent-module@1.0.1:
    resolution: {integrity: sha512-GQ2EWRpQV8/o+Aw8YqtfZZPfNRWZYkbidE9k5rpl/hC3vtHHBfGm2Ifi6qWV+coDGkrUKZAxE3Lot5kcsRlh+g==}
    engines: {node: '>=6'}

  parseurl@1.3.3:
    resolution: {integrity: sha512-CiyeOxFT/JZyN5m0z9PfXw4SCBJ6Sygz1Dpl0wqjlhDEGGBP1GnsUVEL0p63hoG1fcj3fHynXi9NYO4nWOL+qQ==}
    engines: {node: '>= 0.8'}

  path-exists@4.0.0:
    resolution: {integrity: sha512-ak9Qy5Q7jYb2Wwcey5Fpvg2KoAc/ZIhLSLOSBmRmygPsGwkVVt0fZa0qrtMz+m6tJTAHfZQ8FnmB4MG4LWy7/w==}
    engines: {node: '>=8'}

  path-is-absolute@1.0.1:
    resolution: {integrity: sha512-AVbw3UJ2e9bq64vSaS9Am0fje1Pa8pbGqTTsmXfaIiMpnr5DlDhfJOuLj9Sf95ZPVDAUerDfEk88MPmPe7UCQg==}
    engines: {node: '>=0.10.0'}

  path-key@3.1.1:
    resolution: {integrity: sha512-ojmeN0qd+y0jszEtoY48r0Peq5dwMEkIlCOu6Q5f41lfkswXuKtYrhgoTpLnyIcHm24Uhqx+5Tqm2InSwLhE6Q==}
    engines: {node: '>=8'}

  path-parse@1.0.7:
    resolution: {integrity: sha512-LDJzPVEEEPR+y48z93A0Ed0yXb8pAByGWo/k5YYdYgpY2/2EsOsksJrq7lOHxryrVOn1ejG6oAp8ahvOIQD8sw==}

  path-scurry@1.11.1:
    resolution: {integrity: sha512-Xa4Nw17FS9ApQFJ9umLiJS4orGjm7ZzwUrwamcGQuHSzDyth9boKDaycYdDcZDuqYATXw4HFXgaqWTctW/v1HA==}
    engines: {node: '>=16 || 14 >=14.18'}

  path-to-regexp@8.3.0:
    resolution: {integrity: sha512-7jdwVIRtsP8MYpdXSwOS0YdD0Du+qOoF/AEPIt88PcCFrZCzx41oxku1jD88hZBwbNUIEfpqvuhjFaMAqMTWnA==}

  picocolors@1.1.1:
    resolution: {integrity: sha512-xceH2snhtb5M9liqDsmEw56le376mTZkEX/jEb/RxNFyegNul7eNslCXP9FDj/Lcu0X8KEyMceP2ntpaHrDEVA==}

  picomatch@2.3.1:
    resolution: {integrity: sha512-JU3teHTNjmE2VCGFzuY8EXzCDVwEqB2a8fsIvwaStHhAWJEeVd1o1QD80CU6+ZdEXXSLbSsuLwJjkCBWqRQUVA==}
    engines: {node: '>=8.6'}

  picomatch@4.0.3:
    resolution: {integrity: sha512-5gTmgEY/sqK6gFXLIsQNH19lWb4ebPDLA4SdLP7dsWkIXHWlG66oPuVvXSGFPppYZz8ZDZq0dYYrbHfBCVUb1Q==}
    engines: {node: '>=12'}

  pify@2.3.0:
    resolution: {integrity: sha512-udgsAY+fTnvv7kI7aaxbqwWNb0AHiB0qBO89PZKPkoTmGOgdbrHDKD+0B2X4uTfJ/FT1R09r9gTsjUjNJotuog==}
    engines: {node: '>=0.10.0'}

  pirates@4.0.7:
    resolution: {integrity: sha512-TfySrs/5nm8fQJDcBDuUng3VOUKsd7S+zqvbOTiGXHfxX4wK31ard+hoNuvkicM/2YFzlpDgABOevKSsB4G/FA==}
    engines: {node: '>= 6'}

  possible-typed-array-names@1.1.0:
    resolution: {integrity: sha512-/+5VFTchJDoVj3bhoqi6UeymcD00DAwb1nJwamzPvHEszJ4FpF6SNNbUbOS8yI56qHzdV8eK0qEfOSiodkTdxg==}
    engines: {node: '>= 0.4'}

  postcss-import@15.1.0:
    resolution: {integrity: sha512-hpr+J05B2FVYUAXHeK1YyI267J/dDDhMU6B6civm8hSY1jYJnBXxzKDKDswzJmtLHryrjhnDjqqp/49t8FALew==}
    engines: {node: '>=14.0.0'}
    peerDependencies:
      postcss: ^8.0.0

  postcss-js@4.1.0:
    resolution: {integrity: sha512-oIAOTqgIo7q2EOwbhb8UalYePMvYoIeRY2YKntdpFQXNosSu3vLrniGgmH9OKs/qAkfoj5oB3le/7mINW1LCfw==}
    engines: {node: ^12 || ^14 || >= 16}
    peerDependencies:
      postcss: ^8.4.21

  postcss-load-config@4.0.2:
    resolution: {integrity: sha512-bSVhyJGL00wMVoPUzAVAnbEoWyqRxkjv64tUl427SKnPrENtq6hJwUojroMz2VB+Q1edmi4IfrAPpami5VVgMQ==}
    engines: {node: '>= 14'}
    peerDependencies:
      postcss: '>=8.0.9'
      ts-node: '>=9.0.0'
    peerDependenciesMeta:
      postcss:
        optional: true
      ts-node:
        optional: true

  postcss-nested@6.2.0:
    resolution: {integrity: sha512-HQbt28KulC5AJzG+cZtj9kvKB93CFCdLvog1WFLf1D+xmMvPGlBstkpTEZfK5+AN9hfJocyBFCNiqyS48bpgzQ==}
    engines: {node: '>=12.0'}
    peerDependencies:
      postcss: ^8.2.14

  postcss-selector-parser@6.1.2:
    resolution: {integrity: sha512-Q8qQfPiZ+THO/3ZrOrO0cJJKfpYCagtMUkXbnEfmgUjwXg6z/WBeOyS9APBBPCTSiDV+s4SwQGu8yFsiMRIudg==}
    engines: {node: '>=4'}

  postcss-value-parser@4.2.0:
    resolution: {integrity: sha512-1NNCs6uurfkVbeXG4S8JFT9t19m45ICnif8zWLd5oPSZ50QnwMfK+H3jv408d4jw/7Bttv5axS5IiHoLaVNHeQ==}

  postcss@8.5.6:
    resolution: {integrity: sha512-3Ybi1tAuwAP9s0r1UQ2J4n5Y0G05bJkpUIO0/bI9MhwmD70S5aTWbXGBwxHrelT+XM1k6dM0pk+SwNkpTRN7Pg==}
    engines: {node: ^10 || ^12 || >=14}

  prelude-ls@1.1.2:
    resolution: {integrity: sha512-ESF23V4SKG6lVSGZgYNpbsiaAkdab6ZgOxe52p7+Kid3W3u3bxR4Vfd/o21dmN7jSt0IwgZ4v5MUd26FEtXE9w==}
    engines: {node: '>= 0.8.0'}

  prelude-ls@1.2.1:
    resolution: {integrity: sha512-vkcDPrRZo1QZLbn5RLGPpg/WmIQ65qoWWhcGKf/b5eplkkarX0m9z8ppCat4mlOqUsWpyNuYgO3VRyrYHSzX5g==}
    engines: {node: '>= 0.8.0'}

  process-nextick-args@2.0.1:
    resolution: {integrity: sha512-3ouUOpQhtgrbOa17J7+uxOTpITYWaGP7/AhoR3+A+/1e9skrzelGi/dXzEYyvbxubEF6Wn2ypscTKiKJFFn1ag==}

  process@0.11.10:
    resolution: {integrity: sha512-cdGef/drWFoydD1JsMzuFf8100nZl+GT+yacc2bEced5f9Rjk4z+WtFUTBu9PhOi9j/jfmBPu0mMEY4wIdAF8A==}
    engines: {node: '>= 0.6.0'}

  proxy-addr@2.0.7:
    resolution: {integrity: sha512-llQsMLSUDUPT44jdrU/O37qlnifitDP+ZwrmmZcoSKyLKvtZxpyV0n2/bD/N4tBAAZ/gJEdZU7KMraoK1+XYAg==}
    engines: {node: '>= 0.10'}

  punycode@2.3.1:
    resolution: {integrity: sha512-vYt7UD1U9Wg6138shLtLOvdAu+8DsC/ilFtEVHcH+wydcSpNE20AfSOduf6MkRFahL5FY7X1oU7nKVZFtfq8Fg==}
    engines: {node: '>=6'}

  qs@6.14.0:
    resolution: {integrity: sha512-YWWTjgABSKcvs/nWBi9PycY/JiPJqOD4JA6o9Sej2AtvSGarXxKC3OQSk4pAarbdQlKAh5D4FCQkJNkW+GAn3w==}
    engines: {node: '>=0.6'}

  queue-microtask@1.2.3:
    resolution: {integrity: sha512-NuaNSa6flKT5JaSYQzJok04JzTL1CA6aGhv5rfLW3PgqA+M2ChpZQnAC8h8i4ZFkBS8X5RqkDBHA7r4hej3K9A==}

  range-parser@1.2.1:
    resolution: {integrity: sha512-Hrgsx+orqoygnmhFbKaHE6c296J+HTAQXoxEF6gNupROmmGJRoyzfG3ccAveqCBrwr/2yxQ5BVd/GTl5agOwSg==}
    engines: {node: '>= 0.6'}

  raw-body@3.0.1:
    resolution: {integrity: sha512-9G8cA+tuMS75+6G/TzW8OtLzmBDMo8p1JRxN5AZ+LAp8uxGA8V8GZm4GQ4/N5QNQEnLmg6SS7wyuSmbKepiKqA==}
    engines: {node: '>= 0.10'}

  react-dom@18.3.1:
    resolution: {integrity: sha512-5m4nQKp+rZRb09LNH59GM4BxTh9251/ylbKIbpe7TpGxfJ+9kv6BLkLBXIjjspbgbnIBNqlI23tRnTWT0snUIw==}
    peerDependencies:
      react: ^18.3.1

  react-hot-toast@2.5.2:
    resolution: {integrity: sha512-Tun3BbCxzmXXM7C+NI4qiv6lT0uwGh4oAfeJyNOjYUejTsm35mK9iCaYLGv8cBz9L5YxZLx/2ii7zsIwPtPUdw==}
    engines: {node: '>=10'}
    peerDependencies:
      react: '>=16'
      react-dom: '>=16'

  react-router-dom@6.26.0:
    resolution: {integrity: sha512-RRGUIiDtLrkX3uYcFiCIxKFWMcWQGMojpYZfcstc63A1+sSnVgILGIm9gNUA6na3Fm1QuPGSBQH2EMbAZOnMsQ==}
    engines: {node: '>=14.0.0'}
    peerDependencies:
      react: '>=16.8'
      react-dom: '>=16.8'

  react-router@6.26.0:
    resolution: {integrity: sha512-wVQq0/iFYd3iZ9H2l3N3k4PL8EEHcb0XlU2Na8nEwmiXgIUElEH6gaJDtUQxJ+JFzmIXaQjfdpcGWaM6IoQGxg==}
    engines: {node: '>=14.0.0'}
    peerDependencies:
      react: '>=16.8'

  react@18.3.1:
    resolution: {integrity: sha512-wS+hAgJShR0KhEvPJArfuPVN1+Hz1t0Y6n5jLrGQbkb4urgPE/0Rve+1kMB1v/oWgHgm4WIcV+i7F2pTVj+2iQ==}
    engines: {node: '>=0.10.0'}

  read-cache@1.0.0:
    resolution: {integrity: sha512-Owdv/Ft7IjOgm/i0xvNDZ1LrRANRfew4b2prF3OWMQLxLfu3bS8FVhCsrSCMK4lR56Y9ya+AThoTpDCTxCmpRA==}

  readable-stream@2.3.8:
    resolution: {integrity: sha512-8p0AUk4XODgIewSi0l8Epjs+EVnWiK7NoDIEGU0HhE7+ZyY8D1IMY7odu5lRrFXGg71L15KG8QrPmum45RTtdA==}

  readable-stream@3.6.2:
    resolution: {integrity: sha512-9u/sniCrY3D5WdsERHzHE4G2YCXqoG5FTHUiCC4SIbr6XcLZBY05ya9EKjYek9O5xOAwjGq+1JdGBAS7Q9ScoA==}
    engines: {node: '>= 6'}

  readdir-glob@1.1.3:
    resolution: {integrity: sha512-v05I2k7xN8zXvPD9N+z/uhXPaj0sUFCe2rcWZIpBsqxfP7xXFQ0tipAd/wjj1YxWyWtUS5IDJpOG82JKt2EAVA==}

  readdirp@3.6.0:
    resolution: {integrity: sha512-hOS089on8RduqdbhvQ5Z37A0ESjsqz6qnRcffsMU3495FuTdqSm+7bhJ29JvIOsBDEEnan5DPu9t3To9VRlMzA==}
    engines: {node: '>=8.10.0'}

  reflect-metadata@0.1.13:
    resolution: {integrity: sha512-Ts1Y/anZELhSsjMcU605fU9RE4Oi3p5ORujwbIKXfWa+0Zxs510Qrmrce5/Jowq3cHSZSJqBjypxmHarc+vEWg==}

  resolve-from@4.0.0:
    resolution: {integrity: sha512-pb/MYmXstAkysRFx8piNI1tGFNQIFA3vkE3Gq4EuA1dF6gHp/+vgZqsCGJapvy8N3Q+4o7FwvquPJcnZ7RYy4g==}
    engines: {node: '>=4'}

  resolve-pkg-maps@1.0.0:
    resolution: {integrity: sha512-seS2Tj26TBVOC2NIc2rOe2y2ZO7efxITtLZcGSOnHHNOQ7CkiUBfw0Iw2ck6xkIhPwLhKNLS8BO+hEpngQlqzw==}

  resolve@1.22.11:
    resolution: {integrity: sha512-RfqAvLnMl313r7c9oclB1HhUEAezcpLjz95wFH4LVuhk9JF/r22qmVP9AMmOU4vMX7Q8pN8jwNg/CSpdFnMjTQ==}
    engines: {node: '>= 0.4'}
    hasBin: true

  reusify@1.1.0:
    resolution: {integrity: sha512-g6QUff04oZpHs0eG5p83rFLhHeV00ug/Yf9nZM6fLeUrPguBTkTQOdpAWWspMh55TZfVQDPaN3NQJfbVRAxdIw==}
    engines: {iojs: '>=1.0.0', node: '>=0.10.0'}

  rimraf@2.7.1:
    resolution: {integrity: sha512-uWjbaKIK3T1OSVptzX7Nl6PvQ3qAGtKEtVRjRuazjfL3Bx5eI409VZSqgND+4UNnmzLVdPj9FqFJNPqBZFve4w==}
    deprecated: Rimraf versions prior to v4 are no longer supported
    hasBin: true

  rollup@4.53.2:
    resolution: {integrity: sha512-MHngMYwGJVi6Fmnk6ISmnk7JAHRNF0UkuucA0CUW3N3a4KnONPEZz+vUanQP/ZC/iY1Qkf3bwPWzyY84wEks1g==}
    engines: {node: '>=18.0.0', npm: '>=8.0.0'}
    hasBin: true

  router@2.2.0:
    resolution: {integrity: sha512-nLTrUKm2UyiL7rlhapu/Zl45FwNgkZGaCpZbIHajDYgwlJCOzLSk+cIPAnsEqV955GjILJnKbdQC1nVPz+gAYQ==}
    engines: {node: '>= 18'}

  run-parallel@1.2.0:
    resolution: {integrity: sha512-5l4VyZR86LZ/lDxZTR6jqL8AFE2S0IFLMP26AbjsLVADxHdhB/c0GUsH+y39UfCi3dzz8OlQuPmnaJOMoDHQBA==}

  safe-buffer@5.1.2:
    resolution: {integrity: sha512-Gd2UZBJDkXlY7GbJxfsE8/nvKkUEU1G38c1siN6QP6a9PT9MmHB8GnpscSmMJSoF8LOIrt8ud/wPtojys4G6+g==}

  safe-buffer@5.2.1:
    resolution: {integrity: sha512-rp3So07KcdmmKbGvgaNxQSJr7bGVSVk5S9Eq1F+ppbRo70+YeaDxkw5Dd8NPN+GD6bjnYm2VuPuCXmpuYvmCXQ==}

  safe-regex-test@1.1.0:
    resolution: {integrity: sha512-x/+Cz4YrimQxQccJf5mKEbIa1NzeCRNI5Ecl/ekmlYaampdNLPalVyIcCZNNH3MvmqBugV5TMYZXv0ljslUlaw==}
    engines: {node: '>= 0.4'}

  safer-buffer@2.1.2:
    resolution: {integrity: sha512-YZo3K82SD7Riyi0E1EQPojLz7kpepnSQI9IyPbHHg1XXXevb5dJI7tpyN2ADxGcQbHG7vcyRHk0cbwqcQriUtg==}

  saxes@5.0.1:
    resolution: {integrity: sha512-5LBh1Tls8c9xgGjw3QrMwETmTMVk0oFgvrFSvWx62llR2hcEInrKNZ2GZCCuuy2lvWrdl5jhbpeqc5hRYKFOcw==}
    engines: {node: '>=10'}

  scheduler@0.23.2:
    resolution: {integrity: sha512-UOShsPwz7NrMUqhR6t0hWjFduvOzbtv7toDH1/hIrfRNIDBnnBWd0CwJTGvTpngVlmwGCdP9/Zl/tVrDqcuYzQ==}

  semver@7.7.3:
    resolution: {integrity: sha512-SdsKMrI9TdgjdweUSR9MweHA4EJ8YxHn8DFaDisvhVlUOe4BF1tLD7GAj0lIqWVl+dPb/rExr0Btby5loQm20Q==}
    engines: {node: '>=10'}
    hasBin: true

  send@1.2.0:
    resolution: {integrity: sha512-uaW0WwXKpL9blXE2o0bRhoL2EGXIrZxQ2ZQ4mgcfoBxdFmQold+qWsD2jLrfZ0trjKL6vOw0j//eAwcALFjKSw==}
    engines: {node: '>= 18'}

  serve-static@2.2.0:
    resolution: {integrity: sha512-61g9pCh0Vnh7IutZjtLGGpTA355+OPn2TyDv/6ivP2h/AdAVX9azsoxmg2/M6nZeQZNYBEwIcsne1mJd9oQItQ==}
    engines: {node: '>= 18'}

  set-function-length@1.2.2:
    resolution: {integrity: sha512-pgRc4hJ4/sNjWCSS9AmnS40x3bNMDTknHgL5UaMBTMyJnU90EgWh1Rz+MC9eFu4BuN/UwZjKQuY/1v3rM7HMfg==}
    engines: {node: '>= 0.4'}

  setimmediate@1.0.5:
    resolution: {integrity: sha512-MATJdZp8sLqDl/68LfQmbP8zKPLQNV6BIZoIgrscFDQ+RsvK/BxeDQOgyxKKoh0y/8h3BqVFnCqQ/gd+reiIXA==}

  setprototypeof@1.2.0:
    resolution: {integrity: sha512-E5LDX7Wrp85Kil5bhZv46j8jOeboKq5JMmYM3gVGdGH8xFpPWXUMsNrlODCrkoxMEeNi/XZIwuRvY4XNwYMJpw==}

  shebang-command@2.0.0:
    resolution: {integrity: sha512-kHxr2zZpYtdmrN1qDjrrX/Z1rR1kG8Dx+gkpK1G4eXmvXswmcE1hTWBWYUzlraYw1/yZp6YuDY77YtvbN0dmDA==}
    engines: {node: '>=8'}

  shebang-regex@3.0.0:
    resolution: {integrity: sha512-7++dFhtcx3353uBaq8DDR4NuxBetBzC7ZQOhmTQInHEd6bSrXdiEyzCvG07Z44UYdLShWUyXt5M/yhz8ekcb1A==}
    engines: {node: '>=8'}

  side-channel-list@1.0.0:
    resolution: {integrity: sha512-FCLHtRD/gnpCiCHEiJLOwdmFP+wzCmDEkc9y7NsYxeF4u7Btsn1ZuwgwJGxImImHicJArLP4R0yX4c2KCrMrTA==}
    engines: {node: '>= 0.4'}

  side-channel-map@1.0.1:
    resolution: {integrity: sha512-VCjCNfgMsby3tTdo02nbjtM/ewra6jPHmpThenkTYh8pG9ucZ/1P8So4u4FGBek/BjpOVsDCMoLA/iuBKIFXRA==}
    engines: {node: '>= 0.4'}

  side-channel-weakmap@1.0.2:
    resolution: {integrity: sha512-WPS/HvHQTYnHisLo9McqBHOJk2FkHO/tlpvldyrnem4aeQp4hai3gythswg6p01oSoTl58rcpiFAjF2br2Ak2A==}
    engines: {node: '>= 0.4'}

  side-channel@1.1.0:
    resolution: {integrity: sha512-ZX99e6tRweoUXqR+VBrslhda51Nh5MTQwou5tnUDgbtyM0dBgmhEDtWGP/xbKn6hqfPRHujUNwz5fy/wbbhnpw==}
    engines: {node: '>= 0.4'}

  signal-exit@4.1.0:
    resolution: {integrity: sha512-bzyZ1e88w9O1iNJbKnOlvYTrWPDl46O1bG0D3XInv+9tkPrxrN8jUUTiFlDkkmKWgn1M6CfIA13SuGqOa9Korw==}
    engines: {node: '>=14'}

  source-map-js@1.2.1:
    resolution: {integrity: sha512-UXWMKhLOwVKb728IUtQPXxfYU+usdybtUrK/8uGE8CQMvrhOpwvzDBwj0QhSL7MQc7vIsISBG8VQ8+IDQxpfQA==}
    engines: {node: '>=0.10.0'}

  source-map-support@0.5.21:
    resolution: {integrity: sha512-uBHU3L3czsIyYXKX88fdrGovxdSCoTGDRZ6SYXtSRxLZUzHg5P/66Ht6uoUlHu9EZod+inXhKo3qQgwXUT/y1w==}

  source-map@0.6.1:
    resolution: {integrity: sha512-UjgapumWlbMhkBgzT7Ykc5YXUT46F0iKu8SGXq0bcwP5dz/h0Plj6enJqjz1Zbq2l5WaqYnrVbwWOWMyF3F47g==}
    engines: {node: '>=0.10.0'}

  statuses@2.0.1:
    resolution: {integrity: sha512-RwNA9Z/7PrK06rYLIzFMlaF+l73iwpzsqRIFgbMLbTcLD6cOao82TaWefPXQvB2fOC4AjuYSEndS7N/mTCbkdQ==}
    engines: {node: '>= 0.8'}

  statuses@2.0.2:
    resolution: {integrity: sha512-DvEy55V3DB7uknRo+4iOGT5fP1slR8wQohVdknigZPMpMstaKJQWhwiYBACJE3Ul2pTnATihhBYnRhZQHGBiRw==}
    engines: {node: '>= 0.8'}

  streamsearch@1.1.0:
    resolution: {integrity: sha512-Mcc5wHehp9aXz1ax6bZUyY5afg9u2rv5cqQI3mRrYkGC8rW2hM02jWuwjtL++LS5qinSyhj2QfLyNsuc+VsExg==}
    engines: {node: '>=10.0.0'}

  string-template@1.0.0:
    resolution: {integrity: sha512-SLqR3GBUXuoPP5MmYtD7ompvXiG87QjT6lzOszyXjTM86Uu7At7vNnt2xgyTLq5o9T4IxTYFyGxcULqpsmsfdg==}

  string-width@4.2.3:
    resolution: {integrity: sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==}
    engines: {node: '>=8'}

  string-width@5.1.2:
    resolution: {integrity: sha512-HnLOCR3vjcY8beoNLtcjZ5/nxn2afmME6lhrDrebokqMap+XbeW8n9TXpPDOqdGK5qcI3oT0GKTW6wC7EMiVqA==}
    engines: {node: '>=12'}

  string_decoder@1.1.1:
    resolution: {integrity: sha512-n/ShnvDi6FHbbVfviro+WojiFzv+s8MPMHBczVePfUpDJLwoLT0ht1l4YwBCbi8pJAveEEdnkHyPyTP/mzRfwg==}

  string_decoder@1.3.0:
    resolution: {integrity: sha512-hkRX8U1WjJFd8LsDJ2yQ/wWWxaopEsABU1XfkM8A+j0+85JAGppt16cr1Whg6KIbb4okU6Mql6BOj+uup/wKeA==}

  stringz@2.1.0:
    resolution: {integrity: sha512-KlywLT+MZ+v0IRepfMxRtnSvDCMc3nR1qqCs3m/qIbSOWkNZYT8XHQA31rS3TnKp0c5xjZu3M4GY/2aRKSi/6A==}

  strip-ansi@6.0.1:
    resolution: {integrity: sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==}
    engines: {node: '>=8'}

  strip-ansi@7.1.2:
    resolution: {integrity: sha512-gmBGslpoQJtgnMAvOVqGZpEz9dyoKTCzy2nfz/n8aIFhN/jCE/rCmcxabB6jOOHV+0WNnylOxaxBQPSvcWklhA==}
    engines: {node: '>=12'}

  strip-json-comments@3.1.1:
    resolution: {integrity: sha512-6fPc+R4ihwqP6N/aIv2f1gMH8lOVtWQHoqC4yK6oSDVVocumAsfCqjkXnqiYMhmMwS/mEHLp7Vehlt3ql6lEig==}
    engines: {node: '>=8'}

  sucrase@3.35.0:
    resolution: {integrity: sha512-8EbVDiu9iN/nESwxeSxDKe0dunta1GOlHufmSSXxMD2z2/tMZpDMpvXQGsc+ajGo8y2uYUmixaSRUc/QPoQ0GA==}
    engines: {node: '>=16 || 14 >=14.17'}
    hasBin: true

  supports-color@7.2.0:
    resolution: {integrity: sha512-qpCAvRl9stuOHveKsn7HncJRvv501qIacKzQlO/+Lwxc9+0q2wLyv4Dfvt80/DPn2pqOBsJdDiogXGR9+OvwRw==}
    engines: {node: '>=8'}

  supports-preserve-symlinks-flag@1.0.0:
    resolution: {integrity: sha512-ot0WnXS9fgdkgIcePe6RHNk1WA8+muPa6cSjeR3V8K27q9BB1rTE3R1p7Hv0z1ZyAc8s6Vvv8DIyWf681MAt0w==}
    engines: {node: '>= 0.4'}

  tailwindcss@3.4.17:
    resolution: {integrity: sha512-w33E2aCvSDP0tW9RZuNXadXlkHXqFzSkQew/aIa2i/Sj8fThxwovwlXHSPXTbAHwEIhBFXAedUhP2tueAKP8Og==}
    engines: {node: '>=14.0.0'}
    hasBin: true

  tar-stream@2.2.0:
    resolution: {integrity: sha512-ujeqbceABgwMZxEJnk2HDY2DlnUZ+9oEcb1KzTVfYHio0UE6dG71n60d8D2I4qNvleWrrXpmjpt7vZeF1LnMZQ==}
    engines: {node: '>=6'}

  text-table@0.2.0:
    resolution: {integrity: sha512-N+8UisAXDGk8PFXP4HAzVR9nbfmVJ3zYLAWiTIoqC5v5isinhr+r5uaO8+7r3BMfuNIufIsA7RdpVgacC2cSpw==}

  thenify-all@1.6.0:
    resolution: {integrity: sha512-RNxQH/qI8/t3thXJDwcstUO4zeqo64+Uy/+sNVRBx4Xn2OX+OZ9oP+iJnNFqplFra2ZUVeKCSa2oVWi3T4uVmA==}
    engines: {node: '>=0.8'}

  thenify@3.3.1:
    resolution: {integrity: sha512-RVZSIV5IG10Hk3enotrhvz0T9em6cyHBLkH/YAZuKqd8hRkKhSfCGIcP2KUY0EPxndzANBmNllzWPwak+bheSw==}

  tinyglobby@0.2.15:
    resolution: {integrity: sha512-j2Zq4NyQYG5XMST4cbs02Ak8iJUdxRM0XI5QyxXuZOzKOINmWurp3smXu3y5wDcJrptwpSjgXHzIQxR0omXljQ==}
    engines: {node: '>=12.0.0'}

  tmp@0.2.5:
    resolution: {integrity: sha512-voyz6MApa1rQGUxT3E+BK7/ROe8itEx7vD8/HEvt4xwXucvQ5G5oeEiHkmHZJuBO21RpOf+YYm9MOivj709jow==}
    engines: {node: '>=14.14'}

  to-regex-range@5.0.1:
    resolution: {integrity: sha512-65P7iz6X5yEr1cwcgvQxbbIw7Uk3gOy5dIdtZ4rDveLqhrdJP+Li/Hx6tyK0NEb+2GCyneCMJiGqrADCSNk8sQ==}
    engines: {node: '>=8.0'}

  toidentifier@1.0.1:
    resolution: {integrity: sha512-o5sSPKEkg/DIQNmH43V0/uerLrpzVedkUh8tGNvaeXpfpuwjKenlSox/2O/BTlZUtEe+JG7s5YhEz608PlAHRA==}
    engines: {node: '>=0.6'}

  traverse@0.3.9:
    resolution: {integrity: sha512-iawgk0hLP3SxGKDfnDJf8wTz4p2qImnyihM5Hh/sGvQ3K37dPi/w8sRhdNIxYA1TwFwc5mDhIJq+O0RsvXBKdQ==}

  ts-api-utils@1.4.3:
    resolution: {integrity: sha512-i3eMG77UTMD0hZhgRS562pv83RC6ukSAC2GMNWc+9dieh/+jDM5u5YG+NHX6VNDRHQcHwmsTHctP9LhbC3WxVw==}
    engines: {node: '>=16'}
    peerDependencies:
      typescript: '>=4.2.0'

  ts-interface-checker@0.1.13:
    resolution: {integrity: sha512-Y/arvbn+rrz3JCKl9C4kVNfTfSm2/mEp5FSz5EsZSANGPSlQrpRI5M4PKF+mJnE52jOO90PnPSc3Ur3bTQw0gA==}

  tslib@2.5.0:
    resolution: {integrity: sha512-336iVw3rtn2BUK7ORdIAHTyxHGRIHVReokCR3XjbckJMK7ms8FysBfhLR8IXnAgy7T0PTPNBWKiH514FOW/WSg==}

  tslib@2.8.1:
    resolution: {integrity: sha512-oJFu94HQb+KVduSUQL7wnpmqnfmLsOA/nAh6b6EH0wCEoK0/mPeXU6c3wKDV83MkOuHPRHtSXKKU99IBazS/2w==}

  tsx@4.20.6:
    resolution: {integrity: sha512-ytQKuwgmrrkDTFP4LjR0ToE2nqgy886GpvRSpU0JAnrdBYppuY5rLkRUYPU1yCryb24SsKBTL/hlDQAEFVwtZg==}
    engines: {node: '>=18.0.0'}
    hasBin: true

  type-check@0.3.2:
    resolution: {integrity: sha512-ZCmOJdvOWDBYJlzAoFkC+Q0+bUyEOS1ltgp1MGU03fqHG+dbi9tBFU2Rd9QKiDZFAYrhPh2JUf7rZRIuHRKtOg==}
    engines: {node: '>= 0.8.0'}

  type-check@0.4.0:
    resolution: {integrity: sha512-XleUoc9uwGXqjWwXaUTZAmzMcFZ5858QA2vvx1Ur5xIcixXIP+8LnFDgRplU30us6teqdlskFfu+ae4K79Ooew==}
    engines: {node: '>= 0.8.0'}

  type-is@1.6.18:
    resolution: {integrity: sha512-TkRKr9sUTxEH8MdfuCSP7VizJyzRNMjj2J2do2Jr3Kym598JVdEksuzPQCnlFPW4ky9Q+iA+ma9BGm06XQBy8g==}
    engines: {node: '>= 0.6'}

  type-is@2.0.1:
    resolution: {integrity: sha512-OZs6gsjF4vMp32qrCbiVSkrFmXtG/AZhY3t0iAMrMBiAZyV9oALtXO8hsrHbMXF9x6L3grlFuwW2oAz7cav+Gw==}
    engines: {node: '>= 0.6'}

  typedarray@0.0.6:
    resolution: {integrity: sha512-/aCDEGatGvZ2BIk+HmLf4ifCJFwvKFNb9/JeZPMulfgFracn9QFcAf5GO8B/mweUjSoblS5In0cWhqpfs/5PQA==}

  typescript-eslint@8.3.0:
    resolution: {integrity: sha512-EvWjwWLwwKDIJuBjk2I6UkV8KEQcwZ0VM10nR1rIunRDIP67QJTZAHBXTX0HW/oI1H10YESF8yWie8fRQxjvFA==}
    engines: {node: ^18.18.0 || ^20.9.0 || >=21.1.0}
    peerDependencies:
      typescript: '*'
    peerDependenciesMeta:
      typescript:
        optional: true

  typescript@5.5.3:
    resolution: {integrity: sha512-/hreyEujaB0w76zKo6717l3L0o/qEUtRgdvUBvlkhoWeOVMjMuHNHk0BRBzikzuGDqNmPQbg5ifMEqsHLiIUcQ==}
    engines: {node: '>=14.17'}
    hasBin: true

  ufo@1.6.1:
    resolution: {integrity: sha512-9a4/uxlTWJ4+a5i0ooc1rU7C7YOw3wT+UGqdeNNHWnOF9qcMBgLRS+4IYUqbczewFx4mLEig6gawh7X6mFlEkA==}

  undici-types@7.16.0:
    resolution: {integrity: sha512-Zz+aZWSj8LE6zoxD+xrjh4VfkIG8Ya6LvYkZqtUQGJPZjYl53ypCaUwWqo7eI0x66KBGeRo+mlBEkMSeSZ38Nw==}

  unpipe@1.0.0:
    resolution: {integrity: sha512-pjy2bYhSsufwWlKwPc+l3cN7+wuJlK6uz0YdJEOlQDbl6jo/YlPi4mb8agUkVC8BF7V8NuzeyPNqRksA3hztKQ==}
    engines: {node: '>= 0.8'}

  unzipper@0.10.14:
    resolution: {integrity: sha512-ti4wZj+0bQTiX2KmKWuwj7lhV+2n//uXEotUmGuQqrbVZSEGFMbI68+c6JCQ8aAmUWYvtHEz2A8K6wXvueR/6g==}

  update-browserslist-db@1.1.4:
    resolution: {integrity: sha512-q0SPT4xyU84saUX+tomz1WLkxUbuaJnR1xWt17M7fJtEJigJeWUNGUqrauFXsHnqev9y9JTRGwk13tFBuKby4A==}
    hasBin: true
    peerDependencies:
      browserslist: '>= 4.21.0'

  uri-js@4.4.1:
    resolution: {integrity: sha512-7rKUyy33Q1yc98pQ1DAmLtwX109F7TIfWlW1Ydo8Wl1ii1SeHieeh0HHfPeL2fMXK6z0s8ecKs9frCuLJvndBg==}

  util-deprecate@1.0.2:
    resolution: {integrity: sha512-EPD5q1uXyFxJpCrLnCc1nHnq3gOa6DZBocAIiI2TaSCA7VCJ1UJDMagCzIkXNsUYfD1daK//LTEQ8xiIbrHtcw==}

  util@0.12.5:
    resolution: {integrity: sha512-kZf/K6hEIrWHI6XqOFUiiMa+79wE/D8Q+NCNAWclkyg3b4d2k7s0QGepNjiABc+aR3N1PAyHL7p6UcLY6LmrnA==}

  uuid@11.1.0:
    resolution: {integrity: sha512-0/A9rDy9P7cJ+8w1c9WD9V//9Wj15Ce2MPz8Ri6032usz+NfePxx5AcN3bN+r6ZL6jEo066/yNYB3tn4pQEx+A==}
    hasBin: true

  uuid@8.3.2:
    resolution: {integrity: sha512-+NYs2QeMWy+GWFOEm9xnn6HCDp0l7QBD7ml8zLUmJ+93Q5NF0NocErnwkTkXVFNiX3/fpC6afS8Dhb/gz7R7eg==}
    hasBin: true

  validator@13.15.23:
    resolution: {integrity: sha512-4yoz1kEWqUjzi5zsPbAS/903QXSYp0UOtHsPpp7p9rHAw/W+dkInskAE386Fat3oKRROwO98d9ZB0G4cObgUyw==}
    engines: {node: '>= 0.10'}

  vary@1.1.2:
    resolution: {integrity: sha512-BNGbWLfd0eUPabhkXUVm0j8uuvREyTh5ovRa/dyow/BqAbZJyC+5fU+IzQOzmAKzYqYRAISoRhdQr3eIZ/PXqg==}
    engines: {node: '>= 0.8'}

  vite-plugin-javascript-obfuscator@3.1.0:
    resolution: {integrity: sha512-sf4JFlG1iUPl7bLXHGOy+bKWOQUFyXzJFWa+n2S2xMMvyfM+V9R40HhpZoIF1eAjifArM1SF7fbSFIaTuUIbPA==}

  vite-plugin-obfuscator@1.0.5:
    resolution: {integrity: sha512-5kflM0I3dIpFYIRmPHtdr5Y54Zrtzrhzm6eQMdIh8kcq3Mde/Fr8E3wR4Z2kdtZYSP3DjqeR4LfXRAIsNBGoFg==}

  vite@7.2.2:
    resolution: {integrity: sha512-BxAKBWmIbrDgrokdGZH1IgkIk/5mMHDreLDmCJ0qpyJaAteP8NvMhkwr/ZCQNqNH97bw/dANTE9PDzqwJghfMQ==}
    engines: {node: ^20.19.0 || >=22.12.0}
    hasBin: true
    peerDependencies:
      '@types/node': ^20.19.0 || >=22.12.0
      jiti: '>=1.21.0'
      less: ^4.0.0
      lightningcss: ^1.21.0
      sass: ^1.70.0
      sass-embedded: ^1.70.0
      stylus: '>=0.54.8'
      sugarss: ^5.0.0
      terser: ^5.16.0
      tsx: ^4.8.1
      yaml: ^2.4.2
    peerDependenciesMeta:
      '@types/node':
        optional: true
      jiti:
        optional: true
      less:
        optional: true
      lightningcss:
        optional: true
      sass:
        optional: true
      sass-embedded:
        optional: true
      stylus:
        optional: true
      sugarss:
        optional: true
      terser:
        optional: true
      tsx:
        optional: true
      yaml:
        optional: true

  which-typed-array@1.1.19:
    resolution: {integrity: sha512-rEvr90Bck4WZt9HHFC4DJMsjvu7x+r6bImz0/BrbWb7A2djJ8hnZMrWnHo9F8ssv0OMErasDhftrfROTyqSDrw==}
    engines: {node: '>= 0.4'}

  which@2.0.2:
    resolution: {integrity: sha512-BLI3Tl1TW3Pvl70l3yq3Y64i+awpwXqsGBYWkkqMtnbXgrMD+yj7rhW0kuEDxzJaYXGjEW5ogapKNMEKNMjibA==}
    engines: {node: '>= 8'}
    hasBin: true

  word-wrap@1.2.5:
    resolution: {integrity: sha512-BN22B5eaMMI9UMtjrGd5g5eCYPpCPDUy0FJXbYsaT5zYxjFOckS53SQDE3pWkVoWpHXVb3BrYcEN4Twa55B5cA==}
    engines: {node: '>=0.10.0'}

  wrap-ansi@7.0.0:
    resolution: {integrity: sha512-YVGIj2kamLSTxw6NsZjoBxfSwsn0ycdesmc4p+Q21c5zPuZ1pl+NfxVdxPtdHvmNVOQ6XSYG4AUtyt/Fi7D16Q==}
    engines: {node: '>=10'}

  wrap-ansi@8.1.0:
    resolution: {integrity: sha512-si7QWI6zUMq56bESFvagtmzMdGOtoxfR+Sez11Mobfc7tm+VkUckk9bW2UeffTGVUbOksxmSw0AA2gs8g71NCQ==}
    engines: {node: '>=12'}

  wrappy@1.0.2:
    resolution: {integrity: sha512-l4Sp/DRseor9wL6EvV2+TuQn63dMkPjZ/sp9XkghTEbV9KlPS1xUsZ3u7/IQO4wxtcFB4bgpQPRcR3QCvezPcQ==}

  ws@8.18.3:
    resolution: {integrity: sha512-PEIGCY5tSlUt50cqyMXfCzX+oOPqN0vuGqWzbcJ2xvnkzkq46oOpz7dQaTDBdfICb4N14+GARUDw2XV2N4tvzg==}
    engines: {node: '>=10.0.0'}
    peerDependencies:
      bufferutil: ^4.0.1
      utf-8-validate: '>=5.0.2'
    peerDependenciesMeta:
      bufferutil:
        optional: true
      utf-8-validate:
        optional: true

  xmlchars@2.2.0:
    resolution: {integrity: sha512-JZnDKK8B0RCDw84FNdDAIpZK+JuJw+s7Lz8nksI7SIuU3UXJJslUthsi+uWBUYOwPFwW7W7PRLRfUKpxjtjFCw==}

  xtend@4.0.2:
    resolution: {integrity: sha512-LKYU1iAXJXUgAXn9URjiu+MWhyUXHsvfp7mcuYm9dSUKK0/CjtrUwFAxD82/mCWbtLsGjFIad0wIsod4zrTAEQ==}
    engines: {node: '>=0.4'}

  yaml@2.8.1:
    resolution: {integrity: sha512-lcYcMxX2PO9XMGvAJkJ3OsNMw+/7FKes7/hgerGUYWIoWu5j/+YQqcZr5JnPZWzOsEBgMbSbiSTn/dv/69Mkpw==}
    engines: {node: '>= 14.6'}
    hasBin: true

  yocto-queue@0.1.0:
    resolution: {integrity: sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q==}
    engines: {node: '>=10'}

  zip-stream@4.1.1:
    resolution: {integrity: sha512-9qv4rlDiopXg4E69k+vMHjNN63YFMe9sZMrdlvKnCjlCRWeCBswPPMPUfx+ipsAWq1LXHe70RcbaHdJJpS6hyQ==}
    engines: {node: '>= 10'}

snapshots:

  '@alloc/quick-lru@5.2.0': {}

  '@esbuild/aix-ppc64@0.25.12':
    optional: true

  '@esbuild/android-arm64@0.25.12':
    optional: true

  '@esbuild/android-arm@0.25.12':
    optional: true

  '@esbuild/android-x64@0.25.12':
    optional: true

  '@esbuild/darwin-arm64@0.25.12':
    optional: true

  '@esbuild/darwin-x64@0.25.12':
    optional: true

  '@esbuild/freebsd-arm64@0.25.12':
    optional: true

  '@esbuild/freebsd-x64@0.25.12':
    optional: true

  '@esbuild/linux-arm64@0.25.12':
    optional: true

  '@esbuild/linux-arm@0.25.12':
    optional: true

  '@esbuild/linux-ia32@0.25.12':
    optional: true

  '@esbuild/linux-loong64@0.25.12':
    optional: true

  '@esbuild/linux-mips64el@0.25.12':
    optional: true

  '@esbuild/linux-ppc64@0.25.12':
    optional: true

  '@esbuild/linux-riscv64@0.25.12':
    optional: true

  '@esbuild/linux-s390x@0.25.12':
    optional: true

  '@esbuild/linux-x64@0.25.12':
    optional: true

  '@esbuild/netbsd-arm64@0.25.12':
    optional: true

  '@esbuild/netbsd-x64@0.25.12':
    optional: true

  '@esbuild/openbsd-arm64@0.25.12':
    optional: true

  '@esbuild/openbsd-x64@0.25.12':
    optional: true

  '@esbuild/openharmony-arm64@0.25.12':
    optional: true

  '@esbuild/sunos-x64@0.25.12':
    optional: true

  '@esbuild/win32-arm64@0.25.12':
    optional: true

  '@esbuild/win32-ia32@0.25.12':
    optional: true

  '@esbuild/win32-x64@0.25.12':
    optional: true

  '@eslint-community/eslint-utils@4.9.0(eslint@9.9.1(jiti@1.21.7))':
    dependencies:
      eslint: 9.9.1(jiti@1.21.7)
      eslint-visitor-keys: 3.4.3

  '@eslint-community/regexpp@4.12.2': {}

  '@eslint/config-array@0.18.0':
    dependencies:
      '@eslint/object-schema': 2.1.7
      debug: 4.4.3
      minimatch: 3.1.2
    transitivePeerDependencies:
      - supports-color

  '@eslint/eslintrc@3.3.1':
    dependencies:
      ajv: 6.12.6
      debug: 4.4.3
      espree: 10.4.0
      globals: 14.0.0
      ignore: 5.3.2
      import-fresh: 3.3.1
      js-yaml: 4.1.1
      minimatch: 3.1.2
      strip-json-comments: 3.1.1
    transitivePeerDependencies:
      - supports-color

  '@eslint/js@9.9.1': {}

  '@eslint/object-schema@2.1.7': {}

  '@fast-csv/format@4.3.5':
    dependencies:
      '@types/node': 14.18.63
      lodash.escaperegexp: 4.1.2
      lodash.isboolean: 3.0.3
      lodash.isequal: 4.5.0
      lodash.isfunction: 3.0.9
      lodash.isnil: 4.0.0

  '@fast-csv/parse@4.3.6':
    dependencies:
      '@types/node': 14.18.63
      lodash.escaperegexp: 4.1.2
      lodash.groupby: 4.6.0
      lodash.isfunction: 3.0.9
      lodash.isnil: 4.0.0
      lodash.isundefined: 3.0.1
      lodash.uniq: 4.5.0

  '@humanwhocodes/module-importer@1.0.1': {}

  '@humanwhocodes/retry@0.3.1': {}

  '@isaacs/cliui@8.0.2':
    dependencies:
      string-width: 5.1.2
      string-width-cjs: string-width@4.2.3
      strip-ansi: 7.1.2
      strip-ansi-cjs: strip-ansi@6.0.1
      wrap-ansi: 8.1.0
      wrap-ansi-cjs: wrap-ansi@7.0.0

  '@javascript-obfuscator/escodegen@2.3.0':
    dependencies:
      '@javascript-obfuscator/estraverse': 5.4.0
      esprima: 4.0.1
      esutils: 2.0.3
      optionator: 0.8.3
    optionalDependencies:
      source-map: 0.6.1

  '@javascript-obfuscator/estraverse@5.4.0': {}

  '@jridgewell/gen-mapping@0.3.13':
    dependencies:
      '@jridgewell/sourcemap-codec': 1.5.5
      '@jridgewell/trace-mapping': 0.3.31

  '@jridgewell/resolve-uri@3.1.2': {}

  '@jridgewell/sourcemap-codec@1.5.5': {}

  '@jridgewell/trace-mapping@0.3.31':
    dependencies:
      '@jridgewell/resolve-uri': 3.1.2
      '@jridgewell/sourcemap-codec': 1.5.5

  '@lumi.new/sdk@0.2.1':
    dependencies:
      crypto-js: 4.2.0
      object-hash: 3.0.0
      ofetch: 1.5.1
      uuid: 11.1.0

  '@nodelib/fs.scandir@2.1.5':
    dependencies:
      '@nodelib/fs.stat': 2.0.5
      run-parallel: 1.2.0

  '@nodelib/fs.stat@2.0.5': {}

  '@nodelib/fs.walk@1.2.8':
    dependencies:
      '@nodelib/fs.scandir': 2.1.5
      fastq: 1.19.1

  '@pkgjs/parseargs@0.11.0':
    optional: true

  '@remix-run/router@1.19.0': {}

  '@rolldown/pluginutils@1.0.0-beta.27': {}

  '@rollup/rollup-android-arm-eabi@4.53.2':
    optional: true

  '@rollup/rollup-android-arm64@4.53.2':
    optional: true

  '@rollup/rollup-darwin-arm64@4.53.2':
    optional: true

  '@rollup/rollup-darwin-x64@4.53.2':
    optional: true

  '@rollup/rollup-freebsd-arm64@4.53.2':
    optional: true

  '@rollup/rollup-freebsd-x64@4.53.2':
    optional: true

  '@rollup/rollup-linux-arm-gnueabihf@4.53.2':
    optional: true

  '@rollup/rollup-linux-arm-musleabihf@4.53.2':
    optional: true

  '@rollup/rollup-linux-arm64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-arm64-musl@4.53.2':
    optional: true

  '@rollup/rollup-linux-loong64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-ppc64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-riscv64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-riscv64-musl@4.53.2':
    optional: true

  '@rollup/rollup-linux-s390x-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-x64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-linux-x64-musl@4.53.2':
    optional: true

  '@rollup/rollup-openharmony-arm64@4.53.2':
    optional: true

  '@rollup/rollup-win32-arm64-msvc@4.53.2':
    optional: true

  '@rollup/rollup-win32-ia32-msvc@4.53.2':
    optional: true

  '@rollup/rollup-win32-x64-gnu@4.53.2':
    optional: true

  '@rollup/rollup-win32-x64-msvc@4.53.2':
    optional: true

  '@supabase/auth-js@2.81.1':
    dependencies:
      tslib: 2.8.1

  '@supabase/functions-js@2.81.1':
    dependencies:
      tslib: 2.8.1

  '@supabase/postgrest-js@2.81.1':
    dependencies:
      tslib: 2.8.1

  '@supabase/realtime-js@2.81.1':
    dependencies:
      '@types/phoenix': 1.6.6
      '@types/ws': 8.18.1
      tslib: 2.8.1
      ws: 8.18.3
    transitivePeerDependencies:
      - bufferutil
      - utf-8-validate

  '@supabase/storage-js@2.81.1':
    dependencies:
      tslib: 2.8.1

  '@supabase/supabase-js@2.81.1':
    dependencies:
      '@supabase/auth-js': 2.81.1
      '@supabase/functions-js': 2.81.1
      '@supabase/postgrest-js': 2.81.1
      '@supabase/realtime-js': 2.81.1
      '@supabase/storage-js': 2.81.1
    transitivePeerDependencies:
      - bufferutil
      - utf-8-validate

  '@swc/core-darwin-arm64@1.13.3':
    optional: true

  '@swc/core-darwin-x64@1.13.3':
    optional: true

  '@swc/core-linux-arm-gnueabihf@1.13.3':
    optional: true

  '@swc/core-linux-arm64-gnu@1.13.3':
    optional: true

  '@swc/core-linux-arm64-musl@1.13.3':
    optional: true

  '@swc/core-linux-x64-gnu@1.13.3':
    optional: true

  '@swc/core-linux-x64-musl@1.13.3':
    optional: true

  '@swc/core-win32-arm64-msvc@1.13.3':
    optional: true

  '@swc/core-win32-ia32-msvc@1.13.3':
    optional: true

  '@swc/core-win32-x64-msvc@1.13.3':
    optional: true

  '@swc/core@1.13.3':
    dependencies:
      '@swc/counter': 0.1.3
      '@swc/types': 0.1.25
    optionalDependencies:
      '@swc/core-darwin-arm64': 1.13.3
      '@swc/core-darwin-x64': 1.13.3
      '@swc/core-linux-arm-gnueabihf': 1.13.3
      '@swc/core-linux-arm64-gnu': 1.13.3
      '@swc/core-linux-arm64-musl': 1.13.3
      '@swc/core-linux-x64-gnu': 1.13.3
      '@swc/core-linux-x64-musl': 1.13.3
      '@swc/core-win32-arm64-msvc': 1.13.3
      '@swc/core-win32-ia32-msvc': 1.13.3
      '@swc/core-win32-x64-msvc': 1.13.3

  '@swc/counter@0.1.3': {}

  '@swc/types@0.1.25':
    dependencies:
      '@swc/counter': 0.1.3

  '@types/body-parser@1.19.6':
    dependencies:
      '@types/connect': 3.4.38
      '@types/node': 24.10.1

  '@types/connect@3.4.38':
    dependencies:
      '@types/node': 24.10.1

  '@types/cors@2.8.19':
    dependencies:
      '@types/node': 24.10.1

  '@types/estree@1.0.8': {}

  '@types/express-serve-static-core@5.1.0':
    dependencies:
      '@types/node': 24.10.1
      '@types/qs': 6.14.0
      '@types/range-parser': 1.2.7
      '@types/send': 1.2.1

  '@types/express@5.0.5':
    dependencies:
      '@types/body-parser': 1.19.6
      '@types/express-serve-static-core': 5.1.0
      '@types/serve-static': 1.15.10

  '@types/http-errors@2.0.5': {}

  '@types/mime@1.3.5': {}

  '@types/minimatch@3.0.5': {}

  '@types/multer@2.0.0':
    dependencies:
      '@types/express': 5.0.5

  '@types/node@14.18.63': {}

  '@types/node@24.10.1':
    dependencies:
      undici-types: 7.16.0

  '@types/papaparse@5.5.0':
    dependencies:
      '@types/node': 24.10.1

  '@types/phoenix@1.6.6': {}

  '@types/prop-types@15.7.15': {}

  '@types/qs@6.14.0': {}

  '@types/range-parser@1.2.7': {}

  '@types/react-dom@18.3.0':
    dependencies:
      '@types/react': 18.3.5

  '@types/react@18.3.5':
    dependencies:
      '@types/prop-types': 15.7.15
      csstype: 3.2.1

  '@types/send@0.17.6':
    dependencies:
      '@types/mime': 1.3.5
      '@types/node': 24.10.1

  '@types/send@1.2.1':
    dependencies:
      '@types/node': 24.10.1

  '@types/serve-static@1.15.10':
    dependencies:
      '@types/http-errors': 2.0.5
      '@types/node': 24.10.1
      '@types/send': 0.17.6

  '@types/validator@13.15.9': {}

  '@types/ws@8.18.1':
    dependencies:
      '@types/node': 24.10.1

  '@typescript-eslint/eslint-plugin@8.3.0(@typescript-eslint/parser@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3))(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)':
    dependencies:
      '@eslint-community/regexpp': 4.12.2
      '@typescript-eslint/parser': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      '@typescript-eslint/scope-manager': 8.3.0
      '@typescript-eslint/type-utils': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      '@typescript-eslint/utils': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      '@typescript-eslint/visitor-keys': 8.3.0
      eslint: 9.9.1(jiti@1.21.7)
      graphemer: 1.4.0
      ignore: 5.3.2
      natural-compare: 1.4.0
      ts-api-utils: 1.4.3(typescript@5.5.3)
    optionalDependencies:
      typescript: 5.5.3
    transitivePeerDependencies:
      - supports-color

  '@typescript-eslint/parser@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)':
    dependencies:
      '@typescript-eslint/scope-manager': 8.3.0
      '@typescript-eslint/types': 8.3.0
      '@typescript-eslint/typescript-estree': 8.3.0(typescript@5.5.3)
      '@typescript-eslint/visitor-keys': 8.3.0
      debug: 4.4.3
      eslint: 9.9.1(jiti@1.21.7)
    optionalDependencies:
      typescript: 5.5.3
    transitivePeerDependencies:
      - supports-color

  '@typescript-eslint/scope-manager@8.3.0':
    dependencies:
      '@typescript-eslint/types': 8.3.0
      '@typescript-eslint/visitor-keys': 8.3.0

  '@typescript-eslint/type-utils@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)':
    dependencies:
      '@typescript-eslint/typescript-estree': 8.3.0(typescript@5.5.3)
      '@typescript-eslint/utils': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      debug: 4.4.3
      ts-api-utils: 1.4.3(typescript@5.5.3)
    optionalDependencies:
      typescript: 5.5.3
    transitivePeerDependencies:
      - eslint
      - supports-color

  '@typescript-eslint/types@8.3.0': {}

  '@typescript-eslint/typescript-estree@8.3.0(typescript@5.5.3)':
    dependencies:
      '@typescript-eslint/types': 8.3.0
      '@typescript-eslint/visitor-keys': 8.3.0
      debug: 4.4.3
      fast-glob: 3.3.3
      is-glob: 4.0.3
      minimatch: 9.0.5
      semver: 7.7.3
      ts-api-utils: 1.4.3(typescript@5.5.3)
    optionalDependencies:
      typescript: 5.5.3
    transitivePeerDependencies:
      - supports-color

  '@typescript-eslint/utils@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)':
    dependencies:
      '@eslint-community/eslint-utils': 4.9.0(eslint@9.9.1(jiti@1.21.7))
      '@typescript-eslint/scope-manager': 8.3.0
      '@typescript-eslint/types': 8.3.0
      '@typescript-eslint/typescript-estree': 8.3.0(typescript@5.5.3)
      eslint: 9.9.1(jiti@1.21.7)
    transitivePeerDependencies:
      - supports-color
      - typescript

  '@typescript-eslint/visitor-keys@8.3.0':
    dependencies:
      '@typescript-eslint/types': 8.3.0
      eslint-visitor-keys: 3.4.3

  '@vitejs/plugin-react-swc@3.11.0(vite@7.2.2(@types/node@24.10.1)(jiti@1.21.7)(tsx@4.20.6)(yaml@2.8.1))':
    dependencies:
      '@rolldown/pluginutils': 1.0.0-beta.27
      '@swc/core': 1.13.3
      vite: 7.2.2(@types/node@24.10.1)(jiti@1.21.7)(tsx@4.20.6)(yaml@2.8.1)
    transitivePeerDependencies:
      - '@swc/helpers'

  accepts@2.0.0:
    dependencies:
      mime-types: 3.0.1
      negotiator: 1.0.0

  acorn-jsx@5.3.2(acorn@8.15.0):
    dependencies:
      acorn: 8.15.0

  acorn@8.15.0: {}

  acorn@8.8.2: {}

  ajv@6.12.6:
    dependencies:
      fast-deep-equal: 3.1.3
      fast-json-stable-stringify: 2.1.0
      json-schema-traverse: 0.4.1
      uri-js: 4.4.1

  ansi-regex@5.0.1: {}

  ansi-regex@6.2.2: {}

  ansi-styles@4.3.0:
    dependencies:
      color-convert: 2.0.1

  ansi-styles@6.2.3: {}

  any-promise@1.3.0: {}

  anymatch@3.1.3:
    dependencies:
      normalize-path: 3.0.0
      picomatch: 2.3.1

  append-field@1.0.0: {}

  archiver-utils@2.1.0:
    dependencies:
      glob: 7.2.3
      graceful-fs: 4.2.11
      lazystream: 1.0.1
      lodash.defaults: 4.2.0
      lodash.difference: 4.5.0
      lodash.flatten: 4.4.0
      lodash.isplainobject: 4.0.6
      lodash.union: 4.6.0
      normalize-path: 3.0.0
      readable-stream: 2.3.8

  archiver-utils@3.0.4:
    dependencies:
      glob: 7.2.3
      graceful-fs: 4.2.11
      lazystream: 1.0.1
      lodash.defaults: 4.2.0
      lodash.difference: 4.5.0
      lodash.flatten: 4.4.0
      lodash.isplainobject: 4.0.6
      lodash.union: 4.6.0
      normalize-path: 3.0.0
      readable-stream: 3.6.2

  archiver@5.3.2:
    dependencies:
      archiver-utils: 2.1.0
      async: 3.2.6
      buffer-crc32: 0.2.13
      readable-stream: 3.6.2
      readdir-glob: 1.1.3
      tar-stream: 2.2.0
      zip-stream: 4.1.1

  arg@5.0.2: {}

  argparse@2.0.1: {}

  array-differ@3.0.0: {}

  array-union@2.1.0: {}

  arrify@2.0.1: {}

  assert@2.0.0:
    dependencies:
      es6-object-assign: 1.1.0
      is-nan: 1.3.2
      object-is: 1.1.6
      util: 0.12.5

  async@3.2.6: {}

  autoprefixer@10.4.21(postcss@8.5.6):
    dependencies:
      browserslist: 4.28.0
      caniuse-lite: 1.0.30001754
      fraction.js: 4.3.7
      normalize-range: 0.1.2
      picocolors: 1.1.1
      postcss: 8.5.6
      postcss-value-parser: 4.2.0

  available-typed-arrays@1.0.7:
    dependencies:
      possible-typed-array-names: 1.1.0

  balanced-match@1.0.2: {}

  base64-js@1.5.1: {}

  baseline-browser-mapping@2.8.28: {}

  bcryptjs@3.0.3: {}

  big-integer@1.6.52: {}

  binary-extensions@2.3.0: {}

  binary@0.3.0:
    dependencies:
      buffers: 0.1.1
      chainsaw: 0.1.0

  bl@4.1.0:
    dependencies:
      buffer: 5.7.1
      inherits: 2.0.4
      readable-stream: 3.6.2

  bluebird@3.4.7: {}

  body-parser@2.2.0:
    dependencies:
      bytes: 3.1.2
      content-type: 1.0.5
      debug: 4.4.3
      http-errors: 2.0.0
      iconv-lite: 0.6.3
      on-finished: 2.4.1
      qs: 6.14.0
      raw-body: 3.0.1
      type-is: 2.0.1
    transitivePeerDependencies:
      - supports-color

  brace-expansion@1.1.12:
    dependencies:
      balanced-match: 1.0.2
      concat-map: 0.0.1

  brace-expansion@2.0.2:
    dependencies:
      balanced-match: 1.0.2

  braces@3.0.3:
    dependencies:
      fill-range: 7.1.1

  browserslist@4.28.0:
    dependencies:
      baseline-browser-mapping: 2.8.28
      caniuse-lite: 1.0.30001754
      electron-to-chromium: 1.5.254
      node-releases: 2.0.27
      update-browserslist-db: 1.1.4(browserslist@4.28.0)

  buffer-crc32@0.2.13: {}

  buffer-from@1.1.2: {}

  buffer-indexof-polyfill@1.0.2: {}

  buffer@5.7.1:
    dependencies:
      base64-js: 1.5.1
      ieee754: 1.2.1

  buffers@0.1.1: {}

  busboy@1.6.0:
    dependencies:
      streamsearch: 1.1.0

  bytes@3.1.2: {}

  call-bind-apply-helpers@1.0.2:
    dependencies:
      es-errors: 1.3.0
      function-bind: 1.1.2

  call-bind@1.0.8:
    dependencies:
      call-bind-apply-helpers: 1.0.2
      es-define-property: 1.0.1
      get-intrinsic: 1.3.0
      set-function-length: 1.2.2

  call-bound@1.0.4:
    dependencies:
      call-bind-apply-helpers: 1.0.2
      get-intrinsic: 1.3.0

  callsites@3.1.0: {}

  camelcase-css@2.0.1: {}

  caniuse-lite@1.0.30001754: {}

  chainsaw@0.1.0:
    dependencies:
      traverse: 0.3.9

  chalk@4.1.2:
    dependencies:
      ansi-styles: 4.3.0
      supports-color: 7.2.0

  chance@1.1.9: {}

  char-regex@1.0.2: {}

  charenc@0.0.2: {}

  chokidar@3.6.0:
    dependencies:
      anymatch: 3.1.3
      braces: 3.0.3
      glob-parent: 5.1.2
      is-binary-path: 2.1.0
      is-glob: 4.0.3
      normalize-path: 3.0.0
      readdirp: 3.6.0
    optionalDependencies:
      fsevents: 2.3.3

  class-validator@0.14.1:
    dependencies:
      '@types/validator': 13.15.9
      libphonenumber-js: 1.12.26
      validator: 13.15.23

  color-convert@2.0.1:
    dependencies:
      color-name: 1.1.4

  color-name@1.1.4: {}

  commander@10.0.0: {}

  commander@4.1.1: {}

  compress-commons@4.1.2:
    dependencies:
      buffer-crc32: 0.2.13
      crc32-stream: 4.0.3
      normalize-path: 3.0.0
      readable-stream: 3.6.2

  concat-map@0.0.1: {}

  concat-stream@2.0.0:
    dependencies:
      buffer-from: 1.1.2
      inherits: 2.0.4
      readable-stream: 3.6.2
      typedarray: 0.0.6

  content-disposition@1.0.1: {}

  content-type@1.0.5: {}

  cookie-signature@1.2.2: {}

  cookie@0.7.2: {}

  core-util-is@1.0.3: {}

  cors@2.8.5:
    dependencies:
      object-assign: 4.1.1
      vary: 1.1.2

  crc-32@1.2.2: {}

  crc32-stream@4.0.3:
    dependencies:
      crc-32: 1.2.2
      readable-stream: 3.6.2

  cross-spawn@7.0.6:
    dependencies:
      path-key: 3.1.1
      shebang-command: 2.0.0
      which: 2.0.2

  crypt@0.0.2: {}

  crypto-js@4.2.0: {}

  cssesc@3.0.0: {}

  csstype@3.2.1: {}

  dayjs@1.11.19: {}

  debug@4.4.3:
    dependencies:
      ms: 2.1.3

  deep-is@0.1.4: {}

  define-data-property@1.1.4:
    dependencies:
      es-define-property: 1.0.1
      es-errors: 1.3.0
      gopd: 1.2.0

  define-properties@1.2.1:
    dependencies:
      define-data-property: 1.1.4
      has-property-descriptors: 1.0.2
      object-keys: 1.1.1

  depd@2.0.0: {}

  destr@2.0.5: {}

  didyoumean@1.2.2: {}

  dlv@1.1.3: {}

  dunder-proto@1.0.1:
    dependencies:
      call-bind-apply-helpers: 1.0.2
      es-errors: 1.3.0
      gopd: 1.2.0

  duplexer2@0.1.4:
    dependencies:
      readable-stream: 2.3.8

  eastasianwidth@0.2.0: {}

  ee-first@1.1.1: {}

  electron-to-chromium@1.5.254: {}

  emoji-regex@8.0.0: {}

  emoji-regex@9.2.2: {}

  encodeurl@2.0.0: {}

  end-of-stream@1.4.5:
    dependencies:
      once: 1.4.0

  es-define-property@1.0.1: {}

  es-errors@1.3.0: {}

  es-object-atoms@1.1.1:
    dependencies:
      es-errors: 1.3.0

  es6-object-assign@1.1.0: {}

  esbuild@0.25.12:
    optionalDependencies:
      '@esbuild/aix-ppc64': 0.25.12
      '@esbuild/android-arm': 0.25.12
      '@esbuild/android-arm64': 0.25.12
      '@esbuild/android-x64': 0.25.12
      '@esbuild/darwin-arm64': 0.25.12
      '@esbuild/darwin-x64': 0.25.12
      '@esbuild/freebsd-arm64': 0.25.12
      '@esbuild/freebsd-x64': 0.25.12
      '@esbuild/linux-arm': 0.25.12
      '@esbuild/linux-arm64': 0.25.12
      '@esbuild/linux-ia32': 0.25.12
      '@esbuild/linux-loong64': 0.25.12
      '@esbuild/linux-mips64el': 0.25.12
      '@esbuild/linux-ppc64': 0.25.12
      '@esbuild/linux-riscv64': 0.25.12
      '@esbuild/linux-s390x': 0.25.12
      '@esbuild/linux-x64': 0.25.12
      '@esbuild/netbsd-arm64': 0.25.12
      '@esbuild/netbsd-x64': 0.25.12
      '@esbuild/openbsd-arm64': 0.25.12
      '@esbuild/openbsd-x64': 0.25.12
      '@esbuild/openharmony-arm64': 0.25.12
      '@esbuild/sunos-x64': 0.25.12
      '@esbuild/win32-arm64': 0.25.12
      '@esbuild/win32-ia32': 0.25.12
      '@esbuild/win32-x64': 0.25.12

  escalade@3.2.0: {}

  escape-html@1.0.3: {}

  escape-string-regexp@4.0.0: {}

  eslint-plugin-react-hooks@5.1.0-rc.0(eslint@9.9.1(jiti@1.21.7)):
    dependencies:
      eslint: 9.9.1(jiti@1.21.7)

  eslint-plugin-react-refresh@0.4.11(eslint@9.9.1(jiti@1.21.7)):
    dependencies:
      eslint: 9.9.1(jiti@1.21.7)

  eslint-scope@7.1.1:
    dependencies:
      esrecurse: 4.3.0
      estraverse: 5.3.0

  eslint-scope@8.4.0:
    dependencies:
      esrecurse: 4.3.0
      estraverse: 5.3.0

  eslint-visitor-keys@3.3.0: {}

  eslint-visitor-keys@3.4.3: {}

  eslint-visitor-keys@4.2.1: {}

  eslint@9.9.1(jiti@1.21.7):
    dependencies:
      '@eslint-community/eslint-utils': 4.9.0(eslint@9.9.1(jiti@1.21.7))
      '@eslint-community/regexpp': 4.12.2
      '@eslint/config-array': 0.18.0
      '@eslint/eslintrc': 3.3.1
      '@eslint/js': 9.9.1
      '@humanwhocodes/module-importer': 1.0.1
      '@humanwhocodes/retry': 0.3.1
      '@nodelib/fs.walk': 1.2.8
      ajv: 6.12.6
      chalk: 4.1.2
      cross-spawn: 7.0.6
      debug: 4.4.3
      escape-string-regexp: 4.0.0
      eslint-scope: 8.4.0
      eslint-visitor-keys: 4.2.1
      espree: 10.4.0
      esquery: 1.6.0
      esutils: 2.0.3
      fast-deep-equal: 3.1.3
      file-entry-cache: 8.0.0
      find-up: 5.0.0
      glob-parent: 6.0.2
      ignore: 5.3.2
      imurmurhash: 0.1.4
      is-glob: 4.0.3
      is-path-inside: 3.0.3
      json-stable-stringify-without-jsonify: 1.0.1
      levn: 0.4.1
      lodash.merge: 4.6.2
      minimatch: 3.1.2
      natural-compare: 1.4.0
      optionator: 0.9.4
      strip-ansi: 6.0.1
      text-table: 0.2.0
    optionalDependencies:
      jiti: 1.21.7
    transitivePeerDependencies:
      - supports-color

  espree@10.4.0:
    dependencies:
      acorn: 8.15.0
      acorn-jsx: 5.3.2(acorn@8.15.0)
      eslint-visitor-keys: 4.2.1

  esprima@4.0.1: {}

  esquery@1.6.0:
    dependencies:
      estraverse: 5.3.0

  esrecurse@4.3.0:
    dependencies:
      estraverse: 5.3.0

  estraverse@5.3.0: {}

  esutils@2.0.3: {}

  etag@1.8.1: {}

  exceljs@4.4.0:
    dependencies:
      archiver: 5.3.2
      dayjs: 1.11.19
      fast-csv: 4.3.6
      jszip: 3.10.1
      readable-stream: 3.6.2
      saxes: 5.0.1
      tmp: 0.2.5
      unzipper: 0.10.14
      uuid: 8.3.2

  express@5.1.0:
    dependencies:
      accepts: 2.0.0
      body-parser: 2.2.0
      content-disposition: 1.0.1
      content-type: 1.0.5
      cookie: 0.7.2
      cookie-signature: 1.2.2
      debug: 4.4.3
      encodeurl: 2.0.0
      escape-html: 1.0.3
      etag: 1.8.1
      finalhandler: 2.1.0
      fresh: 2.0.0
      http-errors: 2.0.0
      merge-descriptors: 2.0.0
      mime-types: 3.0.1
      on-finished: 2.4.1
      once: 1.4.0
      parseurl: 1.3.3
      proxy-addr: 2.0.7
      qs: 6.14.0
      range-parser: 1.2.1
      router: 2.2.0
      send: 1.2.0
      serve-static: 2.2.0
      statuses: 2.0.2
      type-is: 2.0.1
      vary: 1.1.2
    transitivePeerDependencies:
      - supports-color

  fast-csv@4.3.6:
    dependencies:
      '@fast-csv/format': 4.3.5
      '@fast-csv/parse': 4.3.6

  fast-deep-equal@3.1.3: {}

  fast-glob@3.3.3:
    dependencies:
      '@nodelib/fs.stat': 2.0.5
      '@nodelib/fs.walk': 1.2.8
      glob-parent: 5.1.2
      merge2: 1.4.1
      micromatch: 4.0.8

  fast-json-stable-stringify@2.1.0: {}

  fast-levenshtein@2.0.6: {}

  fastq@1.19.1:
    dependencies:
      reusify: 1.1.0

  fdir@6.5.0(picomatch@4.0.3):
    optionalDependencies:
      picomatch: 4.0.3

  file-entry-cache@8.0.0:
    dependencies:
      flat-cache: 4.0.1

  fill-range@7.1.1:
    dependencies:
      to-regex-range: 5.0.1

  finalhandler@2.1.0:
    dependencies:
      debug: 4.4.3
      encodeurl: 2.0.0
      escape-html: 1.0.3
      on-finished: 2.4.1
      parseurl: 1.3.3
      statuses: 2.0.2
    transitivePeerDependencies:
      - supports-color

  find-up@5.0.0:
    dependencies:
      locate-path: 6.0.0
      path-exists: 4.0.0

  flat-cache@4.0.1:
    dependencies:
      flatted: 3.3.3
      keyv: 4.5.4

  flatted@3.3.3: {}

  for-each@0.3.5:
    dependencies:
      is-callable: 1.2.7

  foreground-child@3.3.1:
    dependencies:
      cross-spawn: 7.0.6
      signal-exit: 4.1.0

  forwarded@0.2.0: {}

  fraction.js@4.3.7: {}

  framer-motion@12.23.11(react-dom@18.3.1(react@18.3.1))(react@18.3.1):
    dependencies:
      motion-dom: 12.23.23
      motion-utils: 12.23.6
      tslib: 2.8.1
    optionalDependencies:
      react: 18.3.1
      react-dom: 18.3.1(react@18.3.1)

  fresh@2.0.0: {}

  fs-constants@1.0.0: {}

  fs.realpath@1.0.0: {}

  fsevents@2.3.3:
    optional: true

  fstream@1.0.12:
    dependencies:
      graceful-fs: 4.2.11
      inherits: 2.0.4
      mkdirp: 0.5.6
      rimraf: 2.7.1

  function-bind@1.1.2: {}

  generator-function@2.0.1: {}

  get-intrinsic@1.3.0:
    dependencies:
      call-bind-apply-helpers: 1.0.2
      es-define-property: 1.0.1
      es-errors: 1.3.0
      es-object-atoms: 1.1.1
      function-bind: 1.1.2
      get-proto: 1.0.1
      gopd: 1.2.0
      has-symbols: 1.1.0
      hasown: 2.0.2
      math-intrinsics: 1.1.0

  get-proto@1.0.1:
    dependencies:
      dunder-proto: 1.0.1
      es-object-atoms: 1.1.1

  get-tsconfig@4.13.0:
    dependencies:
      resolve-pkg-maps: 1.0.0

  glob-parent@5.1.2:
    dependencies:
      is-glob: 4.0.3

  glob-parent@6.0.2:
    dependencies:
      is-glob: 4.0.3

  glob@10.4.5:
    dependencies:
      foreground-child: 3.3.1
      jackspeak: 3.4.3
      minimatch: 9.0.5
      minipass: 7.1.2
      package-json-from-dist: 1.0.1
      path-scurry: 1.11.1

  glob@7.2.3:
    dependencies:
      fs.realpath: 1.0.0
      inflight: 1.0.6
      inherits: 2.0.4
      minimatch: 3.1.2
      once: 1.4.0
      path-is-absolute: 1.0.1

  globals@14.0.0: {}

  globals@15.9.0: {}

  goober@2.1.18(csstype@3.2.1):
    dependencies:
      csstype: 3.2.1

  gopd@1.2.0: {}

  graceful-fs@4.2.11: {}

  graphemer@1.4.0: {}

  has-flag@4.0.0: {}

  has-property-descriptors@1.0.2:
    dependencies:
      es-define-property: 1.0.1

  has-symbols@1.1.0: {}

  has-tostringtag@1.0.2:
    dependencies:
      has-symbols: 1.1.0

  hasown@2.0.2:
    dependencies:
      function-bind: 1.1.2

  http-errors@2.0.0:
    dependencies:
      depd: 2.0.0
      inherits: 2.0.4
      setprototypeof: 1.2.0
      statuses: 2.0.1
      toidentifier: 1.0.1

  iconv-lite@0.6.3:
    dependencies:
      safer-buffer: 2.1.2

  iconv-lite@0.7.0:
    dependencies:
      safer-buffer: 2.1.2

  ieee754@1.2.1: {}

  ignore@5.3.2: {}

  immediate@3.0.6: {}

  import-fresh@3.3.1:
    dependencies:
      parent-module: 1.0.1
      resolve-from: 4.0.0

  imurmurhash@0.1.4: {}

  inflight@1.0.6:
    dependencies:
      once: 1.4.0
      wrappy: 1.0.2

  inherits@2.0.4: {}

  inversify@6.0.1: {}

  ipaddr.js@1.9.1: {}

  is-arguments@1.2.0:
    dependencies:
      call-bound: 1.0.4
      has-tostringtag: 1.0.2

  is-binary-path@2.1.0:
    dependencies:
      binary-extensions: 2.3.0

  is-buffer@1.1.6: {}

  is-callable@1.2.7: {}

  is-core-module@2.16.1:
    dependencies:
      hasown: 2.0.2

  is-extglob@2.1.1: {}

  is-fullwidth-code-point@3.0.0: {}

  is-generator-function@1.1.2:
    dependencies:
      call-bound: 1.0.4
      generator-function: 2.0.1
      get-proto: 1.0.1
      has-tostringtag: 1.0.2
      safe-regex-test: 1.1.0

  is-glob@4.0.3:
    dependencies:
      is-extglob: 2.1.1

  is-nan@1.3.2:
    dependencies:
      call-bind: 1.0.8
      define-properties: 1.2.1

  is-number@7.0.0: {}

  is-path-inside@3.0.3: {}

  is-promise@4.0.0: {}

  is-regex@1.2.1:
    dependencies:
      call-bound: 1.0.4
      gopd: 1.2.0
      has-tostringtag: 1.0.2
      hasown: 2.0.2

  is-typed-array@1.1.15:
    dependencies:
      which-typed-array: 1.1.19

  isarray@1.0.0: {}

  isexe@2.0.0: {}

  jackspeak@3.4.3:
    dependencies:
      '@isaacs/cliui': 8.0.2
    optionalDependencies:
      '@pkgjs/parseargs': 0.11.0

  javascript-obfuscator@4.1.1:
    dependencies:
      '@javascript-obfuscator/escodegen': 2.3.0
      '@javascript-obfuscator/estraverse': 5.4.0
      acorn: 8.8.2
      assert: 2.0.0
      chalk: 4.1.2
      chance: 1.1.9
      class-validator: 0.14.1
      commander: 10.0.0
      eslint-scope: 7.1.1
      eslint-visitor-keys: 3.3.0
      fast-deep-equal: 3.1.3
      inversify: 6.0.1
      js-string-escape: 1.0.1
      md5: 2.3.0
      mkdirp: 2.1.3
      multimatch: 5.0.0
      opencollective-postinstall: 2.0.3
      process: 0.11.10
      reflect-metadata: 0.1.13
      source-map-support: 0.5.21
      string-template: 1.0.0
      stringz: 2.1.0
      tslib: 2.5.0

  jiti@1.21.7: {}

  js-string-escape@1.0.1: {}

  js-tokens@4.0.0: {}

  js-yaml@4.1.1:
    dependencies:
      argparse: 2.0.1

  json-buffer@3.0.1: {}

  json-schema-traverse@0.4.1: {}

  json-stable-stringify-without-jsonify@1.0.1: {}

  jszip@3.10.1:
    dependencies:
      lie: 3.3.0
      pako: 1.0.11
      readable-stream: 2.3.8
      setimmediate: 1.0.5

  keyv@4.5.4:
    dependencies:
      json-buffer: 3.0.1

  lazystream@1.0.1:
    dependencies:
      readable-stream: 2.3.8

  levn@0.3.0:
    dependencies:
      prelude-ls: 1.1.2
      type-check: 0.3.2

  levn@0.4.1:
    dependencies:
      prelude-ls: 1.2.1
      type-check: 0.4.0

  libphonenumber-js@1.12.26: {}

  lie@3.3.0:
    dependencies:
      immediate: 3.0.6

  lilconfig@3.1.3: {}

  lines-and-columns@1.2.4: {}

  listenercount@1.0.1: {}

  locate-path@6.0.0:
    dependencies:
      p-locate: 5.0.0

  lodash.defaults@4.2.0: {}

  lodash.difference@4.5.0: {}

  lodash.escaperegexp@4.1.2: {}

  lodash.flatten@4.4.0: {}

  lodash.groupby@4.6.0: {}

  lodash.isboolean@3.0.3: {}

  lodash.isequal@4.5.0: {}

  lodash.isfunction@3.0.9: {}

  lodash.isnil@4.0.0: {}

  lodash.isplainobject@4.0.6: {}

  lodash.isundefined@3.0.1: {}

  lodash.merge@4.6.2: {}

  lodash.union@4.6.0: {}

  lodash.uniq@4.5.0: {}

  loose-envify@1.4.0:
    dependencies:
      js-tokens: 4.0.0

  lru-cache@10.4.3: {}

  lucide-react@0.540.0(react@18.3.1):
    dependencies:
      react: 18.3.1

  math-intrinsics@1.1.0: {}

  md5@2.3.0:
    dependencies:
      charenc: 0.0.2
      crypt: 0.0.2
      is-buffer: 1.1.6

  media-typer@0.3.0: {}

  media-typer@1.1.0: {}

  merge-descriptors@2.0.0: {}

  merge2@1.4.1: {}

  micromatch@4.0.8:
    dependencies:
      braces: 3.0.3
      picomatch: 2.3.1

  mime-db@1.52.0: {}

  mime-db@1.54.0: {}

  mime-types@2.1.35:
    dependencies:
      mime-db: 1.52.0

  mime-types@3.0.1:
    dependencies:
      mime-db: 1.54.0

  minimatch@3.1.2:
    dependencies:
      brace-expansion: 1.1.12

  minimatch@5.1.6:
    dependencies:
      brace-expansion: 2.0.2

  minimatch@9.0.5:
    dependencies:
      brace-expansion: 2.0.2

  minimist@1.2.8: {}

  minipass@7.1.2: {}

  mkdirp@0.5.6:
    dependencies:
      minimist: 1.2.8

  mkdirp@2.1.3: {}

  motion-dom@12.23.23:
    dependencies:
      motion-utils: 12.23.6

  motion-utils@12.23.6: {}

  ms@2.1.3: {}

  multer@2.0.2:
    dependencies:
      append-field: 1.0.0
      busboy: 1.6.0
      concat-stream: 2.0.0
      mkdirp: 0.5.6
      object-assign: 4.1.1
      type-is: 1.6.18
      xtend: 4.0.2

  multimatch@5.0.0:
    dependencies:
      '@types/minimatch': 3.0.5
      array-differ: 3.0.0
      array-union: 2.1.0
      arrify: 2.0.1
      minimatch: 3.1.2

  mz@2.7.0:
    dependencies:
      any-promise: 1.3.0
      object-assign: 4.1.1
      thenify-all: 1.6.0

  nanoid@3.3.11: {}

  natural-compare@1.4.0: {}

  negotiator@1.0.0: {}

  node-fetch-native@1.6.7: {}

  node-releases@2.0.27: {}

  normalize-path@3.0.0: {}

  normalize-range@0.1.2: {}

  object-assign@4.1.1: {}

  object-hash@3.0.0: {}

  object-inspect@1.13.4: {}

  object-is@1.1.6:
    dependencies:
      call-bind: 1.0.8
      define-properties: 1.2.1

  object-keys@1.1.1: {}

  ofetch@1.5.1:
    dependencies:
      destr: 2.0.5
      node-fetch-native: 1.6.7
      ufo: 1.6.1

  on-finished@2.4.1:
    dependencies:
      ee-first: 1.1.1

  once@1.4.0:
    dependencies:
      wrappy: 1.0.2

  opencollective-postinstall@2.0.3: {}

  optionator@0.8.3:
    dependencies:
      deep-is: 0.1.4
      fast-levenshtein: 2.0.6
      levn: 0.3.0
      prelude-ls: 1.1.2
      type-check: 0.3.2
      word-wrap: 1.2.5

  optionator@0.9.4:
    dependencies:
      deep-is: 0.1.4
      fast-levenshtein: 2.0.6
      levn: 0.4.1
      prelude-ls: 1.2.1
      type-check: 0.4.0
      word-wrap: 1.2.5

  p-limit@3.1.0:
    dependencies:
      yocto-queue: 0.1.0

  p-locate@5.0.0:
    dependencies:
      p-limit: 3.1.0

  package-json-from-dist@1.0.1: {}

  pako@1.0.11: {}

  papaparse@5.5.3: {}

  parent-module@1.0.1:
    dependencies:
      callsites: 3.1.0

  parseurl@1.3.3: {}

  path-exists@4.0.0: {}

  path-is-absolute@1.0.1: {}

  path-key@3.1.1: {}

  path-parse@1.0.7: {}

  path-scurry@1.11.1:
    dependencies:
      lru-cache: 10.4.3
      minipass: 7.1.2

  path-to-regexp@8.3.0: {}

  picocolors@1.1.1: {}

  picomatch@2.3.1: {}

  picomatch@4.0.3: {}

  pify@2.3.0: {}

  pirates@4.0.7: {}

  possible-typed-array-names@1.1.0: {}

  postcss-import@15.1.0(postcss@8.5.6):
    dependencies:
      postcss: 8.5.6
      postcss-value-parser: 4.2.0
      read-cache: 1.0.0
      resolve: 1.22.11

  postcss-js@4.1.0(postcss@8.5.6):
    dependencies:
      camelcase-css: 2.0.1
      postcss: 8.5.6

  postcss-load-config@4.0.2(postcss@8.5.6):
    dependencies:
      lilconfig: 3.1.3
      yaml: 2.8.1
    optionalDependencies:
      postcss: 8.5.6

  postcss-nested@6.2.0(postcss@8.5.6):
    dependencies:
      postcss: 8.5.6
      postcss-selector-parser: 6.1.2

  postcss-selector-parser@6.1.2:
    dependencies:
      cssesc: 3.0.0
      util-deprecate: 1.0.2

  postcss-value-parser@4.2.0: {}

  postcss@8.5.6:
    dependencies:
      nanoid: 3.3.11
      picocolors: 1.1.1
      source-map-js: 1.2.1

  prelude-ls@1.1.2: {}

  prelude-ls@1.2.1: {}

  process-nextick-args@2.0.1: {}

  process@0.11.10: {}

  proxy-addr@2.0.7:
    dependencies:
      forwarded: 0.2.0
      ipaddr.js: 1.9.1

  punycode@2.3.1: {}

  qs@6.14.0:
    dependencies:
      side-channel: 1.1.0

  queue-microtask@1.2.3: {}

  range-parser@1.2.1: {}

  raw-body@3.0.1:
    dependencies:
      bytes: 3.1.2
      http-errors: 2.0.0
      iconv-lite: 0.7.0
      unpipe: 1.0.0

  react-dom@18.3.1(react@18.3.1):
    dependencies:
      loose-envify: 1.4.0
      react: 18.3.1
      scheduler: 0.23.2

  react-hot-toast@2.5.2(react-dom@18.3.1(react@18.3.1))(react@18.3.1):
    dependencies:
      csstype: 3.2.1
      goober: 2.1.18(csstype@3.2.1)
      react: 18.3.1
      react-dom: 18.3.1(react@18.3.1)

  react-router-dom@6.26.0(react-dom@18.3.1(react@18.3.1))(react@18.3.1):
    dependencies:
      '@remix-run/router': 1.19.0
      react: 18.3.1
      react-dom: 18.3.1(react@18.3.1)
      react-router: 6.26.0(react@18.3.1)

  react-router@6.26.0(react@18.3.1):
    dependencies:
      '@remix-run/router': 1.19.0
      react: 18.3.1

  react@18.3.1:
    dependencies:
      loose-envify: 1.4.0

  read-cache@1.0.0:
    dependencies:
      pify: 2.3.0

  readable-stream@2.3.8:
    dependencies:
      core-util-is: 1.0.3
      inherits: 2.0.4
      isarray: 1.0.0
      process-nextick-args: 2.0.1
      safe-buffer: 5.1.2
      string_decoder: 1.1.1
      util-deprecate: 1.0.2

  readable-stream@3.6.2:
    dependencies:
      inherits: 2.0.4
      string_decoder: 1.3.0
      util-deprecate: 1.0.2

  readdir-glob@1.1.3:
    dependencies:
      minimatch: 5.1.6

  readdirp@3.6.0:
    dependencies:
      picomatch: 2.3.1

  reflect-metadata@0.1.13: {}

  resolve-from@4.0.0: {}

  resolve-pkg-maps@1.0.0: {}

  resolve@1.22.11:
    dependencies:
      is-core-module: 2.16.1
      path-parse: 1.0.7
      supports-preserve-symlinks-flag: 1.0.0

  reusify@1.1.0: {}

  rimraf@2.7.1:
    dependencies:
      glob: 7.2.3

  rollup@4.53.2:
    dependencies:
      '@types/estree': 1.0.8
    optionalDependencies:
      '@rollup/rollup-android-arm-eabi': 4.53.2
      '@rollup/rollup-android-arm64': 4.53.2
      '@rollup/rollup-darwin-arm64': 4.53.2
      '@rollup/rollup-darwin-x64': 4.53.2
      '@rollup/rollup-freebsd-arm64': 4.53.2
      '@rollup/rollup-freebsd-x64': 4.53.2
      '@rollup/rollup-linux-arm-gnueabihf': 4.53.2
      '@rollup/rollup-linux-arm-musleabihf': 4.53.2
      '@rollup/rollup-linux-arm64-gnu': 4.53.2
      '@rollup/rollup-linux-arm64-musl': 4.53.2
      '@rollup/rollup-linux-loong64-gnu': 4.53.2
      '@rollup/rollup-linux-ppc64-gnu': 4.53.2
      '@rollup/rollup-linux-riscv64-gnu': 4.53.2
      '@rollup/rollup-linux-riscv64-musl': 4.53.2
      '@rollup/rollup-linux-s390x-gnu': 4.53.2
      '@rollup/rollup-linux-x64-gnu': 4.53.2
      '@rollup/rollup-linux-x64-musl': 4.53.2
      '@rollup/rollup-openharmony-arm64': 4.53.2
      '@rollup/rollup-win32-arm64-msvc': 4.53.2
      '@rollup/rollup-win32-ia32-msvc': 4.53.2
      '@rollup/rollup-win32-x64-gnu': 4.53.2
      '@rollup/rollup-win32-x64-msvc': 4.53.2
      fsevents: 2.3.3

  router@2.2.0:
    dependencies:
      debug: 4.4.3
      depd: 2.0.0
      is-promise: 4.0.0
      parseurl: 1.3.3
      path-to-regexp: 8.3.0
    transitivePeerDependencies:
      - supports-color

  run-parallel@1.2.0:
    dependencies:
      queue-microtask: 1.2.3

  safe-buffer@5.1.2: {}

  safe-buffer@5.2.1: {}

  safe-regex-test@1.1.0:
    dependencies:
      call-bound: 1.0.4
      es-errors: 1.3.0
      is-regex: 1.2.1

  safer-buffer@2.1.2: {}

  saxes@5.0.1:
    dependencies:
      xmlchars: 2.2.0

  scheduler@0.23.2:
    dependencies:
      loose-envify: 1.4.0

  semver@7.7.3: {}

  send@1.2.0:
    dependencies:
      debug: 4.4.3
      encodeurl: 2.0.0
      escape-html: 1.0.3
      etag: 1.8.1
      fresh: 2.0.0
      http-errors: 2.0.0
      mime-types: 3.0.1
      ms: 2.1.3
      on-finished: 2.4.1
      range-parser: 1.2.1
      statuses: 2.0.2
    transitivePeerDependencies:
      - supports-color

  serve-static@2.2.0:
    dependencies:
      encodeurl: 2.0.0
      escape-html: 1.0.3
      parseurl: 1.3.3
      send: 1.2.0
    transitivePeerDependencies:
      - supports-color

  set-function-length@1.2.2:
    dependencies:
      define-data-property: 1.1.4
      es-errors: 1.3.0
      function-bind: 1.1.2
      get-intrinsic: 1.3.0
      gopd: 1.2.0
      has-property-descriptors: 1.0.2

  setimmediate@1.0.5: {}

  setprototypeof@1.2.0: {}

  shebang-command@2.0.0:
    dependencies:
      shebang-regex: 3.0.0

  shebang-regex@3.0.0: {}

  side-channel-list@1.0.0:
    dependencies:
      es-errors: 1.3.0
      object-inspect: 1.13.4

  side-channel-map@1.0.1:
    dependencies:
      call-bound: 1.0.4
      es-errors: 1.3.0
      get-intrinsic: 1.3.0
      object-inspect: 1.13.4

  side-channel-weakmap@1.0.2:
    dependencies:
      call-bound: 1.0.4
      es-errors: 1.3.0
      get-intrinsic: 1.3.0
      object-inspect: 1.13.4
      side-channel-map: 1.0.1

  side-channel@1.1.0:
    dependencies:
      es-errors: 1.3.0
      object-inspect: 1.13.4
      side-channel-list: 1.0.0
      side-channel-map: 1.0.1
      side-channel-weakmap: 1.0.2

  signal-exit@4.1.0: {}

  source-map-js@1.2.1: {}

  source-map-support@0.5.21:
    dependencies:
      buffer-from: 1.1.2
      source-map: 0.6.1

  source-map@0.6.1: {}

  statuses@2.0.1: {}

  statuses@2.0.2: {}

  streamsearch@1.1.0: {}

  string-template@1.0.0: {}

  string-width@4.2.3:
    dependencies:
      emoji-regex: 8.0.0
      is-fullwidth-code-point: 3.0.0
      strip-ansi: 6.0.1

  string-width@5.1.2:
    dependencies:
      eastasianwidth: 0.2.0
      emoji-regex: 9.2.2
      strip-ansi: 7.1.2

  string_decoder@1.1.1:
    dependencies:
      safe-buffer: 5.1.2

  string_decoder@1.3.0:
    dependencies:
      safe-buffer: 5.2.1

  stringz@2.1.0:
    dependencies:
      char-regex: 1.0.2

  strip-ansi@6.0.1:
    dependencies:
      ansi-regex: 5.0.1

  strip-ansi@7.1.2:
    dependencies:
      ansi-regex: 6.2.2

  strip-json-comments@3.1.1: {}

  sucrase@3.35.0:
    dependencies:
      '@jridgewell/gen-mapping': 0.3.13
      commander: 4.1.1
      glob: 10.4.5
      lines-and-columns: 1.2.4
      mz: 2.7.0
      pirates: 4.0.7
      ts-interface-checker: 0.1.13

  supports-color@7.2.0:
    dependencies:
      has-flag: 4.0.0

  supports-preserve-symlinks-flag@1.0.0: {}

  tailwindcss@3.4.17:
    dependencies:
      '@alloc/quick-lru': 5.2.0
      arg: 5.0.2
      chokidar: 3.6.0
      didyoumean: 1.2.2
      dlv: 1.1.3
      fast-glob: 3.3.3
      glob-parent: 6.0.2
      is-glob: 4.0.3
      jiti: 1.21.7
      lilconfig: 3.1.3
      micromatch: 4.0.8
      normalize-path: 3.0.0
      object-hash: 3.0.0
      picocolors: 1.1.1
      postcss: 8.5.6
      postcss-import: 15.1.0(postcss@8.5.6)
      postcss-js: 4.1.0(postcss@8.5.6)
      postcss-load-config: 4.0.2(postcss@8.5.6)
      postcss-nested: 6.2.0(postcss@8.5.6)
      postcss-selector-parser: 6.1.2
      resolve: 1.22.11
      sucrase: 3.35.0
    transitivePeerDependencies:
      - ts-node

  tar-stream@2.2.0:
    dependencies:
      bl: 4.1.0
      end-of-stream: 1.4.5
      fs-constants: 1.0.0
      inherits: 2.0.4
      readable-stream: 3.6.2

  text-table@0.2.0: {}

  thenify-all@1.6.0:
    dependencies:
      thenify: 3.3.1

  thenify@3.3.1:
    dependencies:
      any-promise: 1.3.0

  tinyglobby@0.2.15:
    dependencies:
      fdir: 6.5.0(picomatch@4.0.3)
      picomatch: 4.0.3

  tmp@0.2.5: {}

  to-regex-range@5.0.1:
    dependencies:
      is-number: 7.0.0

  toidentifier@1.0.1: {}

  traverse@0.3.9: {}

  ts-api-utils@1.4.3(typescript@5.5.3):
    dependencies:
      typescript: 5.5.3

  ts-interface-checker@0.1.13: {}

  tslib@2.5.0: {}

  tslib@2.8.1: {}

  tsx@4.20.6:
    dependencies:
      esbuild: 0.25.12
      get-tsconfig: 4.13.0
    optionalDependencies:
      fsevents: 2.3.3

  type-check@0.3.2:
    dependencies:
      prelude-ls: 1.1.2

  type-check@0.4.0:
    dependencies:
      prelude-ls: 1.2.1

  type-is@1.6.18:
    dependencies:
      media-typer: 0.3.0
      mime-types: 2.1.35

  type-is@2.0.1:
    dependencies:
      content-type: 1.0.5
      media-typer: 1.1.0
      mime-types: 3.0.1

  typedarray@0.0.6: {}

  typescript-eslint@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3):
    dependencies:
      '@typescript-eslint/eslint-plugin': 8.3.0(@typescript-eslint/parser@8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3))(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      '@typescript-eslint/parser': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
      '@typescript-eslint/utils': 8.3.0(eslint@9.9.1(jiti@1.21.7))(typescript@5.5.3)
    optionalDependencies:
      typescript: 5.5.3
    transitivePeerDependencies:
      - eslint
      - supports-color

  typescript@5.5.3: {}

  ufo@1.6.1: {}

  undici-types@7.16.0: {}

  unpipe@1.0.0: {}

  unzipper@0.10.14:
    dependencies:
      big-integer: 1.6.52
      binary: 0.3.0
      bluebird: 3.4.7
      buffer-indexof-polyfill: 1.0.2
      duplexer2: 0.1.4
      fstream: 1.0.12
      graceful-fs: 4.2.11
      listenercount: 1.0.1
      readable-stream: 2.3.8
      setimmediate: 1.0.5

  update-browserslist-db@1.1.4(browserslist@4.28.0):
    dependencies:
      browserslist: 4.28.0
      escalade: 3.2.0
      picocolors: 1.1.1

  uri-js@4.4.1:
    dependencies:
      punycode: 2.3.1

  util-deprecate@1.0.2: {}

  util@0.12.5:
    dependencies:
      inherits: 2.0.4
      is-arguments: 1.2.0
      is-generator-function: 1.1.2
      is-typed-array: 1.1.15
      which-typed-array: 1.1.19

  uuid@11.1.0: {}

  uuid@8.3.2: {}

  validator@13.15.23: {}

  vary@1.1.2: {}

  vite-plugin-javascript-obfuscator@3.1.0:
    dependencies:
      anymatch: 3.1.3
      javascript-obfuscator: 4.1.1

  vite-plugin-obfuscator@1.0.5:
    dependencies:
      javascript-obfuscator: 4.1.1

  vite@7.2.2(@types/node@24.10.1)(jiti@1.21.7)(tsx@4.20.6)(yaml@2.8.1):
    dependencies:
      esbuild: 0.25.12
      fdir: 6.5.0(picomatch@4.0.3)
      picomatch: 4.0.3
      postcss: 8.5.6
      rollup: 4.53.2
      tinyglobby: 0.2.15
    optionalDependencies:
      '@types/node': 24.10.1
      fsevents: 2.3.3
      jiti: 1.21.7
      tsx: 4.20.6
      yaml: 2.8.1

  which-typed-array@1.1.19:
    dependencies:
      available-typed-arrays: 1.0.7
      call-bind: 1.0.8
      call-bound: 1.0.4
      for-each: 0.3.5
      get-proto: 1.0.1
      gopd: 1.2.0
      has-tostringtag: 1.0.2

  which@2.0.2:
    dependencies:
      isexe: 2.0.0

  word-wrap@1.2.5: {}

  wrap-ansi@7.0.0:
    dependencies:
      ansi-styles: 4.3.0
      string-width: 4.2.3
      strip-ansi: 6.0.1

  wrap-ansi@8.1.0:
    dependencies:
      ansi-styles: 6.2.3
      string-width: 5.1.2
      strip-ansi: 7.1.2

  wrappy@1.0.2: {}

  ws@8.18.3: {}

  xmlchars@2.2.0: {}

  xtend@4.0.2: {}

  yaml@2.8.1: {}

  yocto-queue@0.1.0: {}

  zip-stream@4.1.1:
    dependencies:
      archiver-utils: 3.0.4
      compress-commons: 4.1.2
      readable-stream: 3.6.2



================================================================
File Path: postcss.config.js
================================================================

 export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}



================================================================
File Path: tailwind.config.js
================================================================

/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
} 



================================================================
File Path: tsconfig.app.json
================================================================

{
  "compilerOptions": {
    "target": "ES2020",
    "useDefineForClassFields": true,
    "lib": ["ES2020", "DOM", "DOM.Iterable"],
    "module": "ESNext",
    "skipLibCheck": true,

    /* Bundler mode */
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "isolatedModules": true,
    "moduleDetection": "force",
    "noEmit": true,
    "jsx": "react-jsx",

    /* Linting */
    "strict": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "noFallthroughCasesInSwitch": true,

    "baseUrl": ".",
    "paths": {
      "@/*": ["src/*"]
    }
  },
  "include": ["src"]
}
 



================================================================
File Path: tsconfig.json
================================================================

{
  "files": [],
  "references": [
    { "path": "./tsconfig.app.json" },
    { "path": "./tsconfig.node.json" }
  ]
}
 



================================================================
File Path: tsconfig.node.json
================================================================

{
  "compilerOptions": {
    "target": "ES2022",
    "lib": ["ES2023"],
    "module": "ESNext",
    "skipLibCheck": true,

    /* Bundler mode */
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "isolatedModules": true,
    "moduleDetection": "force",
    "noEmit": true,

    /* Linting */
    "strict": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "noFallthroughCasesInSwitch": true
  },
  "include": ["vite.config.ts"]
}
 



================================================================
File Path: upload.log
================================================================

 
[啟動] 已清空 upload.log 
[2025-11-23 14:02:23] ✅ 上傳服務器運行在 http://localhost:3001
[2025-11-23 14:02:23] 📁 LOG 檔案位置: C:\Users\user\Downloads\1122\upload.log



================================================================
File Path: videoBase.backup.2025-11-21T15-35-57.ts
================================================================

// src/services/videoBase.ts

export interface VideoItem {
  videoId: string;
  title_zh: string;
  title_en: string;
  description_zh: string;
  description_en: string;
  category: 'hero' | 'gallery';
  enabled: boolean;
}

export const videoBase: VideoItem[] = [
  {
    "videoId": "PK7veIY94Rc",
    "title_zh": "客戶回訪實錄。",
    "title_en": "Customer Revisit Record.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "GhZYPoq9-P0",
    "title_zh": "重要關鍵—信賴EGD。",
    "title_en": "Key Factor—Trust EGD.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "INnUG4JHrOQ",
    "title_zh": "您的擔心，都被「都值得了」取代。",
    "title_en": "Your Worries, All Replaced by \"It Was Worth It\".",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "TFQMGVSEOA4",
    "title_zh": "侘寂之境(Wabi-Sabi)，極簡美學。",
    "title_en": "Wabi-Sabi Realm, Minimalist Aesthetics.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "h8edKG3H-6Y",
    "title_zh": "台灣EGD: 願美好永遠存在。",
    "title_en": "Taiwan EGD: May Goodness Forever Endure.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "byFTTj1znH0",
    "title_zh": "再有難度-用心作園藝。",
    "title_en": "No Matter How Difficult—Gardening with Heart.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "uwDDYu8mI3Q",
    "title_zh": "帶你上雲端！為高空定義真正的夢幻花園。",
    "title_en": "Take You to the Clouds! Defining a True Dream Garden at Heights.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "ddGXcJUxORM",
    "title_zh": "征服困難崎零地，打造夢幻庭園!",
    "title_en": "Conquer Difficult Terrain, Create a Dream Garden!",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "rfS4HxVM1ps",
    "title_zh": "植癒生活:讓美好,在指尖與花葉間永續。",
    "title_en": "Plant Healing Life: Let Beauty Flourish Sustainably, Between Your Fingertips and the Greenery.",
    "description_zh": "植癒生活:讓美好,在指尖與花葉間永續。",
    "description_en": "Plant Healing Life: Let Beauty Flourish Sustainably, Between Your Fingertips and the Greenery.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "o3qBmM54Fbs",
    "title_zh": "視覺魔術-瞬間上色!",
    "title_en": "Visual Alchemy! Monochrome Rendered in Color!",
    "description_zh": "視覺魔術-瞬間上色!",
    "description_en": "Visual Alchemy! Monochrome Rendered in Color!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "U_XKi919euc",
    "title_zh": "超越視野-定義新標竿。",
    "title_en": "Beyond the Horizon: Defining the New Benchmark.",
    "description_zh": "超越視野-定義新標竿。",
    "description_en": "Beyond the horizon: Defining the new benchmark.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "xm3UtfIysl0",
    "title_zh": "施工、驗收與完美交付!",
    "title_en": "Execution, Verification, and Perfect Handoff!",
    "description_zh": "施工、驗收與完美交付!",
    "description_en": "Execution, Verification, and Perfect Handoff!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "9au64VDA06k",
    "title_zh": "復育生態鏈:給下一代最好的禮物。",
    "title_en": "The Ultimate Forest Gift for the Next Generation.",
    "description_zh": "復育生態鏈:給下一代最好的禮物。",
    "description_en": "The Ultimate Forest Gift for the Next Generation.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "GO9AFVEqFzk",
    "title_zh": "秋日黃金海",
    "title_en": "A Golden Sea in Autumn, Dyeing a Thousand Peaks.",
    "description_zh": "秋日黃金海",
    "description_en": "A Golden Sea in Autumn, Dyeing a Thousand Peaks.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "0N4J6sYIr50",
    "title_zh": "草地變魔戒森林？頻率是關鍵！",
    "title_en": "Frequency is the Key!",
    "description_zh": "草地變魔戒森林？頻率是關鍵！",
    "description_en": "Frequency is the Key!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "SV9H23E_R9Q",
    "title_zh": "15秒!就是台灣系列: 預告片。",
    "title_en": "Taiwan in 15 Seconds! The Teaser.",
    "description_zh": "15秒!就是台灣系列: 預告片。",
    "description_en": "Taiwan in 15 Seconds! The Teaser.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "ylhvXL8ueW0",
    "title_zh": "從零到有,實現你的夢幻花園。",
    "title_en": "From Zero to Bloom: Realize Your Dream Garden.",
    "description_zh": "從零到有,實現你的夢幻花園。",
    "description_en": "From Zero to Bloom: Realize your dream garden.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "Rdg3Wo8p5bU",
    "title_zh": "白領: 享受周末的園藝時光!",
    "title_en": "Our Dreamy Weekend Indoor Gardening Routine.",
    "description_zh": "白領: 享受周末的園藝時光!",
    "description_en": "Our Dreamy Weekend Indoor Gardening Routine.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "AOUNGkD064I",
    "title_zh": "從積水到美景: 雨水花園。",
    "title_en": "Building Our Dream Rain Garden from Scratch.",
    "description_zh": "從積水到美景: 雨水花園。",
    "description_en": "Building Our Dream Rain Garden from Scratch.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "ryaP_GS_Hi8",
    "title_zh": "肖楠: 種子覺醒。",
    "title_en": "Seed to Life",
    "description_zh": "肖楠: 種子覺醒。",
    "description_en": "Seed to Life",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "K879oNZvLr8",
    "title_zh": "月桃: 何止是記憶,更是溫暖印記。",
    "title_en": "It's Grandma's Warm Legacy.",
    "description_zh": "月桃: 何止是記憶,更是溫暖印記。",
    "description_en": "It's Grandma's Warm Legacy.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "-4x07g4rlxo",
    "title_zh": "ESG-綠色永續營運。",
    "title_en": "ESG - Green Sustainable Operations.",
    "description_zh": "ESG-綠色永續營運。",
    "description_en": "ESG - Green Sustainable Operations.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "hO_fIaq0mjA",
    "title_zh": "浪載星屑，灣藏夢幻光。",
    "title_en": "Waves Carry Stardust, the Bay Holds a Magical Light.",
    "description_zh": "浪載星屑，灣藏夢幻光。",
    "description_en": "Waves carry stardust, the bay holds a magical light.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "hoYBYkCaoxg",
    "title_zh": "台灣衫: 極致的心靈森呼吸。",
    "title_en": "Give Your Mind the Ultimate Forest Bathing (Shinrin-yoku).",
    "description_zh": "台灣衫: 極致的心靈森呼吸。",
    "description_en": "Give Your Mind the Ultimate Forest Bathing (Shinrin-yoku).",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "oLwpEJpcd3k",
    "title_zh": "玉山圓柏: 環境再艱苦也絕不放棄。",
    "title_en": "A Resilience Guide",
    "description_zh": "玉山圓柏: 環境再艱苦也絕不放棄。",
    "description_en": "A Resilience Guide",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "rDlbaw7znEs",
    "title_zh": "藍眼淚，共同守護藍色星魂。",
    "title_en": "The Emotion of Guarding the Blue Star Soul.",
    "description_zh": "藍眼淚，共同守護藍色星魂。",
    "description_en": "The Emotion of Guarding the Blue Star Soul.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "sFtCKquZYwM",
    "title_zh": "退休不空虛：告別無聊人生的實用指南。",
    "title_en": "A Practical Guide to Saying Goodbye to a Boring Life.",
    "description_zh": "退休不空虛：告別無聊人生的實用指南。",
    "description_en": "A Practical Guide to Saying Goodbye to a Boring Life.",
    "category": "gallery",
    "enabled": true
  }
];



================================================================
File Path: vite.config.ts
================================================================

import type { UserConfig } from 'vite'
import react from '@vitejs/plugin-react-swc'
import { defineConfig } from 'vite'
import JavaScriptObfuscator from 'vite-plugin-javascript-obfuscator'

export default defineConfig(({ mode }) => {
  let build: UserConfig['build'], esbuild: UserConfig['esbuild'], define: UserConfig['define']
  let plugins = [react()]

  if (mode === 'development') {
    build = {
      minify: false,
      sourcemap: true,
      rollupOptions: {
        output: {
          manualChunks: undefined,
        },
      },
    }

    esbuild = {
      jsxDev: true,
      keepNames: true,
      minifyIdentifiers: false,
    }

    define = {
      'process.env.NODE_ENV': '"development"',
      '__DEV__': 'true',
    }
  } else {
    build = {
      sourcemap: false,
      rollupOptions: {
        output: {
          manualChunks(id) {
            // React 相關庫
            if (id.includes('node_modules/react') || 
                id.includes('node_modules/react-dom') || 
                id.includes('node_modules/react-router-dom')) {
              return 'react-vendor'
            }
            
            // Supabase
            if (id.includes('node_modules/@supabase')) {
              return 'supabase'
            }
            
            // UI 庫
            if (id.includes('node_modules/lucide-react')) {
              return 'ui-libs'
            }
            
            // 🔥 每個 component 打包成獨立檔案
            if (id.includes('/components/')) {
              const match = id.match(/\/components\/([^/]+)\.(tsx|ts|jsx|js)/)
              if (match) {
                return match[1]
              }
            }
          },
          entryFileNames: 'assets/[name]-[hash].js',
          chunkFileNames: 'assets/[name]-[hash].js',
        }
      },
      chunkSizeWarningLimit: 10000
    }

    plugins.push(
      JavaScriptObfuscator({
        include: ['src/**/*.tsx', 'src/**/*.ts'],
        exclude: [
          '**/react-vendor*.js',
          '**/supabase*.js',
          '**/ui-libs*.js'
        ],
        options: {
          compact: true,
          controlFlowFlattening: false,
          deadCodeInjection: false,
          stringArray: true,
          stringArrayThreshold: 0.75
        }
      })
    )
  }

  return {
    plugins,
    build,
    esbuild,
    define,
    resolve: {
      alias: {
        '@': '/src',
      }
    },
    optimizeDeps: {
      exclude: ['lucide-react'],
    },
    server: {
      port: 5173,
    },
    preview: {
      port: 4173,
    }
  }
})


================================================================
File Path: 啟動_含影片管理+知識庫管理上傳功能.bat
================================================================

REM ========================================
REM 完整開發環境啟動腳本
REM ========================================
REM 
REM 功能：
REM ✅ 清空舊 LOG 檔案
REM ✅ 啟動後端_知識庫服務器（PORT 3002）
REM ✅ 啟動後端_影片管理服務器（PORT 3001）
REM ✅ 啟動前端服務器（PORT 5173）
REM ✅ 自動打開 LOG 檔案
REM ✅ 自動打開瀏覽器
REM 
REM 會清理的檔案：
REM ✅ videoBase.backup.2025-11-19T14-30-45.ts
REM ✅ videoBase.backup.1763605533886.ts（舊格式也會清）
REM 
REM 不會清理的檔案：
REM ❌ upload.log
REM ❌ knowledge.log
REM ❌ package.json
REM ❌ App.tsx
REM ❌ 其他任何檔案
REM 
REM 完美！
REM 現在架構超清楚：
REM 📚 後端_知識庫服務器 (3002)
REM 📹 後端_影片管理服務器 (3001)
REM 🌐 前端服務器 (5173)
REM 一看就知道誰是後端、誰是前端！ 👍
REM ========================================

@echo on
chcp 65001 >nul
title 完整開發環境

echo ========================================
echo 🚀 正在啟動完整開發環境...
echo ========================================

REM 清除 7 天前的備份檔案（註解掉，測試時手動啟用）
forfiles /P . /M videoBase.backup.*.ts /D -7 /C "cmd /c del @path" 2>nul

REM 清除 30 分鐘前的備份檔案（註解掉，測試時手動啟用）
REM powershell -Command "Get-ChildItem -Path . -Filter 'videoBase.backup.*.ts' | Where-Object { $_.LastWriteTime -lt (Get-Date).AddMinutes(-30) } | Remove-Item -Force"

REM 啟動前端服務器
echo 🌐 啟動前端服務器...
call pnpm install
REM 等待 2 秒
timeout /t 2 /nobreak >nul

REM 清空舊 LOG
echo. > upload.log
echo [啟動] 已清空 upload.log >> upload.log
echo. > knowledge.log
echo [啟動] 已清空 knowledge.log >> knowledge.log

REM 啟動後端_知識庫服務器
echo 📚 啟動後端_知識庫服務器...
start "後端_知識庫服務器 (PORT 3002)" cmd /k "cd src/server && node index.js"

REM 等待 2 秒
timeout /t 2 /nobreak >nul

REM 啟動後端_影片管理服務器
echo 📹 啟動後端_影片管理服務器...
start "後端_影片管理服務器 (PORT 3001)" cmd /k "node scripts/uploadServer.cjs"

REM 等待 2 秒
timeout /t 2 /nobreak >nul

REM 啟動前端服務器
echo 🌐 啟動前端服務器...
start "前端服務器 (PORT 5173)" cmd /k "pnpm run dev"

REM 等待 3 秒
timeout /t 3 /nobreak >nul

REM 自動打開 LOG 檔案
echo 📋 打開 LOG 檔案...
start notepad upload.log
start notepad knowledge.log

REM 等待 2 秒
timeout /t 2 /nobreak >nul

REM 自動打開瀏覽器
echo 🌐 打開瀏覽器...
start http://localhost:5173

echo.
echo ========================================
echo ✅ 開發環境已啟動完成！
echo ========================================
echo.
echo 📌 後端_知識庫服務器:   http://localhost:3002
echo 📌 後端_影片管理服務器: http://localhost:3001
echo 📌 前端服務器:         http://localhost:5173
echo.
echo 📋 LOG 檔案:
echo    - upload.log (影片管理)
echo    - knowledge.log (知識庫)
echo.
echo 💡 提示：
echo    - 移除第 35 行的 REM 可啟用「清除 7 天前的備份」
echo    - 移除第 38 行的 REM 可啟用「清除 30 分鐘前的備份」
echo.
echo 🛑 關閉方式：
echo    - 直接關閉所有 CMD 視窗即可
echo.
pause



================================================================
File Path: scripts/uploadServer.cjs
================================================================

const express = require('express');
const multer = require('multer');
const cors = require('cors');
const ExcelJS = require('exceljs');
const fs = require('fs').promises;
const path = require('path');

const app = express();
const upload = multer({ storage: multer.memoryStorage() });

app.use(cors());
app.use(express.json());

// 寫入 LOG 的函數 - 使用 GMT+8 時間
async function writeLog(message) {
  const now = new Date();
  // 轉換成 GMT+8 時間
  const taiwanTime = new Date(now.getTime() + (8 * 60 * 60 * 1000));
  const timestamp = taiwanTime.toISOString().replace('T', ' ').substring(0, 19);
  const logMessage = `[${timestamp}] ${message}\n`;
  const logPath = path.join(__dirname, '../upload.log');
  
  try {
    await fs.appendFile(logPath, logMessage, 'utf-8');
    console.log(message); // 同時輸出到終端
  } catch (error) {
    console.error('寫入 LOG 失敗:', error);
  }
}

// 上傳端點
app.post('/api/upload-videos', upload.single('file'), async (req, res) => {
  try {
    await writeLog('\n========== 開始新的上傳 ==========');
    
    if (!req.file) {
      await writeLog('❌ 沒有收到檔案');
      return res.status(400).json({ success: false, message: '沒有收到檔案' });
    }

    await writeLog(`📁 檔案名稱: ${req.file.originalname}`);
    await writeLog(`📊 檔案大小: ${(req.file.size / 1024).toFixed(2)} KB`);

    // 解析 Excel
    await writeLog('🔍 開始解析 Excel...');
    const workbook = new ExcelJS.Workbook();
    await workbook.xlsx.load(req.file.buffer);
    const worksheet = workbook.getWorksheet(1);

    const videos = [];
    const headers = worksheet.getRow(1).values;

    worksheet.eachRow((row, rowNumber) => {
      if (rowNumber === 1) return;

      const rowData = {};
      headers.forEach((header, index) => {
        if (header) {
          rowData[header] = row.getCell(index).value;
        }
      });

      videos.push({
        videoId: String(rowData.videoId || ''),
        title_zh: String(rowData.title_zh || ''),
        title_en: String(rowData.title_en || ''),
        description_zh: String(rowData.description_zh || ''),
        description_en: String(rowData.description_en || ''),
        category: (rowData.category === 'hero' || rowData.category === 'gallery') ? rowData.category : 'gallery',
        enabled: rowData.enabled === 'true' || rowData.enabled === true || rowData.enabled === 1
      });
    });

    await writeLog(`✅ 解析完成，共 ${videos.length} 筆資料`);
    
    // 記錄每筆資料
    await writeLog('\n📋 資料內容：');
    for (let i = 0; i < videos.length; i++) {
      const v = videos[i];
      await writeLog(`  ${i + 1}. [${v.category}] ${v.videoId} - ${v.title_zh} (enabled: ${v.enabled})`);
    }

    // 生成新的 videoBase.ts 內容
    const fileContent = `// src/services/videoBase.ts

export interface VideoItem {
  videoId: string;
  title_zh: string;
  title_en: string;
  description_zh: string;
  description_en: string;
  category: 'hero' | 'gallery';
  enabled: boolean;
}

export const videoBase: VideoItem[] = ${JSON.stringify(videos, null, 2)};
`;

    // 寫入檔案
    const filePath = path.join(__dirname, '../src/services/videoBase.ts');
    await writeLog(`\n📝 準備寫入檔案: ${filePath}`);
    
    // 備份舊檔案 - 使用易讀的日期格式 (GMT+8)
    try {
      const oldContent = await fs.readFile(filePath, 'utf-8');
      const now = new Date();
      const taiwanTime = new Date(now.getTime() + (8 * 60 * 60 * 1000));
      const dateStr = taiwanTime.toISOString().replace(/[:.]/g, '-').substring(0, 19); // 2025-11-20T10-30-45
      const backupPath = path.join(__dirname, `../videoBase.backup.${dateStr}.ts`);
      await fs.writeFile(backupPath, oldContent, 'utf-8');
      await writeLog(`💾 已備份舊檔案: ${backupPath}`);
    } catch (error) {
      await writeLog(`⚠️  無法備份舊檔案: ${error.message}`);
    }
    
    await fs.writeFile(filePath, fileContent, 'utf-8');
    
    await writeLog('✅ 已成功寫入檔案');
    await writeLog(`📊 寫入統計: ${videos.length} 筆資料, 檔案大小: ${(fileContent.length / 1024).toFixed(2)} KB`);
    await writeLog('========== 上傳完成 ==========\n');

    res.json({
      success: true,
      message: `成功更新 ${videos.length} 筆影片資料到 videoBase.ts`
    });

  } catch (error) {
    await writeLog(`❌ 上傳失敗: ${error.message}`);
    await writeLog(`❌ 錯誤堆疊: ${error.stack}`);
    res.status(500).json({
      success: false,
      message: error.message
    });
  }
});

const PORT = 3001;
app.listen(PORT, async () => {
  const message = `✅ 上傳服務器運行在 http://localhost:${PORT}`;
  console.log(message);
  await writeLog(message);
  await writeLog(`📁 LOG 檔案位置: ${path.join(__dirname, '../upload.log')}`);
});


================================================================
File Path: src/App.tsx
================================================================

import React, { useState, lazy, Suspense } from 'react'
import { LanguageProvider } from './contexts/LanguageContext'
import Navbar from './components/Navbar'
import HeroSection from './components/HeroSection'
{/*  import { AudioPlayer } from './components/AudioPlayer' */}
import VideoManager from "./components/VideoManager"
import KnowledgeBaseManager from "./components/KnowledgeBaseManager"


{/* 動態導入非首屏組件(Code Splitting) */}
const AboutSection = lazy(() => import('./components/AboutSection'))
const ServicesSection = lazy(() => import('./components/ServicesSection'))
const PortfolioSection = lazy(() => import('./components/PortfolioSection'))
const TestimonialsSection = lazy(() => import('./components/TestimonialsSection'))
const YouTubeGallery = lazy(() => import('./components/YouTubeGallery'))
const ContactSection = lazy(() => import('./components/ContactSection'))
const Footer = lazy(() => import('./components/Footer'))
const VideoModal = lazy(() => import('./components/VideoModal'))
const ChatBot = lazy(() => import('./components/ChatBot/ChatBot'))
const VisitorAnalytics = lazy(() => import('./components/VisitorAnalytics'))

function App() {
  const [isVideoModalOpen, setIsVideoModalOpen] = useState(false)

  const openVideoModal = () => {
    setIsVideoModalOpen(true)
  }

  const closeVideoModal = () => {
    setIsVideoModalOpen(false)
  }

  return (
    <LanguageProvider>
      <div className="min-h-screen bg-[#0B0919] text-white">
        <Navbar />
        <main>
          <HeroSection onPlayVideo={openVideoModal} />
          
          {/* Suspense 包裹延遲載入的組件 */}
          <Suspense fallback={
            <div className="flex items-center justify-center py-20">
              <div className="w-12 h-12 border-4 border-emerald-500 border-t-transparent rounded-full animate-spin"></div>
            </div>
          }>
            <AboutSection />
            <ServicesSection />
            <PortfolioSection onPlayVideo={openVideoModal} />
            <YouTubeGallery />
            <TestimonialsSection />
            <ContactSection />
          </Suspense>
        </main>
        
        <Suspense fallback={null}>
          <Footer />
        </Suspense>
        
        {/* 視頻模態框 - 延遲載入 */}
        <Suspense fallback={null}>
          {isVideoModalOpen && (
            <VideoModal
              isOpen={isVideoModalOpen}
              onClose={closeVideoModal}
            />
          )}
        </Suspense>
        
        {/* 聊天機器人 - 延遲載入 */}
        <Suspense fallback={null}>
          <ChatBot />
        </Suspense>
        
        {/* 訪客分析組件 - 延遲載入 */}
        <Suspense fallback={null}>
          <VisitorAnalytics />
        </Suspense>
        
        {/* 多語言音頻播放器 - 自動根據語言切換 
        <AudioPlayer />  */}
      </div>
    </LanguageProvider>
  )
}

export default App



================================================================
File Path: src/index.css
================================================================

@tailwind base;
@tailwind components;
@tailwind utilities;

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animate-fadeIn {
  animation: fadeIn 0.3s ease-in-out;
}

/* 自定義動畫 */
@keyframes fade-in {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in {
  animation: fade-in 0.3s ease-out;
}

/* 聊天機器人樣式增強 */
.chat-message {
  word-wrap: break-word;
  overflow-wrap: break-word;
}

/* 滾動條樣式 */
.overflow-y-auto::-webkit-scrollbar {
  width: 4px;
}

.overflow-y-auto::-webkit-scrollbar-track {
  background: #f1f5f9;
}

.overflow-y-auto::-webkit-scrollbar-thumb {
  background: #cbd5e1;
  border-radius: 2px;
}

.overflow-y-auto::-webkit-scrollbar-thumb:hover {
  background: #94a3b8;
}

/* 響應式調整 */
@media (max-width: 640px) {
  .chat-container {
    width: calc(100vw - 1.5rem);
    height: calc(100vh - 3rem);
    bottom: 0;
    right: 0;
    border-radius: 0;
  }
}

/* 文字選取樣式 */
::selection {
  background-color: #10b981;
  color: white;
}

/* 專用於聊天訊息的樣式 */
.chat-message-content {
  line-height: 1.5;
  font-size: 14px;
}

.chat-message-content strong {
  font-weight: 600;
  color: #374151;
}

.chat-message-content em {
  font-style: italic;
  color: #6b7280;
}
 



================================================================
File Path: src/main.tsx
================================================================

import { createRoot } from "react-dom/client"
import App from "./App.tsx"
import "./index.css"

createRoot(document.getElementById("root")!).render(
  <App />,
)
 



================================================================
File Path: src/vite-env.d.ts
================================================================

/// <reference types="vite/client" /> 



================================================================
File Path: src/components/AboutSection.tsx
================================================================

import React from 'react'
import {Award, Users, Clock} from 'lucide-react'
import { useLanguage } from '../contexts/LanguageContext'

const AboutSection: React.FC = () => {
  const { t } = useLanguage()

  const stats = [
    {
      icon: <Award className="w-8 h-8 text-emerald-600" />,
      title: t('about.experience'),
      description: t('about.experienceDesc')
    },
    {
      icon: <Users className="w-8 h-8 text-emerald-600" />,
      title: t('about.projects'),
      description: t('about.projectsDesc')
    },
    {
      icon: <Clock className="w-8 h-8 text-emerald-600" />,
      title: t('about.support'),
      description: t('about.supportDesc')
    }
  ]

  return (
    <section id="about" className="py-20 bg-white">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div className="animate-on-scroll">
            <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
              {t('about.title')}
            </h2>
            <h3 className="text-xl text-emerald-600 font-semibold mb-6">
              {t('about.subtitle')}
            </h3>
            <p className="text-lg text-gray-600 leading-relaxed mb-8">
              {t('about.description')}
            </p>
            
            <div className="grid grid-cols-1 sm:grid-cols-3 gap-6">
              {stats.map((stat, index) => (
                <div key={index} className="text-center p-4">
                  <div className="flex justify-center mb-3">{stat.icon}</div>
                  <h4 className="font-semibold text-gray-900 mb-2">{stat.title}</h4>
                  <p className="text-sm text-gray-600">{stat.description}</p>
                </div>
              ))}
            </div>
          </div>

          <div className="animate-on-scroll">
            <img
              src="https://i.ibb.co/HLz737Jn/5.webp"
              className="rounded-xl shadow-lg w-full h-auto"
            />
          </div>
        </div>
      </div>
    </section>
  )
}

export default AboutSection 



================================================================
File Path: src/components/AdminLogin.tsx
================================================================

import React, { useState } from "react";
import { supabase } from "../lib/supabase";

interface AdminLoginProps {
  onSuccess: () => void;
  onClose: () => void;
}

const AdminLogin: React.FC<AdminLoginProps> = ({ onSuccess, onClose }) => {
  const [username, setUsername] = useState("");
  const [password, setPassword] = useState("");
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState("");
  const [showPassword, setShowPassword] = useState(false);

  const handleLogin = async (e: React.FormEvent) => {
    e.preventDefault();
    setError("");
    setLoading(true);

    try {
      if (!username.trim() || !password.trim()) {
        setError("請輸入用戶名和密碼");
        setLoading(false);
        return;
      }

      // 呼叫 Supabase RPC Function (移除 IP，改用 Supabase 伺服器端取得)
      const { data, error: rpcError } = await supabase
        .rpc("admin_login", {
          input_username: username.trim(),
          input_password: password,
          client_user_agent: navigator.userAgent
        });

      if (rpcError) {
        console.error("RPC Error:", rpcError);
        setError("登入過程發生錯誤,請稍後再試");
        setLoading(false);
        return;
      }

      if (!data.success) {
        setError(data.message || "用戶名或密碼錯誤");
        setLoading(false);
        return;
      }

      const sessionToken = crypto.randomUUID();
      const expiryTime = Date.now() + 10 * 60 * 1000;

      sessionStorage.setItem("admin_session_token", sessionToken);
      sessionStorage.setItem("admin_session_expiry", expiryTime.toString());
      sessionStorage.setItem("admin_username", username);

      onSuccess();
    } catch (err) {
      console.error("Login error:", err);
      setError("登入過程發生錯誤,請稍後再試");
    } finally {
      setLoading(false);
    }
  };

  return (
    <div className="fixed inset-0 bg-black/70 backdrop-blur-sm z-[100] flex items-center justify-center p-4">
      <div className="bg-gradient-to-br from-gray-900 to-gray-800 text-white rounded-2xl shadow-2xl max-w-md w-full p-8 border border-emerald-500/30 animate-fade-in">
        <div className="flex justify-between items-center mb-6">
          <div className="flex items-center gap-3">
            <div className="w-12 h-12 bg-emerald-500/20 rounded-full flex items-center justify-center">
              <svg className="w-6 h-6 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
              </svg>
            </div>
            <h2 className="text-2xl font-bold">管理員登入</h2>
          </div>
          <button
            onClick={onClose}
            className="text-gray-400 hover:text-white transition-colors"
          >
            <svg className="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>

        <form onSubmit={handleLogin} className="space-y-5">
          <div>
            <label htmlFor="username" className="block text-sm font-medium text-gray-300 mb-2">
              用戶名
            </label>
            <div className="relative">
              <div className="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                <svg className="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                </svg>
              </div>
              <input
                id="username"
                type="text"
                value={username}
                onChange={(e) => setUsername(e.target.value)}
                className="w-full pl-10 pr-4 py-3 bg-gray-800 border border-gray-700 rounded-xl text-white placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-transparent transition-all"
                placeholder="請輸入用戶名"
                disabled={loading}
                autoComplete="username"
              />
            </div>
          </div>

          <div>
            <label htmlFor="password" className="block text-sm font-medium text-gray-300 mb-2">
              密碼
            </label>
            <div className="relative">
              <div className="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                <svg className="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z" />
                </svg>
              </div>
              <input
                id="password"
                type={showPassword ? "text" : "password"}
                value={password}
                onChange={(e) => setPassword(e.target.value)}
                className="w-full pl-10 pr-12 py-3 bg-gray-800 border border-gray-700 rounded-xl text-white placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-transparent transition-all"
                placeholder="請輸入密碼"
                disabled={loading}
                autoComplete="current-password"
              />
              <button
                type="button"
                onClick={() => setShowPassword(!showPassword)}
                className="absolute inset-y-0 right-0 pr-3 flex items-center text-gray-400 hover:text-white transition-colors"
              >
                {showPassword ? (
                  <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13.875 18.825A10.05 10.05 0 0112 19c-4.478 0-8.268-2.943-9.543-7a9.97 9.97 0 011.563-3.029m5.858.908a3 3 0 114.243 4.243M9.878 9.878l4.242 4.242M9.88 9.88l-3.29-3.29m7.532 7.532l3.29 3.29M3 3l3.59 3.59m0 0A9.953 9.953 0 0112 5c4.478 0 8.268 2.943 9.543 7a10.025 10.025 0 01-4.132 5.411m0 0L21 21" />
                  </svg>
                ) : (
                  <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                  </svg>
                )}
              </button>
            </div>
          </div>

          {error && (
            <div className="bg-red-500/10 border border-red-500/30 rounded-xl p-3 flex items-start gap-2">
              <svg className="w-5 h-5 text-red-400 flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <p className="text-red-400 text-sm">{error}</p>
            </div>
          )}

          <button
            type="submit"
            disabled={loading}
            className="w-full bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-600 hover:to-teal-700 text-white px-6 py-3 rounded-xl font-semibold transition-all duration-300 hover:scale-105 shadow-lg disabled:opacity-50 disabled:cursor-not-allowed disabled:hover:scale-100 flex items-center justify-center gap-2"
          >
            {loading ? (
              <>
                <svg className="animate-spin h-5 w-5" fill="none" viewBox="0 0 24 24">
                  <circle className="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" strokeWidth="4"></circle>
                  <path className="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                </svg>
                登入中...
              </>
            ) : (
              <>
                <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M11 16l-4-4m0 0l4-4m-4 4h14m-5 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h7a3 3 0 013 3v1" />
                </svg>
                登入
              </>
            )}
          </button>
        </form>
      </div>

      <style>{`
        @keyframes fade-in {
          from {
            opacity: 0;
            transform: scale(0.95);
          }
          to {
            opacity: 1;
            transform: scale(1);
          }
        }
        .animate-fade-in {
          animation: fade-in 0.3s ease-out;
        }
      `}</style>
    </div>
  );
};

export default AdminLogin;


================================================================
File Path: src/components/AnalyticsCharts.tsx
================================================================

import React from "react";
import { ChartData, CountryData, TimeRange, VisitorLog, ComparisonStats, COUNTRY_NAME_MAP, WORLD_MAP_PATHS } from "../constants/analyticsConstants";

interface AnalyticsChartsProps {
  visitors: VisitorLog[];
  chartData: ChartData[];
  countryData: CountryData[];
  timeRange: TimeRange;
  setTimeRange: (range: TimeRange) => void;
  loading: boolean;
  totalVisits: number;
  uniqueVisitors: number;
  comparisonStats: ComparisonStats | null;
  reachedMilestone: number | null;
  exportToXLSX: () => void;
  hoveredCountry: string | null;
  setHoveredCountry: (country: string | null) => void;
}

export const AnalyticsCharts: React.FC<AnalyticsChartsProps> = ({
  visitors,
  chartData,
  countryData,
  timeRange,
  setTimeRange,
  loading,
  totalVisits,
  uniqueVisitors,
  comparisonStats,
  reachedMilestone,
  exportToXLSX,
  hoveredCountry,
  setHoveredCountry,
}) => {
  const normalizeCountryName = (country: string): string => {
    return COUNTRY_NAME_MAP[country] || country;
  };

  // ✅ 修改：淺綠色 → 黃色 → 橘色 → 紅色
  const getCountryColor = (country: string): string => {
    const normalizedCountry = normalizeCountryName(country);
    const data = countryData.find((c) => normalizeCountryName(c.country) === normalizedCountry);
    if (!data) return "#374151"; // 深灰色（無數據）

    const maxCount = Math.max(...countryData.map((c) => c.count), 1);
    const intensity = data.count / maxCount;

    if (intensity > 0.7) return "#dc2626"; // 紅色（熱區）
    if (intensity > 0.4) return "#f97316"; // 橘色（頻繁）
    if (intensity > 0.2) return "#eab308"; // 黃色（中等）
    return "#86efac"; // 淺綠色（一般）
  };

  const maxCount = Math.max(
    ...chartData.map((d) => Math.max(d.count, d.compareCount || 0)),
    1
  );

  return (
    <>
      {/* 統計卡片區 */}
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
        <div className="bg-gradient-to-br from-blue-500/20 to-blue-600/20 p-6 rounded-xl border border-blue-500/30">
          <div className="text-blue-400 text-sm mb-2">總訪問次數</div>
          <div className="text-4xl font-bold">{totalVisits}</div>
          {comparisonStats && (
            <div className={`text-xs mt-2 ${
              comparisonStats.changeType === "increase" ? "text-green-400" : 
              comparisonStats.changeType === "decrease" ? "text-red-400" : "text-gray-400"
            }`}>
              {comparisonStats.changeType === "increase" ? "↑" : 
               comparisonStats.changeType === "decrease" ? "↓" : "→"} 
              {Math.abs(comparisonStats.changePercent).toFixed(1)}% vs 上期
            </div>
          )}
        </div>

        <div className="bg-gradient-to-br from-emerald-500/20 to-emerald-600/20 p-6 rounded-xl border border-emerald-500/30">
          <div className="text-emerald-400 text-sm mb-2">獨立訪客</div>
          <div className="text-4xl font-bold">{uniqueVisitors}</div>
          <div className="text-xs text-gray-400 mt-2">來自 {countryData.length} 個國家</div>
        </div>

        <div className="bg-gradient-to-br from-purple-500/20 to-purple-600/20 p-6 rounded-xl border border-purple-500/30">
          <div className="text-purple-400 text-sm mb-2">時間範圍</div>
          <select
            value={timeRange}
            onChange={(e) => setTimeRange(e.target.value as TimeRange)}
            className="bg-gray-700 text-white px-4 py-2 rounded-lg text-sm w-full"
          >
            <option value="week">最近 7 天</option>
            <option value="twoWeeks">最近 14 天</option>  {/* ✅ 新增 */}
            <option value="month">最近 30 天</option>
            <option value="year">最近 1 年</option>
          </select>
          {reachedMilestone && (
            <div className="text-xs text-yellow-400 mt-2">
              🎉 達成 {reachedMilestone} 訪客里程碑！
            </div>
          )}
        </div>
      </div>

      {/* 地圖區 + 匯出按鈕 */}
      <div className="bg-gray-800 p-6 rounded-xl">
        <div className="flex justify-between items-center mb-4">
          <h3 className="text-lg font-semibold">全球訪客分佈 (支援 195+ 國家)</h3>
          <button
            onClick={exportToXLSX}
            className="flex items-center gap-2 px-4 py-2 bg-emerald-600 text-white rounded-lg hover:bg-emerald-700 transition-colors"
          >
            <svg className="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
            </svg>
            匯出 Excel
          </button>
        </div>

        {loading ? (
          <div className="flex justify-center items-center h-64">
            <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-emerald-500"></div>
          </div>
        ) : (
          <div className="relative">
            <svg
              viewBox="0 0 900 500"
              className="w-full h-auto"
              style={{ maxHeight: "400px" }}
            >
              <rect width="900" height="500" fill="#1f2937" />
              
              {Object.entries(WORLD_MAP_PATHS).map(([country, path]) => {
                const color = getCountryColor(country);
                const normalizedCountry = normalizeCountryName(country);
                const matchedData = countryData.find((c) => normalizeCountryName(c.country) === normalizedCountry);
                
                return (
                  <path
                    key={country}
                    d={path}
                    fill={color}
                    stroke="#374151"
                    strokeWidth="1"
                    className="transition-all duration-300 cursor-pointer hover:opacity-80"
                    onMouseEnter={() => setHoveredCountry(matchedData ? matchedData.country : country)}
                    onMouseLeave={() => setHoveredCountry(null)}
                  />
                );
              })}
            </svg>

            {hoveredCountry && (
              <div className="absolute top-4 left-4 bg-gray-900 border border-emerald-500 rounded-lg p-3 shadow-xl z-20">
                <div className="font-semibold text-emerald-400">{hoveredCountry}</div>
                {countryData.find((c) => c.country === hoveredCountry) && (
                  <div className="text-sm text-gray-300 mt-1">
                    訪問次數: {countryData.find((c) => c.country === hoveredCountry)?.count || 0}
                    <br />
                    訪客數: {countryData.find((c) => c.country === hoveredCountry)?.visitors || 0}
                  </div>
                )}
              </div>
            )}

            {/* ✅ 修改：圖例顏色 */}
            <div className="flex items-center gap-4 mt-4 text-sm">
              <span className="text-gray-400">訪問密度:</span>
              <div className="flex items-center gap-2">
                <div className="w-6 h-4 bg-[#86efac] rounded"></div>
                <span className="text-gray-400">一般</span>
              </div>
              <div className="flex items-center gap-2">
                <div className="w-6 h-4 bg-[#eab308] rounded"></div>
                <span className="text-gray-400">中等</span>
              </div>
              <div className="flex items-center gap-2">
                <div className="w-6 h-4 bg-[#f97316] rounded"></div>
                <span className="text-gray-400">頻繁</span>
              </div>
              <div className="flex items-center gap-2">
                <div className="w-6 h-4 bg-[#dc2626] rounded"></div>
                <span className="text-gray-400">熱區</span>
              </div>
            </div>
            
            {countryData.length > 0 && (
              <div className="mt-4 p-3 bg-gray-900 rounded-lg text-xs">
                <div className="font-semibold text-emerald-400 mb-2">
                  數據庫中的國家 ({countryData.length}) | 地圖支援: {Object.keys(WORLD_MAP_PATHS).length} 個國家
                </div>
                <div className="flex flex-wrap gap-2">
                  {countryData.map((c) => {
                    const normalized = normalizeCountryName(c.country);
                    const hasMap = WORLD_MAP_PATHS.hasOwnProperty(normalized);
                    return (
                      <span
                        key={c.country}
                        className={`px-2 py-1 rounded ${
                          hasMap ? "bg-green-900 text-green-300" : "bg-red-900 text-red-300"
                        }`}
                        title={hasMap ? "已匹配" : "未匹配地圖"}
                      >
                        {c.country} {!hasMap && "❌"}
                      </span>
                    );
                  })}
                </div>
              </div>
            )}
          </div>
        )}
      </div>

      <div className="bg-gray-800 p-6 rounded-xl">
        <h3 className="text-lg font-semibold mb-4">國家訪問排行</h3>
        <div className="space-y-3">
          {countryData.slice(0, 5).map((country, index) => {
            const maxCountryCount = countryData[0]?.count || 1;
            const percentage = (country.count / maxCountryCount) * 100;
            
            return (
              <div key={country.country} className="space-y-1">
                <div className="flex justify-between items-center text-sm">
                  <div className="flex items-center gap-2">
                    <span className="text-emerald-400 font-bold">#{index + 1}</span>
                    <span>{country.country}</span>
                  </div>
                  <div className="text-gray-400">
                    {country.count} 次訪問 · {country.visitors} 訪客
                  </div>
                </div>
                <div className="w-full bg-gray-700 rounded-full h-2">
                  <div
                    className="bg-gradient-to-r from-emerald-500 to-teal-500 h-2 rounded-full transition-all duration-500"
                    style={{ width: `${percentage}%` }}
                  ></div>
                </div>
              </div>
            );
          })}
        </div>
      </div>

      <div className="bg-gray-800 p-6 rounded-xl">
        <div className="flex justify-between items-center mb-4">
          <h3 className="text-lg font-semibold">訪問趨勢對比</h3>
          <div className="flex gap-4 text-sm">
            <div className="flex items-center gap-2">
              <div className="w-4 h-4 bg-gradient-to-t from-emerald-600 to-teal-500 rounded"></div>
              <span className="text-gray-400">當前期間</span>
            </div>
            <div className="flex items-center gap-2">
              <div className="w-4 h-4 bg-gradient-to-t from-orange-600 to-yellow-500 rounded"></div>
              <span className="text-gray-400">對比期間</span>
            </div>
          </div>
        </div>
        {loading ? (
          <div className="flex justify-center items-center h-64">
            <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-emerald-500"></div>
          </div>
        ) : (
          <div className="h-64 flex items-end justify-between gap-1">
            {chartData.map((item, index) => (
              <div
                key={index}
                className="flex-1 flex flex-col items-center group"
              >
                <div className="relative w-full flex gap-0.5">
                  <div
                    className="flex-1 bg-gradient-to-t from-emerald-600 to-teal-500 rounded-t transition-all duration-300 hover:from-emerald-500 hover:to-teal-400 cursor-pointer"
                    style={{
                      height: `${(item.count / maxCount) * 200}px`,
                      minHeight: "4px",
                    }}
                  >
                    <div className="absolute -top-16 left-1/2 transform -translate-x-1/2 bg-gray-900 px-2 py-1 rounded text-xs opacity-0 group-hover:opacity-100 transition-opacity whitespace-nowrap z-10">
                      當前: {item.count} 次<br/>
                      對比: {item.compareCount || 0} 次
                    </div>
                  </div>
                  <div
                    className="flex-1 bg-gradient-to-t from-orange-600 to-yellow-500 rounded-t transition-all duration-300 opacity-60 hover:opacity-80 cursor-pointer"
                    style={{
                      height: `${((item.compareCount || 0) / maxCount) * 200}px`,
                      minHeight: "4px",
                    }}
                  ></div>
                </div>
                <div className="text-xs text-gray-400 mt-2 transform -rotate-45 origin-left whitespace-nowrap">
                  {item.date}
                </div>
              </div>
            ))}
          </div>
        )}
      </div>
    </>
  );
};


================================================================
File Path: src/components/AnalyticsTabContent.tsx
================================================================

import React from "react";
import { OperationLog, OperationStats } from "../constants/analyticsConstants";

interface OperationsTabProps {
  operationStats: OperationStats | null;
  operationLogs: OperationLog[];
  logsLoading: boolean;
  logFilter: string | null;
  setLogFilter: (filter: string | null) => void;
}

export const OperationsTab: React.FC<OperationsTabProps> = ({
  operationStats,
  operationLogs,
  logsLoading,
  logFilter,
  setLogFilter,
}) => {
  return (
    <>
      {operationStats && (
        <div className="grid grid-cols-3 gap-4">
          <div className="bg-gradient-to-br from-blue-500/20 to-blue-600/20 p-6 rounded-xl border border-blue-500/30">
            <div className="text-blue-400 text-sm mb-2">總操作數</div>
            <div className="text-4xl font-bold">{operationStats.total_operations}</div>
            <div className="text-xs text-gray-400 mt-2">最近 7 天: {operationStats.last_7_days}</div>
          </div>
          <div className="bg-gradient-to-br from-green-500/20 to-green-600/20 p-6 rounded-xl border border-green-500/30">
            <div className="text-green-400 text-sm mb-2">成功登入</div>
            <div className="text-4xl font-bold">{operationStats.login_success}</div>
            <div className="text-xs text-gray-400 mt-2">今日: {operationStats.today_operations}</div>
          </div>
          <div className="bg-gradient-to-br from-red-500/20 to-red-600/20 p-6 rounded-xl border border-red-500/30">
            <div className="text-red-400 text-sm mb-2">失敗/阻擋</div>
            <div className="text-4xl font-bold">{operationStats.login_failed + operationStats.login_blocked}</div>
            <div className="text-xs text-gray-400 mt-2">失敗: {operationStats.login_failed} | 阻擋: {operationStats.login_blocked}</div>
          </div>
        </div>
      )}

      <div className="bg-gray-800 p-6 rounded-xl">
        <div className="flex justify-between items-center mb-4">
          <h3 className="text-lg font-semibold">操作記錄</h3>
          <div className="flex gap-2">
            <button
              onClick={() => setLogFilter(null)}
              className={`px-3 py-1 rounded-lg text-sm transition-all ${
                logFilter === null
                  ? "bg-emerald-600 text-white"
                  : "bg-gray-700 text-gray-400 hover:bg-gray-600"
              }`}
            >
              全部
            </button>
            <button
              onClick={() => setLogFilter("login_success")}
              className={`px-3 py-1 rounded-lg text-sm transition-all ${
                logFilter === "login_success"
                  ? "bg-green-600 text-white"
                  : "bg-gray-700 text-gray-400 hover:bg-gray-600"
              }`}
            >
              成功
            </button>
            <button
              onClick={() => setLogFilter("login_failed")}
              className={`px-3 py-1 rounded-lg text-sm transition-all ${
                logFilter === "login_failed"
                  ? "bg-red-600 text-white"
                  : "bg-gray-700 text-gray-400 hover:bg-gray-600"
              }`}
            >
              失敗
            </button>
            <button
              onClick={() => setLogFilter("login_blocked")}
              className={`px-3 py-1 rounded-lg text-sm transition-all ${
                logFilter === "login_blocked"
                  ? "bg-orange-600 text-white"
                  : "bg-gray-700 text-gray-400 hover:bg-gray-600"
              }`}
            >
              阻擋
            </button>
          </div>
        </div>

        {logsLoading ? (
          <div className="flex justify-center items-center h-64">
            <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-emerald-500"></div>
          </div>
        ) : (
          <div className="overflow-x-auto">
            <table className="w-full text-sm">
              <thead>
                <tr className="border-b border-gray-700">
                  <th className="text-left py-3 px-2">時間</th>
                  <th className="text-left py-3 px-2">帳號</th>
                  <th className="text-left py-3 px-2">操作類型</th>
                  <th className="text-left py-3 px-2">詳情</th>
                  <th className="text-left py-3 px-2">IP 地址</th>
                </tr>
              </thead>
              <tbody>
                {operationLogs.length === 0 ? (
                  <tr>
                    <td colSpan={5} className="text-center py-8 text-gray-500">
                      暫無操作記錄
                    </td>
                  </tr>
                ) : (
                  operationLogs.map((log) => (
                    <tr
                      key={log.id}
                      className="border-b border-gray-700/50 hover:bg-gray-700/30 transition-colors"
                    >
                      <td className="py-3 px-2 text-xs text-gray-400">
                        {new Date(log.created_at).toLocaleString("zh-TW")}
                      </td>
                      <td className="py-3 px-2 font-semibold">
                        {log.username}
                      </td>
                      <td className="py-3 px-2">
                        <span
                          className={`px-2 py-1 rounded text-xs font-semibold ${
                            log.operation_type === "login_success"
                              ? "bg-green-600 text-white"
                              : log.operation_type === "login_failed"
                              ? "bg-red-600 text-white"
                              : log.operation_type === "login_blocked"
                              ? "bg-orange-600 text-white"
                              : "bg-gray-600 text-white"
                          }`}
                        >
                          {log.operation_type === "login_success" && "✓ 登入成功"}
                          {log.operation_type === "login_failed" && "✗ 登入失敗"}
                          {log.operation_type === "login_blocked" && "🚫 登入阻擋"}
                          {!log.operation_type.startsWith("login") && log.operation_type}
                        </span>
                      </td>
                      <td className="py-3 px-2 text-xs text-gray-400">
                        {log.operation_detail}
                      </td>
                      <td className="py-3 px-2 font-mono text-xs">
                        {log.ip_address}
                      </td>
                    </tr>
                  ))
                )}
              </tbody>
            </table>
          </div>
        )}
      </div>
    </>
  );
};



================================================================
File Path: src/components/AudioPlayer.tsx
================================================================

import React, { useState, useEffect, useRef } from "react";
import { Volume2, VolumeX, Play, Pause, Maximize2 } from 'lucide-react';
import { useLanguage } from "../contexts/LanguageContext";
import { createPortal } from 'react-dom';

export const AudioPlayer: React.FC = () => {
  const { t, getAudioUrl, language } = useLanguage()
  const audioRef = useRef<HTMLAudioElement>(null)
  
  const [showPrompt, setShowPrompt] = useState(false)
  const [isMinimized, setIsMinimized] = useState(true)
  const [isPlaying, setIsPlaying] = useState(false)
  const [currentTime, setCurrentTime] = useState(0)
  const [duration, setDuration] = useState(0)
  const [volume, setVolume] = useState(0.7)
  const [isMuted, setIsMuted] = useState(false)
  const [isDragging, setIsDragging] = useState(false)
  const [currentAudioUrl, setCurrentAudioUrl] = useState(getAudioUrl())

  // 監聽語言切換，更新音頻 URL
  useEffect(() => {
    const newAudioUrl = getAudioUrl()
    if (newAudioUrl !== currentAudioUrl) {
      const wasPlaying = isPlaying
      const currentPosition = currentTime
      
      // 暫停當前播放
      if (audioRef.current) {
        audioRef.current.pause()
      }
      
      // 更新 URL
      setCurrentAudioUrl(newAudioUrl)
      setIsPlaying(false)
      setCurrentTime(0)
      
      // 如果之前正在播放，載入新音頻後繼續播放
      if (wasPlaying && audioRef.current) {
        audioRef.current.load()
        audioRef.current.play().then(() => {
          setIsPlaying(true)
        }).catch((error) => {
          console.error("語言切換後播放失敗:", error)
        })
      }
    }
  }, [language, getAudioUrl, currentAudioUrl, isPlaying, currentTime])


  // 首次訪問提示邏輯
  useEffect(() => {
    const promptSeen = localStorage.getItem("audioPromptSeen");
    const playerMinimized = localStorage.getItem("audioPlayerMinimized");

    if (playerMinimized === "false") {
      setIsMinimized(false);
    }

    if (!promptSeen) {
      const timer = setTimeout(() => {
        setShowPrompt(true);
      }, 2000);
      return () => clearTimeout(timer);
    }
  }, []);

  // 音頻事件監聽
  useEffect(() => {
    const audio = audioRef.current;
    if (!audio) return;

    const handleLoadedMetadata = () => {
      if (audio.duration && !isNaN(audio.duration) && isFinite(audio.duration)) {
        setDuration(audio.duration);
      }
    };

    const handleCanPlay = () => {
      if (audio.duration && !isNaN(audio.duration) && isFinite(audio.duration)) {
        setDuration(audio.duration);
      }
    };

    const handleTimeUpdate = () => {
      if (!isDragging) {
        setCurrentTime(audio.currentTime);
      }
    };

    const handleEnded = () => {
      setIsPlaying(false);
      setCurrentTime(0);
    };

    audio.addEventListener("loadedmetadata", handleLoadedMetadata);
    audio.addEventListener("canplay", handleCanPlay);
    audio.addEventListener("timeupdate", handleTimeUpdate);
    audio.addEventListener("ended", handleEnded);

    return () => {
      audio.removeEventListener("loadedmetadata", handleLoadedMetadata);
      audio.removeEventListener("canplay", handleCanPlay);
      audio.removeEventListener("timeupdate", handleTimeUpdate);
      audio.removeEventListener("ended", handleEnded);
    };
  }, [isDragging]);

  // 音量控制
  useEffect(() => {
    if (audioRef.current) {
      audioRef.current.volume = isMuted ? 0 : volume;
    }
  }, [volume, isMuted]);

  const handleStartListening = async () => {
    setShowPrompt(false);
    setIsMinimized(false);
    localStorage.setItem("audioPromptSeen", "true");
    localStorage.setItem("audioPlayerMinimized", "false");

    // 強制載入音頻
    if (audioRef.current) {
      audioRef.current.load();
      try {
        await audioRef.current.play();
        setIsPlaying(true);
      } catch (error) {
        console.error("播放失敗:", error);
      }
    }
  };

  const handleDecline = () => {
    setShowPrompt(false);
    setIsMinimized(true);
    localStorage.setItem("audioPromptSeen", "true");
    localStorage.setItem("audioPlayerMinimized", "true");
  };

  const togglePlay = async () => {
    if (!audioRef.current) return;

    try {
      if (isPlaying) {
        audioRef.current.pause();
        setIsPlaying(false);
      } else {
        await audioRef.current.play();
        setIsPlaying(true);
      }
    } catch (error) {
      console.error("播放操作失敗:", error);
    }
  };

  const handleProgressChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    const newTime = parseFloat(e.target.value);
    setCurrentTime(newTime);
    if (audioRef.current) {
      audioRef.current.currentTime = newTime;
    }
  };

  const handleVolumeChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    const newVolume = parseFloat(e.target.value);
    setVolume(newVolume);
    setIsMuted(false);
  };

  const toggleMute = () => {
    setIsMuted(!isMuted);
  };

  const handleMinimize = () => {
    setIsMinimized(true);
    localStorage.setItem("audioPlayerMinimized", "true");
  };

  const handleExpand = () => {
    setIsMinimized(false);
    localStorage.setItem("audioPlayerMinimized", "false");
  };

  const formatTime = (time: number): string => {
    if (!time || isNaN(time) || !isFinite(time)) return "0:00";
    const minutes = Math.floor(time / 60);
    const seconds = Math.floor(time % 60);
    return `${minutes}:${seconds.toString().padStart(2, "0")}`;
  };

  console.log('AudioPlayer 狀態:', { showPrompt, isMinimized })

  return (
    <>
      <audio
        ref={audioRef}
        src={currentAudioUrl}
        preload="metadata"
      />

      {/* 首次訪問提示卡片 - 使用 Portal 渲染到 body */}
      {showPrompt && createPortal(
        <div className="fixed bottom-24 right-6 z-[60] w-80 bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl p-6 animate-[slideUp_0.5s_ease-out]">
          <div className="flex items-start gap-3 mb-4">
            <div className="w-12 h-12 bg-gradient-to-br from-emerald-500 to-teal-500 rounded-full flex items-center justify-center flex-shrink-0">
              <Volume2 className="w-6 h-6 text-white" />
            </div>
            <div>
              <h3 className="font-bold text-gray-800 text-lg mb-1">
                {t("audio.promptTitle")}
              </h3>
              <p className="text-sm text-gray-600">{t("audio.promptSubtitle")}</p>
            </div>
          </div>
          <div className="flex gap-2">
            <button
              onClick={handleStartListening}
              className="flex-1 bg-gradient-to-r from-emerald-500 to-teal-500 text-white py-2.5 px-4 rounded-lg font-medium hover:from-emerald-600 hover:to-teal-600 transition-all"
            >
              {t("audio.startListening")}
            </button>
            <button
              onClick={handleDecline}
              className="flex-1 bg-gray-200 text-gray-700 py-2.5 px-4 rounded-lg font-medium hover:bg-gray-300 transition-all"
            >
              {t("audio.decline")}
            </button>
          </div>
        </div>,
        document.body
      )}

      {/* 音頻播放器 - 永遠顯示 */}
      {isMinimized ? (
        /* 最小化狀態 - 內聯在 Navbar 中 */
        <div className="flex items-center gap-2 ml-4">
          {/* 播放/暫停按鈕 */}
          <button
            onClick={togglePlay}
            className="w-8 h-8 bg-gradient-to-r from-emerald-500 to-teal-500 rounded-full flex items-center justify-center hover:from-emerald-600 hover:to-teal-600 transition-all shadow-lg"
            title={isPlaying ? t("audio.pause") : t("audio.play")}
          >
            {isPlaying ? (
              <Pause className="w-4 h-4 text-white" />
            ) : (
              <Play className="w-4 h-4 text-white ml-0.5" />
            )}
          </button>

          {/* 展開按鈕 */}
          <button
            onClick={handleExpand}
            className="w-8 h-8 bg-white/10 hover:bg-white/20 rounded-full flex items-center justify-center transition-all"
            title={t("audio.expand")}
          >
            <Maximize2 className="w-4 h-4 text-white" />
          </button>

          {/* 音樂波形動畫 */}
          {isPlaying && (
            <div className="flex items-center gap-1 h-6">
              {[1, 2, 3].map((i) => (
                <div
                  key={i}
                  className="w-1 bg-emerald-400 rounded-full animate-pulse"
                  style={{
                    height: `${Math.random() * 16 + 8}px`,
                    animationDelay: `${i * 0.15}s`,
                    animationDuration: '0.6s'
                  }}
                />
              ))}
            </div>
          )}
        </div>
      ) : (
        /* 完整播放器 - 固定在右上角 */
        <div className="fixed top-20 right-6 z-40 w-80 md:w-96 bg-white/95 backdrop-blur-sm rounded-2xl shadow-2xl p-6 animate-[fadeIn_0.3s_ease-out]">
          {/* 頂部控制按鈕 */}
          <div className="flex justify-between items-center mb-4">
            <h3 className="font-bold text-gray-800 text-lg">
              {t("audio.title")}
            </h3>
            <button
              onClick={handleMinimize}
              className="text-emerald-500 hover:text-emerald-600 transition-colors"
              title={t("audio.minimize")}
            >
              <Maximize2 className="w-5 h-5 rotate-180" />
            </button>
          </div>

          {/* 播放按鈕 */}
          <div className="flex items-center gap-4 mb-4">
            <button
              onClick={togglePlay}
              className="w-14 h-14 bg-gradient-to-r from-emerald-500 to-teal-500 rounded-full flex items-center justify-center hover:from-emerald-600 hover:to-teal-600 transition-all shadow-lg"
            >
              {isPlaying ? (
                <Pause className="w-6 h-6 text-white" />
              ) : (
                <Play className="w-6 h-6 text-white ml-1" />
              )}
            </button>
            <div className="flex-1">
              <div className="text-sm text-gray-600 mb-1">
                {formatTime(currentTime)} / {formatTime(duration)}
              </div>
              <input
                type="range"
                min="0"
                max={duration || 0}
                value={currentTime}
                onChange={handleProgressChange}
                onMouseDown={() => setIsDragging(true)}
                onMouseUp={() => setIsDragging(false)}
                className="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer audio-progress-bar"
                style={{
                  background: `linear-gradient(to right, #10b981 0%, #10b981 ${
                    duration ? (currentTime / duration) * 100 : 0
                  }%, #e5e7eb ${duration ? (currentTime / duration) * 100 : 0}%, #e5e7eb 100%)`
                }}
              />
            </div>
          </div>

          {/* 音量控制 */}
          <div className="flex items-center gap-3">
            <button
              onClick={toggleMute}
              className="text-gray-600 hover:text-emerald-500 transition-colors"
            >
              {isMuted || volume === 0 ? (
                <VolumeX className="w-5 h-5" />
              ) : (
                <Volume2 className="w-5 h-5" />
              )}
            </button>
            <input
              type="range"
              min="0"
              max="1"
              step="0.01"
              value={isMuted ? 0 : volume}
              onChange={handleVolumeChange}
              className="flex-1 h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer audio-volume-bar"
              style={{
                background: `linear-gradient(to right, #10b981 0%, #10b981 ${
                  (isMuted ? 0 : volume) * 100
                }%, #e5e7eb ${(isMuted ? 0 : volume) * 100}%, #e5e7eb 100%)`
              }}
            />
          </div>
        </div>
      )}

      <style>{`
        @keyframes fadeIn {
          from {
            opacity: 0;
            transform: scale(0.9);
          }
          to {
            opacity: 1;
            transform: scale(1);
          }
        }

        @keyframes slideUp {
          from {
            opacity: 0;
            transform: translateY(20px);
          }
          to {
            opacity: 1;
            transform: translateY(0);
          }
        }

        .audio-progress-bar::-webkit-slider-thumb {
          appearance: none;
          width: 16px;
          height: 16px;
          border-radius: 50%;
          background: #10b981;
          cursor: pointer;
          box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .audio-progress-bar::-moz-range-thumb {
          width: 16px;
          height: 16px;
          border-radius: 50%;
          background: #10b981;
          cursor: pointer;
          border: none;
          box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .audio-volume-bar::-webkit-slider-thumb {
          appearance: none;
          width: 14px;
          height: 14px;
          border-radius: 50%;
          background: #10b981;
          cursor: pointer;
          box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .audio-volume-bar::-moz-range-thumb {
          width: 14px;
          height: 14px;
          border-radius: 50%;
          background: #10b981;
          cursor: pointer;
          border: none;
          box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
      `}</style>
    </>
  );
};



================================================================
File Path: src/components/ContactSection.tsx
================================================================


import React, { useState } from 'react'
import {Mail, Phone, MapPin, Send} from 'lucide-react'
import { useLanguage } from '../contexts/LanguageContext'

const ContactSection: React.FC = () => {
  const { t } = useLanguage()
  const [formData, setFormData] = useState({
    name: '',
    email: '',
    phone: '',
    location: '',
    serviceType: '',
    projectSize: '',
    budget: '',
    timeline: '',
    message: ''
  })
  const [isSubmitting, setIsSubmitting] = useState(false)
  const [submitStatus, setSubmitStatus] = useState<'idle' | 'success' | 'error'>('idle')

  const handleInputChange = (e: React.ChangeEvent<HTMLInputElement | HTMLTextAreaElement | HTMLSelectElement>) => {
    const { name, value } = e.target
    setFormData(prev => ({ ...prev, [name]: value }))
  }

  const handleSubmit = async (e: React.FormEvent<HTMLFormElement>) => {
    e.preventDefault()
    setIsSubmitting(true)
    
    try {
      // 使用 Formspree 發送郵件
      const response = await fetch('https://formspree.io/f/mldoqrea', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify(formData)
      })

      if (response.ok) {
        setSubmitStatus('success')
        setFormData({
          name: '',
          email: '',
          phone: '',
          location: '',
          serviceType: '',
          projectSize: '',
          budget: '',
          timeline: '',
          message: ''
        })
      } else {
        setSubmitStatus('error')
      }
    } catch (error) {
      console.error('表單提交失敗：', error)
      setSubmitStatus('error')
    } finally {
      setIsSubmitting(false)
    }
  }

  return (
    <section id="contact" className="py-20 bg-gray-50">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-16 animate-on-scroll">
          <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            {t('contact.title')}
          </h2>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto mb-4">
            {t('contact.subtitle')}
          </p>
          <p className="text-gray-600 max-w-3xl mx-auto">
            {t('contact.description')}
          </p>
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-3 gap-12">
          {/* 聯絡資訊 */}
          <div className="lg:col-span-1 animate-on-scroll">
            <div className="bg-emerald-600 text-white p-8 rounded-xl h-full">
              <h3 className="text-2xl font-bold mb-8">{t('contact.freeConsult')}</h3>
              <p className="mb-8 text-emerald-100">
                {t('contact.consultDesc')}
              </p>
              
              <div className="space-y-6">
                <div className="flex items-start">
                  <Phone className="w-6 h-6 mr-4 mt-1 flex-shrink-0" />
                  <div>
                    <p className="font-semibold">0983-695-834</p>
                    <p className="text-emerald-100 text-sm">週一至週六 07:00-19:00</p>
                  </div>
                </div>
                
                <div className="flex items-start">
                  <Mail className="w-6 h-6 mr-4 mt-1 flex-shrink-0" />
                  <div>
                    <p className="font-semibold">itsamliu2027@gmail.com</p>
                    <p className="text-emerald-100 text-sm">48小時內回覆</p>
                  </div>
                </div>
                
                <div className="flex items-start">
                  <MapPin className="w-6 h-6 mr-4 mt-1 flex-shrink-0" />
                  <div>
                    <p className="font-semibold">{t('contact.address')}</p>
                    <p className="text-emerald-100 text-sm">育苗場: 新竹縣竹東鎮民生路33-5號</p>
                  </div>
                </div>
              </div>
              
             {/*  <button className="w-full bg-white text-emerald-600 py-3 px-6 rounded-lg font-semibold mt-8 hover:bg-gray-50 transition-colors">
                {t('contact.bookConsult')}
              </button> */}
            </div>
          </div>

          {/* 需求表單 */}
          <div className="lg:col-span-2 animate-on-scroll">
            <div className="bg-white p-8 rounded-xl shadow-lg">
              {submitStatus === 'success' ? (
                <div className="text-center py-12">
                  <div className="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
                    <Send className="w-8 h-8 text-green-600" />
                  </div>
                  <h3 className="text-2xl font-bold text-gray-900 mb-4">提交成功!</h3>
                  <p className="text-gray-600 mb-6">{t('contact.successMessage')}</p>
                  <button
                    onClick={() => setSubmitStatus('idle')}
                    className="bg-emerald-600 text-white px-6 py-3 rounded-lg hover:bg-emerald-700 transition-colors"
                  >
                    填寫新的需求
                  </button>
                </div>
              ) : (
                <form onSubmit={handleSubmit} className="space-y-6">
                  <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.name')} *
                      </label>
                      <input
                        type="text"
                        name="name"
                        value={formData.name}
                        onChange={handleInputChange}
                        placeholder={t('contact.namePlaceholder')}
                        required
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      />
                    </div>
                    
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.email')} *
                      </label>
                      <input
                        type="email"
                        name="email"
                        value={formData.email}
                        onChange={handleInputChange}
                        placeholder={t('contact.emailPlaceholder')}
                        required
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      />
                    </div>
                  </div>

                  <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.phone')}
                      </label>
                      <input
                        type="tel"
                        name="phone"
                        value={formData.phone}
                        onChange={handleInputChange}
                        placeholder={t('contact.phonePlaceholder')}
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      />
                    </div>
                    
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.location')} *
                      </label>
                      <input
                        type="text"
                        name="location"
                        value={formData.location}
                        onChange={handleInputChange}
                        placeholder={t('contact.locationPlaceholder')}
                        required
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      />
                    </div>
                  </div>

                  <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.serviceType')} *
                      </label>
                      <select
                        name="serviceType"
                        value={formData.serviceType}
                        onChange={handleInputChange}
                        required
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      >
                        <option value="">{t('contact.selectService')}</option>
                        <option value="garden-design">{t('contact.gardenDesign')}</option>
                        <option value="landscaping">{t('contact.landscaping')}</option>
                        <option value="maintenance">{t('contact.maintenance')}</option>
                        <option value="planting">{t('contact.planting')}</option>
                        <option value="irrigation">{t('contact.irrigation')}</option>
                        <option value="consultation">{t('contact.consultation')}</option>
                      </select>
                    </div>
                    
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.projectSize')} *
                      </label>
                      <select
                        name="projectSize"
                        value={formData.projectSize}
                        onChange={handleInputChange}
                        required
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      >
                        <option value="">{t('contact.selectSize')}</option>
                        <option value="small">{t('contact.smallProject')}</option>
                        <option value="medium">{t('contact.mediumProject')}</option>
                        <option value="large">{t('contact.largeProject')}</option>
                      </select>
                    </div>
                  </div>

                  <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.budget')}
                      </label>
                      <select
                        name="budget"
                        value={formData.budget}
                        onChange={handleInputChange}
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      >
                        <option value="">{t('contact.selectBudget')}</option>
                        <option value="under-50k">{t('contact.budgetUnder50k')}</option>
                        <option value="50k-100k">{t('contact.budget50k100k')}</option>
                        <option value="100k-200k">{t('contact.budget100k200k')}</option>
                        <option value="over-200k">{t('contact.budgetOver200k')}</option>
                      </select>
                    </div>
                    
                    <div>
                      <label className="block text-sm font-semibold text-gray-700 mb-2">
                        {t('contact.timeline')}
                      </label>
                      <select
                        name="timeline"
                        value={formData.timeline}
                        onChange={handleInputChange}
                        className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors text-gray-900"
                      >
                        <option value="">{t('contact.selectTimeline')}</option>
                        <option value="asap">{t('contact.timelineASAP')}</option>
                        <option value="1-3months">{t('contact.timeline1to3')}</option>
                        <option value="3-6months">{t('contact.timeline3to6')}</option>
                        <option value="6plus">{t('contact.timeline6plus')}</option>
                      </select>
                    </div>
                  </div>

                  <div>
                    <label className="block text-sm font-semibold text-gray-700 mb-2">
                      {t('contact.message')}
                    </label>
                    <textarea
                      name="message"
                      value={formData.message}
                      onChange={handleInputChange}
                      placeholder={t('contact.messagePlaceholder')}
                      rows={4}
                      className="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500 transition-colors resize-vertical text-gray-900"
                    />
                  </div>

                  {submitStatus === 'error' && (
                    <div className="bg-red-50 border border-red-200 text-red-700 px-4 py-3 rounded-lg">
                      {t('contact.errorMessage')}
                    </div>
                  )}

                  <button
                    type="submit"
                    disabled={isSubmitting}
                    className="w-full bg-emerald-600 text-white py-4 px-6 rounded-lg font-semibold text-lg hover:bg-emerald-700 disabled:bg-gray-400 disabled:cursor-not-allowed transition-colors flex items-center justify-center gap-2"
                  >
                    {isSubmitting ? (
                      <>
                        <div className="w-5 h-5 border-2 border-white border-t-transparent rounded-full animate-spin"></div>
                        {t('contact.sending')}
                      </>
                    ) : (
                      <>
                        <Send className="w-5 h-5" />
                        {t('contact.send')}
                      </>
                    )}
                  </button>
                </form>
              )}
            </div>
          </div>
        </div>
      </div>
    </section>
  )
}

export default ContactSection
 



================================================================
File Path: src/components/Footer.tsx
================================================================

import React from 'react'
import { useLanguage } from '../contexts/LanguageContext'

const Footer: React.FC = () => {
  const { t } = useLanguage()

  return (
    <footer className="bg-slate-800 text-white">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
        {/* 公司資訊 */}
        <div className="text-center">
          <div className="flex items-center justify-center mb-6">
            <img 
              src="https://i.ibb.co/YTbBqbkm/LOGO.png" 
              alt="悅境園藝 Logo" 
              className="h-14 w-auto mr-2"
            />
            <span className="text-2xl font-bold">悅境園藝</span>
          </div>
          
          <p className="text-slate-300 mb-6 leading-relaxed max-w-2xl mx-auto">
            悅境園藝專業提供園藝設計、景觀工程與植栽維護服務，為您打造完美的綠色空間。
          </p>
          
          <div className="flex justify-center space-x-4 mb-8">
            <a 
              href="https://www.youtube.com/channel/UCiFQ-8sqejs_DA08qB5YO6A" 
              className="w-12 h-12 bg-red-600 rounded-lg flex items-center justify-center hover:bg-red-700 transition-colors"
              aria-label="YouTube"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg className="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/>
              </svg>
            </a>
            <a 
              href="https://line.me/R/oa/call/@055hjhgm?confirmation=true&from=call_url" 
              className="w-12 h-12 bg-emerald-600 rounded-lg flex items-center justify-center hover:bg-emerald-700 transition-colors"
              aria-label="LINE"
              target="_blank"
              rel="noopener noreferrer"
            >
              <svg className="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M19.365 9.863c.349 0 .63.285.63.631 0 .345-.281.63-.63.63H17.61v1.125h1.755c.349 0 .63.283.63.63 0 .344-.281.629-.63.629h-2.386c-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.627-.63h2.386c.349 0 .63.285.63.63 0 .349-.281.63-.63.63H17.61v1.125h1.755zm-3.855 3.016c0 .27-.174.51-.432.596-.064.021-.133.031-.199.031-.211 0-.391-.09-.51-.25l-2.443-3.317v2.94c0 .344-.279.629-.631.629-.346 0-.626-.285-.626-.629V8.108c0-.27.173-.51.43-.595.06-.023.136-.033.194-.033.195 0 .375.104.495.254l2.462 3.33V8.108c0-.345.282-.63.63-.63.345 0 .63.285.63.63v4.771zm-5.741 0c0 .344-.282.629-.631.629-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.627-.63.349 0 .631.285.631.63v4.771zm-2.466.629H4.917c-.345 0-.63-.285-.63-.629V8.108c0-.345.285-.63.63-.63.348 0 .63.285.63.63v4.141h1.756c.348 0 .629.283.629.630 0 .344-.282.629-.629.629M24 10.314C24 4.943 18.615.572 12 .572S0 4.943 0 10.314c0 4.811 4.27 8.842 10.035 9.608.391.082.923.258 1.058.59.12.301.079.766.038 1.08l-.164 1.02c-.045.301-.24 1.186 1.049.645 1.291-.539 6.916-4.070 9.436-6.975C23.176 14.393 24 12.458 24 10.314"/>
              </svg>
            </a>
          </div>
        </div>
        
        <div className="border-t border-slate-700 mt-12 pt-8 text-center">
          <p className="text-slate-400">
            © 2012 悅境園藝. All rights reserved.
          </p>
        </div>
      </div>
    </footer>
  );
};

export default Footer 



================================================================
File Path: src/components/HeroSection.tsx
================================================================

import React, { useEffect, useRef, useState } from "react"
import { useLanguage } from "../contexts/LanguageContext"
import VideoImporter from "../services/videoImporter"

// =========================================================
// 優化圖片元件(內部實現 - 簡化版)
// =========================================================
const OptimizedImage: React.FC<{
  src: string
  alt: string
  className?: string
  style?: React.CSSProperties
}> = ({ src, alt, className = "", style = {} }) => {
  const [isLoaded, setIsLoaded] = useState(false)
  const imgRef = useRef<HTMLImageElement>(null)

  useEffect(() => {
    const img = imgRef.current
    if (!img) return

    if (img.complete) {
      setIsLoaded(true)
    }
  }, [])

  return (
    <div
      className={className}
      style={{
        ...style,
        position: "relative",
        overflow: "hidden",
      }}
    >
      <img
        ref={imgRef}
        src={src}
        alt={alt}
        onLoad={() => setIsLoaded(true)}
        style={{
          width: "100%",
          height: "100%",
          objectFit: "cover",
          opacity: isLoaded ? 1 : 0,
          transition: "opacity 0.5s ease-in-out",
        }}
      />
      {!isLoaded && (
        <div
          style={{
            position: "absolute",
            inset: 0,
            background: "linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%)",
            backgroundSize: "200% 100%",
            animation: "shimmer 1.5s infinite",
          }}
        />
      )}
    </div>
  )
}

// =========================================================
// 樣式定義
// =========================================================
const styles = {
  card: {
    width: "25%",
    height: "100%",
    perspective: 1000,
    cursor: "default",
    userSelect: "none" as const,
    position: "relative" as const,
  },
  cardInner: (flipped: boolean) => ({
    position: "relative" as const,
    width: "100%",
    height: "100%",
    transition: "transform 0.3s ease-in-out",
    transformStyle: "preserve-3d" as const,
    transform: flipped ? "rotateY(180deg)" : "none",
  }),
  cardFace: {
    position: "absolute" as const,
    width: "100%",
    height: "100%",
    borderRadius: "30px",
    backfaceVisibility: "hidden" as const,
    top: 0,
    left: 0,
    boxShadow: "0 4px 12px rgba(0,0,0,0.25)",
  },
  cardFront: {
    background: "linear-gradient(145deg, #d9d9d9, #a6a6a6)",
    border: "1.5px solid #b0b0b0",
    boxShadow:
      "inset 0 2px 5px rgba(255,255,255,0.8), inset 0 -2px 8px rgba(0,0,0,0.3), 0 8px 15px rgba(0,0,0,0.25)",
    zIndex: 2,
  },
  cardBack: {
    transform: "rotateY(180deg)",
    border: "2px solid #b0b0b0",
    backgroundColor: "#eee",
    boxShadow: "0 4px 12px rgba(0,0,0,0.3), inset 0 0 0 2px rgba(255,255,255,0.3)",
    borderRadius: "30px",
    zIndex: 1,
    overflow: "hidden",
  },
}

// =========================================================
// 圖片 URL 定義(優化:集中管理)
// =========================================================
const IMAGES = [
  "https://i.ibb.co/Ldkc2p6N/1.webp",
  "https://i.ibb.co/YBDT6g47/2.webp",
  "https://i.ibb.co/XxwjJy3R/3.webp",
  "https://i.ibb.co/vvYDHmxP/4.webp",
  "https://i.ibb.co/Jwzg3JYF/5.webp",
  "https://i.ibb.co/HTP2jxTp/6.webp",
  "https://i.ibb.co/jqbsBfT/7.webp",
  "https://i.ibb.co/xKHhVRjQ/8.webp",
]

// =========================================================
// 幫助函式
// =========================================================
function getRandomIndices(total: number, count: number): number[] {
  const indices = Array.from({ length: total }, (_, i) => i)
  const result: number[] = []
  for (let i = 0; i < count; i++) {
    const randIdx = Math.floor(Math.random() * indices.length)
    result.push(indices[randIdx])
    indices.splice(randIdx, 1)
  }
  return result
}

// =========================================================
// FlipCard 元件(優化版)
// =========================================================
const FlipCard: React.FC<{ imageUrl: string; flipped: boolean }> = ({
  imageUrl,
  flipped,
}) => (
  <div style={styles.card}>
    <div style={styles.cardInner(flipped)}>
      <div style={{ ...styles.cardFace, ...styles.cardFront }}>
        <div
          style={{
            position: "absolute",
            top: 18,
            left: "50%",
            transform: "translateX(-50%)",
            width: 150,
            height: 8,
            background: "#e0e0e0",
            borderRadius: 20,
            boxShadow: "0 2px 6px rgba(0,0,0,0.15)",
          }}
        />
        <div
          style={{
            position: "absolute",
            bottom: 18,
            left: "50%",
            transform: "translateX(-50%)",
            width: 90,
            height: 8,
            background: "#e0e0e0",
            borderRadius: 20,
            boxShadow: "0 2px 5px rgba(0,0,0,0.12)",
          }}
        />
      </div>
      <div
        style={{
          ...styles.cardFace,
          ...styles.cardBack,
        }}
      >
        <img
          src={imageUrl}
          alt="卡片背面"
          style={{
            width: "100%",
            height: "100%",
            objectFit: "cover",
            borderRadius: "28px",
          }}
        />
      </div>
    </div>
  </div>
)

// =========================================================
// VideoPlayerTabs 元件
// =========================================================
declare global {
  interface Window {
    YT: any
    onYouTubeIframeAPIReady: (() => void) | null
  }
}

const VideoPlayerTabs: React.FC = () => {
  const { language } = useLanguage()
  const videoImporter = VideoImporter.getInstance()
  const heroVideos = videoImporter.getHeroVideos()
  const videos = heroVideos.map(v => ({
    id: v.videoId,
    title: language === 'zh' ? v.title_zh : v.title_en
  }))

  const playerRef = useRef<any>(null)
  const containerRef = useRef<HTMLDivElement>(null)
  const [selected, setSelected] = useState(0)
  const [ready, setReady] = useState(false)
  const [isMobile, setIsMobile] = useState(false)

  // 檢測是否為手機
  useEffect(() => {
    const checkMobile = () => {
      setIsMobile(window.innerWidth < 768)
    }
    checkMobile()
    window.addEventListener("resize", checkMobile)
    return () => window.removeEventListener("resize", checkMobile)
  }, [])

  useEffect(() => {
    const initPlayer = () => {
      if (containerRef.current && window.YT?.Player) {
        window.YT.ready(() => {
          playerRef.current = new window.YT.Player(containerRef.current, {
            height: isMobile ? "180" : "238",
            width: isMobile ? "320" : "424",
            videoId: videos[selected].id,
            playerVars: { autoplay: 0, mute: 1, controls: 1, modestbranding: 1, rel: 0 },
            events: { onReady: () => setReady(true) },
          })
        })
      }
    }

    if (!window.YT || !window.YT.Player) {
      const script = document.createElement("script")
      script.src = "https://www.youtube.com/iframe_api"
      script.async = true
      script.onload = initPlayer
      document.body.appendChild(script)
    } else {
      initPlayer()
    }

    return () => {
      if (playerRef.current?.destroy) playerRef.current.destroy()
      playerRef.current = null
    }
  }, [isMobile])

  useEffect(() => {
    if (ready && playerRef.current) {
      playerRef.current.loadVideoById(videos[selected].id)
      playerRef.current.mute()
    }
  }, [selected, ready])

  const currentTitle = videos[selected].title

  return (
    <div className="flex flex-col items-center bg-black/10 backdrop-blur rounded-xl p-3 shadow-xl max-w-lg mx-auto">
      <h3 className="text-base md:text-xl font-semibold mb-2 text-white text-center px-2">{currentTitle}</h3>
      <div className="mb-2 text-white text-xs md:text-sm font-medium">Sound On for the full experience.</div>
      
      {/* 固定尺寸容器 */}
      <div 
        className="relative flex justify-center items-center bg-black rounded-lg overflow-hidden"
        style={{ 
          width: isMobile ? "320px" : "424px",
          height: isMobile ? "180px" : "238px"
        }}
      >
        <div ref={containerRef} className="w-full h-full" />
      </div>

      <div className="flex flex-wrap justify-center gap-x-2 md:gap-x-3 gap-y-2 mt-3">
        {videos.map((v, i) => (
          <button
            key={i}
            className={`w-7 h-7 md:w-5 md:h-5 rounded-full border-2 flex items-center justify-center transition ${
              i === selected ? "border-white bg-white" : "border-gray-400 bg-gray-600/70"
            }`}
            style={{
              outline: i === selected ? "2px solid #22c55e" : "none",
              outlineOffset: i === selected ? "2px" : "0",
            }}
            onClick={() => setSelected(i)}
            aria-label={v.title}
          >
            {i === selected ? <span className="w-2 h-2 md:w-3 md:h-3 rounded-full bg-green-500 block" /> : null}
          </button>
        ))}
      </div>
    </div>
  )
}

// =========================================================
// 添加 shimmer 動畫樣式
// =========================================================
if (typeof document !== "undefined") {
  const style = document.createElement("style")
  style.textContent = `
    @keyframes shimmer {
      0% { background-position: 200% 0; }
      100% { background-position: -200% 0; }
    }
  `
  document.head.appendChild(style)
}

// =========================================================
// HeroSection 元件(優化版)
// =========================================================
const HeroSection: React.FC = () => {
  const { t } = useLanguage()
  const [isMobile, setIsMobile] = useState(false)
  const [indices, setIndices] = useState<number[]>([])
  const [flipped, setFlipped] = useState([false, false, false, false])

  useEffect(() => {
    const handleResize = () => setIsMobile(window.innerWidth < 768)
    handleResize()
    window.addEventListener("resize", handleResize)
    return () => window.removeEventListener("resize", handleResize)
  }, [])

  useEffect(() => {
    if (isMobile) {
      setIndices([0, 1, 2, 3])
      setFlipped([false, false, false, false])
      return
    }

    let currentIndex = -1
    let timeoutId: NodeJS.Timeout | null = null
    let intervalId: NodeJS.Timeout | null = null

    let currentRound = getRandomIndices(IMAGES.length, 4)
    setIndices(currentRound)

    const flipNext = () => {
      currentIndex++
      if (currentIndex < currentRound.length) {
        setFlipped((prev) => {
          const next = [...prev]
          next[currentIndex] = true
          return next
        })
      } else if (currentIndex === currentRound.length) {
        timeoutId = setTimeout(() => {
          setFlipped([false, false, false, false])
          currentRound = getRandomIndices(IMAGES.length, 4)
          setIndices(currentRound)
          currentIndex = -1
        }, 2000)
      }
    }

    intervalId = setInterval(() => {
      if (currentIndex === currentRound.length) return
      flipNext()
    }, 2000)

    flipNext()
    return () => {
      if (intervalId) clearInterval(intervalId)
      if (timeoutId) clearTimeout(timeoutId)
    }
  }, [isMobile])

  return (
    <section className="relative min-h-screen overflow-hidden">
      <div className="absolute inset-0 w-full h-full">
        {isMobile ? (
          <div className="w-full h-full relative">
            <OptimizedImage
              src={IMAGES[0]}
              alt="背景圖"
              className="w-full h-full"
            />
            <div className="absolute inset-0 bg-black/40" />
          </div>
        ) : (
          <div className="flex w-full h-full">
            {indices.map((img, i) => (
              <FlipCard
                key={img}
                imageUrl={IMAGES[img]}
                flipped={flipped[i]}
              />
            ))}
            <div className="absolute inset-0 bg-black/40" />
          </div>
        )}
      </div>

      <div className="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-[40%] z-10 text-center text-white px-4 sm:px-6 lg:px-8 max-w-4xl w-full">
        <h1 className="text-4xl md:text-6xl font-bold mb-6 drop-shadow-lg">{t("hero.title")}</h1>
        <p className="text-xl md:text-2xl mb-6 text-gray-200 font-light">{t("hero.subtitle")}</p>
        <p className="text-sm md:text-base mb-6 text-gray-300 leading-relaxed">
          {t("hero.description")}
        </p>
        <div className="flex justify-center">
          <VideoPlayerTabs />
        </div>
      </div>
    </section>
  )
}

export default HeroSection


================================================================
File Path: src/components/KnowledgeBaseManager.tsx
================================================================

import React, { useState, useCallback, useRef } from 'react';
import { Upload, FileText, AlertCircle, CheckCircle, Download, RefreshCw, X, FileDown } from 'lucide-react';
import { validateFile } from '../utils/fileValidator';
import { UploadProgress, ValidationResult } from '../types/uploadTypes';
import toast from 'react-hot-toast';

const KnowledgeBaseManager: React.FC = () => {
  const fileInputRef = useRef<HTMLInputElement>(null);
  
  const [isDragOver, setIsDragOver] = useState(false);
  const [selectedFile, setSelectedFile] = useState<File | null>(null);
  const [uploadProgress, setUploadProgress] = useState<UploadProgress>({
    status: 'idle',
    progress: 0,
    message: ''
  });
  const [validation, setValidation] = useState<ValidationResult | null>(null);
  const [mode, setMode] = useState<'replace' | 'merge'>('replace');

  // 重置上傳狀態
  const resetUpload = useCallback(() => {
    setSelectedFile(null);
    setValidation(null);
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    if (fileInputRef.current) {
      fileInputRef.current.value = '';
    }
  }, []);

  // 處理拖拽
  const handleDragOver = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(true);
  }, []);

  const handleDragLeave = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
  }, []);

  const handleDrop = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
    
    const files = Array.from(e.dataTransfer.files);
    if (files.length > 0) {
      handleFileSelect(files[0]);
    }
  }, []);

  // 處理檔案選擇
  const handleFileSelect = async (file: File) => {
    console.log('=== 檔案選擇 ===');
    console.log('檔案名稱:', file.name);
    console.log('檔案大小:', file.size);
    console.log('檔案類型:', file.type);
    
    // 重置之前的狀態
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    setSelectedFile(file);
    
    // 立即驗證檔案
    const fileValidation = validateFile(file);
    setValidation(fileValidation);
    
    console.log('驗證結果:', fileValidation);

    if (fileValidation.isValid) {
      toast.success('檔案選擇成功');
    } else {
      toast.error(fileValidation.errors.join('\n'));
    }
  };

  // 執行上傳
  const handleUpload = async () => {
    if (!selectedFile || !validation?.isValid) return;

    // 確認對話框
    const confirmMessage = mode === 'replace' 
      ? '確認替換整個知識庫嗎？此操作無法復原。'
      : '確認合併到現有知識庫嗎？';
    
    if (!window.confirm(confirmMessage)) {
      return;
    }

    try {
      setUploadProgress({ status: 'uploading', progress: 20, message: '上傳中...' });
      
      const formData = new FormData();
      formData.append('file', selectedFile);
      formData.append('mode', mode);

      const response = await fetch('http://localhost:3002/api/upload-knowledge', {
        method: 'POST',
        body: formData,
      });

      const result = await response.json();

      setUploadProgress({ status: 'processing', progress: 60, message: '處理中...' });
      await new Promise(resolve => setTimeout(resolve, 500));

      setUploadProgress({ status: 'validating', progress: 90, message: '驗證中...' });
      await new Promise(resolve => setTimeout(resolve, 300));

      if (result.success) {
        setUploadProgress({ status: 'success', progress: 100, message: '導入成功!' });
        toast.success(result.message);
        
        // 顯示統計資訊
        if (result.stats) {
          toast.success(
            `中文: ${result.stats.zh} 筆 | 英文: ${result.stats.en} 筆 | 分類: ${result.stats.categories.join(', ')}`
          );
        }
        
        // 成功後自動重置
        setTimeout(() => {
          resetUpload();
        }, 1500);
      } else {
        throw new Error(result.message);
      }
      
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      setUploadProgress({ status: 'error', progress: 0, message: `導入失敗: ${errorMessage}` });
      toast.error(`導入失敗: ${errorMessage}`);
      
      // 3秒後自動重置為可重試狀態
      setTimeout(() => {
        setUploadProgress({ status: 'idle', progress: 0, message: '' });
      }, 3000);
    }
  };

  // 執行導出
  const handleExport = async () => {
    try {
      const response = await fetch('http://localhost:3002/api/export-knowledge');
      const blob = await response.blob();
      const url = window.URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `knowledge-base-${new Date().toISOString().split('T')[0]}.xlsx`;
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      window.URL.revokeObjectURL(url);
      toast.success('知識庫導出成功!');
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`導出失敗: ${errorMessage}`);
    }
  };

  // 執行範本下載
  const handleTemplateDownload = async () => {
    try {
      const response = await fetch('http://localhost:3002/api/download-template');
      const blob = await response.blob();
      const url = window.URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'knowledge-base-template.xlsx';
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      window.URL.revokeObjectURL(url);
      toast.success('範本下載成功!');
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`範本下載失敗: ${errorMessage}`);
    }
  };

  // 判斷是否正在上傳中
  const isUploading = ['uploading', 'processing', 'validating'].includes(uploadProgress.status);

  return (
    <div className="space-y-6">
      {/* 模式選擇 */}
      <div className="flex gap-4 p-4 bg-gray-50 rounded-lg">
        <label className="flex items-center space-x-2 cursor-pointer">
          <input
            type="radio"
            name="mode"
            value="replace"
            checked={mode === 'replace'}
            onChange={(e) => setMode(e.target.value as 'replace' | 'merge')}
            className="w-4 h-4 text-red-600"
          />
          <span className="text-sm font-medium text-gray-700">覆蓋模式（清空後重新匯入）</span>
        </label>
        <label className="flex items-center space-x-2 cursor-pointer">
          <input
            type="radio"
            name="mode"
            value="merge"
            checked={mode === 'merge'}
            onChange={(e) => setMode(e.target.value as 'replace' | 'merge')}
            className="w-4 h-4 text-blue-600"
          />
          <span className="text-sm font-medium text-gray-700">合併模式（保留現有資料）</span>
        </label>
      </div>

      {/* 工具欄 */}
      <div className="flex flex-wrap gap-4">
        <button
          onClick={handleTemplateDownload}
          className="flex items-center space-x-2 px-4 py-2 bg-blue-50 text-blue-600 rounded-lg hover:bg-blue-100 transition-colors"
        >
          <Download className="w-4 h-4" />
          <span>下載範本</span>
        </button>
        
        <button
          onClick={handleExport}
          className="flex items-center space-x-2 px-4 py-2 bg-green-50 text-green-600 rounded-lg hover:bg-green-100 transition-colors"
        >
          <FileDown className="w-4 h-4" />
          <span>導出知識庫</span>
        </button>

        {/* 重置按鈕 - 當有選擇檔案時顯示 */}
        {selectedFile && (
          <button
            onClick={resetUpload}
            disabled={isUploading}
            className="flex items-center space-x-2 px-4 py-2 bg-gray-50 text-gray-600 rounded-lg hover:bg-gray-100 transition-colors disabled:opacity-50 disabled:cursor-not-allowed ml-auto"
          >
            <X className="w-4 h-4" />
            <span>重新選擇檔案</span>
          </button>
        )}
      </div>

      {/* 上傳區域 */}
      <div
        onDragOver={handleDragOver}
        onDragLeave={handleDragLeave}
        onDrop={handleDrop}
        className={`border-2 border-dashed rounded-xl p-8 text-center transition-all ${
          isDragOver
            ? 'border-blue-400 bg-blue-50'
            : selectedFile
            ? 'border-blue-300 bg-blue-50'
            : 'border-gray-300 hover:border-blue-300'
        }`}
      >
        <div className="flex flex-col items-center space-y-4">
          <div className={`p-4 rounded-full ${selectedFile ? 'bg-blue-100' : 'bg-gray-100'}`}>
            {selectedFile ? (
              <CheckCircle className="w-8 h-8 text-blue-600" />
            ) : (
              <Upload className="w-8 h-8 text-gray-400" />
            )}
          </div>
          
          <div>
            {selectedFile ? (
              <div className="space-y-2">
                <p className="text-sm text-gray-500">已選擇:</p>
                <p className="text-lg font-medium text-gray-700">
                  {selectedFile.name}
                </p>
                <p className="text-xs text-gray-400">
                  {(selectedFile.size / 1024).toFixed(2)} KB
                </p>
              </div>
            ) : (
              <>
                <p className="text-lg font-medium text-gray-200 mb-2">拖放檔案到此處，或點擊選擇檔案</p>
                <p className="text-sm text-gray-300 mt-1">支援格式: CSV, Excel (.xlsx, .xls)</p>
                <p className="text-xs text-gray-500">最大檔案大小: 10MB</p>
              </>
            )}
          </div>

          {!selectedFile && (
            <button
              onClick={() => fileInputRef.current?.click()}
              className="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors font-medium"
            >
              選擇檔案
            </button>
          )}
        </div>
      </div>

      <input
        ref={fileInputRef}
        type="file"
        accept=".xlsx,.xls,.csv"
        onChange={(e) => {
          console.log('檔案輸入變更事件觸發');
          console.log('檔案列表:', e.target.files);
          if (e.target.files?.[0]) {
            handleFileSelect(e.target.files[0]);
          }
        }}
        className="hidden"
      />

      {/* 檔案資訊顯示 - 只要選擇檔案就顯示 */}
      {selectedFile && (
        <div className="rounded-lg p-4 bg-blue-50 border border-blue-200">
          <div className="flex items-start space-x-3">
            <FileText className="w-5 h-5 text-blue-600 flex-shrink-0 mt-0.5" />
            <div className="flex-1 min-w-0">
              <h3 className="font-medium text-blue-800 mb-2">檔案路徑</h3>
              <p className="text-sm text-blue-700 break-all font-mono bg-blue-100 p-2 rounded">
                {selectedFile.name}
              </p>
              <div className="mt-2 flex gap-4 text-xs text-blue-600">
                <span>大小: {(selectedFile.size / 1024).toFixed(2)} KB</span>
                <span>類型: {selectedFile.type || '未知'}</span>
              </div>
            </div>
          </div>
        </div>
      )}

      {/* 驗證結果 */}
      {validation && (
        <div className={`rounded-lg p-4 ${
          validation.isValid ? 'bg-green-50 border border-green-200' : 'bg-red-50 border border-red-200'
        }`}>
          <div className="flex items-center space-x-2 mb-2">
            {validation.isValid ? (
              <CheckCircle className="w-5 h-5 text-green-600" />
            ) : (
              <AlertCircle className="w-5 h-5 text-red-600" />
            )}
            <h3 className={`font-medium ${validation.isValid ? 'text-green-800' : 'text-red-800'}`}>
              {validation.isValid ? '驗證通過' : '驗證失敗'}
            </h3>
          </div>

          {validation.errors.length > 0 && (
            <div className="mt-2">
              <p className="text-sm font-medium text-red-700 mb-1">錯誤:</p>
              <ul className="text-sm text-red-600 space-y-1">
                {validation.errors.map((error, index) => (
                  <li key={index}>• {error}</li>
                ))}
              </ul>
            </div>
          )}

          {validation.warnings.length > 0 && (
            <div className="mt-2">
              <p className="text-sm font-medium text-yellow-700 mb-1">警告:</p>
              <ul className="text-sm text-yellow-600 space-y-1">
                {validation.warnings.map((warning, index) => (
                  <li key={index}>• {warning}</li>
                ))}
              </ul>
            </div>
          )}
        </div>
      )}

      {/* 錯誤訊息顯示 */}
      {uploadProgress.status === 'error' && (
        <div className="rounded-lg p-4 bg-red-50 border border-red-200">
          <div className="flex items-center space-x-2">
            <AlertCircle className="w-5 h-5 text-red-600" />
            <p className="text-sm text-red-700">{uploadProgress.message}</p>
          </div>
        </div>
      )}

      {/* 按鈕區域 - 只要有選擇檔案就顯示 */}
      {selectedFile && (
        <div className="flex gap-4">
          <button
            onClick={resetUpload}
            disabled={isUploading}
            className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-gray-100 text-gray-700 rounded-lg hover:bg-gray-200 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
          >
            <X className="w-5 h-5" />
            <span>取消</span>
          </button>

          <button
            onClick={handleUpload}
            disabled={!validation?.isValid || isUploading || uploadProgress.status === 'success'}
            className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
          >
            {isUploading ? (
              <>
                <RefreshCw className="w-5 h-5 animate-spin" />
                <span>{uploadProgress.message}</span>
              </>
            ) : uploadProgress.status === 'success' ? (
              <>
                <CheckCircle className="w-5 h-5" />
                <span>導入成功!</span>
              </>
            ) : (
              <>
                <Upload className="w-5 h-5" />
                <span>確認導入</span>
              </>
            )}
          </button>
        </div>
      )}

      {/* 上傳進度 */}
      {(isUploading || uploadProgress.status === 'success') && (
        <div>
          <div className="bg-gray-200 rounded-full h-2">
            <div
              className={`h-2 rounded-full transition-all duration-300 ${
                uploadProgress.status === 'success' ? 'bg-green-600' : 'bg-blue-600'
              }`}
              style={{ width: `${uploadProgress.progress}%` }}
            />
          </div>
          <p className="text-sm text-gray-600 mt-2 text-center">{uploadProgress.message}</p>
        </div>
      )}
    </div>
  );
};

export default KnowledgeBaseManager;



================================================================
File Path: src/components/KnowledgeBaseUpload.tsx
================================================================

import React, { useState } from 'react';
import { Upload, Button, Radio, message, Card, Space } from 'antd';
import { UploadOutlined, InboxOutlined } from '@ant-design/icons';
import type { UploadFile, UploadProps } from 'antd';

const { Dragger } = Upload;

export const KnowledgeBaseUpload: React.FC = () => {
  const [fileList, setFileList] = useState<UploadFile[]>([]);
  const [uploading, setUploading] = useState(false);
  const [mode, setMode] = useState<'replace' | 'merge'>('replace');

  const handleUpload = async () => {
    if (fileList.length === 0) {
      message.error('請選擇檔案');
      return;
    }

    const formData = new FormData();
    formData.append('file', fileList[0] as any);
    formData.append('mode', mode);

    setUploading(true);

    try {
      const response = await fetch('http://localhost:3002/api/upload-knowledge', {
        method: 'POST',
        body: formData,
      });

      const result = await response.json();

      if (result.success) {
        message.success(result.message);
        setFileList([]);
        
        // 顯示統計資訊
        if (result.stats) {
          message.info(
            `中文: ${result.stats.zh} 筆 | 英文: ${result.stats.en} 筆 | 分類: ${result.stats.categories.join(', ')}`
          );
        }
      } else {
        message.error(result.message || '上傳失敗');
      }
    } catch (error) {
      console.error('上傳錯誤:', error);
      message.error('上傳失敗，請檢查後端伺服器是否運行');
    } finally {
      setUploading(false);
    }
  };

  const uploadProps: UploadProps = {
    onRemove: (file) => {
      const index = fileList.indexOf(file);
      const newFileList = fileList.slice();
      newFileList.splice(index, 1);
      setFileList(newFileList);
    },
    beforeUpload: (file) => {
      const isValidType = 
        file.type === 'text/csv' || 
        file.type === 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' ||
        file.type === 'application/vnd.ms-excel';
      
      if (!isValidType) {
        message.error('只支援 CSV 或 Excel 檔案');
        return false;
      }

      setFileList([file]);
      return false;
    },
    fileList,
    maxCount: 1,
  };

  return (
    <Card title="知識庫批次上傳" style={{ maxWidth: 800, margin: '20px auto' }}>
      <Space direction="vertical" style={{ width: '100%' }} size="large">
        <Radio.Group value={mode} onChange={(e) => setMode(e.target.value)}>
          <Radio value="replace">覆蓋模式（清空後重新匯入）</Radio>
          <Radio value="merge">合併模式（保留現有資料，新增不重複項目）</Radio>
        </Radio.Group>

        <Dragger {...uploadProps}>
          <p className="ant-upload-drag-icon">
            <InboxOutlined />
          </p>
          <p className="ant-upload-text">點擊或拖曳檔案到此區域上傳</p>
          <p className="ant-upload-hint">
            支援 CSV 或 Excel 檔案，檔案大小限制 10MB
          </p>
        </Dragger>

        <Button
          type="primary"
          onClick={handleUpload}
          disabled={fileList.length === 0}
          loading={uploading}
          icon={<UploadOutlined />}
          block
        >
          {uploading ? '上傳中...' : '開始上傳'}
        </Button>

        <div style={{ fontSize: '12px', color: '#666' }}>
          <p><strong>檔案格式要求：</strong></p>
          <ul>
            <li>必須包含欄位：language, keywords, question, answer, category, priority, enabled</li>
            <li>language: zh 或 en</li>
            <li>keywords: 多個關鍵字用逗號分隔</li>
            <li>enabled: true 或 false</li>
          </ul>
        </div>
      </Space>
    </Card>
  );
};



================================================================
File Path: src/components/LanguageSwitcher.tsx
================================================================

import React from 'react'
import { useLanguage } from '../contexts/LanguageContext'

const LanguageSwitcher: React.FC = () => {
  const { language, setLanguage } = useLanguage()

  return (
    <div className="flex items-center space-x-2">
      <button
        onClick={() => setLanguage('zh')}
        className={`px-3 py-1 text-sm rounded transition-colors ${
          language === 'zh'
            ? 'bg-emerald-600 text-white'
            : 'text-gray-600 hover:text-emerald-600'
        }`}
      >
        中文
      </button>
      <span className="text-gray-400">|</span>
      <button
        onClick={() => setLanguage('en')}
        className={`px-3 py-1 text-sm rounded transition-colors ${
          language === 'en'
            ? 'bg-emerald-600 text-white'
            : 'text-gray-600 hover:text-emerald-600'
        }`}
      >
        EN
      </button>
    </div>
  )
}

export default LanguageSwitcher
 



================================================================
File Path: src/components/Navbar.tsx
================================================================

import React, { useState } from 'react'
import {Menu, X} from 'lucide-react'
import { useLanguage } from '../contexts/LanguageContext'
import LanguageSwitcher from './LanguageSwitcher'
import { AudioPlayer } from './AudioPlayer'

const Navbar: React.FC = () => {
  const [isOpen, setIsOpen] = useState(false)
  const { t } = useLanguage()

  const toggleMenu = () => {
    setIsOpen(!isOpen)
  }

  const scrollToSection = (sectionId: string) => {
    const element = document.getElementById(sectionId)
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' })
      setIsOpen(false)
    }
  }

  return (
    <nav className="fixed top-0 left-0 right-0 z-50 bg-black/90 backdrop-blur-sm border-b border-gray-800">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="flex justify-between items-center h-16">
          {/* Logo */}
          <div className="flex items-center">
            <div className="flex-shrink-0 flex items-center">
              <img 
                src="https://i.ibb.co/YTbBqbkm/LOGO.png" 
                alt="悅境園藝 Logo" 
                className="h-10 md:h-12 w-auto mr-3"
              />
              {/* 桌面版顯示文字,手機版隱藏 */}
              <span className="hidden md:block text-white font-bold text-xl">悅境園藝</span>
              
              {/* 音樂播放器 - 常駐在標題旁邊 */}
             <AudioPlayer /> 
            </div>
          </div>

          {/* Desktop Menu */}
          <div className="hidden md:block">
            <div className="ml-10 flex items-baseline space-x-8">
              <button 
                onClick={() => scrollToSection('about')}
                className="text-gray-300 hover:text-emerald-400 px-3 py-2 text-sm font-medium transition-colors duration-200"
              >
                {t('nav.about')}
              </button>
              <button 
                onClick={() => scrollToSection('services')}
                className="text-gray-300 hover:text-emerald-400 px-3 py-2 text-sm font-medium transition-colors duration-200"
              >
                {t('nav.services')}
              </button>
              <button 
                onClick={() => scrollToSection('portfolio')}
                className="text-gray-300 hover:text-emerald-400 px-3 py-2 text-sm font-medium transition-colors duration-200"
              >
                {t('nav.portfolio')}
              </button>
              <button 
                onClick={() => scrollToSection('testimonials')}
                className="text-gray-300 hover:text-emerald-400 px-3 py-2 text-sm font-medium transition-colors duration-200"
              >
                {t('nav.testimonials')}
              </button>
              <button 
                onClick={() => scrollToSection('youtube-gallery')}
                className="text-gray-300 hover:text-emerald-400 px-3 py-2 text-sm font-medium transition-colors duration-200"
              >
                {t('nav.videos')}
              </button>
              <button 
                onClick={() => scrollToSection('contact')}
                className="bg-emerald-600 hover:bg-emerald-700 text-white px-4 py-2 rounded-lg text-sm font-medium transition-colors duration-200"
              >
                {t('nav.contact')}
              </button>
              <LanguageSwitcher />
            </div>
          </div>

          {/* Mobile menu button */}
          <div className="md:hidden flex items-center space-x-4">
            <div className="flex-shrink-0">
              <LanguageSwitcher />
            </div>
            <button
              onClick={toggleMenu}
              className="text-gray-300 hover:text-white focus:outline-none focus:text-white p-2"
            >
              {isOpen ? <X className="h-6 w-6" /> : <Menu className="h-6 w-6" />}
            </button>
          </div>
        </div>

        {/* Mobile Menu */}
        {isOpen && (
          <div className="md:hidden">
            <div className="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-black/95 backdrop-blur-sm">
              <button 
                onClick={() => scrollToSection('about')}
                className="text-gray-300 hover:text-emerald-400 block px-3 py-2 text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.about')}
              </button>
              <button 
                onClick={() => scrollToSection('services')}
                className="text-gray-300 hover:text-emerald-400 block px-3 py-2 text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.services')}
              </button>
              <button 
                onClick={() => scrollToSection('portfolio')}
                className="text-gray-300 hover:text-emerald-400 block px-3 py-2 text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.portfolio')}
              </button>
              <button 
                onClick={() => scrollToSection('testimonials')}
                className="text-gray-300 hover:text-emerald-400 block px-3 py-2 text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.testimonials')}
              </button>
              <button 
                onClick={() => scrollToSection('youtube-gallery')}
                className="text-gray-300 hover:text-emerald-400 block px-3 py-2 text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.videos')}
              </button>
              <button 
                onClick={() => scrollToSection('contact')}
                className="bg-emerald-600 hover:bg-emerald-700 text-white block px-3 py-2 rounded-lg text-base font-medium w-full text-left transition-colors duration-200"
              >
                {t('nav.contact')}
              </button>
            </div>
          </div>
        )}
      </div>
    </nav>
  )
}

export default Navbar


================================================================
File Path: src/components/PortfolioSection.tsx
================================================================

import React from "react"
import {ArrowRight} from 'lucide-react'
import { useLanguage } from "../contexts/LanguageContext"

const PortfolioSection: React.FC = () => {
  const { t } = useLanguage()

  const projects = [
    {
      title: t("portfolio.residential"),
      description: t("portfolio.residentialDesc"),
      category: t("portfolio.category.residential"),
      image: "https://i.ibb.co/4L5CZpD/2.webp",
      categoryColor: "bg-emerald-500"
    },
    {
      title: t("portfolio.commercial"),
      description: t("portfolio.commercialDesc"),
      category: t("portfolio.category.commercial"),
      image: "https://i.ibb.co/cKbbDJ5t/3.webp",
      categoryColor: "bg-emerald-600"
    },
    {
      title: t("portfolio.public"),
      description: t("portfolio.publicDesc"),
      category: t("portfolio.category.public"),
      image: "https://i.ibb.co/h1MHh1w3/1.webp",
      categoryColor: "bg-emerald-700"
    },
    {
      title: t("portfolio.rooftop"),
      description: t("portfolio.rooftopDesc"),
      category: t("portfolio.category.specialty"),
      image: "https://i.ibb.co/5xX5Dxtq/4.webp",
      categoryColor: "bg-emerald-800"
    }
  ]

  return (
    <section id="portfolio" className="py-20 bg-gray-50">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-16 animate-on-scroll">
          <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            {t("portfolio.title")}
          </h2>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto">
            {t("portfolio.subtitle")}
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-6 lg:gap-8">
          {projects.map((project, index) => (
            <div
              key={index}
              className="relative group rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-on-scroll min-h-[280px] md:min-h-[400px]"
              style={{ 
                animationDelay: `${index * 0.1}s`,
              }}
            >
              {/* 背景圖片 */}
              <div className="absolute inset-0">
                <img
                  src={project.image}
                  alt={project.title}
                  className="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                />
                {/* 漸層遮罩 */}
                <div className="absolute inset-0 bg-gradient-to-t from-black/80 via-black/40 to-transparent"></div>
              </div>

              {/* 內容區域 */}
              <div className="relative z-10 h-full flex flex-col justify-between p-6 md:p-8">
                {/* 頂部標籤 */}
                <div className="flex justify-start">
                  <span className={`${project.categoryColor} text-white px-3 py-1 md:px-4 md:py-2 rounded-full text-xs md:text-sm font-semibold shadow-lg`}>
                    {project.category}
                  </span>
                </div>

                {/* 底部內容 */}
                <div className="space-y-3 md:space-y-4">
                  <h3 className="text-xl md:text-2xl font-bold text-white leading-tight">
                    {project.title}
                  </h3>
                  <p className="text-gray-200 leading-relaxed text-sm md:text-base">
                    {project.description}
                  </p>
                  
                  {/* 查看項目按鈕 */}
                  <a 
                    href="#contact"
                    className="inline-flex items-center gap-2 text-white bg-white/20 backdrop-blur-sm hover:bg-white/30 px-4 py-2 md:px-6 md:py-3 rounded-lg font-semibold transition-all duration-300 group-hover:translate-x-2 text-sm md:text-base"
                  >
                    {t("portfolio.viewProject")}
                    <ArrowRight className="w-4 h-4 transition-transform duration-300 group-hover:translate-x-1" />
                  </a>
                </div>
              </div>

              {/* Hover效果 */}
              <div className="absolute inset-0 bg-emerald-600/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </div>
          ))}
        </div>
      </div>
    </section>
  )
}

export default PortfolioSection


================================================================
File Path: src/components/QuestionUploader.tsx
================================================================

import React, { useState, useCallback, useRef } from 'react';
import {Upload, FileText, AlertCircle, CheckCircle, Download, RefreshCw, X, FileDown} from 'lucide-react';
import { useLanguage } from '../contexts/LanguageContext';
import { dataImporter } from '../services/dataImporter';
import { validateFile } from '../utils/fileValidator';
import { UploadProgress, ValidationResult } from '../types/uploadTypes';
import toast from 'react-hot-toast';

interface QuestionUploaderProps {
  onClose: () => void;
  onSuccess?: () => void;
}

const QuestionUploader: React.FC<QuestionUploaderProps> = ({ onClose, onSuccess }) => {
  const { language } = useLanguage();
  const fileInputRef = useRef<HTMLInputElement>(null);
  
  const [isDragOver, setIsDragOver] = useState(false);
  const [selectedFile, setSelectedFile] = useState<File | null>(null);
  const [uploadProgress, setUploadProgress] = useState<UploadProgress>({
    status: 'idle',
    progress: 0,
    message: ''
  });
  const [validation, setValidation] = useState<ValidationResult | null>(null);

  const texts = {
    zh: {
      title: '知識庫管理',
      subtitle: '導入CSV檔案替換整個知識庫',
      dragText: '拖拽檔案到此處，或點擊選擇檔案',
      supportedFormats: '支援格式:CSV, Excel (.xlsx, .xls)',
      maxSize: '最大檔案大小:10MB',
      selectFile: '選擇檔案',
      downloadTemplate: '下載範本',
      exportData: '導出知識庫',
      upload: '確認導入',
      uploading: '導入中...',
      processing: '處理中...',
      validating: '驗證中...',
      success: '導入成功!',
      close: '關閉',
      cancel: '取消',
      errors: '錯誤',
      warnings: '警告',
      fileSelected: '已選擇檔案',
      validationPassed: '驗證通過',
      validationFailed: '驗證失敗',
      exportSuccess: '知識庫導出成功!',
      templateDownloadSuccess: '範本下載成功!',
      confirmReplace: '確認替換整個知識庫嗎?此操作無法復原。',
      resetUpload: '重新選擇檔案',
      selectedFile: '已選擇',
      filePath: '檔案路徑',
      fileSize: '大小',
      fileType: '類型',
      unknown: '未知'
    },
    en: {
      title: 'Knowledge Base Management',
      subtitle: 'Import CSV file to replace entire knowledge base',
      dragText: 'Drag files here, or click to select file',
      supportedFormats: 'Supported formats: CSV, Excel (.xlsx, .xls)',
      maxSize: 'Maximum file size: 10MB',
      selectFile: 'Select File',
      downloadTemplate: 'Download Template',
      exportData: 'Export Knowledge Base',
      upload: 'Confirm Import',
      uploading: 'Importing...',
      processing: 'Processing...',
      validating: 'Validating...',
      success: 'Import Successful!',
      close: 'Close',
      cancel: 'Cancel',
      errors: 'Errors',
      warnings: 'Warnings',
      fileSelected: 'File Selected',
      validationPassed: 'Validation Passed',
      validationFailed: 'Validation Failed',
      exportSuccess: 'Knowledge base exported successfully!',
      templateDownloadSuccess: 'Template downloaded successfully!',
      confirmReplace: 'Are you sure you want to replace the entire knowledge base? This action cannot be undone.',
      resetUpload: 'Select New File',
      selectedFile: 'Selected',
      filePath: 'File Path',
      fileSize: 'Size',
      fileType: 'Type',
      unknown: 'Unknown'
    }
  };

  const t = texts[language];

  // 重置上傳狀態
  const resetUpload = useCallback(() => {
    setSelectedFile(null);
    setValidation(null);
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    if (fileInputRef.current) {
      fileInputRef.current.value = '';
    }
  }, []);

  // 處理拖拽
  const handleDragOver = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(true);
  }, []);

  const handleDragLeave = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
  }, []);

  const handleDrop = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
    
    const files = Array.from(e.dataTransfer.files);
    if (files.length > 0) {
      handleFileSelect(files[0]);
    }
  }, []);

  // 處理檔案選擇
  const handleFileSelect = (file: File) => {
    console.log('=== 檔案選擇 ===');
    console.log('檔案名稱:', file.name);
    console.log('檔案大小:', file.size);
    console.log('檔案類型:', file.type);
    
    // 重置之前的狀態
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    setSelectedFile(file);
    
    // 立即驗證檔案
    const fileValidation = validateFile(file);
    setValidation(fileValidation);
    
    console.log('驗證結果:', fileValidation);

    if (fileValidation.isValid) {
      toast.success(t.fileSelected);
    } else {
      toast.error(fileValidation.errors.join('\n'));
    }
  };

  // 執行上傳
  const handleUpload = async () => {
    if (!selectedFile || !validation?.isValid) return;

    // 確認對話框
    if (!window.confirm(t.confirmReplace)) {
      return;
    }

    try {
      setUploadProgress({ status: 'uploading', progress: 20, message: t.uploading });
      
      await new Promise(resolve => setTimeout(resolve, 500));
      
      setUploadProgress({ status: 'processing', progress: 60, message: t.processing });
      
      const result = await dataImporter.importData(selectedFile, 'replace');
      
      setUploadProgress({ status: 'validating', progress: 90, message: t.validating });
      
      await new Promise(resolve => setTimeout(resolve, 300));
      
      if (result.success) {
        setUploadProgress({ status: 'success', progress: 100, message: t.success });
        toast.success(result.message);
        
        setTimeout(() => {
          onSuccess?.();
          onClose();
        }, 1500);
      } else {
        throw new Error(result.message);
      }
      
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      setUploadProgress({ status: 'error', progress: 0, message: `導入失敗: ${errorMessage}` });
      toast.error(`導入失敗: ${errorMessage}`);
      
      // 3秒後自動重置為可重試狀態
      setTimeout(() => {
        setUploadProgress({ status: 'idle', progress: 0, message: '' });
      }, 3000);
    }
  };

  // 執行導出
  const handleExport = () => {
    try {
      dataImporter.downloadKnowledgeBase();
      toast.success(t.exportSuccess);
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`導出失敗: ${errorMessage}`);
    }
  };

  // 執行範本下載
  const handleTemplateDownload = () => {
    try {
      dataImporter.downloadTemplate();
      toast.success(t.templateDownloadSuccess);
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`範本下載失敗: ${errorMessage}`);
    }
  };

  // 判斷是否正在上傳中
  const isUploading = ['uploading', 'processing', 'validating'].includes(uploadProgress.status);

  return (
    <>
      <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 p-4">
        <div className="bg-white rounded-2xl shadow-2xl w-full max-w-4xl max-h-[90vh] overflow-hidden">
          {/* 標題欄 */}
          <div className="bg-gradient-to-r from-green-600 to-emerald-600 text-white p-6">
            <div className="flex items-center justify-between">
              <div>
                <h2 className="text-2xl font-bold">{t.title}</h2>
              </div>
              <button
                onClick={onClose}
                className="text-white hover:bg-white hover:bg-opacity-20 rounded-full p-2 transition-colors"
              >
                <X className="w-6 h-6" />
              </button>
            </div>
          </div>

          <div className="p-6 overflow-y-auto max-h-[calc(90vh-120px)]">
            {/* 工具欄 */}
            <div className="flex flex-wrap gap-4 mb-6">
              <button
                onClick={handleTemplateDownload}
                className="flex items-center space-x-2 px-4 py-2 bg-blue-50 text-blue-600 rounded-lg hover:bg-blue-100 transition-colors"
              >
                <Download className="w-4 h-4" />
                <span>{t.downloadTemplate}</span>
              </button>
              
              <button
                onClick={handleExport}
                className="flex items-center space-x-2 px-4 py-2 bg-green-50 text-green-600 rounded-lg hover:bg-green-100 transition-colors"
              >
                <FileDown className="w-4 h-4" />
                <span>{t.exportData}</span>
              </button>

              {/* 重置按鈕 - 當有選擇檔案時顯示 */}
              {selectedFile && (
                <button
                  onClick={resetUpload}
                  disabled={isUploading}
                  className="flex items-center space-x-2 px-4 py-2 bg-gray-50 text-gray-600 rounded-lg hover:bg-gray-100 transition-colors disabled:opacity-50 disabled:cursor-not-allowed ml-auto"
                >
                  <X className="w-4 h-4" />
                  <span>{t.resetUpload}</span>
                </button>
              )}
            </div>

            {/* 上傳區域 */}
            <div
              onDragOver={handleDragOver}
              onDragLeave={handleDragLeave}
              onDrop={handleDrop}
              className={`border-2 border-dashed rounded-xl p-8 text-center transition-all ${
                isDragOver
                  ? 'border-green-400 bg-green-50'
                  : selectedFile
                  ? 'border-green-300 bg-green-50'
                  : 'border-gray-300 hover:border-green-300'
              }`}
            >
              <div className="flex flex-col items-center space-y-4">
                <div className={`p-4 rounded-full ${selectedFile ? 'bg-green-100' : 'bg-gray-100'}`}>
                  {selectedFile ? (
                    <CheckCircle className="w-8 h-8 text-green-600" />
                  ) : (
                    <Upload className="w-8 h-8 text-gray-400" />
                  )}
                </div>
                
                <div>
                  {selectedFile ? (
                    <div className="space-y-2">
                      <p className="text-sm text-gray-500">{t.selectedFile}:</p>
                      <p className="text-lg font-medium text-gray-700">
                        {selectedFile.name}
                      </p>
                      <p className="text-xs text-gray-400">
                        {(selectedFile.size / 1024).toFixed(2)} KB
                      </p>
                    </div>
                  ) : (
                    <>
                      <p className="text-lg font-medium text-gray-700">{t.dragText}</p>
                      <p className="text-sm text-gray-500 mt-1">{t.supportedFormats}</p>
                      <p className="text-xs text-gray-400">{t.maxSize}</p>
                    </>
                  )}
                </div>

                {!selectedFile && (
                  <button
                    onClick={() => fileInputRef.current?.click()}
                    className="px-6 py-3 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors font-medium"
                  >
                    {t.selectFile}
                  </button>
                )}
              </div>
            </div>

            <input
              ref={fileInputRef}
              type="file"
              accept=".csv,.xlsx,.xls"
              onChange={(e) => {
                console.log('檔案輸入變更事件觸發');
                console.log('檔案列表:', e.target.files);
                if (e.target.files?.[0]) {
                  handleFileSelect(e.target.files[0]);
                }
              }}
              className="hidden"
            />

            {/* 檔案資訊顯示 - 只要選擇檔案就顯示 */}
            {selectedFile && (
              <div className="mt-6">
                <div className="rounded-lg p-4 bg-blue-50 border border-blue-200">
                  <div className="flex items-start space-x-3">
                    <FileText className="w-5 h-5 text-blue-600 flex-shrink-0 mt-0.5" />
                    <div className="flex-1 min-w-0">
                      <h3 className="font-medium text-blue-800 mb-2">{t.filePath}</h3>
                      <p className="text-sm text-blue-700 break-all font-mono bg-blue-100 p-2 rounded">
                        {selectedFile.name}
                      </p>
                      <div className="mt-2 flex gap-4 text-xs text-blue-600">
                        <span>{t.fileSize}: {(selectedFile.size / 1024).toFixed(2)} KB</span>
                        <span>{t.fileType}: {selectedFile.type || t.unknown}</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            )}

            {/* 驗證結果 */}
            {validation && (
              <div className="mt-6">
                <div className={`rounded-lg p-4 ${
                  validation.isValid ? 'bg-green-50 border border-green-200' : 'bg-red-50 border border-red-200'
                }`}>
                  <div className="flex items-center space-x-2 mb-2">
                    {validation.isValid ? (
                      <CheckCircle className="w-5 h-5 text-green-600" />
                    ) : (
                      <AlertCircle className="w-5 h-5 text-red-600" />
                    )}
                    <h3 className={`font-medium ${validation.isValid ? 'text-green-800' : 'text-red-800'}`}>
                      {validation.isValid ? t.validationPassed : t.validationFailed}
                    </h3>
                  </div>

                  {validation.errors.length > 0 && (
                    <div className="mt-2">
                      <p className="text-sm font-medium text-red-700 mb-1">{t.errors}:</p>
                      <ul className="text-sm text-red-600 space-y-1">
                        {validation.errors.map((error, index) => (
                          <li key={index}>• {error}</li>
                        ))}
                      </ul>
                    </div>
                  )}

                  {validation.warnings.length > 0 && (
                    <div className="mt-2">
                      <p className="text-sm font-medium text-yellow-700 mb-1">{t.warnings}:</p>
                      <ul className="text-sm text-yellow-600 space-y-1">
                        {validation.warnings.map((warning, index) => (
                          <li key={index}>• {warning}</li>
                        ))}
                      </ul>
                    </div>
                  )}
                </div>
              </div>
            )}

            {/* 錯誤訊息顯示 */}
            {uploadProgress.status === 'error' && (
              <div className="mt-6">
                <div className="rounded-lg p-4 bg-red-50 border border-red-200">
                  <div className="flex items-center space-x-2">
                    <AlertCircle className="w-5 h-5 text-red-600" />
                    <p className="text-sm text-red-700">{uploadProgress.message}</p>
                  </div>
                </div>
              </div>
            )}

            {/* 按鈕區域 - 只要有選擇檔案就顯示 */}
            {selectedFile && (
              <div className="mt-6 flex gap-4">
                <button
                  onClick={onClose}
                  disabled={isUploading}
                  className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-gray-100 text-gray-700 rounded-lg hover:bg-gray-200 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
                >
                  <X className="w-5 h-5" />
                  <span>{t.cancel}</span>
                </button>

                <button
                  onClick={handleUpload}
                  disabled={!validation?.isValid || isUploading || uploadProgress.status === 'success'}
                  className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-red-600 text-white rounded-lg hover:bg-red-700 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
                >
                  {isUploading ? (
                    <>
                      <RefreshCw className="w-5 h-5 animate-spin" />
                      <span>{uploadProgress.message}</span>
                    </>
                  ) : uploadProgress.status === 'success' ? (
                    <>
                      <CheckCircle className="w-5 h-5" />
                      <span>{t.success}</span>
                    </>
                  ) : (
                    <>
                      <Upload className="w-5 h-5" />
                      <span>{t.upload}</span>
                    </>
                  )}
                </button>
              </div>
            )}

            {/* 上傳進度 */}
            {(isUploading || uploadProgress.status === 'success') && (
              <div className="mt-6">
                <div className="bg-gray-200 rounded-full h-2">
                  <div
                    className={`h-2 rounded-full transition-all duration-300 ${
                      uploadProgress.status === 'success' ? 'bg-green-600' : 'bg-blue-600'
                    }`}
                    style={{ width: `${uploadProgress.progress}%` }}
                  />
                </div>
                <p className="text-sm text-gray-600 mt-2 text-center">{uploadProgress.message}</p>
              </div>
            )}
          </div>
        </div>
      </div>
    </>
  );
};

export default QuestionUploader;


================================================================
File Path: src/components/ServicesSection.tsx
================================================================

import React from 'react'
import {Palette, Hammer, Leaf, Droplets} from 'lucide-react'
import { useLanguage } from '../contexts/LanguageContext'

const ServicesSection: React.FC = () => {
  const { t } = useLanguage()

  const services = [
    {
      icon: <Palette className="w-12 h-12 text-emerald-600" />,
      title: t('services.gardenDesign'),
      description: t('services.gardenDesignDesc')
    },
    {
      icon: <Hammer className="w-12 h-12 text-emerald-600" />,
      title: t('services.landscaping'),
      description: t('services.landscapingDesc')
    },
    {
      icon: <Leaf className="w-12 h-12 text-emerald-600" />,
      title: t('services.maintenance'),
      description: t('services.maintenanceDesc')
    },
    {
      icon: <Droplets className="w-12 h-12 text-emerald-600" />,
      title: t('services.irrigation'),
      description: t('services.irrigationDesc')
    }
  ]

  return (
    <section id="services" className="py-20 bg-gray-50">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-16 animate-on-scroll">
          <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            {t('services.title')}
          </h2>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto">
            {t('services.subtitle')}
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          {services.map((service, index) => (
            <div
              key={index}
              className="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 animate-on-scroll"
              style={{ animationDelay: `${index * 0.1}s` }}
            >
              <div className="mb-6">{service.icon}</div>
              <h3 className="text-xl font-semibold text-gray-900 mb-4">
                {service.title}
              </h3>
              <p className="text-gray-600 leading-relaxed">
                {service.description}
              </p>
            </div>
          ))}
        </div>
      </div>
    </section>
  )
}

export default ServicesSection 



================================================================
File Path: src/components/TestimonialsSection.tsx
================================================================

import React from "react"
import {Star} from 'lucide-react'
import { useLanguage } from "../contexts/LanguageContext"

const TestimonialsSection: React.FC = () => {
  const { t } = useLanguage()

  const testimonials = [
    {
      name: t("testimonials.client1"),
      title: t("testimonials.client1Title"),
      text: t("testimonials.client1Text"),
      rating: 5
    },
    {
      name: t("testimonials.client2"),
      title: t("testimonials.client2Title"),
      text: t("testimonials.client2Text"),
      rating: 5
    },
    {
      name: t("testimonials.client3"),
      title: t("testimonials.client3Title"),
      text: t("testimonials.client3Text"),
      rating: 5
    },
    {
      name: t("testimonials.client4"),
      title: t("testimonials.client4Title"),
      text: t("testimonials.client4Text"),
      rating: 5
    },
    {
      name: t("testimonials.client5"),
      title: t("testimonials.client5Title"),
      text: t("testimonials.client5Text"),
      rating: 5
    },
    {
      name: t("testimonials.client6"),
      title: t("testimonials.client6Title"),
      text: t("testimonials.client6Text"),
      rating: 5
    }
  ]

  return (
    <section id="testimonials" className="py-20 bg-gray-50">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-16">
          <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            {t("testimonials.title")}
          </h2>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto">
            {t("testimonials.subtitle")}
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          {testimonials.map((testimonial, index) => (
            <div
              key={index}
              className="bg-white p-6 rounded-lg shadow-sm border border-gray-100 hover:shadow-md transition-shadow duration-300"
            >
              <div className="flex mb-4">
                {[...Array(testimonial.rating)].map((_, i) => (
                  <Star key={i} className="w-5 h-5 text-yellow-400 fill-current" />
                ))}
              </div>
              
              <p className="text-gray-700 mb-6 leading-relaxed text-sm">
                "{testimonial.text}"
              </p>
              
              <div className="border-t pt-4">
                <h3 className="font-semibold text-gray-900 text-sm">
                  {testimonial.name}
                </h3>
                <p className="text-gray-600 text-sm">{testimonial.title}</p>
              </div>
            </div>
          ))}
        </div>
      </div>
    </section>
  )
}

export default TestimonialsSection 



================================================================
File Path: src/components/VideoManager.tsx
================================================================

import React, { useState, useCallback, useRef } from 'react';
import { Upload, FileText, AlertCircle, CheckCircle, Download, RefreshCw, X, FileDown } from 'lucide-react';
import VideoImporter from '../services/videoImporter';
import { validateFile } from '../utils/fileValidator';
import { UploadProgress, ValidationResult } from '../types/uploadTypes';
import toast from 'react-hot-toast';

const VideoManager: React.FC = () => {
  const videoImporter = VideoImporter.getInstance();
  const fileInputRef = useRef<HTMLInputElement>(null);
  
  const [isDragOver, setIsDragOver] = useState(false);
  const [selectedFile, setSelectedFile] = useState<File | null>(null);
  const [uploadProgress, setUploadProgress] = useState<UploadProgress>({
    status: 'idle',
    progress: 0,
    message: ''
  });
  const [validation, setValidation] = useState<ValidationResult | null>(null);

  // 重置上傳狀態
  const resetUpload = useCallback(() => {
    setSelectedFile(null);
    setValidation(null);
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    if (fileInputRef.current) {
      fileInputRef.current.value = '';
    }
  }, []);

  // 處理拖拽
  const handleDragOver = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(true);
  }, []);

  const handleDragLeave = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
  }, []);

  const handleDrop = useCallback((e: React.DragEvent) => {
    e.preventDefault();
    setIsDragOver(false);
    
    const files = Array.from(e.dataTransfer.files);
    if (files.length > 0) {
      handleFileSelect(files[0]);
    }
  }, []);

  // 處理檔案選擇
  const handleFileSelect = async (file: File) => {
    console.log('=== 檔案選擇 ===');
    console.log('檔案名稱:', file.name);
    console.log('檔案大小:', file.size);
    console.log('檔案類型:', file.type);
    
    // 重置之前的狀態
    setUploadProgress({ status: 'idle', progress: 0, message: '' });
    setSelectedFile(file);
    
    // 立即驗證檔案
    const fileValidation = validateFile(file);
    
    if (fileValidation.isValid) {
      const excelValidation = await videoImporter.validateExcelFile(file);
      setValidation(excelValidation);
      
      console.log('驗證結果:', excelValidation);

      if (excelValidation.isValid) {
        toast.success('檔案選擇成功');
      } else {
        toast.error(excelValidation.errors.join('\n'));
      }
    } else {
      setValidation(fileValidation);
      console.log('驗證結果:', fileValidation);
      toast.error(fileValidation.errors.join('\n'));
    }
  };

  // 執行上傳
  const handleUpload = async () => {
    if (!selectedFile || !validation?.isValid) return;

    // 確認對話框
    if (!window.confirm('確認替換整個影片庫嗎？此操作無法復原。')) {
      return;
    }

    try {
      setUploadProgress({ status: 'uploading', progress: 20, message: '導入中...' });
      
      await new Promise(resolve => setTimeout(resolve, 500));
      
      setUploadProgress({ status: 'processing', progress: 60, message: '處理中...' });
      
      const result = await videoImporter.importFromExcel(selectedFile);
      
      setUploadProgress({ status: 'validating', progress: 90, message: '驗證中...' });
      
      await new Promise(resolve => setTimeout(resolve, 300));
      
      if (result.success) {
        setUploadProgress({ status: 'success', progress: 100, message: '導入成功!' });
        toast.success(result.message);
        
        // 成功後自動重置
        setTimeout(() => {
          resetUpload();
        }, 1500);
      } else {
        throw new Error(result.message);
      }
      
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      setUploadProgress({ status: 'error', progress: 0, message: `導入失敗: ${errorMessage}` });
      toast.error(`導入失敗: ${errorMessage}`);
      
      // 3秒後自動重置為可重試狀態
      setTimeout(() => {
        setUploadProgress({ status: 'idle', progress: 0, message: '' });
      }, 3000);
    }
  };

  // 執行導出
  const handleExport = async () => {
    try {
      await videoImporter.exportToExcel();
      toast.success('影片庫導出成功!');
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`導出失敗: ${errorMessage}`);
    }
  };

  // 執行範本下載
  const handleTemplateDownload = async () => {
    try {
      await videoImporter.downloadTemplate();
      toast.success('範本下載成功!');
    } catch (error) {
      const errorMessage = error instanceof Error ? error.message : '未知錯誤';
      toast.error(`範本下載失敗: ${errorMessage}`);
    }
  };

  // 判斷是否正在上傳中
  const isUploading = ['uploading', 'processing', 'validating'].includes(uploadProgress.status);

  return (
    <div className="space-y-6">
      {/* 工具欄 */}
      <div className="flex flex-wrap gap-4">
        <button
          onClick={handleTemplateDownload}
          className="flex items-center space-x-2 px-4 py-2 bg-blue-50 text-blue-600 rounded-lg hover:bg-blue-100 transition-colors"
        >
          <Download className="w-4 h-4" />
          <span>下載範本</span>
        </button>
        
        <button
          onClick={handleExport}
          className="flex items-center space-x-2 px-4 py-2 bg-green-50 text-green-600 rounded-lg hover:bg-green-100 transition-colors"
        >
          <FileDown className="w-4 h-4" />
          <span>導出影片庫</span>
        </button>

        {/* 重置按鈕 - 當有選擇檔案時顯示 */}
        {selectedFile && (
          <button
            onClick={resetUpload}
            disabled={isUploading}
            className="flex items-center space-x-2 px-4 py-2 bg-gray-50 text-gray-600 rounded-lg hover:bg-gray-100 transition-colors disabled:opacity-50 disabled:cursor-not-allowed ml-auto"
          >
            <X className="w-4 h-4" />
            <span>重新選擇檔案</span>
          </button>
        )}
      </div>

      {/* 上傳區域 */}
      <div
        onDragOver={handleDragOver}
        onDragLeave={handleDragLeave}
        onDrop={handleDrop}
        className={`border-2 border-dashed rounded-xl p-8 text-center transition-all ${
          isDragOver
            ? 'border-red-400 bg-red-50'
            : selectedFile
            ? 'border-red-300 bg-red-50'
            : 'border-gray-300 hover:border-red-300'
        }`}
      >
        <div className="flex flex-col items-center space-y-4">
          <div className={`p-4 rounded-full ${selectedFile ? 'bg-red-100' : 'bg-gray-100'}`}>
            {selectedFile ? (
              <CheckCircle className="w-8 h-8 text-red-600" />
            ) : (
              <Upload className="w-8 h-8 text-gray-400" />
            )}
          </div>
          
          <div>
            {selectedFile ? (
              <div className="space-y-2">
                <p className="text-sm text-gray-500">已選擇:</p>
                <p className="text-lg font-medium text-gray-700">
                  {selectedFile.name}
                </p>
                <p className="text-xs text-gray-400">
                  {(selectedFile.size / 1024).toFixed(2)} KB
                </p>
              </div>
            ) : (
              <>
                <p className="text-lg font-medium text-gray-200 mb-2">拖放檔案到此處，或點擊選擇檔案</p>
                <p className="text-sm text-gray-300 mt-1">支援格式: Excel (.xlsx, .xls)</p>
                <p className="text-xs text-gray-500">最大檔案大小: 10MB</p>
              </>
            )}
          </div>

          {!selectedFile && (
            <button
              onClick={() => fileInputRef.current?.click()}
              className="px-6 py-3 bg-red-600 text-white rounded-lg hover:bg-red-700 transition-colors font-medium"
            >
              選擇檔案
            </button>
          )}
        </div>
      </div>

      <input
        ref={fileInputRef}
        type="file"
        accept=".xlsx,.xls"
        onChange={(e) => {
          console.log('檔案輸入變更事件觸發');
          console.log('檔案列表:', e.target.files);
          if (e.target.files?.[0]) {
            handleFileSelect(e.target.files[0]);
          }
        }}
        className="hidden"
      />

      {/* 檔案資訊顯示 - 只要選擇檔案就顯示 */}
      {selectedFile && (
        <div className="rounded-lg p-4 bg-blue-50 border border-blue-200">
          <div className="flex items-start space-x-3">
            <FileText className="w-5 h-5 text-blue-600 flex-shrink-0 mt-0.5" />
            <div className="flex-1 min-w-0">
              <h3 className="font-medium text-blue-800 mb-2">檔案路徑</h3>
              <p className="text-sm text-blue-700 break-all font-mono bg-blue-100 p-2 rounded">
                {selectedFile.name}
              </p>
              <div className="mt-2 flex gap-4 text-xs text-blue-600">
                <span>大小: {(selectedFile.size / 1024).toFixed(2)} KB</span>
                <span>類型: {selectedFile.type || '未知'}</span>
              </div>
            </div>
          </div>
        </div>
      )}

      {/* 驗證結果 */}
      {validation && (
        <div className={`rounded-lg p-4 ${
          validation.isValid ? 'bg-green-50 border border-green-200' : 'bg-red-50 border border-red-200'
        }`}>
          <div className="flex items-center space-x-2 mb-2">
            {validation.isValid ? (
              <CheckCircle className="w-5 h-5 text-green-600" />
            ) : (
              <AlertCircle className="w-5 h-5 text-red-600" />
            )}
            <h3 className={`font-medium ${validation.isValid ? 'text-green-800' : 'text-red-800'}`}>
              {validation.isValid ? '驗證通過' : '驗證失敗'}
            </h3>
          </div>

          {validation.errors.length > 0 && (
            <div className="mt-2">
              <p className="text-sm font-medium text-red-700 mb-1">錯誤:</p>
              <ul className="text-sm text-red-600 space-y-1">
                {validation.errors.map((error, index) => (
                  <li key={index}>• {error}</li>
                ))}
              </ul>
            </div>
          )}

          {validation.warnings.length > 0 && (
            <div className="mt-2">
              <p className="text-sm font-medium text-yellow-700 mb-1">警告:</p>
              <ul className="text-sm text-yellow-600 space-y-1">
                {validation.warnings.map((warning, index) => (
                  <li key={index}>• {warning}</li>
                ))}
              </ul>
            </div>
          )}
        </div>
      )}

      {/* 錯誤訊息顯示 */}
      {uploadProgress.status === 'error' && (
        <div className="rounded-lg p-4 bg-red-50 border border-red-200">
          <div className="flex items-center space-x-2">
            <AlertCircle className="w-5 h-5 text-red-600" />
            <p className="text-sm text-red-700">{uploadProgress.message}</p>
          </div>
        </div>
      )}

      {/* 按鈕區域 - 只要有選擇檔案就顯示 */}
      {selectedFile && (
        <div className="flex gap-4">
          <button
            onClick={resetUpload}
            disabled={isUploading}
            className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-gray-100 text-gray-700 rounded-lg hover:bg-gray-200 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
          >
            <X className="w-5 h-5" />
            <span>取消</span>
          </button>

          <button
            onClick={handleUpload}
            disabled={!validation?.isValid || isUploading || uploadProgress.status === 'success'}
            className="flex-1 flex items-center justify-center space-x-2 px-6 py-3 bg-red-600 text-white rounded-lg hover:bg-red-700 transition-colors disabled:opacity-50 disabled:cursor-not-allowed font-medium text-lg"
          >
            {isUploading ? (
              <>
                <RefreshCw className="w-5 h-5 animate-spin" />
                <span>{uploadProgress.message}</span>
              </>
            ) : uploadProgress.status === 'success' ? (
              <>
                <CheckCircle className="w-5 h-5" />
                <span>導入成功!</span>
              </>
            ) : (
              <>
                <Upload className="w-5 h-5" />
                <span>確認導入</span>
              </>
            )}
          </button>
        </div>
      )}

      {/* 上傳進度 */}
      {(isUploading || uploadProgress.status === 'success') && (
        <div>
          <div className="bg-gray-200 rounded-full h-2">
            <div
              className={`h-2 rounded-full transition-all duration-300 ${
                uploadProgress.status === 'success' ? 'bg-green-600' : 'bg-blue-600'
              }`}
              style={{ width: `${uploadProgress.progress}%` }}
            />
          </div>
          <p className="text-sm text-gray-600 mt-2 text-center">{uploadProgress.message}</p>
        </div>
      )}
    </div>
  );
};

export default VideoManager;


================================================================
File Path: src/components/VideoModal.tsx
================================================================

import React, { useEffect, useState } from "react"
import {X} from 'lucide-react'

interface VideoModalProps {
  isOpen: boolean
  onClose: () => void
}

const VideoModal: React.FC<VideoModalProps> = ({ isOpen, onClose }) => {
  const [isLoading, setIsLoading] = useState(true)
  const [videoSrc, setVideoSrc] = useState("")

  useEffect(() => {
    if (isOpen) {
      setIsLoading(true)
      setVideoSrc("")
      
      const videoId = "Plcv-VsZ3Uo"
      const embedUrl = `https://www.youtube.com/embed/${videoId}?autoplay=1&rel=0&modestbranding=1`
      
      setTimeout(() => {
        setIsLoading(false)
        setVideoSrc(embedUrl)
      }, 1500)
    } else {
      setVideoSrc("")
      setIsLoading(true)
    }
  }, [isOpen])

  useEffect(() => {
    const handleEscapeKey = (e: KeyboardEvent) => {
      if (e.key === "Escape") {
        onClose()
      }
    }

    if (isOpen) {
      document.addEventListener("keydown", handleEscapeKey)
    }

    return () => {
      document.removeEventListener("keydown", handleEscapeKey)
    }
  }, [isOpen, onClose])

  const handleBackdropClick = (e: React.MouseEvent) => {
    if (e.target === e.currentTarget) {
      onClose()
    }
  }

  if (!isOpen) return null

  return (
    <div className="fixed inset-0 bg-black bg-opacity-75 flex items-center justify-center z-50 p-4" onClick={handleBackdropClick}>
      <div className="bg-white rounded-lg max-w-4xl w-full max-h-[90vh] md:max-h-[85vh] overflow-auto relative">
        <button 
          onClick={onClose} 
          className="absolute top-4 right-4 z-10 bg-gray-800 hover:bg-gray-900 text-white rounded-full p-3 md:p-2 shadow-lg transition-all duration-200 hover:scale-110 focus:outline-none focus:ring-2 focus:ring-gray-600 focus:ring-offset-2"
          aria-label="關閉影片"
        >
          <X className="w-6 h-6" />
        </button>
        
        {/* 載入動畫 */}
        {isLoading && (
          <div className="flex flex-col items-center justify-center p-12">
            <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-green-600 mb-4"></div>
            <p className="text-gray-600">正在載入影片...</p>
          </div>
        )}
        
        {/* 影片內容 */}
        {!isLoading && (
          <div className="p-4 md:p-6">
            <h2 className="text-xl md:text-2xl font-bold text-gray-900 mb-4 text-center">悅境園藝介紹</h2>
            
            <div className="relative pb-[56.25%] h-0 mb-6">
              <iframe 
                src={videoSrc}
                className="absolute top-0 left-0 w-full h-full rounded-lg"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowFullScreen
                title="悅境園藝介紹影片"
              />
            </div>
            
            <div className="text-center">
              <div className="bg-green-50 p-4 rounded-lg border-l-4 border-green-400">
                <h3 className="text-green-800 font-semibold mb-2 text-sm md:text-base">園藝景觀顧問解說</h3>
                <p className="text-green-700 text-xs md:text-sm">由豐富經驗的園藝技師和景觀設計師組成,無論是科技廠區/高檔社區或是私人會所都有相當多樣的工程實績。</p>
              </div>
            </div>
          </div>
        )}
      </div>
    </div>
  )
}

export default VideoModal


================================================================
File Path: src/components/VisitorAnalytics.tsx
================================================================

import React, { useState, useEffect } from "react";
import * as ExcelJS from "exceljs";
import AdminLogin from "./AdminLogin";
import { AnalyticsCharts } from "./AnalyticsCharts";
import { OperationsTab } from "./AnalyticsTabContent";
import VideoManager from "./VideoManager";
import KnowledgeBaseManager from "./KnowledgeBaseManager";
import { DashboardTab, TimeRange, VisitorLog } from "../constants/analyticsConstants";
import { useAnalyticsData } from "../hooks/useAnalyticsData";

import { supabase } from "../lib/supabase";

const VisitorAnalytics: React.FC = () => {
  const [showAnalytics, setShowAnalytics] = useState(false);
  const [isAuthenticated, setIsAuthenticated] = useState(false);
  const [showLogin, setShowLogin] = useState(false);
  const [activeTab, setActiveTab] = useState<DashboardTab>("visitors");

  const {
    visitors,
    chartData,
    countryData,
    timeRange,
    setTimeRange,
    loading,
    totalVisits,
    uniqueVisitors,
    comparisonStats,
    reachedMilestone,
    showCookieConsent,
    handleCookieConsent,
    fetchVisitorData,
    operationLogs,
    operationStats,
    logFilter,
    setLogFilter,
    logsLoading,
    fetchOperationLogs,
    fetchOperationStats,
    hoveredCountry,
    setHoveredCountry,
  } = useAnalyticsData();

  useEffect(() => {
    const checkAdminSession = () => {
      const sessionToken = sessionStorage.getItem("admin_session_token");
      const sessionExpiry = sessionStorage.getItem("admin_session_expiry");
      
      if (sessionToken && sessionExpiry) {
        const expiryTime = parseInt(sessionExpiry, 10);
        if (Date.now() < expiryTime) {
          setIsAuthenticated(true);
          return;
        }
      }
      
      sessionStorage.removeItem("admin_session_token");
      sessionStorage.removeItem("admin_session_expiry");
      setIsAuthenticated(false);
    };

    checkAdminSession();
  }, []);

  const handleLoginSuccess = () => {
    setIsAuthenticated(true);
    setShowLogin(false);
  };

  const handleLogout = () => {
    sessionStorage.removeItem("admin_session_token");
    sessionStorage.removeItem("admin_session_expiry");
    setIsAuthenticated(false);
    setShowAnalytics(false);
  };

  const exportToXLSX = async () => {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet("訪客數據");

    worksheet.columns = [
      { header: "IP地址", key: "ip_address", width: 20 },
      { header: "國家", key: "country", width: 15 },
      { header: "城市", key: "city", width: 15 },
      { header: "訪問次數", key: "visit_count", width: 12 },
      { header: "首次訪問", key: "first_visit", width: 20 },
      { header: "最後訪問", key: "last_visit", width: 20 },
    ];

    visitors.forEach((v: VisitorLog) => {
      worksheet.addRow({
        ip_address: v.ip_address,
        country: v.country || "Unknown",
        city: v.city || "Unknown",
        visit_count: v.visit_count,
        first_visit: new Date(v.first_visit).toLocaleString("zh-TW"),
        last_visit: new Date(v.last_visit).toLocaleString("zh-TW"),
      });
    });

    worksheet.getRow(1).font = { bold: true };
    worksheet.getRow(1).fill = {
      type: "pattern",
      pattern: "solid",
      fgColor: { argb: "FF10B981" },
    };

    const buffer = await workbook.xlsx.writeBuffer();
    const blob = new Blob([buffer], {
      type: "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
    });
    const url = window.URL.createObjectURL(blob);
    const link = document.createElement("a");
    link.href = url;
    link.download = `visitor_analytics_${timeRange}_${
      new Date().toISOString().split("T")[0]
    }.xlsx`;
    link.click();
    window.URL.revokeObjectURL(url);
  };

  useEffect(() => {
    if (showAnalytics && isAuthenticated) {
      fetchVisitorData();
      const interval = setInterval(fetchVisitorData, 30000);
      return () => clearInterval(interval);
    }
  }, [showAnalytics, isAuthenticated, fetchVisitorData]);

  useEffect(() => {
    if (showAnalytics && isAuthenticated && activeTab === "operations") {
      fetchOperationLogs();
      fetchOperationStats();
    }
  }, [showAnalytics, isAuthenticated, activeTab, logFilter, fetchOperationLogs, fetchOperationStats]);

  const handleOpenAnalytics = () => {
    if (isAuthenticated) {
      setShowAnalytics(true);
    } else {
      setShowLogin(true);
    }
  };

  return (
    <>
      {showCookieConsent && (
        <div className="fixed inset-0 bg-black/60 backdrop-blur-sm z-[100] flex items-end justify-center p-4">
          <div className="bg-gradient-to-br from-gray-900 to-gray-800 text-white rounded-2xl shadow-2xl max-w-2xl w-full p-8 border border-emerald-500/30 animate-slide-up">
            <div className="flex items-start gap-4">
              <div className="flex-shrink-0 w-12 h-12 bg-emerald-500/20 rounded-full flex items-center justify-center">
                <svg className="w-6 h-6 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                </svg>
              </div>
              <div className="flex-1">
                <h3 className="text-xl font-bold mb-2">🍪 我們使用Cookie (We Use Cookies)</h3>
                <p className="text-gray-300 mb-4 leading-relaxed">
                  為了確保網站正常運作並提升您的體驗，我們使用功能性 Cookie。我們也希望使用分析性 (Analytics) 
				  和行銷性 (Marketing) Cookie 來了解您如何使用我們的網站，
				  以便我們優化相關內容。您可隨時拒絕或前往設定管理您的偏好。
                </p>
                <div className="flex gap-3">
                  <button
                    onClick={() => handleCookieConsent(true)}
                    className="flex-1 bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-600 hover:to-teal-700 text-white px-6 py-3 rounded-xl font-semibold transition-all duration-300 hover:scale-105 shadow-lg"
                  >
                    ✓ 接受所有 (Accept All)
                  </button>
                  <button
                    onClick={() => handleCookieConsent(false)}
                    className="flex-1 bg-gray-700 hover:bg-gray-600 text-white px-6 py-3 rounded-xl font-semibold transition-all duration-300"
                  >
                    ✗ 拒絕非必要 (Decline All)
                  </button>
                </div>
                <p className="text-xs text-gray-500 mt-3">
                  您可以隨時在瀏覽器中清除 Cookie 來重置此設定
                </p>
              </div>
            </div>
          </div>
        </div>
      )}

      {showLogin && (
        <AdminLogin 
          onSuccess={handleLoginSuccess} 
          onClose={() => setShowLogin(false)} 
        />
      )}

      <div className="fixed top-2 right-1 z-50">
        {!showAnalytics ? (
          <button
            onClick={handleOpenAnalytics}
            className="bg-gradient-to-r from-emerald-500 to-teal-600 text-white px-6 py-3 rounded-full shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 flex items-center gap-2"
          >
            {isAuthenticated ? "管理儀錶板" : "🔒 管理儀錶板"}
          </button>
        ) : (
          <div className="bg-gray-900 text-white rounded-2xl shadow-2xl w-[900px] max-h-[80vh] overflow-y-auto">
            <div className="sticky top-0 bg-gradient-to-r from-emerald-500 to-teal-600 p-6 rounded-t-2xl z-10">
              <div className="flex justify-between items-center mb-4">
                <h2 className="text-2xl font-bold">管理儀表板</h2>
                <div className="flex items-center gap-3">
                  <button
                    onClick={handleLogout}
                    className="text-white hover:bg-white/20 rounded-full px-4 py-2 transition-colors text-sm flex items-center gap-2"
                  >
                    <svg className="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1" />
                    </svg>
                    登出
                  </button>
                  <button
                    onClick={() => setShowAnalytics(false)}
                    className="text-white hover:bg-white/20 rounded-full p-2 transition-colors"
                  >
                    <svg
                      className="w-6 h-6"
                      fill="none"
                      stroke="currentColor"
                      viewBox="0 0 24 24"
                    >
                      <path
                        strokeLinecap="round"
                        strokeLinejoin="round"
                        strokeWidth={2}
                        d="M6 18L18 6M6 6l12 12"
                      />
                    </svg>
                  </button>
                </div>
              </div>
              
              <div className="flex gap-2 flex-wrap">
                <button
                  onClick={() => setActiveTab("visitors")}
                  className={`px-6 py-2 rounded-lg font-semibold transition-all ${
                    activeTab === "visitors"
                      ? "bg-white text-emerald-600"
                      : "bg-white/20 text-white hover:bg-white/30"
                  }`}
                >
                  📊 訪客分析
                </button>
                <button
                  onClick={() => setActiveTab("operations")}
                  className={`px-6 py-2 rounded-lg font-semibold transition-all ${
                    activeTab === "operations"
                      ? "bg-white text-emerald-600"
                      : "bg-white/20 text-white hover:bg-white/30"
                  }`}
                >
                  📋 操作日誌
                </button>
                <button
                  onClick={() => setActiveTab("knowledgeBase")}
                  className={`px-6 py-2 rounded-lg font-semibold transition-all ${
                    activeTab === "knowledgeBase"
                      ? "bg-white text-emerald-600"
                      : "bg-white/20 text-white hover:bg-white/30"
                  }`}
                >
                  💾 知識庫管理
                </button>
                <button
                  onClick={() => setActiveTab("videos")}
                  className={`px-6 py-2 rounded-lg font-semibold transition-all ${
                    activeTab === "videos"
                      ? "bg-white text-emerald-600"
                      : "bg-white/20 text-white hover:bg-white/30"
                  }`}
                >
                  🎬 影片管理
                </button>
              </div>
            </div>

            <div className="p-6 space-y-6">
              {activeTab === "visitors" ? (
                <AnalyticsCharts
                  visitors={visitors}
                  chartData={chartData}
                  countryData={countryData}
                  timeRange={timeRange}
                  setTimeRange={setTimeRange}
                  loading={loading}
                  totalVisits={totalVisits}
                  uniqueVisitors={uniqueVisitors}
                  comparisonStats={comparisonStats}
                  reachedMilestone={reachedMilestone}
                  exportToXLSX={exportToXLSX}
                  hoveredCountry={hoveredCountry}
                  setHoveredCountry={setHoveredCountry}
                />
              ) : activeTab === "operations" ? (
                <OperationsTab
                  operationStats={operationStats}
                  operationLogs={operationLogs}
                  logsLoading={logsLoading}
                  logFilter={logFilter}
                  setLogFilter={setLogFilter}
                />
              ) : activeTab === "knowledgeBase" ? (
                <KnowledgeBaseManager />
              ) : activeTab === "videos" ? (
                <VideoManager />
              ) : null}
            </div>
          </div>
        )}
      </div>

      <style>{`
        @keyframes slide-up {
          from {
            transform: translateY(100%);
            opacity: 0;
          }
          to {
            transform: translateY(0);
            opacity: 1;
          }
        }
        .animate-slide-up {
          animation: slide-up 0.4s ease-out;
        }
      `}</style>
    </>
  );
};

export default VisitorAnalytics;



================================================================
File Path: src/components/YouTubeGallery.tsx
================================================================

import React, { useState, useEffect, useRef, useCallback, useMemo } from "react"
import {X, Play, ChevronDown, ChevronUp} from 'lucide-react'
import { useLanguage } from "../contexts/LanguageContext"
import VideoImporter from "../services/videoImporter"

interface VideoData {
  id: string
  title: string
  description: string
}

// ==========================//
// 優化的圖片預載入元件
// ==========================//
interface OptimizedThumbnailProps {
  videoId: string
  title: string
  isVisible: boolean
  onLoad?: () => void
}

const OptimizedThumbnail: React.FC<OptimizedThumbnailProps> = ({
  videoId,
  title,
  isVisible,
  onLoad,
}) => {
  const [loaded, setLoaded] = useState(false)
  const [error, setError] = useState(false)
  const imgRef = useRef<HTMLImageElement>(null)

  useEffect(() => {
    if (!isVisible) return

    const img = imgRef.current
    if (!img) return

    const thumbnailUrl = `https://i.ytimg.com/vi/${videoId}/hqdefault.jpg`

    const handleLoad = () => {
      setLoaded(true)
      onLoad?.()
    }

    const handleError = () => {
      setError(true)
      if (img.src.includes("hqdefault")) {
        img.src = `https://i.ytimg.com/vi/${videoId}/mqdefault.jpg`
      }
    }

    img.addEventListener("load", handleLoad)
    img.addEventListener("error", handleError)

    img.src = thumbnailUrl

    return () => {
      img.removeEventListener("load", handleLoad)
      img.removeEventListener("error", handleError)
    }
  }, [isVisible, videoId, onLoad])

  return (
    <>
      {!loaded && (
        <div className="absolute inset-0 bg-gradient-to-br from-gray-100 to-gray-200 animate-pulse">
          <div className="absolute inset-0 flex items-center justify-center">
            <div className="w-12 h-12 border-4 border-emerald-500 border-t-transparent rounded-full animate-spin"></div>
          </div>
        </div>
      )}

      <img
        ref={imgRef}
        alt={title}
        className={`absolute inset-0 w-full h-full object-cover transition-all duration-700 ${
          loaded ? "opacity-100 scale-100" : "opacity-0 scale-95"
        }`}
        style={{ display: isVisible ? "block" : "none" }}
      />

      {!loaded && (
        <div className="absolute inset-0 overflow-hidden">
          <div
            className="absolute inset-0 -translate-x-full animate-shimmer bg-gradient-to-r from-transparent via-white/20 to-transparent"
            style={{
              animation: "shimmer 2s infinite",
            }}
          />
        </div>
      )}

      <style>{`
        @keyframes shimmer {
          100% {
            transform: translateX(100%);
          }
        }
      `}</style>
    </>
  )
}

// ==========================//
// 可折疊影片卡片元件（手機專用）
// ==========================//
interface CollapsibleVideoCardProps {
  video: VideoData
  isExpanded: boolean
  onToggle: () => void
  isVisible: boolean
  onThumbnailLoad: () => void
}

const CollapsibleVideoCard: React.FC<CollapsibleVideoCardProps> = ({
  video,
  isExpanded,
  onToggle,
  isVisible,
  onThumbnailLoad,
}) => {
  return (
    <div className="bg-white rounded-xl overflow-hidden shadow-lg border-2 border-emerald-100">
      {/* 標題欄（可點擊） */}
      <button
        onClick={onToggle}
        className="w-full flex items-center justify-between p-4 hover:bg-emerald-50 transition-colors duration-200"
      >
        <div className="flex items-center gap-3 flex-1 min-w-0">
          {/* 縮圖 */}
          <div className="relative w-20 h-12 rounded-lg overflow-hidden flex-shrink-0 bg-gray-200">
            <OptimizedThumbnail
              videoId={video.id}
              title={video.title}
              isVisible={isVisible}
              onLoad={onThumbnailLoad}
            />
          </div>
          {/* 標題 */}
          <div className="text-left flex-1 min-w-0">
            <h3 className="font-semibold text-gray-900 text-sm line-clamp-2">
              {video.title}
            </h3>
          </div>
        </div>
        {/* 展開/收合圖示 */}
        <div className="ml-2 flex-shrink-0">
          {isExpanded ? (
            <ChevronUp className="w-6 h-6 text-emerald-600" />
          ) : (
            <ChevronDown className="w-6 h-6 text-emerald-600" />
          )}
        </div>
      </button>

      {/* 影片播放器（展開時顯示） */}
      {isExpanded && (
        <div className="border-t border-emerald-100">
          <div className="relative w-full" style={{ paddingBottom: "56.25%" }}>
            <iframe
              src={`https://www.youtube.com/embed/${video.id}?rel=0&modestbranding=1`}
              className="absolute top-0 left-0 w-full h-full"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowFullScreen
              title={video.title}
              loading="lazy"
            />
          </div>
          {/* 描述 */}
          {video.description && (
            <div className="p-4 bg-emerald-50">
              <p className="text-sm text-gray-700">{video.description}</p>
            </div>
          )}
        </div>
      )}
    </div>
  )
}

// =======================//
// 主元件
// =======================//
const YouTubeGallery: React.FC = () => {
  const { t, language } = useLanguage()
  const videoImporter = VideoImporter.getInstance()
  
  // 使用 state 儲存影片列表
  const [galleryVideos, setGalleryVideos] = useState(() => 
    videoImporter.getGalleryVideos()
  )

  // 訂閱 VideoImporter 更新事件
  useEffect(() => {
    const unsubscribe = videoImporter.subscribe(() => {
      setGalleryVideos(videoImporter.getGalleryVideos())
    })
    return unsubscribe
  }, [videoImporter])
  
  const videos: VideoData[] = useMemo(() => 
    galleryVideos.map(v => ({
      id: v.videoId,
      title: language === 'zh' ? v.title_zh : v.title_en,
      description: language === 'zh' ? v.description_zh : v.description_en
    })), [galleryVideos, language])

  const [selectedVideo, setSelectedVideo] = useState<string | null>(null)
  const [hoveredVideo, setHoveredVideo] = useState<string | null>(null)
  const [visibleVideos, setVisibleVideos] = useState<Set<string>>(new Set())
  const [loadedCount, setLoadedCount] = useState(0)
  const [expandedVideos, setExpandedVideos] = useState<Set<string>>(new Set())
  const [isMobile, setIsMobile] = useState(false)
  const observerRef = useRef<IntersectionObserver | null>(null)
  const hoverTimeoutRef = useRef<NodeJS.Timeout | null>(null)
  const videoRefs = useRef<Map<string, HTMLDivElement>>(new Map())

  // 檢測是否為手機
  useEffect(() => {
    const checkMobile = () => {
      setIsMobile(window.innerWidth < 768)
    }
    checkMobile()
    window.addEventListener("resize", checkMobile)
    return () => window.removeEventListener("resize", checkMobile)
  }, [])

  // 優化的懶加載設置
  useEffect(() => {
    const initialVideos = videos.map((v) => v.id)
    setVisibleVideos(new Set(initialVideos))

    observerRef.current = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          const videoId = entry.target.getAttribute("data-video-id")
          if (!videoId) return

          if (entry.isIntersecting) {
            setVisibleVideos((prev) => {
              if (prev.has(videoId)) return prev
              const newSet = new Set(prev)
              newSet.add(videoId)
              return newSet
            })
          }
        })
      },
      {
        rootMargin: "100px",
        threshold: 0.01,
      }
    )

    return () => {
      if (observerRef.current) {
        observerRef.current.disconnect()
      }
    }
  }, [videos.length])

  const registerVideoRef = useCallback((videoId: string, element: HTMLDivElement | null) => {
    if (element) {
      videoRefs.current.set(videoId, element)
      if (observerRef.current) {
        observerRef.current.observe(element)
      }
    }
  }, [])

  const handleMouseEnter = (videoId: string) => {
    if (isMobile) return
    hoverTimeoutRef.current = setTimeout(() => {
      setHoveredVideo(videoId)
    }, 1000)
  }

  const handleMouseLeave = () => {
    if (hoverTimeoutRef.current) {
      clearTimeout(hoverTimeoutRef.current)
    }
    setHoveredVideo(null)
  }

  const handleThumbnailLoad = useCallback(() => {
    setLoadedCount((prev) => prev + 1)
  }, [])

  const toggleVideoExpansion = useCallback((videoId: string) => {
    setExpandedVideos((prev) => {
      const newSet = new Set(prev)
      if (newSet.has(videoId)) {
        newSet.delete(videoId)
      } else {
        newSet.add(videoId)
      }
      return newSet
    })
  }, [])

  const expandAll = useCallback(() => {
    setExpandedVideos(new Set(videos.map((v) => v.id)))
  }, [videos])

  const collapseAll = useCallback(() => {
    setExpandedVideos(new Set())
  }, [])

  useEffect(() => {
    const handleEsc = (e: KeyboardEvent) => {
      if (e.key === "Escape" && selectedVideo) {
        setSelectedVideo(null)
      }
    }
    window.addEventListener("keydown", handleEsc)
    return () => window.removeEventListener("keydown", handleEsc)
  }, [selectedVideo])

  useEffect(() => {
    if (selectedVideo) {
      document.body.style.overflow = "hidden"
    } else {
      document.body.style.overflow = ""
    }
    return () => {
      document.body.style.overflow = ""
    }
  }, [selectedVideo])

  return (
    <section id="youtube-gallery" className="py-20 bg-white">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-16 animate-on-scroll">
          <h2 className="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
            {t("youtube.title")}
          </h2>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto">
            {t("youtube.subtitle")}
          </p>
          {loadedCount < videos.length && (
            <div className="mt-4 text-sm text-gray-500">
              載入中... {loadedCount} / {videos.length}
            </div>
          )}
        </div>

        {/* 手機版：全部展開/收合按鈕 */}
        {isMobile && (
          <div className="flex gap-3 mb-6 justify-center">
            <button
              onClick={expandAll}
              className="px-4 py-2 bg-emerald-600 text-white rounded-lg font-semibold hover:bg-emerald-700 transition-colors duration-200 text-sm"
            >
              全部展開
            </button>
            <button
              onClick={collapseAll}
              className="px-4 py-2 bg-gray-600 text-white rounded-lg font-semibold hover:bg-gray-700 transition-colors duration-200 text-sm"
            >
              全部收合
            </button>
          </div>
        )}

        {/* 影片網格 */}
        <div className={`grid ${isMobile ? 'grid-cols-1 gap-4' : 'grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6'}`}>
          {videos.map((video, index) => {
            const isVisible = visibleVideos.has(video.id)
            const isHovered = hoveredVideo === video.id
            const isExpanded = expandedVideos.has(video.id)

            // 手機版：使用可折疊卡片
            if (isMobile) {
              return (
                <div
                  key={video.id}
                  data-video-id={video.id}
                  ref={(el) => registerVideoRef(video.id, el)}
                  className="animate-on-scroll"
                  style={{
                    animationDelay: `${index * 0.05}s`,
                  }}
                >
                  <CollapsibleVideoCard
                    video={video}
                    isExpanded={isExpanded}
                    onToggle={() => toggleVideoExpansion(video.id)}
                    isVisible={isVisible}
                    onThumbnailLoad={handleThumbnailLoad}
                  />
                </div>
              )
            }

            // 桌面版：保持原樣
            return (
              <div
                key={video.id}
                data-video-id={video.id}
                ref={(el) => registerVideoRef(video.id, el)}
                className="group relative aspect-video rounded-xl overflow-hidden cursor-pointer shadow-lg hover:shadow-2xl transform transition-all duration-500 hover:scale-105 animate-on-scroll"
                style={{
                  animationDelay: `${index * 0.05}s`,
                }}
                onMouseEnter={() => handleMouseEnter(video.id)}
                onMouseLeave={handleMouseLeave}
                onClick={() => setSelectedVideo(video.id)}
              >
                <div className="absolute inset-0 bg-gradient-to-br from-emerald-400 via-emerald-500 to-emerald-600 rounded-xl p-[2px] group-hover:p-[3px] transition-all duration-300">
                  <div className="absolute inset-0 bg-white rounded-xl"></div>
                </div>

                <div className="absolute inset-0 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-500 pointer-events-none">
                  <div className="absolute inset-0 bg-emerald-500/20 blur-xl"></div>
                </div>

                <div className="relative h-full rounded-2xl overflow-hidden">
                  <OptimizedThumbnail
                    videoId={video.id}
                    title={video.title}
                    isVisible={isVisible}
                    onLoad={handleThumbnailLoad}
                  />

                  {isHovered && isVisible && (
                    <div className="absolute inset-0 bg-black z-10">
                      <iframe
                        src={`https://www.youtube.com/embed/${video.id}?autoplay=1&mute=1&controls=0&loop=1&playlist=${video.id}&modestbranding=1&rel=0`}
                        className="w-full h-full"
                        allow="autoplay; encrypted-media"
                        allowFullScreen
                        title={video.title}
                        loading="lazy"
                      />
                    </div>
                  )}

                  {!isHovered && (
                    <div className="absolute inset-0 flex items-center justify-center bg-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none">
                      <div className="w-16 h-16 bg-white/90 rounded-full flex items-center justify-center transform group-hover:scale-110 transition-transform duration-300">
                        <Play
                          className="w-8 h-8 text-emerald-600 ml-1"
                          fill="currentColor"
                        />
                      </div>
                    </div>
                  )}

                  <div className="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent p-4 transform translate-y-full group-hover:translate-y-0 transition-transform duration-300 pointer-events-none">
                    <h3 className="text-white font-semibold text-sm mb-1 line-clamp-1">
                      {video.title}
                    </h3>
                    <p className="text-gray-300 text-xs line-clamp-2">
                      {video.description}
                    </p>
                  </div>
                </div>
              </div>
            )
          })}
        </div>
      </div>

      {/* 全屏播放模態框（桌面版） */}
      {selectedVideo && !isMobile && (
        <div
          className="fixed inset-0 bg-black/95 z-50 flex items-center justify-center p-4 animate-fadeIn"
          onClick={() => setSelectedVideo(null)}
        >
          <button
            className="absolute top-4 right-4 text-white hover:text-emerald-400 transition-colors duration-200 z-10 w-10 h-10 flex items-center justify-center rounded-full bg-black/50 hover:bg-black/70"
            onClick={() => setSelectedVideo(null)}
            aria-label="關閉影片"
          >
            <X className="w-6 h-6" />
          </button>
          <div
            className="w-full max-w-5xl aspect-video rounded-xl overflow-hidden shadow-2xl"
            onClick={(e) => e.stopPropagation()}
          >
            <iframe
              src={`https://www.youtube.com/embed/${selectedVideo}?autoplay=1&rel=0&modestbranding=1`}
              className="w-full h-full"
              allow="autoplay; encrypted-media; fullscreen"
              allowFullScreen
              title="YouTube video player"
            />
          </div>
        </div>
      )}
    </section>
  )
}

export default YouTubeGallery


================================================================
File Path: src/components/ChatBot/CategorySelector.tsx
================================================================

 
import React, { useState } from 'react';
import { useLanguage } from '../../contexts/LanguageContext';
import { getCategories, getQuestionsByCategory } from '../../services/knowledgeBase';
import {ChevronDown, ChevronUp} from 'lucide-react';

interface CategorySelectorProps {
  selectedCategory: string | null;
  onCategorySelect: (category: string) => void;
  onQuestionSelect: (question: string) => void;
}

const CategorySelector: React.FC<CategorySelectorProps> = ({
  selectedCategory,
  onCategorySelect,
  onQuestionSelect
}) => {
  const { language } = useLanguage();
  const categories = getCategories(language);
  const [isExpanded, setIsExpanded] = useState(true);
  const [isQuestionsExpanded, setIsQuestionsExpanded] = useState(true);

  if (selectedCategory) {
    const questions = getQuestionsByCategory(selectedCategory, language);
    
    return (
      <div className="bg-white border-b border-gray-200">
        <div className="flex items-center justify-between p-4">
          <div className="flex items-center space-x-2">
            <h4 className="font-medium text-gray-800 text-sm">
              {selectedCategory}
            </h4>
            <button
              onClick={() => setIsQuestionsExpanded(!isQuestionsExpanded)}
              className="p-1 hover:bg-gray-100 rounded transition-colors"
            >
              {isQuestionsExpanded ? (
                <ChevronUp className="w-4 h-4 text-gray-600" />
              ) : (
                <ChevronDown className="w-4 h-4 text-gray-600" />
              )}
            </button>
          </div>
          <button
            onClick={() => onCategorySelect('')}
            className="text-xs text-green-600 hover:text-green-700 font-medium"
          >
            {language === 'zh' ? '返回分類' : 'Back to Categories'}
          </button>
        </div>
        
        {isQuestionsExpanded && (
          <div className="px-4 pb-4 space-y-2 max-h-40 overflow-y-auto">
            {questions.map((item, index) => (
              <button
                key={index}
                onClick={() => onQuestionSelect(item.question)}
                className="w-full text-left text-xs text-gray-600 hover:text-green-600 hover:bg-green-50 p-2 rounded-md transition-colors border border-gray-100 hover:border-green-200"
              >
                {item.question}
              </button>
            ))}
          </div>
        )}
      </div>
    );
  }

  return (
    <div className="bg-white border-b border-gray-200">
      <button
        onClick={() => setIsExpanded(!isExpanded)}
        className="w-full flex items-center justify-between p-4 hover:bg-gray-50 transition-colors"
      >
        <h4 className="font-medium text-gray-800 text-sm">
          {language === 'zh' ? '常見問題' : 'Frequently Asked Questions'}
        </h4>
        {isExpanded ? (
          <ChevronUp className="w-4 h-4 text-gray-600" />
        ) : (
          <ChevronDown className="w-4 h-4 text-gray-600" />
        )}
      </button>
      
      {isExpanded && (
        <div className="px-4 pb-4">
          <div className="grid grid-cols-2 gap-2">
            {categories.map((category, index) => (
              <button
                key={index}
                onClick={() => onCategorySelect(category)}
                className="text-xs text-gray-600 hover:text-green-600 hover:bg-green-50 p-2 rounded-md transition-colors border border-gray-100 hover:border-green-200 text-left"
              >
                {category}
              </button>
            ))}
          </div>
        </div>
      )}
    </div>
  );
};

export default CategorySelector; 



================================================================
File Path: src/components/ChatBot/ChatAvatar.tsx
================================================================

import React from 'react';

interface ChatAvatarProps {
  size?: 'small' | 'normal' | 'large';
  animate?: boolean;
}

const ChatAvatar: React.FC<ChatAvatarProps> = ({ 
  size = 'normal', 
  animate = true 
}) => {
  const getSizeClasses = () => {
    switch (size) {
      case 'small':
        return 'w-8 h-8 text-xs';
      case 'large':
        return 'w-14 h-14 text-lg';
      default:
        return 'w-10 h-10 text-sm';
    }
  };
  
  return (
    <div className={`${getSizeClasses()} bg-gradient-to-br from-green-100 via-emerald-50 to-green-200 rounded-full border-2 border-green-400 flex items-center justify-center shadow-lg relative overflow-hidden flex-shrink-0`}>
      {/* 虛擬園藝客服人像 */}
      <div className={`relative z-10 ${animate ? 'animate-pulse' : ''} flex items-center justify-center`}>
        {/* 主要人像 - 園藝師女性形象 */}
        <div className="relative">
          {/* 臉部 */}
          <div className="w-6 h-6 bg-gradient-to-b from-amber-100 to-amber-200 rounded-full border border-amber-300 flex items-center justify-center relative">
            {/* 眼睛 */}
            <div className="flex space-x-1 mb-1">
              <div className="w-1 h-1 bg-gray-700 rounded-full"></div>
              <div className="w-1 h-1 bg-gray-700 rounded-full"></div>
            </div>
            {/* 微笑 */}
            <div className="absolute bottom-1 left-1/2 transform -translate-x-1/2 w-2 h-1 border-b border-gray-600 rounded-full"></div>
          </div>
          
          {/* 頭髮 - 園藝師帽子 */}
          <div className="absolute -top-1 left-1/2 transform -translate-x-1/2 w-7 h-3 bg-gradient-to-r from-green-600 to-green-500 rounded-t-full border border-green-700">
            {/* 身體 - 園藝圍裙 */}
            <div className="absolute top-5 left-1/2 transform -translate-x-1/2 w-4 h-2 bg-gradient-to-b from-green-300 to-green-400 rounded-b border border-green-500"></div>
          </div>
        </div>
      </div>
      
      {/* 背景動畫層 */}
      {animate && (
        <>
          <div className="absolute inset-0 bg-gradient-to-t from-green-300/30 to-transparent rounded-full animate-ping opacity-75"></div>
          <div className="absolute inset-0 bg-gradient-radial from-green-200/40 to-transparent rounded-full animate-pulse"></div>
        </>
      )}
      
      {/* 光暈效果 */}
      <div className="absolute -inset-1 bg-gradient-to-r from-green-400/20 to-emerald-400/20 rounded-full blur-sm animate-pulse"></div>
      
      {/* 專業園藝師光環效果 */}
      {animate && size !== 'small' && (
        <div className="absolute -top-1 -right-1 w-3 h-3">
          <div className="w-full h-full bg-yellow-300 rounded-full animate-bounce opacity-60 flex items-center justify-center text-xs">
          </div>
        </div>
      )}
    </div>
  );
};

export default ChatAvatar;
 



================================================================
File Path: src/components/ChatBot/ChatBot.tsx
================================================================

import React, { useState, useEffect, useRef } from 'react';
import {MessageCircleDashed as MessageCircle, X, Send, RotateCcw} from 'lucide-react';
import { useLanguage } from '../../contexts/LanguageContext';
import { searchKnowledge, getRandomResponse } from '../../services/knowledgeBase';
import ChatMessage from './ChatMessage';
import ChatInput from './ChatInput';
import ChatAvatar from './ChatAvatar';
import CategorySelector from './CategorySelector';
import NoResultsMessage from './NoResultsMessage';

interface Message {
  id: string;
  type: 'user' | 'bot';
  content: string;
  timestamp: Date;
  isTyping?: boolean;
}

const ChatBot: React.FC = () => {
  const { language } = useLanguage();
  const [isOpen, setIsOpen] = useState(false);
  const [messages, setMessages] = useState<Message[]>([]);
  const [isTyping, setIsTyping] = useState(false);
  const [selectedCategory, setSelectedCategory] = useState<string | null>(null);
  const messagesEndRef = useRef<HTMLDivElement>(null);
  const audioRef = useRef<HTMLAudioElement | null>(null);
  const isPlayingRef = useRef(false);

  const scrollToBottom = () => {
    messagesEndRef.current?.scrollIntoView({ behavior: 'smooth' });
  };

  useEffect(() => {
    scrollToBottom();
  }, [messages]);

  useEffect(() => {
    if (isOpen && messages.length === 0) {
      const welcomeMessage: Message = {
        id: Date.now().toString(),
        type: 'bot',
        content: language === 'zh' 
          ? '您好!我是景觀設計助手,很高興為您服務!\n\n我可以幫您解答關於:\n• 植栽養護\n• 景觀設計\n• 施工作業\n• 付款條件\n• 社區承作\n• 菁英高階服務\n\n請告訴我您想了解什麼?'
          : 'Hello! I\'m your landscape design assistant, happy to help!\n\nI can answer questions about:\n• Plant Care\n• Landscape Design\n• Construction\n• Payment Terms\n• Community Projects\n• Premium Services\n\nWhat would you like to know?',
        timestamp: new Date()
      };
      setMessages([welcomeMessage]);
    }
  }, [isOpen, language]);

  const handleMouseEnter = () => {
    if (isPlayingRef.current) return;
    
    // 根據語系選擇不同的音頻檔案
    const audioUrl = language === 'zh' 
      ? 'https://raw.githubusercontent.com/jojoyo37198/audio/refs/heads/main/DRGrant_CH.mp3'
      : 'https://raw.githubusercontent.com/jojoyo37198/audio/refs/heads/main/DRGrant.mp3'; 
    
    const audio = new Audio(audioUrl);
    audioRef.current = audio;
    isPlayingRef.current = true;
    
    audio.play().catch(err => console.log('Audio play failed:', err));
    
    audio.onended = () => {
      isPlayingRef.current = false;
      audioRef.current = null;
    };
  };

  const handleSendMessage = async (content: string) => {
    if (!content.trim()) return;

    // 添加用戶消息
    const userMessage: Message = {
      id: Date.now().toString(),
      type: 'user',
      content: content.trim(),
      timestamp: new Date()
    };

    setMessages(prev => [...prev, userMessage]);
    setIsTyping(true);

    // 模擬思考時間
    await new Promise(resolve => setTimeout(resolve, 800 + Math.random() * 700));

    // 搜索知識庫
    const knowledge = searchKnowledge(content, language);
    const response = knowledge ? knowledge.answer : getRandomResponse(language);

    // 添加機器人回應
    const botMessage: Message = {
      id: (Date.now() + 1).toString(),
      type: 'bot',
      content: response,
      timestamp: new Date()
    };

    setIsTyping(false);
    setMessages(prev => [...prev, botMessage]);
  };

  const handleCategorySelect = (category: string) => {
    setSelectedCategory(category);
  };

  const handleQuestionSelect = (question: string) => {
    handleSendMessage(question);
  };

  const handleReset = () => {
    setMessages([]);
    setSelectedCategory(null);
    setIsTyping(false);
  };

  if (!isOpen) {
    return (
      <button
        onClick={() => setIsOpen(true)}
        onMouseEnter={handleMouseEnter}
        className="fixed bottom-6 right-6 transform hover:scale-105 transition-all duration-200 z-40 group"
      >
        <img 
          src="https://i.ibb.co/wZfhQSBs/OK.webp"
          alt="Landscape Assistant"
          className="w-[200px] h-[200px] object-contain"
        />
        <div className="absolute top-0 left-1/2 -translate-x-1/2 bg-gray-800 text-white px-3 py-1 rounded-lg text-sm opacity-0 group-hover:opacity-100 transition-opacity whitespace-nowrap">
          {language === 'zh' ? '我是Dr. Grant，專業景觀顧問' : 'Landscape Consultation'}
        </div>
      </button>
    );
  }

  return (
    <>
      <div className="fixed bottom-6 right-6 w-96 h-[600px] bg-white rounded-2xl shadow-2xl flex flex-col z-40 border border-gray-200">
        {/* 標題欄 */}
        <div className="bg-gradient-to-r from-green-600 to-emerald-600 text-white p-4 rounded-t-2xl flex items-center justify-between">
          <div className="flex items-center space-x-3">
            <ChatAvatar />
            <div>
              <h3 className="font-semibold text-sm">
                {language === 'zh' ? '景觀設計助手' : 'Landscape Assistant'}
              </h3>
              <p className="text-xs text-green-100">
                {language === 'zh' ? '線上為您服務' : 'Online to help you'}
              </p>
            </div>
          </div>
          
          <div className="flex items-center space-x-2">
            {/* 重置按鈕 */}
            <button
              onClick={handleReset}
              className="p-2 rounded-full hover:bg-white hover:bg-opacity-20 transition-colors"
              title={language === 'zh' ? '重新開始' : 'Reset Chat'}
            >
              <RotateCcw className="w-4 h-4" />
            </button>

            {/* 關閉按鈕 */}
            <button
              onClick={() => setIsOpen(false)}
              className="p-2 rounded-full hover:bg-white hover:bg-opacity-20 transition-colors"
            >
              <X className="w-4 h-4" />
            </button>
          </div>
        </div>

        {/* 常見問題選擇器 */}
        <CategorySelector
          selectedCategory={selectedCategory}
          onCategorySelect={handleCategorySelect}
          onQuestionSelect={handleQuestionSelect}
        />

        {/* 消息區域 */}
        <div className="flex-1 overflow-y-auto p-4 space-y-4 bg-gray-50">
          {messages.map((message) => (
            <ChatMessage key={message.id} message={message} />
          ))}
          
          {isTyping && (
            <div className="flex items-start space-x-3">
              <ChatAvatar size="sm" />
              <div className="bg-white rounded-2xl rounded-tl-md p-3 shadow-sm border max-w-[80%]">
                <div className="flex space-x-1">
                  <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce"></div>
                  <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce" style={{ animationDelay: '0.1s' }}></div>
                  <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce" style={{ animationDelay: '0.2s' }}></div>
                </div>
              </div>
            </div>
          )}

          {messages.length === 1 && messages[0].type === 'bot' && (
            <NoResultsMessage />
          )}

          <div ref={messagesEndRef} />
        </div>

        {/* 輸入區域 */}
        <div className="border-t border-gray-200 p-4">
          <ChatInput onSendMessage={handleSendMessage} disabled={isTyping} />
        </div>
      </div>
    </>
  );
};

export default ChatBot;



================================================================
File Path: src/components/ChatBot/ChatInput.tsx
================================================================

import React, { useState, useRef, useEffect } from "react";
import {Send} from 'lucide-react';

interface ChatInputProps {
  onSendMessage: (message: string) => void;
  disabled?: boolean;
  language?: "zh" | "en";
}

const ChatInput: React.FC<ChatInputProps> = ({ 
  onSendMessage, 
  disabled = false,
  language = "zh"
}) => {
  const [inputValue, setInputValue] = useState("");
  const inputRef = useRef<HTMLInputElement>(null);

  const placeholder = language === "zh" 
    ? "輸入您的園藝問題..." 
    : "Type your gardening question...";

  useEffect(() => {
    if (!disabled) {
      inputRef.current?.focus();
    }
  }, [disabled]);

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    const trimmedValue = inputValue.trim();
    
    if (trimmedValue && !disabled) {
      onSendMessage(trimmedValue);
      setInputValue("");
    }
  };

  const handleKeyDown = (e: React.KeyboardEvent) => {
    if (e.key === "Enter" && !e.shiftKey) {
      e.preventDefault();
      handleSubmit(e);
    }
  };

  const handleInputChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    setInputValue(e.target.value);
  };

  return (
    <div className="border-t border-gray-200 bg-white">
      {/* 輸入區域 */}
      <form onSubmit={handleSubmit} className="p-4">
        <div className="flex items-center space-x-3">
          {/* 輸入框 */}
          <div className="flex-1 relative">
            <input
              ref={inputRef}
              type="text"
              value={inputValue}
              onChange={handleInputChange}
              onKeyDown={handleKeyDown}
              placeholder={placeholder}
              disabled={disabled}
              maxLength={500}
              // className="w-full px-4 py-3 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent disabled:bg-gray-100 disabled:cursor-not-allowed transition-all duration-200"
			  className="w-full px-4 py-3 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent disabled:bg-gray-100 disabled:cursor-not-allowed transition-all duration-200 text-gray-900"
            />
            
            {/* 字符計數 */}
            {inputValue.length > 400 && (
              <div className="absolute -top-6 right-0 text-xs text-gray-400">
                {inputValue.length}/500
              </div>
            )}
          </div>

          {/* 發送按鈕 */}
          <button
            type="submit"
            disabled={!inputValue.trim() || disabled}
            className="bg-gradient-to-r from-green-500 to-green-600 text-white p-3 rounded-full hover:from-green-600 hover:to-green-700 disabled:from-gray-300 disabled:to-gray-400 disabled:cursor-not-allowed transform hover:scale-105 transition-all duration-200 shadow-lg hover:shadow-xl"
          >
            <Send size={18} />
          </button>
        </div>
      </form>
    </div>
  );
};

export default ChatInput; 



================================================================
File Path: src/components/ChatBot/ChatMessage.tsx
================================================================

import React from "react";
import ChatAvatar from "./ChatAvatar";

interface Message {
  id: string;
  type: "user" | "bot";
  content: string;
  timestamp: Date;
  isTyping?: boolean;
}

interface ChatMessageProps {
  message: Message;
}

const ChatMessage: React.FC<ChatMessageProps> = ({ message }) => {
  const formatContent = (content: string) => {
    return content.split("\n").map((line, index) => (
      <span key={index}>
        {line}
        {index < content.split("\n").length - 1 && <br />}
      </span>
    ));
  };

  const formatTime = (date: Date) => {
    return date.toLocaleTimeString("zh-TW", {
      hour: "2-digit",
      minute: "2-digit"
    });
  };

  if (message.type === "bot") {
    return (
      <div className="flex items-start space-x-3 animate-fade-in">
        <ChatAvatar size="sm" />
        <div className="bg-white rounded-2xl rounded-tl-md p-4 shadow-sm border max-w-[85%] min-h-[40px]">
          <div className="text-gray-800 text-sm leading-relaxed whitespace-pre-wrap">
            {formatContent(message.content)}
          </div>
          <div className="text-xs text-gray-400 mt-2">
            {formatTime(message.timestamp)}
          </div>
        </div>
      </div>
    );
  }

  return (
    <div className="flex items-start space-x-3 justify-end animate-fade-in">
      <div className="bg-gradient-to-r from-green-600 to-emerald-600 text-white rounded-2xl rounded-tr-md p-4 shadow-sm max-w-[85%] min-h-[40px]">
        <div className="text-sm leading-relaxed whitespace-pre-wrap">
          {formatContent(message.content)}
        </div>
        <div className="text-xs text-green-100 mt-2 text-right">
          {formatTime(message.timestamp)}
        </div>
      </div>
      <div className="w-8 h-8 bg-gray-300 rounded-full flex items-center justify-center flex-shrink-0">
        <span className="text-xs font-medium text-gray-600">您</span>
      </div>
    </div>
  );
};

export default ChatMessage;
 



================================================================
File Path: src/components/ChatBot/NoResultsMessage.tsx
================================================================

import React from 'react';
import { useLanguage } from '../../contexts/LanguageContext';

interface NoResultsMessageProps {
  message: string;
}

const NoResultsMessage: React.FC<NoResultsMessageProps> = ({ message }) => {
  const { language } = useLanguage();

  return (
    <div className="bg-gradient-to-r from-orange-50 to-yellow-50 border border-orange-200 rounded-2xl rounded-tl-md px-4 py-3 shadow-sm">
      <div className="flex items-start space-x-2">
        <span className="text-orange-500 text-lg flex-shrink-0">🤔</span>
        <div className="flex-1">
          <p className="whitespace-pre-line leading-relaxed text-gray-700">
            {message}
          </p>
          
          {/* 快速操作按鈕 */}
          <div className="mt-3 flex flex-wrap gap-2">
          {/*  <button className="text-xs px-3 py-1 bg-green-100 text-green-700 rounded-full border border-green-200 hover:bg-green-200 transition-colors">
              {language === 'zh' ? '📞 聯繫專家' : '📞 Contact Expert'}
            </button> 
          */}

          <button
    onClick={() => window.open('https://line.me/R/oa/call/@055hjhgm?confirmation=true&from=call_url', '_blank')}
    className="text-xs px-3 py-1 bg-green-100 text-green-700 rounded-full border border-green-200 hover:bg-green-200 transition-colors"
  >
    {language === 'zh' ? '📞 聯繫專家' : '📞 Contact Expert'}
  </button>

            <button className="text-xs px-3 py-1 bg-blue-100 text-blue-700 rounded-full border border-blue-200 hover:bg-blue-200 transition-colors">
              {language === 'zh' ? '📋 常見問題' : '📋 FAQ'}
            </button>
            <button className="text-xs px-3 py-1 bg-purple-100 text-purple-700 rounded-full border border-purple-200 hover:bg-purple-200 transition-colors">
              {language === 'zh' ? '💬 重新提問' : '💬 Ask Again'}
            </button>
          </div>
        </div>
      </div>
    </div>
  );
};

export default NoResultsMessage;



================================================================
File Path: src/constants/analyticsConstants.ts
================================================================

import { supabase } from "../lib/supabase";

export interface VisitorLog {
  id: number;
  ip_address: string;
  country: string | null;
  city: string | null;
  visit_count: number;
  first_visit: string;
  last_visit: string;
  user_agent: string | null;
  created_at: string;
}

export interface ChartData {
  date: string;
  count: number;
  compareCount?: number;
}

export interface CountryData {
  country: string;
  count: number;
  visitors: number;
}

export interface ComparisonStats {
  currentTotal: number;
  previousTotal: number;
  changePercent: number;
  changeType: "increase" | "decrease" | "neutral";
}

export interface OperationLog {
  id: number;
  username: string;
  operation_type: string;
  operation_detail: string;
  ip_address: string;
  user_agent: string;
  created_at: string;
}

export interface OperationStats {
  total_operations: number;
  login_success: number;
  login_failed: number;
  login_blocked: number;
  today_operations: number;
  last_7_days: number;
}

export type TimeRange = "week" | "twoWeeks" | "month" | "year";
export type DashboardTab = "visitors" | "operations" | "knowledge" | "videos";  // ← 加了 "videos"

export const COUNTRY_NAME_MAP: { [key: string]: string } = {
  "United States of America": "United States",
  "USA": "United States",
  "US": "United States",
  "UK": "United Kingdom",
  "Great Britain": "United Kingdom",
  "Holland": "Netherlands",
  "UAE": "United Arab Emirates",
  "South Korea": "South Korea",
  "Korea, Republic of": "South Korea",
  "Korea, Democratic People's Republic of": "North Korea",
  "Viet Nam": "Vietnam",
  "Czech Republic": "Czech Republic",
  "Czechia": "Czech Republic",
  "Macedonia": "North Macedonia",
  "Burma": "Myanmar",
  "Ivory Coast": "Côte d'Ivoire",
  "Côte d'Ivoire": "Côte d'Ivoire",
  "Republic of the Congo": "Congo",
  "Democratic Republic of the Congo": "DR Congo",
  "DRC": "DR Congo",
  "Congo-Kinshasa": "DR Congo",
  "Congo-Brazzaville": "Congo",
  "Laos": "Lao PDR",
  "Lao People's Democratic Republic": "Lao PDR",
  "East Timor": "Timor-Leste",
  "Swaziland": "Eswatini",
  "The Gambia": "Gambia",
  "The Bahamas": "Bahamas",
  "Cape Verde": "Cabo Verde",
  "São Tomé and Príncipe": "Sao Tome and Principe",
  "Bosnia": "Bosnia and Herzegovina",
  "Herzegovina": "Bosnia and Herzegovina",
  "Trinidad": "Trinidad and Tobago",
  "Saint Kitts": "Saint Kitts and Nevis",
  "Saint Vincent": "Saint Vincent and the Grenadines",
  "Antigua": "Antigua and Barbuda",
  "Vatican": "Vatican City",
  "Holy See": "Vatican City",
  "Brunei Darussalam": "Brunei",
  "Micronesia": "Federated States of Micronesia",
  "FSM": "Federated States of Micronesia",
  "Marshall Islands": "Marshall Islands",
  "Palau": "Palau",
  "Solomon Islands": "Solomon Islands",
  "Kiribati": "Kiribati",
  "Tuvalu": "Tuvalu",
  "Nauru": "Nauru",
  "Vanuatu": "Vanuatu",
  "Fiji": "Fiji",
  "Samoa": "Samoa",
  "Tonga": "Tonga",
};

export const WORLD_MAP_PATHS: { [key: string]: string } = {
  "United States": "M100,150 L250,150 L250,250 L100,250 Z",
  "Canada": "M100,80 L280,80 L280,140 L100,140 Z",
  "Mexico": "M120,220 L180,220 L180,260 L120,260 Z",
  "Guatemala": "M175,255 L200,255 L200,270 L175,270 Z",
  "Belize": "M200,255 L210,255 L210,265 L200,265 Z",
  "El Salvador": "M190,260 L210,260 L210,270 L190,270 Z",
  "Honduras": "M185,255 L210,255 L210,265 L185,265 Z",
  "Nicaragua": "M195,265 L220,265 L220,280 L195,280 Z",
  "Costa Rica": "M200,265 L220,265 L220,275 L200,275 Z",
  "Panama": "M215,275 L240,275 L240,282 L215,282 Z",
  "Cuba": "M200,240 L250,240 L250,250 L200,250 Z",
  "Jamaica": "M220,250 L235,250 L235,258 L220,258 Z",
  "Haiti": "M235,245 L250,245 L250,255 L235,255 Z",
  "Dominican Republic": "M240,245 L260,245 L260,255 L240,255 Z",
  "Bahamas": "M250,230 L270,230 L270,245 L250,245 Z",
  "Trinidad and Tobago": "M270,265 L280,265 L280,272 L270,272 Z",
  "Barbados": "M275,268 L280,268 L280,273 L275,273 Z",
  "Saint Lucia": "M272,267 L276,267 L276,271 L272,271 Z",
  "Saint Vincent and the Grenadines": "M271,268 L275,268 L275,272 L271,272 Z",
  "Grenada": "M270,269 L274,269 L274,273 L270,273 Z",
  "Antigua and Barbuda": "M268,260 L273,260 L273,264 L268,264 Z",
  "Dominica": "M270,264 L274,264 L274,268 L270,268 Z",
  "Saint Kitts and Nevis": "M265,258 L270,258 L270,262 L265,262 Z",
  "Brazil": "M280,280 L360,280 L360,380 L280,380 Z",
  "Argentina": "M260,380 L310,380 L310,450 L260,450 Z",
  "Chile": "M240,350 L260,350 L260,450 L240,450 Z",
  "Colombia": "M240,260 L280,260 L280,290 L240,290 Z",
  "Peru": "M240,290 L280,290 L280,340 L240,340 Z",
  "Venezuela": "M250,260 L290,260 L290,285 L250,285 Z",
  "Ecuador": "M220,280 L250,280 L250,300 L220,300 Z",
  "Bolivia": "M260,310 L300,310 L300,350 L260,350 Z",
  "Paraguay": "M280,350 L315,350 L315,385 L280,385 Z",
  "Uruguay": "M295,385 L320,385 L320,410 L295,410 Z",
  "Guyana": "M280,270 L295,270 L295,285 L280,285 Z",
  "Suriname": "M295,270 L310,270 L310,285 L295,285 Z",
  "French Guiana": "M310,270 L325,270 L325,285 L310,285 Z",
  "United Kingdom": "M400,120 L440,120 L440,150 L400,150 Z",
  "Ireland": "M380,125 L400,125 L400,150 L380,150 Z",
  "France": "M420,140 L450,140 L450,170 L420,170 Z",
  "Germany": "M450,130 L480,130 L480,160 L450,160 Z",
  "Spain": "M410,170 L440,170 L440,190 L410,190 Z",
  "Portugal": "M390,170 L410,170 L410,195 L390,195 Z",
  "Italy": "M460,160 L480,160 L480,200 L460,200 Z",
  "Netherlands": "M440,125 L460,125 L460,140 L440,140 Z",
  "Belgium": "M440,140 L455,140 L455,150 L440,150 Z",
  "Switzerland": "M455,150 L470,150 L470,160 L455,160 Z",
  "Austria": "M470,145 L490,145 L490,155 L470,155 Z",
  "Poland": "M480,120 L510,120 L510,145 L480,145 Z",
  "Czech Republic": "M470,135 L485,135 L485,145 L470,145 Z",
  "Sweden": "M460,90 L480,90 L480,125 L460,125 Z",
  "Norway": "M440,80 L465,80 L465,120 L440,120 Z",
  "Finland": "M480,85 L510,85 L510,120 L480,120 Z",
  "Denmark": "M455,115 L470,115 L470,125 L455,125 Z",
  "Greece": "M490,165 L515,165 L515,185 L490,185 Z",
  "Turkey": "M515,155 L560,155 L560,180 L515,180 Z",
  "Romania": "M490,145 L520,145 L520,165 L490,165 Z",
  "Ukraine": "M510,125 L560,125 L560,155 L510,155 Z",
  "Hungary": "M480,145 L505,145 L505,155 L480,155 Z",
  "Belarus": "M490,115 L520,115 L520,130 L490,130 Z",
  "Bulgaria": "M485,155 L510,155 L510,165 L485,165 Z",
  "Serbia": "M475,150 L490,150 L490,160 L475,160 Z",
  "Croatia": "M465,145 L480,145 L480,155 L465,155 Z",
  "Bosnia and Herzegovina": "M470,150 L485,150 L485,160 L470,160 Z",
  "Slovenia": "M465,142 L478,142 L478,150 L465,150 Z",
  "Slovakia": "M475,135 L495,135 L495,145 L475,145 Z",
  "Albania": "M475,160 L490,160 L490,170 L475,170 Z",
  "North Macedonia": "M480,160 L495,160 L495,168 L480,168 Z",
  "Montenegro": "M472,155 L482,155 L482,162 L472,162 Z",
  "Kosovo": "M478,157 L487,157 L487,164 L478,164 Z",
  "Estonia": "M485,100 L505,100 L505,110 L485,110 Z",
  "Latvia": "M480,105 L500,105 L500,115 L480,115 Z",
  "Lithuania": "M475,110 L495,110 L495,120 L475,120 Z",
  "Moldova": "M505,140 L520,140 L520,150 L505,150 Z",
  "Iceland": "M380,75 L410,75 L410,90 L380,90 Z",
  "Luxembourg": "M445,137 L452,137 L452,143 L445,143 Z",
  "Monaco": "M447,165 L450,165 L450,167 L447,167 Z",
  "Liechtenstein": "M462,152 L465,152 L465,155 L462,155 Z",
  "Andorra": "M418,175 L422,175 L422,178 L418,178 Z",
  "San Marino": "M468,162 L471,162 L471,165 L468,165 Z",
  "Vatican City": "M469,168 L471,168 L471,170 L469,170 Z",
  "Malta": "M470,195 L475,195 L475,198 L470,198 Z",
  "Cyprus": "M515,170 L525,170 L525,175 L515,175 Z",
  "Russia": "M480,60 L750,60 L750,140 L480,140 Z",
  "China": "M650,150 L750,150 L750,240 L650,240 Z",
  "India": "M600,200 L650,200 L650,270 L600,270 Z",
  "Japan": "M770,180 L800,180 L800,240 L770,240 Z",
  "South Korea": "M740,195 L760,195 L760,215 L740,215 Z",
  "North Korea": "M740,185 L760,185 L760,195 L740,195 Z",
  "Taiwan": "M720,230 L730,230 L730,245 L720,245 Z",
  "Thailand": "M670,240 L690,240 L690,280 L670,280 Z",
  "Vietnam": "M690,230 L710,230 L710,280 L690,280 Z",
  "Malaysia": "M680,280 L710,280 L710,295 L680,295 Z",
  "Singapore": "M685,295 L690,295 L690,298 L685,298 Z",
  "Indonesia": "M680,295 L750,295 L750,320 L680,320 Z",
  "Philippines": "M720,250 L745,250 L745,285 L720,285 Z",
  "Pakistan": "M575,185 L605,185 L605,215 L575,215 Z",
  "Bangladesh": "M640,215 L655,215 L655,230 L640,230 Z",
  "Myanmar": "M655,215 L675,215 L675,260 L655,260 Z",
  "Iran": "M540,165 L580,165 L580,195 L540,195 Z",
  "Iraq": "M520,165 L545,165 L545,185 L520,185 Z",
  "Saudi Arabia": "M520,185 L560,185 L560,220 L520,220 Z",
  "Israel": "M505,175 L515,175 L515,185 L505,185 Z",
  "Palestine": "M506,177 L512,177 L512,183 L506,183 Z",
  "Jordan": "M515,180 L530,180 L530,190 L515,190 Z",
  "Lebanon": "M510,175 L520,175 L520,182 L510,182 Z",
  "Syria": "M515,165 L540,165 L540,180 L515,180 Z",
  "Yemen": "M540,210 L570,210 L570,230 L540,230 Z",
  "Oman": "M565,205 L585,205 L585,225 L565,225 Z",
  "United Arab Emirates": "M555,210 L575,210 L575,220 L555,220 Z",
  "Qatar": "M555,200 L565,200 L565,208 L555,208 Z",
  "Kuwait": "M540,190 L555,190 L555,200 L540,200 Z",
  "Bahrain": "M556,202 L560,202 L560,206 L556,206 Z",
  "Afghanistan": "M580,180 L610,180 L610,200 L580,200 Z",
  "Kazakhstan": "M540,120 L620,120 L620,160 L540,160 Z",
  "Uzbekistan": "M565,155 L600,155 L600,175 L565,175 Z",
  "Turkmenistan": "M560,165 L595,165 L595,185 L560,185 Z",
  "Kyrgyzstan": "M590,155 L615,155 L615,170 L590,170 Z",
  "Tajikistan": "M580,165 L605,165 L605,180 L580,180 Z",
  "Mongolia": "M650,130 L720,130 L720,160 L650,160 Z",
  "Nepal": "M630,200 L650,200 L650,210 L630,210 Z",
  "Bhutan": "M650,205 L665,205 L665,213 L650,213 Z",
  "Sri Lanka": "M625,265 L640,265 L640,285 L625,285 Z",
  "Maldives": "M615,275 L622,275 L622,283 L615,283 Z",
  "Cambodia": "M690,255 L710,255 L710,275 L690,275 Z",
  "Lao PDR": "M680,230 L700,230 L700,260 L680,260 Z",
  "Brunei": "M705,285 L715,285 L715,292 L705,292 Z",
  "Timor-Leste": "M740,308 L755,308 L755,315 L740,315 Z",
  "Armenia": "M535,160 L550,160 L550,170 L535,170 Z",
  "Azerbaijan": "M550,160 L570,160 L570,175 L550,175 Z",
  "Georgia": "M525,155 L545,155 L545,165 L525,165 Z",
  "Egypt": "M490,195 L520,195 L520,220 L490,220 Z",
  "South Africa": "M480,360 L530,360 L530,410 L480,410 Z",
  "Nigeria": "M430,250 L460,250 L460,275 L430,275 Z",
  "Kenya": "M510,270 L535,270 L535,295 L510,295 Z",
  "Ethiopia": "M515,245 L545,245 L545,275 L515,275 Z",
  "Morocco": "M395,190 L425,190 L425,210 L395,210 Z",
  "Algeria": "M420,195 L470,195 L470,230 L420,230 Z",
  "Libya": "M465,205 L505,205 L505,235 L465,235 Z",
  "Sudan": "M495,230 L530,230 L530,260 L495,260 Z",
  "South Sudan": "M500,260 L530,260 L530,280 L500,280 Z",
  "Tanzania": "M510,290 L540,290 L540,315 L510,315 Z",
  "Ghana": "M410,260 L430,260 L430,280 L410,280 Z",
  "Angola": "M460,310 L495,310 L495,350 L460,350 Z",
  "Mozambique": "M515,315 L545,315 L545,360 L515,360 Z",
  "Madagascar": "M545,320 L565,320 L565,360 L545,360 Z",
  "Cameroon": "M455,260 L480,260 L480,285 L455,285 Z",
  "Côte d'Ivoire": "M400,265 L420,265 L420,280 L400,280 Z",
  "Niger": "M435,225 L475,225 L475,250 L435,250 Z",
  "Burkina Faso": "M410,245 L435,245 L435,260 L410,260 Z",
  "Mali": "M405,220 L445,220 L445,250 L405,250 Z",
  "Malawi": "M515,305 L530,305 L530,325 L515,325 Z",
  "Zambia": "M495,315 L530,315 L530,345 L495,345 Z",
  "Zimbabwe": "M505,340 L535,340 L535,365 L505,365 Z",
  "Botswana": "M490,350 L520,350 L520,375 L490,375 Z",
  "Namibia": "M475,350 L510,350 L510,390 L475,390 Z",
  "Senegal": "M385,235 L405,235 L405,248 L385,248 Z",
  "Guinea": "M390,255 L410,255 L410,270 L390,270 Z",
  "Sierra Leone": "M385,260 L400,260 L400,272 L385,272 Z",
  "Liberia": "M390,270 L405,270 L405,282 L390,282 Z",
  "Tunisia": "M450,185 L470,185 L470,205 L450,205 Z",
  "Uganda": "M505,275 L525,275 L525,290 L505,290 Z",
  "Rwanda": "M505,285 L520,285 L520,295 L505,295 Z",
  "Burundi": "M508,292 L520,292 L520,302 L508,302 Z",
  "Somalia": "M530,255 L560,255 L560,285 L530,285 Z",
  "Djibouti": "M530,250 L542,250 L542,258 L530,258 Z",
  "Eritrea": "M520,240 L540,240 L540,253 L520,253 Z",
  "Chad": "M460,225 L495,225 L495,260 L460,260 Z",
  "Central African Republic": "M470,260 L505,260 L505,280 L470,280 Z",
  "Congo": "M465,280 L495,280 L495,310 L465,310 Z",
  "DR Congo": "M475,280 L520,280 L520,325 L475,325 Z",
  "Gabon": "M455,285 L475,285 L475,305 L455,305 Z",
  "Equatorial Guinea": "M450,280 L462,280 L462,288 L450,288 Z",
  "Benin": "M425,258 L438,258 L438,275 L425,275 Z",
  "Togo": "M420,260 L430,260 L430,275 L420,275 Z",
  "Mauritania": "M385,210 L420,210 L420,235 L385,235 Z",
  "Western Sahara": "M380,200 L410,200 L410,218 L380,218 Z",
  "Gambia": "M385,240 L400,240 L400,245 L385,245 Z",
  "Guinea-Bissau": "M385,248 L398,248 L398,258 L385,258 Z",
  "Lesotho": "M505,395 L518,395 L518,405 L505,405 Z",
  "Eswatini": "M520,375 L532,375 L532,385 L520,385 Z",
  "Mauritius": "M570,360 L578,360 L578,368 L570,368 Z",
  "Comoros": "M540,300 L548,300 L548,308 L540,308 Z",
  "Seychelles": "M560,270 L568,270 L568,278 L560,278 Z",
  "Sao Tome and Principe": "M448,288 L454,288 L454,294 L448,294 Z",
  "Cape Verde": "M365,235 L373,235 L373,243 L365,243 Z",
  "Australia": "M700,330 L800,330 L800,420 L700,420 Z",
  "New Zealand": "M820,380 L850,380 L850,430 L820,430 Z",
  "Papua New Guinea": "M760,295 L800,295 L800,315 L760,315 Z",
  "Fiji": "M855,330 L870,330 L870,342 L855,342 Z",
  "Solomon Islands": "M810,305 L830,305 L830,318 L810,318 Z",
  "Vanuatu": "M825,320 L838,320 L838,335 L825,335 Z",
  "New Caledonia": "M830,340 L845,340 L845,352 L830,352 Z",
  "Samoa": "M875,325 L888,325 L888,335 L875,335 Z",
  "Tonga": "M870,340 L880,340 L880,350 L870,350 Z",
  "Kiribati": "M880,310 L895,310 L895,320 L880,320 Z",
  "Micronesia": "M810,290 L830,290 L830,300 L810,300 Z",
  "Marshall Islands": "M835,295 L850,295 L850,305 L835,305 Z",
  "Palau": "M755,295 L765,295 L765,303 L755,303 Z",
  "Nauru": "M825,305 L832,305 L832,312 L825,312 Z",
  "Tuvalu": "M845,318 L852,318 L852,325 L845,325 Z",
};

export const MILESTONES = [100, 500, 1000, 5000, 10000];


================================================================
File Path: src/contexts/LanguageContext.tsx
================================================================

import React, { createContext, useContext, useState, ReactNode } from 'react'

type Language = 'zh' | 'en'

interface LanguageContextType {
  language: Language
  setLanguage: (lang: Language) => void
  t: (key: string) => string
  getAudioUrl: () => string
}

// 音频文件 URL 配置
const audioUrls = {
  zh: "https://raw.githubusercontent.com/jojoyo37198/audio/refs/heads/main/Public_TW.mp3",
  en: "https://raw.githubusercontent.com/jojoyo37198/audio/refs/heads/main/Public_EN.mp3"
}

const translations = {
  zh: {
    // 導航欄 - 保持原始內容
    'nav.home': '首頁',
    'nav.about': '關於我們',
    'nav.services': '服務項目',
    'nav.portfolio': '作品集',
    'nav.testimonials': '客戶見證',
    'nav.contact': '免費諮詢',
    'nav.watchVideo': '觀看影片',
    'nav.videos': '影片展示',
    
    // 英雄區塊 - 園藝主題
    'hero.title': '專業園藝景觀設計',
    'hero.subtitle': '打造您的綠色夢想空間',
    'hero.description': '一站式園藝服務:設計、施工、植栽維護。專注創造美麗舒適的戶外環境。',
    'hero.getStarted': '立即開始',
    'hero.learnMore': '了解更多',
    
    // 服務項目 - 園藝相關
    'services.title': '我們的服務(桃園新屋/新竹地區)',
    'services.subtitle': '專業全方位園藝景觀解決方案',
    'services.gardenDesign': '花園設計',
    'services.gardenDesignDesc': '量身打造專屬花園設計,融合美學與實用性',
    'services.landscaping': '景觀工程',
    'services.landscapingDesc': '專業景觀施工團隊,確保工程品質與安全',
    'services.maintenance': '植栽維護',
    'services.maintenanceDesc': '定期養護服務,讓您的花園四季常綠',
    'services.irrigation': '灌溉系統',
    'services.irrigationDesc': '智能灌溉系統設計,節水環保又便利',
    
    // 關於我們 - 園藝專業
    'about.title': '關於悅境園藝',
    'about.subtitle': '專業團隊,用心服務',
    'about.description': '我們是一支充滿熱忱的專業園藝團隊,致力於為客戶創造美麗的戶外空間。憑藉多年的園藝經驗與專業技術,我們已成功完成眾多園藝景觀項目,為客戶打造夢想中的綠色家園。',
    'about.experience': '豐富經驗',
    'about.experienceDesc': '超過20年的園藝設計經驗',
    'about.projects': '成功案例',
    'about.projectsDesc': '完成500+個園藝項目',
    'about.support': '專業維護',
    'about.supportDesc': '提供長期植栽維護服務',
    
    // 作品集 - 按照圖片更新為4個項目
    'portfolio.title': '作品集',
    'portfolio.subtitle': '我們的園藝傑作',
    'portfolio.residential': '住宅庭園',
    'portfolio.residentialDesc': '私人住宅景觀設計,打造溫馨庭院綠洲',
    'portfolio.commercial': '商業空間',
    'portfolio.commercialDesc': '辦公大樓景觀工程,提升作業環境品質',
    'portfolio.public': '公共園區',
    'portfolio.publicDesc': '社區公園景觀改造,創造休憩新天地',
    'portfolio.rooftop': '屋頂花園',
    'portfolio.rooftopDesc': '都市屋頂綠化,充分利用垂直造景',
    'portfolio.viewProject': '查看項目',
    'portfolio.category.residential': '住宅',
    'portfolio.category.commercial': '商業',
    'portfolio.category.public': '公共',
    'portfolio.category.specialty': '專業',
    
    // 客戶見證 - 更新為6位客戶
    'testimonials.title': '客戶見證',
    'testimonials.subtitle': '客戶的滿意是我們的榮耀',
    'testimonials.client1': '林先生',
    'testimonials.client1Title': '超大型社區(>500戶)',
    'testimonials.client1Text': '悅境團隊作到了他們承諾的優化改造,我們對住戶有交代了,大家都很滿意。',
    'testimonials.client2': '王先生',
    'testimonials.client2Title': '地方首長公館(別墅)',
    'testimonials.client2Text': '為公館裡帶來豐富多樣的舒適感,維護工作也很棒,深得我們官長滿意.',
    'testimonials.client3': '李先生',
    'testimonials.client3Title': '科技廠商',
    'testimonials.client3Text': '廠區整體維護一致化,園藝技師專業優質。',
    'testimonials.client4': '黃小姐',
    'testimonials.client4Title': '商務大樓',
    'testimonials.client4Text': '長期配合的廠商,園藝師父們都很熱情好配合。',
    'testimonials.client5': '陳小姐',
    'testimonials.client5Title': '四星級飯店',
    'testimonials.client5Text': '利用巧妙的設計和創新點子,展現園藝工藝的細節,增添人氣感與活力。',
    'testimonials.client6': '張先生',
    'testimonials.client6Title': '頂級私人會所',
    'testimonials.client6Text': '在過去的合作經驗很不錯,但高峰期要提早約時間。',
    
    // 聯絡我們 - 園藝需求表單
    'contact.title': '讓您的綠色夢想啟航!',
    'contact.subtitle': '讓我們開始合作',
    'contact.description': '我們會準備您專屬的園藝景觀優惠方案。請填寫以下資訊,讓我們更了解您的需求。',
    'contact.name': '姓名',
    'contact.namePlaceholder': '請輸入您的姓名',
    'contact.email': '電子郵件',
    'contact.emailPlaceholder': '請輸入您的電子郵件',
    'contact.phone': '聯絡電話',
    'contact.phonePlaceholder': '請輸入您的聯絡電話',
    'contact.location': '專案地點',
    'contact.locationPlaceholder': '請輸入專案所在地區',
    'contact.serviceType': '服務類型',
    'contact.selectService': '請選擇服務類型',
    'contact.gardenDesign': '花園設計',
    'contact.landscaping': '景觀工程',
    'contact.maintenance': '園藝維護',
    'contact.planting': '植栽規劃',
    'contact.irrigation': '灌溉系統',
    'contact.consultation': '諮詢服務',
    'contact.projectSize': '專案規模',
    'contact.selectSize': '請選擇專案規模',
    'contact.smallProject': '小型專案(20坪以下)',
    'contact.mediumProject': '中型專案(20-100坪)',
    'contact.largeProject': '大型專案(100坪以上)',
    'contact.budget': '預算範圍',
    'contact.selectBudget': '請選擇預算範圍',
    'contact.budgetUnder50k': '2萬以下',
    'contact.budget50k100k': '2-10萬',
    'contact.budget100k200k': '10-50萬',
    'contact.budgetOver200k': '50萬以上',
    'contact.timeline': '預期時程',
    'contact.selectTimeline': '請選擇預期時程',
    'contact.timelineASAP': '盡快開始',
    'contact.timeline1to3': '1週內',
    'contact.timeline3to6': '2週內',
    'contact.timeline6plus': '1個月以上',
    'contact.message': '詳細需求描述',
    'contact.messagePlaceholder': '請描述您的園藝需求、特殊要求或其他相關資訊...',
    'contact.send': '提交需求',
    'contact.sending': '提交中...',
    'contact.successMessage': '感謝您的提交!我們會在24小時內與您聯繫,為您準備專屬的園藝方案。',
    'contact.errorMessage': '提交失敗,請稍後再試或直接聯繫我們。',
    'contact.address': '地址',
    'contact.freeConsult': '免費諮詢',
    'contact.consultDesc': '立即預約免費諮詢,了解我們如何為您打造夢想花園',
    'contact.bookConsult': '預約諮詢',
    
    // 頁尾
    'footer.description': '悅境園藝專業提供園藝設計、景觀工程與植栽維護服務,為您打造完美的綠色空間。',
    'footer.quickLinks': '快速連結',
    'footer.services': '服務項目',
    'footer.contact': '聯絡資訊',
    'footer.rights': '版權所有',
    
    // YouTube影片展示區
    'youtube.title': '觀看次數超過 60K⁺ 的精選影片',
    'youtube.subtitle': '探索我們的專業園藝作品與服務實例',
	
    // 音頻播放器
    'audio.promptTitle': '想聽聽 EGD 的故事嗎?',
    'audio.promptSubtitle': '了解我們的理念',
    'audio.startListening': '開始聆聽',
    'audio.decline': '稍後再說',
    'audio.title': 'EGD 介紹 (30秒)',
    'audio.minimize': '最小化',
    'audio.expand': '展開',
    'audio.play': '播放',
    'audio.pause': '暫停',
    'audio.close': '關閉',
  },
  en: {
    // Navigation
    'nav.home': 'Home',
    'nav.about': 'About Us',
    'nav.services': 'Services',
    'nav.portfolio': 'Portfolio',
    'nav.testimonials': 'Testimonials',
    'nav.contact': 'Free Consultation',
    'nav.watchVideo': 'Watch Video',
    'nav.videos': 'Videos',
    
    // Hero Section - Garden Theme
    'hero.title': 'Landscape Design',
    'hero.subtitle': 'Create Your Dream Green Space',
    'hero.description': 'Professional landscape design and engineering.',
    'hero.getStarted': 'Get Started',
    'hero.learnMore': 'Learn More',
    
    // Services - Garden Related
    'services.title': 'Our Services (Taoyuan / Hsinchu Area)',
    'services.subtitle': 'Professional Comprehensive Garden & Landscape Solutions',
    'services.gardenDesign': 'Garden Design',
    'services.gardenDesignDesc': 'Custom garden design that combines aesthetics with functionality',
    'services.landscaping': 'Landscape Construction',
    'services.landscapingDesc': 'Professional landscape construction team ensuring quality and safety',
    'services.maintenance': 'Plant Maintenance',
    'services.maintenanceDesc': 'Regular maintenance services to keep your garden green all year round',
    'services.irrigation': 'Irrigation System',
    'services.irrigationDesc': 'Smart irrigation system design that saves water and is eco-friendly',
    
    // About - Garden Professional
    'about.title': 'About EG Design',
    'about.subtitle': 'Professional Team, Dedicated Service',
    'about.description': 'We are a passionate professional garden team dedicated to creating beautiful outdoor spaces for our clients. With years of gardening experience and professional expertise, we have successfully completed numerous garden landscape projects, creating dream green homes for our clients.',
    'about.experience': 'Rich Experience',
    'about.experienceDesc': 'Over 20 years of garden design experience',
    'about.projects': 'Success Stories',
    'about.projectsDesc': 'Completed 500+ garden projects',
    'about.support': 'Professional Maintenance',
    'about.supportDesc': 'Providing long-term plant maintenance services',
    
    // Portfolio - Updated to match the 4 projects in image
    'portfolio.title': 'Portfolio',
    'portfolio.subtitle': 'Our Garden Masterpieces',
    'portfolio.residential': 'Residential Garden',
    'portfolio.residentialDesc': 'Private residential landscape design, creating cozy courtyard oasis',
    'portfolio.commercial': 'Commercial Space',
    'portfolio.commercialDesc': 'Office building landscape projects, enhancing work environment quality',
    'portfolio.public': 'Public Garden',
    'portfolio.publicDesc': 'Community park landscape renovation, creating new recreational spaces',
    'portfolio.rooftop': 'Rooftop Garden',
    'portfolio.rooftopDesc': 'Urban rooftop greening, maximizing vertical landscaping',
    'portfolio.viewProject': 'View Project',
    'portfolio.category.residential': 'Residential',
    'portfolio.category.commercial': 'Commercial',
    'portfolio.category.public': 'Public',
    'portfolio.category.specialty': 'Specialty',
    
    // Testimonials - Updated to 6 clients
    'testimonials.title': 'Testimonials',
    'testimonials.subtitle': 'Client satisfaction is our pride',
    'testimonials.client1': 'Mr. Lin',
    'testimonials.client1Title': 'Large Community (>500 Units)',
    'testimonials.client1Text': 'Project Harmony delivered the promised upgrades, satisfying all residents.',
    'testimonials.client2': 'Mr. Wang',
    'testimonials.client2Title': 'Governor\'s Residence (Villa)',
    'testimonials.client2Text': 'The residence now offers diverse and luxurious comfort, and the excellent maintenance work has completely satisfied our supervising officer.',
    'testimonials.client3': 'Mr. Li',
    'testimonials.client3Title': 'Technology Company',
    'testimonials.client3Text': 'Uniform facility maintenance is achieved across the entire site, supported by professional and high-quality horticultural technicians.',
    'testimonials.client4': 'Ms. Huang',
    'testimonials.client4Title': 'Commercial Building',
    'testimonials.client4Text': 'Our long-term vendor, whose horticultural staff are both enthusiastic and highly cooperative.',
    'testimonials.client5': 'Ms. Chen',
    'testimonials.client5Title': 'Four-Star Hotel',
    'testimonials.client5Text': 'Utilizing ingenious designs and innovative ideas to showcase detailed horticultural craftsmanship, boosting both vitality and a sense of inviting warmth.',
    'testimonials.client6': 'Mr. Zhang',
    'testimonials.client6Title': 'Premium Private Club',
    'testimonials.client6Text': 'Our past collaborations have been excellent, but advance booking is essential during peak seasons.',
    
    // Contact - Garden Requirements Form
    'contact.title': 'Let Your Green Dreams Take Flight!',
    'contact.subtitle': 'Let\'s Start Working Together',
    'contact.description': 'We will prepare an exclusive garden landscape package just for you. Please fill out the following information so we can better understand your needs.',
    'contact.name': 'Name',
    'contact.namePlaceholder': 'Please enter your name',
    'contact.email': 'Email',
    'contact.emailPlaceholder': 'Please enter your email address',
    'contact.phone': 'Phone',
    'contact.phonePlaceholder': 'Please enter your phone number',
    'contact.location': 'Project Location',
    'contact.locationPlaceholder': 'Please enter the project location',
    'contact.serviceType': 'Service Type',
    'contact.selectService': 'Please select service type',
    'contact.gardenDesign': 'Garden Design',
    'contact.landscaping': 'Landscaping',
    'contact.maintenance': 'Garden Maintenance',
    'contact.planting': 'Planting Planning',
    'contact.irrigation': 'Irrigation System',
    'contact.consultation': 'Consultation Service',
    'contact.projectSize': 'Project Size',
    'contact.selectSize': 'Please select project size',
    'contact.smallProject': 'Small Project (Under 1,800 sq ft)',
    'contact.mediumProject': 'Medium Project (1,800-7,200 sq ft)',
    'contact.largeProject': 'Large Project (Over 7,200 sq ft)',
    'contact.budget': 'Budget Range',
    'contact.selectBudget': 'Please select budget range',
    'contact.budgetUnder50k': 'Under $1,500',
    'contact.budget50k100k': '$1,500-$3,000',
    'contact.budget100k200k': '$3,000-$6,000',
    'contact.budgetOver200k': 'Over $6,000',
    'contact.timeline': 'Timeline',
    'contact.selectTimeline': 'Please select expected timeline',
    'contact.timelineASAP': 'Start ASAP',
    'contact.timeline1to3': 'Within 1-3 months',
    'contact.timeline3to6': 'Within 3-6 months',
    'contact.timeline6plus': 'Over 6 months',
    'contact.message': 'Detailed Requirements',
    'contact.messagePlaceholder': 'Please describe your garden requirements, special requests, or other relevant information...',
    'contact.send': 'Submit Requirements',
    'contact.sending': 'Submitting...',
    'contact.successMessage': 'Thank you for your submission! We will contact you within 24 hours to prepare an exclusive garden plan for you.',
    'contact.errorMessage': 'Submission failed. Please try again later or contact us directly.',
    'contact.address': 'Address',
    'contact.freeConsult': 'Free Consultation',
    'contact.consultDesc': 'Book a free consultation now to learn how we can create your dream garden',
    'contact.bookConsult': 'Book Consultation',
    
    // Footer
    'footer.description': 'EG Design Garden professionally provides garden design, landscape construction and plant maintenance services to create the perfect green space for you.',
    'footer.quickLinks': 'Quick Links',
    'footer.services': 'Services',
    'footer.contact': 'Contact Info',
    'footer.rights': 'All rights reserved',
    
    // YouTube Gallery
    'youtube.title': 'Our Most Popular Videos (60K⁺ Views)',
    'youtube.subtitle': 'Explore our professional garden works and service examples',
	
    // AudioPlayer
    'audio.promptTitle': 'Would you like to hear EGD story?',
    'audio.promptSubtitle': 'Understand our philosophy in 30 Seconds',
    'audio.startListening': 'Start Listening',
    'audio.decline': 'Later',
    'audio.title': 'EGD Introduction (30 Seconds)',
    'audio.minimize': 'Minimize',
    'audio.expand': 'Expand',
    'audio.play': 'Play',
    'audio.pause': 'Pause',
    'audio.close': 'Close',
  }
}

const LanguageContext = createContext<LanguageContextType | undefined>(undefined)

export function useLanguage() {
  const context = useContext(LanguageContext)
  if (context === undefined) {
    throw new Error('useLanguage must be used within a LanguageProvider')
  }
  return context
}

export function LanguageProvider({ children }: { children: ReactNode }) {
  const [language, setLanguage] = useState<Language>('en')

  const t = (key: string): string => {
    return translations[language][key] || key
  }

  const getAudioUrl = (): string => {
    return audioUrls[language]
  }

  return (
    <LanguageContext.Provider value={{ language, setLanguage, t, getAudioUrl }}>
      {children}
    </LanguageContext.Provider>
  )
}


================================================================
File Path: src/hooks/useAnalyticsData.ts
================================================================

import { useState, useEffect, useCallback } from "react";
import { createClient } from "@supabase/supabase-js";
import {
  VisitorLog,
  ChartData,
  CountryData,
  ComparisonStats,
  TimeRange,
  OperationLog,
  OperationStats,
  MILESTONES
} from "../constants/analyticsConstants";

import { supabase } from "../lib/supabase";

export const useAnalyticsData = () => {
  const [visitors, setVisitors] = useState<VisitorLog[]>([]);
  const [chartData, setChartData] = useState<ChartData[]>([]);
  const [countryData, setCountryData] = useState<CountryData[]>([]);
  const [timeRange, setTimeRange] = useState<TimeRange>("week");
  const [loading, setLoading] = useState(true);
  const [totalVisits, setTotalVisits] = useState(0);
  const [uniqueVisitors, setUniqueVisitors] = useState(0);
  const [comparisonStats, setComparisonStats] = useState<ComparisonStats | null>(null);
  const [reachedMilestone, setReachedMilestone] = useState<number | null>(null);

  const [cookieConsent, setCookieConsent] = useState<boolean | null>(null);
  const [showCookieConsent, setShowCookieConsent] = useState(false);

  const [operationLogs, setOperationLogs] = useState<OperationLog[]>([]);
  const [operationStats, setOperationStats] = useState<OperationStats | null>(null);
  const [logFilter, setLogFilter] = useState<string | null>(null);
  const [logsLoading, setLogsLoading] = useState(false);

  const [hoveredCountry, setHoveredCountry] = useState<string | null>(null);

  const checkMilestone = useCallback((visitorCount: number) => {
    const achievedMilestones = MILESTONES.filter(m => visitorCount >= m);
    const highestMilestone = achievedMilestones[achievedMilestones.length - 1];
    
    if (highestMilestone) {
      setReachedMilestone(highestMilestone);
    }
  }, []);

  // ✅ 新版：使用 Supabase Function 自動記錄 IP
  const trackVisitor = useCallback(async () => {
    if (cookieConsent === false) return;
    
    try {
      const { data, error } = await supabase.rpc('track_visitor', {
        p_user_agent: navigator.userAgent
      });

      if (error) {
        console.error("❌ 追蹤失敗:", error);
      } else {
        console.log("✅ 訪客已記錄，IP:", data?.ip);
      }
    } catch (error) {
      console.error("❌ 追蹤錯誤:", error);
    }
  }, [cookieConsent]);

  const calculateCountryData = useCallback((data: VisitorLog[]) => {
    const countryMap = new Map<string, { count: number; visitors: number }>();

    data.forEach((visitor) => {
      const country = visitor.country || "Unknown";
      const existing = countryMap.get(country) || { count: 0, visitors: 0 };
      countryMap.set(country, {
        count: existing.count + visitor.visit_count,
        visitors: existing.visitors + 1,
      });
    });

    const countryArray = Array.from(countryMap.entries())
      .map(([country, data]) => ({
        country,
        count: data.count,
        visitors: data.visitors,
      }))
      .sort((a, b) => b.count - a.count);

    setCountryData(countryArray);
  }, []);

  const calculateComparison = useCallback((data: VisitorLog[], range: TimeRange) => {
    const now = new Date();
    let currentStart: Date, currentEnd: Date, previousStart: Date, previousEnd: Date;

    if (range === "week") {
      currentEnd = now;
      currentStart = new Date(now.getTime() - 7 * 24 * 60 * 60 * 1000);
      previousEnd = new Date(currentStart.getTime() - 1);
      previousStart = new Date(previousEnd.getTime() - 7 * 24 * 60 * 60 * 1000);
    } else if (range === "twoWeeks") {
      currentEnd = now;
      currentStart = new Date(now.getTime() - 14 * 24 * 60 * 60 * 1000);
      previousEnd = new Date(currentStart.getTime() - 1);
      previousStart = new Date(previousEnd.getTime() - 14 * 24 * 60 * 60 * 1000);
    } else if (range === "month") {
      currentEnd = now;
      currentStart = new Date(now.getTime() - 30 * 24 * 60 * 60 * 1000);
      previousEnd = new Date(currentStart.getTime() - 1);
      previousStart = new Date(previousEnd.getTime() - 30 * 24 * 60 * 60 * 1000);
    } else {
      currentEnd = now;
      currentStart = new Date(now.getTime() - 365 * 24 * 60 * 60 * 1000);
      previousEnd = new Date(currentStart.getTime() - 1);
      previousStart = new Date(previousEnd.getTime() - 365 * 24 * 60 * 60 * 1000);
    }

    const currentTotal = data.reduce((sum, visitor) => {
      const visitDate = new Date(visitor.last_visit);
      if (visitDate >= currentStart && visitDate <= currentEnd) {
        return sum + visitor.visit_count;
      }
      return sum;
    }, 0);

    const previousTotal = data.reduce((sum, visitor) => {
      const visitDate = new Date(visitor.last_visit);
      if (visitDate >= previousStart && visitDate <= previousEnd) {
        return sum + visitor.visit_count;
      }
      return sum;
    }, 0);

    const changePercent = previousTotal === 0 
      ? (currentTotal > 0 ? 100 : 0)
      : ((currentTotal - previousTotal) / previousTotal) * 100;

    const changeType: "increase" | "decrease" | "neutral" = 
      changePercent > 0 ? "increase" : changePercent < 0 ? "decrease" : "neutral";

    setComparisonStats({
      currentTotal,
      previousTotal,
      changePercent,
      changeType,
    });
  }, []);

  const generateChartDataWithComparison = useCallback((data: VisitorLog[], range: TimeRange) => {
    const now = new Date();
    const chartMap = new Map<string, number>();
    const compareMap = new Map<string, number>();

    let daysBack = 7;
    let dateFormat: (date: Date) => string = (d) =>
      `${d.getMonth() + 1}/${d.getDate()}`;

    if (range === "twoWeeks") {
      daysBack = 14;
    } else if (range === "month") {
      daysBack = 30;
    } else if (range === "year") {
      daysBack = 365;
      dateFormat = (d) => `${d.getFullYear()}/${d.getMonth() + 1}`;
    }

    for (let i = daysBack - 1; i >= 0; i--) {
      const date = new Date(now);
      date.setDate(date.getDate() - i);
      const key = dateFormat(date);
      chartMap.set(key, 0);
    }

    for (let i = daysBack - 1; i >= 0; i--) {
      const date = new Date(now);
      date.setDate(date.getDate() - daysBack - i);
      const key = dateFormat(date);
      compareMap.set(key, 0);
    }

    data.forEach((visitor) => {
      const visitDate = new Date(visitor.last_visit);
      const daysDiff = Math.floor(
        (now.getTime() - visitDate.getTime()) / (1000 * 60 * 60 * 24)
      );

      if (daysDiff < daysBack) {
        const key = dateFormat(visitDate);
        chartMap.set(key, (chartMap.get(key) || 0) + visitor.visit_count);
      } else if (daysDiff >= daysBack && daysDiff < daysBack * 2) {
        const key = dateFormat(visitDate);
        compareMap.set(key, (compareMap.get(key) || 0) + visitor.visit_count);
      }
    });

    const chartArray = Array.from(chartMap.entries()).map(([date, count], index) => {
      const compareValues = Array.from(compareMap.values());
      return {
        date,
        count,
        compareCount: compareValues[index] || 0,
      };
    });

    setChartData(chartArray);
  }, []);

  const fetchVisitorData = useCallback(async () => {
    setLoading(true);
    try {
      const { data, error } = await supabase
        .from("visitor_logs")
        .select("*")
        .order("last_visit", { ascending: false });

      if (error) {
        console.error("Error fetching visitors:", error);
        return;
      }

      setVisitors(data || []);
      
      const total = (data || []).reduce((sum, v) => sum + v.visit_count, 0);
      setTotalVisits(total);
      const uniqueCount = (data || []).length;
      setUniqueVisitors(uniqueCount);
      
      checkMilestone(uniqueCount);
      generateChartDataWithComparison(data || [], timeRange);
      calculateComparison(data || [], timeRange);
      calculateCountryData(data || []);
    } catch (error) {
      console.error("Error:", error);
    } finally {
      setLoading(false);
    }
  }, [timeRange, calculateCountryData, checkMilestone, calculateComparison, generateChartDataWithComparison]);

  const fetchOperationLogs = useCallback(async () => {
    setLogsLoading(true);
    try {
      const { data, error } = await supabase
        .rpc("get_operation_logs", {
          p_limit: 100,
          p_offset: 0,
          p_operation_type: logFilter
        });

      if (error) {
        console.error("Error fetching operation logs:", error);
        return;
      }

      setOperationLogs(data || []);
    } catch (error) {
      console.error("Error:", error);
    } finally {
      setLogsLoading(false);
    }
  }, [logFilter]);

  const fetchOperationStats = useCallback(async () => {
    try {
      const { data, error } = await supabase.rpc("get_operation_stats");

      if (error) {
        console.error("Error fetching operation stats:", error);
        return;
      }

      setOperationStats(data || null);
    } catch (error) {
      console.error("Error:", error);
    }
  }, []);

  useEffect(() => {
    const consent = localStorage.getItem("visitor_tracking_consent");
    if (consent === null) {
      setShowCookieConsent(true);
      setCookieConsent(null);
    } else {
      setCookieConsent(consent === "true");
    }
  }, []);

  useEffect(() => {
    if (cookieConsent === true) {
      trackVisitor();
    }
  }, [cookieConsent, trackVisitor]);

  useEffect(() => {
    if (visitors.length > 0) {
      generateChartDataWithComparison(visitors, timeRange);
      calculateComparison(visitors, timeRange);
    }
  }, [timeRange, visitors, calculateComparison, generateChartDataWithComparison]);

  const handleCookieConsent = (accepted: boolean) => {
    localStorage.setItem("visitor_tracking_consent", accepted.toString());
    setCookieConsent(accepted);
    setShowCookieConsent(false);
    
    if (accepted) {
      trackVisitor();
    }
  };

  return {
    visitors,
    chartData,
    countryData,
    timeRange,
    setTimeRange,
    loading,
    totalVisits,
    uniqueVisitors,
    comparisonStats,
    reachedMilestone,
    cookieConsent,
    showCookieConsent,
    handleCookieConsent,
    fetchVisitorData,
    operationLogs,
    operationStats,
    logFilter,
    setLogFilter,
    logsLoading,
    fetchOperationLogs,
    fetchOperationStats,
    hoveredCountry,
    setHoveredCountry,
  };
};


================================================================
File Path: src/lib/supabase.ts
================================================================

import { createClient } from "@supabase/supabase-js";

const supabaseUrl = import.meta.env.VITE_SUPABASE_URL;
const supabaseAnonKey = import.meta.env.VITE_SUPABASE_ANON_KEY;

if (!supabaseUrl || !supabaseAnonKey) {
  throw new Error("缺少 Supabase 環境變數");
}

export const supabase = createClient(supabaseUrl, supabaseAnonKey);


================================================================
File Path: src/server/index.js
================================================================

const express = require('express');
const cors = require('cors');
const multer = require('multer');
const fs = require('fs').promises;
const path = require('path');
const Papa = require('papaparse');
const ExcelJS = require('exceljs');

const app = express();
const PORT = 3002;

// 修正 CORS 設定
app.use(cors({
  origin: '*',
  credentials: true
}));

app.use(express.json());

const upload = multer({ 
  dest: 'uploads/',
  limits: { fileSize: 10 * 1024 * 1024 }
});

const KNOWLEDGE_BASE_PATH = path.join(__dirname, '../../src/services/knowledgeBase.ts');

async function parseCSV(filePath) {
  const fileContent = await fs.readFile(filePath, 'utf-8');
  return new Promise((resolve, reject) => {
    Papa.parse(fileContent, {
      header: true,
      skipEmptyLines: true,
      complete: (results) => resolve(results.data),
      error: (error) => reject(error)
    });
  });
}

async function parseExcel(filePath) {
  const workbook = new ExcelJS.Workbook();
  await workbook.xlsx.readFile(filePath);
  
  const worksheet = workbook.worksheets[0];
  if (!worksheet) throw new Error('Excel 文件中沒有工作表');

  const jsonData = [];
  worksheet.eachRow((row, rowNumber) => {
    const rowValues = row.values.slice(1);
    jsonData.push(rowValues);
  });

  if (jsonData.length < 2) throw new Error('Excel 文件至少需要標題行和一行數據');

  const headers = jsonData[0].map(h => String(h || ''));
  const rows = jsonData.slice(1);

  return rows
    .filter(row => row.some(cell => cell !== null && cell !== undefined && cell !== ''))
    .map(row => {
      const obj = {};
      headers.forEach((header, index) => {
        const value = row[index];
        obj[header] = value !== null && value !== undefined ? String(value) : '';
      });
      return obj;
    });
}

app.post('/api/upload-knowledge', upload.single('file'), async (req, res) => {
  let uploadedFilePath = null;
  
  try {
    if (!req.file) {
      return res.status(400).json({ success: false, message: '沒有上傳檔案' });
    }

    uploadedFilePath = req.file.path;
    const mode = req.body.mode || 'replace';
    const fileExtension = req.file.originalname.toLowerCase().split('.').pop();

    let rawData;
    if (fileExtension === 'csv') {
      rawData = await parseCSV(uploadedFilePath);
    } else if (['xlsx', 'xls'].includes(fileExtension)) {
      rawData = await parseExcel(uploadedFilePath);
    } else {
      throw new Error('不支援的檔案格式');
    }

    const zhData = [];
    const enData = [];
    const categories = new Set();

    rawData.forEach(row => {
      const item = {
        keywords: row.keywords ? row.keywords.split(',').map(k => k.trim()) : [],
        question: row.question || '',
        answer: row.answer || '',
        category: row.category || '其他',
        priority: parseInt(row.priority) || 1,
        enabled: row.enabled === 'true' || row.enabled === true
      };

      categories.add(item.category);

      if (row.language === 'zh') {
        zhData.push(item);
      } else if (row.language === 'en') {
        enData.push(item);
      }
    });

    const dir = path.dirname(KNOWLEDGE_BASE_PATH);
    await fs.mkdir(dir, { recursive: true });

    let existingZh = [];
    let existingEn = [];
    
    try {
      const fileContent = await fs.readFile(KNOWLEDGE_BASE_PATH, 'utf-8');
      if (mode === 'merge') {
        existingZh = extractExistingData(fileContent, 'zh');
        existingEn = extractExistingData(fileContent, 'en');
      }
    } catch (e) {
      console.log('無法讀取現有知識庫，將建立新檔案');
    }

    const finalZh = mode === 'merge' ? mergeData(existingZh, zhData) : zhData;
    const finalEn = mode === 'merge' ? mergeData(existingEn, enData) : enData;

    const newContent = generateKnowledgeBaseContent(finalZh, finalEn);
    await fs.writeFile(KNOWLEDGE_BASE_PATH, newContent, 'utf-8');

    await fs.unlink(uploadedFilePath);

    res.json({
      success: true,
      message: `成功導入 ${rawData.length} 筆資料`,
      stats: {
        total: rawData.length,
        zh: zhData.length,
        en: enData.length,
        categories: Array.from(categories)
      }
    });

    console.log(`✅ 成功上傳知識庫: ${rawData.length} 筆資料 (中文: ${zhData.length}, 英文: ${enData.length})`);

  } catch (error) {
    console.error('上傳錯誤:', error);
    
    if (uploadedFilePath) {
      try {
        await fs.unlink(uploadedFilePath);
      } catch (e) {
        console.error('刪除暫存檔失敗:', e);
      }
    }

    res.status(500).json({
      success: false,
      message: error.message || '上傳失敗'
    });
  }
});

app.get('/api/download-template', async (req, res) => {
  try {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('知識庫範本');

    worksheet.columns = [
      { header: 'language', key: 'language', width: 10 },
      { header: 'keywords', key: 'keywords', width: 30 },
      { header: 'question', key: 'question', width: 40 },
      { header: 'answer', key: 'answer', width: 50 },
      { header: 'category', key: 'category', width: 15 },
      { header: 'priority', key: 'priority', width: 10 },
      { header: 'enabled', key: 'enabled', width: 10 }
    ];

    worksheet.addRow({
      language: 'zh',
      keywords: '關鍵字1,關鍵字2',
      question: '這是問題範例',
      answer: '這是答案範例',
      category: '一般問題',
      priority: 1,
      enabled: true
    });

    worksheet.addRow({
      language: 'en',
      keywords: 'keyword1,keyword2',
      question: 'This is a sample question',
      answer: 'This is a sample answer',
      category: 'General',
      priority: 1,
      enabled: true
    });

    worksheet.getRow(1).font = { bold: true };
    worksheet.getRow(1).fill = {
      type: 'pattern',
      pattern: 'solid',
      fgColor: { argb: 'FFE0E0E0' }
    };

    res.setHeader('Content-Type', 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet');
    res.setHeader('Content-Disposition', 'attachment; filename=knowledge-template.xlsx');

    await workbook.xlsx.write(res);
    res.end();

    console.log('✅ 成功下載範本');

  } catch (error) {
    console.error('下載範本錯誤:', error);
    res.status(500).json({ success: false, message: '下載範本失敗: ' + error.message });
  }
});

app.get('/api/export-knowledge', async (req, res) => {
  try {
    const fileContent = await fs.readFile(KNOWLEDGE_BASE_PATH, 'utf-8');
    const zhData = extractExistingData(fileContent, 'zh');
    const enData = extractExistingData(fileContent, 'en');

    if (zhData.length === 0 && enData.length === 0) {
      return res.status(404).json({ 
        success: false, 
        message: '知識庫中沒有資料' 
      });
    }

    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('知識庫');

    worksheet.columns = [
      { header: 'language', key: 'language', width: 10 },
      { header: 'keywords', key: 'keywords', width: 30 },
      { header: 'question', key: 'question', width: 40 },
      { header: 'answer', key: 'answer', width: 50 },
      { header: 'category', key: 'category', width: 15 },
      { header: 'priority', key: 'priority', width: 10 },
      { header: 'enabled', key: 'enabled', width: 10 }
    ];

    zhData.forEach(item => {
      worksheet.addRow({
        language: 'zh',
        keywords: Array.isArray(item.keywords) ? item.keywords.join(',') : '',
        question: item.question || '',
        answer: item.answer || '',
        category: item.category || '',
        priority: item.priority || 1,
        enabled: item.enabled !== false
      });
    });

    enData.forEach(item => {
      worksheet.addRow({
        language: 'en',
        keywords: Array.isArray(item.keywords) ? item.keywords.join(',') : '',
        question: item.question || '',
        answer: item.answer || '',
        category: item.category || '',
        priority: item.priority || 1,
        enabled: item.enabled !== false
      });
    });

    worksheet.getRow(1).font = { bold: true };
    worksheet.getRow(1).fill = {
      type: 'pattern',
      pattern: 'solid',
      fgColor: { argb: 'FFE0E0E0' }
    };

    const timestamp = new Date().toISOString().replace(/[:.]/g, '-').slice(0, 19);
    const filename = `knowledge-export-${timestamp}.xlsx`;

    res.setHeader('Content-Type', 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet');
    res.setHeader('Content-Disposition', `attachment; filename=${filename}`);

    await workbook.xlsx.write(res);
    res.end();

    console.log(`✅ 成功導出知識庫: ${zhData.length + enData.length} 筆資料`);

  } catch (error) {
    console.error('導出知識庫錯誤:', error);
    res.status(500).json({ success: false, message: '導出知識庫失敗: ' + error.message });
  }
});

function generateKnowledgeBaseContent(zhData, enData) {
  const formatItem = (item) => {
    const keywords = item.keywords.map(k => `'${k}'`).join(', ');
    const question = item.question.replace(/'/g, "\\'").replace(/\n/g, '\\n');
    const answer = item.answer.replace(/'/g, "\\'").replace(/\n/g, '\\n');
    return `    {
      keywords: [${keywords}],
      question: '${question}',
      answer: '${answer}',
      category: '${item.category}',
      priority: ${item.priority},
      enabled: ${item.enabled}
    }`;
  };

  const zhItems = zhData.map(formatItem).join(',\n');
  const enItems = enData.map(formatItem).join(',\n');

  return `// 知識庫類型定義
export interface KnowledgeItem {
  keywords: string[];
  question: string;
  answer: string;
  category: string;
  priority: number;
  enabled: boolean;
}

// 知識庫數據
export const knowledgeBase: Record<'zh' | 'en', KnowledgeItem[]> = {
  zh: [
${zhItems}
  ],
  en: [
${enItems}
  ]
};

// 搜索知識庫
export const searchKnowledge = (query: string, language: 'zh' | 'en' = 'zh'): KnowledgeItem | null => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  const lowerQuery = query.toLowerCase();
  
  // 尋找最佳匹配
  for (const item of items) {
    // 跳過未啟用的項目
    if (item.enabled === false) continue;
    
    for (const keyword of item.keywords) {
      if (lowerQuery.includes(keyword.toLowerCase())) {
        return item;
      }
    }
  }
  
  return null;
};

// 獲取隨機回應(當沒有找到匹配時)
export const getRandomResponse = (language: 'zh' | 'en' = 'zh'): string => {
  const responses = language === 'zh' ? [
    '很抱歉，我在知識庫中沒有找到相關的資訊。\\n\\n不過別擔心！您可以：\\n• 直接聯繫我們的專業園藝顧問\\n• 重新描述您的問題，我會再次為您查找\\n• 查看我們的常見問題頁面\\n\\n我們的專家團隊隨時準備為您提供專業建議！',
    '抱歉我暫時無法回答這個問題。\\n\\n建議您可以：\\n• 嘗試用不同的關鍵字重新提問\\n• 撥打我們的服務專線\\n• 透過聯絡表單詳細描述您的需求\\n\\n我們會盡快為您提供專業的園藝建議！',
    '這個問題超出了我目前的知識範圍。\\n\\n為了給您最專業的回答：\\n• 建議預約免費諮詢服務\\n• 加入我們的官方LINE獲得即時協助\\n• 瀏覽我們的作品集找尋靈感\\n\\n讓專業團隊為您打造夢想花園！'
  ] : [
    'I apologize, but I couldn\\'t find relevant information in my knowledge base.\\n\\nDon\\'t worry! You can:\\n• Contact our professional gardening consultants directly\\n• Rephrase your question and I\\'ll search again\\n• Check our FAQ page\\n\\nOur expert team is always ready to provide professional advice!',
    'Sorry, I can\\'t answer this question at the moment.\\n\\nI suggest you:\\n• Try different keywords to rephrase your question\\n• Call our service hotline\\n• Use our contact form to describe your needs in detail\\n\\nWe\\'ll provide professional gardening advice as soon as possible!',
    'This question is beyond my current knowledge scope.\\n\\nFor the most professional answer:\\n• Book a free consultation service\\n• Join our official LINE for instant assistance\\n• Browse our portfolio for inspiration\\n\\nLet our professional team create your dream garden!'
  ];
  
  return responses[Math.floor(Math.random() * responses.length)];
};

// 獲取所有分類
export const getCategories = (language: 'zh' | 'en' = 'zh'): string[] => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  const categories = [...new Set(items.map(item => item.category))];
  return categories;
};

// 根據分類獲取問題
export const getQuestionsByCategory = (category: string, language: 'zh' | 'en' = 'zh'): KnowledgeItem[] => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  return items.filter(item => item.category === category && item.enabled !== false);
};
`;
}

function extractExistingData(fileContent, lang) {
  const data = [];
  
  const langStart = fileContent.indexOf(`${lang}: [`);
  if (langStart === -1) return data;
  
  let braceCount = 0;
  let inArray = false;
  let currentItem = {};
  let currentKey = '';
  let currentValue = '';
  let inString = false;
  let inArray2 = false;
  
  for (let i = langStart; i < fileContent.length; i++) {
    const char = fileContent[i];
    
    if (char === '[' && !inString) {
      if (!inArray) {
        inArray = true;
        continue;
      } else {
        inArray2 = true;
      }
    }
    
    if (char === ']' && !inString) {
      if (inArray2) {
        inArray2 = false;
        if (currentKey === 'keywords') {
          currentItem.keywords = currentValue.split(',').map(k => k.trim().replace(/'/g, ''));
          currentValue = '';
        }
      } else if (inArray && braceCount === 0) {
        if (Object.keys(currentItem).length > 0) {
          data.push(currentItem);
        }
        break;
      }
    }
    
    if (char === '{' && !inString) {
      braceCount++;
      if (braceCount === 1) {
        currentItem = {};
      }
      continue;
    }
    
    if (char === '}' && !inString) {
      braceCount--;
      if (braceCount === 0 && Object.keys(currentItem).length > 0) {
        if (currentKey && currentValue) {
          if (currentKey === 'priority') {
            currentItem[currentKey] = parseInt(currentValue);
          } else if (currentKey === 'enabled') {
            currentItem[currentKey] = currentValue.trim() === 'true';
          } else {
            currentItem[currentKey] = currentValue.replace(/\\n/g, '\n').replace(/\\'/g, "'");
          }
        }
        data.push(currentItem);
        currentItem = {};
        currentKey = '';
        currentValue = '';
      }
      continue;
    }
    
    if (braceCount > 0) {
      if (char === "'" && fileContent[i - 1] !== '\\') {
        inString = !inString;
        continue;
      }
      
      if (!inString && char === ':') {
        currentKey = currentValue.trim();
        currentValue = '';
        continue;
      }
      
      if (!inString && (char === ',' || char === '\n') && currentKey && !inArray2) {
        if (currentKey === 'keywords') {
        } else if (currentKey === 'priority') {
          currentItem[currentKey] = parseInt(currentValue.trim());
        } else if (currentKey === 'enabled') {
          currentItem[currentKey] = currentValue.trim() === 'true';
        } else {
          currentItem[currentKey] = currentValue.trim().replace(/\\n/g, '\n').replace(/\\'/g, "'");
        }
        currentKey = '';
        currentValue = '';
        continue;
      }
      
      if (inString || inArray2 || (char !== ' ' && char !== '\n' && char !== '\t') || currentValue.length > 0) {
        currentValue += char;
      }
    }
  }
  
  return data;
}

function mergeData(existing, newData) {
  const questionSet = new Set(existing.map(item => item.question));
  const merged = [...existing];

  newData.forEach(item => {
    if (!questionSet.has(item.question)) {
      merged.push(item);
    }
  });

  return merged;
}

app.listen(PORT, () => {
  console.log(`🚀 後端伺服器運行在 http://localhost:${PORT}`);
  console.log(`📁 知識庫路徑: ${KNOWLEDGE_BASE_PATH}`);
});



================================================================
File Path: src/server/package.json
================================================================

{
  "name": "knowledge-base-server",
  "version": "1.0.0",
  "description": "Knowledge Base Upload Server",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  },
  "dependencies": {
    "express": "^4.18.2",
    "cors": "^2.8.5",
    "multer": "^1.4.5-lts.1",
    "papaparse": "^5.4.1",
    "exceljs": "^4.3.0"
  },
  "devDependencies": {
    "nodemon": "^3.0.1"
  }
}



================================================================
File Path: src/services/dataImporter.ts
================================================================

import Papa from 'papaparse';
import ExcelJS from 'exceljs';
import { CSVRow, ProcessedKnowledgeItem } from '../types/uploadTypes';
import { validateData, sanitizeData } from '../utils/fileValidator';
import { knowledgeBase, KnowledgeItem } from './knowledgeBase';

export class DataImporter {
  // 解析 CSV 文件
  async parseCSV(file: File): Promise<CSVRow[]> {
    return new Promise((resolve, reject) => {
      Papa.parse(file, {
        header: true,
        skipEmptyLines: true,
        encoding: 'UTF-8',
        complete: (results) => {
          if (results.errors.length > 0) {
            reject(new Error(`CSV 解析錯誤：${results.errors.map(e => e.message).join(', ')}`));
          } else {
            resolve(results.data as CSVRow[]);
          }
        },
        error: (error) => {
          reject(new Error(`CSV 解析失敗：${error.message}`));
        }
      });
    });
  }

  // 解析 Excel 文件 - 使用 ExcelJS
  async parseExcel(file: File): Promise<CSVRow[]> {
    return new Promise((resolve, reject) => {
      const reader = new FileReader();
      
      reader.onload = async (e) => {
        try {
          const data = new Uint8Array(e.target?.result as ArrayBuffer);
          
          const workbook = new ExcelJS.Workbook();
          await workbook.xlsx.load(data.buffer);
          
          const worksheet = workbook.worksheets[0];
          
          if (!worksheet) {
            reject(new Error('Excel 文件中沒有工作表'));
            return;
          }

          const jsonData: any[][] = [];
          
          worksheet.eachRow((row, rowNumber) => {
            const rowValues = row.values as any[];
            jsonData.push(rowValues.slice(1));
          });
          
          if (jsonData.length < 2) {
            reject(new Error('Excel 文件至少需要標題行和一行數據'));
            return;
          }

          const headers = jsonData[0].map(h => String(h || ''));
          const rows = jsonData.slice(1);

          const csvData: CSVRow[] = rows
            .filter(row => row.some(cell => cell !== null && cell !== undefined && cell !== ''))
            .map(row => {
              const obj: any = {};
              headers.forEach((header, index) => {
                const value = row[index];
                obj[header] = value !== null && value !== undefined ? String(value) : '';
              });
              return obj;
            });

          resolve(csvData);
        } catch (error) {
          reject(new Error(`Excel 解析失敗：${error instanceof Error ? error.message : String(error)}`));
        }
      };

      reader.onerror = () => {
        reject(new Error('檔案讀取失敗'));
      };

      reader.readAsArrayBuffer(file);
    });
  }

  // 解析文件（自動判斷類型）
  async parseFile(file: File): Promise<CSVRow[]> {
    const fileExtension = file.name.toLowerCase().split('.').pop();
    
    if (fileExtension === 'csv') {
      return this.parseCSV(file);
    } else if (['xlsx', 'xls'].includes(fileExtension || '')) {
      return this.parseExcel(file);
    } else {
      throw new Error('不支援的檔案格式');
    }
  }

  // 處理並導入數據
  async importData(file: File, mode: 'replace' | 'merge' = 'replace'): Promise<{
    success: boolean;
    message: string;
    stats: {
      total: number;
      zh: number;
      en: number;
      categories: string[];
    };
  }> {
    try {
      // 1. 驗證檔案
      const rawData = await this.parseFile(file);
      const validation = validateData(rawData);
      
      if (!validation.isValid) {
        throw new Error(`數據驗證失敗：\n${validation.errors.join('\n')}`);
      }

      // 2. 上傳到後端
      const formData = new FormData();
      formData.append('file', file);
      formData.append('mode', mode);

      const response = await fetch('http://localhost:3001/api/upload-knowledge', {
        method: 'POST',
        body: formData
      });

      if (!response.ok) {
        const errorData = await response.json().catch(() => ({}));
        throw new Error(errorData.message || `伺服器錯誤：${response.status}`);
      }

      const result = await response.json();

      if (!result.success) {
        throw new Error(result.message);
      }

      // 3. 成功後重新載入頁面
      setTimeout(() => {
        window.location.reload();
      }, 1500);

      return {
        success: true,
        message: result.message,
        stats: result.stats
      };

    } catch (error) {
      return {
        success: false,
        message: `導入失敗：${error instanceof Error ? error.message : String(error)}`,
        stats: { total: 0, zh: 0, en: 0, categories: [] }
      };
    }
  }

  // 導出當前知識庫為 Excel
  async exportToExcel(): Promise<ExcelJS.Buffer> {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('Knowledge Base');

    worksheet.columns = [
      { header: 'keywords', key: 'keywords', width: 30 },
      { header: 'question', key: 'question', width: 40 },
      { header: 'answer', key: 'answer', width: 60 },
      { header: 'category', key: 'category', width: 20 },
      { header: 'priority', key: 'priority', width: 10 },
      { header: 'enabled', key: 'enabled', width: 10 },
      { header: 'language', key: 'language', width: 10 }
    ];

    knowledgeBase.zh.forEach(item => {
      worksheet.addRow({
        keywords: item.keywords.join(','),
        question: item.question,
        answer: item.answer,
        category: item.category,
        priority: item.priority,
        enabled: item.enabled,
        language: 'zh'
      });
    });

    knowledgeBase.en.forEach(item => {
      worksheet.addRow({
        keywords: item.keywords.join(','),
        question: item.question,
        answer: item.answer,
        category: item.category,
        priority: item.priority,
        enabled: item.enabled,
        language: 'en'
      });
    });

    worksheet.getRow(1).font = { bold: true };
    worksheet.getRow(1).fill = {
      type: 'pattern',
      pattern: 'solid',
      fgColor: { argb: 'FFE0E0E0' }
    };

    return await workbook.xlsx.writeBuffer();
  }

  // 下載 Excel 範本
  async downloadTemplate(): Promise<void> {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('Template');

    worksheet.columns = [
      { header: 'keywords', key: 'keywords', width: 30 },
      { header: 'question', key: 'question', width: 40 },
      { header: 'answer', key: 'answer', width: 60 },
      { header: 'category', key: 'category', width: 20 },
      { header: 'priority', key: 'priority', width: 10 },
      { header: 'enabled', key: 'enabled', width: 10 },
      { header: 'language', key: 'language', width: 10 }
    ];

    worksheet.addRow({
      keywords: '澆水,頻率,多肉',
      question: '多肉植物多久澆一次水？',
      answer: '多肉澆水指南：多肉植物建議7-10天澆水一次，冬季可延長至2週。澆水要澆透，但避免積水。小撇步：觀察土壤乾燥程度，確保排水良好。',
      category: '植栽養護',
      priority: 1,
      enabled: true,
      language: 'zh'
    });

    worksheet.addRow({
      keywords: 'watering,frequency,succulent',
      question: 'How often should I water succulents?',
      answer: 'Succulent Watering Guide: Water every 7-10 days, extending to 2 weeks in winter. Water thoroughly but avoid waterlogging. Tip: Check soil dryness and ensure good drainage.',
      category: 'Plant Care',
      priority: 1,
      enabled: true,
      language: 'en'
    });

    worksheet.getRow(1).font = { bold: true };
    worksheet.getRow(1).fill = {
      type: 'pattern',
      pattern: 'solid',
      fgColor: { argb: 'FFE0E0E0' }
    };

    const buffer = await workbook.xlsx.writeBuffer();
    const blob = new Blob([buffer], { 
      type: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' 
    });
    
    const link = document.createElement('a');
    const url = URL.createObjectURL(blob);
    
    link.setAttribute('href', url);
    link.setAttribute('download', 'knowledge_base_template.xlsx');
    link.style.visibility = 'hidden';
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    
    setTimeout(() => URL.revokeObjectURL(url), 100);
  }

  // 導出完整知識庫為 Excel
  async downloadKnowledgeBase(): Promise<void> {
    const buffer = await this.exportToExcel();
    
    const blob = new Blob([buffer], { 
      type: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' 
    });
    
    const link = document.createElement('a');
    const url = URL.createObjectURL(blob);
    
    const now = new Date();
    const timestamp = now.toISOString().slice(0, 19).replace(/[:.]/g, '-');
    const filename = `knowledge_base_export_${timestamp}.xlsx`;
    
    link.setAttribute('href', url);
    link.setAttribute('download', filename);
    link.style.visibility = 'hidden';
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    
    setTimeout(() => URL.revokeObjectURL(url), 100);
  }
}

export const dataImporter = new DataImporter();


================================================================
File Path: src/services/knowledgeBase.ts
================================================================

// 知識庫類型定義
export interface KnowledgeItem {
  keywords: string[];
  question: string;
  answer: string;
  category: string;
  priority: number;
  enabled: boolean;
}

// 知識庫數據
export const knowledgeBase: Record<'zh' | 'en', KnowledgeItem[]> = {
  zh: [
    {
      keywords: ['[[[[澆水', '頻率', '多肉', '多久'],
      question: '多肉植物多久澆一次水？',
      answer: '多肉澆水指南：\n\n多肉植物建議7-10天澆水一次，冬季可延長至2週。澆水要澆透，但避免積水。\n\n小撇步：觀察土壤乾燥程度，確保排水良好。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[澆水', '時間', '夏天', '每天', '中午'],
      question: '夏天植物需要每天澆水嗎？',
      answer: '夏季澆水指南：\n\n大部分植物需要早晚澆水，避免中午高溫時段，可能造成根部燙傷。\n\n重要提醒：中午澆水會傷害植物根系，選擇清晨或傍晚時段。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[施肥', '頻率', '盆栽', '多久'],
      question: '盆栽植物多久施肥一次？',
      answer: '盆栽施肥時程：\n\n• 春夏季：每月一次\n• 秋冬季：每2-3個月一次\n• 注意：避免過量造成肥傷\n\n適當施肥有助植物健康成長。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[修剪', '時機', '樹木', '什麼時候'],
      question: '樹木什麼時候修剪最好？',
      answer: '修剪最佳時機：\n\n落葉樹在冬季休眠期修剪，常綠樹在春季新芽萌發前。避免梅雨季修剪。\n\n正確修剪促進健康生長。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[病蟲害', '防治', '預防', '處理'],
      question: '如何預防植物病蟲害？',
      answer: '病蟲害防治：\n\n定期檢查葉片、保持通風、適度澆水，發現問題及早處理。\n\n早期發現早期治療最有效。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[土壤', '改良', '排水', '透氣'],
      question: '如何改良土壤排水？',
      answer: '土壤改良方法：\n\n添加珍珠岩、蛭石或粗砂改善排水，混合腐葉土增加透氣性。\n\n良好排水是植物健康的基礎。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[換盆', '時機', '盆栽', '什麼時候'],
      question: '盆栽什麼時候需要換盆？',
      answer: '換盆時機判斷：\n\n當根系從排水孔長出或土壤板結時需要換盆，通常1-2年一次。\n\n適時換盆讓植物持續健康成長。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[陽光', '需求', '室內', '光照'],
      question: '室內植物需要多少陽光？',
      answer: '室內植物光照需求：\n\n大部分室內植物需要明亮散射光，避免直射強光。可放置在窗邊或使用植物燈補光。\n\n適當光照是植物生長的關鍵。',
      category: '植栽養護',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[色彩', '搭配', '花園', '植物'],
      question: '花園植物色彩該如何搭配？',
      answer: '色彩搭配原則：\n\n運用三色原則：主色調吸引目光，輔助色平衡視覺，點綴色增加層次變化。\n\n創造和諧又有變化的視覺效果。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[空間', '規劃', '小庭院', '設計'],
      question: '小庭院如何規劃空間？',
      answer: '小空間設計技巧：\n\n採用垂直綠化、多層次種植，運用鏡面或淺色系放大視覺空間。\n\n巧妙設計讓小空間也能很精彩。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[風格', '選擇', '庭院', '設計風格'],
      question: '庭院設計有哪些風格？',
      answer: '常見庭院風格：\n\n• 現代簡約：線條俐落，色彩單純\n• 自然野趣：模擬自然生態\n• 日式禪風：注重意境與平衡\n• 歐式古典：對稱布局，精緻雕飾\n\n選擇符合生活型態的風格。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[水景', '設計', '庭院', '噴泉'],
      question: '庭院水景如何設計？',
      answer: '水景設計要點：\n\n考慮水循環系統、防水處理、周邊植栽搭配，營造自然生態感。\n\n流水聲能創造放鬆氛圍。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[照明', '夜景', '庭院', '燈光'],
      question: '庭院夜間照明如何規劃？',
      answer: '夜景照明設計：\n\n結合功能照明與情境照明，重點照射植栽與景觀特色，避免光害。\n\n營造溫馨浪漫的夜間氛圍。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[步道', '設計', '庭院', '動線'],
      question: '庭院步道如何設計？',
      answer: '步道設計原則：\n\n考慮動線流暢性、材質防滑性、寬度適宜性，搭配兩側植栽引導視線。\n\n好的步道設計引導探索樂趣。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[圍籬', '隱私', '庭院', '遮蔽'],
      question: '如何設計庭院隱私空間？',
      answer: '隱私空間營造：\n\n運用植栽圍籬、格柵屏風或高低層次種植，既保有隱私又不失美觀。\n\n自然圍籬比硬體圍牆更有生命力。',
      category: '景觀設計',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[施工', '時間', '工期', '多久'],
      question: '庭院施工需要多長時間？',
      answer: '施工工期評估：\n\n小型庭院1-2週，大型景觀約3-4週，需視天氣與複雜度調整。\n\n實際工期依現場狀況而定。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[準備', '施工前', '注意事項', '準備工作'],
      question: '施工前需要準備什麼？',
      answer: '施工前準備事項：\n\n• 確認設計圖面\n• 清理施工區域\n• 確保水電管線位置\n• 準備臨時停車空間\n\n充分準備讓施工更順利。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[天氣', '影響', '施工', '下雨'],
      question: '天氣會影響施工進度嗎？',
      answer: '天氣對施工的影響：\n\n雨天會暫停戶外作業，強風影響高空作業，我們會依天氣調整工序。\n\n安全第一，品質為重。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[材料', '選擇', '品質', '建材'],
      question: '如何選擇合適的施工材料？',
      answer: '材料選擇原則：\n\n考慮耐候性、維護便利性、美觀性與預算平衡，選用品質認證材料。\n\n好材料是品質保證的基礎。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[安全', '施工', '注意', '防護'],
      question: '施工現場如何確保安全？',
      answer: '施工安全措施：\n\n設置安全圍籬、配戴防護設備、定期安全檢查，確保工作人員與住戶安全。\n\n安全是我們的首要考量。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[驗收', '完工', '檢查', '標準'],
      question: '完工後如何進行驗收？',
      answer: '驗收檢查項目：\n\n• 植栽存活狀況\n• 排水系統功能\n• 硬體設施完整性\n• 清潔整理完成度\n\n詳細驗收確保品質。',
      category: '施工作業',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[付款', '方式', '施工', '分期'],
      question: '施工付款如何安排？',
      answer: '付款方式說明：\n\n一般採三階段付款：簽約30%、施工中40%、完工30%。\n\n依工程進度付款較有保障。',
      category: '付款條件',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[報價', '費用', '估價', '多少錢'],
      question: '庭院設計費用如何計算？',
      answer: '費用計算方式：\n\n依設計複雜度、施工面積、材料等級綜合評估，提供透明化報價單。\n\n詳細報價讓您清楚每項費用。',
      category: '付款條件',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[保固', '期間', '維修', '保養'],
      question: '完工後有保固期嗎？',
      answer: '保固服務說明：\n\n植栽提供3個月保固，硬體設施1年保固，保固期內免費維修更換。\n\n完善保固讓您安心。',
      category: '付款條件',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[合約', '內容', '簽約', '注意'],
      question: '簽約時需要注意什麼？',
      answer: '合約注意事項：\n\n• 確認設計圖面與規格\n• 了解付款時程\n• 明確工期與保固條件\n• 保留變更設計彈性\n\n詳閱合約保障雙方權益。',
      category: '付款條件',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[服務', '範圍', '社區', '景觀', '維護'],
      question: '社區景觀維護包含哪些服務？',
      answer: '維護服務內容：\n\n包含修剪、除草、施肥、病蟲害防治及植栽補植等。\n\n全方位維護保持美觀。',
      category: '社區承作',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[合約', '社區', '長期', '維護'],
      question: '社區維護合約如何簽訂？',
      answer: '維護合約說明：\n\n可簽訂年度或多年期合約，依社區需求客製化服務內容與頻率。\n\n長期合作關係更穩定。',
      category: '社區承作',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[團隊', '專業', '證照', '經驗'],
      question: '維護團隊具備什麼專業？',
      answer: '專業團隊介紹：\n\n團隊具備園藝技術士證照，豐富社區維護經驗，定期教育訓練。\n\n專業認證品質保證。',
      category: '社區承作',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[緊急', '處理', '颱風', '災害'],
      question: '遇到緊急狀況如何處理？',
      answer: '緊急應變機制：\n\n24小時緊急聯絡專線，颱風後立即巡檢，優先處理安全隱患。\n\n快速應變確保安全。',
      category: '社區承作',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[規劃', '社區', '景觀', '整體'],
      question: '社區整體景觀如何規劃？',
      answer: '社區景觀規劃：\n\n考慮整體風格統一、分區功能明確、維護便利性，創造宜居環境。\n\n整體規劃提升居住品質。',
      category: '社區承作',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[風格', '諮詢', '別墅', '花園', '適合'],
      question: '別墅花園適合什麼風格？',
      answer: '別墅風格選擇：\n\n可選擇現代簡約、地中海、英式花園或日式禪風，依生活型態設計。\n\n打造專屬夢想花園。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[客製化', '設計', '個人', '需求'],
      question: '可以完全客製化設計嗎？',
      answer: '客製化設計服務：\n\n當然可以！我們提供一對一設計諮詢，依您的喜好與需求量身打造。\n\n獨一無二的專屬設計。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[智慧', '澆水', '自動', '系統'],
      question: '有智慧澆水系統嗎？',
      answer: '智慧澆水系統：\n\n提供自動澆水系統，可依天氣、土壤濕度自動調節，手機APP遠端控制。\n\n科技讓園藝更輕鬆。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[進口', '植栽', '特殊', '品種'],
      question: '可以種植進口特殊品種嗎？',
      answer: '進口植栽服務：\n\n可協助引進適合台灣氣候的進口品種，提供專業馴化與養護建議。\n\n引進世界級珍稀植栽。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[戶外家具', '庭園家具', '挑選', '家具'],
      question: '庭園家具如何挑選？',
      answer: '戶外家具選擇：\n\n選防水、防UV材質如鋁合金或藤編家具，兼顧美觀與耐用。\n\n耐候材質經久耐用。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[泳池景觀', '搭配', '泳池', '綠化'],
      question: '如何搭配泳池與綠化？',
      answer: '泳池景觀設計：\n\n採用棕櫚、芒果樹等熱帶植物搭配石材步道，營造度假氛圍。\n\n熱帶風情度假感受。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[地形設計', '坡地別墅', '造景', '坡地'],
      question: '坡地別墅如何造景？',
      answer: '坡地造景技巧：\n\n以階梯式花壇與天然石擋土牆分層設計，強化景觀深度。\n\n善用地形創造層次。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[環境永續', '高端景觀', 'ESG', '結合'],
      question: '高端景觀可結合ESG嗎？',
      answer: '永續景觀設計：\n\n可使用節能照明與雨水回收系統，符合永續理念。\n\n環保與美觀兼具。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[景觀維護', '完工後', '定期維護', '提供'],
      question: '完工後是否提供定期維護？',
      answer: '維護服務承諾：\n\n是，可提供月或季維護方案，確保綠化長期穩定。\n\n專業維護長期保障。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[視覺焦點', '庭院', '主視覺', '設計'],
      question: '庭院主視覺該如何設計？',
      answer: '視覺焦點設計：\n\n以雕塑、水景或孤植大樹作為焦點，加強空間層次。\n\n打造令人印象深刻的焦點。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[材料保養', '高階建材', '維護', '保養'],
      question: '高階建材要如何維護？',
      answer: '建材保養方法：\n\n定期清潔與防水塗層更新，延長耐候材料壽命。\n\n細心保養延長使用壽命。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[聲音設計', '靜謐氛圍', '打造', '氛圍'],
      question: '如何打造靜謐氛圍？',
      answer: '靜謐空間營造：\n\n利用流水聲或自然風鈴聲遮蔽外界噪音，營造放鬆空間。\n\n自然音律舒緩心靈。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[景觀整合', '花園', '建築外觀', '協調'],
      question: '花園與建築外觀如何協調？',
      answer: '建築景觀協調：\n\n採用相同色系與材質延續，使景觀與建築和諧統一。\n\n整體設計和諧統一。',
      category: '菁英高階',
      priority: 1,
      enabled: true
    }
  ],
  en: [
    {
      keywords: ['[[[[watering', 'frequency', 'succulent', 'how often'],
      question: 'How often should I water succulents?',
      answer: 'Succulent Watering Guide:\n\nSucculents should be watered every 7-10 days, extending to 2 weeks in winter. Water thoroughly but avoid waterlogging.\n\nTip: Check soil dryness and ensure good drainage.',
      category: 'Plant Care',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[watering', 'time', 'summer', 'daily', 'noon'],
      question: 'Do plants need daily watering in summer?',
      answer: 'Summer Watering Guidelines:\n\nMost plants need watering morning and evening, avoid noon high temperature periods that may cause root burn.\n\nImportant: Noon watering can damage plant roots, choose early morning or evening.',
      category: 'Plant Care',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[fertilizer', 'frequency', 'potted', 'how often'],
      question: 'How often should I fertilize potted plants?',
      answer: 'Potted Plant Fertilizing Schedule:\n\n• Spring/Summer: Once a month\n• Fall/Winter: Every 2-3 months\n• Note: Avoid excess to prevent fertilizer burn\n\nProper fertilizing promotes healthy plant growth.',
      category: 'Plant Care',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[color', 'matching', 'garden', 'plants'],
      question: 'How should garden plant colors be matched?',
      answer: 'Color Matching Principles:\n\nUse three main color rule: main color for attraction, secondary color for balance, accent color for layered variation.\n\nCreate harmonious yet varied visual effects.',
      category: 'Landscape Design',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[construction', 'duration', 'how long', 'time'],
      question: 'How long does garden construction take?',
      answer: 'Construction Duration Estimate:\n\nSmall gardens 1-2 weeks, large landscaping about 3-4 weeks, adjusted for weather and complexity.\n\nActual duration depends on site conditions.',
      category: 'Construction',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[payment', 'method', 'construction', 'installment'],
      question: 'How is construction payment structured?',
      answer: 'Payment Structure:\n\nGeneral three-stage payment: 30% at signing, 40% mid-construction, 30% at completion.\n\nProgress-based payment provides security.',
      category: 'Payment Terms',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[service', 'scope', 'community', 'landscape', 'maintenance'],
      question: 'What does community landscape maintenance include?',
      answer: 'Maintenance Service Content:\n\nIncludes pruning, weeding, fertilizing, pest control and plant replacement.\n\nComprehensive maintenance keeps beauty.',
      category: 'Community Projects',
      priority: 1,
      enabled: true
    },
    {
      keywords: ['[[[[style', 'consultation', 'villa', 'garden', 'suitable'],
      question: 'What styles suit villa gardens?',
      answer: 'Villa Style Options:\n\nChoose from modern minimalist, Mediterranean, English garden or Japanese zen, designed according to lifestyle.\n\nCreate your exclusive dream garden.',
      category: 'Premium Services',
      priority: 1,
      enabled: true
    }
  ]
};

// 搜索知識庫
export const searchKnowledge = (query: string, language: 'zh' | 'en' = 'zh'): KnowledgeItem | null => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  const lowerQuery = query.toLowerCase();
  
  // 尋找最佳匹配
  for (const item of items) {
    // 跳過未啟用的項目
    if (item.enabled === false) continue;
    
    for (const keyword of item.keywords) {
      if (lowerQuery.includes(keyword.toLowerCase())) {
        return item;
      }
    }
  }
  
  return null;
};

// 獲取隨機回應(當沒有找到匹配時)
export const getRandomResponse = (language: 'zh' | 'en' = 'zh'): string => {
  const responses = language === 'zh' ? [
    '很抱歉，我在知識庫中沒有找到相關的資訊。\n\n不過別擔心！您可以：\n• 直接聯繫我們的專業園藝顧問\n• 重新描述您的問題，我會再次為您查找\n• 查看我們的常見問題頁面\n\n我們的專家團隊隨時準備為您提供專業建議！',
    '抱歉我暫時無法回答這個問題。\n\n建議您可以：\n• 嘗試用不同的關鍵字重新提問\n• 撥打我們的服務專線\n• 透過聯絡表單詳細描述您的需求\n\n我們會盡快為您提供專業的園藝建議！',
    '這個問題超出了我目前的知識範圍。\n\n為了給您最專業的回答：\n• 建議預約免費諮詢服務\n• 加入我們的官方LINE獲得即時協助\n• 瀏覽我們的作品集找尋靈感\n\n讓專業團隊為您打造夢想花園！'
  ] : [
    'I apologize, but I couldn\'t find relevant information in my knowledge base.\n\nDon\'t worry! You can:\n• Contact our professional gardening consultants directly\n• Rephrase your question and I\'ll search again\n• Check our FAQ page\n\nOur expert team is always ready to provide professional advice!',
    'Sorry, I can\'t answer this question at the moment.\n\nI suggest you:\n• Try different keywords to rephrase your question\n• Call our service hotline\n• Use our contact form to describe your needs in detail\n\nWe\'ll provide professional gardening advice as soon as possible!',
    'This question is beyond my current knowledge scope.\n\nFor the most professional answer:\n• Book a free consultation service\n• Join our official LINE for instant assistance\n• Browse our portfolio for inspiration\n\nLet our professional team create your dream garden!'
  ];
  
  return responses[Math.floor(Math.random() * responses.length)];
};

// 獲取所有分類
export const getCategories = (language: 'zh' | 'en' = 'zh'): string[] => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  const categories = [...new Set(items.map(item => item.category))];
  return categories;
};

// 根據分類獲取問題
export const getQuestionsByCategory = (category: string, language: 'zh' | 'en' = 'zh'): KnowledgeItem[] => {
  const items = knowledgeBase[language] || knowledgeBase.zh;
  return items.filter(item => item.category === category && item.enabled !== false);
};



================================================================
File Path: src/services/videoBase.ts
================================================================

// src/services/videoBase.ts

export interface VideoItem {
  videoId: string;
  title_zh: string;
  title_en: string;
  description_zh: string;
  description_en: string;
  category: 'hero' | 'gallery';
  enabled: boolean;
}

export const videoBase: VideoItem[] = [
  {
    "videoId": "PK7veIY94Rc",
    "title_zh": "客戶回訪實錄。",
    "title_en": "Customer Revisit Record.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "GhZYPoq9-P0",
    "title_zh": "重要關鍵—信賴EGD。",
    "title_en": "Key Factor—Trust EGD.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "INnUG4JHrOQ",
    "title_zh": "您的擔心，都被「都值得了」取代。",
    "title_en": "Your Worries, All Replaced by \"It Was Worth It\".",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "TFQMGVSEOA4",
    "title_zh": "侘寂之境(Wabi-Sabi)，極簡美學。",
    "title_en": "Wabi-Sabi Realm, Minimalist Aesthetics.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "h8edKG3H-6Y",
    "title_zh": "台灣EGD: 願美好永遠存在。",
    "title_en": "Taiwan EGD: May Goodness Forever Endure.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "byFTTj1znH0",
    "title_zh": "再有難度-用心作園藝。",
    "title_en": "No Matter How Difficult—Gardening with Heart.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "uwDDYu8mI3Q",
    "title_zh": "帶你上雲端！為高空定義真正的夢幻花園。",
    "title_en": "Take You to the Clouds! Defining a True Dream Garden at Heights.",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "ddGXcJUxORM",
    "title_zh": "征服困難崎零地，打造夢幻庭園!",
    "title_en": "Conquer Difficult Terrain, Create a Dream Garden!",
    "description_zh": "",
    "description_en": "",
    "category": "hero",
    "enabled": true
  },
  {
    "videoId": "rfS4HxVM1ps",
    "title_zh": "植癒生活:讓美好,在指尖與花葉間永續。",
    "title_en": "Plant Healing Life: Let Beauty Flourish Sustainably, Between Your Fingertips and the Greenery.",
    "description_zh": "植癒生活:讓美好,在指尖與花葉間永續。",
    "description_en": "Plant Healing Life: Let Beauty Flourish Sustainably, Between Your Fingertips and the Greenery.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "o3qBmM54Fbs",
    "title_zh": "視覺魔術-瞬間上色!",
    "title_en": "Visual Alchemy! Monochrome Rendered in Color!",
    "description_zh": "視覺魔術-瞬間上色!",
    "description_en": "Visual Alchemy! Monochrome Rendered in Color!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "U_XKi919euc",
    "title_zh": "超越視野-定義新標竿。",
    "title_en": "Beyond the Horizon: Defining the New Benchmark.",
    "description_zh": "超越視野-定義新標竿。",
    "description_en": "Beyond the horizon: Defining the new benchmark.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "xm3UtfIysl0",
    "title_zh": "施工、驗收與完美交付!",
    "title_en": "Execution, Verification, and Perfect Handoff!",
    "description_zh": "施工、驗收與完美交付!",
    "description_en": "Execution, Verification, and Perfect Handoff!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "9au64VDA06k",
    "title_zh": "復育生態鏈:給下一代最好的禮物。",
    "title_en": "The Ultimate Forest Gift for the Next Generation.",
    "description_zh": "復育生態鏈:給下一代最好的禮物。",
    "description_en": "The Ultimate Forest Gift for the Next Generation.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "GO9AFVEqFzk",
    "title_zh": "秋日黃金海",
    "title_en": "A Golden Sea in Autumn, Dyeing a Thousand Peaks.",
    "description_zh": "秋日黃金海",
    "description_en": "A Golden Sea in Autumn, Dyeing a Thousand Peaks.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "0N4J6sYIr50",
    "title_zh": "草地變魔戒森林？頻率是關鍵！",
    "title_en": "Frequency is the Key!",
    "description_zh": "草地變魔戒森林？頻率是關鍵！",
    "description_en": "Frequency is the Key!",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "SV9H23E_R9Q",
    "title_zh": "15秒!就是台灣系列: 預告片。",
    "title_en": "Taiwan in 15 Seconds! The Teaser.",
    "description_zh": "15秒!就是台灣系列: 預告片。",
    "description_en": "Taiwan in 15 Seconds! The Teaser.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "ylhvXL8ueW0",
    "title_zh": "從零到有,實現你的夢幻花園。",
    "title_en": "From Zero to Bloom: Realize Your Dream Garden.",
    "description_zh": "從零到有,實現你的夢幻花園。",
    "description_en": "From Zero to Bloom: Realize your dream garden.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "Rdg3Wo8p5bU",
    "title_zh": "白領: 享受周末的園藝時光!",
    "title_en": "Our Dreamy Weekend Indoor Gardening Routine.",
    "description_zh": "白領: 享受周末的園藝時光!",
    "description_en": "Our Dreamy Weekend Indoor Gardening Routine.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "AOUNGkD064I",
    "title_zh": "從積水到美景: 雨水花園。",
    "title_en": "Building Our Dream Rain Garden from Scratch.",
    "description_zh": "從積水到美景: 雨水花園。",
    "description_en": "Building Our Dream Rain Garden from Scratch.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "ryaP_GS_Hi8",
    "title_zh": "肖楠: 種子覺醒。",
    "title_en": "Seed to Life",
    "description_zh": "肖楠: 種子覺醒。",
    "description_en": "Seed to Life",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "K879oNZvLr8",
    "title_zh": "月桃: 何止是記憶,更是溫暖印記。",
    "title_en": "It's Grandma's Warm Legacy.",
    "description_zh": "月桃: 何止是記憶,更是溫暖印記。",
    "description_en": "It's Grandma's Warm Legacy.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "-4x07g4rlxo",
    "title_zh": "ESG-綠色永續營運。",
    "title_en": "ESG - Green Sustainable Operations.",
    "description_zh": "ESG-綠色永續營運。",
    "description_en": "ESG - Green Sustainable Operations.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "hO_fIaq0mjA",
    "title_zh": "浪載星屑，灣藏夢幻光。",
    "title_en": "Waves Carry Stardust, the Bay Holds a Magical Light.",
    "description_zh": "浪載星屑，灣藏夢幻光。",
    "description_en": "Waves carry stardust, the bay holds a magical light.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "hoYBYkCaoxg",
    "title_zh": "台灣衫: 極致的心靈森呼吸。",
    "title_en": "Give Your Mind the Ultimate Forest Bathing (Shinrin-yoku).",
    "description_zh": "台灣衫: 極致的心靈森呼吸。",
    "description_en": "Give Your Mind the Ultimate Forest Bathing (Shinrin-yoku).",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "oLwpEJpcd3k",
    "title_zh": "玉山圓柏: 環境再艱苦也絕不放棄。",
    "title_en": "A Resilience Guide",
    "description_zh": "玉山圓柏: 環境再艱苦也絕不放棄。",
    "description_en": "A Resilience Guide",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "rDlbaw7znEs",
    "title_zh": "藍眼淚，共同守護藍色星魂。",
    "title_en": "The Emotion of Guarding the Blue Star Soul.",
    "description_zh": "藍眼淚，共同守護藍色星魂。",
    "description_en": "The Emotion of Guarding the Blue Star Soul.",
    "category": "gallery",
    "enabled": true
  },
  {
    "videoId": "sFtCKquZYwM",
    "title_zh": "退休不空虛：告別無聊人生的實用指南。",
    "title_en": "A Practical Guide to Saying Goodbye to a Boring Life.",
    "description_zh": "退休不空虛：告別無聊人生的實用指南。",
    "description_en": "A Practical Guide to Saying Goodbye to a Boring Life.",
    "category": "gallery",
    "enabled": true
  }
];



================================================================
File Path: src/services/videoImporter.ts
================================================================

import ExcelJS from 'exceljs';
import { videoBase, VideoItem } from './videoBase';
import type { ValidationResult, ProcessedVideoItem, VideoCSVRow } from '../types/uploadTypes';

class VideoImporter {
  private static instance: VideoImporter;
  private videos: VideoItem[] = [...videoBase];
  private listeners: Set<() => void> = new Set();

  private constructor() {}

  static getInstance(): VideoImporter {
    if (!VideoImporter.instance) {
      VideoImporter.instance = new VideoImporter();
    }
    return VideoImporter.instance;
  }

  // 訂閱更新事件
  subscribe(listener: () => void): () => void {
    this.listeners.add(listener);
    return () => this.listeners.delete(listener);
  }

  // 通知所有訂閱者
  private notify(): void {
    this.listeners.forEach(listener => listener());
  }

  // 取得所有影片
  getAllVideos(): VideoItem[] {
    return this.videos;
  }

  // 取得 Hero Section 影片
  getHeroVideos(): VideoItem[] {
    return this.videos.filter(v => v.category === 'hero' && v.enabled);
  }

  // 取得 Gallery 影片
  getGalleryVideos(): VideoItem[] {
    return this.videos.filter(v => v.category === 'gallery' && v.enabled);
  }

  // 新增影片
  addVideo(video: VideoItem): void {
    this.videos.push(video);
    this.notify();
  }

  // 更新影片
  updateVideo(videoId: string, updatedVideo: VideoItem): void {
    const index = this.videos.findIndex(v => v.videoId === videoId);
    if (index !== -1) {
      this.videos[index] = updatedVideo;
      this.notify();
    }
  }

  // 刪除影片
  deleteVideo(videoId: string): void {
    this.videos = this.videos.filter(v => v.videoId !== videoId);
    this.notify();
  }

  // 驗證 Excel 檔案
  async validateExcelFile(file: File): Promise<ValidationResult> {
    const errors: string[] = [];
    const warnings: string[] = [];

    try {
      const workbook = new ExcelJS.Workbook();
      const arrayBuffer = await file.arrayBuffer();
      await workbook.xlsx.load(arrayBuffer);

      const worksheet = workbook.getWorksheet(1);
      if (!worksheet) {
        errors.push('找不到工作表');
        return { isValid: false, errors, warnings };
      }

      const headerRow = worksheet.getRow(1);
      const headers = headerRow.values as any[];
      
      const requiredColumns = ['videoId', 'title_zh', 'title_en', 'description_zh', 'description_en', 'category', 'enabled'];
      
      requiredColumns.forEach(col => {
        if (!headers.includes(col)) {
          errors.push(`缺少必要欄位: ${col}`);
        }
      });

      if (worksheet.rowCount < 2) {
        warnings.push('檔案中沒有資料行');
      }

      return {
        isValid: errors.length === 0,
        errors,
        warnings
      };

    } catch (error) {
      errors.push(`檔案解析失敗: ${error instanceof Error ? error.message : '未知錯誤'}`);
      return { isValid: false, errors, warnings };
    }
  }

  // 匯入 Excel
  async importFromExcel(file: File): Promise<{ success: boolean; message: string }> {
    try {
      const validation = await this.validateExcelFile(file);
      if (!validation.isValid) {
        throw new Error(validation.errors.join(', '));
      }

      // 上傳到本地服務器
      const formData = new FormData();
      formData.append('file', file);

      const response = await fetch('http://localhost:3001/api/upload-videos', {
        method: 'POST',
        body: formData
      });

      const result = await response.json();

      if (!result.success) {
        throw new Error(result.message);
      }


   // 成功後重新載入頁面
      setTimeout(() => {
        window.location.reload();
      }, 500);

      return {
        success: true,
        message: result.message,
      };

    } catch (error) {
      return {
        success: false,
        message: error instanceof Error ? error.message : '匯入失敗'
      };
    }
  }

  // 匯出 Excel
  async exportToExcel(): Promise<void> {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('Videos');

    // 設定欄位
    worksheet.columns = [
      { header: 'videoId', key: 'videoId', width: 20 },
      { header: 'title_zh', key: 'title_zh', width: 40 },
      { header: 'title_en', key: 'title_en', width: 40 },
      { header: 'description_zh', key: 'description_zh', width: 50 },
      { header: 'description_en', key: 'description_en', width: 50 },
      { header: 'category', key: 'category', width: 15 },
      { header: 'enabled', key: 'enabled', width: 10 }
    ];

    // 加入資料
    this.videos.forEach(video => {
      worksheet.addRow({
        videoId: video.videoId,
        title_zh: video.title_zh,
        title_en: video.title_en,
        description_zh: video.description_zh,
        description_en: video.description_en,
        category: video.category,
        enabled: video.enabled
      });
    });

    // 下載
    const buffer = await workbook.xlsx.writeBuffer();
    const blob = new Blob([buffer], { type: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' });
    const url = URL.createObjectURL(blob);
    const link = document.createElement('a');
    link.href = url;
    link.download = `videos-${new Date().toISOString().split('T')[0]}.xlsx`;
    link.click();
    URL.revokeObjectURL(url);
  }

  // 下載範本
  async downloadTemplate(): Promise<void> {
    const workbook = new ExcelJS.Workbook();
    const worksheet = workbook.addWorksheet('Videos Template');

    worksheet.columns = [
      { header: 'videoId', key: 'videoId', width: 20 },
      { header: 'title_zh', key: 'title_zh', width: 40 },
      { header: 'title_en', key: 'title_en', width: 40 },
      { header: 'description_zh', key: 'description_zh', width: 50 },
      { header: 'description_en', key: 'description_en', width: 50 },
      { header: 'category', key: 'category', width: 15 },
      { header: 'enabled', key: 'enabled', width: 10 }
    ];

    // 範例資料
    worksheet.addRow({
      videoId: 'PK7veIY94Rc',
      title_zh: '範例影片標題',
      title_en: 'Example Video Title',
      description_zh: '範例描述',
      description_en: 'Example Description',
      category: 'hero',
      enabled: true
    });

    const buffer = await workbook.xlsx.writeBuffer();
    const blob = new Blob([buffer], { type: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' });
    const url = URL.createObjectURL(blob);
    const link = document.createElement('a');
    link.href = url;
    link.download = 'video-template.xlsx';
    link.click();
    URL.revokeObjectURL(url);
  }
}

export default VideoImporter;


================================================================
File Path: src/test/testRLS1.ts
================================================================

import { createClient } from '@supabase/supabase-js';
import * as dotenv from 'dotenv';

dotenv.config();

const supabase = createClient(
  process.env.VITE_SUPABASE_URL!,
  process.env.VITE_SUPABASE_ANON_KEY!
);

const { data, error } = await supabase
  .from('knowledge_items')
  .select('*');

console.log('查詢結果數量:', data?.length);
console.log('資料:', data);
console.log('錯誤:', error);



================================================================
File Path: src/test/testRLS2.ts
================================================================

import { createClient } from '@supabase/supabase-js';
import * as dotenv from 'dotenv';

dotenv.config();

const supabase = createClient(
  process.env.VITE_SUPABASE_URL!,
  process.env.VITE_SUPABASE_ANON_KEY!
);

// 測試匿名新增
const { data, error } = await supabase
  .from('knowledge_items')
  .insert({ 
    language: 'zh', 
    keywords: ['測試新增'], 
    question: '測試', 
    answer: '測試', 
    category: '測試' 
  });

console.log('新增結果:', data);
console.log('錯誤:', error);



================================================================
File Path: src/types/uploadTypes.ts
================================================================

export interface CSVRow {
  keywords: string;
  question: string;
  answer: string;
  category: string;
  priority: string;
  enabled: string;
  language: string;
}

// 新增：影片 CSV 行定義
export interface VideoCSVRow {
  videoId: string;
  title_zh: string;
  title_en: string;
  description_zh: string;
  description_en: string;
  category: string;
  enabled: string;
}

export interface ValidationResult {
  isValid: boolean;
  errors: string[];
  warnings: string[];
  data?: any[];
}

export interface UploadProgress {
  status: 'idle' | 'uploading' | 'processing' | 'validating' | 'success' | 'error';
  progress: number;
  message: string;
}

export interface UploadConfig {
  allowedFormats: string[];
  maxFileSize: number;
  requiredColumns: string[];
  supportedLanguages: string[];
}

export interface ProcessedKnowledgeItem {
  keywords: string[];
  question: string;
  answer: string;
  category: string;
  priority: number;
  enabled: boolean;
  language: 'zh' | 'en';
}

// 新增：處理後的影片項目
export interface ProcessedVideoItem {
  videoId: string;
  title_zh: string;
  title_en: string;
  description_zh: string;
  description_en: string;
  category: 'hero' | 'gallery';
  enabled: boolean;
}


================================================================
File Path: src/utils/fileValidator.ts
================================================================

import { ValidationResult, CSVRow, UploadConfig } from "../types/uploadTypes";

export const uploadConfig: UploadConfig = {
  allowedFormats: [".csv", ".xlsx", ".xls"],
  maxFileSize: 10, // 10MB
  requiredColumns: ["keywords", "question", "answer", "category", "priority", "enabled", "language"],
  supportedLanguages: ["zh", "en"]
};

export const validateFile = (file: File): ValidationResult => {
  const errors: string[] = [];
  const warnings: string[] = [];

  // 檢查文件類型
  const fileExtension = file.name.toLowerCase().split(".").pop();
  if (!uploadConfig.allowedFormats.some(format => format.includes(fileExtension || ""))) {
    errors.push(`不支援的檔案格式。支援格式:${uploadConfig.allowedFormats.join(", ")}`);
  }

  // 檢查文件大小
  const fileSizeMB = file.size / (1024 * 1024);
  if (fileSizeMB > uploadConfig.maxFileSize) {
    errors.push(`檔案大小超過限制 ${uploadConfig.maxFileSize}MB,目前大小:${fileSizeMB.toFixed(2)}MB`);
  }

  return {
    isValid: errors.length === 0,
    errors,
    warnings
  };
};

export const validateData = (data: CSVRow[]): ValidationResult => {
  const errors: string[] = [];
  const warnings: string[] = [];

  if (!data || data.length === 0) {
    errors.push("檔案內容為空");
    return { isValid: false, errors, warnings };
  }

  // 檢查必要欄位
  const firstRow = data[0];
  const missingColumns = uploadConfig.requiredColumns.filter(
    col => !(col in firstRow)
  );

  if (missingColumns.length > 0) {
    errors.push(`缺少必要欄位:${missingColumns.join(", ")}`);
  }

  // 驗證每一行數據
  data.forEach((row, index) => {
    const rowNumber = index + 1;

    // 檢查必填欄位
    uploadConfig.requiredColumns.forEach(col => {
      if (!row[col as keyof CSVRow] || row[col as keyof CSVRow].trim() === "") {
        errors.push(`第 ${rowNumber} 行:${col} 欄位不能為空`);
      }
    });

    // 檢查語言格式
    if (row.language && !uploadConfig.supportedLanguages.includes(row.language)) {
      errors.push(`第 ${rowNumber} 行:不支援的語言 "${row.language}",支援:${uploadConfig.supportedLanguages.join(", ")}`);
    }

    // 檢查優先級格式
    if (row.priority && isNaN(Number(row.priority))) {
      errors.push(`第 ${rowNumber} 行:優先級必須是數字`);
    }

    // 檢查啟用狀態格式
    if (row.enabled && !["true", "false", "1", "0"].includes(row.enabled.toLowerCase())) {
      warnings.push(`第 ${rowNumber} 行:啟用狀態建議使用 true/false 或 1/0`);
    }

    // 檢查關鍵字格式
    if (row.keywords && row.keywords.includes(",")) {
      // 關鍵字應該用逗號分隔,這是正確的
    } else if (row.keywords && !row.keywords.includes(",")) {
      warnings.push(`第 ${rowNumber} 行:關鍵字建議用逗號分隔多個詞彙`);
    }
  });

  return {
    isValid: errors.length === 0,
    errors,
    warnings,
    data
  };
};

export const sanitizeData = (data: CSVRow[]): any[] => {
  return data.map(row => ({
    keywords: row.keywords?.split(",").map(k => k.trim()).filter(k => k) || [],
    question: row.question?.trim() || "",
    answer: row.answer?.trim() || "",
    category: row.category?.trim() || "",
    priority: parseInt(row.priority) || 1,
    enabled: ["true", "1"].includes(row.enabled?.toLowerCase()) || false,
    language: (row.language?.toLowerCase() as "zh" | "en") || "zh"
  }));
}; 

