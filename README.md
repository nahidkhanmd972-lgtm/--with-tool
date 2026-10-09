<!DOCTYPE html>
<html lang="bn" class="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Nahid Multi-Verse — প্রফেশনাল এআই ড্যাশবোর্ড ও প্রবাসী সাপোর্ট</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        bdGreen: '#006A4E',
                        bdDarkGreen: '#004D38',
                        bdDeepEmerald: '#022C22',
                        bdLightMint: '#ECFDF5',
                        bdSoftMint: '#D1FAE5',
                        bdRed: '#E11D48',
                        bdSoftRose: '#FFE4E6',
                        skOrange: '#EA7614',
                        surfaceWarm: '#F8FAFC',
                        cardBorder: '#E2E8F0'
                    },
                    fontFamily: {
                        bengali: ['"Hind Siliguri"', '"Plus Jakarta Sans"', 'sans-serif'],
                        sans: ['"Plus Jakarta Sans"', '"Hind Siliguri"', 'sans-serif']
                    },
                    boxShadow: {
                        'card': '0 4px 20px -2px rgba(15, 23, 42, 0.05), 0 2px 6px -1px rgba(15, 23, 42, 0.03)',
                        'card-hover': '0 12px 28px -4px rgba(0, 106, 78, 0.12), 0 4px 10px -2px rgba(15, 23, 42, 0.05)',
                        'elevated': '0 10px 30px -5px rgba(0, 77, 56, 0.16), 0 4px 12px -2px rgba(15, 23, 42, 0.06)',
                        'glow-emerald': '0 0 20px -2px rgba(16, 185, 129, 0.25)'
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Leaflet.js Interactive Map -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
    <!-- jsPDF for NID/Passport/Image to PDF -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <!-- QRCode.js Lightweight Library for Profile Links & Document References -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <!-- Custom CSS File -->
    <link rel="stylesheet" href="style.css">
</head>
<body class="min-h-screen transition-colors duration-300">

    <!-- ===================================================================== -->
    <!-- MANDATORY STEP 1 & STEP 2 GATEWAY:                                    -->
    <!-- 1) LANGUAGE SELECTION (বাংলা / ENGLISH)                                -->
    <!-- 2) REGISTRATION WITH PASSWORD + GOOGLE BEFORE SHOWING DASHBOARD       -->
    <!-- ===================================================================== -->
    <div id="registration-gateway-overlay" class="fixed inset-0 z-50 bg-gradient-to-b from-[#004D38] via-[#006A4E] to-[#022c22] overflow-y-auto flex items-center justify-center p-4">

        <!-- STEP 1: LANGUAGE SELECTION CARD (বাংলা / ENGLISH) -->
        <div id="gateway-step-lang" class="w-full max-w-md bg-white dark:bg-slate-900 rounded-[32px] p-6 shadow-2xl border-2 border-emerald-400/30 text-center space-y-5">
            <!-- Top 1-Week Launch Notice Banner on Gateway -->
            <div class="bg-gradient-to-r from-[#EA7614] via-[#F42A41] to-[#006A4E] text-white rounded-2xl p-2.5 shadow-md text-[11px] font-extrabold leading-relaxed">
                📢 আমাদের এই সব ফিউচারগুলো এক সপ্তাহের ভিতরে সবকিছু চালু হতে যাচ্ছে আপনারা আমাদের সাথেই থাকুন এবং আমাদেরকে সাপোর্ট করুন ❤️
            </div>

            <div class="w-24 h-24 rounded-full bg-gradient-to-br from-[#006A4E] to-[#004D38] mx-auto p-1 shadow-xl border-2 border-amber-400 overflow-hidden flex items-center justify-center">
                <img src="https://user42641.na.imgto.link/public/20261009/fef3654d712b69431e85593b-1000463415.avif"
                    alt="Nahid Multi-Verse Logo"
                    onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';"
                    class="w-full h-full object-cover rounded-full">
                <div style="display:none" class="w-16 h-16 rounded-full bg-[#F42A41] items-center justify-center text-white text-2xl font-extrabold shadow">
                    NM
                </div>
            </div>

            <div class="space-y-1">
                <span class="bg-amber-100 text-amber-800 text-[11px] font-extrabold px-3 py-1 rounded-full">
                    🌟 Nahid Multi-Verse-এ আপনাদের স্বাগতম
                </span>
                <h1 class="text-2xl font-extrabold text-slate-900 dark:text-white pt-1">
                    Nahid Multi-Verse
                </h1>
                <p class="text-xs text-slate-500">
                    চালিয়ে যেতে প্রথমে আপনার ভাষা নির্বাচন করুন / Please select your language first
                </p>
            </div>

            <div class="grid grid-cols-2 gap-3.5 pt-2">
                <button type="button" onclick="selectGatewayLanguage('bn')"
                    class="bg-[#006A4E] hover:bg-[#004D38] text-white rounded-2xl py-4 px-3 shadow-lg flex flex-col items-center justify-center gap-1.5 border-2 border-[#006A4E] transition transform active:scale-95">
                    <span class="text-2xl">🇧🇩</span>
                    <span class="text-base font-extrabold">বাংলা</span>
                    <span class="text-[10px] text-emerald-100">বাংলা ভাষায় প্রবেশ করুন</span>
                </button>

                <button type="button" onclick="selectGatewayLanguage('en')"
                    class="bg-[#F42A41] hover:bg-rose-700 text-white rounded-2xl py-4 px-3 shadow-lg flex flex-col items-center justify-center gap-1.5 border-2 border-[#F42A41] transition transform active:scale-95">
                    <span class="text-2xl">🇬🇧</span>
                    <span class="text-base font-extrabold">ENGLISH</span>
                    <span class="text-[10px] text-rose-100">Continue in English</span>
                </button>
            </div>

            <p class="text-[11px] text-slate-400 pt-1">
                একবার ভাষা সিলেক্ট ও রেজিস্ট্রেশন/লগইন করলে আজীবন সচল থাকবে — বারবার লগইন করতে হবে না।
            </p>

            <!-- About Nahid Multi-Verse & Firebase Cloud Security Info Card -->
            <div class="pt-3 border-t border-slate-100 dark:border-slate-800 text-left space-y-2">
                <div class="bg-emerald-50/90 dark:bg-slate-800/90 rounded-2xl p-3 border border-emerald-200/70 dark:border-emerald-800/50 space-y-1.5">
                    <div class="flex items-center justify-between">
                        <span class="text-[11px] font-extrabold text-[#004D38] dark:text-emerald-300 flex items-center gap-1.5">
                            <i class="fa-solid fa-shield-halved text-[#006A4E]"></i>
                            <span>আমাদের সম্পর্কে ও সেবা পরিচিতি</span>
                        </span>
                        <span class="bg-[#006A4E] text-white text-[9px] font-extrabold px-2 py-0.5 rounded-full">
                            Play Store Ready
                        </span>
                    </div>
                    <p class="text-[11px] text-slate-600 dark:text-slate-300 leading-relaxed">
                        <b>Nahid Multi-Verse</b> মালয়েশিয়া ও বাংলাদেশ প্রবাসীদের জন্য একটি পূর্ণাঙ্গ অফিশিয়াল ডিজিটাল প্ল্যাটফর্ম। এখানে মালয়েশিয়া ভিসা ও পাসপোর্ট চেক, FOMEMA মেডিকেল, এআই চ্যাটবট, এআই ফটো স্টুডিও এবং ৬৪ জেলার প্রবাসী সেবা এক জায়গায় পাবেন।
                    </p>
                    <div class="flex flex-wrap items-center gap-1.5 pt-1">
                        <span class="bg-white dark:bg-slate-900 text-[#006A4E] dark:text-emerald-400 text-[10px] font-bold px-2 py-0.5 rounded-lg border border-emerald-200/60">☁️ Firebase Cloud Sync</span>
                        <span class="bg-white dark:bg-slate-900 text-amber-700 dark:text-amber-400 text-[10px] font-bold px-2 py-0.5 rounded-lg border border-amber-200/60">🔑 অটো-লগইন সচল</span>
                        <span class="bg-white dark:bg-slate-900 text-rose-600 dark:text-rose-400 text-[10px] font-bold px-2 py-0.5 rounded-lg border border-rose-200/60">🔒 Anti-Copy Protected</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- STEP 2: MANDATORY REGISTRATION FORM -->
        <div id="gateway-step-reg" class="hidden w-full max-w-md bg-white dark:bg-slate-900 rounded-[32px] p-5 shadow-2xl border-2 border-emerald-400/40 space-y-3.5 my-auto">
            <div class="bg-[#EA7614] text-white rounded-2xl px-3 py-2 text-[11px] font-extrabold text-center shadow-sm">
                🚀 আমাদের এই সব ফিউচারগুলো এক সপ্তাহের ভিতরে সবকিছু চালু হতে যাচ্ছে আপনারা আমাদের সাথেই থাকুন এবং আমাদেরকে সাপোর্ট করুন!
            </div>
            <div class="flex items-center justify-between">
                <button type="button" onclick="backToLanguageStep()" class="text-xs font-extrabold text-[#006A4E] flex items-center gap-1">
                    <i class="fa-solid fa-arrow-left"></i> <span id="gateBackBtnText">ভাষা পরিবর্তন</span>
                </button>
                <div class="flex items-center gap-2">
                    <img src="https://user42641.na.imgto.link/public/20261009/fef3654d712b69431e85593b-1000463415.avif" alt="Logo" class="w-7 h-7 rounded-full object-cover border border-amber-400">
                    <span id="gateSelectedLangBadge" class="bg-[#E6F4F0] text-[#004D38] text-[11px] font-extrabold px-3 py-1 rounded-full">
                        🇧🇩 বাংলা নির্বাচিত
                    </span>
                </div>
            </div>

            <div class="text-center space-y-1">
                <h2 id="gateTitle" class="text-xl font-extrabold text-slate-900 dark:text-white">
                    স্বাগতম! রেজিস্ট্রেশন সম্পন্ন করুন
                </h2>
                <p id="gateSub" class="text-xs text-slate-500">
                    মূল ওয়েবসাইট ও নাহিদ এআই ড্যাশবোর্ডে প্রবেশ করতে নিচের তথ্য ও পাসওয়ার্ড দিন
                </p>
            </div>

            <!-- Google Connect Button -->
            <button type="button" onclick="connectGoogleAccount()"
                class="w-full flex items-center justify-center gap-2.5 bg-white dark:bg-slate-800 border-2 border-slate-200 dark:border-slate-700 hover:border-[#006A4E] rounded-2xl py-3 px-4 text-slate-800 dark:text-white text-xs font-extrabold transition shadow-sm">
                <i class="fa-brands fa-google text-[#F42A41] text-base"></i>
                <span id="googleBtnLabel">গুগল দিয়ে সাইন-ইন / কানেক্ট করুন</span>
            </button>

            <form id="home-reg-form" class="space-y-2.5">
                <input type="text" id="regNameInput" required placeholder="আপনার পূর্ণ নাম (Full Name) *"
                    class="w-full px-4 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-semibold outline-none focus:border-[#006A4E]">

                <input type="email" id="regGoogleEmailInput" required placeholder="আপনার গুগল জিমেইল (yourname@gmail.com) *"
                    class="w-full px-4 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-semibold outline-none focus:border-[#006A4E]">

                <input type="tel" id="regPhoneInput" required placeholder="মোবাইল বা হোয়াটসঅ্যাপ নম্বর (Phone Number) *"
                    class="w-full px-4 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-semibold outline-none focus:border-[#006A4E]">

                <input type="password" id="regPasswordInput" required minlength="4" placeholder="গোপন পাসওয়ার্ড দিন (কমপক্ষে ৪ অক্ষর - বাধ্যতামূলক) *"
                    class="w-full px-4 py-3 rounded-2xl border border-rose-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-semibold outline-none focus:border-[#006A4E]">

                <!-- Country Selector -->
                <div class="space-y-1.5">
                    <label id="regCountryLabel" class="block text-[11px] font-extrabold text-slate-600 dark:text-slate-300 text-left px-1">
                        আপনি কোন দেশ বা স্থান থেকে রেজিস্ট্রেশন করছেন? *
                    </label>
                    <div class="grid grid-cols-2 gap-2">
                        <button type="button" id="countryBtnMalaysia" onclick="selectRegCountry('MY')"
                            class="py-2.5 px-3 rounded-2xl border-2 border-[#006A4E] bg-[#006A4E] text-white text-xs font-extrabold flex items-center justify-center gap-1.5 shadow-sm transition">
                            <span>🇲🇾</span>
                            <span>মালয়েশিয়া (Malaysia)</span>
                        </button>
                        <button type="button" id="countryBtnBangladesh" onclick="selectRegCountry('BD')"
                            class="py-2.5 px-3 rounded-2xl border-2 border-slate-200 dark:border-slate-700 bg-slate-50 dark:bg-slate-800 text-slate-700 dark:text-slate-200 text-xs font-extrabold flex items-center justify-center gap-1.5 transition">
                            <span>🇧🇩</span>
                            <span>ঢাকা (বাংলাদেশ)</span>
                        </button>
                    </div>
                </div>

                <!-- State/Division & District Selection -->
                <div class="grid grid-cols-2 gap-2">
                    <select id="regDivisionSelect" onchange="populateRegDistricts()" required
                        class="w-full px-3 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-bold outline-none focus:border-[#006A4E]">
                    </select>
                    <select id="regDistrictSelect" required
                        class="w-full px-3 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-bold outline-none focus:border-[#006A4E]">
                    </select>
                </div>

                <input type="text" id="regVillageInput" required placeholder="মালয়েশিয়ার এলাকা / কোম্পানি বা বাংলাদেশের গ্রামের নাম *"
                    class="w-full px-4 py-3 rounded-2xl border border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-xs font-semibold outline-none focus:border-[#006A4E]">

                <div id="regErrorBanner" class="hidden bg-[#FFE4E8] border border-[#F42A41] text-[#F42A41] rounded-2xl p-2.5 text-center text-xs font-extrabold"></div>

                <button type="submit" id="homeRegSubmitBtn"
                    class="w-full bg-[#006A4E] hover:bg-[#004D38] text-white font-extrabold py-3.5 rounded-2xl shadow-lg text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-right-to-bracket"></i>
                    <span id="regSubmitBtnLabel">রেজিস্ট্রেশন সম্পন্ন করে ওয়েবসাইটে প্রবেশ করুন</span>
                </button>
            </form>
        </div>
    </div>

    <!-- ===================================================================== -->
    <!-- MAIN WEBSITE & NAHID AI DASHBOARD (LOCKED UNTIL REGISTERED)           -->
    <!-- ===================================================================== -->
    <div id="main-website-wrapper" class="hidden">

        <!-- 1. TOP BANNERS & BRAND HEADER -->
        <div class="sticky top-0 z-40 shadow-sm backdrop-blur-md bg-white/90 dark:bg-slate-900/90">
            <div id="topPromoBanner" class="bg-gradient-to-r from-[#022C22] via-[#004D38] to-[#006A4E] text-white px-4 py-2 flex items-center justify-between gap-3 border-b border-emerald-500/20">
                <div class="flex items-center gap-2 overflow-hidden">
                    <span class="inline-flex items-center justify-center w-5 h-5 rounded-full bg-amber-400/20 text-amber-300 text-xs shrink-0">📢</span>
                    <div class="overflow-hidden whitespace-nowrap">
                        <span id="liveTickerText" class="ticker-marquee text-xs font-semibold tracking-wide text-emerald-50">
                            আমাদের এই সব ফিউচারগুলো এক সপ্তাহের ভিতরে সবকিছু চালু হতে যাচ্ছে আপনারা আমাদের সাথেই থাকুন এবং আমাদেরকে সাপোর্ট করুন • Nahid Multi-Verse — প্রফেশনাল এআই ড্যাশবোর্ড ও প্রবাসী সাপোর্ট!
                        </span>
                    </div>
                </div>
                <button onclick="openAdminModal()" class="bg-white/15 hover:bg-white/25 text-white text-[11px] font-bold px-3 py-1 rounded-full shrink-0 flex items-center gap-1 border border-white/15 transition">
                    <span>নোটিশ</span> <i class="fa-solid fa-arrow-right text-[10px]"></i>
                </button>
            </div>

            <!-- Brand Header Bar -->
            <div class="max-w-lg mx-auto px-4 py-3 flex items-center justify-between border-b border-slate-200/70 dark:border-slate-800/80">
                <div class="flex items-center gap-3">
                    <div onclick="handleLogoTap()" class="w-11 h-11 rounded-2xl bg-gradient-to-br from-[#006A4E] to-[#004D38] p-0.5 flex items-center justify-center shadow-card cursor-pointer ring-2 ring-amber-400/80 overflow-hidden shrink-0 transition transform active:scale-95">
                        <img src="https://user42641.na.imgto.link/public/20261009/fef3654d712b69431e85593b-1000463415.avif"
                            alt="Nahid Multi-Verse Logo"
                            onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';"
                            class="w-full h-full object-cover rounded-[14px]">
                        <i style="display:none" class="fa-solid fa-wand-magic-sparkles text-white text-base"></i>
                    </div>
                    <div>
                        <div class="flex items-center gap-1.5">
                            <span id="headerAppTitle" class="text-lg font-extrabold tracking-tight text-slate-900 dark:text-white leading-none">Nahid</span>
                            <span class="text-lg font-extrabold tracking-tight text-amber-500 leading-none">Multi-Verse</span>
                        </div>
                        <p id="headerAppSub" class="text-[10px] font-bold tracking-widest text-slate-500 dark:text-slate-400 uppercase mt-1">প্রবাসী সাপোর্ট • NAHID MULTI-VERSE</p>
                    </div>
                </div>

                <div class="flex items-center gap-2">
                    <button onclick="openQrGeneratorModal()" title="QR Code Generator" class="bg-emerald-50 dark:bg-emerald-950/60 text-[#006A4E] dark:text-emerald-300 hover:bg-[#006A4E] hover:text-white w-9 h-9 rounded-xl text-xs font-bold flex items-center justify-center transition shadow-sm border border-emerald-200/80 dark:border-emerald-800/60">
                        <i class="fa-solid fa-qrcode text-sm"></i>
                    </button>

                    <div class="bg-amber-50/90 dark:bg-slate-800 text-amber-900 dark:text-amber-300 px-3 py-1.5 rounded-xl text-xs font-extrabold flex items-center gap-1.5 border border-amber-200/80 dark:border-slate-700 shadow-sm">
                        <i class="fa-solid fa-coins text-amber-500"></i>
                        <span id="user-credits">100</span>
                    </div>

                    <button onclick="toggleAppLanguage()" class="bg-slate-900 dark:bg-slate-800 hover:bg-slate-800 text-white font-extrabold text-[11px] px-2.5 py-1.5 rounded-xl shadow-sm border border-slate-700/60 transition">
                        <span id="langToggleText">EN</span>
                    </button>

             
