---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS
css: unocss
---

# Microsoft .NET

Vari framework per lo sviluppo cross-platform e in passato Windows only


---


# Cos'è .NET

Il framework .NET

.NET è un framework basato su C# che consente di creare backend per siti web, applicazioni cross-platform, bot e tanto altro.

Per fare un paragone è simile a Node.JS solo che usa C# come linguaggio di programmazione.

<br>

<div flex justify-center items-center gap-2>
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Microsoft_.NET_logo.svg" width="256">
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/0d/C_Sharp_wordmark.svg" width="256">
</div>


---

# La storia di Microsoft .NET

Microsoft .NET viene creato da Microsoft nel 2002 per sviluppare applicazioni Windows e per la contrastare PHP nello sviluppo backend di siti web
Si distingue in 2 versioni:

- .NET(in precedenza .NET Core), Framework per la creazione di applicazioni cross-platform, creazione del backend per siti web e per lo sviluppo general-purpose(AI, Bot...)
- .NET Framework, Framework per la creazione di applicazioni GUI Windows only

Prima del 2016, .NET era un framework closed-source e funzionante solo su Windows, alcuni sviluppatori però provarono a portare .NET su Linux e MacOS con il progetto Mono.
<br/>
<br/>
Nel 2016 nasce .NET Core, una fork di Mono, ufficialmente supportato da Microsoft che porta il supporto su MacOS e Linux, supporta solo però ASP.NET per creare backend.
<br/>
<br/>
Anche .NET Framework diventa open-source come molti altre parti del linguaggio c#.
Successivamente nascono progetti open-source per la creazione di GUI cross-platform.
<br/>
<br/>
Nel 2022/2023 nasce .NET MAUI, un framework ufficiale di Microsoft che permette la creazione di GUI su tutte le piattaforme.
[Dotnet source code](https://github.com/dotnet)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# Linguaggio C#

Il linguaggio di .NET

C# è il linguaggio ufficiale del framework .NET insieme a F#.
<br>
<br>
è un linguaggio compilato in un linguaggio intermedio simile al linguaggio macchina e poi interpretato successivamente dal runtime, ed è per questo che garantisce performance migliori di Node.JS o Python ma inferiori a Rust o Go.
<br>
<br>
C# implementa completamente tutti i paradigmi di un linguaggio ad oggetti.


```c# {all|2|1-6|9|all}
public class Persona{
  String name;
  String cognome;
  Datetime nascita;
  public int anni{
    return Datetime.now - this.nascita;
  }
}
// Questa classe descrive una persona e il metodo anni restituisce gli anni di età
```
Un programma del genere scritto in C# ci impiega nell'esecuzione 298ms mentre C++ 152ms.

---

# NET rispetto a Node.JS

<br/>
 
- ASP.NET per il backend è molto più veloce di Node.JS ed implementa un server web completo e performante detto Kestrel.
In un semplice stress test, .NET con Kestrel riesce a gestire 50000 richieste con un tempo di 1,43ms mentre Node.JS con Express.JS(dato che node non implementa un server web completo ma ha una libreria basica per gestire le richieste) gestisce solo 35000 richieste con un tempo di 7ms.

- C# implementa anche i puntatori anche se Microsoft non consiglia questa pratica. 

- Essendo C# un linguaggio ad oggetti, il server API viene molto pulito dove ogni endpoint è una classe, quindi un file separato ed è quindi più facile fare manutenziane al codice.

- .NET implementa una libreria detta Linq che porta una maggiore sicurezza nel caso di operazioni su un DB SQL(riduce le probabilità di SQL injection) e porta la sintassi di SQL anche per vari tipi di strutture dati.

- Solitamaente backend e frontend girano sullo stesso server Kestrel, su Node.JS durante lo sviluppo il backend e il frontend sono su due server separati e quindi hanno 2 porte diverse

---
class: px-20
---

# Difetti di .NET

I difetti di .NET

- Su Linux non ha ancora una IDE dedicata gratuita, tuttavia si può usare VSCode con delle estensioni senza problemi oppure Rider(a pagamento), l'unica IDE open-source che esisteva(Monodevelop) è stata resa closed-source da Microsoft e resa compatibile solo con MacOS.
- Rispetto a JS è più complicato però sinceramente preferisco così, ad esempio la tipizzazione dei dati.
- Eseguire lo scaffolding di un DB che non è Microsoft SQL può risultare complicato.
- I framework per sviluppare app mobili sono molto complicati e poco documentati. Molto meglio quelli basati su Node.JS


---

# Come ho usato .NET nel mio PCTO

I progetti

.NET è stato il cuore di tutti i progetti che abbiamo fatto, infatti tutto il backend era basato su .NET mentre il frontend è stato sviluppato in Svelte, tuttavia il web server per entrambi i progetti è sempre stato Kestrel dato che su .NET backend e frontend vanno insieme.

In particolare è stato usato per creare un password manager che implementasse una criptazione delle password e in base alla persona e al gruppo a cui apparteneva il portale restituiva delle password diverse.<br><br>
Poi abbiammo usato .NET per un sistema gestionale per una carrozzeria insieme a React mentre l'app per telefono era scritta con Java anche se mi sono occupato sul del backend.<br><br>
Infine abbiamo fatto un sito vetrina per un gommista ma non avendo bisogno del backend abbiamo usato solo Svelte

