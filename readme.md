

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

