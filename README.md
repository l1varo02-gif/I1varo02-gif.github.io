# I1varo02-gif.github.io
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator Parkir - Presentasi Slide Interaktif</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Google Fonts Inter & Fira Code -->
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
        }
        code, pre {
            font-family: 'Fira Code', monospace;
        }
        /* Custom smooth slide transition */
        .slide-container {
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex items-center justify-center p-4 sm:p-6 lg:p-8">

    <div class="w-full max-w-6xl mx-auto slide-container bg-gradient-to-br from-slate-900 via-indigo-950 to-slate-900 border border-slate-800 rounded-3xl overflow-hidden shadow-2xl relative flex flex-col">
        
        <!-- Top Presentation Header Bar -->
        <div class="px-8 py-5 border-b border-slate-800/80 flex items-center justify-between bg-slate-900/50 backdrop-blur-md">
            <div class="flex items-center space-x-3">
                <div class="h-10 w-10 rounded-xl bg-indigo-600 flex items-center justify-center shadow-lg shadow-indigo-500/30">
                    <i data-lucide="presentation" class="w-5 h-5 text-white"></i>
                </div>
                <div>
                    <span class="text-xs font-semibold tracking-wider text-indigo-400 uppercase">Studi Kasus Python & Algoritma</span>
                    <h1 class="text-lg font-bold text-white">Aplikasi Kalkulator Pembayaran Parkir</h1>
                </div>
            </div>
            <div class="flex items-center space-x-2">
                <button onclick="switchTab('code')" id="btn-code" class="px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-indigo-600 text-white shadow-lg shadow-indigo-600/20">
                    <i data-lucide="code" class="w-4 h-4"></i>
                    <span>Kode Python</span>
                </button>
                <button onclick="switchTab('demo')" id="btn-demo" class="px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-slate-800 text-slate-300 hover:bg-slate-700 hover:text-white">
                    <i data-lucide="play-circle" class="w-4 h-4"></i>
                    <span>Live Simulator</span>
                </button>
            </div>
        </div>

        <div class="p-6 sm:p-10 flex-1 relative overflow-y-auto">
            
            <!-- TAB 1: CODE VIEW -->
            <div id="tab-code" class="space-y-6">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
                    
                    <!-- Left: Code Explanation & Breakdown -->
                    <div class="lg:col-span-5 space-y-4">
                        <div class="bg-indigo-950/40 border border-indigo-500/20 rounded-2xl p-6 backdrop-blur-sm">
                            <div class="flex items-center space-x-2 text-indigo-400 mb-3">
                                <i data-lucide="sparkles" class="w-5 h-5"></i>
                                <h2 class="font-bold text-white text-base">Logika Utama Algoritma</h2>
                            </div>
                            <p class="text-sm text-slate-300 leading-relaxed">
                                Program ini menghitung tarif progresif berdasarkan jenis kendaraan (<code class="text-indigo-300 font-mono">motor</code> atau <code class="text-indigo-300 font-mono">mobil</code>) serta durasi parkir dalam jam.
                            </p>
                        </div>

                        <div class="space-y-3">
                            <div class="bg-slate-800/50 border border-slate-700/60 rounded-xl p-4 flex items-start space-x-3">
                                <div class="bg-blue-500/10 text-blue-400 p-2 rounded-lg mt-0.5">
                                    <i data-lucide="function-square" class="w-4 h-4"></i>
                                </div>
                                <div>
                                    <h3 class="text-sm font-bold text-white">Fungsi <code class="text-blue-300">hitung_parkir(kendaraan, jam)</code></h3>
                                    <p class="text-xs text-slate-400 mt-1">Mengatur tarif dasar 1 jam pertama dan penambahan per jam berikutnya secara kondisional.</p>
                                </div>
                            </div>

                            <div class="bg-slate-800/50 border border-slate-700/60 rounded-xl p-4 flex items-start space-x-3">
                                <div class="bg-emerald-500/10 text-emerald-400 p-2 rounded-lg mt-0.5">
                                    <i data-lucide="receipt" class="w-4 h-4"></i>
                                </div>
                                <div>
                                    <h3 class="text-sm font-bold text-white">Struk & Validasi Pembayaran</h3>
                                    <p class="text-xs text-slate-400 mt-1">Menerima input nama, mencetak rincian biaya, serta menghitung uang kembalian secara otomatis.</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Right: Styled Python Code Box -->
                    <div class="lg:col-span-7 bg-slate-950/80 border border-slate-800 rounded-2xl overflow-hidden shadow-xl">
                        <div class="bg-slate-900/80 px-4 py-3 border-b border-slate-800 flex items-center justify-between">
                            <div class="flex items-center space-x-2">
                                <div class="w-3 h-3 rounded-full bg-rose-500"></div>
                                <div class="w-3 h-3 rounded-full bg-amber-500"></div>
                                <div class="w-3 h-3 rounded-full bg-emerald-500"></div>
                                <span class="text-xs font-mono text-slate-400 ml-2">parkir.py</span>
                            </div>
                            <button onclick="copyCode()" class="text-xs text-slate-400 hover:text-white flex items-center space-x-1.5 bg-slate-800 hover:bg-slate-700 px-3 py-1.5 rounded-lg transition-all">
                                <i data-lucide="copy" class="w-3.5 h-3.5"></i>
                                <span id="copy-text">Salin Kode</span>
                            </button>
                        </div>
                        <div class="p-5 overflow-x-auto text-xs sm:text-sm font-mono leading-relaxed text-slate-300 max-h-[420px] overflow-y-auto">
                            <pre><code id="source-code"><span class="text-indigo-400">def</span> <span class="text-emerald-400">hitung_parkir</span>(kendaraan, jam):
    <span class="text-indigo-400">if</span> kendaraan == <span class="text-amber-300">"motor"</span>:
        <span class="text-indigo-400">if</span> jam &lt;= <span class="text-orange-400">1</span>:
            biaya = <span class="text-orange-400">3000</span>
        <span class="text-indigo-400">else</span>:
            biaya = <span class="text-orange-400">3000</span> + (jam - <span class="text-orange-400">1</span>) * <span class="text-orange-400">1000</span>

    <span class="text-indigo-400">elif</span> kendaraan == <span class="text-amber-300">"mobil"</span>:
        <span class="text-indigo-400">if</span> jam &lt;= <span class="text-orange-400">1</span>:
            biaya = <span class="text-orange-400">5000</span>
        <span class="text-indigo-400">else</span>:
            biaya = <span class="text-orange-400">5000</span> + (jam - <span class="text-orange-400">1</span>) * <span class="text-orange-400">2000</span>

    <span class="text-indigo-400">else</span>:
        biaya = <span class="text-orange-400">0</span>

    <span class="text-indigo-400">return</span> biaya

<span class="text-slate-500"># Input Data Pengguna</span>
nama = <span class="text-sky-300">input</span>(<span class="text-amber-300">"Nama              : "</span>)
kendaraan = <span class="text-sky-300">input</span>(<span class="text-amber-300">"Jenis kendaraan   : "</span>).lower()
jam = <span class="text-sky-300">int</span>(<span class="text-sky-300">input</span>(<span class="text-amber-300">"Lama parkir (jam) : "</span>))

biaya = hitung_parkir(kendaraan, jam)

<span class="text-indigo-400">if</span> biaya &gt; <span class="text-orange-400">0</span>:
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"\n================================"</span>)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"          STRUK PARKIR"</span>)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"================================"</span>)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"Nama              :"</span>, nama)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"Kendaraan         :"</span>, kendaraan)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"Lama parkir       :"</span>, jam, <span class="text-amber-300">"jam"</span>)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"Total pembayaran  : Rp"</span>, biaya)
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"================================"</span>)
    
    uang = <span class="text-sky-300">int</span>(<span class="text-sky-300">input</span>(<span class="text-amber-300">"Uang pembayaran   : Rp "</span>))
    <span class="text-indigo-400">if</span> uang &gt;= biaya:
        kembalian = uang - biaya
        <span class="text-sky-300">print</span>(<span class="text-amber-300">"Kembalian         : Rp"</span>, kembalian)
        <span class="text-sky-300">print</span>(<span class="text-amber-300">"Pembayaran berhasil!"</span>)
    <span class="text-indigo-400">else</span>:
        kurang = biaya - uang
        <span class="text-sky-300">print</span>(<span class="text-amber-300">"Uang Anda kurang  : Rp"</span>, kurang)
        <span class="text-sky-300">print</span>(<span class="text-amber-300">"Pembayaran gagal."</span>)
