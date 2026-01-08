<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crescenza Flow | Ritual de Encerramento</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Lora:ital,wght@0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">

    <style>
        /* ==================== DESIGN SYSTEM CRESCENZA ==================== */
        :root {
            --primary: #e65100;      /* Laranja da Marca */
            --primary-soft: #fff3e0;
            --secondary: #263238;    /* Cinza Escuro */
            --text-main: #334155;
            --bg-body: #F8FAFC;
            --surface: #FFFFFF;
            --border: #E2E8F0;
            --success: #10B981;
            --radius: 12px;
            --shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.1);
            
            --font-display: 'Plus Jakarta Sans', sans-serif;
            --font-read: 'Lora', serif;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; outline: none; }
        
        body { 
            font-family: var(--font-display); 
            background: var(--bg-body); 
            color: var(--text-main); 
            line-height: 1.5;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
            min-height: 100vh;
        }

        /* --- TELA DE LOGIN --- */
        .auth-overlay { 
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
            background: rgba(30, 41, 59, 0.95); z-index: 999; 
            display: flex; align-items: center; justify-content: center; 
            backdrop-filter: blur(8px); 
        }
        .auth-box { 
            background: white; padding: 50px; border-radius: 16px; 
            width: 100%; max-width: 400px; text-align: center; 
            box-shadow: 0 20px 50px rgba(0,0,0,0.5); border-top: 6px solid var(--primary); 
        }
        
        /* --- PAPEL A4 (INTERFACE) --- */
        .page {
            width: 210mm;
            min-height: 297mm;
            background: var(--surface);
            padding: 15mm;
            box-shadow: var(--shadow);
            position: relative;
            display: flex;
            flex-direction: column;
        }

        /* HEADER */
        header {
            display: flex; justify-content: space-between; align-items: flex-end;
            border-bottom: 2px solid var(--secondary); padding-bottom: 20px; margin-bottom: 30px;
        }
        .brand h1 { font-size: 1.8rem; color: var(--secondary); margin: 0; text-transform: uppercase; letter-spacing: -1px; }
        .brand span { color: var(--primary); }
        .meta-info { text-align: right; font-size: 0.85rem; color: #64748B; }
        .meta-info input { border: none; border-bottom: 1px dashed #ccc; width: 120px; text-align: right; font-family: inherit; font-weight: 600; color: var(--primary); }

        /* CIÊNCIA BOX */
        .science-box {
            background: var(--primary-soft);
            border-left: 4px solid var(--primary);
            padding: 20px;
            border-radius: 0 8px 8px 0;
            margin-bottom: 30px;
            font-size: 0.9rem;
            color: var(--secondary);
        }
        .science-box strong { color: #bf360c; text-transform: uppercase; font-size: 0.8rem; letter-spacing: 1px; display: block; margin-bottom: 5px; }

        /* BARRA DE PROGRESSO (GAMIFICAÇÃO) */
        .progress-container { margin-bottom: 30px; }
        .progress-label { display: flex; justify-content: space-between; font-size: 0.8rem; font-weight: 700; margin-bottom: 5px; text-transform: uppercase; color: var(--text-main); }
        .progress-track { width: 100%; height: 10px; background: #E2E8F0; border-radius: 5px; overflow: hidden; }
        .progress-fill { height: 100%; background: var(--success); width: 0%; transition: width 0.5s ease; }

        /* SEÇÕES */
        .section-title {
            display: flex; align-items: center; gap: 10px;
            font-size: 1.1rem; font-weight: 800; color: var(--secondary);
            margin-bottom: 15px; border-bottom: 1px solid var(--border); padding-bottom: 8px;
        }
        .section-title i { color: var(--primary); }

        /* CHECKLIST INTERATIVO */
        .task-row {
            display: flex; align-items: flex-start; gap: 15px;
            padding: 12px; background: #fff; border: 1px solid var(--border);
            border-radius: 8px; margin-bottom: 10px; transition: 0.2s; cursor: pointer;
        }
        .task-row:hover { border-color: var(--primary); background: #FAFAFA; }
        .task-row.checked { background: #F0FDF4; border-color: var(--success); opacity: 0.8; }
        
        /* Checkbox Custom */
        .custom-check {
            width: 24px; height: 24px; border: 2px solid #CBD5E1; border-radius: 6px;
            display: flex; align-items: center; justify-content: center; flex-shrink: 0;
            transition: 0.2s; background: white; margin-top: 2px;
        }
        .task-row.checked .custom-check { background: var(--success); border-color: var(--success); color: white; }
        
        .task-content h4 { margin: 0; font-size: 1rem; color: var(--secondary); }
        .task-content p { margin: 2px 0 0; font-size: 0.85rem; color: #64748B; }

        /* ÁREAS EDITÁVEIS */
        .editable-box {
            width: 100%; min-height: 80px; border: 1px dashed #94A3B8;
            border-radius: 8px; padding: 15px; font-family: var(--font-read);
            background: #F8FAFC; color: var(--secondary);
        }
        .editable-box:focus { background: white; outline: 2px solid var(--primary); border-style: solid; }

        /* FOOTER */
        footer { margin-top: auto; text-align: center; padding-top: 20px; border-top: 1px solid var(--border); font-size: 0.8rem; color: #94A3B8; }

        /* BOTÕES UI */
        .btn { padding: 12px 24px; border-radius: 8px; font-weight: 700; cursor: pointer; border: none; font-size: 1rem; transition: 0.2s; width: 100%; }
        .btn-primary { background: var(--primary); color: white; }
        .btn-primary:hover { background: #bf360c; }
        .form-input { width: 100%; padding: 12px; margin-bottom: 15px; border: 1px solid #ddd; border-radius: 8px; text-align: center; font-size: 1.1rem; letter-spacing: 2px; }

        .fab-print {
            position: fixed; bottom: 30px; right: 30px;
            background: var(--secondary); color: white;
            width: 60px; height: 60px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
            cursor: pointer; transition: 0.3s; font-size: 1.5rem;
        }
        .fab-print:hover { transform: scale(1.1); background: var(--primary); }

        /* --- IMPRESSÃO --- */
        @media print {
            body { background: white; padding: 0; }
            .auth-overlay, .fab-print { display: none !important; }
            .page { box-shadow: none; width: 100%; padding: 0; }
            .editable-box { border: 1px solid #eee; }
            /* Esconde placeholder vazio ao imprimir */
            .editable-box:empty::before { content: " (Vazio)"; color: #ccc; }
        }
    </style>
</head>
<body>

    <div id="auth-screen" class="auth-overlay">
        <div class="auth-box">
            <h1 style="color:var(--primary); margin-bottom:10px;">Crescenza<span style="color:var(--secondary);">Flow</span></h1>
            <p style="color:#64748B; margin-bottom:30px;">Digite a senha exclusiva para acessar sua ferramenta de gestão.</p>
            
            <input type="password" id="pass-input" class="form-input" placeholder="SENHA" onkeyup="if(event.key==='Enter') Auth.login()">
            <button class="btn btn-primary" onclick="Auth.login()">ACESSAR SISTEMA</button>
            <p id="error-msg" style="color:var(--danger); margin-top:15px; font-weight:700; display:none;">Senha Incorreta</p>
        </div>
    </div>

    <div class="fab-print" onclick="window.print()" title="Salvar PDF"><i class="fas fa-print"></i></div>

    <div class="page" id="app-content">
        
        <header>
            <div class="brand">
                <h1>Crescenza<span>Flow</span></h1>
                <div style="font-size:0.8rem; letter-spacing:2px; text-transform:uppercase;">Consultoria & Gestão</div>
            </div>
            <div class="meta-info">
                <strong>RITUAL DE ENCERRAMENTO</strong><br>
                Líder: <input type="text" placeholder="Seu Nome"><br>
                Data: <input type="text" id="date-display">
            </div>
        </header>

        <div class="science-box">
            <strong><i class="fas fa-brain"></i> Neurociência & Gestão</strong>
            <p style="margin:0;">O cérebro tem um limite de "Fadiga de Decisão". Sexta-feira não é dia de abrir problemas complexos (que geram ansiedade no fim de semana), mas de <strong>fechar ciclos</strong>. Use este ritual para limpar sua mente e começar a segunda-feira no ataque, não na defesa.</p>
        </div>

        <div class="progress-container">
            <div class="progress-label">
                <span>Status do Ritual</span>
                <span id="progress-text">0% Concluído</span>
            </div>
            <div class="progress-track">
                <div class="progress-fill" id="progress-bar"></div>
            </div>
        </div>

        <div style="margin-bottom:30px;">
            <div class="section-title"><i class="fas fa-broom"></i> 1. Higiene Operacional (Esvaziar)</div>
            
            <div class="task-row" onclick="App.toggle(this)">
                <div class="custom-check"><i class="fas fa-check"></i></div>
                <div class="task-content">
                    <h4>Zero Pendências Críticas</h4>
                    <p>Respondi tudo que era urgente? O que não é, agendei para segunda?</p>
                </div>
            </div>

            <div class="task-row" onclick="App.toggle(this)">
                <div class="custom-check"><i class="fas fa-check"></i></div>
                <div class="task-content">
                    <h4>Mesa Limpa (Física e Digital)</h4>
                    <p>Fechei as abas do navegador? Organizei a mesa física? (Reduz cortisol visual).</p>
                </div>
            </div>
        </div>

        <div style="margin-bottom:30px;">
            <div class="section-title"><i class="fas fa-chess"></i> 2. Estratégia (Priorizar)</div>
            
            <div class="task-row" onclick="App.toggle(this)">
                <div class="custom-check"><i class="fas fa-check"></i></div>
                <div class="task-content">
                    <h4>As 3 Vitórias de Segunda-feira</h4>
                    <p>Quais são as 3 únicas coisas que preciso fazer segunda de manhã para o dia valer a pena?</p>
                </div>
            </div>
            
            <div class="editable-box" contenteditable="true" style="margin-top:10px;">
                1. <br>
                2. <br>
                3. 
            </div>
        </div>

        <div style="margin-bottom:30px;">
            <div class="section-title"><i class="fas fa-heart"></i> 3. Cultura & Gente (Conectar)</div>
            
            <div class="task-row" onclick="App.toggle(this)">
                <div class="custom-check"><i class="fas fa-check"></i></div>
                <div class="task-content">
                    <h4>O Elogio da Semana (Dopamina)</h4>
                    <p>Quem me surpreendeu? Enviei uma mensagem de áudio ou texto agradecendo?</p>
                </div>
            </div>

            <div class="task-row" onclick="App.toggle(this)">
                <div class="custom-check"><i class="fas fa-check"></i></div>
                <div class="task-content">
                    <h4>Destrava</h4>
                    <p>Tem alguém da minha equipe esperando algo meu para trabalhar na segunda? Já enviei?</p>
                </div>
            </div>
        </div>

        <div style="margin-top:auto;">
            <div class="section-title" style="border:none;"><i class="fas fa-lightbulb"></i> Insight da Semana</div>
            <div class="editable-box" contenteditable="true" style="min-height:60px; font-style:italic;">
                "O que eu aprendi essa semana que não quero esquecer..."
            </div>
        </div>

        <footer>
            <p><strong>Idionara Prass</strong> | Consultoria Estratégica & Gestão Humanizada</p>
            <p style="margin-top:5px; font-size:0.7rem;">Baseado no livro "Entre a Raiz e o Voo" | www.crescenzaonline.com</p>
        </footer>

    </div>

    <script>
        // --- CONFIGURAÇÃO ---
        const PASSWORD = "FLOW"; // Senha simples e poderosa

        const App = {
            totalTasks: 5, // Número total de checkbox para a barra de progresso
            
            init: () => {
                // Data automática
                const today = new Date();
                document.getElementById('date-display').value = today.toLocaleDateString('pt-BR');
            },

            toggle: (el) => {
                el.classList.toggle('checked');
                App.calcProgress();
            },

            calcProgress: () => {
                const checked = document.querySelectorAll('.task-row.checked').length;
                const total = document.querySelectorAll('.task-row').length;
                const pct = Math.round((checked / total) * 100);
                
                document.getElementById('progress-bar').style.width = pct + "%";
                document.getElementById('progress-text').innerText = pct + "% Concluído";

                if(pct === 100) {
                    document.getElementById('progress-bar').style.backgroundColor = "#10B981"; // Verde Sucesso
                }
            }
        };

        const Auth = {
            login: () => {
                const input = document.getElementById('pass-input').value.toUpperCase();
                if(input === PASSWORD) {
                    document.getElementById('auth-screen').style.opacity = '0';
                    setTimeout(() => {
                        document.getElementById('auth-screen').style.display = 'none';
                    }, 500);
                } else {
                    const err = document.getElementById('error-msg');
                    err.style.display = 'block';
                    // Animação de tremor
                    const box = document.querySelector('.auth-box');
                    box.style.transform = 'translateX(10px)';
                    setTimeout(() => box.style.transform = 'translateX(-10px)', 100);
                    setTimeout(() => box.style.transform = 'translateX(0)', 200);
                }
            }
        };

        // Inicializar
        App.init();

    </script>
</body>
</html>
