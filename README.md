# V8-DOHC-Crossplane

Interaktives Modell eines Viertakt-V8 mit 90°-Crossplane-Kurbelwelle, vier obenliegenden Nockenwellen und Steuerkette. Die Geometrie folgt veröffentlichten Motordaten, nicht einer freien Animation.

Öffnen: `V8_DOHCV8_FULL_READY.html` im Browser. Drehzahl 0–4000, Orbit mit der Maus, `Schritt 90°` rückt eine Zündung weiter.

## Was das Modell festlegt

| Größe | Wert | Herkunft |
| --- | --- | --- |
| Bankwinkel | 90° | üblicher Crossplane-V8 |
| Hubzapfen | vier, je zwei Pleuel, Ebenen um 90° versetzt, äußere und innere Zapfen je 180° | Crossplane-Kurbelwelle |
| Drehrichtung | im Uhrzeigersinn von vorn | Small-Block-Chevrolet |
| Zählung | 1-3-5-7 links, 2-4-6-8 rechts, von vorn | GM |
| Zündfolge | 1-8-4-3-6-5-7-2 | Small- und Big-Block ohne 4/7-Tausch |
| Begleiter (gemeinsamer OT, gegenläufiger Takt) | 1/6, 8/5, 4/7, 3/2 | dieselbe Kurbel |
| Hub / Pleuel | 3,48″ / 5,70″, Verhältnis 1,64 | Chevrolet 350 |
| Nocken | halbe Kurbeldrehzahl, Kette 2:1 | Viertakt |
| Auslass | öffnet 50° vor UT, schließt 18° nach OT | innerhalb 40–80° vor UT und 10–50° nach OT |
| Einlass | öffnet 18° vor OT, schließt 50° nach UT | innerhalb 10–50° vor OT und 40–80° nach UT |
| Zündung | fest 15° vor OT | kein Verstellkennfeld |
| Bankfolge | L-R-R-L-R-L-L-R | Intervalle je Bank 90/180/180/270 |

Die linke Bank steht 45° rechts der Senkrechten, wenn man von vorn auf die Kurbel sieht (Fahrerseite). Dieselbe Kurbelkröpfung erreicht die rechte Zylinderachse erst nach 270° im Uhrzeigersinn. Dadurch zündet Zylinder 2 bei 630°, nicht 90° nach Zylinder 1. Zapfenwinkel bei Zünd-OT von Zylinder 1, gemessen im Uhrzeigersinn ab Senkrechter: 45°, 135°, 315°, 225°.

Kolbenweg ist das ebene Schubkurbelgetriebe mit Bohrungsachse durch die Kurbelmitte:

`d = r·cos φ + √(l² − r²·sin² φ)`

`φ` ist der Winkel zwischen Hubzapfen und Bohrungsachse. Ventilhub ist eine harmonische Nocke (0 an den Rampenenden). Der gezeichnete Hub ist gegenüber einem Serienventil vergrößert, damit die Bewegung lesbar bleibt. Je Zylinder ein Einlass- und ein Auslassventil; die Steuerzeiten gelten ebenso für ein zweites Ventil derselben Nocke.

## Quellen

- [Crossplane](https://en.wikipedia.org/wiki/Crossplane) — zwei Zapfenebenen, gleichmäßige 90°-Zündabstände, ungleiche Bankintervalle 180/90/180/270, schwere Gegengewichte
- [Hot Rod: Cross-Plane und Flat-Plane](https://www.hotrod.com/how-to/difference-between-cross-plane-and-flat-plane-cranks) — äußere Zapfen in einer Ebene, innere senkrecht dazu, Zündfolge 1-8-4-3-6-5-7-2
- [OnAllCylinders: Chevy firing orders](https://www.onallcylinders.com/2022/12/27/chevy-small-block-firing-orders-the-evolution-of-cylinder-firing-order-swaps/) — Begleiterpaare und der spätere LS-Tausch auf 1-8-7-2-6-5-4-3
- [MOTOR, März 2009](https://www.motor.com/magazine-summary/performance-perspectives-march-2009/) — Paare 1/6, 2/3, 4/7, 5/8
- [JEGS: Firing order](https://www.jegs.com/tech-articles/engine-firing-order-explained/) — GM-V8 im Uhrzeigersinn, Begleiter
- [AA1Car: Chevy firing order](https://www.aa1car.com/library/chevy_firing_orders.htm) — 1-8-4-3-6-5-7-2 für Small- und Big-Block
- [Engine Builder: Rod ratios](https://www.enginebuildermag.com/2016/08/understanding-rod-ratios/) und [Hot Rod: 350](https://www.hotrod.com/how-to/inch-small-block-chevrolet/) — 5,7″ Pleuel, 3,48″ Hub
- [Ventilsteuerung, TU Košice](https://katedry.sjf.tuke.sk/kkadi/images/ZS_2024-25/KAeng/AD_2L23.pdf) — Öffnungsbereiche und Übersetzung 2:1
- [EngineersUniverse V8-Simulator](https://engineersuniverse.com/labs/engineering/mechanical/v8-engine) und [DOHC-V8-Modell](https://www.printables.com/model/1564524-v8-functional-engine-model-dohc-version) — dieselbe Zündfolge als Funktionsmodell

## Grenzen

Keine Gasdynamik, kein Massenausgleich über die sichtbaren Gegengewichte hinaus, keine last- oder drehzahlabhängige Zündverstellung, kein Ventilspiel. Die Bohrung ist etwas enger gezeichnet als 4,00″ im gewählten Maßstab, damit sich die 90°-Laufbuchsen nicht durchdringen. Ein LS- oder Flatplane-Kurbeltrieb ist nicht umschaltbar.
