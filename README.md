<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Naar de 'Republiek Indonesia' (1925) - Tan Malaka</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700&family=Lora:ital,wght@0,400;0,600;1,400&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-paper: #FAF8F5;
            --bg-card: #FFFFFF;
            --text-main: #2C2825;
            --text-muted: #66605B;
            --maroon: #7A1C1C;
            --maroon-dark: #521212;
            --maroon-light: #F7EBEB;
            --accent-gold: #C59B27;
            --border-color: #E6E0D8;
            --shadow-sm: 0 2px 8px rgba(44, 40, 37, 0.05);
            --shadow-md: 0 6px 18px rgba(44, 40, 37, 0.08);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-paper);
            color: var(--text-main);
            line-height: 1.7;
        }

        /* Top Bar Student Identity */
        .top-identity {
            background: linear-gradient(90deg, #1A1817 0%, var(--maroon-dark) 50%, #1A1817 100%);
            color: #FFFFFF;
            text-align: center;
            padding: 10px 20px;
            font-size: 0.9rem;
            letter-spacing: 1px;
            font-weight: 600;
            border-bottom: 2px solid var(--accent-gold);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .top-identity span {
            color: var(--accent-gold);
            font-family: 'Cinzel', serif;
        }

        /* Layout Container */
        .container {
            max-width: 960px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Header / Hero */
        header {
            padding: 60px 0 40px;
            text-align: center;
            border-bottom: 2px dashed var(--border-color);
            margin-bottom: 50px;
        }

        .badge-year {
            display: inline-block;
            background-color: var(--maroon-light);
            color: var(--maroon);
            font-weight: 700;
            font-size: 0.85rem;
            padding: 6px 16px;
            border-radius: 50px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            margin-bottom: 20px;
            border: 1px solid rgba(122, 28, 28, 0.2);
        }

        h1 {
            font-family: 'Cinzel', serif;
            font-size: 2.8rem;
            color: var(--maroon);
            line-height: 1.2;
            margin-bottom: 12px;
        }

        .subtitle {
            font-family: 'Lora', serif;
            font-style: italic;
            font-size: 1.3rem;
            color: var(--text-muted);
            margin-bottom: 24px;
        }

        .author-tag {
            font-size: 1rem;
            color: var(--text-main);
            font-weight: 600;
        }

        /* Section Styling */
        section {
            margin-bottom: 60px;
        }

        .section-title {
            font-family: 'Cinzel', serif;
            font-size: 1.6rem;
            color: var(--maroon-dark);
            margin-bottom: 24px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section-title::after {
            content: '';
            flex: 1;
            height: 1px;
            background-color: var(--border-color);
        }

        /* Summary Cards Grid */
        .grid-summary {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .card {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 24px;
            box-shadow: var(--shadow-sm);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .card:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-md);
            border-color: var(--accent-gold);
        }

        .card h3 {
            font-family: 'Lora', serif;
            font-size: 1.2rem;
            color: var(--maroon);
            margin-bottom: 10px;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Interactive Tabs Section */
        .tabs-wrapper {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 30px;
            box-shadow: var(--shadow-sm);
        }

        .tabs-header {
            display: flex;
            gap: 10px;
            border-bottom: 2px solid var(--border-color);
            margin-bottom: 24px;
            overflow-x: auto;
        }

        .tab-btn {
            background: none;
            border: none;
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-weight: 600;
            font-size: 0.95rem;
            color: var(--text-muted);
            padding: 12px 20px;
            cursor: pointer;
            border-bottom: 3px solid transparent;
            margin-bottom: -2px;
            white-space: nowrap;
            transition: all 0.2s ease;
        }

        .tab-btn:hover {
            color: var(--maroon);
        }

        .tab-btn.active {
            color: var(--maroon);
            border-bottom-color: var(--maroon);
        }

        .tab-panel {
            display: none;
        }

        .tab-panel.active {
            display: block;
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .tab-panel h4 {
            font-family: 'Lora', serif;
            font-size: 1.3rem;
            color: var(--maroon-dark);
            margin-bottom: 12px;
        }

        .tab-panel p {
            color: var(--text-main);
            font-size: 1rem;
            margin-bottom: 16px;
        }

        .highlight-box {
            background-color: var(--bg-paper);
            border-left: 4px solid var(--accent-gold);
            padding: 16px;
            font-style: italic;
            font-family: 'Lora', serif;
            color: var(--text-muted);
        }

        /* Fun Facts Section */
        .facts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(420px, 1fr));
            gap: 20px;
        }

        @media (max-width: 500px) {
            .facts-grid {
                grid-template-columns: 1fr;
            }
        }

        .fact-item {
            background-color: var(--bg-card);
            border-left: 4px solid var(--maroon);
            border-top: 1px solid var(--border-color);
            border-right: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
            padding: 20px;
            border-radius: 0 8px 8px 0;
            box-shadow: var(--shadow-sm);
        }

        .fact-number {
            font-family: 'Cinzel', serif;
            font-size: 0.85rem;
            font-weight: 700;
            color: var(--accent-gold);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 6px;
        }

        .fact-title {
            font-family: 'Lora', serif;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--maroon-dark);
            margin-bottom: 8px;
        }

        .fact-desc {
            font-size: 0.92rem;
            color: var(--text-muted);
        }

        /* Simple Timeline */
        .timeline {
            position: relative;
            padding-left: 20px;
            border-left: 2px solid var(--border-color);
        }

        .timeline-item {
            margin-bottom: 24px;
            position: relative;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -26px;
            top: 6px;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: var(--maroon);
            border: 2px solid var(--bg-paper);
        }

        .timeline-date {
            font-weight: 700;
            color: var(--maroon);
            font-size: 0.9rem;
        }

        .timeline-desc {
            color: var(--text-main);
            font-size: 0.95rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid var(--border-color);
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 40px;
        }

        footer strong {
            color: var(--maroon);
        }
    </style>
</head>
<body>

    <!-- TOP IDENTITY BAR -->
    <div class="top-identity">
        KARYA & PRESENTASI SEJARAH OLEH: <span>DAVID XI-2/5</span>
    </div>

    <div class="container">
        <!-- HEADER / HERO SECTION -->
        <header>
            <span class="badge-year">Pamflet Politik 1925</span>
            <h1>Naar de 'Republiek Indonesia'</h1>
            <div class="subtitle">(Menuju Republik Indonesia)</div>
            <div class="author-tag">Penulis: <strong>Tan Malaka</strong> (Canton, China)</div>
        </header>

        <!-- RINGKASAN INTI -->
        <section>
            <h2 class="section-title">Konsep Utama</h2>
            <div class="grid-summary">
                <div class="card">
                    <h3>Cetak Biru Republik Pertama</h3>
                    <p>Karya tertulis tertua yang secara gamblang merumuskan gagasan Negara Republik Indonesia yang berdaulat, jauh sebelum Sumpah Pemuda 1928 dan Proklamasi 1945.</p>
                </div>
                <div class="card">
                    <h3>Kritik Ekonomi Kolonial</h3>
                    <p>Menganalisis secara tajam eksploitasi ekonomi oleh pemerintah kolonial Belanda, kemiskinan tanah, serta penindasan terhadap kaum buruh dan petani.</p>
                </div>
                <div class="card">
                    <h3>Program Politik Total</h3>
                    <p>Menuntut penghentian total kekuasaan kolonial, hak politik penuh untuk pria dan wanita, serta pembentukan Majelis Permusyawaratan Nasional.</p>
                </div>
            </div>
        </section>

        <!-- EXPLORER INTERAKTIF -->
        <section>
            <h2 class="section-title">Detail Pemikiran</h2>
            <div class="tabs-wrapper">
                <div class="tabs-header">
                    <button class="tab-btn active" onclick="openTab(event, 'tab1')">Bentuk Negara</button>
                    <button class="tab-btn" onclick="openTab(event, 'tab2')">Hak & Gender</button>
                    <button class="tab-btn" onclick="openTab(event, 'tab3')">Ekonomi & Bank</button>
                    <button class="tab-btn" onclick="openTab(event, 'tab4')">Majelis Rakyat</button>
                </div>

                <div id="tab1" class="tab-panel active">
                    <h4>Republik Modern vs Kerajaan Tradisional</h4>
                    <p>Tan Malaka menolak gagasan mengembalikan bentuk kerajaan feodal lama atau perserikatan jajahan yang terikat dengan Belanda. Ia menegaskan bahwa Indonesia harus berbentuk <strong>Republik Modern</strong> yang berdaulat penuh.</p>
                    <div class="highlight-box">
                        "Indonesia bukan hanya sekadar bebas dari Belanda, tetapi harus berdiri sebagai Republik yang demokratis dan berdaulat."
                    </div>
                </div>

                <div id="tab2" class="tab-panel">
                    <h4>Kesetaraan Hak Politik & Gender</h4>
                    <p>Pemikiran yang sangat maju pada zamannya. Tan Malaka menuntut hak pilih dan hak politik yang sama tanpa membedakan jenis kelamin, memberikan perempuan ruang penuh dalam kedaulatan negara.</p>
                    <div class="highlight-box">
                        Memperjuangkan hak politik penuh bagi kaum pria maupun wanita tanpa diskriminasi.
                    </div>
                </div>

                <div id="tab3" class="tab-panel">
                    <h4>Nasionalisasi Industri Kunci</h4>
                    <p>Untuk mengakhiri eksploitasi ekonomi, seluruh industri vital, tambang, perbankan, dan aset strategis milik kolonial harus dinasionalisasi demi kemakmuran rakyat banyak.</p>
                    <div class="highlight-box">
                        Penguasaan aset vital negara harus berada di tangan rakyat melalui pemerintah republik.
                    </div>
                </div>

                <div id="tab4" class="tab-panel">
                    <h4>Majelis Permusyawaratan Nasional</h4>
                    <p>Pembentukan lembaga perwakilan rakyat (Majelis Permusyawaratan Nasional) yang mewakili suara kaum terindas, buruh, dan petani sebagai pemegang kekuasaan tertinggi.</p>
                    <div class="highlight-box">
                        Suara massa rakyat yang tertindas menjadi fondasi utama dalam pengambilan keputusan negara.
                    </div>
                </div>
            </div>
        </section>

        <!-- FUN FACTS & CATATAN SEJARAH -->
        <section>
            <h2 class="section-title">Fun Facts & Catatan Sejarah</h2>
            <div class="facts-grid">
                <div class="fact-item">
                    <div class="fact-number">Fact 01</div>
                    <div class="fact-title">Buku 'Haram' yang Harganya Meroket</div>
                    <div class="fact-desc">Karena dilarang keras oleh pemerintah kolonial Belanda, buku ini diselundupkan secara rahasia. Di pasar gelap Hindia Belanda, harganya bisa melambung hingga puluhan kali lipat dari harga asli.</div>
                </div>

                <div class="fact-item">
                    <div class="fact-number">Fact 02</div>
                    <div class="fact-title">20 Tahun Sebelum Proklamasi</div>
                    <div class="fact-desc">Ditulis pada tahun 1925 di Canton (Guangzhou), China. Gagasan konkrit tentang "Republiek Indonesia" ini lahir 20 tahun sebelum Soekarno-Hatta memproklamasikan kemerdekaan pada 1945.</div>
                </div>

                <div class="fact-item">
                    <div class="fact-number">Fact 03</div>
                    <div class="fact-title">Inspirasi Para Tokoh Bangsa</div>
                    <div class="fact-desc">Bung Karno, Bung Hatta, dan Muhammad Yamin membaca serta menjadikan pamflet ini sebagai rujukan utama dalam merumuskan konsep negara Indonesia di sidang BPUPKI.</div>
                </div>

                <div class="fact-item">
                    <div class="fact-number">Fact 04</div>
                    <div class="fact-title">Ditulis Dalam Pelarian</div>
                    <div class="fact-desc">Tan Malaka menulis karya monumental ini saat berada dalam pelarian internasional dari incaran intelijen imperialis di kawasan Asia Pasifik.</div>
                </div>
            </div>
        </section>

        <!-- TIMELINE SINGKAT -->
        <section>
            <h2 class="section-title">Garis Waktu Historis</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">1925</div>
                    <div class="timeline-desc">Tan Malaka menulis dan menerbitkan <em>Naar de 'Republiek Indonesia'</em> di Canton, China.</div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">1928</div>
                    <div class="timeline-desc">Sumpah Pemuda mengikrarkan persatuan identitas bangsa Indonesia.</div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">1945</div>
                    <div class="timeline-desc">Proklamasi Kemerdekaan Indonesia, menguji dan mewujudkan konsep Republik yang dicita-citakan.</div>
                </div>
            </div>
        </section>

        <!-- FOOTER -->
        <footer>
            <p>Disusun untuk tugas & presentasi Sejarah oleh <strong>David XI-2/5</strong></p>
            <p style="margin-top: 6px; font-size: 0.8rem;">Materi: <em>Naar de 'Republiek Indonesia' (1925) - Tan Malaka</em></p>
        </footer>
    </div>

    <!-- JAVASCRIPT UNTUK TAB INTERAKTIF -->
    <script>
        function openTab(evt, tabId) {
            const tabPanels = document.querySelectorAll('.tab-panel');
            tabPanels.forEach(panel => panel.classList.remove('active'));

            const tabBtns = document.querySelectorAll('.tab-btn');
            tabBtns.forEach(btn => btn.classList.remove('active'));

            document.getElementById(tabId).classList.add('active');
            evt.currentTarget.classList.add('active');
        }
    </script>
</body>
</html>
