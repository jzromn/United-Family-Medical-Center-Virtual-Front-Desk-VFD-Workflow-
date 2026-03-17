# United-Family-Medical-Center-Virtual-Front-Desk-VFD-Workflow-
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
                        'blue-primary': '#0056D2',
                        'blue-secondary': '#E6F0FF',
                        'blue-accent': '#007BFF',
                        'blue-text': '#001F4D',
                        'blue-muted': '#A0C4FF',
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-blue-secondary text-blue-text p-4 md:p-8">

    <header class="text-center mb-12">
        <h1 class="text-4xl font-bold text-blue-primary">Medical Virtual Front Desk</h1>
        <p class="text-xl text-blue-accent mt-2 uppercase tracking-wide font-medium">United Family Medical Center</p>
        
        <div class="flex flex-wrap justify-center gap-4 mt-6">
            <a href="https://docs.google.com/document/d/11a2h8jLfv8HxST0fp8g5ztCp2bzGY9sP4QczfyiPfVQ/edit?tab=t.0" target="_blank" class="flex items-center gap-2 bg-blue-primary text-white px-5 py-2.5 rounded-full font-semibold shadow-md hover:bg-blue-accent transition">
                <span>📄</span> Detailed Workflow Document
            </a>
            <a href="https://unitedfamilymedicalcenter.com/" target="_blank" class="flex items-center gap-2 bg-white text-blue-primary border-2 border-blue-primary px-5 py-2.5 rounded-full font-semibold shadow-md hover:bg-blue-secondary transition">
                <span>🌐</span> Official UFMC Website
            </a>
        </div>

        <div class="mt-6">
            <span class="inline-block bg-white text-blue-primary font-bold px-6 py-1.5 rounded-full border border-blue-muted shadow-sm">
                🕒 Shift: 8 AM – 5 PM EST
            </span>
        </div>
    </header>

    <div class="grid grid-cols-1 md:grid-cols-12 gap-6 max-w-7xl mx-auto">

        <div class="md:col-span-4 bg-white p-6 rounded-2xl shadow-sm border-l-8 border-blue-primary">
            <h2 class="text-2xl font-bold text-blue-primary mb-4 flex items-center gap-2"><span>⏰</span> 08:00 AM Start</h2>
            <div class="space-y-4">
                <div class="p-3 bg-blue-secondary rounded-lg">
                    <p class="font-bold text-blue-accent">Attendance Check</p>
                    <ul class="text-sm list-disc list-inside mt-1">
                        <li>Clockify: Clock In</li>
                        <li>G-Chat: "Good Morning"</li>
                    </ul>
                </div>
                <div class="p-3 bg-blue-secondary rounded-lg">
                    <p class="font-bold text-blue-accent">Comms Setup</p>
                    <ul class="text-sm list-disc list-inside mt-1">
                        <li>Join Nurse GMeet (Stay Active)</li>
                        <li>Open AthenaText Group Chats</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="md:col-span-8 bg-white p-6 rounded-2xl shadow-lg border-2 border-blue-accent">
            <h2 class="text-2xl font-bold text-blue-primary mb-4 flex items-center gap-2"><span>📞</span> Active Call Workflow</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div class="border border-blue-muted p-4 rounded-xl">
                    <p class="font-bold text-blue-primary">1. Identify & Verify</p>
                    <p class="text-xs text-blue-text mt-1 italic">"How may I assist you?"</p>
                    <p class="text-sm mt-2">Confirm Name, DOB, and Phone Number in EHR.</p>
                </div>
                <div class="border border-blue-muted p-4 rounded-xl">
                    <p class="font-bold text-blue-primary">2. Categorize Concern</p>
                    <p class="text-sm mt-1">Determine if Scheduling, Refills, or Info Request.</p>
                </div>
            </div>
            <div class="mt-4 p-4 bg-blue-primary text-white rounded-xl flex items-center justify-between">
                <div>
                    <p class="font-bold">Consult Protocol</p>
                    <p class="text-sm opacity-90">Always refer to the Medical Assistant Handbook.</p>
                </div>
                <a href="https://docs.google.com/document/d/1Jj8ZuAlQuJUszhPi22DbhomjfX7aqPDT_T8D2W-yL_g/edit?tab=t.0#heading=h.36whwnd8o5to" target="_blank" class="bg-white text-blue-primary text-xs font-bold py-1 px-3 rounded uppercase">Open Handbook</a>
            </div>
        </div>

        <div class="md:col-span-12 bg-white p-6 rounded-2xl shadow-sm border border-blue-muted">
            <h2 class="text-2xl font-bold text-blue-primary mb-6">Common Tasks & Actions</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="p-4 bg-blue-secondary rounded-xl">
                    <p class="font-bold text-blue-accent underline">Scheduling</p>
                    <p class="text-sm mt-2">Book directly in EHR. For new patients, collect full demographics & insurance.</p>
                </div>
                <div class="p-4 bg-blue-secondary rounded-xl">
                    <p class="font-bold text-blue-accent underline">Medication Refills</p>
                    <p class="text-sm mt-2">Create **Patient Case** in Athena and route to the nursing bucket.</p>
                </div>
                <div class="p-4 bg-blue-secondary rounded-xl">
                    <p class="font-bold text-blue-accent underline">Internal Comms</p>
                    <p class="text-sm mt-2">Use GMeet/AthenaText for Nurses. Use AthenaText for Office Staff.</p>
                </div>
            </div>
        </div>

        <div class="md:col-span-12 flex flex-col md:flex-row gap-6">
            <div class="flex-1 bg-blue-text text-white p-6 rounded-2xl shadow-md">
                <p class="text-xl font-bold mb-2 flex items-center gap-2"><span>📝</span> Call Documentation</p>
                <p class="text-sm opacity-80 mb-4">Log Date, Caller, Reason, and Action for EVERY call.</p>
                <a href="https://docs.google.com/spreadsheets/d/1zEuLw1jCDET6KyeC86r6lteM3cavHWLvq6ugvYmddWg/edit?usp=sharing" target="_blank" class="text-blue-muted font-bold hover:text-white underline text-sm">Open VA Call Log Sheet →</a>
            </div>
            <div class="flex-1 bg-white p-6 rounded-2xl border-2 border-dashed border-blue-muted flex items-center justify-between">
                <div>
                    <h3 class="text-xl font-bold text-blue-primary">05:00 PM Close</h3>
                    <p class="text-sm">Clockify Out & "Good Night" on G-Chat.</p>
                </div>
                <span class="text-4xl opacity-30">💤</span>
            </div>
        </div>

    </div>

    <footer class="text-center mt-12 text-blue-text opacity-60 text-xs">
        <p>© United Family Medical Center | Virtual Front Desk SOP Visualization</p>
    </footer>

</body>
</html>
