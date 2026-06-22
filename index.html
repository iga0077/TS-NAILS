<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>TS Nails — Записи</title>

    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#7f603e">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="default">
    <meta name="apple-mobile-web-app-title" content="TS Nails">
    <link rel="apple-touch-icon" href="icons/icon-192.png">
    <link rel="icon" href="icons/icon-192.png" type="image/png">
    
    <script src="https://unpkg.com/react@18/umd/react.production.min.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js" crossorigin></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://www.gstatic.com/firebasejs/10.14.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.14.1/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.14.1/firebase-firestore-compat.js"></script>
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        nude: '#ecd0c2',       // Пудровый/Жемчужный
                        nudedark: '#d8b5a3',   // Темный пудровый
                        bronze: '#7f603e',     // Бронза/Карамель
                        bronzedark: '#5c442a', // Глубокая бронза
                        gold: '#d4af37',       // Золото для камня
                        golddark: '#a3803c',   // Темное золото
                        stonebg: '#0a0a0a',    // Глубокий черный камень
                        stonepanel: '#151515'  // Чуть светлее для панелей
                    }
                }
            }
        }
    </script>

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fdfbf9; /* Очень теплый, чуть кремовый белый */
            color: #3a2e26; /* Мягкий темный шоколад вместо черного/серого */
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            -webkit-tap-highlight-color: transparent;
            transition: background-color 0.4s ease, color 0.4s ease;
        }

        .dark body {
            background-color: #050505; /* Глубокий черный камень */
            color: #f1f0ea; /* Мягкий теплый белый */
        }

        /* Мягкие цветовые пятна - светлая тема (Нюд и Бронза) */
        .blob {
            position: fixed;
            border-radius: 50%;
            filter: blur(70px);
            z-index: -1;
            transition: all 0.6s ease;
            animation: float 12s ease-in-out infinite;
        }

        .blob-1 { top: -10%; left: -10%; width: 350px; height: 350px; background: #ecd0c2; opacity: 0.8; animation-delay: 0s; }
        .blob-2 { bottom: -10%; right: -10%; width: 400px; height: 400px; background: #f5e8e1; opacity: 0.9; animation-delay: -2s; }
        .blob-3 { top: 40%; left: 60%; width: 300px; height: 300px; background: #d8b5a3; opacity: 0.5; animation-delay: -4s; }

        /* Золотые прожилки - темная тема (Свечение из-под черного камня) */
        .dark .blob-1 { background: #d4af37; opacity: 0.15; width: 500px; height: 200px; transform: rotate(45deg); filter: blur(90px); }
        .dark .blob-2 { background: #a3803c; opacity: 0.2; width: 400px; height: 400px; filter: blur(100px); }
        .dark .blob-3 { background: #ffd700; opacity: 0.1; width: 300px; height: 500px; transform: rotate(-30deg); filter: blur(80px); }

        @keyframes float {
            0% { transform: translateY(0) scale(1) rotate(0deg); }
            50% { transform: translateY(-20px) scale(1.05) rotate(5deg); }
            100% { transform: translateY(0) scale(1) rotate(0deg); }
        }

        /* Глассморфизм - Светлый (Нежный хрусталь) */
        .glass-panel {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 1);
            box-shadow: 0 8px 32px -5px rgba(127, 96, 62, 0.08); /* Тень с легким бронзовым оттенком */
        }

        /* Глассморфизм - Темный (Матовый черный камень с золотым отблеском) */
        .dark .glass-panel {
            background: rgba(20, 20, 20, 0.6);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border: 1px solid rgba(212, 175, 55, 0.12); /* Едва заметный золотой кант */
            box-shadow: 0 8px 32px -5px rgba(0, 0, 0, 0.8);
        }

        /* Инпуты */
        .glass-input {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(236, 208, 194, 0.6); /* Нюдовая граница */
            color: #3a2e26;
            box-shadow: inset 0 2px 5px 0 rgba(127, 96, 62, 0.03);
            transition: all 0.3s ease;
        }
        
        .dark .glass-input {
            background: rgba(10, 10, 10, 0.6);
            border: 1px solid rgba(212, 175, 55, 0.2); /* Золотая граница */
            color: #f1f0ea;
            box-shadow: inset 0 2px 8px 0 rgba(0, 0, 0, 0.5);
        }

        .glass-input:focus {
            outline: none;
            background: rgba(255, 255, 255, 0.95);
            border-color: #7f603e; /* Бронза при фокусе */
            box-shadow: 0 0 0 3px rgba(127, 96, 62, 0.2);
        }

        .dark .glass-input:focus {
            background: rgba(20, 20, 20, 0.9);
            border-color: #d4af37; /* Золото при фокусе */
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }

        /* Навигация */
        .glass-nav {
            background: rgba(253, 251, 249, 0.85);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border-top: 1px solid rgba(236, 208, 194, 0.4);
        }

        .dark .glass-nav {
            background: rgba(10, 10, 10, 0.85);
            border-top: 1px solid rgba(212, 175, 55, 0.1);
        }

        /* Автодополнение */
        .autocomplete-dropdown {
            position: absolute;
            top: 100%; left: 0; right: 0; z-index: 50; max-height: 200px; overflow-y: auto;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(236, 208, 194, 0.8);
            border-radius: 0.75rem; margin-top: 4px;
            box-shadow: 0 10px 25px rgba(127, 96, 62, 0.1);
        }

        .dark .autocomplete-dropdown {
            background: rgba(20, 20, 20, 0.98);
            border: 1px solid rgba(212, 175, 55, 0.2);
            box-shadow: 0 10px 25px rgba(0,0,0,0.8);
        }

        .autocomplete-item { padding: 12px 16px; cursor: pointer; border-bottom: 1px solid rgba(127,96,62,0.05); color: #3a2e26; }
        .dark .autocomplete-item { border-bottom: 1px solid rgba(212,175,55,0.1); color: #f1f0ea; }
        .autocomplete-item:last-child { border-bottom: none; }
        .autocomplete-item:hover { background: rgba(236, 208, 194, 0.2); }
        .dark .autocomplete-item:hover { background: rgba(212, 175, 55, 0.1); }

        ::-webkit-scrollbar { width: 0px; background: transparent; }

        .modal-enter { animation: modalFadeIn 0.3s cubic-bezier(0.16, 1, 0.3, 1) forwards; }
        @keyframes modalFadeIn {
            from { opacity: 0; transform: translateY(20px) scale(0.95); }
            to { opacity: 1; transform: translateY(0) scale(1); }
        }
        .pb-safe { padding-bottom: env(safe-area-inset-bottom, 20px); }

        .auth-screen {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
        }
    </style>
</head>

<body class="antialiased min-h-screen relative pb-24 text-stone-800 dark:text-stone-100 transition-colors duration-300">

    <div class="blob blob-1"></div>
    <div class="blob blob-2"></div>
    <div class="blob blob-3"></div>

    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect, useMemo, useCallback } = React;

        const firebaseConfig = {
            apiKey: "AIzaSyDoHGxQFGFjUyAqFYAwapN3Bal9c6u-4vM",
            authDomain: "ts-nails.firebaseapp.com",
            projectId: "ts-nails",
            storageBucket: "ts-nails.firebasestorage.app",
            messagingSenderId: "704843662677",
            appId: "1:704843662677:web:f779b63044b34dbd3a9bdc",
            measurementId: "G-QXT4JNX4NV"
        };

        if (!firebase.apps.length) {
            firebase.initializeApp(firebaseConfig);
        }
        const auth = firebase.auth();
        const db = firebase.firestore();
        const googleProvider = new firebase.auth.GoogleAuthProvider();

        const Icons = {
            Calendar: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>,
            Users: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M23 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>,
            Plus: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>,
            Sparkles: () => <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"></path></svg>,
            Phone: () => <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path></svg>,
            Trash: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ef4444" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="3 6 5 6 21 6"></polyline><path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2"></path></svg>,
            Close: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg>,
            Search: () => <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>,
            XCircle: () => <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="10"></circle><line x1="15" y1="9" x2="9" y2="15"></line><line x1="9" y1="9" x2="15" y2="15"></line></svg>,
            Edit: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path><path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path></svg>,
            Sun: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="5"></circle><line x1="12" y1="1" x2="12" y2="3"></line><line x1="12" y1="21" x2="12" y2="23"></line><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line><line x1="1" y1="12" x2="3" y2="12"></line><line x1="21" y1="12" x2="23" y2="12"></line><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line></svg>,
            Moon: () => <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>,
            SunMoon: () => (
                <span
                    className="inline-block w-6 h-6 bg-current"
                    style={{
                        WebkitMaskImage: 'url(https://static.thenounproject.com/png/sun-and-moon-icon-5326330-512.png)',
                        maskImage: 'url(https://static.thenounproject.com/png/sun-and-moon-icon-5326330-512.png)',
                        WebkitMaskSize: 'contain',
                        maskSize: 'contain',
                        WebkitMaskRepeat: 'no-repeat',
                        maskRepeat: 'no-repeat',
                        WebkitMaskPosition: 'center',
                        maskPosition: 'center',
                    }}
                    aria-hidden="true"
                />
            ),
            Chart: () => <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><line x1="12" y1="20" x2="12" y2="10"></line><line x1="18" y1="20" x2="18" y2="4"></line><line x1="6" y1="20" x2="6" y2="16"></line></svg>,
            LogOut: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4"></path><polyline points="16 17 21 12 16 7"></polyline><line x1="21" y1="12" x2="9" y2="12"></line></svg>,
            Google: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/><path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/><path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/><path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/></svg>,
            WhatsApp: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.435 9.884-9.884 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>,
            Check: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.5" strokeLinecap="round" strokeLinejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>,
            Undo: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><polyline points="1 4 1 10 7 10"></polyline><path d="M3.51 15a9 9 0 1 0 2.13-9.36L1 10"></path></svg>,
            ContactImport: () => <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><line x1="19" y1="8" x2="19" y2="14"></line><line x1="22" y1="11" x2="16" y2="11"></line></svg>,
            Note: () => <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line></svg>
        };

        const openWhatsApp = (phone) => {
            const digits = (phone || '').replace(/\D/g, '');
            if (!digits) return;
            window.open(`https://wa.me/${digits}`, '_blank', 'noopener');
        };

        const isNote = (record) => record.type === 'note';

        const SERVICE_PRESETS = [
            { name: 'Коррекция(короткие)', price: 6000 },
            { name: 'Коррекция(длинные)', price: 7000 },
            { name: 'Снятие', price: 2000 },
            { name: 'Наращивание 8', price: 8000 },
            { name: 'Наращивание 9', price: 9000 },
            { name: 'Наращивание 10', price: 10000 },
            { name: 'Стразы', price: 1000 },
            { name: 'Ремонт', price: 1000 },
        ];

        const PRESET_NAMES = SERVICE_PRESETS.map(p => p.name);

        const parseService = (service) => {
            const parts = (service || '').split(' + ').map(s => s.trim()).filter(Boolean);
            const presets = [];
            const custom = [];
            parts.forEach(p => {
                if (PRESET_NAMES.includes(p)) presets.push(p);
                else custom.push(p);
            });
            return { presets, custom: custom.join(' + ') };
        };

        const buildService = (presets, custom) => {
            const orderedPresets = PRESET_NAMES.filter(p => presets.includes(p));
            const parts = [...orderedPresets];
            if (custom && custom.trim()) parts.push(custom.trim());
            return parts.join(' + ');
        };

        const calcPriceFromPresets = (presetNames) => {
            return SERVICE_PRESETS
                .filter(p => presetNames.includes(p.name))
                .reduce((sum, p) => sum + p.price, 0);
        };

        const recordsRef = () => db.collection('records');
        const clientsRef = () => db.collection('clients');
        const userProfileRef = (uid) => db.collection('userProfiles').doc(uid);
        const bookingWindowRef = () => db.collection('settings').doc('bookingWindow');
        const bookedSlotsRef = () => db.collection('bookedSlots');
        const phoneLookupRef = (phone) => {
            const digits = normalizePhone(phone).replace(/\D/g, '');
            return db.collection('phoneLookup').doc(digits);
        };
        const legacyUserRecordsRef = (uid) => db.collection('users').doc(uid).collection('records');
        const legacyUserClientsRef = (uid) => db.collection('users').doc(uid).collection('clients');

        const DEFAULT_SLOTS = ['09:00', '14:00', '16:30'];
        const DEFAULT_ENABLED = ['09:00', '14:00'];

        const checkIsAdmin = async (email) => {
            if (!email) return false;
            const doc = await db.collection('allowedUsers').doc(email).get();
            return doc.exists && doc.data().active !== false;
        };

        const normalizePhone = (phone) => {
            let d = (phone || '').replace(/\D/g, '');
            if (d.length === 11 && d.startsWith('8')) d = '7' + d.slice(1);
            if (d.length === 10) d = '7' + d;
            return d ? '+' + d : '';
        };

        const slotKey = (date, time) => date + '_' + (time || '').replace(':', '-');

        const getClientAdminName = (client) => client.adminName || client.name || '';

        const getGreeting = () => {
            const h = new Date().getHours();
            if (h >= 5 && h < 12) return 'Доброе утро';
            if (h >= 12 && h < 18) return 'Добрый день';
            return 'Добрый вечер';
        };

        const getDaysInRange = (startDate, endDate, excludedDates) => {
            if (!startDate || !endDate) return [];
            const excluded = excludedDates || [];
            const days = [];
            const d = new Date(startDate + 'T12:00:00');
            const end = new Date(endDate + 'T12:00:00');
            while (d <= end) {
                const str = d.toISOString().split('T')[0];
                if (!excluded.includes(str)) days.push(str);
                d.setDate(d.getDate() + 1);
            }
            return days;
        };

        const useClickOutside = (ref, isActive, onClose) => {
            useEffect(() => {
                if (!isActive) return;
                const handler = (e) => {
                    if (ref.current && !ref.current.contains(e.target)) onClose();
                };
                const t = setTimeout(() => {
                    document.addEventListener('mousedown', handler);
                    document.addEventListener('touchstart', handler);
                }, 0);
                return () => {
                    clearTimeout(t);
                    document.removeEventListener('mousedown', handler);
                    document.removeEventListener('touchstart', handler);
                };
            }, [isActive, onClose]);
        };

        const syncBookedSlot = async (recordId, date, time, bookedByUid) => {
            if (!date || !time) return;
            await bookedSlotsRef().doc(slotKey(date, time)).set({ date, time, recordId, bookedByUid: bookedByUid || null });
        };

        const removeBookedSlot = async (date, time) => {
            if (!date || !time) return;
            await bookedSlotsRef().doc(slotKey(date, time)).delete().catch(() => {});
        };

        const LoginScreen = ({ onSignIn, error, loading }) => (
            <div className="auth-screen">
                <div className="glass-panel w-full max-w-sm rounded-3xl p-8 text-center shadow-2xl">
                    <h1 className="text-2xl font-extrabold text-stone-800 dark:text-stone-100 mb-2">TS Nails</h1>
                    <p className="text-stone-500 dark:text-stone-400 text-sm mb-8">Записи клиентов на маникюр</p>
                    {error && (
                        <div className="mb-4 px-4 py-3 rounded-xl bg-red-50 dark:bg-red-900/20 text-red-600 dark:text-red-400 text-sm border border-red-100 dark:border-red-900/30">
                            {error}
                        </div>
                    )}
                    <button
                        onClick={onSignIn}
                        disabled={loading}
                        className="w-full flex items-center justify-center gap-3 bg-white dark:bg-stonepanel border border-nude/60 dark:border-gold/20 rounded-xl py-3.5 px-4 font-semibold text-stone-700 dark:text-stone-200 shadow-sm hover:bg-stone-50 dark:hover:bg-white/5 transition-colors disabled:opacity-60"
                    >
                        <Icons.Google />
                        {loading ? 'Вход...' : 'Войти через Google'}
                    </button>
                </div>
            </div>
        );

        const formatMonthYear = (yearMonth) => {
            const [year, month] = yearMonth.split('-');
            const date = new Date(Number(year), Number(month) - 1, 1);
            return date.toLocaleDateString('ru-RU', { month: 'long', year: 'numeric' });
        };

        const formatYear = (year) => `${year} год`;

        const getDaysWord = (number) => {
            const lastDigit = number % 10;
            const lastTwoDigits = number % 100;
            if (lastTwoDigits >= 11 && lastTwoDigits <= 19) return 'дней';
            if (lastDigit === 1) return 'день';
            if (lastDigit >= 2 && lastDigit <= 4) return 'дня';
            return 'дней';
        };

        const formatDate = (dateString) => {
            if (!dateString) return '';
            const options = { month: 'long', day: 'numeric', weekday: 'short' };
            const date = new Date(dateString);
            return date.toLocaleDateString('ru-RU', options);
        };

        const todayString = new Date().toISOString().split('T')[0];

        const isBookingWindowActive = (window) => {
            if (!window || !window.isOpen) return false;
            if (window.endDate && window.endDate < todayString) return false;
            return true;
        };

        const getTimeBasedTheme = () => {
            const hour = new Date().getHours();
            return (hour >= 20 || hour < 7) ? 'dark' : 'light';
        };

        const cycleThemeMode = (current) => {
            if (current === 'auto') return 'light';
            if (current === 'light') return 'dark';
            return 'auto';
        };

        const getThemeTitle = (mode, effective) => {
            if (mode === 'auto') return `Авто · сейчас ${effective === 'dark' ? 'тёмная' : 'светлая'}`;
            return mode === 'dark' ? 'Тёмная тема' : 'Светлая тема';
        };

        const ThemeToggleButton = ({ themeMode, effectiveTheme, onToggle, className }) => (
            <button
                onClick={onToggle}
                className={className}
                title={getThemeTitle(themeMode, effectiveTheme)}
            >
                {themeMode === 'auto' ? <Icons.SunMoon /> : themeMode === 'light' ? <Icons.Sun /> : <Icons.Moon />}
            </button>
        );

        const ConfirmDialog = ({ isOpen, title, message, confirmLabel, cancelLabel, onConfirm, onCancel, danger }) => {
            if (!isOpen) return null;
            return (
                <div className="fixed inset-0 z-[60] flex items-center justify-center p-4 bg-stone-900/50 dark:bg-black/75 backdrop-blur-sm" onClick={onCancel}>
                    <div className="glass-panel w-full max-w-sm rounded-3xl shadow-2xl modal-enter overflow-hidden" onClick={e => e.stopPropagation()}>
                        <div className="p-6">
                            <h3 className="text-lg font-bold text-stone-800 dark:text-stone-100 mb-2">{title || 'Подтверждение'}</h3>
                            <p className="text-sm text-stone-600 dark:text-stone-300 leading-relaxed">{message}</p>
                        </div>
                        <div className="flex gap-3 p-4 pt-0">
                            <button
                                type="button"
                                onClick={onCancel}
                                className="flex-1 py-3 rounded-xl border border-nude/60 dark:border-gold/20 text-stone-600 dark:text-stone-300 font-medium hover:bg-white/60 dark:hover:bg-white/5 transition-colors"
                            >
                                {cancelLabel || 'Отмена'}
                            </button>
                            <button
                                type="button"
                                onClick={onConfirm}
                                className={`flex-1 py-3 rounded-xl font-semibold text-white transition-colors ${danger ? 'bg-red-500 hover:bg-red-600 dark:bg-red-600 dark:hover:bg-red-500' : 'bg-bronze hover:bg-bronzedark dark:bg-gradient-to-r dark:from-gold dark:to-golddark dark:text-stone-900'}`}
                            >
                                {confirmLabel || 'Да'}
                            </button>
                        </div>
                    </div>
                </div>
            );
        };

        const AlertDialog = ({ isOpen, title, message, buttonLabel, onClose }) => {
            if (!isOpen) return null;
            return (
                <div className="fixed inset-0 z-[60] flex items-center justify-center p-4 bg-stone-900/50 dark:bg-black/75 backdrop-blur-sm" onClick={onClose}>
                    <div className="glass-panel w-full max-w-sm rounded-3xl shadow-2xl modal-enter overflow-hidden" onClick={e => e.stopPropagation()}>
                        <div className="p-6">
                            <h3 className="text-lg font-bold text-stone-800 dark:text-stone-100 mb-2">{title || 'Внимание'}</h3>
                            <p className="text-sm text-stone-600 dark:text-stone-300 leading-relaxed">{message}</p>
                        </div>
                        <div className="p-4 pt-0">
                            <button
                                type="button"
                                onClick={onClose}
                                className="w-full py-3 rounded-xl bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-semibold"
                            >
                                {buttonLabel || 'OK'}
                            </button>
                        </div>
                    </div>
                </div>
            );
        };

        const RecordCard = ({ record, isArchiveView, onEdit, onDelete, onArchive, onRestore, onAcknowledge }) => {
            const [showActions, setShowActions] = useState(false);
            const cardRef = React.useRef(null);
            const note = isNote(record);
            const isNewSelf = record.isSelfBooked && record.isNewFromClient;

            useClickOutside(cardRef, showActions, () => setShowActions(false));

            const handleCardClick = () => {
                if (isNewSelf && onAcknowledge) {
                    onAcknowledge(record.id);
                    return;
                }
                setShowActions(!showActions);
            };

            const stripeClass = isNewSelf
                ? 'bg-gradient-to-b from-emerald-400 to-emerald-600 dark:from-emerald-500 dark:to-emerald-700'
                : note
                    ? 'bg-gradient-to-b from-violet-300 to-violet-500 dark:from-violet-400 dark:to-violet-600'
                    : 'bg-gradient-to-b from-nude to-bronze dark:from-gold dark:to-golddark';

            return (
                <div 
                    ref={cardRef}
                    className="glass-panel rounded-2xl p-4 mb-4 relative overflow-hidden transition-all cursor-pointer select-none" 
                    onClick={handleCardClick}
                >
                    <div className={`absolute left-0 top-0 bottom-0 w-1.5 opacity-90 ${stripeClass}`}></div>
                    
                    {note ? (
                        <div className="ml-2">
                            <div className="flex justify-between items-start">
                                <div className="flex items-center gap-2 text-violet-600 dark:text-violet-300 text-sm font-medium">
                                    <Icons.Note /> Заметка
                                </div>
                                <div className="inline-block bg-white/80 dark:bg-stonepanel backdrop-blur-sm rounded-lg px-3 py-1 font-semibold text-violet-600 dark:text-violet-300 shadow-sm border border-violet-200/60 dark:border-violet-500/20">
                                    {record.time}
                                </div>
                            </div>
                            <p className="mt-3 text-stone-700 dark:text-stone-200 text-sm whitespace-pre-wrap">{record.noteText}</p>
                        </div>
                    ) : (
                        <React.Fragment>
                            <div className="flex justify-between items-start ml-2">
                                <div className="flex-1 min-w-0 pr-2">
                                    <h3 className="text-lg font-bold text-stone-800 dark:text-stone-100 flex items-center gap-1.5">
                                        {record.isSelfBooked && (
                                            <span className="inline-flex items-center justify-center w-5 h-5 rounded-full bg-green-100 dark:bg-green-900/40 text-green-600 dark:text-green-400 text-[10px] font-bold shrink-0" title="Запись клиента">К</span>
                                        )}
                                        <span className="truncate">{record.clientName}</span>
                                    </h3>
                                    {record.phone && (
                                        <div className="flex items-center text-stone-500 dark:text-stone-400 text-sm mt-1">
                                            <span className="text-bronze dark:text-gold mr-1.5"><Icons.Phone /></span>
                                            {record.phone}
                                        </div>
                                    )}
                                </div>
                                <div className="text-right shrink-0">
                                    <div className="inline-block bg-white/80 dark:bg-stonepanel backdrop-blur-sm rounded-lg px-3 py-1 font-semibold text-bronze dark:text-gold shadow-sm border border-nude/60 dark:border-gold/20">
                                        {record.time}
                                    </div>
                                </div>
                            </div>
                            <div className="mt-4 ml-2 pt-3 border-t border-stone-200/60 dark:border-stone-700/50 flex justify-between items-center">
                                <div className="flex items-center text-stone-600 dark:text-stone-300 font-medium text-sm min-w-0">
                                    <span className="text-bronze dark:text-gold mr-2 shrink-0"><Icons.Sparkles /></span>
                                    <span className="truncate">{record.service}</span>
                                </div>
                                <div className="font-bold text-stone-800 dark:text-stone-100 shrink-0 ml-2">
                                    {record.price ? `${record.price} ₸` : ''}
                                </div>
                            </div>
                        </React.Fragment>
                    )}

                    {showActions && (
                        <div className="absolute inset-y-0 right-0 flex items-center space-x-2 bg-white/98 dark:bg-stonebg/98 backdrop-blur-md px-4 pl-5 rounded-r-2xl border-l border-nude/40 dark:border-gold/20 shadow-[-15px_0_20px_rgba(255,255,255,0.9)] dark:shadow-[-15px_0_20px_rgba(10,10,10,0.9)] z-10" onClick={(e) => e.stopPropagation()}>
                            {!note && record.phone && (
                                <button onClick={(e) => { e.stopPropagation(); openWhatsApp(record.phone); setShowActions(false); }} className="p-3 bg-green-50 dark:bg-green-900/20 rounded-full hover:bg-green-100 dark:hover:bg-green-900/40 text-green-600 dark:text-green-400 transition-colors shadow-sm border border-green-100 dark:border-green-900/30" title="WhatsApp">
                                    <Icons.WhatsApp />
                                </button>
                            )}
                            {isArchiveView ? (
                                <button onClick={(e) => { e.stopPropagation(); onRestore(record.id); setShowActions(false); }} className="p-3 bg-nude/30 dark:bg-gold/10 rounded-full hover:bg-nude/50 dark:hover:bg-gold/20 text-bronze dark:text-gold transition-colors shadow-sm border border-nude/60 dark:border-gold/20" title="Вернуть из архива">
                                    <Icons.Undo />
                                </button>
                            ) : (
                                <button onClick={(e) => { e.stopPropagation(); onArchive(record.id); setShowActions(false); }} className="p-3 bg-emerald-50 dark:bg-emerald-900/20 rounded-full hover:bg-emerald-100 dark:hover:bg-emerald-900/40 text-emerald-600 dark:text-emerald-400 transition-colors shadow-sm border border-emerald-100 dark:border-emerald-900/30" title="В архив">
                                    <Icons.Check />
                                </button>
                            )}
                            <button onClick={(e) => { e.stopPropagation(); onEdit(record); setShowActions(false); }} className="p-3 bg-stone-100 dark:bg-stonepanel rounded-full hover:bg-stone-200 dark:hover:bg-white/10 text-stone-600 dark:text-stone-200 transition-colors shadow-sm border border-stone-200 dark:border-white/5" title="Редактировать">
                                <Icons.Edit />
                            </button>
                            <button onClick={(e) => { e.stopPropagation(); onDelete(record.id); setShowActions(false); }} className="p-3 bg-red-50 dark:bg-red-900/20 rounded-full hover:bg-red-100 dark:hover:bg-red-900/40 text-red-500 dark:text-red-400 transition-colors shadow-sm border border-red-100 dark:border-red-900/30" title="Удалить">
                                <Icons.Trash />
                            </button>
                        </div>
                    )}
                </div>
            );
        };

        const EditClientModal = ({ client, isOpen, onClose, onSave, onDelete, confirm }) => {
            const [formData, setFormData] = useState({ id: '', adminName: '', phone: '', isInactive: false });

            useEffect(() => {
                if (isOpen && client) {
                    setFormData({
                        ...client,
                        adminName: getClientAdminName(client)
                    });
                }
            }, [isOpen, client]);

            if (!isOpen || !client) return null;
            const isNew = !client.id;

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm transition-opacity">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden relative">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 bg-white/50 dark:bg-stonepanel/50">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">{isNew ? 'Новый клиент' : 'Профиль клиента'}</h2>
                            <button onClick={onClose} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 transition-colors text-stone-600 dark:text-stone-300">
                                <Icons.Close />
                            </button>
                        </div>
                        <form onSubmit={(e) => { e.preventDefault(); onSave(formData); }} className="p-5 space-y-4">
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Имя *</label>
                                <input required type="text" value={formData.adminName} onChange={e => setFormData({...formData, adminName: e.target.value})} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Телефон</label>
                                <input type="tel" value={formData.phone} onChange={e => setFormData({...formData, phone: e.target.value})} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            {!isNew && (
                                <React.Fragment>
                                    <button
                                        type="button"
                                        onClick={async () => {
                                            if (await confirm('Удалить клиента навсегда?', { title: 'Удаление клиента', confirmLabel: 'Удалить', danger: true })) {
                                                onDelete(formData.id);
                                            }
                                        }}
                                        className="w-full py-3 px-4 rounded-xl border border-red-200 dark:border-red-900/40 text-red-600 dark:text-red-400 font-medium hover:bg-red-50 dark:hover:bg-red-900/20 transition-colors"
                                    >
                                        Удалить клиента
                                    </button>
                                    <div className="flex items-center bg-white/50 dark:bg-stonepanel p-3 rounded-xl border border-nude/50 dark:border-gold/10">
                                        <input type="checkbox" id="inactive" checked={formData.isInactive} onChange={e => setFormData({...formData, isInactive: e.target.checked})} className="mr-3 w-5 h-5 rounded border-stone-300 dark:border-stone-600 bg-white dark:bg-stonebg accent-bronze dark:accent-gold" />
                                        <label htmlFor="inactive" className="text-stone-700 dark:text-stone-300 text-sm">Неактуальный клиент (в архив)</label>
                                    </div>
                                </React.Fragment>
                            )}
                            <div className="pt-4">
                                <button type="submit" className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3.5 px-4 rounded-xl shadow-lg shadow-bronze/20 dark:shadow-gold/10 transform transition active:scale-95">
                                    {isNew ? 'Добавить клиента' : 'Сохранить изменения'}
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            );
        };

        const AddModal = ({ initialData, clients, isOpen, onClose, onSave, bookingWindow, bookedSlots }) => {
            const [entryType, setEntryType] = useState('appointment');
            const [customTime, setCustomTime] = useState(false);
            const [formData, setFormData] = useState({
                type: 'appointment', clientName: '', phone: '', date: todayString, time: '10:00', service: '', price: '', noteText: '', archived: false, customTime: false
            });
            const [selectedPresets, setSelectedPresets] = useState([]);
            const [customService, setCustomService] = useState('');
            const [showSuggestions, setShowSuggestions] = useState(false);

            useEffect(() => {
                if (isOpen) {
                    if (initialData) {
                        const ct = !!initialData.customTime;
                        setCustomTime(ct);
                        setFormData({ type: 'appointment', archived: false, customTime: ct, ...initialData });
                        if (isNote(initialData)) {
                            setEntryType('note');
                        } else {
                            setEntryType('appointment');
                            const parsed = parseService(initialData.service);
                            setSelectedPresets(parsed.presets);
                            setCustomService(parsed.custom);
                        }
                    } else {
                        setEntryType('appointment');
                        setCustomTime(false);
                        const firstDay = isBookingWindowActive(bookingWindow)
                            ? getDaysInRange(bookingWindow.startDate, bookingWindow.endDate, bookingWindow.excludedDates).find(d => d >= todayString)
                            : todayString;
                        const firstTime = (bookingWindow && bookingWindow.enabledSlots && bookingWindow.enabledSlots[0]) || '09:00';
                        setFormData({ type: 'appointment', clientName: '', phone: '', date: firstDay || todayString, time: firstTime, service: '', price: '', noteText: '', archived: false, customTime: false });
                        setSelectedPresets([]);
                        setCustomService('');
                    }
                    setShowSuggestions(false);
                }
            }, [isOpen, initialData, bookingWindow]);

            const takenSet = useMemo(() => new Set((bookedSlots || []).map(s => slotKey(s.date, s.time))), [bookedSlots]);

            const windowDays = useMemo(() => {
                if (!isBookingWindowActive(bookingWindow)) return [];
                return getDaysInRange(bookingWindow.startDate, bookingWindow.endDate, bookingWindow.excludedDates)
                    .filter(d => d >= todayString);
            }, [bookingWindow]);

            const availableTimesForDate = (date) => {
                if (!isBookingWindowActive(bookingWindow) || !date) return [];
                const editingKey = initialData && initialData.date === date && initialData.time ? slotKey(date, initialData.time) : null;
                return (bookingWindow.enabledSlots || []).filter(t => {
                    const key = slotKey(date, t);
                    return key === editingKey || !takenSet.has(key);
                });
            };

            const updateService = (presets, custom) => {
                const service = buildService(presets, custom);
                const price = calcPriceFromPresets(presets);
                setSelectedPresets(presets);
                setCustomService(custom);
                setFormData(prev => ({ ...prev, service, price: price ? String(price) : prev.price }));
            };

            const togglePreset = (presetName) => {
                const next = selectedPresets.includes(presetName)
                    ? selectedPresets.filter(p => p !== presetName)
                    : [...selectedPresets, presetName];
                updateService(next, customService);
            };

            const handleServiceInput = (value) => {
                const parsed = parseService(value);
                const price = calcPriceFromPresets(parsed.presets);
                setSelectedPresets(parsed.presets);
                setCustomService(parsed.custom);
                setFormData(prev => ({ ...prev, service: value, price: price ? String(price) : prev.price }));
            };

            if (!isOpen) return null;

            const filteredClients = clients.filter(c => 
                !c.isInactive && 
                getClientAdminName(c).toLowerCase().includes((formData.clientName || '').toLowerCase())
            );

            const handleChange = (e) => {
                const { name, value } = e.target;
                setFormData(prev => ({ ...prev, [name]: value }));
            };

            const handleSubmit = (e) => {
                e.preventDefault();
                if (entryType === 'note') {
                    onSave({ ...formData, type: 'note', archived: formData.archived || false });
                } else {
                    onSave({ ...formData, type: 'appointment', archived: formData.archived || false, customTime });
                }
            };

            const isEditing = !!initialData;
            const title = isEditing
                ? (entryType === 'note' ? 'Редактировать заметку' : 'Редактировать запись')
                : (entryType === 'note' ? 'Новая заметка' : 'Новая запись');

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm transition-opacity">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden relative max-h-[90vh] flex flex-col">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 bg-white/50 dark:bg-stonepanel/50 shrink-0">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">{title}</h2>
                            <button onClick={onClose} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 transition-colors text-stone-600 dark:text-stone-300">
                                <Icons.Close />
                            </button>
                        </div>

                        <form onSubmit={handleSubmit} className="p-5 space-y-4 overflow-y-auto">
                            {!isEditing && (
                                <div className="flex bg-nude/20 dark:bg-stonepanel p-1 rounded-xl border border-nude/40 dark:border-gold/10">
                                    <button type="button" onClick={() => setEntryType('appointment')} className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${entryType === 'appointment' ? 'bg-white shadow-sm text-bronze dark:bg-gold/10 dark:text-gold dark:shadow-none dark:border dark:border-gold/20' : 'text-stone-500 dark:text-stone-400'}`}>
                                        Запись клиента
                                    </button>
                                    <button type="button" onClick={() => setEntryType('note')} className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${entryType === 'note' ? 'bg-white shadow-sm text-violet-600 dark:bg-violet-900/30 dark:text-violet-300 dark:shadow-none dark:border dark:border-violet-500/20' : 'text-stone-500 dark:text-stone-400'}`}>
                                        Заметка
                                    </button>
                                </div>
                            )}

                            {entryType === 'note' ? (
                                <React.Fragment>
                                    <div className="grid grid-cols-2 gap-4">
                                        <div>
                                            <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Дата *</label>
                                            <input required type="date" name="date" value={formData.date} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                                        </div>
                                        <div>
                                            <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Время *</label>
                                            <input required type="time" name="time" value={formData.time} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                                        </div>
                                    </div>
                                    <div>
                                        <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Текст заметки *</label>
                                        <textarea required name="noteText" value={formData.noteText || ''} onChange={handleChange} rows={4} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500 resize-none" placeholder="Напоминание..." />
                                    </div>
                                </React.Fragment>
                            ) : (
                                <React.Fragment>
                            <div className="relative">
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Имя клиента *</label>
                                <input 
                                    required 
                                    type="text" 
                                    name="clientName" 
                                    value={formData.clientName} 
                                    autoComplete="off"
                                    onFocus={() => setShowSuggestions(true)}
                                    onBlur={() => setTimeout(() => setShowSuggestions(false), 200)}
                                    onChange={(e) => { handleChange(e); setShowSuggestions(true); }} 
                                    className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" 
                                    placeholder="Например: Катя" 
                                />
                                {showSuggestions && filteredClients.length > 0 && formData.clientName && (
                                    <div className="autocomplete-dropdown">
                                        {filteredClients.map(c => (
                                            <div key={c.id} className="autocomplete-item" onClick={() => {
                                                setFormData({...formData, clientName: getClientAdminName(c), phone: c.phone || formData.phone});
                                                setShowSuggestions(false);
                                            }}>
                                                <div className="font-medium">{getClientAdminName(c)}</div>
                                                {c.phone && <div className="text-xs text-stone-500 dark:text-stone-400">{c.phone}</div>}
                                            </div>
                                        ))}
                                    </div>
                                )}
                            </div>

                            {isBookingWindowActive(bookingWindow) && (
                                <label className="flex items-center gap-2 bg-white/50 dark:bg-stonepanel p-3 rounded-xl border border-nude/50 dark:border-gold/10 cursor-pointer">
                                    <input type="checkbox" checked={customTime} onChange={e => setCustomTime(e.target.checked)} className="w-5 h-5 accent-bronze dark:accent-gold" />
                                    <span className="text-sm text-stone-700 dark:text-stone-300">Нестандартное время</span>
                                </label>
                            )}

                            {customTime || !isBookingWindowActive(bookingWindow) ? (
                            <div className="grid grid-cols-2 gap-4">
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Дата *</label>
                                    <input required type="date" name="date" value={formData.date} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                                </div>
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Время *</label>
                                    <input required type="time" name="time" value={formData.time} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                                </div>
                            </div>
                            ) : (
                            <React.Fragment>
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Дата *</label>
                                    <select required value={formData.date} onChange={e => {
                                        const date = e.target.value;
                                        const times = availableTimesForDate(date);
                                        setFormData(prev => ({ ...prev, date, time: times[0] || prev.time }));
                                    }} className="glass-input w-full px-4 py-3 rounded-xl">
                                        {windowDays.map(d => (
                                            <option key={d} value={d}>{formatDate(d)}</option>
                                        ))}
                                    </select>
                                </div>
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Время *</label>
                                    <div className="flex flex-wrap gap-2">
                                        {availableTimesForDate(formData.date).map(time => (
                                            <button key={time} type="button" onClick={() => setFormData(prev => ({ ...prev, time }))} className={`px-4 py-2 rounded-xl text-sm border ${formData.time === time ? 'bg-bronze text-white border-bronze dark:bg-gold/20 dark:text-gold dark:border-gold/40' : 'bg-white/70 border-nude/60 dark:bg-stonepanel dark:border-gold/10'}`}>
                                                {time}
                                            </button>
                                        ))}
                                    </div>
                                </div>
                            </React.Fragment>
                            )}

                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Услуга</label>
                                <input type="text" name="service" value={formData.service || ''} onChange={(e) => handleServiceInput(e.target.value)} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="Услуги..." />
                                <div className="flex flex-wrap gap-2 mt-2.5">
                                    {SERVICE_PRESETS.map(preset => (
                                        <button
                                            key={preset.name}
                                            type="button"
                                            onClick={() => togglePreset(preset.name)}
                                            className={`px-3 py-1.5 rounded-full text-xs font-medium transition-all border ${
                                                selectedPresets.includes(preset.name)
                                                    ? 'bg-bronze text-white border-bronze dark:bg-gold/20 dark:text-gold dark:border-gold/40'
                                                    : 'bg-white/70 text-stone-600 border-nude/60 hover:border-bronze/40 dark:bg-stonepanel dark:text-stone-300 dark:border-gold/10 dark:hover:border-gold/30'
                                            }`}
                                        >
                                            {preset.name}
                                        </button>
                                    ))}
                                </div>
                            </div>

                            <div className="grid grid-cols-2 gap-4">
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Стоимость (₸)</label>
                                    <input type="text" name="price" value={formData.price || ''} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="6000" />
                                </div>
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Телефон</label>
                                    <input type="tel" name="phone" value={formData.phone || ''} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="+7..." />
                                </div>
                            </div>
                                </React.Fragment>
                            )}

                            <div className="pt-4">
                                <button type="submit" className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3.5 px-4 rounded-xl shadow-lg shadow-bronze/20 dark:shadow-gold/10 transform transition active:scale-95">
                                    {isEditing ? 'Сохранить изменения' : (entryType === 'note' ? 'Добавить заметку' : 'Добавить запись')}
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            );
        };

        const ContactImportModal = ({ isOpen, onClose, onImport, existingClients }) => {
            const [contacts, setContacts] = useState([]);
            const [selected, setSelected] = useState({});
            const [loading, setLoading] = useState(false);
            const [error, setError] = useState('');

            useEffect(() => {
                if (!isOpen) {
                    setContacts([]);
                    setSelected({});
                    setError('');
                    return;
                }
                pickContacts();
            }, [isOpen]);

            const pickContacts = async () => {
                setLoading(true);
                setError('');
                try {
                    if (!('contacts' in navigator && 'ContactsManager' in window)) {
                        setError('Импорт контактов доступен в Chrome на Android. На iPhone добавьте клиентов вручную.');
                        setLoading(false);
                        return;
                    }
                    const picked = await navigator.contacts.select(['name', 'tel'], { multiple: true });
                    const normalized = picked.map((c, i) => ({
                        id: `c-${i}`,
                        name: (c.name && c.name[0]) || 'Без имени',
                        phone: (c.tel && c.tel[0]) || ''
                    })).filter(c => c.name);
                    const existingPhones = new Set(existingClients.map(c => (c.phone || '').replace(/\D/g, '')).filter(Boolean));
                    const existingNames = new Set(existingClients.map(c => getClientAdminName(c).toLowerCase()));
                    const fresh = normalized.filter(c => {
                        const phoneKey = c.phone.replace(/\D/g, '');
                        if (phoneKey && existingPhones.has(phoneKey)) return false;
                        if (existingNames.has(c.name.toLowerCase())) return false;
                        return true;
                    });
                    setContacts(fresh);
                    const sel = {};
                    fresh.forEach(c => { sel[c.id] = true; });
                    setSelected(sel);
                    if (!fresh.length) setError('Новых контактов для импорта не найдено.');
                } catch (e) {
                    if (e.name !== 'InvalidStateError') setError('Не удалось получить контакты.');
                } finally {
                    setLoading(false);
                }
            };

            if (!isOpen) return null;

            const toggle = (id) => setSelected(prev => ({ ...prev, [id]: !prev[id] }));
            const selectedCount = contacts.filter(c => selected[c.id]).length;

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden max-h-[85vh] flex flex-col">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 shrink-0">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">Импорт контактов</h2>
                            <button onClick={onClose} className="p-2 rounded-full hover:bg-white/60 dark:hover:bg-white/10"><Icons.Close /></button>
                        </div>
                        <div className="p-5 overflow-y-auto flex-1 space-y-3">
                            {loading && <p className="text-sm text-stone-500 text-center">Загрузка...</p>}
                            {error && <p className="text-sm text-stone-500 dark:text-stone-400 text-center">{error}</p>}
                            {contacts.map(c => (
                                <label key={c.id} className="flex items-center gap-3 p-3 rounded-xl border border-nude/40 dark:border-gold/10 cursor-pointer hover:bg-white/50 dark:hover:bg-white/5">
                                    <input type="checkbox" checked={!!selected[c.id]} onChange={() => toggle(c.id)} className="w-5 h-5 accent-bronze dark:accent-gold" />
                                    <div className="min-w-0">
                                        <div className="font-medium text-stone-800 dark:text-stone-100">{c.name}</div>
                                        {c.phone && <div className="text-sm text-stone-500">{c.phone}</div>}
                                    </div>
                                </label>
                            ))}
                        </div>
                        {contacts.length > 0 && (
                            <div className="p-5 border-t border-nude/40 dark:border-gold/10 shrink-0">
                                <button
                                    onClick={() => onImport(contacts.filter(c => selected[c.id]))}
                                    disabled={!selectedCount}
                                    className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3 rounded-xl disabled:opacity-50"
                                >
                                    Импортировать ({selectedCount})
                                </button>
                            </div>
                        )}
                    </div>
                </div>
            );
        };

        const ProfileSetupScreen = ({ onSave, loading, error }) => {
            const [firstName, setFirstName] = useState('');
            const [lastName, setLastName] = useState('');
            const [phone, setPhone] = useState('');
            const [validationError, setValidationError] = useState('');

            const handleSubmit = (e) => {
                e.preventDefault();
                const normalized = normalizePhone(phone);
                if (!firstName.trim() || !lastName.trim() || normalized.length < 12) {
                    setValidationError('Заполните имя, фамилию и номер телефона в формате +7...');
                    return;
                }
                setValidationError('');
                onSave({ firstName: firstName.trim(), lastName: lastName.trim(), phone: normalized });
            };

            return (
                <div className="auth-screen">
                    <div className="glass-panel w-full max-w-sm rounded-3xl p-8 shadow-2xl">
                        <h1 className="text-xl font-bold text-stone-800 dark:text-stone-100 mb-2">Добро пожаловать!</h1>
                        <p className="text-stone-500 dark:text-stone-400 text-sm mb-6">Заполните данные для записи к мастеру</p>
                        {error && <p className="text-red-500 text-sm mb-4">{error}</p>}
                        {validationError && <p className="text-red-500 text-sm mb-4">{validationError}</p>}
                        <form onSubmit={handleSubmit} className="space-y-4">
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1">Имя *</label>
                                <input required value={firstName} onChange={e => setFirstName(e.target.value)} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1">Фамилия *</label>
                                <input required value={lastName} onChange={e => setLastName(e.target.value)} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1">WhatsApp *</label>
                                <input required type="tel" value={phone} onChange={e => setPhone(e.target.value)} placeholder="+77001234567" className="glass-input w-full px-4 py-3 rounded-xl" />
                                <p className="text-xs text-stone-400 mt-1">Формат: +7 и 10 цифр</p>
                            </div>
                            <button type="submit" disabled={loading} className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3.5 rounded-xl disabled:opacity-60">
                                {loading ? 'Сохранение...' : 'Продолжить'}
                            </button>
                        </form>
                    </div>
                </div>
            );
        };

        const ClientBookingApp = ({ profile, bookingWindow, bookedSlots, myRecords, onBook, onSignOut, themeMode, effectiveTheme, onThemeToggle, confirm }) => {
            const [selectedDate, setSelectedDate] = useState('');
            const [selectedTime, setSelectedTime] = useState('');

            const upcomingBooking = useMemo(() => {
                return myRecords
                    .filter(r => !r.archived && r.type !== 'note' && r.date >= todayString)
                    .sort((a, b) => a.date !== b.date ? a.date.localeCompare(b.date) : a.time.localeCompare(b.time))[0];
            }, [myRecords]);

            const daysSinceVisit = useMemo(() => {
                const past = myRecords.filter(r => r.type !== 'note' && r.date < todayString);
                if (!past.length) return null;
                const last = past.sort((a, b) => b.date.localeCompare(a.date))[0];
                const diff = Math.floor((new Date(todayString) - new Date(last.date)) / (86400000));
                return diff;
            }, [myRecords]);

            const availableDays = useMemo(() => {
                if (!isBookingWindowActive(bookingWindow)) return [];
                return getDaysInRange(bookingWindow.startDate, bookingWindow.endDate, bookingWindow.excludedDates)
                    .filter(d => d >= todayString);
            }, [bookingWindow]);

            const takenSet = useMemo(() => new Set(bookedSlots.map(s => slotKey(s.date, s.time))), [bookedSlots]);

            const slotsForDay = (date) => {
                if (!bookingWindow) return [];
                return (bookingWindow.enabledSlots || []).filter(t => !takenSet.has(slotKey(date, t)));
            };

            const handleBook = async () => {
                if (!selectedDate || !selectedTime) return;
                const ok = await confirm(
                    `Записаться на ${formatDate(selectedDate)} в ${selectedTime}?`,
                    { title: 'Подтверждение записи', confirmLabel: 'Записаться' }
                );
                if (!ok) return;
                onBook(selectedDate, selectedTime);
                setSelectedDate('');
                setSelectedTime('');
            };

            return (
                <div className="max-w-md mx-auto min-h-screen flex flex-col relative pt-8 px-4 pb-28">
                    <div className="flex justify-between items-center mb-6 px-2">
                        <div />
                        <div className="flex gap-2">
                            <ThemeToggleButton themeMode={themeMode} effectiveTheme={effectiveTheme} onToggle={onThemeToggle} className="h-[42px] w-[42px] rounded-xl glass-panel text-bronze dark:text-gold border border-nude/60 dark:border-gold/20 flex items-center justify-center" />
                            <button onClick={onSignOut} className="h-[42px] w-[42px] rounded-xl border flex items-center justify-center bg-white/70 border-nude/60 text-stone-500 dark:bg-stonepanel dark:border-gold/10" title="Выйти"><Icons.LogOut /></button>
                        </div>
                    </div>

                    <div className="px-2 mb-6">
                        <h1 className="text-2xl font-bold text-stone-800 dark:text-stone-100">
                            {getGreeting()}, {profile.firstName} {profile.lastName}!
                        </h1>
                        {daysSinceVisit !== null && (
                            <p className="text-sm text-stone-500 dark:text-stone-400 mt-2">
                                С последнего визита: {daysSinceVisit} {getDaysWord(daysSinceVisit)}
                            </p>
                        )}
                    </div>

                    {upcomingBooking && (
                        <div className="mx-2 mb-6 glass-panel rounded-2xl p-4 border border-bronze/30 dark:border-gold/20">
                            <div className="text-sm font-medium text-bronze dark:text-gold mb-1">Моя запись</div>
                            <div className="font-bold text-stone-800 dark:text-stone-100">{formatDate(upcomingBooking.date)} · {upcomingBooking.time}</div>
                        </div>
                    )}

                    {!isBookingWindowActive(bookingWindow) ? (
                        <div className="text-center py-16 glass-panel rounded-3xl mx-2 text-stone-500">Окно записи пока закрыто</div>
                    ) : upcomingBooking ? (
                        <div className="text-center py-10 px-6 glass-panel rounded-3xl mx-2 text-stone-500 text-sm">У вас уже есть запись. Дождитесь визита или свяжитесь с мастером.</div>
                    ) : (
                        <div className="space-y-6 px-2 flex-1">
                            {availableDays.map(date => {
                                const slots = slotsForDay(date);
                                if (!slots.length) return null;
                                return (
                                    <div key={date}>
                                        <div className="text-sm font-semibold text-stone-700 dark:text-stone-300 mb-2 capitalize">{formatDate(date)}</div>
                                        <div className="flex flex-wrap gap-2">
                                            {slots.map(time => (
                                                <button
                                                    key={time}
                                                    onClick={() => { setSelectedDate(date); setSelectedTime(time); }}
                                                    className={`px-4 py-2.5 rounded-xl text-sm font-medium border transition-all ${selectedDate === date && selectedTime === time ? 'bg-bronze text-white border-bronze dark:bg-gold/20 dark:text-gold dark:border-gold/40' : 'bg-white/70 border-nude/60 text-stone-700 dark:bg-stonepanel dark:border-gold/10 dark:text-stone-200'}`}
                                                >
                                                    {time}
                                                </button>
                                            ))}
                                        </div>
                                    </div>
                                );
                            })}
                        </div>
                    )}

                    {selectedDate && selectedTime && !upcomingBooking && (
                        <div className="fixed bottom-0 left-0 right-0 p-4 glass-nav pb-safe z-40">
                            <div className="max-w-md mx-auto">
                                <button onClick={handleBook} className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-4 rounded-2xl shadow-lg">
                                    Записаться · {selectedTime}
                                </button>
                            </div>
                        </div>
                    )}
                </div>
            );
        };

        const BookingWindowScreen = ({ onBack, onOpen, onCloseWindow, initial, confirm }) => {
            const [startDate, setStartDate] = useState(initial && initial.startDate ? initial.startDate : todayString);
            const [endDate, setEndDate] = useState(initial && initial.endDate ? initial.endDate : todayString);
            const [excludedDates, setExcludedDates] = useState(initial && initial.excludedDates ? initial.excludedDates : []);
            const [timeSlots, setTimeSlots] = useState(initial && initial.timeSlots ? initial.timeSlots : DEFAULT_SLOTS.slice());
            const [enabledSlots, setEnabledSlots] = useState(initial && initial.enabledSlots ? initial.enabledSlots : DEFAULT_ENABLED.slice());
            const [newTime, setNewTime] = useState('');

            const rangeDays = useMemo(() => getDaysInRange(startDate, endDate, []), [startDate, endDate]);

            const toggleExcluded = (date) => {
                setExcludedDates(prev => prev.includes(date) ? prev.filter(d => d !== date) : [...prev, date]);
            };

            const toggleSlot = (time) => {
                setEnabledSlots(prev => prev.includes(time) ? prev.filter(t => t !== time) : [...prev, time]);
            };

            const addTime = () => {
                if (!newTime || timeSlots.includes(newTime)) return;
                setTimeSlots(prev => [...prev, newTime].sort());
                setNewTime('');
            };

            return (
                <div className="max-w-md mx-auto min-h-screen pt-8 px-4 pb-28">
                    <div className="flex items-center gap-3 mb-6 px-2">
                        <button onClick={onBack} className="p-2 rounded-xl glass-panel"><Icons.Undo /></button>
                        <h1 className="text-xl font-bold text-stone-800 dark:text-stone-100">Окно записи</h1>
                    </div>

                    <div className="space-y-5 px-2">
                        <div className="grid grid-cols-2 gap-4">
                            <div>
                                <label className="block text-sm text-stone-600 dark:text-stone-300 mb-1">С</label>
                                <input type="date" value={startDate} onChange={e => setStartDate(e.target.value)} className="glass-input w-full px-3 py-2.5 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                            </div>
                            <div>
                                <label className="block text-sm text-stone-600 dark:text-stone-300 mb-1">По</label>
                                <input type="date" value={endDate} min={startDate} onChange={e => setEndDate(e.target.value)} className="glass-input w-full px-3 py-2.5 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                            </div>
                        </div>

                        <div>
                            <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-2">Выходные в диапазоне</label>
                            <div className="flex flex-wrap gap-2">
                                {rangeDays.map(date => (
                                    <button key={date} type="button" onClick={() => toggleExcluded(date)} className={`px-2.5 py-1 rounded-lg text-xs border ${excludedDates.includes(date) ? 'bg-red-100 text-red-600 border-red-200 dark:bg-red-900/30 dark:text-red-400' : 'bg-white/70 border-nude/60 dark:bg-stonepanel dark:border-gold/10'}`}>
                                        {new Date(date + 'T12:00:00').toLocaleDateString('ru-RU', { day: 'numeric', month: 'short' })}
                                    </button>
                                ))}
                            </div>
                        </div>

                        <div>
                            <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-2">Время</label>
                            <div className="flex flex-wrap gap-2">
                                {timeSlots.map(time => (
                                    <button key={time} type="button" onClick={() => toggleSlot(time)} className={`px-4 py-2 rounded-xl text-sm border ${enabledSlots.includes(time) ? 'bg-bronze text-white border-bronze dark:bg-gold/20 dark:text-gold dark:border-gold/40' : 'bg-white/70 border-nude/60 opacity-50 dark:bg-stonepanel dark:border-gold/10'}`}>
                                        {time}
                                    </button>
                                ))}
                            </div>
                            <div className="flex gap-2 mt-3">
                                <input type="time" value={newTime} onChange={e => setNewTime(e.target.value)} className="glass-input flex-1 px-3 py-2 rounded-xl dark:[&::-webkit-calendar-picker-indicator]:invert" />
                                <button type="button" onClick={addTime} className="px-4 py-2 rounded-xl bg-white/70 border border-nude/60 dark:bg-stonepanel text-sm">Добавить</button>
                            </div>
                        </div>

                        {isBookingWindowActive(initial) && (
                            <div className="p-3 rounded-xl bg-emerald-50 dark:bg-emerald-900/20 border border-emerald-200 dark:border-emerald-800/40 text-sm text-emerald-700 dark:text-emerald-300">
                                Окно открыто до {formatDate(initial.endDate)}
                            </div>
                        )}

                        <button onClick={() => onOpen({ startDate, endDate, excludedDates, timeSlots, enabledSlots, isOpen: true })} className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-4 rounded-2xl mt-4">
                            Открыть окно записей
                        </button>

                        {isBookingWindowActive(initial) && (
                            <button
                                type="button"
                                onClick={async () => {
                                    const ok = await confirm(
                                        'Клиенты больше не смогут записываться.',
                                        { title: 'Закрыть окно записи?', confirmLabel: 'Закрыть', danger: true }
                                    );
                                    if (ok) onCloseWindow({ startDate, endDate, excludedDates, timeSlots, enabledSlots });
                                }}
                                className="w-full py-4 rounded-2xl mt-2 border border-red-200 dark:border-red-900/40 text-red-600 dark:text-red-400 font-semibold hover:bg-red-50 dark:hover:bg-red-900/20 transition-colors"
                            >
                                Закрыть окно
                            </button>
                        )}
                    </div>
                </div>
            );
        };

        const IncomeModal = ({ isOpen, onClose, records }) => {
            const [viewMode, setViewMode] = useState('month');

            const incomeData = useMemo(() => {
                const byMonth = {};
                const byYear = {};
                records.forEach(r => {
                    if (isNote(r)) return;
                    const price = Number(r.price);
                    if (!price || price <= 0 || !r.date) return;
                    const monthKey = r.date.substring(0, 7);
                    const yearKey = r.date.substring(0, 4);
                    byMonth[monthKey] = (byMonth[monthKey] || 0) + price;
                    byYear[yearKey] = (byYear[yearKey] || 0) + price;
                });
                return { byMonth, byYear };
            }, [records]);

            const sortedEntries = useMemo(() => {
                const data = viewMode === 'month' ? incomeData.byMonth : incomeData.byYear;
                return Object.entries(data).sort((a, b) => b[0].localeCompare(a[0]));
            }, [incomeData, viewMode]);

            const totalShown = sortedEntries.reduce((sum, [, amount]) => sum + amount, 0);

            if (!isOpen) return null;

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm transition-opacity">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden relative max-h-[85vh] flex flex-col">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 bg-white/50 dark:bg-stonepanel/50 shrink-0">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">Доходы</h2>
                            <button onClick={onClose} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 transition-colors text-stone-600 dark:text-stone-300">
                                <Icons.Close />
                            </button>
                        </div>

                        <div className="p-5 space-y-4 overflow-y-auto">
                            <div className="flex bg-nude/20 dark:bg-stonepanel p-1 rounded-xl border border-nude/40 dark:border-gold/10">
                                <button
                                    onClick={() => setViewMode('month')}
                                    className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${viewMode === 'month' ? 'bg-white shadow-sm text-bronze dark:bg-gold/10 dark:text-gold dark:shadow-none dark:border dark:border-gold/20' : 'text-stone-500 hover:text-stone-700 dark:text-stone-400 dark:hover:text-stone-300'}`}
                                >
                                    По месяцам
                                </button>
                                <button
                                    onClick={() => setViewMode('year')}
                                    className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${viewMode === 'year' ? 'bg-white shadow-sm text-bronze dark:bg-gold/10 dark:text-gold dark:shadow-none dark:border dark:border-gold/20' : 'text-stone-500 hover:text-stone-700 dark:text-stone-400 dark:hover:text-stone-300'}`}
                                >
                                    По годам
                                </button>
                            </div>

                            {sortedEntries.length > 0 && (
                                <div className="glass-panel rounded-2xl p-4 border border-nude/40 dark:border-gold/10">
                                    <div className="text-sm text-stone-500 dark:text-stone-400 mb-1">Итого за период</div>
                                    <div className="text-2xl font-bold text-bronze dark:text-gold">{totalShown.toLocaleString('ru-RU')} ₸</div>
                                </div>
                            )}

                            {sortedEntries.length === 0 ? (
                                <div className="text-center py-10 text-stone-500 dark:text-stone-500">
                                    <div className="flex justify-center mb-3 text-stone-400 dark:text-stone-600"><Icons.Chart /></div>
                                    <p className="text-sm">Нет записей со стоимостью</p>
                                </div>
                            ) : (
                                <div className="space-y-2">
                                    {sortedEntries.map(([key, amount]) => (
                                        <div key={key} className="flex justify-between items-center glass-panel rounded-xl px-4 py-3 border border-nude/30 dark:border-gold/10">
                                            <span className="font-medium text-stone-700 dark:text-stone-200 capitalize">
                                                {viewMode === 'month' ? formatMonthYear(key) : formatYear(key)}
                                            </span>
                                            <span className="font-bold text-bronze dark:text-gold">{amount.toLocaleString('ru-RU')} ₸</span>
                                        </div>
                                    ))}
                                </div>
                            )}
                        </div>
                    </div>
                </div>
            );
        };

        const App = () => {
            const [user, setUser] = useState(null);
            const [authLoading, setAuthLoading] = useState(true);
            const [isAdmin, setIsAdmin] = useState(false);
            const [accessChecked, setAccessChecked] = useState(false);
            const [authError, setAuthError] = useState('');
            const [signInLoading, setSignInLoading] = useState(false);
            const [profileSaving, setProfileSaving] = useState(false);
            const [dataLoading, setDataLoading] = useState(false);

            const [userProfile, setUserProfile] = useState(null);
            const [records, setRecords] = useState([]);
            const [clients, setClients] = useState([]);
            const [bookingWindow, setBookingWindow] = useState(null);
            const [bookedSlots, setBookedSlots] = useState([]);
            const [myRecords, setMyRecords] = useState([]);

            const [activeTab, setActiveTab] = useState('schedule');
            const [adminView, setAdminView] = useState('main');
            const [scheduleMode, setScheduleMode] = useState('upcoming');
            const [selectedDate, setSelectedDate] = useState('');
            const [scheduleSearch, setScheduleSearch] = useState('');
            const [clientSearch, setClientSearch] = useState('');

            const [isModalOpen, setIsModalOpen] = useState(false);
            const [editingRecord, setEditingRecord] = useState(null);
            const [isClientModalOpen, setIsClientModalOpen] = useState(false);
            const [editingClient, setEditingClient] = useState(null);
            const [isIncomeModalOpen, setIsIncomeModalOpen] = useState(false);
            const [isContactImportOpen, setIsContactImportOpen] = useState(false);
            const [confirmDialog, setConfirmDialog] = useState(null);
            const [alertDialog, setAlertDialog] = useState(null);

            const confirm = useCallback((message, opts = {}) => new Promise((resolve) => {
                setConfirmDialog({
                    message,
                    title: opts.title,
                    confirmLabel: opts.confirmLabel,
                    cancelLabel: opts.cancelLabel,
                    danger: opts.danger,
                    onConfirm: () => { setConfirmDialog(null); resolve(true); },
                    onCancel: () => { setConfirmDialog(null); resolve(false); },
                });
            }), []);

            const showAlert = useCallback((message, opts = {}) => new Promise((resolve) => {
                setAlertDialog({
                    message,
                    title: opts.title,
                    buttonLabel: opts.buttonLabel,
                    onClose: () => { setAlertDialog(null); resolve(); },
                });
            }), []);

            const dialogLayer = (
                <React.Fragment>
                    <ConfirmDialog
                        isOpen={!!confirmDialog}
                        title={confirmDialog ? confirmDialog.title : undefined}
                        message={confirmDialog ? confirmDialog.message : undefined}
                        confirmLabel={confirmDialog ? confirmDialog.confirmLabel : undefined}
                        cancelLabel={confirmDialog ? confirmDialog.cancelLabel : undefined}
                        danger={confirmDialog ? confirmDialog.danger : undefined}
                        onConfirm={confirmDialog ? confirmDialog.onConfirm : () => {}}
                        onCancel={confirmDialog ? confirmDialog.onCancel : () => {}}
                    />
                    <AlertDialog
                        isOpen={!!alertDialog}
                        title={alertDialog ? alertDialog.title : undefined}
                        message={alertDialog ? alertDialog.message : undefined}
                        buttonLabel={alertDialog ? alertDialog.buttonLabel : undefined}
                        onClose={alertDialog ? alertDialog.onClose : () => {}}
                    />
                </React.Fragment>
            );

            const [themeMode, setThemeMode] = useState(() => {
                const saved = localStorage.getItem('manicureTheme');
                if (saved === 'light' || saved === 'dark' || saved === 'auto') return saved;
                return 'auto';
            });
            const effectiveTheme = themeMode === 'auto' ? getTimeBasedTheme() : themeMode;

            useEffect(() => {
                if (effectiveTheme === 'dark') document.documentElement.classList.add('dark');
                else document.documentElement.classList.remove('dark');
                localStorage.setItem('manicureTheme', themeMode);
            }, [effectiveTheme, themeMode]);

            const handleThemeToggle = () => setThemeMode(prev => cycleThemeMode(prev));

            useEffect(() => {
                const unsubscribe = auth.onAuthStateChanged(async (firebaseUser) => {
                    setUser(firebaseUser);
                    setAuthError('');
                    if (!firebaseUser) {
                        setIsAdmin(false);
                        setUserProfile(null);
                        setAccessChecked(true);
                        setRecords([]);
                        setClients([]);
                        setMyRecords([]);
                        setAuthLoading(false);
                        return;
                    }
                    setAccessChecked(false);
                    try {
                        const admin = await checkIsAdmin(firebaseUser.email);
                        setIsAdmin(admin);
                        const profSnap = await userProfileRef(firebaseUser.uid).get();
                        setUserProfile(profSnap.exists ? profSnap.data() : null);
                    } catch (e) {
                        console.error(e);
                        setAuthError('Ошибка загрузки профиля.');
                    } finally {
                        setAccessChecked(true);
                        setAuthLoading(false);
                    }
                });
                return () => unsubscribe();
            }, []);

            const migrateSharedData = useCallback(async (uid) => {
                const existing = await recordsRef().limit(1).get();
                if (!existing.empty) return;
                const legRec = await legacyUserRecordsRef(uid).get();
                const legCli = await legacyUserClientsRef(uid).get();
                if (legRec.empty && legCli.empty) return;
                const batch = db.batch();
                legRec.forEach(d => batch.set(recordsRef().doc(d.id), d.data()));
                legCli.forEach(d => {
                    const data = d.data();
                    const adminName = data.adminName || data.name || '';
                    const phone = data.phone || '';
                    batch.set(clientsRef().doc(d.id), { ...data, adminName });
                    if (phone) batch.set(phoneLookupRef(phone), { clientId: data.id || d.id });
                });
                await batch.commit();
            }, []);

            useEffect(() => {
                if (!user) return;
                let active = true;
                const unsubs = [];

                const setup = async () => {
                    setDataLoading(true);
                    if (isAdmin) await migrateSharedData(user.uid).catch(console.error);
                    if (!active) return;

                    unsubs.push(bookingWindowRef().onSnapshot(s => setBookingWindow(s.exists ? s.data() : null)));
                    unsubs.push(bookedSlotsRef().onSnapshot(s => setBookedSlots(s.docs.map(d => d.data()))));

                    if (isAdmin) {
                        unsubs.push(recordsRef().onSnapshot(s => setRecords(s.docs.map(d => d.data()))));
                        unsubs.push(clientsRef().onSnapshot(s => setClients(s.docs.map(d => d.data()))));
                    } else {
                        unsubs.push(recordsRef().where('bookedByUid', '==', user.uid).onSnapshot(s => setMyRecords(s.docs.map(d => d.data()))));
                    }
                    setDataLoading(false);
                };
                setup();
                return () => { active = false; unsubs.forEach(u => u()); };
            }, [user, isAdmin, migrateSharedData]);

            useEffect(() => {
                if (!isAdmin || !bookingWindow || !bookingWindow.isOpen) return;
                if (bookingWindow.endDate && bookingWindow.endDate < todayString) {
                    bookingWindowRef().update({ isOpen: false, closedAt: Date.now(), closedReason: 'expired' }).catch(console.error);
                }
            }, [isAdmin, bookingWindow]);

            const handleGoogleSignIn = async () => {
                setSignInLoading(true);
                setAuthError('');
                try { await auth.signInWithPopup(googleProvider); }
                catch (e) { if (e.code !== 'auth/popup-closed-by-user') setAuthError('Не удалось войти.'); }
                finally { setSignInLoading(false); }
            };

            const handleSignOut = async () => { await auth.signOut(); };

            const ensureClientInDb = async (phone, adminName, linkedUid) => {
                const norm = normalizePhone(phone);
                const lookup = await phoneLookupRef(phone).get();
                if (lookup.exists) {
                    const clientId = lookup.data().clientId;
                    const clientRef = clientsRef().doc(String(clientId));
                    const clientSnap = await clientRef.get();
                    if (clientSnap.exists && linkedUid && !clientSnap.data().linkedUid) {
                        await clientRef.update({ linkedUid });
                    }
                    return clientSnap.exists ? clientSnap.data() : null;
                }
                const id = Date.now();
                const data = { id, adminName, phone: norm, isInactive: false, linkedUid: linkedUid || null };
                await clientsRef().doc(String(id)).set(data);
                await phoneLookupRef(phone).set({ clientId: id });
                return data;
            };

            const handleSaveProfile = async (data) => {
                if (!user) return;
                setProfileSaving(true);
                try {
                    const profile = { ...data, email: user.email, uid: user.uid };
                    await userProfileRef(user.uid).set(profile);
                    const adminName = data.firstName + ' ' + data.lastName;
                    await ensureClientInDb(data.phone, adminName, user.uid);
                    setUserProfile(profile);
                } catch (e) {
                    setAuthError('Не удалось сохранить профиль.');
                } finally {
                    setProfileSaving(false);
                }
            };

            const handleClientBook = async (date, time) => {
                if (!user || !userProfile) return;
                if (bookedSlots.some(s => s.date === date && s.time === time)) {
                    await showAlert('Это время уже занято. Выберите другое.');
                    return;
                }
                const norm = normalizePhone(userProfile.phone);
                const client = await ensureClientInDb(norm, userProfile.firstName + ' ' + userProfile.lastName, user.uid);
                if (!client) {
                    await showAlert('Не удалось создать запись. Попробуйте позже.');
                    return;
                }
                const id = Date.now();
                const record = {
                    id, type: 'appointment', date, time,
                    clientName: getClientAdminName(client),
                    phone: norm,
                    clientId: client.id,
                    bookedByUid: user.uid,
                    isSelfBooked: true,
                    isNewFromClient: true,
                    service: 'Онлайн-запись',
                    price: '',
                    archived: false
                };
                await recordsRef().doc(String(id)).set(record);
                await syncBookedSlot(id, date, time, user.uid);
            };

            const handleSaveRecord = async (recordData) => {
                if (!user || !isAdmin) return;
                const id = editingRecord ? recordData.id : Date.now();
                const data = { ...recordData, id };
                const old = editingRecord;

                await recordsRef().doc(String(id)).set(data);
                if (!isNote(data)) {
                    if (old && old.date && old.time && !old.customTime) {
                        await removeBookedSlot(old.date, old.time);
                    }
                    if (data.date && data.time && !data.customTime) {
                        await syncBookedSlot(id, data.date, data.time, data.bookedByUid || null);
                    }
                }

                if (!isNote(data) && data.clientName && !data.isSelfBooked) {
                    const norm = normalizePhone(data.phone);
                    const existing = clients.find(c => getClientAdminName(c).toLowerCase() === data.clientName.toLowerCase());
                    if (!existing) {
                        const clientId = Date.now() + 1;
                        await clientsRef().doc(String(clientId)).set({ id: clientId, adminName: data.clientName, phone: norm, isInactive: false });
                        if (norm) await phoneLookupRef(norm).set({ clientId });
                    } else if (norm && !existing.phone) {
                        await clientsRef().doc(String(existing.id)).update({ phone: norm });
                        await phoneLookupRef(norm).set({ clientId: existing.id });
                    }
                }
                setEditingRecord(null);
                setIsModalOpen(false);
            };

            const handleArchiveRecord = async (id) => {
                if (!user || !isAdmin) return;
                await recordsRef().doc(String(id)).update({ archived: true });
            };

            const handleRestoreRecord = async (id) => {
                if (!user || !isAdmin) return;
                await recordsRef().doc(String(id)).update({ archived: false });
            };

            const handleAcknowledgeRecord = async (id) => {
                if (!user || !isAdmin) return;
                await recordsRef().doc(String(id)).update({ isNewFromClient: false });
            };

            const handleDeleteRecord = async (id) => {
                if (!user || !isAdmin) return;
                const ok = await confirm('Удалить запись?', { title: 'Удаление записи', confirmLabel: 'Удалить', danger: true });
                if (!ok) return;
                const rec = records.find(r => r.id === id);
                await recordsRef().doc(String(id)).delete();
                if (rec && rec.date && rec.time && !rec.customTime) await removeBookedSlot(rec.date, rec.time);
            };

            const handleSaveClient = async (updatedClient) => {
                if (!user || !isAdmin) return;
                const isNew = !updatedClient.id;
                const clientId = isNew ? Date.now() : updatedClient.id;
                const adminName = updatedClient.adminName || updatedClient.name || '';
                const data = { ...updatedClient, id: clientId, adminName, phone: normalizePhone(updatedClient.phone) || updatedClient.phone || '' };

                const oldClient = !isNew ? clients.find(c => c.id === updatedClient.id) : null;
                await clientsRef().doc(String(clientId)).set(data);
                if (data.phone) {
                    await phoneLookupRef(data.phone).set({ clientId });
                    if (oldClient && oldClient.phone && normalizePhone(oldClient.phone) !== data.phone) {
                        await phoneLookupRef(oldClient.phone).delete().catch(() => {});
                    }
                }

                if (!isNew) {
                    const oldClient = clients.find(c => c.id === updatedClient.id);
                    const oldName = oldClient ? getClientAdminName(oldClient) : undefined;
                    if (oldName && oldName !== adminName) {
                        const batch = db.batch();
                        records.filter(r => !isNote(r) && r.clientName === oldName).forEach(r => {
                            batch.update(recordsRef().doc(String(r.id)), { clientName: adminName });
                        });
                        await batch.commit();
                    }
                }
                setIsClientModalOpen(false);
                setEditingClient(null);
            };

            const handleDeleteClient = async (clientId) => {
                if (!user || !isAdmin) return;
                const client = clients.find(c => c.id === clientId);
                await clientsRef().doc(String(clientId)).delete();
                if (client && client.phone) await phoneLookupRef(client.phone).delete().catch(() => {});
                setIsClientModalOpen(false);
                setEditingClient(null);
            };

            const handleImportContacts = async (importList) => {
                if (!user || !importList.length) return;
                const batch = db.batch();
                importList.forEach((c, i) => {
                    const id = Date.now() + i;
                    const phone = normalizePhone(c.phone) || c.phone || '';
                    batch.set(clientsRef().doc(String(id)), { id, adminName: c.name, phone, isInactive: false });
                    if (phone) batch.set(phoneLookupRef(phone), { clientId: id });
                });
                await batch.commit();
                setIsContactImportOpen(false);
            };

            const handleOpenBookingWindow = async (config) => {
                await bookingWindowRef().set({ ...config, isOpen: true, updatedAt: Date.now(), closedAt: null, closedReason: null });
                setAdminView('main');
            };

            const handleCloseBookingWindow = async (config) => {
                await bookingWindowRef().set({ ...config, isOpen: false, updatedAt: Date.now(), closedAt: Date.now(), closedReason: 'manual' });
                setAdminView('main');
            };

            const handleFabClick = () => {
                if (activeTab === 'clients') {
                    setEditingClient({ id: null, adminName: '', phone: '', isInactive: false });
                    setIsClientModalOpen(true);
                } else {
                    setEditingRecord(null);
                    setIsModalOpen(true);
                }
            };

            // Обработка расписания
            const groupedRecords = useMemo(() => {
                let filtered = records;

                if (selectedDate) {
                    filtered = filtered.filter(r => r.date === selectedDate);
                } else {
                    if (scheduleMode === 'upcoming') {
                        filtered = filtered.filter(r => !r.archived && r.date >= todayString);
                    } else {
                        filtered = filtered.filter(r => r.archived || r.date < todayString);
                    }
                }

                if (scheduleSearch) {
                    const q = scheduleSearch.toLowerCase();
                    filtered = filtered.filter(r => 
                        (r.clientName && r.clientName.toLowerCase().includes(q)) ||
                        (r.service && r.service.toLowerCase().includes(q)) ||
                        (r.noteText && r.noteText.toLowerCase().includes(q))
                    );
                }
                
                const sorted = filtered.sort((a, b) => {
                    if (a.date !== b.date) {
                        if (scheduleMode === 'archive' && !selectedDate) {
                            return new Date(b.date) - new Date(a.date);
                        }
                        return new Date(a.date) - new Date(b.date);
                    }
                    return a.time.localeCompare(b.time);
                });

                return sorted.reduce((acc, record) => {
                    if (!acc[record.date]) acc[record.date] = [];
                    acc[record.date].push(record);
                    return acc;
                }, {});
            }, [records, scheduleMode, scheduleSearch, selectedDate]);

            // Обработка базы клиентов
            const clientsWithStats = useMemo(() => {
                const statsMap = {};
                clients.forEach(c => {
                    statsMap[c.id] = { ...c, visits: 0, lastVisit: null, daysSince: Infinity };
                });

                records.forEach(r => {
                    if (isNote(r)) return;
                    const client = clients.find(c => getClientAdminName(c) === r.clientName || c.id === r.clientId);
                    if (client && statsMap[client.id]) {
                        statsMap[client.id].visits += 1;
                        if (!statsMap[client.id].lastVisit || r.date > statsMap[client.id].lastVisit) {
                            statsMap[client.id].lastVisit = r.date;
                            if (r.date <= todayString) {
                                const diff = new Date(todayString) - new Date(r.date);
                                statsMap[client.id].daysSince = Math.floor(diff / (1000 * 3600 * 24));
                            } else {
                                statsMap[client.id].daysSince = 0; 
                            }
                        }
                    }
                });

                let resultList = Object.values(statsMap);
                if (clientSearch) {
                    resultList = resultList.filter(c => 
                        getClientAdminName(c).toLowerCase().includes(clientSearch.toLowerCase()) ||
                        (c.phone && c.phone.includes(clientSearch))
                    );
                }

                return resultList.sort((a, b) => {
                    if (a.isInactive !== b.isInactive) return a.isInactive ? 1 : -1;
                    if (a.daysSince === Infinity && b.daysSince === Infinity) return 0;
                    if (a.daysSince === Infinity) return 1;
                    if (b.daysSince === Infinity) return -1;
                    return b.daysSince - a.daysSince;
                });
            }, [clients, records, clientSearch]);


            if (authLoading || (user && !accessChecked)) {
                return (
                    <div className="auth-screen">
                        <div className="text-stone-500 dark:text-stone-400 text-sm">Загрузка...</div>
                    </div>
                );
            }

            if (!user) {
                return <LoginScreen onSignIn={handleGoogleSignIn} error={authError} loading={signInLoading} />;
            }

            if (!isAdmin && !userProfile) {
                return <ProfileSetupScreen onSave={handleSaveProfile} loading={profileSaving} error={authError} />;
            }

            if (!isAdmin) {
                return (
                    <React.Fragment>
                        <ClientBookingApp
                            profile={userProfile}
                            bookingWindow={bookingWindow}
                            bookedSlots={bookedSlots}
                            myRecords={myRecords}
                            onBook={handleClientBook}
                            onSignOut={handleSignOut}
                            themeMode={themeMode}
                            effectiveTheme={effectiveTheme}
                            onThemeToggle={handleThemeToggle}
                            confirm={confirm}
                        />
                        {dialogLayer}
                    </React.Fragment>
                );
            }

            if (adminView === 'bookingWindow') {
                return (
                    <React.Fragment>
                        <BookingWindowScreen
                            onBack={() => setAdminView('main')}
                            onOpen={handleOpenBookingWindow}
                            onCloseWindow={handleCloseBookingWindow}
                            initial={bookingWindow}
                            confirm={confirm}
                        />
                        {dialogLayer}
                    </React.Fragment>
                );
            }

            return (
                <React.Fragment>
                <div className="max-w-md mx-auto min-h-screen flex flex-col relative pt-8 px-4">
                    {dataLoading && (
                        <div className="fixed top-4 left-1/2 -translate-x-1/2 z-50 px-4 py-2 rounded-full glass-panel text-xs text-stone-500 dark:text-stone-400 border border-nude/40 dark:border-gold/10">
                            Синхронизация...
                        </div>
                    )}

                    {/* Навигация расписания и поиск */}
                    {activeTab === 'schedule' && (
                        <div className="mb-6 space-y-4">
                            {/* Доходы, переключатель, тема */}
                            <div className="flex items-center space-x-2 px-2">
                                <button
                                    onClick={() => setIsIncomeModalOpen(true)}
                                    className="h-[42px] w-[42px] shrink-0 rounded-xl border flex items-center justify-center transition-all shadow-sm bg-white/70 border-nude/60 text-bronze hover:text-bronzedark dark:bg-stonepanel dark:border-gold/10 dark:text-gold dark:hover:text-white"
                                    title="Доходы"
                                >
                                    <Icons.Chart />
                                </button>

                                <div className="flex bg-nude/20 dark:bg-stonepanel p-1 rounded-xl border border-nude/40 dark:border-gold/10 flex-1 shadow-inner">
                                    <button 
                                        onClick={() => { setScheduleMode('upcoming'); setSelectedDate(''); setScheduleSearch(''); }} 
                                        className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${scheduleMode === 'upcoming' && !selectedDate ? 'bg-white shadow-sm text-bronze dark:bg-gold/10 dark:text-gold dark:shadow-none dark:border dark:border-gold/20' : 'text-stone-500 hover:text-stone-700 dark:text-stone-400 dark:hover:text-stone-300'}`}
                                    >
                                        Текущие
                                    </button>
                                    <button 
                                        onClick={() => { setScheduleMode('archive'); setSelectedDate(''); setScheduleSearch(''); }} 
                                        className={`flex-1 py-2 rounded-lg text-sm font-medium transition-all ${scheduleMode === 'archive' && !selectedDate ? 'bg-white shadow-sm text-bronze dark:bg-gold/10 dark:text-gold dark:shadow-none dark:border dark:border-gold/20' : 'text-stone-500 hover:text-stone-700 dark:text-stone-400 dark:hover:text-stone-300'}`}
                                    >
                                        Архив
                                    </button>
                                </div>

                                <ThemeToggleButton
                                    themeMode={themeMode}
                                    effectiveTheme={effectiveTheme}
                                    onToggle={handleThemeToggle}
                                    className="h-[42px] w-[42px] shrink-0 rounded-xl glass-panel text-bronze dark:text-gold hover:text-bronzedark dark:hover:text-white transition-colors border border-nude/60 dark:border-gold/20 flex items-center justify-center"
                                />

                                <button
                                    onClick={handleSignOut}
                                    className="h-[42px] w-[42px] shrink-0 rounded-xl border flex items-center justify-center transition-all shadow-sm bg-white/70 border-nude/60 text-stone-500 hover:text-stone-700 dark:bg-stonepanel dark:border-gold/10 dark:text-stone-400 dark:hover:text-stone-200"
                                    title="Выйти"
                                >
                                    <Icons.LogOut />
                                </button>
                            </div>

                            {/* Поиск и календарь */}
                            <div className="flex items-center space-x-2 px-2">
                                <div className="relative flex-1">
                                    <div className="absolute inset-y-0 left-4 flex items-center pointer-events-none text-stone-400 dark:text-stone-500">
                                        <Icons.Search />
                                    </div>
                                    <input 
                                        type="text" 
                                        placeholder={selectedDate ? "Поиск на выбранную дату..." : (scheduleMode === 'upcoming' ? "Поиск в текущих..." : "Поиск в архиве...")}
                                        value={scheduleSearch}
                                        onChange={(e) => setScheduleSearch(e.target.value)}
                                        className="glass-input w-full pl-11 pr-11 py-3.5 rounded-2xl text-sm placeholder-stone-400 dark:placeholder-stone-500"
                                    />
                                    {scheduleSearch && (
                                        <button onClick={() => setScheduleSearch('')} className="absolute inset-y-0 right-4 flex items-center text-stone-400 hover:text-stone-600 dark:hover:text-stone-200 transition-colors">
                                            <Icons.XCircle />
                                        </button>
                                    )}
                                </div>

                                <div className="relative shrink-0">
                                    <button className={`h-[50px] w-[50px] rounded-xl border flex items-center justify-center transition-all shadow-sm ${selectedDate ? 'bg-nude border-bronze/30 text-bronzedark dark:bg-gold/20 dark:border-gold/40 dark:text-gold' : 'bg-white/70 border-nude/60 text-stone-500 dark:bg-stonepanel dark:border-gold/10 dark:text-stone-400'}`}>
                                        <Icons.Calendar />
                                    </button>
                                    <input 
                                        type="date" 
                                        className="absolute inset-0 opacity-0 w-full h-full cursor-pointer" 
                                        onChange={(e) => setSelectedDate(e.target.value)} 
                                        value={selectedDate} 
                                    />
                                </div>
                            </div>

                            {/* Плашка выбранной даты */}
                            {selectedDate && (
                                <div className="px-2">
                                    <div className="flex items-center justify-between bg-nude/30 border border-nude/60 dark:bg-gold/10 dark:border-gold/20 px-4 py-2.5 rounded-xl">
                                        <span className="text-bronzedark dark:text-gold text-sm font-medium">Дата: {formatDate(selectedDate)}</span>
                                        <button onClick={() => setSelectedDate('')} className="text-bronze hover:text-bronzedark dark:text-golddark dark:hover:text-gold transition-colors"><Icons.Close /></button>
                                    </div>
                                </div>
                            )}
                        </div>
                    )}

                    {/* Поиск клиентов */}
                    {activeTab === 'clients' && (
                        <div className="mb-6 px-2 space-y-3">
                            <div className="flex justify-end gap-2">
                                <button
                                    onClick={() => setAdminView('bookingWindow')}
                                    className="h-[42px] px-3 rounded-xl border flex items-center justify-center gap-1.5 transition-all shadow-sm bg-white/70 border-nude/60 text-bronze hover:text-bronzedark dark:bg-stonepanel dark:border-gold/10 dark:text-gold dark:hover:text-white text-xs font-semibold"
                                    title="Окно записи"
                                >
                                    <Icons.Calendar />
                                    <span>Окно</span>
                                </button>
                                <button
                                    onClick={() => setIsContactImportOpen(true)}
                                    className="h-[42px] w-[42px] rounded-xl border flex items-center justify-center transition-all shadow-sm bg-white/70 border-nude/60 text-bronze hover:text-bronzedark dark:bg-stonepanel dark:border-gold/10 dark:text-gold dark:hover:text-white"
                                    title="Импорт из контактов"
                                >
                                    <Icons.ContactImport />
                                </button>
                                <ThemeToggleButton
                                    themeMode={themeMode}
                                    effectiveTheme={effectiveTheme}
                                    onToggle={handleThemeToggle}
                                    className="h-[42px] w-[42px] rounded-xl glass-panel text-bronze dark:text-gold hover:text-bronzedark dark:hover:text-white transition-colors border border-nude/60 dark:border-gold/20 flex items-center justify-center"
                                />
                            </div>
                            <div className="relative">
                            <div className="absolute inset-y-0 left-5 flex items-center pointer-events-none text-stone-400 dark:text-stone-500">
                                <Icons.Search />
                            </div>
                            <input 
                                type="text" 
                                placeholder="Поиск клиентов..."
                                value={clientSearch}
                                onChange={(e) => setClientSearch(e.target.value)}
                                className="glass-input w-full pl-11 pr-11 py-3.5 rounded-2xl text-sm placeholder-stone-400 dark:placeholder-stone-500"
                            />
                            {clientSearch && (
                                <button onClick={() => setClientSearch('')} className="absolute inset-y-0 right-5 flex items-center text-stone-400 hover:text-stone-600 dark:hover:text-stone-200 transition-colors">
                                    <Icons.XCircle />
                                </button>
                            )}
                            </div>
                        </div>
                    )}

                    {/* Основной контент */}
                    <main className="flex-1 pb-20">
                        {activeTab === 'schedule' && (
                            <div className="space-y-6 fade-in">
                                {Object.keys(groupedRecords).length === 0 ? (
                                    <div className="text-center py-16 glass-panel rounded-3xl mx-2">
                                        <div className="flex justify-center mb-4 text-stone-400 dark:text-stone-600">
                                            <Icons.Calendar />
                                        </div>
                                        <h3 className="text-xl font-bold text-stone-700 dark:text-stone-300 mb-2">Пусто</h3>
                                        <p className="text-stone-500 dark:text-stone-500 text-sm px-6">На этот период записей не найдено.</p>
                                    </div>
                                ) : (
                                    Object.keys(groupedRecords).map(date => (
                                        <div key={date} className="px-2">
                                            <div className="inline-block px-4 py-1.5 rounded-full bg-white/80 dark:bg-stonepanel/90 backdrop-blur-md border border-nude/50 dark:border-gold/10 shadow-sm text-sm font-semibold text-stone-700 dark:text-stone-300 mb-4 sticky top-4 z-10">
                                                {date === todayString ? 'Сегодня, ' : ''}{formatDate(date)}
                                            </div>
                                            <div>
                                                {groupedRecords[date].map(record => (
                                                    <RecordCard 
                                                        key={record.id} 
                                                        record={record}
                                                        isArchiveView={scheduleMode === 'archive'}
                                                        onEdit={() => { setEditingRecord(record); setIsModalOpen(true); }} 
                                                        onDelete={handleDeleteRecord}
                                                        onArchive={handleArchiveRecord}
                                                        onRestore={handleRestoreRecord}
                                                        onAcknowledge={handleAcknowledgeRecord}
                                                    />
                                                ))}
                                            </div>
                                        </div>
                                    ))
                                )}
                            </div>
                        )}

                        {activeTab === 'clients' && (
                            <div className="space-y-3 fade-in px-2">
                                <div className="flex justify-between items-center mb-4 ml-1">
                                    <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">Клиенты</h2>
                                    <span className="text-sm font-medium text-stone-600 dark:text-stone-400 bg-white/60 dark:bg-stonepanel px-3 py-1 rounded-full border border-nude/50 dark:border-gold/10">{clientsWithStats.length} чел.</span>
                                </div>
                                
                                {clientsWithStats.map((client) => (
                                    <div key={client.id} className={`glass-panel rounded-2xl p-4 flex justify-between items-center transition-opacity ${client.isInactive ? 'opacity-50' : ''}`}>
                                        <div>
                                            <div className="flex items-center space-x-2">
                                                <h3 className="font-bold text-stone-800 dark:text-stone-100 text-lg">{getClientAdminName(client)}</h3>
                                                {client.isInactive && <span className="text-[10px] uppercase tracking-wider bg-red-100 dark:bg-red-900/30 text-red-600 dark:text-red-400 px-2 py-0.5 rounded-full border border-red-200 dark:border-red-900/50">Архив</span>}
                                            </div>
                                            {client.phone && <p className="text-sm text-stone-500 dark:text-stone-400 mt-0.5">{client.phone}</p>}
                                        </div>
                                        <div className="flex items-center space-x-3">
                                            <div className="text-right">
                                                {client.daysSince === 0 ? (
                                                    <div className="text-xs font-medium mb-1 text-bronze dark:text-gold">Сегодня</div>
                                                ) : client.daysSince !== Infinity && !client.isInactive ? (
                                                    <div className={`text-xs font-medium mb-1 ${client.daysSince > 30 ? 'text-[#a66a5b] dark:text-[#d4af37]' : 'text-stone-600 dark:text-stone-400'}`}>
                                                        {client.daysSince} {getDaysWord(client.daysSince)}
                                                    </div>
                                                ) : null}
                                                <div className="text-xs text-stone-400 dark:text-stone-500">Визиты: {client.visits}</div>
                                            </div>
                                        <div className="flex items-center space-x-2">
                                            {client.phone && (
                                                <button onClick={() => openWhatsApp(client.phone)} className="p-2 bg-green-50 dark:bg-green-900/20 rounded-full hover:bg-green-100 dark:hover:bg-green-900/40 text-green-600 dark:text-green-400 transition-colors border border-green-100 dark:border-green-900/30" title="WhatsApp">
                                                    <Icons.WhatsApp />
                                                </button>
                                            )}
                                            <button onClick={() => { setEditingClient(client); setIsClientModalOpen(true); }} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 text-stone-500 dark:text-stone-300 transition-colors border border-nude/30 dark:border-transparent">
                                                <Icons.Edit />
                                            </button>
                                        </div>
                                        </div>
                                    </div>
                                ))}
                                {clientsWithStats.length === 0 && (
                                    <div className="text-center py-10 text-stone-500 dark:text-stone-500">Ничего не найдено</div>
                                )}
                            </div>
                        )}
                    </main>

                    {/* Модалки */}
                    <AddModal 
                        isOpen={isModalOpen} 
                        initialData={editingRecord}
                        clients={clients}
                        bookingWindow={bookingWindow}
                        bookedSlots={bookedSlots}
                        onClose={() => { setIsModalOpen(false); setEditingRecord(null); }} 
                        onSave={handleSaveRecord} 
                    />

                    <EditClientModal
                        isOpen={isClientModalOpen}
                        client={editingClient}
                        onClose={() => { setIsClientModalOpen(false); setEditingClient(null); }}
                        onSave={handleSaveClient}
                        onDelete={handleDeleteClient}
                        confirm={confirm}
                    />

                    <ContactImportModal
                        isOpen={isContactImportOpen}
                        onClose={() => setIsContactImportOpen(false)}
                        onImport={handleImportContacts}
                        existingClients={clients}
                    />

                    <IncomeModal
                        isOpen={isIncomeModalOpen}
                        onClose={() => setIsIncomeModalOpen(false)}
                        records={records}
                    />

                    {/* Навигация снизу */}
                    <nav className="fixed bottom-0 left-0 right-0 glass-nav pb-safe pt-3 px-6 pb-5 z-40">
                        <div className="max-w-md mx-auto flex justify-between items-center relative">
                            
                            <button 
                                onClick={() => setActiveTab('schedule')}
                                className={`flex flex-col items-center p-2 px-8 rounded-2xl transition-all duration-300 ${activeTab === 'schedule' ? 'text-bronzedark bg-nude/40 shadow-sm border border-nude/60 dark:text-gold dark:bg-gold/10 dark:border-gold/20' : 'text-stone-400 hover:text-stone-600 dark:text-stone-500 dark:hover:text-stone-300'}`}
                            >
                                <Icons.Calendar />
                                <span className="text-[11px] font-bold mt-1.5">Записи</span>
                            </button>

                            <div className="absolute left-1/2 -translate-x-1/2 -top-10">
                                <button 
                                    onClick={handleFabClick}
                                    className="w-[68px] h-[68px] rounded-full bg-bronze dark:bg-gradient-to-tr dark:from-gold dark:to-golddark text-white dark:text-stone-900 flex items-center justify-center shadow-[0_8px_25px_rgba(127,96,62,0.4)] dark:shadow-[0_8px_25px_rgba(212,175,55,0.2)] transform transition hover:scale-105 active:scale-95 border-[6px] border-[#fdfbf9] dark:border-[#050505]"
                                >
                                    <Icons.Plus />
                                </button>
                            </div>

                            <button 
                                onClick={() => setActiveTab('clients')}
                                className={`flex flex-col items-center p-2 px-8 rounded-2xl transition-all duration-300 ${activeTab === 'clients' ? 'text-bronzedark bg-nude/40 shadow-sm border border-nude/60 dark:text-gold dark:bg-gold/10 dark:border-gold/20' : 'text-stone-400 hover:text-stone-600 dark:text-stone-500 dark:hover:text-stone-300'}`}
                            >
                                <Icons.Users />
                                <span className="text-[11px] font-bold mt-1.5">Клиенты</span>
                            </button>
                            
                        </div>
                    </nav>

                </div>
                {dialogLayer}
            </React.Fragment>
            );
        };

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);

        if ('serviceWorker' in navigator) {
            window.addEventListener('load', () => {
                navigator.serviceWorker.register('./service-worker.js').catch((err) => {
                    console.warn('Service worker registration failed:', err);
                });
            });
        }
    </script>
</body>
</html>