<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Записи Маникюр</title>
    
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
            Google: () => <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"><path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/><path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/><path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/><path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/></svg>
        };

        const userRecordsRef = (uid) => db.collection('users').doc(uid).collection('records');
        const userClientsRef = (uid) => db.collection('users').doc(uid).collection('clients');

        const checkUserAllowed = async (email) => {
            if (!email) return false;
            const doc = await db.collection('allowedUsers').doc(email).get();
            return doc.exists && doc.data().active !== false;
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

        const AccessDeniedScreen = ({ email, onSignOut }) => (
            <div className="auth-screen">
                <div className="glass-panel w-full max-w-sm rounded-3xl p-8 text-center shadow-2xl">
                    <h1 className="text-xl font-bold text-stone-800 dark:text-stone-100 mb-3">Нет доступа</h1>
                    <p className="text-stone-500 dark:text-stone-400 text-sm mb-2">
                        Аккаунт <span className="font-medium text-stone-700 dark:text-stone-300">{email}</span> не добавлен в список разрешённых.
                    </p>
                    <p className="text-stone-400 dark:text-stone-500 text-xs mb-6">Обратитесь к администратору, чтобы добавить ваш Gmail в Firebase.</p>
                    <button
                        onClick={onSignOut}
                        className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3 px-4 rounded-xl"
                    >
                        Выйти
                    </button>
                </div>
            </div>
        );

        const SERVICE_PRESETS = ['Маникюр', 'Гель-лак', 'Снятие', 'Наращивание', 'Починка', 'Дизайн'];

        const parseService = (service) => {
            const parts = (service || '').split(' + ').map(s => s.trim()).filter(Boolean);
            const presets = [];
            const custom = [];
            parts.forEach(p => {
                if (SERVICE_PRESETS.includes(p)) presets.push(p);
                else custom.push(p);
            });
            return { presets, custom: custom.join(' + ') };
        };

        const buildService = (presets, custom) => {
            const orderedPresets = SERVICE_PRESETS.filter(p => presets.includes(p));
            const parts = [...orderedPresets];
            if (custom && custom.trim()) parts.push(custom.trim());
            return parts.join(' + ');
        };

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

        const AppointmentCard = ({ record, onEdit, onDelete }) => {
            const [showActions, setShowActions] = useState(false);

            return (
                <div 
                    className="glass-panel rounded-2xl p-4 mb-4 relative overflow-hidden transition-all cursor-pointer select-none" 
                    onClick={() => setShowActions(!showActions)}
                >
                    {/* Акцентная полоса */}
                    <div className="absolute left-0 top-0 bottom-0 w-1.5 bg-gradient-to-b from-nude to-bronze dark:from-gold dark:to-golddark opacity-90"></div>
                    
                    <div className="flex justify-between items-start ml-2">
                        <div>
                            <h3 className="text-lg font-bold text-stone-800 dark:text-stone-100">{record.clientName}</h3>
                            {record.phone && (
                                <div className="flex items-center text-stone-500 dark:text-stone-400 text-sm mt-1">
                                    <span className="text-bronze dark:text-gold mr-1.5"><Icons.Phone /></span>
                                    {record.phone}
                                </div>
                            )}
                        </div>
                        <div className="text-right">
                            <div className="inline-block bg-white/80 dark:bg-stonepanel backdrop-blur-sm rounded-lg px-3 py-1 font-semibold text-bronze dark:text-gold shadow-sm border border-nude/60 dark:border-gold/20">
                                {record.time}
                            </div>
                        </div>
                    </div>
                    
                    <div className="mt-4 ml-2 pt-3 border-t border-stone-200/60 dark:border-stone-700/50 flex justify-between items-center">
                        <div className="flex items-center text-stone-600 dark:text-stone-300 font-medium text-sm">
                            <span className="text-bronze dark:text-gold mr-2"><Icons.Sparkles /></span>
                            {record.service}
                        </div>
                        <div className="font-bold text-stone-800 dark:text-stone-100">
                            {record.price ? `${record.price} ₸` : ''}
                        </div>
                    </div>

                    {/* Оверлей с кнопками (непрозрачный фон перекрывает время) */}
                    {showActions && (
                        <div className="absolute inset-y-0 right-0 flex items-center space-x-3 bg-white/98 dark:bg-stonebg/98 backdrop-blur-md px-5 pl-6 rounded-r-2xl border-l border-nude/40 dark:border-gold/20 shadow-[-15px_0_20px_rgba(255,255,255,0.9)] dark:shadow-[-15px_0_20px_rgba(10,10,10,0.9)] z-10" onClick={(e) => e.stopPropagation()}>
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

        const EditClientModal = ({ client, isOpen, onClose, onSave }) => {
            const [formData, setFormData] = useState({ id: '', name: '', phone: '', isInactive: false });

            useEffect(() => {
                if (isOpen && client) {
                    setFormData(client);
                }
            }, [isOpen, client]);

            if (!isOpen) return null;

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm transition-opacity">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden relative">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 bg-white/50 dark:bg-stonepanel/50">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">Профиль клиента</h2>
                            <button onClick={onClose} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 transition-colors text-stone-600 dark:text-stone-300">
                                <Icons.Close />
                            </button>
                        </div>
                        <form onSubmit={(e) => { e.preventDefault(); onSave(formData); }} className="p-5 space-y-4">
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Имя *</label>
                                <input required type="text" value={formData.name} onChange={e => setFormData({...formData, name: e.target.value})} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            <div>
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Телефон</label>
                                <input type="tel" value={formData.phone} onChange={e => setFormData({...formData, phone: e.target.value})} className="glass-input w-full px-4 py-3 rounded-xl" />
                            </div>
                            <div className="flex items-center mt-4 bg-white/50 dark:bg-stonepanel p-3 rounded-xl border border-nude/50 dark:border-gold/10">
                                <input type="checkbox" id="inactive" checked={formData.isInactive} onChange={e => setFormData({...formData, isInactive: e.target.checked})} className="mr-3 w-5 h-5 rounded border-stone-300 dark:border-stone-600 bg-white dark:bg-stonebg accent-bronze dark:accent-gold" />
                                <label htmlFor="inactive" className="text-stone-700 dark:text-stone-300 text-sm">Неактуальный клиент (в архив)</label>
                            </div>
                            <div className="pt-4">
                                <button type="submit" className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3.5 px-4 rounded-xl shadow-lg shadow-bronze/20 dark:shadow-gold/10 transform transition active:scale-95">
                                    Сохранить изменения
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            );
        };

        const AddModal = ({ initialData, clients, isOpen, onClose, onSave }) => {
            const [formData, setFormData] = useState({
                clientName: '', phone: '', date: todayString, time: '10:00', service: 'Маникюр + Гель-лак', price: ''
            });
            const [selectedPresets, setSelectedPresets] = useState(['Маникюр', 'Гель-лак']);
            const [customService, setCustomService] = useState('');
            const [showSuggestions, setShowSuggestions] = useState(false);

            useEffect(() => {
                if (isOpen) {
                    if (initialData) {
                        setFormData(initialData);
                        const parsed = parseService(initialData.service);
                        setSelectedPresets(parsed.presets);
                        setCustomService(parsed.custom);
                    } else {
                        setFormData({ clientName: '', phone: '', date: todayString, time: '10:00', service: 'Маникюр + Гель-лак', price: '' });
                        setSelectedPresets(['Маникюр', 'Гель-лак']);
                        setCustomService('');
                    }
                    setShowSuggestions(false);
                }
            }, [isOpen, initialData]);

            const updateService = (presets, custom) => {
                const service = buildService(presets, custom);
                setSelectedPresets(presets);
                setCustomService(custom);
                setFormData(prev => ({ ...prev, service }));
            };

            const togglePreset = (preset) => {
                const next = selectedPresets.includes(preset)
                    ? selectedPresets.filter(p => p !== preset)
                    : [...selectedPresets, preset];
                updateService(next, customService);
            };

            const handleServiceInput = (value) => {
                const parsed = parseService(value);
                setSelectedPresets(parsed.presets);
                setCustomService(parsed.custom);
                setFormData(prev => ({ ...prev, service: value }));
            };

            if (!isOpen) return null;

            const filteredClients = clients.filter(c => 
                !c.isInactive && 
                c.name.toLowerCase().includes(formData.clientName.toLowerCase())
            );

            const handleChange = (e) => {
                const { name, value } = e.target;
                setFormData(prev => ({ ...prev, [name]: value }));
            };

            return (
                <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-stone-900/40 dark:bg-black/70 backdrop-blur-sm transition-opacity">
                    <div className="glass-panel w-full max-w-md rounded-3xl shadow-2xl modal-enter overflow-hidden relative">
                        <div className="flex justify-between items-center p-5 border-b border-nude/50 dark:border-gold/20 bg-white/50 dark:bg-stonepanel/50">
                            <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">{initialData ? 'Редактировать запись' : 'Новая запись'}</h2>
                            <button onClick={onClose} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 transition-colors text-stone-600 dark:text-stone-300">
                                <Icons.Close />
                            </button>
                        </div>

                        <form onSubmit={(e) => { e.preventDefault(); onSave(formData); }} className="p-5 space-y-4">
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
                                                setFormData({...formData, clientName: c.name, phone: c.phone || formData.phone});
                                                setShowSuggestions(false);
                                            }}>
                                                <div className="font-medium">{c.name}</div>
                                                {c.phone && <div className="text-xs text-stone-500 dark:text-stone-400">{c.phone}</div>}
                                            </div>
                                        ))}
                                    </div>
                                )}
                            </div>
                            
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
                                <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Услуга</label>
                                <input type="text" name="service" value={formData.service} onChange={(e) => handleServiceInput(e.target.value)} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="Маникюр, Наращивание..." />
                                <div className="flex flex-wrap gap-2 mt-2.5">
                                    {SERVICE_PRESETS.map(preset => (
                                        <button
                                            key={preset}
                                            type="button"
                                            onClick={() => togglePreset(preset)}
                                            className={`px-3.5 py-1.5 rounded-full text-xs font-medium transition-all border ${
                                                selectedPresets.includes(preset)
                                                    ? 'bg-bronze text-white border-bronze dark:bg-gold/20 dark:text-gold dark:border-gold/40'
                                                    : 'bg-white/70 text-stone-600 border-nude/60 hover:border-bronze/40 dark:bg-stonepanel dark:text-stone-300 dark:border-gold/10 dark:hover:border-gold/30'
                                            }`}
                                        >
                                            {preset}
                                        </button>
                                    ))}
                                </div>
                            </div>

                            <div className="grid grid-cols-2 gap-4">
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Стоимость (₸)</label>
                                    <input type="number" name="price" value={formData.price} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="5000" />
                                </div>
                                <div>
                                    <label className="block text-sm font-medium text-stone-600 dark:text-stone-300 mb-1 ml-1">Телефон</label>
                                    <input type="tel" name="phone" value={formData.phone} onChange={handleChange} className="glass-input w-full px-4 py-3 rounded-xl placeholder-stone-400 dark:placeholder-stone-500" placeholder="+7..." />
                                </div>
                            </div>

                            <div className="pt-4">
                                <button type="submit" className="w-full bg-bronze dark:bg-gradient-to-r dark:from-gold dark:to-golddark text-white dark:text-stone-900 font-bold py-3.5 px-4 rounded-xl shadow-lg shadow-bronze/20 dark:shadow-gold/10 transform transition active:scale-95">
                                    {initialData ? 'Сохранить изменения' : 'Добавить запись'}
                                </button>
                            </div>
                        </form>
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
            const [isAllowed, setIsAllowed] = useState(false);
            const [accessChecked, setAccessChecked] = useState(false);
            const [authError, setAuthError] = useState('');
            const [signInLoading, setSignInLoading] = useState(false);
            const [dataLoading, setDataLoading] = useState(false);

            const [records, setRecords] = useState([]);
            const [clients, setClients] = useState([]);
            
            const [activeTab, setActiveTab] = useState('schedule');
            
            // Состояния расписания
            const [scheduleMode, setScheduleMode] = useState('upcoming'); 
            const [selectedDate, setSelectedDate] = useState(''); 
            const [scheduleSearch, setScheduleSearch] = useState('');
            
            const [clientSearch, setClientSearch] = useState('');
            
            const [isModalOpen, setIsModalOpen] = useState(false);
            const [editingRecord, setEditingRecord] = useState(null);
            
            const [isClientModalOpen, setIsClientModalOpen] = useState(false);
            const [editingClient, setEditingClient] = useState(null);
            const [isIncomeModalOpen, setIsIncomeModalOpen] = useState(false);

            // Тема: auto — по времени суток, light/dark — вручную
            const [themeMode, setThemeMode] = useState(() => {
                const saved = localStorage.getItem('manicureTheme');
                if (saved === 'light' || saved === 'dark' || saved === 'auto') return saved;
                return 'auto';
            });
            const effectiveTheme = themeMode === 'auto' ? getTimeBasedTheme() : themeMode;

            useEffect(() => {
                if (effectiveTheme === 'dark') {
                    document.documentElement.classList.add('dark');
                } else {
                    document.documentElement.classList.remove('dark');
                }
                localStorage.setItem('manicureTheme', themeMode);
            }, [effectiveTheme, themeMode]);

            const handleThemeToggle = () => setThemeMode(prev => cycleThemeMode(prev));

            useEffect(() => {
                const unsubscribe = auth.onAuthStateChanged(async (firebaseUser) => {
                    setUser(firebaseUser);
                    setAuthError('');

                    if (!firebaseUser) {
                        setIsAllowed(false);
                        setAccessChecked(true);
                        setRecords([]);
                        setClients([]);
                        setAuthLoading(false);
                        return;
                    }

                    setAccessChecked(false);
                    try {
                        const allowed = await checkUserAllowed(firebaseUser.email);
                        setIsAllowed(allowed);
                    } catch (e) {
                        console.error(e);
                        setAuthError('Не удалось проверить доступ. Попробуйте позже.');
                        setIsAllowed(false);
                    } finally {
                        setAccessChecked(true);
                        setAuthLoading(false);
                    }
                });

                return () => unsubscribe();
            }, []);

            const migrateLocalData = useCallback(async (uid) => {
                const existing = await userRecordsRef(uid).limit(1).get();
                if (!existing.empty) return;

                const localRecords = JSON.parse(localStorage.getItem('manicureRecordsDark') || '[]');
                const localClients = JSON.parse(localStorage.getItem('manicureClientsDark') || '[]');
                if (!localRecords.length && !localClients.length) return;

                const batch = db.batch();
                localRecords.forEach(r => batch.set(userRecordsRef(uid).doc(String(r.id)), r));
                localClients.forEach(c => batch.set(userClientsRef(uid).doc(String(c.id)), c));
                await batch.commit();
            }, []);

            useEffect(() => {
                if (!user || !isAllowed) return;

                let active = true;
                let unsubRecords = null;
                let unsubClients = null;
                setDataLoading(true);

                migrateLocalData(user.uid)
                    .catch(e => console.error('Migration error:', e))
                    .finally(() => {
                        if (!active) return;
                        unsubRecords = userRecordsRef(user.uid).onSnapshot(
                            snap => setRecords(snap.docs.map(d => d.data())),
                            err => console.error('Records sync error:', err)
                        );
                        unsubClients = userClientsRef(user.uid).onSnapshot(
                            snap => setClients(snap.docs.map(d => d.data())),
                            err => console.error('Clients sync error:', err)
                        );
                        setDataLoading(false);
                    });

                return () => {
                    active = false;
                    if (unsubRecords) unsubRecords();
                    if (unsubClients) unsubClients();
                };
            }, [user, isAllowed, migrateLocalData]);

            const handleGoogleSignIn = async () => {
                setSignInLoading(true);
                setAuthError('');
                try {
                    await auth.signInWithPopup(googleProvider);
                } catch (e) {
                    if (e.code !== 'auth/popup-closed-by-user') {
                        setAuthError('Не удалось войти. Попробуйте ещё раз.');
                    }
                } finally {
                    setSignInLoading(false);
                }
            };

            const handleSignOut = async () => {
                await auth.signOut();
            };

            const handleSaveRecord = async (recordData) => {
                if (!user) return;
                const id = editingRecord ? recordData.id : Date.now();
                const data = { ...recordData, id };

                await userRecordsRef(user.uid).doc(String(id)).set(data);

                const existingClient = clients.find(c => c.name.toLowerCase() === recordData.clientName.toLowerCase());
                if (!existingClient) {
                    const clientId = Date.now() + 1;
                    await userClientsRef(user.uid).doc(String(clientId)).set({
                        id: clientId,
                        name: recordData.clientName,
                        phone: recordData.phone || '',
                        isInactive: false
                    });
                } else if (recordData.phone && !existingClient.phone) {
                    await userClientsRef(user.uid).doc(String(existingClient.id)).update({ phone: recordData.phone });
                }

                setEditingRecord(null);
                setIsModalOpen(false);
            };

            const handleDeleteRecord = async (id) => {
                if (!user) return;
                if (window.confirm('Вы уверены, что хотите удалить эту запись?')) {
                    await userRecordsRef(user.uid).doc(String(id)).delete();
                }
            };

            const handleSaveClient = async (updatedClient) => {
                if (!user) return;
                const oldClient = clients.find(c => c.id === updatedClient.id);
                const oldName = oldClient ? oldClient.name : undefined;

                await userClientsRef(user.uid).doc(String(updatedClient.id)).set(updatedClient);

                if (oldName && (oldName !== updatedClient.name || (oldClient ? oldClient.phone : undefined) !== updatedClient.phone)) {
                    const related = records.filter(r => r.clientName === oldName);
                    const batch = db.batch();
                    related.forEach(r => {
                        batch.update(userRecordsRef(user.uid).doc(String(r.id)), {
                            clientName: updatedClient.name,
                            phone: updatedClient.phone
                        });
                    });
                    if (related.length) await batch.commit();
                }

                setIsClientModalOpen(false);
                setEditingClient(null);
            };

            // Обработка расписания
            const groupedRecords = useMemo(() => {
                let filtered = records;

                if (selectedDate) {
                    filtered = filtered.filter(r => r.date === selectedDate);
                } else {
                    if (scheduleMode === 'upcoming') {
                        filtered = filtered.filter(r => r.date >= todayString);
                    } else {
                        filtered = filtered.filter(r => r.date < todayString);
                    }
                }

                if (scheduleSearch) {
                    filtered = filtered.filter(r => 
                        r.clientName.toLowerCase().includes(scheduleSearch.toLowerCase()) ||
                        (r.service && r.service.toLowerCase().includes(scheduleSearch.toLowerCase()))
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
                    const client = clients.find(c => c.name === r.clientName);
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
                        c.name.toLowerCase().includes(clientSearch.toLowerCase()) ||
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

            if (!isAllowed) {
                return <AccessDeniedScreen email={user.email} onSignOut={handleSignOut} />;
            }

            return (
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
                            <div className="flex justify-end">
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
                                                    <AppointmentCard 
                                                        key={record.id} 
                                                        record={record} 
                                                        onEdit={() => { setEditingRecord(record); setIsModalOpen(true); }} 
                                                        onDelete={handleDeleteRecord} 
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
                                    <h2 className="text-xl font-bold text-stone-800 dark:text-stone-100">База</h2>
                                    <span className="text-sm font-medium text-stone-600 dark:text-stone-400 bg-white/60 dark:bg-stonepanel px-3 py-1 rounded-full border border-nude/50 dark:border-gold/10">{clientsWithStats.length} чел.</span>
                                </div>
                                
                                {clientsWithStats.map((client) => (
                                    <div key={client.id} className={`glass-panel rounded-2xl p-4 flex justify-between items-center transition-opacity ${client.isInactive ? 'opacity-50' : ''}`}>
                                        <div>
                                            <div className="flex items-center space-x-2">
                                                <h3 className="font-bold text-stone-800 dark:text-stone-100 text-lg">{client.name}</h3>
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
                                            <button onClick={() => { setEditingClient(client); setIsClientModalOpen(true); }} className="p-2 bg-white/60 dark:bg-white/5 rounded-full hover:bg-white/90 dark:hover:bg-white/10 text-stone-500 dark:text-stone-300 transition-colors border border-nude/30 dark:border-transparent">
                                                <Icons.Edit />
                                            </button>
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
                        onClose={() => { setIsModalOpen(false); setEditingRecord(null); }} 
                        onSave={handleSaveRecord} 
                    />

                    <EditClientModal
                        isOpen={isClientModalOpen}
                        client={editingClient}
                        onClose={() => { setIsClientModalOpen(false); setEditingClient(null); }}
                        onSave={handleSaveClient}
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
                                    onClick={() => { setEditingRecord(null); setIsModalOpen(true); }}
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
                                <span className="text-[11px] font-bold mt-1.5">База</span>
                            </button>
                            
                        </div>
                    </nav>

                </div>
            );
        };

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>