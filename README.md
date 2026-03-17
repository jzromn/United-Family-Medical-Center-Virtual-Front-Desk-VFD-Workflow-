# United-Family-Medical-Center-Virtual-Front-Desk-VFD-Workflow-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UFMC Medical Virtual Front Desk Workflow</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'blue-primary': '#0056D2', // Main brand blue
                        'blue-secondary': '#E6F0FF', // Very pale background blue
                        'blue-accent': '#007BFF', // Interative accent blue
                        'blue-text': '#001F4D', // Deep dark blue for text
                        'blue-muted': '#A0C4FF', // Light blue borders/details
                    }
                }
            }
        }
    </script>
    <style>
        /* Flowchart Arrow connection logic (simplified) */
        .card-container { position: relative; }
        .flow-arrow {
            position: absolute;
            color: #A0C4FF;
            pointer-events: none;
        }
        /* Connect Shift Start -> Setup -> Active Handling */
        #arrow-start-setup { top: 7rem; left: calc(50% - 0.5rem); }
        #arrow-setup-call { top: 15rem; left: calc(50% - 0.5rem); }
        /* Connect Call Handling -> Core Actions */
        #arrow-call-actions { top: 23rem; left: calc(50% - 0.5rem); }
        /* Connect Core Actions -> Escalations */
        #arrow-actions-escl { top: 31rem; left: calc(50% - 0.5rem); }
        /* Connect Call Log -> (Internal workflow connection) */
    </style>
