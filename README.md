<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MadeToStick Title Generator - Amazon SEO Tool</title>
    <meta name="description" content="Generate optimized Amazon listing titles for MadeToStick stickers with SEO scoring and mobile preview">
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Space Mono', monospace;
            background: linear-gradient(135deg, #fde047 0%, #fda4af 50%, #93c5fd 100%);
            min-height: 100vh;
            padding: 2rem;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        /* Decorative elements */
        .decoration {
            position: fixed;
            border-radius: 50%;
            opacity: 0.2;
            filter: blur(60px);
            animation: pulse 3s ease-in-out infinite;
        }

        .decoration-1 {
            top: 10%;
            right: 10%;
            width: 128px;
            height: 128px;
            background: #ec4899;
        }

        .decoration-2 {
            bottom: 20%;
            left: 20%;
            width: 160px;
            height: 160px;
            background: #3b82f6;
            animation-delay: 1s;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.2; transform: scale(1); }
            50% { opacity: 0.3; transform: scale(1.1); }
        }

        /* Header */
        .header {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .header h1 {
            font-family: 'Archivo Black', sans-serif;
            font-size: 4.5rem;
            color: white;
            text-shadow: 4px 4px 0px rgba(0,0,0,0.2), 6px 6px 0px rgba(0,0,0,0.1);
            -webkit-text-stroke: 2px rgba(0,0,0,0.1);
            position: relative;
            display: inline-block;
        }

        .header p {
            font-family: 'Space Mono', monospace;
            font-size: 1.25rem;
            font-weight: 700;
            color: #1f2937;
            margin-top: 1rem;
            letter-spacing: 0.05em;
        }

        /* Grid */
        .grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        @media (max-width: 968px) {
            .grid {
                grid-template-columns: 1fr;
            }
            .header h1 {
                font-size: 3rem;
            }
        }

        /* Cards */
        .card {
            background: white;
            border-radius: 24px;
            padding: 2rem;
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
            position: relative;
            overflow: hidden;
        }

        .card-decoration {
            position: absolute;
            opacity: 0.3;
        }

        .card-decoration-1 {
            top: 0;
            right: 0;
            width: 128px;
            height: 128px;
            background: linear-gradient(135deg, #fef3c7 0%, #fecaca 100%);
            border-bottom-left-radius: 100%;
        }

        .card-decoration-2 {
            bottom: 0;
            left: 0;
            width: 128px;
            height: 128px;
            background: linear-gradient(45deg, #dbeafe 0%, #d9f99d 100%);
            border-top-right-radius: 100%;
        }

        .card-content {
            position: relative;
            z-index: 10;
        }

        .card h2 {
            font-family: 'Archivo Black', sans-serif;
            font-size: 2rem;
            color: #1f2937;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        /* Form elements */
        .form-group {
            margin-bottom: 1.25rem;
        }

        label {
            display: block;
            font-weight: 700;
            font-size: 0.875rem;
            color: #374151;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        input[type="text"],
        select {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 3px solid #d1d5db;
            border-radius: 12px;
            font-family: 'Space Mono', monospace;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.2s;
        }

        input[type="text"]:focus,
        select:focus {
            outline: none;
            border-color: #ec4899;
            box-shadow: 0 0 0 4px rgba(236, 72, 153, 0.2);
        }

        /* Toggle row */
        .toggle-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin-bottom: 1.25rem;
        }

        .toggle-card {
            padding: 1rem;
            border-radius: 12px;
            border: 2px solid;
        }

        .toggle-card.waterproof {
            background: #dbeafe;
            border-color: #93c5fd;
        }

        .toggle-card.language {
            background: #f3e8ff;
            border-color: #d8b4fe;
        }

        .checkbox-label {
            display: flex;
            align-items: center;
            cursor: pointer;
            font-weight: 700;
            color: #1f2937;
            text-transform: none;
            margin: 0;
        }

        input[type="checkbox"] {
            width: 1.25rem;
            height: 1.25rem;
            margin-right: 0.75rem;
            cursor: pointer;
        }

        .language-select {
            margin-top: 0.25rem;
            padding: 0.375rem 0.5rem;
            border: 2px solid #c084fc;
            font-size: 0.875rem;
        }

        /* Positioning buttons */
        .positioning-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 0.5rem;
        }

        .positioning-btn {
            padding: 0.75rem 1rem;
            border: none;
            border-radius: 12px;
            font-family: 'Space Mono', monospace;
            font-weight: 700;
            font-size: 0.875rem;
            text-transform: uppercase;
            cursor: pointer;
            transition: all 0.2s;
            background: #f3f4f6;
            color: #374151;
        }

        .positioning-btn:hover {
            background: #e5e7eb;
            transform: scale(1.05);
        }

        .positioning-btn.active {
            background: linear-gradient(135deg, #ec4899 0%, #a855f7 100%);
            color: white;
            box-shadow: 0 4px 12px rgba(168, 85, 247, 0.4);
        }

        /* Generate button */
        .generate-btn {
            width: 100%;
            padding: 1.5rem;
            border: none;
            border-radius: 16px;
            background: linear-gradient(135deg, #fbbf24 0%, #ec4899 50%, #3b82f6 100%);
            color: white;
            font-family: 'Archivo Black', sans-serif;
            font-size: 1.25rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            cursor: pointer;
            transition: all 0.2s;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.75rem;
            margin-top: 1.5rem;
        }

        .generate-btn:hover {
            box-shadow: 0 8px 30px rgba(0,0,0,0.3);
            transform: scale(1.02);
        }

        /* Results */
        .results-empty {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 300px;
            color: #9ca3af;
            text-align: center;
        }

        .results-empty p {
            font-weight: 700;
            margin-top: 1rem;
        }

        .results-container {
            max-height: 600px;
            overflow-y: auto;
            padding-right: 0.5rem;
        }

        .title-card {
            background: linear-gradient(135deg, #f9fafb 0%, #f3f4f6 100%);
            border: 2px solid #d1d5db;
            border-radius: 16px;
            padding: 1.25rem;
            margin-bottom: 1rem;
            transition: all 0.2s;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .title-card:hover {
            border-color: #ec4899;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }

        .title-text {
            font-size: 0.875rem;
            font-weight: 700;
            line-height: 1.6;
            margin-bottom: 0.75rem;
            color: #111827;
        }

        .title-mobile {
            color: #ec4899;
        }

        .title-rest {
            color: #6b7280;
        }

        .title-metrics {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 0.75rem;
            flex-wrap: wrap;
            gap: 0.75rem;
        }

        .metrics-badges {
            display: flex;
            gap: 0.75rem;
        }

        .badge {
            font-size: 0.75rem;
            font-weight: 700;
            padding: 0.375rem 0.75rem;
            border-radius: 9999px;
        }

        .badge-chars {
            background: #dbeafe;
            color: #1e40af;
        }

        .badge-seo-high {
            background: #dcfce7;
            color: #166534;
        }

        .badge-seo-med {
            background: #fef3c7;
            color: #92400e;
        }

        .badge-seo-low {
            background: #fed7aa;
            color: #9a3412;
        }

        .copy-btn {
            background: linear-gradient(135deg, #a855f7 0%, #ec4899 100%);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 12px;
            font-family: 'Space Mono', monospace;
            font-weight: 700;
            font-size: 0.875rem;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .copy-btn:hover {
            box-shadow: 0 4px 12px rgba(168, 85, 247, 0.4);
            transform: scale(1.05);
        }

        .mobile-indicator {
            font-size: 0.75rem;
            color: #6b7280;
            font-weight: 600;
            background: #fce7f3;
            padding: 0.5rem 0.75rem;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .mobile-indicator-dot {
            width: 8px;
            height: 8px;
            background: #ec4899;
            border-radius: 50%;
        }

        /* Tips section */
        .tips-section {
            background: rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(20px);
            border: 2px solid white;
            border-radius: 24px;
            padding: 2rem;
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
        }

        .tips-section h3 {
            font-family: 'Archivo Black', sans-serif;
            font-size: 1.5rem;
            color: #1f2937;
            margin-bottom: 1rem;
        }

        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1rem;
        }

        .tip-card {
            padding: 1rem;
            border-radius: 12px;
            border: 2px solid;
        }

        .tip-card.yellow {
            background: #fef3c7;
            border-color: #fde047;
        }

        .tip-card.blue {
            background: #dbeafe;
            border-color: #93c5fd;
        }

        .tip-card.pink {
            background: #fce7f3;
            border-color: #fbcfe8;
        }

        .tip-card p:first-child {
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .tip-card p:last-child {
            font-size: 0.875rem;
            line-height: 1.5;
        }

        /* Icons */
        .icon {
            width: 24px;
            height: 24px;
            display: inline-block;
            vertical-align: middle;
        }

        .icon-sm {
            width: 16px;
            height: 16px;
        }

        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #ec4899, #8b5cf6);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(to bottom, #db2777, #7c3aed);
        }
    </style>
</head>
<body>
    <div class="decoration decoration-1"></div>
    <div class="decoration decoration-2"></div>

    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>MadeToStick</h1>
            <p>Title Generator: Amazon Edition</p>
        </div>

        <!-- Main Grid -->
        <div class="grid">
            <!-- Input Form -->
            <div class="card">
                <div class="card-decoration card-decoration-1"></div>
                <div class="card-content">
                    <h2>
                        <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" style="color: #eab308;">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path>
                        </svg>
                        Build Your Title
                    </h2>

                    <form id="titleForm">
                        <!-- Design Theme -->
                        <div class="form-group">
                            <label for="design">Design Theme *</label>
                            <input type="text" id="design" placeholder="e.g., Aesthetic Flowers, Retro Gaming, Cute Animals" required>
                        </div>

                        <!-- Size -->
                        <div class="form-group">
                            <label for="size">Size (inches)</label>
                            <input type="text" id="size" placeholder="e.g., 3, 2-4, Large">
                        </div>

                        <!-- Quantity -->
                        <div class="form-group">
                            <label for="quantity">Quantity</label>
                            <input type="text" id="quantity" placeholder="e.g., 50, 100">
                        </div>

                        <!-- Material -->
                        <div class="form-group">
                            <label for="material">Material</label>
                            <select id="material">
                                <option value="vinyl">Vinyl</option>
                                <option value="holographic">Holographic</option>
                                <option value="matte">Matte</option>
                                <option value="glossy">Glossy</option>
                                <option value="puffy">Puffy/3D</option>
                                <option value="clear">Clear/Transparent</option>
                            </select>
                        </div>

                        <!-- Use Case -->
                        <div class="form-group">
                            <label for="useCase">Use Case</label>
                            <select id="useCase">
                                <option value="">Select use case</option>
                                <option value="laptop">Laptop</option>
                                <option value="waterBottle">Water Bottle</option>
                                <option value="phone">Phone Case</option>
                                <option value="car">Car/Bumper</option>
                                <option value="notebook">Notebook/Planner</option>
                                <option value="skateboard">Skateboard</option>
                                <option value="general">General/Multi-use</option>
                            </select>
                        </div>

                        <!-- Toggles Row -->
                        <div class="toggle-row">
                            <div class="toggle-card waterproof">
                                <label class="checkbox-label">
                                    <input type="checkbox" id="waterproof" checked>
                                    <span>Waterproof</span>
                                </label>
                            </div>

                            <div class="toggle-card language">
                                <label style="font-size: 0.75rem; margin-bottom: 0.25rem;">Language</label>
                                <select id="language" class="language-select">
                                    <option value="english">English</option>
                                    <option value="spanish">Español</option>
                                </select>
                            </div>
                        </div>

                        <!-- Positioning -->
                        <div class="form-group">
                            <label>Brand Positioning</label>
                            <div class="positioning-grid">
                                <button type="button" class="positioning-btn" data-pos="value">Value</button>
                                <button type="button" class="positioning-btn active" data-pos="mid-range">Mid-Range</button>
                                <button type="button" class="positioning-btn" data-pos="premium">Premium</button>
                            </div>
                        </div>

                        <!-- Generate Button -->
                        <button type="submit" class="generate-btn">
                            <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path>
                            </svg>
                            Generate Titles
                            <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path>
                            </svg>
                        </button>
                    </form>
                </div>
            </div>

            <!-- Results -->
            <div class="card">
                <div class="card-decoration card-decoration-2"></div>
                <div class="card-content">
                    <h2>
                        <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" style="color: #22c55e;">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"></path>
                        </svg>
                        Your Titles
                    </h2>

                    <div id="resultsContainer">
                        <div class="results-empty">
                            <div>
                                <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" style="width: 64px; height: 64px; margin: 0 auto; opacity: 0.3;">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path>
                                </svg>
                                <p>Fill in the form and hit Generate!</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Tips Section -->
        <div class="tips-section">
            <h3>Amazon Title Strategy Notes</h3>
            <div class="tips-grid">
                <div class="tip-card yellow">
                    <p style="color: #78350f;">📱 Mobile First</p>
                    <p style="color: #92400e;">First 150 characters are all mobile users see. Put your strongest keywords + brand there.</p>
                </div>
                <div class="tip-card blue">
                    <p style="color: #1e3a8a;">🎯 SEO Hierarchy</p>
                    <p style="color: #1e40af;">Design theme → Material → Use case → Brand. Spanish market is 25% and underserved.</p>
                </div>
                <div class="tip-card pink">
                    <p style="color: #831843;">💎 Value Props</p>
                    <p style="color: #9f1239;">Waterproof = trust. Specialty materials (holographic/puffy) should lead. Quantity = value play.</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Material options
        const materialOptions = {
            vinyl: 'Vinyl',
            holographic: 'Holographic',
            matte: 'Matte',
            glossy: 'Glossy',
            puffy: 'Puffy/3D',
            clear: 'Clear/Transparent'
        };

        // Use case options
        const useCaseOptions = {
            laptop: 'Laptop',
            waterBottle: 'Water Bottle',
            phone: 'Phone Case',
            car: 'Car/Bumper',
            notebook: 'Notebook/Planner',
            skateboard: 'Skateboard',
            general: 'General/Multi-use'
        };

        // Positioning state
        let selectedPositioning = 'mid-range';

        // Positioning buttons
        document.querySelectorAll('.positioning-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.positioning-btn').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                selectedPositioning = btn.dataset.pos;
            });
        });

        // Form submission
        document.getElementById('titleForm').addEventListener('submit', (e) => {
            e.preventDefault();
            generateTitles();
        });

        function generateTitles() {
            const design = document.getElementById('design').value.trim();
            const size = document.getElementById('size').value.trim();
            const quantity = document.getElementById('quantity').value.trim();
            const material = document.getElementById('material').value;
            const waterproof = document.getElementById('waterproof').checked;
            const useCase = document.getElementById('useCase').value;
            const language = document.getElementById('language').value;

            if (!design) {
                alert('Please enter a design theme');
                return;
            }

            const titles = [];
            const isSpanish = language === 'spanish';
            
            const waterproofText = waterproof ? (isSpanish ? 'Impermeables' : 'Waterproof') : '';
            const materialText = materialOptions[material];
            const quantityText = quantity ? `${quantity} Pack` : '';
            const useCaseText = useCase ? useCaseOptions[useCase] : '';
            const sizeText = size ? `${size}"` : '';

            // Strategy 1: Front-load brand + design (mobile-first)
            if (selectedPositioning === 'premium') {
                titles.push(
                    isSpanish
                        ? `MadeToStick ${design} - Calcomanías ${materialText} Premium ${waterproofText} ${quantityText} ${sizeText} ${useCaseText}`.trim().replace(/\s+/g, ' ')
                        : `MadeToStick ${design} Premium ${materialText} Stickers ${waterproofText} ${quantityText} ${sizeText} for ${useCaseText}`.trim().replace(/\s+/g, ' ')
                );
            }

            // Strategy 2: SEO-heavy (design + use case first)
            titles.push(
                isSpanish
                    ? `${design} Calcomanías ${waterproofText} ${materialText} para ${useCaseText} | MadeToStick ${quantityText} ${sizeText}`.trim().replace(/\s+/g, ' ')
                    : `${design} Stickers ${waterproofText} ${materialText} for ${useCaseText} | MadeToStick Brand ${quantityText} ${sizeText}`.trim().replace(/\s+/g, ' ')
            );

            // Strategy 3: Benefit-first (waterproof/durable lead)
            if (waterproof) {
                titles.push(
                    isSpanish
                        ? `Calcomanías Impermeables ${design} ${materialText} - MadeToStick ${quantityText} ${sizeText} para ${useCaseText}`.trim().replace(/\s+/g, ' ')
                        : `Waterproof ${design} ${materialText} Stickers - MadeToStick ${quantityText} ${sizeText} for ${useCaseText}`.trim().replace(/\s+/g, ' ')
                );
            }

            // Strategy 4: Quantity-first (for value positioning)
            if (quantity && selectedPositioning === 'value') {
                titles.push(
                    isSpanish
                        ? `${quantityText} Calcomanías ${design} ${waterproofText} ${materialText} MadeToStick ${sizeText} para ${useCaseText}`.trim().replace(/\s+/g, ' ')
                        : `${quantityText} ${design} Stickers ${waterproofText} ${materialText} - MadeToStick ${sizeText} for ${useCaseText}`.trim().replace(/\s+/g, ' ')
                );
            }

            // Strategy 5: Material-first (for specialty materials)
            if (material === 'holographic' || material === 'puffy') {
                titles.push(
                    isSpanish
                        ? `Calcomanías ${materialText} ${design} ${waterproofText} MadeToStick ${quantityText} ${sizeText}`.trim().replace(/\s+/g, ' ')
                        : `${materialText} ${design} Stickers ${waterproofText} MadeToStick ${quantityText} ${sizeText} for ${useCaseText}`.trim().replace(/\s+/g, ' ')
                );
            }

            // Strategy 6: Use case dominant
            if (useCase && useCase !== 'general') {
                titles.push(
                    isSpanish
                        ? `Calcomanías para ${useCaseText} - ${design} ${waterproofText} ${materialText} MadeToStick ${quantityText}`.trim().replace(/\s+/g, ' ')
                        : `${useCaseText} Stickers - ${design} ${waterproofText} ${materialText} MadeToStick Brand ${quantityText}`.trim().replace(/\s+/g, ' ')
                );
            }

            // Strategy 7: Brand-first for premium
            if (selectedPositioning === 'premium') {
                titles.push(
                    isSpanish
                        ? `MadeToStick | Calcomanías Premium ${design} ${materialText} ${waterproofText} ${sizeText} ${quantityText}`.trim().replace(/\s+/g, ' ')
                        : `MadeToStick Brand | Premium ${design} ${materialText} Stickers ${waterproofText} ${sizeText} ${quantityText}`.trim().replace(/\s+/g, ' ')
                );
            }

            displayResults(titles.filter(t => t.length > 0));
        }

        function getSEOScore(title) {
            let score = 0;
            
            if (title.toLowerCase().includes('madetostick')) score += 20;
            
            const first50 = title.slice(0, 50).toLowerCase();
            if (first50.includes('sticker') || first50.includes('calcomanía')) score += 25;
            
            if (title.toLowerCase().includes('waterproof') || title.toLowerCase().includes('impermeable')) score += 15;
            
            const first100 = title.slice(0, 100).toLowerCase();
            if (Object.keys(materialOptions).some(mat => first100.includes(mat.toLowerCase()))) score += 15;
            
            if (Object.values(useCaseOptions).some(uc => title.toLowerCase().includes(uc.toLowerCase()))) score += 15;
            
            if (title.length >= 50 && title.length <= 200) score += 10;
            
            return score;
        }

        function displayResults(titles) {
            const container = document.getElementById('resultsContainer');
            
            if (titles.length === 0) {
                container.innerHTML = `
                    <div class="results-empty">
                        <div>
                            <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" style="width: 64px; height: 64px; margin: 0 auto; opacity: 0.3;">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path>
                            </svg>
                            <p>Fill in the form and hit Generate!</p>
                        </div>
                    </div>
                `;
                return;
            }

            const html = `
                <div class="results-container">
                    ${titles.map((title, index) => {
                        const mobilePreview = title.slice(0, 150);
                        const rest = title.slice(150);
                        const seoScore = getSEOScore(title);
                        const seoClass = seoScore >= 80 ? 'badge-seo-high' : seoScore >= 60 ? 'badge-seo-med' : 'badge-seo-low';
                        
                        return `
                            <div class="title-card">
                                <div class="title-text">
                                    <span class="title-mobile">${mobilePreview}</span>${rest ? `<span class="title-rest">${rest}</span>` : ''}
                                </div>
                                
                                <div class="title-metrics">
                                    <div class="metrics-badges">
                                        <span class="badge badge-chars">${title.length} chars</span>
                                        <span class="badge ${seoClass}">SEO: ${seoScore}%</span>
                                    </div>
                                    
                                    <button class="copy-btn" onclick="copyTitle('${title.replace(/'/g, "\\'")}', ${index})">
                                        <svg class="icon-sm" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
                                        </svg>
                                        <span id="copyText${index}">Copy</span>
                                    </button>
                                </div>
                                
                                ${rest ? `
                                    <div class="mobile-indicator">
                                        <div class="mobile-indicator-dot"></div>
                                        First 150 chars shown in pink = mobile view
                                    </div>
                                ` : ''}
                            </div>
                        `;
                    }).join('')}
                </div>
            `;
            
            container.innerHTML = html;
        }

        function copyTitle(text, index) {
            navigator.clipboard.writeText(text).then(() => {
                const btn = document.getElementById(`copyText${index}`);
                btn.textContent = 'Copied!';
                setTimeout(() => {
                    btn.textContent = 'Copy';
                }, 2000);
            });
        }
    </script>
</body>
</html>
