---
description: "Неделя 1 программы: семь дней просто наблюдай за своими паттернами скроллинга, ничего пока не ограничивая."
---

# Неделя 1. Просто наблюдай, что происходит

Соблазн на этом этапе — сразу удалить всё и объявить "с 
понедельника новая жизнь". **Не делай этого.** Резкий отказ без 
подготовки почти всегда заканчивается откатом через несколько 
дней, часто с удвоенной силой — потому что ты не успел понять 
свои реальные паттерны (шаблоны) и не успел ничем их заменить.

Первая неделя — только наблюдение. Ты ничего не запрещаешь себе. 
Ты просто анализируешь.

## Что делать каждый день

Заведи простую заметку — в блокноте на телефоне или на бумаге, 
не важно. Каждый раз, когда открываешь приложение с короткими 
видео, делай пометку: время и одно слово о том, что ты чувствовал 
прямо перед этим. Скука. Тревога. Прокрастинация перед задачей. 
Просто рука сама потянулась. Это не должно занимать больше пяти 
секунд — иначе ты бросишь трекинг на второй день.

Также в конце дня посмотри встроенную статистику экранного 
времени в телефоне — она есть в любом современном смартфоне — 
и запиши итоговое число. Это делается не для того, чтобы себя ругать, а чтобы 
увидеть разницу между "мне казалось, что я смотрел минут двадцать" 
и тем, что показывает счётчик.

## Трекер, если он тебе нужен

Можно вести это в бумажном блокноте — работает не хуже. Но скроллинг
обычно происходит в телефоне, так что пусть и подсчёт будет там же. Этот
трекер работает целиком в твоём браузере — ничего никуда не отправляется
и не сохраняется ни на каком сервере, данные остаются приватными на этом
устройстве. Каждый раз, когда открываешь приложение с короткими видео,
нажимай причину.

<div class="ss-tracker" data-ss-tracker>
  <div class="sst-head">
    <div class="sst-today">
      <span class="sst-count" data-sst-count>0</span>
      <span class="sst-label">открытий за сегодня</span>
    </div>
    <button type="button" class="sst-reset" data-sst-reset>Сбросить</button>
  </div>
  <p class="sst-prompt">Что потянуло тебя туда только что?</p>
  <div class="sst-chips">
    <button type="button" class="sst-chip" data-trigger="bored">Скука</button>
    <button type="button" class="sst-chip" data-trigger="anxious">Тревога</button>
    <button type="button" class="sst-chip" data-trigger="procrastinating">Избегаю дело</button>
    <button type="button" class="sst-chip" data-trigger="waiting">Ожидание</button>
    <button type="button" class="sst-chip" data-trigger="habit">Просто привычка</button>
    <button type="button" class="sst-chip" data-trigger="other">Другое</button>
  </div>
  <div class="sst-summary" data-sst-summary></div>
  <div class="sst-foot">
    <button type="button" class="sst-undo" data-sst-undo hidden>Отменить последнее</button>
  </div>
</div>

