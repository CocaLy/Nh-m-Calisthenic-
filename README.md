```html
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
                    <div class="p-3.5