</head>
<body class="bg-blue-secondary text-blue-text p-4 md:p-8">

    <header class="text-center mb-12">
        <h1 class="text-4xl font-bold text-blue-primary">Medical Virtual Front Desk</h1>
        <p class="text-xl text-blue-accent mt-2">United Family Medical Center - Workflow Visualization</p>
        <span class="inline-block mt-4 bg-white text-blue-primary font-medium px-4 py-1 rounded-full border border-blue-muted">8 AM – 5 PM EST</span>
    </header>

    <div class="grid grid-cols-1 md:grid-cols-12 gap-6 card-container">

        <svg class="flow-arrow hidden md:block" id="arrow-start-setup" width="16" height="48" viewBox="0 0 16 48"><path fill="currentColor" d="M11 0v40h5l-8 8-8-8h5v-40h6z"/></svg>
        <svg class="flow-arrow hidden md:block" id="arrow-setup-call" width="16" height="48" viewBox="0 0 16 48"><path fill="currentColor" d="M11 0v40h5l-8 8-8-8h5v-40h6z"/></svg>
        <svg class="flow-arrow hidden md:block" id="arrow-call-actions" width="16" height="48" viewBox="0 0 16 48"><path fill="currentColor" d="M11 0v40h5l-8 8-8-8h5v-40h6z"/></svg>
        <svg class="flow-arrow hidden md:block" id="arrow-actions-escl" width="16" height="48" viewBox="0 0 16 48"><path fill="currentColor" d="M11 0v40h5l-8 8-8-8h5v-40h6z"/></svg>

        <div class="md:col-span-12 lg:col-span-2 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted hover:border-blue-accent transition relative">
            <div class="flex items-center gap-3 mb-4">
                <span class="text-3xl">⏰</span>
                <h2 class="text-2xl font-semibold text-blue-primary">08:00 EST</h2>
            </div>
            <p class="text-sm font-medium mb-1">Attendance Check:</p>
            <ul class="text-sm space-y-1 list-disc list-inside text-blue-accent">
                <li>Clockify (Time Track)</li>
                <li>G-Chat: "Good Morning"</li>
            </ul>
        </div>

        <div class="md:col-span-12 lg:col-span-10 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted hover:border-blue-accent transition">
            <h2 class="text-2xl font-semibold text-blue-primary mb-5 flex items-center gap-3"><span class="text-3xl">🛠️</span>System Setup & Readiness</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 text-center">
                <div class="bg-blue-secondary p-4 rounded-xl border border-blue-muted">
                    <p class="font-bold text-lg text-blue-accent">RingCentral</p>
                    <p class="text-sm mt-1">Status: <span class="text-green-600 font-bold">AVAILABLE</span> (Queue Ready)</p>
                </div>
                <div class="bg-blue-secondary p-4 rounded-xl border border-blue-muted">
                    <p class="font-bold text-lg text-blue-accent">Google Meet</p>
                    <p class="text-sm mt-1">Join ongoing Nurse Call (Active Listening)</p>
                </div>
                <div class="bg-blue-secondary p-4 rounded-xl border border-blue-muted">
                    <p class="font-bold text-lg text-blue-accent">AthenaText</p>
                    <p class="text-sm mt-1">Open: <span class="font-medium">Nurses Chat + Front Staff Chat</span></p>
                </div>
                <div class="bg-blue-secondary p-4 rounded-xl border border-blue-muted">
                    <p class="font-bold text-lg text-blue-accent">Call Log (GSheet)</p>
                    <p class="text-sm mt-1">Open personal tab. Ready to document.</p>
                </div>
            </div>
        </div>

        <div class="hidden lg:block md:col-span-2"></div>

        <div class="md:col-span-12 lg:col-span-10 bg-white p-8 rounded-2xl shadow-lg border-2 border-blue-accent relative">
            <div class="flex items-center justify-between mb-6">
                <h2 class="text-3xl font-extrabold text-blue-primary flex items-center gap-4"><span class="text-4xl">📞</span>Active Call Workflow</h2>
                <div class="text-sm px-4 py-1.5 rounded-xl bg-blue-secondary text-blue-accent border border-blue-muted">
                   Main Goal: Cater to Customer Needs
                </div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="border-l-4 border-blue-muted pl-4">
                    <p class="font-bold text-blue-primary text-lg">1. Greeting & Verify</p>
                    <p class="text-sm italic">"Thank you for calling UFMC, this is [Name]..."</p>
                    <p class="text-sm mt-1 font-medium text-blue-accent">ID Patient: Name, DOB, Phone.</p>
                </div>
                <div class="border-l-4 border-blue-muted pl-4">
                    <p class="font-bold text-blue-primary text-lg">2. Determine Concern</p>
                    <p class="text-sm">Identify if scheduling, medication, registration, or information.</p>
                </div>
                <div class="border-l-4 border-blue-accent pl-4 bg-blue-secondary p-3 rounded-lg">
                    <p class="font-bold text-blue-primary text-lg flex items-center gap-2"><span class="text-xl">📕</span>3. Refer to Handbook</p>
                    <p class="text-xs mt-1">Consult [MA & Front Staff Handbook] for specific protocol.</p>
                </div>
            </div>
        </div>

        <div class="md:col-span-12 lg:col-span-8 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted hover:border-blue-accent transition">
            <h3 class="text-2xl font-semibold text-blue-primary mb-5 flex items-center gap-3"><span class="text-3xl">📋</span>Addressing Patient Needs</h3>
            <div class="space-y-3">
                <div class="flex gap-3 bg-blue-secondary p-4 rounded-xl items-center">
                    <span class="text-2xl w-10 text-center">📅</span>
                    <div>
                        <p class="font-bold text-blue-accent">Scheduling / Rescheduling</p>
                        <p class="text-sm">VA Actions: Check EHR availability. Verify details. Book appointment directly.</p>
                    </div>
                </div>
                <div class="flex gap-3 bg-blue-secondary p-4 rounded-xl items-center hover:bg-white hover:shadow-inner transition">
                    <span class="text-2xl w-10 text-center">➕</span>
                    <div>
                        <p class="font-bold text-blue-accent">New Patient Registration</p>
                        <p class="text-sm">VA Actions: Collect demographics (ID, Insurance, Addr). Create patient profile in Athena.</p>
                    </div>
                </div>
                <div class="flex gap-3 bg-blue-secondary p-4 rounded-xl items-center">
                    <span class="text-2xl w-10 text-center">💊</span>
                    <div>
                        <p class="font-bold text-blue-accent">Medical Refills / Info Requests</p>
                        <p class="text-sm">VA Actions: Direct resolution if administrative (policy/hours). <span class="font-medium text-red-600">Requires Clinical Escalation</span> for refills.</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="md:col-span-12 lg:col-span-4 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted flex flex-col items-center text-center">
            <span class="text-5xl mb-3">📝</span>
            <h3 class="text-xl font-semibold text-blue-primary mb-3">Essential Documentation</h3>
            <p class="text-sm mb-4">Every call must be documented immediately in the GSheet.</p>
            <div class="bg-blue-secondary w-full p-4 rounded-xl text-left text-xs font-mono border border-blue-muted space-y-1">
                <p>Date: YYYY-MM-DD HH:MM</p>
                <p>Caller: John Doe (DOB: MM/DD/YY)</p>
                <p>Reason: Reschedule</p>
                <p>Action: Moved to 3PM Tuesday</p>
            </div>
        </div>

        <div class="md:col-span-12 bg-white p-8 rounded-2xl shadow-lg border-l-8 border-blue-primary">
            <h2 class="text-3xl font-extrabold text-blue-primary mb-6 flex items-center gap-4"><span class="text-4xl">🤝</span>Internal Team Collaboration</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                
                <div class="p-5 border border-blue-muted rounded-xl bg-blue-secondary">
                    <p class="font-bold text-blue-primary text-xl flex items-center gap-2"><span class="text-2xl">👩‍⚕️</span>Clinical Escalations (Nurses)</p>
                    <p class="text-sm mb-3">For refill requests or medical advice requests.</p>
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 text-center text-xs">
                        <p class="bg-white p-2 rounded-lg font-medium border border-blue-muted">AthenaText (Nurse Chat)</p>
                        <p class="bg-white p-2 rounded-lg font-medium border border-blue-muted">GMeet (Voice Call)</p>
                        <p class="bg-blue-primary text-white p-2 rounded-lg font-bold">RingCentral PARK Call (If req)</p>
                    </div>
                </div>

                <div class="p-5 border border-blue-muted rounded-xl bg-blue-secondary">
                    <p class="font-bold text-blue-primary text-xl flex items-center gap-2"><span class="text-2xl">🏢</span>Office Logistics (In-Person)</p>
                    <p class="text-sm mb-3">For physical patient concerns or office operational needs.</p>
                    <div class="text-center">
                        <p class="bg-white p-3 rounded-lg font-medium border border-blue-muted inline-block text-sm">AthenaText (Front Staff Chat)</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="md:col-span-12 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted hover:border-blue-accent transition flex flex-col sm:flex-row sm:justify-between sm:items-center text-center sm:text-left">
            <div>
                <h2 class="text-2xl font-semibold text-blue-primary flex items-center gap-3"><span class="text-3xl">📴</span>17:00 EST Shift End</h2>
                <p class="text-sm mt-1">Ensure all daily documentation is synced and saved.</p>
            </div>
            <div class="mt-4 sm:mt-0 flex gap-4 justify-center">
                <div class="bg-blue-secondary px-4 py-2 rounded-lg border border-blue-muted text-sm">Clockify: <span class="font-bold">OUT</span></div>
                <div class="bg-blue-secondary px-4 py-2 rounded-lg border border-blue-muted text-sm">G-Chat: "Good Night"</div>
            </div>
        </div>

    </div>

    <footer class="text-center mt-16 text-blue-text opacity-70 text-sm">
        <p>© UFMC Virtual Front Desk - Internal Procedure Visualization</p>
    </footer>

</body>
</html>
