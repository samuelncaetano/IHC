---
tags: Monthly
cssclasses: monthly, <% moment().add(1, 'months').format("YYYY-MM") %>
---

# REGISTRO MENSAL – <% moment().add(1, 'months').format("MMMM [de] YYYY") %>

## Visão Geral do Mês

<%*
const today = new Date();
const nextMonthDate = new Date(today.getFullYear(), today.getMonth() + 1, 1);
const year = nextMonthDate.getFullYear();
const month = nextMonthDate.getMonth(); // 0-indexed: janeiro é 0
const totalDays = new Date(year, month + 1, 0).getDate();
const weekdays = ["Dom", "Seg", "Ter", "Qua", "Qui", "Sex", "Sáb"];

let calendar = "";
for (let i = 1; i <= totalDays; i++) {
  const date = new Date(year, month, i);
  const dayName = weekdays[date.getDay()];
  calendar += `${i.toString().padStart(2, '0')} ${dayName} -\n`;
}
tR += calendar;
%>


## Tarefas do Mês

- [ ] Tarefa 1
- [ ] Tarefa 2
- [ ] Tarefa 3

## Notas

- ...
