---
tags: Monthly
cssclasses: monthly, <% tp.date.now("YYYY-MM") %>
---

# REGISTRO MENSAL – <% tp.date.now("MMMM [de] YYYY") %>

## Visão Geral do Mês

<%*
const daysInMonth = (year, month) => new Date(year, month + 1, 0).getDate();
const month = tp.date.now("MM") - 1; // Mês atual (0-11)
const year = tp.date.now("YYYY");
const totalDays = daysInMonth(year, month);
const weekdays = ["Dom", "Seg", "Ter", "Qua", "Qui", "Sex", "Sáb"];

let calendar = "";
for (let i = 1; i <= totalDays; i++) {
  const date = new Date(year, month, i);
  const day = weekdays[date.getDay()];
  calendar += `${i.toString().padStart(2, '0')} ${day} -\n`;
}
tR += calendar;
%>

## Tarefas do Mês

- [ ] Tarefa 1
- [ ] Tarefa 2
- [ ] Tarefa 3

## Notas

- ...