<style>
.ss-tracker{border:1px solid var(--md-default-fg-color--lightest);border-radius:.6rem;padding:1rem 1.1rem;margin:1.4rem 0;background:var(--md-code-bg-color)}
.ss-tracker .sst-head{display:flex;align-items:center;justify-content:space-between;gap:1rem}
.ss-tracker .sst-today{display:flex;align-items:baseline;gap:.5rem}
.ss-tracker .sst-count{font-size:2.2rem;font-weight:700;line-height:1;color:var(--md-primary-fg-color)}
.ss-tracker .sst-label{font-size:.72rem;color:var(--md-default-fg-color--light)}
.ss-tracker .sst-reset{font-size:.68rem;background:none;border:0;color:var(--md-default-fg-color--light);cursor:pointer;text-decoration:underline;padding:.2rem}
.ss-tracker .sst-prompt{margin:.9rem 0 .55rem;font-size:.82rem;color:var(--md-default-fg-color--light)}
.ss-tracker .sst-chips{display:flex;flex-wrap:wrap;gap:.4rem}
.ss-tracker .sst-chip{font:inherit;font-size:.78rem;padding:.4rem .75rem;border-radius:2rem;border:1px solid var(--md-primary-fg-color);background:transparent;color:var(--md-primary-fg-color);cursor:pointer;transition:transform .1s,background .15s,color .15s}
.ss-tracker .sst-chip:hover{background:var(--md-primary-fg-color);color:#fff}
.ss-tracker .sst-chip.is-pulse{transform:scale(.9)}
.ss-tracker .sst-summary{margin-top:1.1rem}
.ss-tracker .sst-week{display:flex;justify-content:space-between;flex-wrap:wrap;gap:.5rem;font-size:.72rem;color:var(--md-default-fg-color--light);margin-bottom:.5rem}
.ss-tracker .sst-bars{display:flex;align-items:flex-end;gap:.35rem}
.ss-tracker .sst-bar{flex:1;display:flex;flex-direction:column;align-items:center;gap:.15rem}
.ss-tracker .sst-track{height:48px;width:100%;display:flex;align-items:flex-end;justify-content:center}
.ss-tracker .sst-fill{width:100%;max-width:24px;background:var(--md-primary-fg-color);border-radius:3px 3px 0 0;opacity:.85;min-height:3px}
.ss-tracker .sst-n{font-size:.62rem;color:var(--md-default-fg-color--light)}
.ss-tracker .sst-d{font-size:.6rem;color:var(--md-default-fg-color--light);opacity:.7}
.ss-tracker .sst-foot{margin-top:.7rem}
.ss-tracker .sst-undo{font-size:.7rem;background:none;border:1px solid var(--md-default-fg-color--lightest);border-radius:.4rem;padding:.28rem .6rem;color:var(--md-default-fg-color--light);cursor:pointer}
</style>

<script>
(function(){
  var S={week:"За неделю:",common:"Чаще всего:",none:"Причин пока нет — нажми любую выше.",confirm:"Очистить всё, что ты отметил? Это нельзя отменить.",
    tr:{bored:"Скука",anxious:"Тревога",procrastinating:"Избегаю дело",waiting:"Ожидание",habit:"Просто привычка",other:"Другое"}};
  var KEY="scrollstop.week1.v1", LOC="ru-RU";
  function dk(d){return d.getFullYear()+"-"+(d.getMonth()+1)+"-"+d.getDate();}
  function load(){try{return JSON.parse(localStorage.getItem(KEY))||[];}catch(e){return[];}}
  function save(a){try{localStorage.setItem(KEY,JSON.stringify(a));}catch(e){}}
  document.querySelectorAll("[data-ss-tracker]").forEach(function(el){
    if(el.__i)return;el.__i=1;
    var cEl=el.querySelector("[data-sst-count]"),sEl=el.querySelector("[data-sst-summary]"),uBtn=el.querySelector("[data-sst-undo]");
    function render(){
      var a=load(),today=dk(new Date());
      cEl.textContent=a.filter(function(e){return e.d===today;}).length;
      uBtn.hidden=a.length===0;
      var days=[],tally={};for(var i=6;i>=0;i--){var d=new Date();d.setDate(d.getDate()-i);days.push(d);}
      a.forEach(function(e){if(e.tr){tally[e.tr]=(tally[e.tr]||0)+1;}});
      var counts=days.map(function(d){var k=dk(d);return a.filter(function(e){return e.d===k;}).length;});
      var total=counts.reduce(function(s,x){return s+x;},0),max=Math.max.apply(null,counts.concat([1]));
      var bars=days.map(function(d,i){var c=counts[i],h=Math.max(Math.round(c/max*100),4);
        return '<div class="sst-bar"><div class="sst-track"><div class="sst-fill" style="height:'+h+'%"></div></div><span class="sst-n">'+c+'</span><span class="sst-d">'+d.toLocaleDateString(LOC,{weekday:"short"})+'</span></div>';}).join("");
      var top=null,tn=0;Object.keys(tally).forEach(function(k){if(tally[k]>tn){tn=tally[k];top=k;}});
      var topLine=top?(S.common+" "+(S.tr[top]||top)+" ("+tn+")"):S.none;
      sEl.innerHTML='<div class="sst-week"><span>'+S.week+" "+total+'</span><span>'+topLine+'</span></div><div class="sst-bars">'+bars+'</div>';
    }
    el.querySelectorAll(".sst-chip").forEach(function(b){b.addEventListener("click",function(){
      var a=load();a.push({d:dk(new Date()),t:Date.now(),tr:b.getAttribute("data-trigger")});save(a);render();
      b.classList.add("is-pulse");setTimeout(function(){b.classList.remove("is-pulse");},220);});});
    uBtn.addEventListener("click",function(){var a=load();a.pop();save(a);render();});
    el.querySelector("[data-sst-reset]").addEventListener("click",function(){if(confirm(S.confirm)){save([]);render();}});
    render();
  });
})();
</script>

## Дни 3-4: ищем закономерность

К третьему дню у тебя накопится достаточно записей, чтобы 
заметить повторяющиеся ситуации. Обычно люди находят три-четыре 
главных триггера: это может быть скука в транспорте, желание 
отсрочить неприятную задачу, привычка листать перед сном, 
или просто автоматическое действие без всякой причины — рука 
тянется к телефону быстрее, чем формируется мысль.

Выпиши эти триггеры отдельно. Они понадобятся тебе уже на 
следующей неделе.

## Дни 5-7: маленький, но важный вопрос

На второй половине недели добавь один пункт: перед тем как 
открыть приложение, задай себе один вопрос — "зачем я делаю 
это сейчас?" Не нужно себе отвечать развёрнуто, не нужно себя 
останавливать. Просто задать вопрос и открыть приложение, если 
хочется. Сам факт паузы в полсекунды перед автоматическим 
действием начинает по чуть-чуть возвращать контроль — ты 
превращаешь рефлекс в выбор, пусть пока и такой же.

## В конце недели

Посмотри на записи целиком. Сколько времени в сумме ушло за 
неделю? Какие три триггера повторялись чаще всего? Было ли 
хоть раз, что ты остановился после вопроса "зачем" и не открыл 
приложение?

Это твоя точка отсчёта. Дальше мы будем работать именно с этими 
конкретными триггерами и конкретными цифрами — не с абстрактной 
"зависимостью", а с твоей конкретной картиной.