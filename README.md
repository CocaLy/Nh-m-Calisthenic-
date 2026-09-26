<!DOCTYPE html>
<html lang="vi" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bio Link Calisthenics - Hướng Dẫn & Addon Tập Luyện</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        tiktok: {
                            cyan: '#25F4EE',
                            pink: '#FE2C55',
                            dark: '#121212',
                            card: '#1E1E24',
                            border: '#2A2A35'
                        }
                    },
                    animation: {
                        'pulse-glow': 'pulseGlow 2s infinite',
                        'float': 'float 3s ease-in-out infinite',
                    },
                    keyframes: {
                        pulseGlow: {
                            '0%, 100%': { boxShadow: '0 0 15px rgba(254, 44, 85, 0.4)' },
                            '50%': { boxShadow: '0 0 25px rgba(37, 244, 238, 0.6)' },
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-6px)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #0d0d11;
            color: #f3f4f6;
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-image: 
                radial-gradient(at 10% 10%, rgba(254, 44, 85, 0.12) 0px, transparent 50%),
                radial-gradient(at 90% 90%, rgba(37, 244, 238, 0.12) 0px, transparent 50%);
            background-attachment: fixed;
        }

        .glass-card {
            background: rgba(26, 26, 36, 0.85);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card:hover {
            border-color: rgba(37, 244, 238, 0.3);
        }

        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #121212;
        }
        ::-webkit-scrollbar-thumb {
            background: #333344;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #FE2C55;
        }

        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }

        .badge-pulse {
            position: relative;
        }
        .badge-pulse::after {
            content: '';
            position: absolute;
            top: -2px; left: -2px; right: -2px; bottom: -2px;
            border-radius: 9999px;
            background: linear-gradient(45deg, #FE2C55, #25F4EE);
            z-index: -1;
            opacity: 0.7;
            filter: blur(4px);
        }

        /* Modal display rule with highest priority */
        .custom-modal {
            display: none !important;
            opacity: 0;
            transition: opacity 0.25s ease-in-out;
        }
        .custom-modal.active {
            display: flex !important;
            opacity: 1;
        }
    </style>
</head>
<body class="min-h-screen pb-12 flex flex-col items-center justify-start px-4 sm:px-6">

    <div id="toast" class="fixed top-5 z-50 transform -translate-y-20 opacity-0 transition-all duration-300 ease-out bg-gray-900 border border-tiktok-cyan/40 text-white px-5 py-3 rounded-xl shadow-2xl flex items-center space-x-3 pointer-events-none">
        <i class="fa-solid fa-circle-check text-tiktok-cyan text-lg"></i>
        <span id="toast-message" class="text-sm font-medium">Đã sao chép liên kết!</span>
    </div>

    <main class="w-full max-w-md mx-auto pt-8 flex flex-col items-center">

        <div class="text-center mb-6 flex flex-col items-center w-full">
            <div class="relative mb-3">
                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-full p-1 badge-pulse bg-gradient-to-tr from-tiktok-pink via-purple-500 to-tiktok-cyan overflow-hidden shadow-xl">
                    <img id="userAvatar"
                         src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?q=80&w=400&auto=format&fit=crop" 
                         alt="David Laid Discipline Avatar" 
                         class="w-full h-full object-cover object-center rounded-full"
                         onerror="this.src='https://placehold.co/200x200/1e1e24/25f4ee?text=CALI'">
                </div>
                <div class="absolute bottom-0 right-1 bg-tiktok-cyan text-gray-900 rounded-full w-6 h-6 flex items-center justify-center text-xs font-bold border-2 border-gray-900">
                    <i class="fa-solid fa-check"></i>
                </div>
            </div>

            <h1 class="text-xl sm:text-2xl font-extrabold tracking-tight flex items-center gap-2">
                Nhóm Calisthenic💪
            </h1>

            <p class="text-xs sm:text-sm text-gray-400 mt-2.5 max-w-xs leading-relaxed px-2">
                💪 Tổng hợp Lịch tập, Hướng dẫn từng nhóm cơ, Lộ Trình Cho Người Mới & Shop Dụng Cụ Shopee
            </p>

            <div class="flex items-center gap-6 mt-4 py-2 px-6 rounded-2xl bg-gray-900/60 border border-gray-800/80 text-xs">
                <div class="text-center">
                    <span class="font-bold text-white block">100%</span>
                    <span class="text-gray-400 text-[10px]">Free Clip</span>
                </div>
                <div class="w-px h-6 bg-gray-800"></div>
                <div class="text-center">
                    <span class="font-bold text-white block text-tiktok-pink">Shopee</span>
                    <span class="text-gray-400 text-[10px]">Voucher</span>
                </div>
            </div>
        </div>

        <div class="w-full space-y-3.5" id="linksContainer">

            <!-- LINK 1: Lịch Tập Hàng Tuần -->
            <div class="link-item group">
                <button type="button" onclick="openModal('scheduleModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-tiktok-cyan cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-tiktok-cyan/10 text-tiktok-cyan flex items-center justify-center text-lg font-bold group-hover:bg-tiktok-cyan group-hover:text-gray-900 transition-colors">
                            <i class="fa-regular fa-calendar-check"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Lịch Tập Hàng Tuần ( T2 - CN )
                                <span class="bg-tiktok-cyan/20 text-tiktok-cyan text-[10px] px-1.5 py-0.5 rounded font-mono">Chi tiết</span>
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Phân chia nhóm cơ theo ngày & Cardio sáng</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 2: Thư Viện Bài Tập Theo Nhóm Cơ -->
            <div class="link-item group">
                <button type="button" onclick="openModal('exercisesModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-tiktok-pink cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-tiktok-pink/10 text-tiktok-pink flex items-center justify-center text-lg font-bold group-hover:bg-tiktok-pink group-hover:text-white transition-colors">
                            <i class="fa-solid fa-dumbbell"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Thư Viện Bài Tập & TikTok Video
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Ngực, Vai, Tay Sau, Lưng Xô, Bụng, Chân</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 3: Bài Tập Cardio Đốt Mỡ -->
            <div class="link-item group">
                <button type="button" onclick="openModal('cardioModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-amber-500 cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center text-lg font-bold group-hover:bg-amber-500 group-hover:text-gray-900 transition-colors">
                            <i class="fa-solid fa-fire-flame-curved"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Bài Tập Cardio Đốt Mỡ
                                <span class="bg-amber-500/20 text-amber-300 text-[10px] px-1.5 py-0.5 rounded">Sáng sớm</span>
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Video hướng dẫn chuẩn lúc chưa ăn sáng</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 4: Lộ Trình Hỗ Trợ Người Mới -->
            <div class="link-item group">
                <button type="button" onclick="openModal('beginnerModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-amber-400 cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-amber-400/10 text-amber-400 flex items-center justify-center text-lg font-bold group-hover:bg-amber-400 group-hover:text-gray-900 transition-colors">
                            <i class="fa-solid fa-graduation-cap"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Mở Khóa Hít Đất & Kéo Xà
                                <span class="bg-amber-400/20 text-amber-300 text-[10px] px-1.5 py-0.5 rounded">Người Mới</span>
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Lộ trình 6 ngày Push up & 4 Level Pull up</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 5: Cửa Hàng Dụng Cụ & Voucher -->
            <div class="link-item group">
                <button type="button" onclick="openModal('shopModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-emerald-400 cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-emerald-400/10 text-emerald-400 flex items-center justify-center text-lg font-bold group-hover:bg-emerald-400 group-hover:text-gray-900 transition-colors">
                            <i class="fa-solid fa-cart-shopping"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Link Mua Dụng Cụ Shopee
                                <span class="bg-emerald-500/20 text-emerald-300 text-[10px] px-1.5 py-0.5 rounded">Tạ / Xà / Dây</span>
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Xà đơn, Tạ đơn, Dây kháng lực combo</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 6: Bảng Chỉ Số Cá Nhân & BMI Calculator -->
            <div class="link-item group">
                <button type="button" onclick="openModal('bmiModal')" 
                        class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-purple-400 cursor-pointer">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-purple-400/10 text-purple-400 flex items-center justify-center text-lg font-bold group-hover:bg-purple-400 group-hover:text-white transition-colors">
                            <i class="fa-solid fa-calculator"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Bảng Chỉ Số Nhóm & Máy Tính BMI
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Dữ liệu Nhân, Bảo, Phát, Ngọc, Toàn, Thịnh</p>
                        </div>
                    </div>
                    <i class="fa-solid fa-chevron-right text-gray-500 text-xs group-hover:text-white group-hover:translate-x-1 transition"></i>
                </button>
            </div>

            <!-- LINK 7: Video Giãn Cơ Direct Link -->
            <div class="link-item group">
                <div class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left border-l-4 border-l-sky-400">
                    <div class="flex items-center space-x-3.5">
                        <div class="w-11 h-11 rounded-xl bg-sky-400/10 text-sky-400 flex items-center justify-center text-lg font-bold group-hover:bg-sky-400 group-hover:text-gray-900 transition-colors">
                            <i class="fa-solid fa-person-stretching"></i>
                        </div>
                        <div>
                            <div class="font-bold text-sm text-white flex items-center gap-1.5">
                                Video Giãn Cơ Sau Khi Tập
                                <i class="fa-brands fa-tiktok text-tiktok-cyan text-xs"></i>
                            </div>
                            <p class="text-xs text-gray-400 mt-0.5">Hướng dẫn chi tiết trên TikTok</p>
                        </div>
                    </div>
                    <div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbLND74V/')" class="px-3 py-2 bg-sky-500/20 text-sky-300 border border-sky-500/30 hover:bg-sky-500 hover:text-gray-900 text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>
            </div>

        </div>

        <footer class="mt-10 text-center text-xs text-gray-500 space-y-2">
            <p>© 2026 Calisthenics TikTok Bio Hub. Mọi video thuộc chủ sở hữu TikTok.</p>
            <p class="text-[11px] text-gray-600">Nhấn vào từng mục để xem hướng dẫn chi tiết & lịch tập chuẩn.</p>
        </footer>

    </main>


    <!-- ==================== MODALS SECTION ==================== -->

    <div id="scheduleModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900/90 sticky top-0">
                <div class="flex items-center gap-2">
                    <i class="fa-regular fa-calendar-check text-tiktok-cyan"></i>
                    <h3 class="font-bold text-white text-base">Lịch Tập Hàng Tuần</h3>
                </div>
                <button type="button" onclick="closeModal('scheduleModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            
            <div class="p-4 overflow-y-auto space-y-3">
                <div class="p-3 bg-tiktok-cyan/10 border border-tiktok-cyan/20 rounded-xl text-xs text-tiktok-cyan flex items-center gap-2">
                    <i class="fa-solid fa-lightbulb text-sm"></i>
                    <span><strong>Cardio:</strong> Khuyên dùng nên tập lúc chưa ăn sáng để tối ưu đốt mỡ!</span>
                </div>

                <div class="grid grid-cols-1 gap-2.5">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-tiktok-cyan text-sm w-12">Thứ 2</span>
                        <span class="text-sm text-gray-200 font-semibold">Ngực, Vai, Tay sau</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 1</span>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-tiktok-pink text-sm w-12">Thứ 3</span>
                        <span class="text-sm text-gray-200 font-semibold">Lưng - xô, Tay trước</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 2</span>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-amber-400 text-sm w-12">Thứ 4</span>
                        <span class="text-sm text-gray-200 font-semibold">Bụng, Chân</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 3</span>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-tiktok-cyan text-sm w-12">Thứ 5</span>
                        <span class="text-sm text-gray-200 font-semibold">Ngực, Vai, Tay sau</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 4</span>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-tiktok-pink text-sm w-12">Thứ 6</span>
                        <span class="text-sm text-gray-200 font-semibold">Lưng - xô, Tay trước</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 5</span>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/50 flex justify-between items-center">
                        <span class="font-bold text-amber-400 text-sm w-12">Thứ 7</span>
                        <span class="text-sm text-gray-200 font-semibold">Bụng, Chân</span>
                        <span class="text-[10px] bg-gray-700 text-gray-300 px-2 py-1 rounded-full">Buổi 6</span>
                    </div>
                    <div class="p-3.5 bg-emerald-500/10 rounded-xl border border-emerald-500/30 flex justify-between items-center">
                        <span class="font-bold text-emerald-400 text-sm w-12">Chủ Nhật</span>
                        <span class="text-sm text-emerald-300 font-semibold">Nghỉ Ngơi / Giãn Cơ</span>
                        <span class="text-[10px] bg-emerald-500/20 text-emerald-300 px-2 py-1 rounded-full">Rest</span>
                    </div>
                </div>
            </div>
            <div class="p-4 border-t border-gray-800 bg-gray-900">
                <button type="button" onclick="closeModal('scheduleModal')" class="w-full py-3 bg-gray-800 text-gray-200 font-bold rounded-xl text-xs hover:bg-gray-700 cursor-pointer">Đóng</button>
            </div>
        </div>
    </div>

    <div id="exercisesModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-xl rounded-t-3xl sm:rounded-3xl max-h-[90vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900 sticky top-0 z-10">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-dumbbell text-tiktok-pink"></i>
                    <h3 class="font-bold text-white text-base">Thư Viện Bài Tập & Link Clip</h3>
                </div>
                <button type="button" onclick="closeModal('exercisesModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div class="flex overflow-x-auto gap-2 p-3 bg-gray-950 border-b border-gray-800 no-scrollbar relative z-20 touch-pan-x">
                <button type="button" onclick="switchTab('nguc')" id="tab-nguc" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-tiktok-pink text-white shadow-lg shadow-tiktok-pink/20 transition-all active:scale-95 cursor-pointer">Ngực</button>
                <button type="button" onclick="switchTab('vai')" id="tab-vai" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Vai</button>
                <button type="button" onclick="switchTab('taysau')" id="tab-taysau" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Tay Sau</button>
                <button type="button" onclick="switchTab('lungxo')" id="tab-lungxo" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Lưng - Xô</button>
                <button type="button" onclick="switchTab('taytruoc')" id="tab-taytruoc" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Tay Trước</button>
                <button type="button" onclick="switchTab('bung')" id="tab-bung" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Bụng (Tà đạo)</button>
                <button type="button" onclick="switchTab('chan')" id="tab-chan" class="tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer">Chân</button>
            </div>

            <div class="p-4 overflow-y-auto space-y-3 flex-1">
                <!-- NGỰC -->
                <div id="content-nguc" class="tab-content space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Push up (Hít đất chuẩn)</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">20 Reps × 3 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdgdaPs/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>

                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Push up dốc đứng</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">20 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdgdaPs/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>

                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Push up dốc xuống</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">10 Reps × 2 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdgdaPs/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- VAI -->
                <div id="content-vai" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Bài Vai Trước</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdtH3kU/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Bài Vai Giữa</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdtH3kU/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Bài Vai Sau</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdtH3kU/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- TAY SAU -->
                <div id="content-taysau" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Diamond Push Up</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">15 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdc4K1r/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Triceps Extension</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">15 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdc4K1r/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- LƯNG XÔ -->
                <div id="content-lungxo" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Pull up (Kéo xà)</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">5 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdTWWHe/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Chin up (Kéo xà ngửa tay)</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">8 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdTWWHe/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- TAY TRƯỚC -->
                <div id="content-taytruoc" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Tay trước - Bài 1 & 2</h4>
                            <p class="text-xs text-gray-400 mt-1">Nâng lên 2-3s rồi hạ xuống 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdwqyVq/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- BỤNG -->
                <div id="content-bung" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Bụng (Tà đạo) - Bài 1, 2 & 3</h4>
                            <p class="text-xs text-gray-400 mt-1">Gập lại 2-3s rồi thả ra 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbdKYGDW/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

                <!-- CHÂN -->
                <div id="content-chan" class="tab-content hidden space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-800 flex justify-between items-center gap-2">
                        <div>
                            <h4 class="font-bold text-white text-sm">Chân - Bài 1, 2, 3, 4</h4>
                            <p class="text-xs text-gray-400 mt-1">Hạ 2-3s rồi nâng lên 1s</p>
                            <span class="inline-block mt-1 text-[11px] font-mono text-tiktok-cyan font-semibold">10-25 Reps × 4 Sets</span>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSb8pKXxT/')" class="px-3 py-2 bg-tiktok-pink/20 text-tiktok-pink border border-tiktok-pink/30 hover:bg-tiktok-pink hover:text-white text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </div>

    <div id="cardioModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900 sticky top-0">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-fire-flame-curved text-amber-400"></i>
                    <h3 class="font-bold text-white text-base">Bài Tập Cardio Đốt Mỡ</h3>
                </div>
                <button type="button" onclick="closeModal('cardioModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div class="p-4 overflow-y-auto space-y-3">
                <div class="p-3.5 bg-amber-500/10 border border-amber-500/30 rounded-xl flex items-center justify-between gap-2">
                    <div>
                        <h4 class="font-bold text-amber-300 text-sm">Bài Tập Cardio Đốt Mỡ Sớm</h4>
                        <p class="text-xs text-gray-400 mt-1">Khuyên dùng tập lúc chưa ăn sáng để tối ưu đốt mỡ thừa</p>
                        <span class="inline-block mt-1 text-[10px] bg-amber-400/20 text-amber-300 px-2 py-0.5 rounded font-mono">TikTok Video Chuẩn</span>
                    </div>
                    <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbLR8Vwh/')" class="px-3 py-2 bg-amber-400/20 text-amber-300 border border-amber-400/30 hover:bg-amber-400 hover:text-gray-900 text-xs font-semibold rounded-xl flex items-center gap-1.5 transition cursor-pointer shrink-0">
                        <i class="fa-regular fa-copy"></i> Sao chép link
                    </button>
                </div>
            </div>
            <div class="p-4 border-t border-gray-800 bg-gray-900">
                <button type="button" onclick="closeModal('cardioModal')" class="w-full py-3 bg-gray-800 text-gray-200 font-bold rounded-xl text-xs hover:bg-gray-700 cursor-pointer">Đóng</button>
            </div>
        </div>
    </div>

    <div id="beginnerModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900 sticky top-0">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-graduation-cap text-amber-400"></i>
                    <h3 class="font-bold text-white text-base">Hỗ Trợ Người Mới</h3>
                </div>
                <button type="button" onclick="closeModal('beginnerModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div class="p-4 overflow-y-auto space-y-5">
                <div>
                    <div class="flex items-center justify-between mb-2.5">
                        <h4 class="font-bold text-sm text-amber-400 flex items-center gap-2">
                            <i class="fa-solid fa-fire-flame-curved"></i> Mở Khóa Hít Đất (Push Up)
                        </h4>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbL8KKPq/')" class="px-2.5 py-1.5 bg-amber-400/20 text-amber-300 border border-amber-400/30 hover:bg-amber-400 hover:text-gray-900 text-xs font-semibold rounded-lg flex items-center gap-1.5 transition cursor-pointer">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="grid grid-cols-2 gap-2 text-xs">
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60"><span class="text-amber-400 font-bold">Ngày 1:</span> Bài 1 (60s × 5 sets)</div>
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60"><span class="text-amber-400 font-bold">Ngày 2:</span> Bài 2 (30 reps × 5 sets)</div>
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60"><span class="text-amber-400 font-bold">Ngày 3:</span> Bài 3 (60s × 5 sets)</div>
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60"><span class="text-amber-400 font-bold">Ngày 4:</span> Bài 4 (20 reps × 5 sets)</div>
                    </div>
                </div>

                <div>
                    <div class="flex items-center justify-between mb-2.5">
                        <h4 class="font-bold text-sm text-tiktok-cyan flex items-center gap-2">
                            <i class="fa-solid fa-child-reaching"></i> Mở Khóa Kéo Xà (Pull Up)
                        </h4>
                        <button type="button" onclick="copyToClipboard('https://vt.tiktok.com/ZSbLL3Laf/')" class="px-2.5 py-1.5 bg-tiktok-cyan/20 text-tiktok-cyan border border-tiktok-cyan/30 hover:bg-tiktok-cyan hover:text-gray-900 text-xs font-semibold rounded-lg flex items-center gap-1.5 transition cursor-pointer">
                            <i class="fa-regular fa-copy"></i> Sao chép link
                        </button>
                    </div>
                    <div class="space-y-2 text-xs">
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60 flex justify-between">
                            <span><strong class="text-tiktok-cyan">Cấp độ 1:</strong> Bài 1</span>
                            <span class="font-mono text-gray-300">15 reps × 4 sets</span>
                        </div>
                        <div class="p-2.5 bg-gray-800/70 rounded-lg border border-gray-700/60 flex justify-between">
                            <span><strong class="text-tiktok-cyan">Cấp độ 2:</strong> Bài 2</span>
                            <span class="font-mono text-gray-300">15 reps × 4 sets</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div id="shopModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900 sticky top-0">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-bag-shopping text-emerald-400"></i>
                    <h3 class="font-bold text-white text-base">Cửa Hàng Dụng Cụ Shopee</h3>
                </div>
                <button type="button" onclick="closeModal('shopModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div class="p-4 overflow-y-auto space-y-3.5">
                <div class="p-3 bg-emerald-500/10 border border-emerald-500/30 rounded-xl flex items-center justify-between">
                    <div>
                        <span class="text-xs font-bold text-emerald-400 block">Voucher Giảm Giá 100K</span>
                        <span class="text-[11px] text-gray-400">Trạng thái: Chưa mở / Cập nhật sớm</span>
                    </div>
                    <span class="px-2.5 py-1 bg-emerald-500/20 text-emerald-300 text-[10px] rounded-full font-semibold">Chờ phát</span>
                </div>

                <div class="space-y-3">
                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/60 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                        <div class="flex items-center space-x-3">
                            <div class="w-10 h-10 rounded-lg bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-base shrink-0">
                                <i class="fa-solid fa-dumbbell"></i>
                            </div>
                            <div>
                                <h5 class="font-bold text-sm text-white">Tạ Đơn (1 – 12kg)</h5>
                                <span class="text-xs text-gray-400">Số lượng: 2 cục</span>
                            </div>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vn.shp.ee/98bWduQP')" class="w-full sm:w-auto px-3.5 py-2 bg-gray-800 hover:bg-gray-700 border border-gray-700 text-gray-200 hover:text-white text-xs font-semibold rounded-xl flex items-center justify-center gap-1.5 transition cursor-pointer">
                            <i class="fa-regular fa-copy text-emerald-400"></i>
                            <span>Sao chép link mua sản phẩm</span>
                        </button>
                    </div>

                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/60 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                        <div class="flex items-center space-x-3">
                            <div class="w-10 h-10 rounded-lg bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-base shrink-0">
                                <i class="fa-solid fa-bars"></i>
                            </div>
                            <div>
                                <h5 class="font-bold text-sm text-white">Xà Đơn Treo Tường</h5>
                                <span class="text-xs text-gray-400">Số lượng: 1 cái</span>
                            </div>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vn.shp.ee/6ibx2CVb')" class="w-full sm:w-auto px-3.5 py-2 bg-gray-800 hover:bg-gray-700 border border-gray-700 text-gray-200 hover:text-white text-xs font-semibold rounded-xl flex items-center justify-center gap-1.5 transition cursor-pointer">
                            <i class="fa-regular fa-copy text-emerald-400"></i>
                            <span>Sao chép link mua sản phẩm</span>
                        </button>
                    </div>

                    <div class="p-3.5 bg-gray-800/60 rounded-xl border border-gray-700/60 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                        <div class="flex items-center space-x-3">
                            <div class="w-10 h-10 rounded-lg bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-base shrink-0">
                                <i class="fa-solid fa-ribbon"></i>
                            </div>
                            <div>
                                <h5 class="font-bold text-sm text-white">Combo Dây Kháng Lực</h5>
                                <span class="text-xs text-gray-400">Đen + Tím (1 combo)</span>
                            </div>
                        </div>
                        <button type="button" onclick="copyToClipboard('https://vn.shp.ee/2tKtn9Sb')" class="w-full sm:w-auto px-3.5 py-2 bg-gray-800 hover:bg-gray-700 border border-gray-700 text-gray-200 hover:text-white text-xs font-semibold rounded-xl flex items-center justify-center gap-1.5 transition cursor-pointer">
                            <i class="fa-regular fa-copy text-emerald-400"></i>
                            <span>Sao chép link mua sản phẩm</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div id="bmiModal" class="custom-modal fixed inset-0 z-50 bg-black/80 backdrop-blur-md items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900 sticky top-0">
                <div class="flex items-center gap-2">
                    <i class="fa-solid fa-chart-line text-purple-400"></i>
                    <h3 class="font-bold text-white text-base">Chỉ Số Nhóm & Máy Tính BMI</h3>
                </div>
                <button type="button" onclick="closeModal('bmiModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center cursor-pointer">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div class="p-4 overflow-y-auto space-y-5">
                <div class="p-4 bg-purple-950/40 border border-purple-800/40 rounded-2xl space-y-3">
                    <h4 class="font-bold text-sm text-purple-300 flex items-center gap-2">
                        <i class="fa-solid fa-calculator"></i> Tính BMI Cá Nhân Của Bạn
                    </h4>
                    <div class="grid grid-cols-2 gap-3">
                        <div>
                            <label class="text-[11px] text-gray-400 block mb-1">Cân nặng (kg)</label>
                            <input type="number" id="calcWeight" placeholder="Ví dụ: 55" class="w-full bg-gray-800 border border-gray-700 text-xs rounded-lg p-2.5 text-white focus:outline-none focus:border-purple-400">
                        </div>
                        <div>
                            <label class="text-[11px] text-gray-400 block mb-1">Chiều cao (cm)</label>
                            <input type="number" id="calcHeight" placeholder="Ví dụ: 165" class="w-full bg-gray-800 border border-gray-700 text-xs rounded-lg p-2.5 text-white focus:outline-none focus:border-purple-400">
                        </div>
                    </div>
                    <button type="button" onclick="calculateUserBMI()" class="w-full py-2.5 bg-purple-600 hover:bg-purple-500 text-white font-bold text-xs rounded-xl transition cursor-pointer">
                        Tính Ngay
                    </button>
                    <div id="bmiResult" class="hidden p-3 bg-gray-900 rounded-xl text-center text-xs"></div>
                </div>

                <div>
                    <h4 class="font-bold text-xs text-gray-400 uppercase tracking-wider mb-2.5">Bảng Chỉ Số Các Thành Viên</h4>
                    <div class="overflow-x-auto border border-gray-800 rounded-xl">
                        <table class="w-full text-xs text-left text-gray-300">
                            <thead class="bg-gray-800 text-gray-400 text-[11px] uppercase">
                                <tr>
                                    <th class="p-2.5">Tên</th>
                                    <th class="p-2.5">Cân nặng</th>
                                    <th class="p-2.5">Chiều cao</th>
                                    <th class="p-2.5">BMI</th>
                                    <th class="p-2.5">Trạng thái</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-gray-800">
                                <tr>
                                    <td class="p-2.5 font-bold text-white">Nhân</td>
                                    <td class="p-2.5">52kg</td>
                                    <td class="p-2.5">1m59</td>
                                    <td class="p-2.5 text-emerald-400 font-mono font-semibold">20.6</td>
                                    <td class="p-2.5"><span class="px-2 py-0.5 bg-emerald-500/20 text-emerald-300 rounded text-[10px]">Bình thường</span></td>
                                </tr>
                                <tr>
                                    <td class="p-2.5 font-bold text-white">Bảo</td>
                                    <td class="p-2.5">48kg</td>
                                    <td class="p-2.5">1m58</td>
                                    <td class="p-2.5 text-emerald-400 font-mono font-semibold">19.2</td>
                                    <td class="p-2.5"><span class="px-2 py-0.5 bg-emerald-500/20 text-emerald-300 rounded text-[10px]">Bình thường</span></td>
                                </tr>
                                <tr>
                                    <td class="p-2.5 font-bold text-white">Phát</td>
                                    <td class="p-2.5">73kg</td>
                                    <td class="p-2.5">1m65</td>
                                    <td class="p-2.5 text-red-400 font-mono font-semibold">26.8</td>
                                    <td class="p-2.5"><span class="px-2 py-0.5 bg-red-500/20 text-red-300 rounded text-[10px]">Béo phì</span></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Modal handlers using class toggle for foolproof visibility
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.classList.add('active');
                document.body.style.overflow = 'hidden';
            }
        }

        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.classList.remove('active');
                document.body.style.overflow = '';
            }
        }

        // Switch muscle tabs inside Exercises Modal
        function switchTab(tabId) {
            const contents = document.querySelectorAll('.tab-content');
            contents.forEach(el => el.classList.add('hidden'));

            const targetContent = document.getElementById('content-' + tabId);
            if (targetContent) {
                targetContent.classList.remove('hidden');
            }

            const buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(btn => {
                btn.className = 'tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-gray-800/80 text-gray-400 hover:text-white border border-gray-700/50 transition-all active:scale-95 cursor-pointer';
            });

            const activeBtn = document.getElementById('tab-' + tabId);
            if (activeBtn) {
                activeBtn.className = 'tab-btn shrink-0 px-3.5 py-2 rounded-xl text-xs font-bold whitespace-nowrap bg-tiktok-pink text-white shadow-lg shadow-tiktok-pink/20 transition-all active:scale-95 cursor-pointer';
            }
        }

        // Toast notification system
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            if (toast && toastMsg) {
                toastMsg.innerText = message || "Đã sao chép!";
                toast.classList.remove('-translate-y-20', 'opacity-0');
                toast.classList.add('translate-y-0', 'opacity-100');
                setTimeout(() => {
                    toast.classList.remove('translate-y-0', 'opacity-100');
                    toast.classList.add('-translate-y-20', 'opacity-0');
                }, 2500);
            }
        }

        // Copy text helper
        function copyToClipboard(text) {
            if (!text) return;
            const textArea = document.createElement("textarea");
            textArea.value = text;
            textArea.style.position = "fixed";
            textArea.style.left = "-999999px";
            textArea.style.top = "-999999px";
            document.body.appendChild(textArea);
            textArea.focus();
            textArea.select();
            try {
                document.execCommand('copy');
                showToast("Đã sao chép liên kết!");
            } catch (err) {
                console.error('Không thể sao chép: ', err);
            }
            document.body.removeChild(textArea);
        }

        // Calculate BMI
        function calculateUserBMI() {
            const w = parseFloat(document.getElementById('calcWeight').value);
            const h = parseFloat(document.getElementById('calcHeight').value) / 100;
            const resDiv = document.getElementById('bmiResult');
            
            if (!w || !h || h <= 0) {
                if (resDiv) {
                    resDiv.innerHTML = '<span class="text-red-400 font-bold">Vui lòng nhập cân nặng và chiều cao hợp lệ!</span>';
                    resDiv.classList.remove('hidden');
                }
                return;
            }
            
            const bmi = (w / (h * h)).toFixed(1);
            let status = "";
            let colorClass = "";
            
            if (bmi < 18.5) {
                status = "Thiếu cân / Gầy";
                colorClass = "text-amber-400";
            } else if (bmi <= 22.9) {
                status = "Bình thường / Lí tưởng";
                colorClass = "text-emerald-400";
            } else if (bmi <= 24.9) {
                status = "Thừa cân nhẹ";
                colorClass = "text-amber-400";
            } else {
                status = "Béo phì / Cần giảm cân";
                colorClass = "text-red-400";
            }
            
            if (resDiv) {
                resDiv.innerHTML = `BMI của bạn: <strong class="text-white font-mono text-sm">${bmi}</strong> - <span class="${colorClass} font-bold">${status}</span>`;
                resDiv.classList.remove('hidden');
            }
        }

        // Close modal when clicking backdrop
        window.onclick = function(event) {
            const modals = ['scheduleModal', 'exercisesModal', 'cardioModal', 'beginnerModal', 'shopModal', 'bmiModal'];
            modals.forEach(id => {
                const modal = document.getElementById(id);
                if (event.target === modal) {
                    closeModal(id);
                }
            });
        };
    </script>
</body>
</html>
