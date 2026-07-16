---
description: "Week 1 of the program: spend seven days just watching your own scrolling patterns, without restricting anything yet."
---

# Week 1. Just Watch What Happens

The temptation at this stage is to delete everything immediately and 
declare "new life starting Monday." Don't do that. A sudden cutoff 
without preparation almost always ends in relapse within a few days — 
often a stronger one, because you never got to understand your real 
patterns or find anything to replace them with.

Week one is observation only. You don't restrict yourself from 
anything. You just watch.

## What to Do Each Day

Set up a simple note — in your phone's notes app or on paper, doesn't 
matter. Every time you open a short-video app, jot down the time and 
one word about what you felt right before. Bored. Anxious. 
Procrastinating on something. Hand just moved on its own. This 
shouldn't take more than five seconds — otherwise you'll drop the 
tracking by day two.

Also check your phone's built-in screen time stats at the end of each 
day — every modern smartphone has this — and write down the total. 
Not to beat yourself up, but to see the gap between "I felt like I 
watched maybe twenty minutes" and what the counter actually shows.

## A Tracker, If You Want One

You can keep this in a paper notebook and it works just as well. But the
phone is usually where the scrolling happens, so it might as well be
where the counting happens too. This one runs entirely in your browser —
nothing is sent anywhere and nothing is saved to any server, so it stays
private to this device. Each time you open a short-video app, tap the
reason.

<div class="ss-tracker" data-ss-tracker>
  <div class="sst-head">
    <div class="sst-today">
      <span class="sst-count" data-sst-count>0</span>
      <span class="sst-label">opens logged today</span>
    </div>
    <button type="button" class="sst-reset" data-sst-reset>Reset</button>
  </div>
  <p class="sst-prompt">What pulled you in just now?</p>
  <div class="sst-chips">
    <button type="button" class="sst-chip" data-trigger="bored">Bored</button>
    <button type="button" class="sst-chip" data-trigger="anxious">Anxious</button>
    <button type="button" class="sst-chip" data-trigger="procrastinating">Avoiding a task</button>
    <button type="button" class="sst-chip" data-trigger="waiting">Waiting</button>
    <button type="button" class="sst-chip" data-trigger="habit">Just habit</button>
    <button type="button" class="sst-chip" data-trigger="other">Other</button>
  </div>
  <div class="sst-summary" data-sst-summary></div>
  <div class="sst-foot">
    <button type="button" class="sst-undo" data-sst-undo hidden>Undo last</button>
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
  var S={week:"This week:",common:"Most common:",none:"No reasons logged yet — tap one above.",confirm:"Clear everything you've logged? This can't be undone.",
    tr:{bored:"Bored",anxious:"Anxious",procrastinating:"Avoiding a task",waiting:"Waiting",habit:"Just habit",other:"Other"}};
  var KEY="scrollstop.week1.v1", LOC="en-US";
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

## Days 3-4: Finding the Pattern

By day three you'll have enough notes to spot recurring situations. 
People usually find three or four main triggers: boredom on transit, 
wanting to delay an unpleasant task, a habit of scrolling before bed, 
or just an automatic action with no real trigger — the hand reaches 
for the phone faster than a thought even forms.

Write these triggers down separately. You'll need them next week.

## Days 5-7: One Small But Important Question

In the second half of the week, add one thing: before opening the 
app, ask yourself one question — "why am I doing this right now?" No 
need to answer at length, no need to stop yourself. Just ask the 
question, then open the app if you still want to. The simple act of 
a half-second pause before an automatic action starts, bit by bit, 
handing control back to you — you turn a reflex into a choice, even 
if it's still the same choice for now.

## By the End of the Week

Look at your notes as a whole. How much total time went by over the 
week? Which three triggers repeated the most? Was there even once 
where you paused after asking "why" and didn't open the app?

This is your baseline. Everything from here forward works with these 
specific triggers and specific numbers — not with an abstract 
"addiction," but with your own personal picture.