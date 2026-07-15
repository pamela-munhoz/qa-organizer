# QA Organizer — Apontamento de Horas

App local para organizar o dia a dia de QA: cronômetro por tarefa, apontamento `/spend` pronto para o GitLab e entrega de versões por sistema (GerencieAqui / SIEM).

## Como usar

Basta abrir o arquivo `index.html` no navegador (duplo clique). Não precisa instalar nada.

> **Importante:** os dados ficam salvos no navegador (localStorage) e são vinculados à forma de abrir o arquivo. Use sempre o mesmo navegador e a mesma forma de abrir (ex.: sempre duplo clique no `index.html`) para não "perder de vista" os dados. Faça backups periódicos em **Configurações → Exportar backup (JSON)**.

## Funcionalidades

### 📅 Agenda
- Adicione tarefas com título + link do GitLab. Se o link já existir, a tarefa é reaproveitada (tempo somado por dia).
- **▶ Iniciar / ⏹ Parar** captura o horário atual do computador. Iniciar uma tarefa para automaticamente a anterior.
- Sessões repetidas da mesma tarefa no mesmo dia são **somadas**.
- Horários de início/fim são **editáveis** manualmente.
- Navegue pelo calendário para ver os apontamentos de qualquer dia.
- Botão **📋 /spend** copia o comando pronto, ex.: `/spend 1h30m 2026-07-15` (tempo + data do dia visualizado).
- **Copiar todos os /spend** copia um resumo do dia com todas as tarefas.

### Ações rápidas (chips roxos)
Atividades recorrentes com link fixo do GitLab (Reunião, Daily, Auxílio equipe...). Um clique já inicia o cronômetro. Cadastre os links em **⚙️ Configurações**.

### Pausas (chips amarelos)
Eventos **sem apontamento** (Cantina 15m, Almoço 60m). Um clique registra a pausa com a duração padrão — os horários podem ser editados depois. Cadastre outros em Configurações.

### 🏷️ Versões
- Cadastre versões por sistema (GerencieAqui e SIEM já vêm criados; cadastre outros em **⚙️ Configurações → Sistemas**).
- Direcione cada tarefa testada para seu sistema + versão.
- **📄 Gerar TXT da entrega**: arquivo com as tarefas agrupadas por sistema e versão, com título e link do GitLab, pronto para enviar ao suporte.
- **Filtro da entrega**: marque exatamente quais versões (por sistema) entram no TXT — botões "Marcar todas" / "Desmarcar todas" ajudam na seleção.

### 📊 Relatórios
- Período padrão: mês atual (editável), com filtros por sistema e versão (default "Todos").
- **Tarefas por tipo**: na tabela "Tarefas testadas" (aba Versões) marque o **Tipo** (Melhoria/Erro/Hotfix) de cada tarefa. O relatório mostra a tabela por sistema e um gráfico de pizza (azul = melhoria, amarelo = erro, vermelho = hotfix).
- **Testado com erro**: marque "voltou" na tarefa e selecione para qual dev ela retornou (cadastre os devs em Configurações). O relatório mostra a tabela de retornos por dev e um gráfico de colunas.
- **📄 Exportar PDF**: gera uma versão limpa do relatório (tabelas + gráficos, respeitando período e filtros) e abre a janela de impressão — escolha "Salvar como PDF" como destino.

### ⚙️ Configurações
- **Sistemas**: cadastre quantos precisar (cada um ganha uma cor própria). Renomear atualiza automaticamente versões e tarefas vinculadas; excluir um sistema exclui as versões dele e desvincula as tarefas.
- **Desenvolvedores**: cadastre os devs da equipe para usar no marcador "testado com erro".
- CRUD de ações rápidas e pausas.
- Backup: exportar/importar JSON e apagar dados.
