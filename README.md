# Tutaj możecie zgłaszać zmiany do konfiguracji. Kilka tych pliczków jest i czasami trochę trudno się połapać, ale wiem, że i tak dacie radę! :)

## skill_types.xml
Tutaj trzymane są akcje. Powiedzmy, że ktoś uważa, że za długo brukuje się drogę - szukamy "road"
![image](https://user-images.githubusercontent.com/10631173/110626131-a2bd5680-81a0-11eb-8386-fe4205bed465.png)
widać od razu, że jest kilka opcji. 
Poprawimy więc w obu <duration const="12 10"/>. Pierwsza wartość to długość bazowa (w sekundach), a druga to obniżenie tego czasu o 1 sekundę per X skilla. 
W tym przypadku 12 - 1 * skill/10. Czyli budowanie drogi zabiera od 12 sekund do 2 sekund. 
Może przerobimy to? Powiedzmy 22 sekundy i obniżamy o 1 za każde 5 skilla? Wyjdzie nam bardziej płynny rozkład - 
~~~xml
<duration const="22 5"/>
~~~
Jest też możliwość, że będzie podana tam wartośc absolutna, tak jak np przy 
![image](https://user-images.githubusercontent.com/10631173/110626523-1d867180-81a1-11eb-97b6-6a4117695a00.png) 
Tutaj sprawa jest prosta - 2 sekundy niezależnie od skilla
