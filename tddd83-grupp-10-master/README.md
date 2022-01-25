# TDDD83-grupp-10
**Medlemmar**  
Alva Ringi - alvri650,
Anton Jervebo - antje840,
Cecilia Persson - cecpe172,
Isak Berntsson - isabe723,
Linus Bergström - linbe 580,
Ludvig Eriksson Knast - ludkn080,
Victor Jonsson - vicjo972,
Vincent Bring - vinbr948

**Riktlinjer för Git**
| Riktlinje | Motivering |
| ------ | ------ |
| Alla commit-meddelanden på engelska. | Detta är best practice + minskar risken för att det blir fel då man använder olika plattformer/versioner etc som annars kan bråka med åäö. |
| Branchnamn på svenska eller engelska, men undvik åäö. | Minskar risken för att det blir fel då man använder olika plattformer/versioner etc som annars kan bråka med åäö. Dock svårt att ha helpt på engelska eftersom alla issues är på svenska. |
| Format för commitmeddelanden: startar med issuenummer. Om flera issues så rekommenderas format enligt följande: "55, 77 fixade bla bla". Engelska! | För att det ska gå att se vem som gjort vad och varför i koden. Förenklar tex felsökning och minskar risken att man råkar ha sönder andras kod pga att man inte visste vad den var viktig för. |
| Format för namn på issue-branches: "issuenummer_issue_name", tex "34_fixa_nån_grej". Måste inkludera minst ett ord efter siffra + underscore. Flera ord separeras med underscore. Undvik åäö! | Skapar överskådlighet över arbetet som görs. |

*Om ditt senaste commit-meddelande är felaktigt, tex saknar issue-nummer (ej pushat koden):*
- git commit --amend -m "&lt;issuenummer> nytt meddelade"
- git push

*Om ditt senaste commit-meddelande är felaktigt, tex saknar issue-nummer (redan pushat koden):*
_OBS detta förutsätter att ingen hunnit klona koden, annars kan det bli bråk!_
- git commit --amend -m "&lt;issuenummer> nytt meddelade"
- git push --force
  - förutsatt att du står i din branch & inte ställt in nån konstig upstream, annars git push origin master --force

**Generella Git-tips**
- Var himla försiktig med git reset --hard
  - Om du råkat använda git reset --hard "av misstag" så ge inte upp! Kolla i stället upp git lost and found, det finns sannolikt en räddning!
- Lite git-kommandon som är najs
  - git log för en lista av commits
  - git branch -l för lista av lokala branches?
  - git branch -r för lista av alla repos inkl de i GitLab?
  - git branch -vv för att lista alla brancher och vad de trackar remote
  - cat [filnamn] ger innehållet av en textfil ut i termainalen
    - less [filnamn] ger i samma, men sökbar och med lite andra features
- git add -i för _interactive_; kommer att visa de filer som har ändringar. Kort guide av detta finns till en början i Teams > General.
- Hanna rekommenderar git log & git ref log!

**Byte av standard-editor Vim > Visual Studio Code**  
- Shift + ctrl/command + p i Visual Studio ger ett sökfält, där skriver du "install code". 
- I terminalen skriver du sedan: _git config --global core.editor "code --wait"_
- Skriv sedan: _git config --global -e_  

**Allmäna tips**  
- Visual studio är bra att använda för att lösa mergekonflikter, men det finns även grafiska verktyg som tex _Source Tree_. Kan vara bra att kolla på om man behöver få visualiserat hur brancherna ser ut.

**Förslag på branching-struktur**  
- En master-branch som alltid ska innehålla en fungerande hemsida
- En branch från master för varje delsprint
- Utifrån sprint-branchen går feature branches för varje distinkt grej man jobbar på
  - När man pushar så gör man det först till sin feature branch och kollar så att den funkar, sen in till sprint-branchen
    - En branch för varje issue, som utgår från delsprint-branchen
  - Sprint-branchen pushas i sin helhet till master i slutet av sprinten, efter att vi testat så allt funkar
  - Specialhantering av bugfixes: merge direkt till master kan vara ok
    - Glöm i så fall inte pusha till feature branches med om det behövs!


**Riktlinjer för merge i tillgänglighetsarbetet**

-Sprint 3.2: Ha kvar det vi gjorde lighthouse på. OBS! Rör ej.

-Sprint 3.2 Funk: Merga bara ny funktionalitet

-Sprint 3.3: Merga tillgänglighet OCH ny funktionalitet

OBS! Om man jobbar med ytterliggare funktionalitet ska man alltså merga två gånger, en gång till sprint3.2 funk och en gång till sprint 3.3




