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
            background: rgba(26, 26, 36, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-card:hover {
            border-color: rgba(37, 244, 238, 0.3);
        }
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #121212; }
        ::-webkit-scrollbar-thumb { background: #333344; border-radius: 10px; }
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
    </style>
</head>
<body class="min-h-screen pb-12 flex flex-col items-center justify-start px-4 sm:px-6">

    <!-- Toast thông báo khi copy link -->
    <div id="toast" class="fixed top-5 z-50 transform -translate-y-20 opacity-0 transition-all duration-300 ease-out bg-gray-900 border border-tiktok-cyan/40 text-white px-5 py-3 rounded-xl shadow-2xl flex items-center space-x-3 pointer-events-none">
        <i class="fa-solid fa-circle-check text-tiktok-cyan text-lg"></i>
        <span id="toast-message" class="text-sm font-medium">Đã sao chép liên kết!</span>
    </div>

    <main class="w-full max-w-md mx-auto pt-8 flex flex-col items-center">

        <!-- Nút Chia sẻ -->
        <div class="w-full flex justify-end items-center mb-6">
            <button type="button" onclick="copyToClipboard(window.location.href)" class="w-9 h-9 rounded-full bg-gray-800/80 border border-gray-700 flex items-center justify-center text-gray-300 hover:text-white hover:bg-gray-700 transition cursor-pointer" title="Chia sẻ trang web">
                <i class="fa-solid fa-share-nodes text-sm"></i>
            </button>
        </div>

        <!-- Profile Card -->
        <div class="text-center mb-6 flex flex-col items-center w-full">
            <div class="relative mb-3">
                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-full p-1 badge-pulse bg-gradient-to-tr from-tiktok-pink via-purple-500 to-tiktok-cyan overflow-hidden shadow-xl">
                    <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?q=80&w=400&auto=format&fit=crop" 
                         alt="Avatar" 
                         class="w-full h-full object-cover object-center rounded-full">
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

        <!-- Danh sách các Link / Nút bấm -->
        <div class="w-full space-y-3.5">

            <!-- LINK 1: Lịch Tập -->
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

            <!-- LINK 2: Thư Viện Bài Tập -->
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

            <!-- LINK 3: Mở Khóa Người Mới -->
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

            <!-- LINK 4: Link Shopee (Mở tab mới trực tiếp) -->
            <div class="link-item group">
                <a href="https://shopee.vn" target="_blank" rel="noopener noreferrer" 
                   class="w-full p-4 rounded-2xl glass-card flex items-center justify-between text-left transition-all duration-300 hover:scale-[1.02] active:scale-[0.98] border-l-4 border-l-emerald-400 block">
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
                    <i class="fa-solid fa-arrow-up-right-from-square text-gray-500 text-xs group-hover:text-white transition"></i>
                </a>
            </div>

        </div>

        <footer class="mt-10 text-center text-xs text-gray-500 space-y-2">
            <p>© 2026 Calisthenics TikTok Bio Hub.</p>
        </footer>

    </main>


    <!-- ==================== PHẦN BẢNG NỘI DUNG (MODAL) ==================== -->

    <!-- Modal 1: Lịch tập -->
    <div id="scheduleModal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900/90">
                <h3 class="font-bold text-white text-base">Lịch Tập Hàng Tuần (T2 - CN)</h3>
                <button type="button" onclick="closeModal('scheduleModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            <div class="p-4 overflow-y-auto space-y-3 text-sm">
                <div class="p-3 bg-gray-800/60 rounded-xl flex justify-between items-center">
                    <span class="font-bold text-tiktok-cyan">Thứ 2</span>
                    <span>Ngực, Vai, Tay sau</span>
                </div>
                <div class="p-3 bg-gray-800/60 rounded-xl flex justify-between items-center">
                    <span class="font-bold text-tiktok-pink">Thứ 3</span>
                    <span>Lưng - xô, Tay trước</span>
                </div>
                <div class="p-3 bg-gray-800/60 rounded-xl flex justify-between items-center">
                    <span class="font-bold text-amber-400">Thứ 4</span>
                    <span>Chân, Bụng (Core)</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal 2: Thư viện bài tập -->
    <div id="exercisesModal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900/90">
                <h3 class="font-bold text-white text-base">Thư Viện Bài Tập</h3>
                <button type="button" onclick="closeModal('exercisesModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            <div class="p-4 overflow-y-auto space-y-3 text-sm text-gray-300">
                <p>👉 Tổng hợp các video hướng dẫn động tác chuẩn kỹ thuật từ cơ bản đến nâng cao.</p>
            </div>
        </div>
    </div>

    <!-- Modal 3: Người mới -->
    <div id="beginnerModal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden items-end sm:items-center justify-center p-0 sm:p-4">
        <div class="bg-gray-900 border border-gray-800 w-full max-w-lg rounded-t-3xl sm:rounded-3xl max-h-[85vh] flex flex-col overflow-hidden shadow-2xl">
            <div class="p-4 border-b border-gray-800 flex items-center justify-between bg-gray-900/90">
                <h3 class="font-bold text-white text-base">Lộ Trình Người Mới</h3>
                <button type="button" onclick="closeModal('beginnerModal')" class="w-8 h-8 rounded-full bg-gray-800 text-gray-400 hover:text-white flex items-center justify-center">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            <div class="p-4 overflow-y-auto space-y-3 text-sm text-gray-300">
                <p>👉 Hướng dẫn từng bước cho người chưa từng tập Calisthenics.</p>
            </div>
        </div>
    </div>


    <!-- ==================== ĐOẠN JAVASCRIPT ĐIỀU KHIỂN ==================== -->
    <script>
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.classList.remove('hidden');
                modal.classList.add('flex');
                document.body.style.overflow = 'hidden';
            }
        }

        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.classList.add('hidden');
                modal.classList.remove('flex');
                document.body.style.overflow = 'auto';
            }
        }

        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                const toast = document.getElementById('toast');
                toast.classList.remove('-translate-y-20', 'opacity-0');
                toast.classList.add('translate-y-0', 'opacity-100');
                setTimeout(() => {
                    toast.classList.remove('translate-y-0', 'opacity-100');
                    toast.classList.add('-translate-y-20', 'opacity-0');
                }, 2000);
            });
        }

        // Bấm ra ngoài vùng đen để tự đóng modal
        window.onclick = function(event) {
            if (event.target.classList.contains('fixed') && event.target.classList.contains('inset-0')) {
                event.target.classList.add('hidden');
                event.target.classList.remove('flex');
                document.body.style.overflow = 'auto';
            }
        }
    </script>
</body>
</html>

