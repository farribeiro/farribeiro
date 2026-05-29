## Hi there 👋

<!--
**farribeiro/farribeiro** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

<div class="calendar-box">
  <div class="calendar-header" id="month-year"></div>
  <div class="calendar-weekdays">
    <div>Dom</div><div>Seg</div><div>Ter</div><div>Qua</div><div>Qui</div><div>Sex</div><div>Sáb</div>
  </div>
  <div class="calendar-days" id="calendar-days"></div>
</div>

<style>
.calendar-box {
  font-family: sans-serif;
  max-width: 300px;
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
.calendar-header {
  text-align: center;
  font-weight: bold;
  margin-bottom: 15px;
  text-transform: capitalize;
}
.calendar-weekdays, .calendar-days {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  text-align: center;
}
.calendar-weekdays div {
  font-size: 0.8rem;
  font-weight: bold;
  color: #666;
  padding-bottom: 5px;
}
.calendar-days div {
  padding: 8px 0;
  font-size: 0.9rem;
}
.calendar-days .today {
  background: #0076ff;
  color: #fff;
  border-radius: 50%;
  font-weight: bold;
}
</style>

<script>
const dateNow = new Date();
const year = dateNow.getFullYear();
const month = dateNow.getMonth();

// Nome do mês no cabeçalho
const monthsBr = ["Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"];
document.getElementById('month-year').textContent = `${monthsBr[month]} ${year}`;

const firstDayIndex = new Date(year, month, 1).getDay();
const lastDay = new Date(year, month + 1, 0).getDate();

const daysContainer = document.getElementById('calendar-days');
let daysHtml = "";

// Espaços em branco para os dias do mês anterior na semana
for (let x = firstDayIndex; x > 0; x--) {
    daysHtml += `<div></div>`;
}

// Preenche os dias do mês
for (let i = 1; i <= lastDay; i++) {
    if (i === dateNow.getDate()) {
        daysHtml += `<div class="today">${i}</div>`;
    } else {
        daysHtml += `<div>${i}</div>`;
    }
}

daysContainer.innerHTML = daysHtml;
</script>

## Links rápidos

[https://www.globo.com](https://www.globo.com)
