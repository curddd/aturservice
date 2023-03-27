der turing hat mal gesagt

also 


man stelle sich ein ticker tape for, oder ne klorolle
auf jeder rolle steht ... 1 byte, ne ich mein auf deme papier, 1byte = 8bits ok

man kann das klopaier ins klo tunken und spülen, dan rollt alles ab, toll
nix passiert

man kann es auch ins 'memory' laden, aber wir haben es ja schon auf papier
nämlich als block, bzw uint8arr = []


jetzt könnte man so sagen
erst liest er immer ne zahl vor die er sieht, papier für papier
aber dann wollen wir auch ein if
also ein byte muss ne if sein... 
sagen wir mal 0

so

123 3 5 0

ok jetzt kommt ein if

if WAS?

ja .. 

also ohne, mehrere file streams oder, stapel. geht es nicht

also es gibt den ersten: machen wir den einfach current
# fd cur
und dann noch einen für zwischenrechnungen
# fd tmp

jetzt wird es aber knapp mit den instructions, weil jede neue inst macht die bytes kleiner

### instruction set 
FLUSH . ein byte ist ein byte

ah aber wie enden wir dne flush?
und was flusht er wo? egal

IF . jetzt kommt ein IF

CONTEXT . setze context

FONT . setzte font? cann mit context gemacht werden

DEFCONTEXT definiere neue kontexte

SETFD . wechlse 'rolle'




sind wir mal nich so geizig mit den bits und bytes

könnte man nciht einfach fonts setzten und dann
print ab jetzt mit font so und so

man kännte auch kontext setzen für ffolgendes etc


---

so aber jezt geht das schon mit betrachtung in das os rein, weil 

os macht eigentlich sachen wie 
öffnen von fd, r/w und das wars

eine cpu hat damit nix am hut ne

wie wäre es mit einem

# fd fds


### cpu layout
FDS | ???????

naja die sache is es gibt operations also
wenn die logik wirklich transistorschaltungen sind
muss es 2 register geben?

OPA OPB



was die CPU macht:

also eigentlcih würde die dann je nach context einfach bytes einelsen am derzeitigen punkt von fd

CTX OFF

vielleicht braucht es einen PUSH CTX

weil, wenn wir im FLUSH sind... und dann brauch es ja mind. ein escape / ret
damit das ENDE da ist

mehr bytes heisst nur das man mehr instructions hat und so

eine 8bit cpu könnte wohl nicht utf8 ausgeben

sonst wärs ja nicht ein flush, sondern ständiges konditionalisieren 
leider geht das in china nicht anders, ausser die lernen englisch

utf8 on 8bit:
DEF CONTEXT  UTF8:
IF byte&b1000000

WARUM SO ALLGEMEIN

soll china doch ihren eigenen decoder haben

china müsste für ihre sachen auf 16 bit laufen?

PUTC:
    also lalso alaos
    putc schaut den byte offset in fd_char nach
    je nach byte anzahl schickt es dne nächsten n bytes an den output

jetzt könnte man noch den byte kontext angeben
oder eine kontext änderung lässt ganz viel anders laufen
d.h. der mov von 1 byte wird mov 2 byte

cpus können doch schon modes hoch switchen
runter und quer is vielleicht nich so gut?

dann muss man halt padden?
EINE IF / TRANSITORITORY SHIT IS SCHION ZU VUEL NE

MEINE PERFORMANCE

JA DANN BLEIB IN 8 BIT

---


naja späte gehts weiter

register brauch man ja weil die cpu sonst, doer iregndiwe

das is halt der schnellzugriff ne 

aber wie is der abluaf von naem computer anywy=?


gibt rechnen
und ausführen von jmp und so, und dann cond checkers

aber wieviel wird gerechnet???

terminal: screen, tasta
terminal-graphical: screen, tasta, touch/mouse

input, könnte dohc direkt an den screne gehen

input -> schickt msg zu screne, 
buffer könnte im screen hängen
bei speziellem input registered:
fire messages...
sonst
die screen chip displayd input nach eigener logik
also cpu im screen

hat doch eh nen jip doer

bei games / videos
stream wird ausgelesen
input muss an den stream provider gehen

"rechenjobs", muss man schauen
send file -> save
get file -> read

hm
xD

cont.










