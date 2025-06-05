<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Formulário de Contratação - Confeiteiro de Bolo de Pote</title>
<style>
  :root {
    --primary-color: #ff6f61;
    --secondary-color: #f9a825;
    --bg-color: #fff8f0;
    --font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  body {
    margin: 0;
    background-color: var(--bg-color);
    font-family: var(--font-family);
    color: #4a4a4a;
  }

  header {
    background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
    color: white;
    padding: 1.8rem 2rem;
    text-align: center;
    font-weight: 700;
    font-size: 1.8rem;
    letter-spacing: 1.2px;
    text-shadow: 0 0 6px rgba(0,0,0,0.2);
  }

  main {
    max-width: 600px;
    margin: 2rem auto 4rem;
    background: white;
    padding: 2rem 2.5rem;
    border-radius: 12px;
    box-shadow: 0 10px 20px rgba(255,111,97,0.15);
  }

  h2 {
    color: var(--primary-color);
    margin-bottom: 1.2rem;
    text-align: center;
  }

  form label {
    display: block;
    margin-top: 1.2rem;
    margin-bottom: 0.4rem;
    font-weight: 600;
    font-size: 0.95rem;
  }

  form input[type="text"],
  form input[type="email"],
  form input[type="tel"],
  form input[type="number"],
  form select,
  form textarea {
    width: 100%;
    padding: 0.6rem 0.8rem;
    border: 2px solid #ffcec7;
    border-radius: 6px;
    font-size: 1rem;
    transition: border-color 0.3s ease;
    resize: vertical;
  }
  form input[type="text"]:focus,
  form input[type="email"]:focus,
  form input[type="tel"]:focus,
  form input[type="number"]:focus,
  form select:focus,
  form textarea:focus {
    outline: none;
    border-color: var(--secondary-color);
    box-shadow: 0 0 8px var(--secondary-color);
  }

  form textarea {
    min-height: 80px;
  }

  .checkbox-group {
    margin-top: 1rem;
  }

  .checkbox-group label {
    font-weight: 500;
    font-size: 1rem;
    display: flex;
    align-items: center;
    cursor: pointer;
  }

  .checkbox-group input[type="checkbox"] {
    margin-right: 0.6rem;
    transform: scale(1.2);
    accent-color: var(--primary-color);
  }

  button[type="submit"] {
    margin-top: 2rem;
    width: 100%;
    background: var(--primary-color);
    color: white;
    border: none;
    border-radius: 8px;
    padding: 1rem 0;
    font-size: 1.2rem;
    font-weight: 700;
    cursor: pointer;
    transition: background-color 0.3s ease;
    box-shadow: 0 5px 12px rgba(255,111,97,0.6);
  }
  button[type="submit"]:hover {
    background: var(--secondary-color);
  }

  .requirements {
    background-color: #fff3e0;
    border-left: 6px solid var(--primary-color);
    padding: 1rem 1.2rem;
    margin-bottom: 1.8rem;
    font-size: 0.95rem;
    color: #6b4c3b;
    border-radius: 6px;
    line-height: 1.4;
  }

  /* Responsive */
  @media screen and (max-width: 640px) {
    main {
      margin: 1rem 1rem 3rem;
      padding: 1.5rem 1.8rem;
    }
  }
</style>
</head>
<body>
<header>
  Contratação: Confeiteiro(a) de Bolo de Pote
</header>
<main>
  <h2>Formulário de Inscrição</h2>

  <div class="requirements" aria-label="Requisitos Necessários">
    <strong>Requisitos necessários para a vaga:</strong>
    <ul>
      <li>Experiência mínima de 1 ano em confeitaria, preferencialmente com bolos de pote.</li>
      <li>Conhecimento em técnicas de preparação, montagem e decoração de bolos.</li>
      <li>Capacidade de seguir receitas e padrões de qualidade da empresa.</li>
      <li>Organização e cuidado com higiene e manipulação dos alimentos.</li>
      <li>Disponibilidade para trabalho em horário comercial.</li>
    </ul>
    <p><em>Por favor, preencha o formulário somente se atender aos requisitos acima.</em></p>
  </div>

  <form id="contratacaoForm" novalidate>
    <label for="nome">Nome completo *</label>
    <input type="text" id="nome" name="nome" required placeholder="Seu nome completo" />

    <label for="email">E-mail *</label>
    <input type="email" id="email" name="email" required placeholder="seu@email.com" />

    <label for="telefone">Telefone *</label>
    <input type="tel" id="telefone" name="telefone" required placeholder="(99) 99999-9999" pattern="\(?\d{2}\)?\s?\d{4,5}\-?\d{4}" title="Formato telefone: (99) 99999-9999" />

    <label for="experiencia">Anos de experiência em confeitaria *</label>
    <input type="number" id="experiencia" name="experiencia" min="0" max="50" required placeholder="Ex: 2" />

    <label for="conhecimento">Quais técnicas você domina? *</label>
    <textarea id="conhecimento" name="conhecimento" required placeholder="Ex: Preparação de massa, creme, decoração, etc."></textarea>

    <label>Você possui experiência com bolos de pote? *</label>
    <select id="experienciaPote" name="experienciaPote" required>
      <option value="" disabled selected>Selecione uma opção</option>
      <option value="sim">Sim</option>
      <option value="nao">Não</option>
    </select>

    <label for="disponibilidade">Disponibilidade de horário *</label>
    <select id="disponibilidade" name="disponibilidade" required>
      <option value="" disabled selected>Selecione</option>
      <option value="manhã">Manhã</option>
      <option value="tarde">Tarde</option>
      <option value="integral">Integral (manhã e tarde)</option>
    </select>

    <label for="expectativa">Expectativa salarial (R$) *</label>
    <input type="number" id="expectativa" name="expectativa" min="600" max="10000" required placeholder="Ex: 2000" />

    <label for="comentarios">Carta de apresentação / Comentários adicionais</label>
    <textarea id="comentarios" name="comentarios" placeholder="Conte um pouco sobre você, sua motivação, etc."></textarea>

    <div class="checkbox-group">
      <label>
        <input type="checkbox" id="confirmaRequisitos" name="confirmaRequisitos" required />
        Confirmo que atendo todos os requisitos mencionados acima.
      </label>
    </div>

    <button type="submit">Enviar inscrição</button>
  </form>
</main>
<script>
  const form = document.getElementById('contratacaoForm');
  form.addEventListener('submit', (e) => {
    e.preventDefault();
    if (!form.reportValidity()) {
      return;
    }
    alert('Inscrição enviada com sucesso! Obrigado por se candidatar.');
    form.reset();
  });
</script>
</body>
</html>

