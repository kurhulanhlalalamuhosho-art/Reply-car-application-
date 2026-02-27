#Replay Car Application and Debt review 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Replay Car Application | Fast Debt & Vehicle Clearance</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
        body { font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        .form-gradient { background: linear-gradient(135deg, #1e3a8a 0%, #172554 100%); }
        .car-card:hover img { transform: scale(1.05); }
        .bank-card { border: 2px dashed #cbd5e1; }
    </style>
</head>
<body class="bg-slate-50 text-slate-900">

    <div class="bg-red-600 text-white text-center py-2 text-xs md:text-sm font-black tracking-widest sticky top-0 z-50 shadow-lg">
        ⚡ 2 - 5 HOUR CLEARANCE WINDOW | JHB & PRETORIA SPECIALISTS
    </div>

    <nav class="flex justify-between items-center px-6 md:px-12 py-5 bg-white shadow-sm border-b border-slate-100">
        <div class="text-xl md:text-2xl font-black text-blue-950 tracking-tighter uppercase">
            REPLAY <span class="text-red-600">Car App</span>
        </div>
        <div class="flex items-center gap-4">
            <a href="tel:0837514725" class="bg-blue-900 text-white px-5 py-2.5 rounded-full font-bold hover:bg-red-600 transition-all flex items-center gap-2">
                <i class="fa-solid fa-phone"></i> <span class="hidden md:inline">083 751 4725</span>
            </a>
        </div>
    </nav>

    <main class="max-w-7xl mx-auto px-6 py-10 md:py-16 grid lg:grid-cols-2 gap-12 items-start">
        
        <div class="space-y-8">
            <h1 class="text-4xl md:text-6xl font-black leading-[1.1] text-slate-900">
                Struggling with <span class="text-red-600">Arrears?</span> <br> Drive Today.
            </h1>
            
            <div class="bank-card bg-white p-6 rounded-2xl shadow-md">
                <div class="flex items-center gap-3 mb-4">
                    <div class="bg-yellow-400 text-black px-3 py-1 rounded font-black text-sm uppercase">TymeBank</div>
                    <h3 class="font-black text-blue-950">Immediate Payment Required</h3>
                </div>
                <div class="space-y-2 text-sm">
                    <div class="flex justify-between border-b pb-2">
                        <span class="text-slate-500">Account Number:</span>
                        <span class="font-bold text-slate-900">51059443678</span>
                    </div>
                    <div class="flex justify-between border-b pb-2">
                        <span class="text-slate-500">Bank Name:</span>
                        <span class="font-bold text-slate-900">TymeBank</span>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-slate-500">Reference:</span>
                        <span class="font-bold text-red-600 uppercase">Name of Selected Car</span>
                    </div>
                </div>
                <p class="text-[10px] text-slate-400 mt-4 italic">Please make immediate payment to expedite your clearance process 🙏</p>
            </div>

            <div class="bg-white p-6 rounded-2xl shadow-sm border-l-4 border-red-600">
                <h3 class="font-bold text-blue-900 mb-2">Required Documents:</h3>
                <p class="text-sm text-slate-500">3 Months Bank Statements, Latest Payslip & SA ID.</p>
            </div>
        </div>

        <div id="application-container" class="form-gradient p-8 md:p-10 rounded-[2.5rem] text-white shadow-2xl border-4 border-white scroll-mt-24">
            
            <div id="car-selection-indicator" class="bg-white/10 border border-white/20 text-white px-4 py-3 rounded-xl mb-6 text-sm font-bold hidden flex items-center justify-between">
                <span>RESERVED: <span id="selected-car-name" class="text-yellow-400 uppercase ml-1">None</span></span>
                <i class="fa-solid fa-lock text-yellow-400"></i>
            </div>
            
            <h2 class="text-3xl font-black mb-1">Apply Now</h2>
            <p class="text-blue-200 text-sm mb-8 font-medium">Select a car below to automatically link it to your application.</p>

            <form action="https://formspree.io/f/YOUR_ID_HERE" method="POST" id="replay-form" class="space-y-5">
                
                <div class="space-y-1">
                    <label class="text-[10px] uppercase font-bold text-blue-300 ml-1">Selected Vehicle (Required)</label>
                    <input type="text" name="Selected_Vehicle" id="interested_car_input" readonly required placeholder="Please select a car from the list below" 
                    class="w-full p-3.5 rounded-xl bg-blue-950/80 border border-yellow-500/50 text-yellow-400 font-bold outline-none cursor-not-allowed">
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <input type="text" name="Name" required placeholder="Full Name" class="w-full p-3.5 rounded-xl bg-blue-950/50 border border-blue-700/50 text-white outline-none focus:ring-2 focus:ring-red-500 transition">
                    <input type="text" name="ID_Number" maxlength="13" required placeholder="ID Number" class="w-full p-3.5 rounded-xl bg-blue-950/50 border border-blue-700/50 text-white outline-none focus:ring-2 focus:ring-red-500 transition">
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <input type="tel" name="WhatsApp_Number" required placeholder="Phone Number" class="w-full p-3.5 rounded-xl bg-blue-950/50 border border-blue-700/50 text-white outline-none focus:ring-2 focus:ring-red-500 transition">
                    <input type="text" name="Income" required placeholder="Gross Monthly Income" class="w-full p-3.5 rounded-xl bg-blue-950/50 border border-blue-700/50 text-white outline-none focus:ring-2 focus:ring-red-500 transition">
                </div>

                <select name="Financial_Status" class="w-full p-3.5 rounded-xl bg-blue-950/50 border border-blue-700/50 text-blue-100 outline-none focus:ring-2 focus:ring-red-500 transition">
                    <option>Currently in Debt Review</option>
                    <option>Arrears on existing Car Finance</option>
                    <option>Blacklisted / Judgments</option>
                </select>
                
                <div class="flex items-start gap-3 py-2">
                    <input type="checkbox" required class="mt-1 w-5 h-5 accent-red-600 rounded">
                    <p class="text-[10px] text-blue-300">I agree to the credit assessment and confirm I will provide POP (Proof of Payment) for faster service.</p>
                </div>

                <button type="submit" class="w-full bg-red-600 hover:bg-red-500 py-5 rounded-2xl font-black uppercase tracking-widest transition-all shadow-xl active:scale-95 text-lg">
                    Submit & Pay Reference
                </button>
            </form>
        </div>
    </main>

    <section class="py-16 px-6 max-w-7xl mx-auto">
        <div class="text-center mb-10">
            <h2 class="text-3xl font-black text-slate-900 uppercase">Available <span class="text-red-600">Inventory</span></h2>
            <p class="text-slate-500">Click "Reserve This Car" to start your application for that specific unit.</p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
            <div class="car-card bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 transition-all">
                <img src="https://images.unsplash.com/photo-1541899481282-d53bffe3c35d?q=80&w=800" class="w-full h-48 object-cover">
                <div class="p-6 text-center">
                    <h3 class="text-xl font-bold text-blue-950">VW Polo Vivo</h3>
                    <p class="text-red-600 font-black mb-4">From R3,200 p/m</p>
                    <button onclick="selectCar('VW Polo Vivo')" class="bg-blue-900 text-white w-full py-3 rounded-xl font-bold hover:bg-red-600 transition uppercase text-sm tracking-tighter">Reserve This Car</button>
                </div>
            </div>
            <div class="car-card bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 transition-all">
                <img src="https://images.unsplash.com/photo-1609521263047-f8f205293f24?q=80&w=800" class="w-full h-48 object-cover">
                <div class="p-6 text-center">
                    <h3 class="text-xl font-bold text-blue-950">Toyota Starlet</h3>
                    <p class="text-red-600 font-black mb-4">From R3,600 p/m</p>
                    <button onclick="selectCar('Toyota Starlet')" class="bg-blue-900 text-white w-full py-3 rounded-xl font-bold hover:bg-red-600 transition uppercase text-sm tracking-tighter">Reserve This Car</button>
                </div>
            </div>
            <div class="car-card bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 transition-all">
                <img src="https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?q=80&w=800" class="w-full h-48 object-cover">
                <div class="p-6 text-center">
                    <h3 class="text-xl font-bold text-blue-950">Haval Jolion</h3>
                    <p class="text-red-600 font-black mb-4">From R5,200 p/m</p>
                    <button onclick="selectCar('Haval Jolion')" class="bg-blue-900 text-white w-full py-3 rounded-xl font-bold hover:bg-red-600 transition uppercase text-sm tracking-tighter">Reserve This Car</button>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-blue-950 text-slate-400 py-12 px-6 text-center">
        <div class="flex flex-col items-center gap-6">
            <a href="https://wa.me/27837514725?text=I%20have%20made%20payment%20for%20my%20car%20application" class="inline-flex items-center gap-2 bg-green-600 text-white px-8 py-4 rounded-full font-bold hover:bg-green-500 transition shadow-lg">
                <i class="fa-brands fa-whatsapp text-2xl"></i> I've Paid - Send POP
            </a>
            <div>
                <p class="text-white font-black text-lg">REPLAY CAR APP &copy; 2026</p>
                <p class="text-xs mt-2 uppercase tracking-widest">TymeBank Acc: 51059443678</p>
            </div>
        </div>
    </footer>

    <script>
        function selectCar(carName) {
            // Update input and show indicator
            const carInput = document.getElementById('interested_car_input');
            carInput.value = carName;
            
            const indicator = document.getElementById('car-selection-indicator');
            const nameSpan = document.getElementById('selected-car-name');
            indicator.classList.remove('hidden');
            nameSpan.innerText = carName;

            // Scroll to the application section
            document.getElementById('application-container').scrollIntoView({ behavior: 'smooth' });
            
            // Visual feedback on the input
            carInput.style.borderColor = "#eab308";
        }
    
