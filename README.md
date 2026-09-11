
 <!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>D&D-Motos — Oficina de Motos</title>
<meta name="description" content="Manutenção preventiva e corretiva para sua moto, diagnóstico elétrico e revisão completa. Agende seu horário online com a D&D-Motos.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=IBM+Plex+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --steel-100: #EAEAEA;
    --steel-200: #D3D3D3;
    --steel-300: #B4B4B4;
    --steel-600: #666666;
    --ink-900: #131313;
    --ink-800: #1D1D1D;
    --ink-700: #292929;
    --paper: #E2E2E2;
    --paper-line: #BFBFBF;
    --stamp: #AE241A;
    --stamp-dark: #841B13;
    --pencil: #9C9C9C;
    --white: #FFFFFF;

    --font-display: 'Big Shoulders Display', sans-serif;
    --font-body: 'IBM Plex Sans', sans-serif;
    --font-mono: 'IBM Plex Mono', monospace;

    --container: 1160px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  section[id] { scroll-margin-top: 76px; }

  body {
    font-family: var(--font-body);
    color: var(--ink-900);
    background: var(--steel-100);
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
  }

  img, svg { display: block; }
  a { color: inherit; text-decoration: none; }
  button { font-family: inherit; cursor: pointer; border: none; background: none; }
  ul { list-style: none; }

  :focus-visible { outline: 3px solid var(--pencil); outline-offset: 2px; }

  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }

  .container { max-width: var(--container); margin: 0 auto; padding: 0 24px; }

  .icon { width: 24px; height: 24px; fill: none; stroke: currentColor; }

  .eyebrow {
    font-family: var(--font-mono);
    font-size: 0.8rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    font-weight: 500;
    display: block;
  }

  h1, h2, h3 {
    font-family: var(--font-display);
    font-weight: 800;
    line-height: 1.02;
    letter-spacing: 0.01em;
    text-transform: uppercase;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 13px 26px;
    border-radius: 4px;
    font-weight: 600;
    font-size: 0.95rem;
    transition: transform 0.15s ease, background 0.15s ease, opacity .15s ease;
    white-space: nowrap;
  }
  .btn-primary { background: var(--stamp); color: var(--white); }
  .btn-primary:hover { background: var(--stamp-dark); transform: translateY(-1px); }
  .btn-primary:disabled { opacity: 0.6; transform: none; cursor: default; }
  .btn-outline { background: transparent; border: 1.5px solid currentColor; }
  .btn-outline:hover { background: rgba(0,0,0,0.05); }

  .site-header {
    position: sticky; top: 0; z-index: 100;
    background: rgba(226, 226, 226, 0.92);
    backdrop-filter: blur(6px);
    border-bottom: 1px solid var(--paper-line);
  }
  .site-header .container { display: flex; align-items: center; justify-content: space-between; height: 76px; }
  .logo { display: flex; flex-direction: column; line-height: 1; }
  .logo .wordmark { font-family: var(--font-display); font-weight: 800; font-size: 1.5rem; letter-spacing: 0.02em; }
  .logo .caption { font-family: var(--font-mono); font-size: 0.62rem; letter-spacing: 0.15em; color: var(--steel-600); margin-top: 3px; }

  .nav-links { display: flex; gap: 30px; align-items: center; }
  .nav-links a:not(.btn) { font-size: 0.94rem; font-weight: 500; position: relative; padding: 4px 0; }
  .nav-links a:not(.btn)::after {
    content: ''; position: absolute; left: 0; bottom: 0; width: 0; height: 2px;
    background: var(--stamp); transition: width 0.2s ease;
  }
  .nav-links a:not(.btn):hover::after { width: 100%; }

  .menu-toggle { display: none; flex-direction: column; gap: 5px; padding: 8px; }
  .menu-toggle span { width: 24px; height: 2px; background: var(--ink-900); transition: transform 0.2s ease, opacity 0.2s ease; }
  .menu-toggle.active span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
  .menu-toggle.active span:nth-child(2) { opacity: 0; }
  .menu-toggle.active span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

  .hero { background: var(--ink-900); color: var(--white); padding: 88px 0 100px; position: relative; overflow: hidden; }
  .hero .container { display: grid; grid-template-columns: 1.1fr 0.9fr; gap: 56px; align-items: center; }
  .hero-eyebrow { color: var(--pencil); margin-bottom: 22px; }
  .hero h1 { font-size: clamp(2.5rem, 5vw, 4.1rem); margin-bottom: 24px; }
  .hero .lead { font-size: 1.1rem; color: var(--steel-300); max-width: 46ch; margin-bottom: 36px; }
  .hero-ctas { display: flex; gap: 16px; flex-wrap: wrap; }
  .hero-ctas .btn-outline { border-color: var(--steel-300); }

  .ticket {
    background: var(--paper); color: var(--ink-900); border-radius: 6px;
    padding: 28px 28px 34px; box-shadow: 0 24px 48px -12px rgba(0,0,0,0.5);
    position: relative; transform: rotate(2deg);
  }
  .ticket-row-top {
    display: flex; justify-content: space-between; align-items: baseline;
    font-family: var(--font-mono); font-size: 0.72rem; letter-spacing: 0.08em;
    color: var(--steel-600); text-transform: uppercase; margin-bottom: 18px;
  }
  .ticket-row-top strong { color: var(--ink-900); font-size: 0.8rem; }
  .ticket-tear { border-top: 2px dashed var(--paper-line); margin: 18px 0; }
  .ticket-checklist { display: flex; flex-direction: column; gap: 13px; margin-bottom: 6px; }
  .ticket-checklist li { display: flex; align-items: center; gap: 10px; font-size: 0.96rem; font-weight: 500; }
  .ticket-checklist .icon { width: 17px; height: 17px; color: var(--pencil); flex-shrink: 0; stroke-width: 2.4; }
  .ticket-foot { font-family: var(--font-mono); font-size: 0.7rem; letter-spacing: 0.06em; color: var(--steel-600); text-transform: uppercase; }
  .ticket-stamp {
    position: absolute; bottom: -16px; right: -8px; width: 100px; height: 100px;
    border: 3px double var(--stamp); border-radius: 50%; color: var(--stamp);
    background: rgba(226,226,226,0.95); display: flex; align-items: center; justify-content: center;
    text-align: center; transform: rotate(-11deg); font-family: var(--font-mono);
    font-weight: 700; font-size: 0.7rem; letter-spacing: 0.06em; text-transform: uppercase; line-height: 1.3;
  }

  .section-head { max-width: 640px; margin-bottom: 52px; }
  .section-head.center { margin-left: auto; margin-right: auto; text-align: center; }
  .section-head .eyebrow { color: var(--stamp); margin-bottom: 14px; }
  .section-head h2 { font-size: clamp(2rem, 3.4vw, 2.7rem); margin-bottom: 16px; }
  .section-head p { color: var(--steel-600); font-size: 1.04rem; }
  .agendamento .section-head .eyebrow { color: var(--pencil); }
  .agendamento .section-head p { color: var(--steel-300); }

  .diferenciais { padding: 100px 0; background: var(--steel-100); }
  .cards-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 26px; }
  .card {
    background: var(--white); border: 1px solid var(--steel-200); border-radius: 8px;
    padding: 32px 24px; transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .card:hover { transform: translateY(-4px); box-shadow: 0 18px 32px -18px rgba(19,19,19,0.25); }
  .card .icon { width: 28px; height: 28px; color: var(--stamp); margin-bottom: 20px; stroke-width: 1.6; }
  .card h3 { font-family: var(--font-body); text-transform: none; font-weight: 700; font-size: 1.08rem; letter-spacing: 0; margin-bottom: 10px; }
  .card p { color: var(--steel-600); font-size: 0.94rem; }

  .servicos { padding: 100px 0; background: var(--paper); }
  .table-wrapper { overflow-x: auto; border: 1px solid var(--paper-line); border-radius: 8px; background: var(--white); }
  table.servicos-table { width: 100%; border-collapse: collapse; min-width: 760px; }
  .servicos-table th {
    font-family: var(--font-mono); font-size: 0.7rem; letter-spacing: 0.08em; text-transform: uppercase;
    text-align: left; padding: 16px 20px; background: var(--ink-900); color: var(--steel-300);
  }
  .servicos-table th:first-child { border-radius: 8px 0 0 0; }
  .servicos-table th:last-child { border-radius: 0 8px 0 0; }
  .servicos-table td { padding: 18px 20px; border-top: 1px solid var(--steel-200); font-size: 0.94rem; vertical-align: top; }
  .servicos-table tr:hover td { background: var(--steel-100); }
  .servicos-table .servico-nome { font-weight: 600; }
  .servicos-table .duracao { white-space: nowrap; color: var(--steel-600); }
  .servicos-table .valor { font-family: var(--font-mono); font-weight: 600; white-space: nowrap; }
  .servicos-note { margin-top: 16px; font-size: 0.85rem; color: var(--steel-600); }

  .agendamento { padding: 100px 0; background: var(--ink-900); color: var(--white); }

  .form-ticket {
    background: var(--paper); color: var(--ink-900); border-radius: 10px; padding: 40px;
    max-width: 760px; margin: 0 auto; position: relative; border-top: 4px dashed var(--paper-line);
  }
  .form-ticket-number {
    position: absolute; top: -15px; right: 32px; background: var(--ink-900); color: var(--pencil);
    font-family: var(--font-mono); font-size: 0.72rem; padding: 6px 14px; border-radius: 4px; letter-spacing: 0.05em;
  }
  .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
  .form-field { display: flex; flex-direction: column; gap: 6px; }
  .form-field.full { grid-column: 1 / -1; }
  .form-field label { font-size: 0.82rem; font-weight: 600; color: var(--ink-700); }
  .form-field label .opt { font-weight: 400; color: var(--steel-600); font-size: 0.78rem; }
  .form-field input, .form-field select, .form-field textarea {
    font-family: var(--font-body); font-size: 0.95rem; padding: 12px 14px;
    border: 1.5px solid var(--paper-line); border-radius: 5px; background: var(--white); color: var(--ink-900);
  }
  .form-field input:focus, .form-field select:focus, .form-field textarea:focus { border-color: var(--stamp); outline: none; }
  .form-field textarea { resize: vertical; min-height: 88px; }

  .form-submit-row { margin-top: 26px; display: flex; align-items: center; gap: 16px; flex-wrap: wrap; }
  .form-note { font-size: 0.8rem; color: var(--steel-600); }

  .form-error {
    display: none; color: var(--stamp); background: rgba(174,36,26,0.08); border: 1px solid var(--stamp);
    padding: 12px 16px; border-radius: 5px; font-size: 0.85rem; margin-top: 18px;
  }
  .form-error.active { display: block; }

  .form-success { display: none; text-align: center; padding: 8px 0 16px; }
  .form-success.active { display: block; }
  .stamp-confirm {
    display: inline-flex; align-items: center; justify-content: center; border: 4px double var(--stamp);
    color: var(--stamp); border-radius: 50%; width: 124px; height: 124px; font-family: var(--font-mono);
    font-weight: 700; letter-spacing: 0.05em; text-transform: uppercase; transform: rotate(-8deg) scale(0);
    margin-bottom: 20px; font-size: 0.92rem; opacity: 0;
  }
  .stamp-confirm.animate { animation: stampIn 0.5s cubic-bezier(.2,1.4,.4,1) forwards; }
  @keyframes stampIn {
    0% { transform: rotate(-8deg) scale(2.4); opacity: 0; }
    60% { transform: rotate(-8deg) scale(0.92); opacity: 1; }
    100% { transform: rotate(-8deg) scale(1); opacity: 1; }
  }
  .form-success h3 { text-transform: none; font-family: var(--font-body); font-size: 1.3rem; margin-bottom: 8px; }
  .form-success p { color: var(--steel-600); max-width: 42ch; margin: 0 auto; }
  .os-summary {
    font-family: var(--font-mono); font-size: 0.85rem; background: var(--steel-100); border-radius: 6px;
    padding: 16px; margin: 20px auto 0; max-width: 420px; text-align: left; color: var(--ink-900); line-height: 1.7;
  }

  .site-footer { background: var(--ink-800); color: var(--steel-300); padding: 72px 0 32px; }
  .footer-grid { display: grid; grid-template-columns: 1.4fr 1fr 1.2fr 1fr; gap: 40px; padding-bottom: 44px; border-bottom: 1px solid var(--ink-700); }
  .footer-grid h4 { font-family: var(--font-mono); font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase; color: #7A8083; margin-bottom: 18px; }
  .footer-grid > div > p { font-size: 0.9rem; line-height: 1.6; }
  .footer-list { display: flex; flex-direction: column; gap: 11px; font-size: 0.9rem; }
  .footer-list li { display: flex; gap: 10px; align-items: flex-start; }
  .footer-list .icon { width: 16px; height: 16px; flex-shrink: 0; margin-top: 3px; color: var(--pencil); stroke-width: 1.8; }
  .footer-list a:hover { color: var(--white); }
  .footer-bottom { padding-top: 26px; font-size: 0.8rem; color: #6C7376; }

  @media (max-width: 968px) {
    .hero .container { grid-template-columns: 1fr; }
    .ticket { transform: none; }
    .cards-grid { grid-template-columns: repeat(2, 1fr); }
    .footer-grid { grid-template-columns: 1fr 1fr; row-gap: 36px; }
  }
  @media (max-width: 720px) {
    .nav-links {
      position: fixed; top: 76px; left: 0; right: 0; background: var(--paper);
      flex-direction: column; align-items: flex-start; padding: 22px 24px 28px; gap: 18px;
      border-bottom: 1px solid var(--paper-line); transform: translateY(-130%); transition: transform 0.25s ease;
    }
    .nav-links.active { transform: translateY(0); }
    .nav-links a.btn { margin-top: 6px; }
    .menu-toggle { display: flex; }
    .hero { padding: 56px 0 64px; }
    .diferenciais, .servicos, .agendamento { padding: 64px 0; }
    .cards-grid { grid-template-columns: 1fr; }
    .form-grid { grid-template-columns: 1fr; }
    .form-ticket { padding: 28px 20px; }
    .footer-grid { grid-template-columns: 1fr; gap: 32px; }
  }
  @media (max-width: 640px) {
    .table-wrapper { overflow-x: visible; border: none; background: none; }
    table.servicos-table { min-width: 0; display: block; }
    .servicos-table thead { display: none; }
    .servicos-table tbody { display: block; }
    .servicos-table tr { display: block; background: var(--white); border: 1px solid var(--paper-line); border-radius: 8px; margin-bottom: 14px; padding: 14px 16px; }
    .servicos-table td { display: block; padding: 4px 0; border: none; white-space: normal; }
    .servicos-table .servico-nome { font-size: 1rem; margin-bottom: 6px; }
    .servicos-table .duracao::before { content: "Duração: "; color: var(--steel-600); font-weight: 600; }
    .servicos-table .valor::before { content: "Valor: "; color: var(--steel-600); font-weight: 600; }
  }
</style>
</head>
<body>

<svg style="display:none" aria-hidden="true">
  <symbol id="icon-wrench" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M21 7.5a5.5 5.5 0 0 1-7.44 5.16L6 20.24 3.76 18l7.58-7.56A5.5 5.5 0 0 1 18.5 3c.74 0 1.45.15 2.1.43l-4.2 4.2 1.94 1.94 4.2-4.2c.28.66.43 1.38.43 2.13z"/></symbol>
  <symbol id="icon-shield" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M12 3l7 3.2v5.3c0 5-3.2 8.3-7 9.5-3.8-1.2-7-4.5-7-9.5V6.2L12 3z"/></symbol>
  <symbol id="icon-receipt" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M6 3h12a1 1 0 0 1 1 1v17l-2.5-1.6L14 21l-2-1.6L10 21l-2.5-1.6L5 21V4a1 1 0 0 1 1-1z"/><line x1="8.5" y1="8" x2="15.5" y2="8"/><line x1="8.5" y1="12" x2="15.5" y2="12"/></symbol>
  <symbol id="icon-clock" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><circle cx="12" cy="12" r="9"/><polyline points="12 7 12 12 15.5 14"/></symbol>
  <symbol id="icon-check" viewBox="0 0 24 24" stroke-linecap="round" stro