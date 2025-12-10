<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>40-Minute Chest & Arms Toning Workout Infographic</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Palette: "Energetic & Playful" -->
    <!-- Colors: #FF6B6B (Red/Orange), #4ECDC4 (Teal), #FFE66D (Yellow), #1A535C (Dark Teal), #F7FFF7 (Off-White) -->
    <!-- NO SVG USED. NO MERMAID JS USED. -->

    <style>
        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: #F7FFF7;
            color: #1A535C;
        }
        
        /* Chart Container Styling - Mandatory Requirements */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px; /* Constraint for larger screens */
            margin-left: auto;
            margin-right: auto;
            height: 300px; /* Base height */
            max-height: 400px;
        }

        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }

        /* Custom Scrollbar for a polished look */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1; 
        }
        ::-webkit-scrollbar-thumb {
            background: #4ECDC4; 
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #1A535C; 
        }

        .card-shadow {
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            transition: transform 0.2s;
        }
        .card-shadow:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
    </style>
</head>
<body class="bg-gray-50">

    <!-- Header Section -->
    <header class="bg-[#1A535C] text-white p-8 text-center shadow-lg">
        <h1 class="text-4xl md:text-5xl font-bold mb-2">40-Minute Chest & Arms</h1>
        <p class="text-xl md:text-2xl text-[#4ECDC4] font-light">Toning & Strength Infographic</p>
        <div class="mt-4 flex justify-center space-x-4 text-sm font-semibold">
            <span class="bg-[#FF6B6B] px-3 py-1 rounded-full">High Intensity</span>
            <span class="bg-[#FFE66D] text-[#1A535C] px-3 py-1 rounded-full">Minimal Equipment</span>
            <span class="bg-[#4ECDC4] text-[#1A535C] px-3 py-1 rounded-full">Superset Structure</span>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="container mx-auto px-4 py-8 space-y-12">

        <!-- Introduction -->
        <section class="max-w-4xl mx-auto text-center">
            <h2 class="text-3xl font-bold text-[#FF6B6B] mb-4">Maximize Your Time</h2>
            <p class="text-lg text-gray-700 leading-relaxed">
                This workout is engineered for efficiency. By utilizing <strong>supersets</strong>—performing two exercises back-to-back with minimal rest—we maintain a high heart rate while maximizing muscle engagement. The 40-minute session is strictly divided to ensure every minute contributes to toning your chest, arms, and core.
            </p>
        </section>

        <!-- Section 1: Time Allocation (Donut Chart) -->
        <section class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center bg-white p-6 rounded-xl card-shadow border-l-8 border-[#FF6B6B]">
            <div>
                <h3 class="text-2xl font-bold text-[#1A535C] mb-4">Time Allocation Breakdown</h3>
                <p class="text-gray-600 mb-4">
                    The session is segmented into five distinct phases. Notice that the majority of the time (60%) is dedicated to the core working sets (Superset Blocks A and B), ensuring muscle stimulus is the priority.
                </p>
                <ul class="space-y-2">
                    <li class="flex items-center"><span class="w-3 h-3 bg-[#4ECDC4] rounded-full mr-2"></span>Warm-up: Activation & Mobility</li>
                    <li class="flex items-center"><span class="w-3 h-3 bg-[#FF6B6B] rounded-full mr-2"></span>Block A: Chest & Biceps</li>
                    <li class="flex items-center"><span class="w-3 h-3 bg-[#1A535C] rounded-full mr-2"></span>Block B: Triceps & Back</li>
                    <li class="flex items-center"><span class="w-3 h-3 bg-[#FFE66D] rounded-full mr-2"></span>Finisher: Core & Conditioning</li>
                    <li class="flex items-center"><span class="w-3 h-3 bg-gray-400 rounded-full mr-2"></span>Cool-down: Recovery</li>
                </ul>
            </div>
            <div class="flex flex-col items-center">
                <div class="chart-container">
                    <canvas id="timeChart"></canvas>
                </div>
                <p class="text-xs text-gray-400 mt-2 italic">Data: Duration in Minutes</p>
            </div>
        </section>

        <!-- Section 2: Workout Intensity Curve (Line Chart) -->
        <section class="bg-white p-6 rounded-xl card-shadow border-l-8 border-[#4ECDC4]">
            <div class="mb-6">
                <h3 class="text-2xl font-bold text-[#1A535C] mb-2">Estimated Intensity Curve</h3>
                <p class="text-gray-600">
                    This chart visualizes the projected intensity (Heart Rate / Perceived Exertion) throughout the 40 minutes. The workout builds during the supersets, peaks during the high-intensity "Finisher," and drops sharply for the cool-down.
                </p>
            </div>
            <div class="chart-container" style="max-width: 800px;">
                <canvas id="intensityChart"></canvas>
            </div>
        </section>

        <!-- Section 3: The Workout Flow (Structured HTML Cards) -->
        <section>
            <h2 class="text-3xl font-bold text-center text-[#1A535C] mb-8">Session Workflow</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                
                <!-- Warm Up -->
                <div class="bg-white rounded-lg p-6 card-shadow border-t-4 border-[#4ECDC4]">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-xl font-bold text-[#1A535C]">01. Warm-Up</h4>
                        <span class="bg-[#4ECDC4] text-white text-xs px-2 py-1 rounded">5 Min</span>
                    </div>
                    <p class="text-sm text-gray-600 mb-4">Dynamic movements to prep joints.</p>
                    <ul class="text-sm space-y-2 text-gray-700">
                        <li>&#8635; Arm Circles (45s)</li>
                        <li>&#8593; Shoulder Shrugs (45s)</li>
                        <li>&#8646; Torso Twists (45s)</li>
                        <li>&#9650; Incline Push-ups (45s)</li>
                        <li>&#9733; Jumping Jacks (45s)</li>
                    </ul>
                </div>

                <!-- Block A -->
                <div class="bg-white rounded-lg p-6 card-shadow border-t-4 border-[#FF6B6B] md:col-span-2">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-xl font-bold text-[#1A535C]">02. Block A: Chest & Biceps</h4>
                        <span class="bg-[#FF6B6B] text-white text-xs px-2 py-1 rounded">12 Min</span>
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div class="bg-red-50 p-4 rounded">
                            <h5 class="font-bold text-[#FF6B6B]">Superset 1</h5>
                            <p class="font-semibold">Dumbbell Chest Press</p>
                            <p class="text-sm text-gray-600">10-12 Reps</p>
                            <p class="text-xs text-gray-500 mt-1">Focus: Pectorals</p>
                        </div>
                        <div class="bg-red-50 p-4 rounded">
                            <h5 class="font-bold text-[#FF6B6B]">Superset 2</h5>
                            <p class="font-semibold">Hammer Curls</p>
                            <p class="text-sm text-gray-600">12-15 Reps</p>
                            <p class="text-xs text-gray-500 mt-1">Focus: Biceps / Brachialis</p>
                        </div>
                    </div>
                    <p class="text-center text-xs font-bold text-gray-400 mt-4 uppercase tracking-widest">Perform 3 Rounds &bull; 60s Rest</p>
                </div>

                <!-- Block B -->
                <div class="bg-white rounded-lg p-6 card-shadow border-t-4 border-[#1A535C] md:col-span-2">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-xl font-bold text-[#1A535C]">03. Block B: Arms Focus</h4>
                        <span class="bg-[#1A535C] text-white text-xs px-2 py-1 rounded">12 Min</span>
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div class="bg-teal-50 p-4 rounded">
                            <h5 class="font-bold text-[#1A535C]">Superset 1</h5>
                            <p class="font-semibold">Overhead Triceps Ext.</p>
                            <p class="text-sm text-gray-600">12-15 Reps</p>
                            <p class="text-xs text-gray-500 mt-1">Focus: Triceps Long Head</p>
                        </div>
                        <div class="bg-teal-50 p-4 rounded">
                            <h5 class="font-bold text-[#1A535C]">Superset 2</h5>
                            <p class="font-semibold">Dumbbell Bent-Over Row</p>
                            <p class="text-sm text-gray-600">10-12 Reps/Arm</p>
                            <p class="text-xs text-gray-500 mt-1">Focus: Back & Biceps</p>
                        </div>
                    </div>
                    <p class="text-center text-xs font-bold text-gray-400 mt-4 uppercase tracking-widest">Perform 3 Rounds &bull; 60s Rest</p>
                </div>

                <!-- Finisher -->
                <div class="bg-white rounded-lg p-6 card-shadow border-t-4 border-[#FFE66D]">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-xl font-bold text-[#1A535C]">04. Finisher</h4>
                        <span class="bg-[#FFE66D] text-[#1A535C] text-xs px-2 py-1 rounded">6 Min</span>
                    </div>
                    <p class="text-sm text-gray-600 mb-4">High intensity interval training.</p>
                    <ul class="text-sm space-y-2 text-gray-700">
                        <li>&#9642; Plank (45s)</li>
                        <li>&#9642; High Knees (60s)</li>
                        <li>&#9642; Mountain Climbers (45s)</li>
                    </ul>
                    <p class="text-xs text-gray-400 mt-4 text-center">2 Rounds Total</p>
                </div>
            </div>
        </section>

        <!-- Section 4: Target Analysis (Radar & Bar) -->
        <section class="grid grid-cols-1 md:grid-cols-2 gap-8">
            
            <!-- Radar Chart: Target Areas -->
            <div class="bg-white p-6 rounded-xl card-shadow">
                <h3 class="text-xl font-bold text-[#1A535C] mb-4">Muscle Focus Distribution</h3>
                <p class="text-gray-600 text-sm mb-4">
                    This radar chart illustrates the balance of the workout. While "Chest" and "Arms" are the primary goals, the inclusion of rows and the finisher ensures a balanced engagement of the Back and Core, with a significant Cardio spike.
                </p>
                <div class="chart-container">
                    <canvas id="radarChart"></canvas>
                </div>
            </div>

            <!-- Bar Chart: Rep Volume -->
            <div class="bg-white p-6 rounded-xl card-shadow">
                <h3 class="text-xl font-bold text-[#1A535C] mb-4">Volume Strategy: Rep Ranges</h3>
                <p class="text-gray-600 text-sm mb-4">
                    Different muscle groups respond to different volume loads. We use higher reps (12-15) for smaller isolation muscles like Biceps and Triceps to induce metabolic stress, and moderate reps (10-12) for larger compound movements like Chest Press and Rows.
                </p>
                <div class="chart-container">
                    <canvas id="barChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Cool Down Section -->
        <section class="bg-[#1A535C] text-white p-8 rounded-xl shadow-lg text-center">
            <h2 class="text-2xl font-bold mb-4 text-[#4ECDC4]">05. Cool-Down & Recovery (5 Min)</h2>
            <p class="max-w-2xl mx-auto mb-6">
                Recovery is where the growth happens. Spend 30 seconds on each stretch. Breathe deeply.
            </p>
            <div class="flex flex-wrap justify-center gap-4 text-sm font-semibold">
                <span class="border border-[#4ECDC4] px-4 py-2 rounded-lg">Chest Stretch</span>
                <span class="border border-[#4ECDC4] px-4 py-2 rounded-lg">Triceps Stretch</span>
                <span class="border border-[#4ECDC4] px-4 py-2 rounded-lg">Biceps Stretch</span>
                <span class="border border-[#4ECDC4] px-4 py-2 rounded-lg">Child's Pose</span>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="text-center py-8 text-gray-500 text-sm">
        <p>&copy; 2023 Workout Infographic Generator. Consult a physician before starting any new exercise routine.</p>
    </footer>

    <!-- Chart.js Logic -->
    <script>
        // --- Helper Function for Label Wrapping ---
        function wrapLabel(label) {
            if (typeof label === 'string' && label.length > 16) {
                const words = label.split(' ');
                const lines = [];
                let currentLine = words[0];

                for (let i = 1; i < words.length; i++) {
                    if ((currentLine + " " + words[i]).length <= 16) {
                        currentLine += " " + words[i];
                    } else {
                        lines.push(currentLine);
                        currentLine = words[i];
                    }
                }
                lines.push(currentLine);
                return lines;
            }
            return label;
        }

        // --- Common Tooltip Configuration ---
        const commonTooltipOptions = {
            callbacks: {
                title: function(tooltipItems) {
                    const item = tooltipItems[0];
                    let label = item.chart.data.labels[item.dataIndex];
                    if (Array.isArray(label)) {
                        return label.join(' ');
                    } else {
                        return label;
                    }
                }
            }
        };

        // --- Chart 1: Time Allocation (Doughnut) ---
        const timeCtx = document.getElementById('timeChart').getContext('2d');
        const timeLabels = ['Warm Up', 'Block A (Chest)', 'Block B (Arms)', 'Finisher', 'Cool Down'];
        const processedTimeLabels = timeLabels.map(wrapLabel);

        new Chart(timeCtx, {
            type: 'doughnut',
            data: {
                labels: processedTimeLabels,
                datasets: [{
                    data: [5, 12, 12, 6, 5], // Minutes
                    backgroundColor: [
                        '#4ECDC4', // Warmup (Teal)
                        '#FF6B6B', // Block A (Red)
                        '#1A535C', // Block B (Dark Teal)
                        '#FFE66D', // Finisher (Yellow)
                        '#C7C7C7'  // Cool Down (Grey)
                    ],
                    borderWidth: 0
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: {
                            boxWidth: 12,
                            padding: 15,
                            font: { size: 11 }
                        }
                    },
                    tooltip: { ...commonTooltipOptions }
                },
                cutout: '60%'
            }
        });

        // --- Chart 2: Intensity Curve (Line) ---
        const intensityCtx = document.getElementById('intensityChart').getContext('2d');
        const intensityLabels = ['Start', 'Warmup', 'Block A Start', 'Block A Peak', 'Block B Start', 'Block B Peak', 'Finisher Start', 'Finisher Peak', 'Cool Down'];
        const processedIntensityLabels = intensityLabels.map(wrapLabel);

        new Chart(intensityCtx, {
            type: 'line',
            data: {
                labels: processedIntensityLabels,
                datasets: [{
                    label: 'Estimated Heart Rate / Intensity',
                    data: [60, 100, 110, 140, 130, 150, 160, 175, 90],
                    borderColor: '#FF6B6B',
                    backgroundColor: 'rgba(255, 107, 107, 0.1)',
                    fill: true,
                    tension: 0.4,
                    pointBackgroundColor: '#1A535C',
                    pointRadius: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        max: 200,
                        title: { display: true, text: 'Intensity %' }
                    },
                    x: {
                        ticks: {
                            maxRotation: 45,
                            minRotation: 0
                        }
                    }
                },
                plugins: {
                    legend: { display: false },
                    tooltip: { ...commonTooltipOptions }
                }
            }
        });

        // --- Chart 3: Muscle Focus (Radar) ---
        const radarCtx = document.getElementById('radarChart').getContext('2d');
        const radarLabels = ['Chest Pectorals', 'Triceps Brachii', 'Biceps Brachii', 'Upper Back', 'Core Stability', 'Cardio System'];
        const processedRadarLabels = radarLabels.map(wrapLabel);

        new Chart(radarCtx, {
            type: 'radar',
            data: {
                labels: processedRadarLabels,
                datasets: [{
                    label: 'Focus Level (1-10)',
                    data: [9, 8, 8, 6, 7, 8],
                    backgroundColor: 'rgba(78, 205, 196, 0.4)',
                    borderColor: '#4ECDC4',
                    pointBackgroundColor: '#1A535C',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: '#1A535C'
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    r: {
                        angleLines: { color: 'rgba(0,0,0,0.1)' },
                        grid: { color: 'rgba(0,0,0,0.1)' },
                        pointLabels: {
                            font: { size: 12 },
                            color: '#1A535C'
                        },
                        suggestedMin: 0,
                        suggestedMax: 10
                    }
                },
                plugins: {
                    legend: { display: false },
                    tooltip: { ...commonTooltipOptions }
                }
            }
        });

        // --- Chart 4: Rep Ranges (Bar) ---
        const barCtx = document.getElementById('barChart').getContext('2d');
        const barLabels = ['Chest Press', 'Hammer Curls', 'Triceps Ext.', 'Bent-Over Row'];
        const processedBarLabels = barLabels.map(wrapLabel);

        new Chart(barCtx, {
            type: 'bar',
            data: {
                labels: processedBarLabels,
                datasets: [{
                    label: 'Max Rep Target',
                    data: [12, 15, 15, 12],
                    backgroundColor: [
                        '#FF6B6B',
                        '#FFE66D',
                        '#4ECDC4',
                        '#1A535C'
                    ],
                    borderRadius: 5,
                    borderSkipped: false
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        title: { display: true, text: 'Reps per Set' }
                    }
                },
                plugins: {
                    legend: { display: false },
                    tooltip: { ...commonTooltipOptions }
                }
            }
        });
    </script>
</body>
</html>
