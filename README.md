# Tutaj możecie zgłaszać zmiany do konfiguracji. Kilka tych pliczków jest i czasami trochę trudno się połapać, ale wiem, że i tak dacie radę! :)

## skill_types.xml
Tutaj trzymane są akcje. Powiedzmy, że ktoś uważa, że za długo brukuje się drogę - szukamy "road"
~~~xml
<ability lvl="0" name="Stone Road" type="Build" id="65">
	<duration const="12 10"/>
	...
</ability>
<ability lvl="0" name="Slate Road" type="Build" id="310">
	<duration const="12 10"/>
	...
</ability>
<ability lvl="0" name="Marble Road" type="Build" id="311">
	<duration const="12 10"/>
	...
</ability>
~~~
widać od razu, że jest kilka opcji. 
Poprawimy więc w obu <duration const="12 10"/>. Pierwsza wartość to długość bazowa (w sekundach), a druga to obniżenie tego czasu o 1 sekundę per X skilla. 
W tym przypadku 12 - 1 * skill/10. Czyli budowanie drogi zabiera od 12 sekund do 2 sekund. 
Może przerobimy to? Powiedzmy 22 sekundy i obniżamy o 1 za każde 5 skilla? Wyjdzie nam bardziej płynny rozkład - 
~~~xml
<duration const="22 5"/>
~~~


Jest też możliwość, że będzie podana tam wartośc absolutna, tak jak np przy 
~~~xml
<ability lvl="30" name="Pull Out of the Kiln" type="Special" id="118">
				<duration const="">2</duration>
~~~
Tutaj sprawa jest prosta - 2 sekundy niezależnie od skilla