<span class="text-indigo-400">else</span>:
    <span class="text-sky-300">print</span>(<span class="text-amber-300">"Jenis kendaraan tidak tersedia."</span>)</code></pre>
                        </div>
                    </div>

                </div>
            </div>

            <!-- TAB 2: LIVE SIMULATOR -->
            <div id="tab-demo" class="hidden space-y-6">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
                    
                    <!-- Input Form Column -->
                    <div class="lg:col-span-6 bg-slate-800/40 border border-slate-700/60 rounded-2xl p-6 backdrop-blur-sm space-y-5">
                        <div class="flex items-center space-x-3 border-b border-slate-700/60 pb-4">
                            <div class="p-2 rounded-xl bg-indigo-600/20 text-indigo-400">
                                <i data-lucide="terminal" class="w-5 h-5"></i>
                            </div>
                            <div>
                                <h2 class="font-bold text-white text-base">Simulator Terminal Python</h2>
                                <p class="text-xs text-slate-400">Uji interaktif kode kalkulator parkir secara langsung</p>
                            </div>
                        </div>

                        <form id="parkingForm" onsubmit="handleCalculate(event)" class="space-y-4">
                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Nama Pemilik / Pengendara</label>
                                <input type="text" id="inputNama" required placeholder="Contoh: Budi Santoso" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-indigo-500 transition-colors">
                            </div>

                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Jenis Kendaraan</label>
                                <div class="grid grid-cols-2 gap-3">
                                    <button type="button" onclick="selectVehicle('motor')" id="btn-motor" class="vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-indigo-500 bg-indigo-600/20 text-white font-medium text-sm transition-all">
                                        <i data-lucide="bike" class="w-4 h-4 text-indigo-400"></i>
                                        <span>Motor (Rp3k/1 jam)</span>
                                    </button>
                                    <button type="button" onclick="selectVehicle('mobil')" id="btn-mobil" class="vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-slate-700 bg-slate-900 text-slate-400 font-medium text-sm transition-all hover:border-slate-600">
                                        <i data-lucide="car" class="w-4 h-4 text-slate-400"></i>
                                        <span>Mobil (Rp5k/1 jam)</span>
                                    </button>
                                </div>
                                <input type="hidden" id="inputKendaraan" value="motor">
                            </div>

                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Lama Parkir (Jam)</label>
                                <div class="flex items-center space-x-3">
                                    <input type="number" id="inputJam" min="1" max="72" value="3" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-indigo-500 transition-colors">
                                    <span class="text-xs text-slate-400 font-medium whitespace-nowrap">Jam</span>
                                </div>
                            </div>

                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1.5">Nominal Uang Pembayaran (Rp)</label>
                                <input type="number" id="inputUang" min="0" step="500" value="20000" required class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-indigo-500 transition-colors">
                            </div>

                            <button type="submit" class="w-full bg-gradient-to-r from-indigo-600 to-violet-600 hover:from-indigo-500 hover:to-violet-500 text-white font-semibold py-3 px-6 rounded-xl shadow-lg shadow-indigo-600/30 transition-all flex items-center justify-center space-x-2">
                                <i data-lucide="calculator" class="w-4 h-4"></i>
                                <span>Hitung Biaya & Cetak Struk</span>
                            </button>
                        </form>
                    </div>

                    <!-- Output / Result Column -->
                    <div class="lg:col-span-6 bg-slate-950/80 border border-slate-800 rounded-2xl p-6 shadow-xl flex flex-col justify-between min-h-[460px]">
                        <div>
                            <div class="flex items-center justify-between border-b border-slate-800 pb-3 mb-4">
                                <span class="text-xs font-mono text-indigo-400 uppercase tracking-wider flex items-center space-x-1.5">
                                    <i data-lucide="receipt" class="w-4 h-4"></i>
                                    <span>Output Struk Parkir</span>
                                </span>
                                <span id="statusBadge" class="px-2.5 py-1 rounded-full text-xs font-semibold bg-emerald-500/10 text-emerald-400 border border-emerald-500/20">Siap Dihitung</span>
                            </div>

                            <!-- Receipt Container -->
                            <div id="receiptOutput" class="font-mono text-xs text-slate-300 space-y-1.5 bg-slate-900/60 p-5 rounded-xl border border-slate-800">
                                <p class="text-slate-500 text-center italic py-10">Tekan tombol "Hitung Biaya & Cetak Struk" untuk melihat hasil eksekusi program.</p>
                            </div>
                        </div>

                        <div class="mt-6 pt-4 border-t border-slate-800/80 flex items-center justify-between text-xs text-slate-400">
                            <span>Status Eksekusi: <strong class="text-emerald-400">Berhasil</strong></span>
                            <button onclick="resetSimulator()" class="text-indigo-400 hover:text-indigo-300 underline font-medium">Reset Data</button>
                        </div>
                    </div>

                </div>
            </div>

        </div>

        <!-- Footer / Slide Navigation Information -->
        <div class="px-8 py-4 border-t border-slate-800/80 bg-slate-900/50 backdrop-blur-md flex items-center justify-between text-xs text-slate-400">
            <div class="flex items-center space-x-2">
                <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
                <span>Slide Interaktif Siap Presentasi (16:9)</span>
            </div>
            <div class="flex items-center space-x-4">
                <span>Teknologi: Python Algoritma & Tailwind Web</span>
                <span class="bg-slate-800 px-2.5 py-1 rounded-md font-mono text-slate-300">Slide 1 dari 1</span>
            </div>
        </div>

    </div>

    <!-- Script Logic -->
    <script>
        // Initialize Lucide icons
        lucide.createIcons();

        // Tab Switching Logic
        function switchTab(tabName) {
            const tabCode = document.getElementById('tab-code');
            const tabDemo = document.getElementById('tab-demo');
            const btnCode = document.getElementById('btn-code');
            const btnDemo = document.getElementById('btn-demo');

            if (tabName === 'code') {
                tabCode.classList.remove('hidden');
                tabDemo.classList.add('hidden');
                btnCode.className = "px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-indigo-600 text-white shadow-lg shadow-indigo-600/20";
                btnDemo.className = "px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-slate-800 text-slate-300 hover:bg-slate-700 hover:text-white";
            } else {
                tabCode.classList.add('hidden');
                tabDemo.classList.remove('hidden');
                btnDemo.className = "px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-indigo-600 text-white shadow-lg shadow-indigo-600/20";
                btnCode.className = "px-4 py-2 rounded-xl text-sm font-semibold transition-all duration-200 flex items-center space-x-2 bg-slate-800 text-slate-300 hover:bg-slate-700 hover:text-white";
            }
            lucide.createIcons();
        }

        // Vehicle Selector Logic
        function selectVehicle(type) {
            document.getElementById('inputKendaraan').value = type;
            const btnMotor = document.getElementById('btn-motor');
            const btnMobil = document.getElementById('btn-mobil');

            if (type === 'motor') {
                btnMotor.className = "vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-indigo-500 bg-indigo-600/20 text-white font-medium text-sm transition-all";
                btnMotor.innerHTML = '<i data-lucide="bike" class="w-4 h-4 text-indigo-400"></i><span>Motor (Rp3k/1 jam)</span>';
                btnMobil.className = "vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-slate-700 bg-slate-900 text-slate-400 font-medium text-sm transition-all hover:border-slate-600";
                btnMobil.innerHTML = '<i data-lucide="car" class="w-4 h-4 text-slate-400"></i><span>Mobil (Rp5k/1 jam)</span>';
            } else {
                btnMobil.className = "vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-indigo-500 bg-indigo-600/20 text-white font-medium text-sm transition-all";
                btnMobil.innerHTML = '<i data-lucide="car" class="w-4 h-4 text-indigo-400"></i><span>Mobil (Rp5k/1 jam)</span>';
                btnMotor.className = "vehicle-btn flex items-center justify-center space-x-2 py-3 px-4 rounded-xl border border-slate-700 bg-slate-900 text-slate-400 font-medium text-sm transition-all hover:border-slate-600";
                btnMotor.innerHTML = '<i data-lucide="bike" class="w-4 h-4 text-slate-400"></i><span>Motor (Rp3k/1 jam)</span>';
            }
            lucide.createIcons();
        }

        // Python Parking Calculation Function Simulation in JS
        function hitung_parkir(kendaraan, jam) {
            let biaya = 0;
            if (kendaraan === "motor") {
                if (jam <= 1) {
                    biaya = 3000;
                } else {
                    biaya = 3000 + (jam - 1) * 1000;
                }
            } else if (kendaraan === "mobil") {
                if (jam <= 1) {
                    biaya = 5000;
                } else {
                    biaya = 5000 + (jam - 1) * 2000;
                }
            } else {
                biaya = 0;
            }
            return biaya;
        }

        // Form Submit Handler
        function handleCalculate(e) {
            e.preventDefault();
            const nama = document.getElementById('inputNama').value || "Tanpa Nama";
            const kendaraan = document.getElementById('inputKendaraan').value;
            const jam = parseInt(document.getElementById('inputJam').value) || 1;
            const uang = parseInt(document.getElementById('inputUang').value) || 0;

            const biaya = hitung_parkir(kendaraan, jam);
            const receiptDiv = document.getElementById('receiptOutput');
            const statusBadge = document.getElementById('statusBadge');

            let htmlContent = "";

            if (biaya > 0) {
                htmlContent += `<p class="text-slate-400">Nama              : ${nama}</p>`;
                htmlContent += `<p class="text-slate-400">Jenis kendaraan   : ${kendaraan}</p>`;
                htmlContent += `<p class="text-slate-400">Lama parkir (jam) : ${jam}</p>`;
                htmlContent += `<div class="border-t border-dashed border-slate-700 my-2"></div>`;
                htmlContent += `<p class="text-emerald-400 font-bold">================================</p>`;
                htmlContent += `<p class="text-emerald-400 font-bold text-center">          STRUK PARKIR          </p>`;
                htmlContent += `<p class="text-emerald-400 font-bold">================================</p>`;
                htmlContent += `<p class="text-white">Nama              : ${nama}</p>`;
                htmlContent += `<p class="text-white">Kendaraan         : ${kendaraan}</p>`;
                htmlContent += `<p class="text-white">Lama parkir       : ${jam} jam</p>`;
                htmlContent += `<p class="text-emerald-300 font-bold">Total pembayaran  : Rp ${biaya.toLocaleString('id-ID')}</p>`;
                htmlContent += `<p class="text-emerald-400 font-bold">================================</p>`;
                htmlContent += `<p class="text-slate-400 mt-2">Uang pembayaran   : Rp ${uang.toLocaleString('id-ID')}</p>`;

                if (uang >= biaya) {
                    const kembalian = uang - biaya;
                    htmlContent += `<p class="text-sky-400 font-semibold">Kembalian         : Rp ${kembalian.toLocaleString('id-ID')}</p>`;
                    htmlContent += `<p class="text-emerald-400 font-bold mt-1">Pembayaran berhasil!</p>`;
                    statusBadge.className = "px-2.5 py-1 rounded-full text-xs font-semibold bg-emerald-500/10 text-emerald-400 border border-emerald-500/20";
                    statusBadge.textContent = "Pembayaran Sukses";
                } else {
                    const kurang = biaya - uang;
                    htmlContent += `<p class="text-rose-400 font-semibold">Uang Anda kurang  : Rp ${kurang.toLocaleString('id-ID')}</p>`;
                    htmlContent += `<p class="text-rose-400 font-bold mt-1">Pembayaran gagal.</p>`;
                    statusBadge.className = "px-2.5 py-1 rounded-full text-xs font-semibold bg-rose-500/10 text-rose-400 border border-rose-500/20";
                    statusBadge.textContent = "Uang Kurang";
                }
            } else {
                htmlContent += `<p class="text-rose-400">Jenis kendaraan tidak tersedia.</p>`;
                statusBadge.className = "px-2.5 py-1 rounded-full text-xs font-semibold bg-rose-500/10 text-rose-400 border border-rose-500/20";
                statusBadge.textContent = "Error Kendaraan";
            }

            receiptOutput.innerHTML = htmlContent;
        }

        // Copy Code to Clipboard
        function copyCode() {
            const codeText = document.getElementById('source-code').innerText;
            const copyTextSpan = document.getElementById('copy-text');
            
            // Using standard execCommand for reliable copying in iframe environments
            const textArea = document.createElement("textarea");
