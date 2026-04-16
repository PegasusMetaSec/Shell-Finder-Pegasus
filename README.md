<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Access - Bayar dengan Bitcoin / Saweria</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-900 text-white flex items-center justify-center min-h-screen p-4">
    <div class="max-w-md w-full bg-gray-800 rounded-2xl shadow-xl p-6 text-center">
        <h1 class="text-2xl font-bold mb-2">Akses Premium</h1>
        <p class="text-gray-400 mb-6">Pilih metode pembayaran untuk mendapatkan akses penuh.</p>

        <!-- Bitcoin -->
        <div class="bg-gray-700 p-4 rounded-xl mb-4">
            <p class="font-mono text-sm break-all">bc1qxy2kg9yqety0k0a3j0k3j0k3j0k3j0k3j0k3j0</p>
            <button onclick="copyText('bc1qxy2kg9yqety0k0a3j0k3j0k3j0k3j0k3j0k3j0')" class="mt-2 bg-orange-600 hover:bg-orange-700 px-4 py-2 rounded-lg text-sm">Salin Alamat BTC</button>
        </div>

        <!-- Saweria -->
        <a href="https://saweria.co/usernamekamu" target="_blank" class="block bg-yellow-500 hover:bg-yellow-600 text-black font-semibold py-3 rounded-xl mb-4">
            💛 Bayar via Saweria
        </a>

        <!-- Verifikasi (simulasi) -->
        <button id="verifyBtn" class="w-full bg-green-600 hover:bg-green-700 py-3 rounded-xl font-semibold">Saya Sudah Bayar</button>
        <p id="status" class="text-sm text-gray-400 mt-4"></p>
    </div>

    <script>
        function copyText(text) {
            navigator.clipboard.writeText(text);
            alert("Alamat BTC disalin!");
        }

        document.getElementById("verifyBtn").onclick = () => {
            const status = document.getElementById("status");
            status.innerHTML = "⏳ Verifikasi... (demo)";
            setTimeout(() => {
                status.innerHTML = "✅ Akses diberikan! (demo - integrasikan webhook asli)";
            }, 1500);
        };
    </script>
</body>
</html>
