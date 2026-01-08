<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crescenza Flow | Ritual de Sexta</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&family=Lora:ital,wght@0,400;1,400&display=swap" rel="stylesheet">

    <style>
        /* --- IDENTIDADE VISUAL (Baseada nas suas imagens) --- */
        :root {
            --brand: #FF6600;       /* Laranja Vibrante */
            --brand-dark: #cc5200;
            --dark: #1E1E1E;        /* Fundo Dark das imagens */
            --paper: #FFFFFF;
            --text: #334155;
            --bg-app: #F3F4F6;
        }

        * { box-sizing: border-box; outline: none; }
        
        body {
            margin: 0;
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: var(--bg-app);
            color: var(--text);
            display: flex;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* --- TELA DE LOGIN (Proteção) --- */
        #login-screen {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(30, 30, 30, 0.98);
            z-index: 9999;
            display: flex; align-items: center; justify-content: center; flex-direction: column;
        }
        .login-box {
            text-align: center; color: white; max-width: 300px;
        }
        .login-box h1 { color: var(--brand); text-transform: uppercase; letter-spacing: 2px; margin-bottom: 10px; }
        .pass-input {
            padding: 15px; border-radius: 8px; border: none; width: 100%;
            text-align: center; font-size: 18px; letter-spacing: 3px; margin-bottom: 15px;
            text-transform: uppercase;
        }
        .btn-login {
            background: var(--brand); color: white; padding: 12px; width: 100%;
            border: none; border-radius: 8px; font-weight: 800; cursor: pointer;
            text-transform: uppercase; transition: 0.3s;
        }
        .btn-login:hover { background: var(--brand-dark); box-shadow: 0 0 15px rgba(255, 102, 0, 0.4); }

        /* --- PAPEL A4 (A Ferramenta) --- */
        .page {
            width: 210mm;
            min-height: 297mm; /* Tamanho A4 */
            background: var(--paper);
            padding: 15mm;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            position: relative;
            display: none; /* Escondido até logar */
            flex-direction: column;
        }

        /* CABEÇALHO */
        header {
            border-bottom: 4px solid var(--brand);
            padding-bottom: 20px; margin-bottom: 30px;
            display: flex; justify-content: space-between; align-items: flex-end;
        }
        .logo h1 { margin: 0; font-size: 24px; color: var(--dark); text-transform: uppercase; letter-spacing: -1px; }
        .logo span { color: var(--brand); }
        .meta input { 
            border: none; border-bottom: 1px dashed #ccc; text-align: right; 
            font-family: inherit; font-weight: 600; color: var(--brand); width: 150px;
        }

        /* CONCEITO CIENTÍFICO (Box Educativo) */
        .science-alert {
            background: #FFF7ED; border-left: 5px solid var(--brand);
            padding: 20px; border-radius: 0 8px 8px 0; margin-bottom: 30px;
            display: flex; gap: 15px; align-items: start;
        }
        .science-icon { font-size: 24px; color: var(--brand); }
        .science-text h4 { margin: 0 0 5px 0; color: var(--dark); text-transform: uppercase; font-size: 14px; }
        .science-text p { margin: 0; font-size: 13px; color: #666; font-family: 'Lora', serif; }

        /* SEÇÕES DO RITUAL */
        .section-header {
            display: flex; align-items: center; gap: 10px;
            margin-bottom: 15px; margin-top: 30px;
        }
        .section-header h3 { margin: 0; font-size: 16px; text-transform: uppercase; color: var(--dark); }
        .section-header i { color: var(--brand); }

        /* CHECKLIST */
        .task {
            display: flex; align-items: center; gap: 15px;
            padding: 12px; border-bottom: 1px solid #eee;
            transition: 0.2s; cursor: pointer;
        }
        .task:hover { background: #f9f9f9; }
        .task.checked h4 { text-decoration: line-through; color: #ccc; }
        .task.checked .check-box { background: var(--success); border-color: var(--success); color: white; }
        
        .check-box {
            width: 24px; height: 24px; border: 2px solid #ccc; border-radius: 6px;
            display: flex; align-items: center; justify-content: center; color: transparent;
        }
        .task-info h4 { margin: 0; font-size: 15px; color: var(--dark); }
        .task-info p { margin: 2px 0 0; font-size: 12px; color: #888; }

        /* ÁREAS DE ESCRITA */
        .input-box {
            width: 100%; border: 1px dashed #ccc; background: #FAFAFA;
            padding: 15px; border-radius: 8px; font-family: 'Lora', serif;
            font-size: 14px; color: var(--dark); margin-top: 10px;
        }
        .input-box:focus { background: white; outline: 2px solid var(--brand); }

        /* RODAPÉ */
        footer {
            margin-top: auto; text-align: center; border-top: 1px solid #eee;
            padding-top: 20px; font-size: 12px; color: #aaa;
        }

        /* BOTÃO FLUTUANTE DE IMPRESSÃO */
        .fab {
            position: fixed; bottom: 30px; right: 30px;
            background: var(--dark); color: white; width: 60px; height: 60px;
            border-radius: 50%; display: flex; align-items: center; justify-content: center;
            font-size: 24px; cursor: pointer; box-shadow: 0 10px 20px rgba(0,0,0,0.3);
            transition: 0.3s;
        }
        .fab:hover { background: var(--brand); transform: scale(1.1); }

        /* AJUSTE PARA IMPRESSÃO */
        @media print {
            body { background: white; padding: 0; }
            .page { box-shadow: none; width: 100%; display: flex !important; }
            #login-screen, .fab { display: none !important; }
            .input-box { border: 1px solid #eee; }
        }
    </style>
</head>
<body>

    <div id="login-screen">
        <div class="login-box">
            <h1>Crescenza</h1>
            <p style="font-size: 14px; color: #ccc; margin-bottom: 20px;">Área Exclusiva de Gestão</p>
            <input type="password" id="pass" class="pass-input" placeholder="SENHA" onkeyup="checkEnter(event)">
            <button class="btn-login" onclick="login()">Acessar Ferramenta</button>
            <p id="error" style="color: #ff4444; font-size: 12px; margin-top: 10px; display: none;">Senha incorreta</p>
        </div>
    </div>

    <div class="fab" onclick="window.print()" title="Salvar PDF"><i class="fas fa-print"></i></div>

    <div class="page" id="app">
        
        <header>
            <div class="logo">
                <h1>Crescenza<span>Flow</span></h1>
                <small style="color: #666; letter-spacing: 1px;">SISTEMA DE GESTÃO DE ENERGIA</small>
            </div>
            <div class="meta">
                Gestor: <input type="text" placeholder="Seu Nome"><br>
                Data: <span id="dateDisplay"></span>
            </div>
        </header>

        <div class="science-alert">
            <div class="science-icon"><i class="fas fa-battery-half"></i></div>
            <div class="science-text">
                <h4>A Ciência da "Reserva Cognitiva"</h4>
                <p>O córtex pré-frontal funciona como uma bateria. Após uma semana de decisões, sua capacidade analítica reduz drasticamente na sexta à tarde. <strong>Não force decisões. Organize processos.</strong></p>
            </div>
        </div>

        <div class="section-header">
            <i class="fas fa-broom"></i>
            <h3>1. Higiene Mental (Esvaziar)</h3>
        </div>
        
        <div class="task" onclick="toggle(this)">
            <div class="check-box"><i class="fas fa-check"></i></div>
            <div class="task-info">
                <h4>E-mail e Mensagens Zero</h4>
                <p>Respondi o que era urgente? O que não é, foi agendado para segunda?</p>
            </div>
        </div>
        <div class="task" onclick="toggle(this)">
            <div class="check-box"><i class="fas fa-check"></i></div>
            <div class="task-info">
                <h4>Limpeza de Ambiente (Físico/Digital)</h4>
                <p>Fechei as abas do navegador? Minha mesa está limpa para segunda?</p>
            </div>
        </div>

        <div class="section-header">
            <i class="fas fa-chess"></i>
            <h3>2. Estratégia (Priorizar)</h3>
        </div>

        <div class="task" onclick="toggle(this)">
            <div class="check-box"><i class="fas fa-check"></i></div>
            <div class="task-info">
                <h4>A "Única Coisa" de Segunda-feira</h4>
                <p>Qual é a tarefa ÚNICA que, se realizada na segunda de manhã, fará o dia valer a pena?</p>
            </div>
        </div>
        <div class="input-box" contenteditable="true">
            Minha prioridade nº 1 para segunda é...
        </div>

        <div class="section-header">
            <i class="fas fa-heart"></i>
            <h3>3. Gestão de Pessoas (Conectar)</h3>
        </div>

        <div class="task" onclick="toggle(this)">
            <div class="check-box"><i class="fas fa-check"></i></div>
            <div class="task-info">
                <h4>Reconhecimento (Dopamina)</h4>
                <p>Quem da minha equipe mandou bem essa semana? Enviei um "obrigado"?</p>
            </div>
        </div>
        <div class="input-box" contenteditable="true" style="min-height: 50px;">
            Pessoa / Motivo: 
        </div>

        <div class="section-header" style="margin-top: 30px;">
            <i class="fas fa-lightbulb"></i>
            <h3>Insight da Semana (O que aprendi?)</h3>
        </div>
        <div class="input-box" contenteditable="true" style="min-height: 80px; font-style: italic;">
            "Escreva aqui um aprendizado para não esquecer..."
        </div>

        <footer>
            <p><strong>Idionara Prass</strong> | Especialista em Gestão e Cultura</p>
            <p>www.crescenzaonline.com | Método Entre a Raiz e o Voo</p>
        </footer>

    </div>

    <script>
        // SENHA DE ACESSO
        const PASS = "CRESCENZA"; 

        // Data Automática
        const hoje = new Date();
        document.getElementById('dateDisplay').innerText = hoje.toLocaleDateString('pt-BR');

        function login() {
            const val = document.getElementById('pass').value.toUpperCase();
            if(val === PASS) {
                document.getElementById('login-screen').style.display = 'none';
                document.querySelector('.page').style.display = 'flex';
            } else {
                document.getElementById('error').style.display = 'block';
            }
        }

        function checkEnter(e) {
            if(e.key === "Enter") login();
        }

        function toggle(el) {
            el.classList.toggle('checked');
        }
    </script>

</body>
</html>
